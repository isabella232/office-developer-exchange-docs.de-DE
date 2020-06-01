---
title: Synchronisieren von Ordnern unter Verwendung von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d3bbacd1-8e4b-4fd0-8d27-4cbbc045ec3f
description: Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um eine Liste der Ordner oder eine Liste von Ordnern abzurufen, die sich geändert haben, um den Client zu synchronisieren.
ms.openlocfilehash: e49fdaf2faf97c2369f2ad7dbb141c5ac3100884
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455863"
---
# <a name="synchronize-folders-by-using-ews-in-exchange"></a>Synchronisieren von Ordnern unter Verwendung von EWS in Exchange

Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um eine Liste der Ordner oder eine Liste von Ordnern abzurufen, die sich geändert haben, um den Client zu synchronisieren.
  
EWS in Exchange verwendet die Element Synchronisierung und die Ordnersynchronisierung zum Synchronisieren von Postfachinhalten zwischen dem Client und dem Server. Die Ordnersynchronisierung Ruft die anfängliche Liste der Ordner aus einem Stammordner ab und ruft dann im Laufe der Zeit Änderungen ab, die an diesen Ordnern vorgenommen wurden, und ruft auch neue Ordner ab.
  
Wenn Sie die Ordnersynchronisierung mit dem verwaltete EWS-API durchführen, erhalten Sie zunächst die erste [Liste der Ordner im Stammordner](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) mithilfe der [Datei "ExchangeService. SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) -Methode. Anschließend aktualisieren Sie den Wert des Parameters _cSyncState_ bei nachfolgenden Aufrufen, um die Liste der neuen und geänderten Ordner abzurufen. 
  
Um die Ordnersynchronisierung mithilfe von EWS durchzuführen, fordern Sie die [anfängliche Liste der Ordner im Stammordner](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) mithilfe des [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) -Vorgangs an, analysieren die Antwort und dann zu einem späteren Zeitpunkt [die Änderungen an den Ordnern im Stamm](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews)Verzeichnis und analysieren die Antwort. Nachdem der Client die Liste der anfänglichen oder geänderten Ordner empfangen hat, werden [Aktualisierungen lokal vorgenommen](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps). Wie und wann Sie Änderungen in der Zukunft abrufen, hängt vom [Synchronisierungs Entwurfsmuster](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) ab, das Ihre Anwendung verwendet. 
  
## <a name="get-the-list-of-all-folders-or-changed-folders-by-using-the-ews-managed-api"></a>Abrufen der Liste aller Ordner oder geänderten Ordner mithilfe der verwaltete EWS-API
<a name="bk_cesyncinitialewsma"> </a>

Im folgenden Codebeispiel wird gezeigt, wie eine anfängliche Liste von Ordnern in einem Stammordner abgerufen und dann eine Liste der Änderungen an Ordnern im Stammordner abgerufen wird, die seit der vorherigen Synchronisierung aufgetreten sind. Legen Sie beim ersten Aufruf der [Datei "ExchangeService. SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) -Methode den _cSyncState_ -Wert auf NULL fest. Wenn die Methode abgeschlossen ist, speichern Sie den _cSyncState_ -Wert lokal, um ihn im nächsten Aufruf der **SyncFolderHierarchy** -Methode zu verwenden. Sowohl in der ersten als auch in den nachfolgenden Aufrufen werden die Ordner mit aufeinanderfolgenden Aufrufen der **SyncFolderHierarchy** -Methode in Batches von zehn abgerufen, bis keine weiteren Änderungen mehr vorgenommen werden. In diesem Beispiel wird der _PropertySet-_ Parameter auf IdOnly festgelegt, um Aufrufe an die Exchange-Datenbank zu reduzieren, was eine [bewährte Synchronisierungsmethode](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)ist. In diesem Beispiel wird davon ausgegangen, dass **Dienst** eine gültige **Datei "ExchangeService** -Objektbindung ist und dass _cSyncState_ den Synchronisierungs Zustand darstellt, der von einem vorherigen Aufruf von **SyncFolderHierarchy**zurückgegeben wurde. 
  
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

Nachdem Sie die Liste der neuen oder geänderten Ordner auf dem Server abgerufen haben, [erstellen oder aktualisieren Sie die Ordner auf dem Client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).
  
## <a name="get-the-initial-list-of-folders-by-using-ews"></a>Abrufen der anfänglichen Liste der Ordner mithilfe von EWS
<a name="bk_cesyncewsrequest"> </a>

Das folgende Beispiel zeigt eine XML-Anforderung zum Abrufen der anfänglichen Ordnerhierarchie mithilfe des [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) -Vorgangs. Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn die [Liste der anfänglichen Ordner mithilfe der SyncFolderHierarchy-Methode abgerufen](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)wird. Das [von "SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) -Element des [SyncFolderHierarchy](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) -Vorgangs ist nicht enthalten, da dies die anfängliche Synchronisierung ist. In diesem Beispiel wird das [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Element auf **IdOnly** festgelegt, um Aufrufe an die Exchange-Datenbank zu reduzieren, was eine [bewährte Synchronisierungsmethode](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)ist.
  
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

Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) -Vorgangsanforderung verarbeitet wurde. Die anfängliche Antwort umfasst [Create](https://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) -Elemente für alle Ordner, da alle Ordner bei einer Erstsynchronisierung als neu betrachtet werden. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt, und einige **Create** -Elementblöcke wurden aus Gründen der Kürze entfernt. 
  
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

Nachdem Sie die Liste der neuen Ordner auf dem Server abgerufen haben, [Erstellen Sie die Ordner auf dem Client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a>Abrufen der Änderungen seit der letzten Synchronisierung mithilfe von EWS
<a name="bk_cesyncrespews"> </a>

Das folgende Beispiel zeigt die XML-Anforderung zum Abrufen der Liste der Änderungen an Ordnern im Stammordner mithilfe des [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) -Vorgangs. Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn [die Liste der Änderungen am Stammordner abgerufen](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)wird. In diesem Beispiel wird der Wert des [von "SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) -Elements auf den in der vorherigen Antwort zurückgegebenen Wert festgelegt. In diesem Beispiel wird das [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Element zu Demonstrationszwecken auf **allproperties** statt auf **IdOnly** festgelegt, um die zurückgegebenen zusätzlichen Eigenschaften anzuzeigen. Das Festlegen des [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Elements auf **IdOnly** ist eine [bewährte Methode](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)für die Synchronisierung. Der Wert von **von "SyncState** wurde zur Lesbarkeit gekürzt. 
  
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

Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die [SyncFolderHierarchy-Vorgangs](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) Anforderung vom Client verarbeitet wurde. Diese Antwort gibt an, dass ein Ordner aktualisiert wurde, ein Ordner erstellt wurde und ein Ordner seit der vorherigen Synchronisierung gelöscht wurde. Der Wert für das [von "SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) -Element, das **ID-** Attribut und das **ChangeKey** -Attribut wurde zur Lesbarkeit gekürzt. 
  
Beachten Sie, dass die Anforderung die **allproperties**-[BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)enthalten hat. Dies dient nur zu Demonstrationszwecken. Es wird empfohlen, das **BaseShape** -Element auf **IdOnly** in Production festzulegen. 
  
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

Wenn Sie die verwaltete EWS-API verwenden, nachdem Sie die Liste der neuen oder geänderten Ordner abgerufen haben, verwenden Sie die [Folder. Laden](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) -Methode, um Eigenschaften für die neuen oder geänderten Elemente abzurufen, die Eigenschaften mit den lokalen Werten zu vergleichen und die Ordner auf dem Client zu aktualisieren oder zu erstellen. 
  
Wenn Sie EWS verwenden, verwenden Sie den [GetFolder-Vorgang](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) , um Eigenschaften für die neuen oder geänderten Ordner abzurufen und die Ordner auf dem Client zu aktualisieren oder zu erstellen. 
  
## <a name="see-also"></a>Siehe auch

- [Postfachsynchronisierung und EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)   
- [Synchronisieren von Elementen unter Verwendung von EWS in Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)   
- [Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    

