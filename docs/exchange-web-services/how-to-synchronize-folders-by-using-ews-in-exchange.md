---
title: Synchronisieren von Ordnern unter Verwendung von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: d3bbacd1-8e4b-4fd0-8d27-4cbbc045ec3f
description: Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um eine Liste von Ordnern oder eine Liste von Ordnern abzurufen, die sich geändert haben, um Ihren Client zu synchronisieren.
ms.openlocfilehash: f22cb3b4ba92da9c044e08e7164d116293cf43ff
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521092"
---
# <a name="synchronize-folders-by-using-ews-in-exchange"></a>Synchronisieren von Ordnern unter Verwendung von EWS in Exchange

Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um eine Liste von Ordnern oder eine Liste von Ordnern abzurufen, die sich geändert haben, um Ihren Client zu synchronisieren.
  
EWS in Exchange verwendet die Elementsynchronisierung und Ordnersynchronisierung, um Postfachinhalte zwischen Client und Server zu synchronisieren. Die Ordnersynchronisierung ruft die anfängliche Liste der Ordner aus einem Stammordner ab und ruft dann im Laufe der Zeit Änderungen ab, die an diesen Ordnern vorgenommen wurden, und ruft auch neue Ordner ab.
  
Wenn Sie die Ordnersynchronisierung mithilfe der verwalteten EWS-API durchführen, rufen Sie zunächst [die anfängliche Liste der Ordner im Stammordner](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) mithilfe der [ExchangeService.SyncFolderHierarchy-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) ab. Anschließend aktualisieren Sie den Wert des  _cSyncState-Parameters_ bei nachfolgenden Aufrufen, um die Liste der neuen und geänderten Ordner abzurufen. 
  
Um die Ordnersynchronisierung mithilfe von EWS durchzuführen, fordern Sie die [anfängliche Liste der Ordner im Stammordner](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) mithilfe des [SyncFolderHierarchy-Vorgangs](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) an, analysieren die Antwort und rufen dann zu einem späteren Zeitpunkt [die Änderungen an den Ordnern im Stammverzeichnis](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews)ab und analysieren die Antwort. Nachdem der Client die Liste der anfänglichen oder geänderten Ordner erhalten hat, [werden Updates lokal vorgenommen.](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps) Wie und wann Sie änderungen in der Zukunft abrufen, hängt vom [Synchronisierungsentwurfsmuster](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) ab, das Ihre Anwendung verwendet. 
  
## <a name="get-the-list-of-all-folders-or-changed-folders-by-using-the-ews-managed-api"></a>Abrufen der Liste aller Ordner oder geänderter Ordner mithilfe der verwalteten EWS-API
<a name="bk_cesyncinitialewsma"> </a>

Das folgende Codebeispiel zeigt, wie Sie eine anfängliche Liste von Ordnern in einem Stammordner abrufen und dann eine Liste der Änderungen an Ordnern im Stammordner abrufen, die seit der vorherigen Synchronisierung aufgetreten sind. Legen Sie während des anfänglichen Aufrufs der [ExchangeService.SyncFolderHierarchy-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) den  _cSyncState-Wert_ auf NULL fest. Speichern Sie nach Abschluss der Methode den  _cSyncState-Wert_ lokal, um ihn im nächsten **SyncFolderHierarchy-Methodenaufruf** zu verwenden. Sowohl beim anfänglichen Aufruf als auch bei den nachfolgenden Aufrufen werden die Ordner in Batches von zehn abgerufen, indem aufeinanderfolgende Aufrufe der **SyncFolderHierarchy-Methode** verwendet werden, bis keine weiteren Änderungen verbleiben. In diesem Beispiel wird der _parameter propertySet_ auf IdOnly festgelegt, um Aufrufe der Exchange Datenbank zu reduzieren, was eine bewährte Methode für die [Synchronisierung](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)ist. In diesem Beispiel wird davon ausgegangen, dass **der Dienst** eine gültige **ExchangeService-Objektbindung** ist und dass cSyncState den  _Synchronisierungsstatus_ darstellt, der von einem vorherigen Aufruf von **SyncFolderHierarchy** zurückgegeben wurde. 
  
```cs
// Get a list of all folders in the mailbox by calling SyncFolderHierarchy.
// The folderId parameter must be set to the root folder to synchronize. 
// The propertySet parameter is set to IdOnly to reduce calls to the Exchange database
// because any additional properties result in additional calls to the Exchange database. 
// The syncState parameter is set to cSyncState, which should be null in the initial call, 
// and should be set to the sync state returned by the previous SyncFolderHierarchy call 
// in subsequent calls.
ChangeCollection<FolderChange> fcc = service.SyncFolderHierarchy(new FolderId(WellKnownFolderName.Root), PropertySet.IdOnly, cSyncState);
// If the count of changes is zero, there are no changes to synchronize.
if (fcc.Count == 0)
{
    Console.WriteLine("There are no folders to synchronize.");
}
// Otherwise, write all the changes included in the response 
// to the console. 
// For the initial synchronization, all the changes will be of type
// ChangeType.Create.
else
{
    foreach (FolderChange fc in fcc)
    {
        Console.WriteLine("ChangeType: " + fc.ChangeType.ToString());
        Console.WriteLine("FolderId: " + fc.FolderId);
        Console.WriteLine("===========");
    }
}
// Save the sync state for use in future SyncFolderItems requests.
// The sync state is used by the server to determine what changes to report
// to the client.
string fSyncState = fcc.SyncState;

```

Nachdem Sie die Liste der neuen oder geänderten Ordner auf dem Server abgerufen haben, erstellen oder aktualisieren Sie [die Ordner auf dem Client.](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)
  
## <a name="get-the-initial-list-of-folders-by-using-ews"></a>Abrufen der anfänglichen Liste von Ordnern mithilfe von EWS
<a name="bk_cesyncewsrequest"> </a>

Das folgende Beispiel zeigt eine XML-Anforderung zum Abrufen der anfänglichen Ordnerhierarchie mithilfe des [SyncFolderHierarchy-Vorgangs.](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn [die Liste der ursprünglichen Ordner mithilfe der SyncFolderHierarchy -Methode abgerufen](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)wird. Das [SyncState-Element](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) des [SyncFolderHierarchy-Vorgangs](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) ist nicht enthalten, da dies die erste Synchronisierung ist. In diesem Beispiel wird das [BaseShape-Element](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) auf **IdOnly** festgelegt, um Aufrufe der Exchange Datenbank zu reduzieren, was eine bewährte Methode für die [Synchronisierung](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)ist.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:SyncFolderHierarchy>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="root" />
      </m:SyncFolderId>
    </m:SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die [SyncFolderHierarchy-Vorgangsanforderung](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) verarbeitet wurde. Die erste Antwort enthält [Create-Elemente](https://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) für alle Ordner, da alle Ordner während einer ersten Synchronisierung als neu betrachtet werden. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt, und einige **Create-Elementblöcke** wurden aus Platzgründen entfernt. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                   xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAA==</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADM="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADMzM="
                            ChangeKey="AQAAABY"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkAD/AAA="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADBh="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            ...
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderHierarchyResponse>
  </s:Body>
</s:Envelope>
```

Nachdem Sie die Liste der neuen Ordner auf dem Server abgerufen haben, [erstellen Sie die Ordner auf dem Client.](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a>Abrufen der Änderungen seit der letzten Synchronisierung mithilfe von EWS
<a name="bk_cesyncrespews"> </a>

Das folgende Beispiel zeigt die XML-Anforderung zum Abrufen der Liste der Änderungen an Ordnern im Stammordner mithilfe des [SyncFolderHierarchy-Vorgangs.](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn [die Liste der Änderungen an den Stammordner abgerufen](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)wird. In diesem Beispiel wird der [SyncState-Elementwert](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) auf den in der vorherigen Antwort zurückgegebenen Wert festgelegt. Zu Demonstrationszwecken wird in diesem Beispiel das [BaseShape-Element](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) auf **AllProperties** anstelle von **IdOnly** festgelegt, um die zurückgegebenen zusätzlichen Eigenschaften anzuzeigen. Das Festlegen des [BaseShape-Elements](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) auf **IdOnly** ist eine bewährte Methode für [die Synchronisierung.](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices) Der Wert von **SyncState** wurde zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:SyncFolderHierarchy>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="root" />
      </m:SyncFolderId>
      <m:SyncState>H4sIAA==</m:SyncState>
    </m:SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die [SyncFolderHierarchy-Vorgangsanforderung](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) vom Client verarbeitet wurde. Diese Antwort gibt an, dass ein Ordner aktualisiert, ein Ordner erstellt und ein Ordner seit der vorherigen Synchronisierung gelöscht wurde. Der Wert des [SyncState-Elements,](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) **der ID-Attribute** und der **ChangeKey-Attribute** wurde zur besseren Lesbarkeit gekürzt. 
  
Denken Sie daran, dass die Anforderung die **AllProperties-BaseShape**[](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)enthielt. Dies dient nur zu Demonstrationszwecken. Es wird empfohlen, das **BaseShape-Element** in der Produktion auf **"IdOnly"** festzulegen. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
<h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="745" MinorBuildNumber="21" Version="V2_3" 
           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Update>
              <t:Folder>
                <t:FolderId Id="AAMkADM=" ChangeKey="AQAAABY" />
                <t:ParentFolderId Id="AQMkADMzADI1==" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>Meeting Notes</t:DisplayName>
                <t:TotalCount>3</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:EffectiveRights>
                  <t:CreateAssociated>true</t:CreateAssociated>
                  <t:CreateContents>true</t:CreateContents>
                  <t:CreateHierarchy>true</t:CreateHierarchy>
                  <t:Delete>true</t:Delete>
                  <t:Modify>true</t:Modify>
                  <t:Read>true</t:Read>
                  <t:ViewPrivateItems>true</t:ViewPrivateItems>
                </t:EffectiveRights>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Update>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADMzM=" ChangeKey="AQAAABYAA" />
                <t:ParentFolderId Id="AQMkO67A==" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>Schedules</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:EffectiveRights>
                  <t:CreateAssociated>true</t:CreateAssociated>
                  <t:CreateContents>true</t:CreateContents>
                  <t:CreateHierarchy>true</t:CreateHierarchy>
                  <t:Delete>true</t:Delete>
                  <t:Modify>true</t:Modify>
                  <t:Read>true</t:Read>
                  <t:ViewPrivateItems>true</t:ViewPrivateItems>
                </t:EffectiveRights>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Create>
            <t:Delete>
              <t:FolderId Id="AAMkAD/AAA=" ChangeKey="AQAAAA==" />
            </t:Delete>
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderHierarchyResponse>
  </s:Body>
</s:Envelope>

```

## <a name="update-the-client"></a>Aktualisieren des Clients
<a name="bk_nextsteps"> </a>

Wenn Sie die verwaltete EWS-API verwenden, verwenden Sie nach dem Abrufen der Liste der neuen oder geänderten Ordner die [Folder.Load-Methode,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) um Eigenschaften für die neuen oder geänderten Elemente abzurufen, die Eigenschaften mit den lokalen Werten zu vergleichen und die Ordner auf dem Client zu aktualisieren oder zu erstellen. 
  
Wenn Sie EWS verwenden, verwenden Sie den [GetFolder-Vorgang,](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) um Eigenschaften für die neuen oder geänderten Ordner abzurufen und die Ordner auf dem Client zu aktualisieren oder zu erstellen. 
  
## <a name="see-also"></a>Siehe auch

- [Postfachsynchronisierung und EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)   
- [Synchronisieren von Elementen unter Verwendung von EWS in Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)   
- [Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    

