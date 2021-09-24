---
title: Synchronisieren von Elementen unter Verwendung von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 886e7d35-9096-480b-8a8c-a7db27da06c2
description: Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um eine Liste aller Elemente in einem Ordner oder eine Liste der Änderungen abzurufen, die in einem Ordner aufgetreten sind, um Ihren Client zu synchronisieren.
ms.openlocfilehash: 82d9304f4060583a5bbffdcf4020c5822ab7c006
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513080"
---
# <a name="synchronize-items-by-using-ews-in-exchange"></a>Synchronisieren von Elementen unter Verwendung von EWS in Exchange

Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um eine Liste aller Elemente in einem Ordner oder eine Liste der Änderungen abzurufen, die in einem Ordner aufgetreten sind, um Ihren Client zu synchronisieren.
  
EWS in Exchange verwendet die Elementsynchronisierung und Ordnersynchronisierung, um Postfachinhalte zwischen Client und Server zu synchronisieren. Die Elementsynchronisierung ruft die anfängliche Liste der Elemente in einem Ordner ab und ruft dann im Laufe der Zeit Änderungen ab, die an diesen Elementen vorgenommen wurden, und ruft auch neue Elemente ab.
  
Beachten Sie, dass Sie zuerst die [Ordnerhierarchie synchronisieren](how-to-synchronize-folders-by-using-ews-in-exchange.md)müssen, bevor Sie Elemente mit einem Client synchronisieren können. Nachdem die Ordnerhierarchie auf dem Client eingerichtet wurde, rufen Sie, wenn Sie die Elementsynchronisierung mithilfe der verwalteten EWS-API durchführen, zuerst [die anfängliche Liste der Elemente im Posteingang](#bk_cesyncongoingewsma) mithilfe der [ExchangeService.SyncFolderItems-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) ab. Anschließend aktualisieren Sie den Wert des  _cSyncState-Parameters_ bei nachfolgenden Aufrufen, um die Liste der geänderten Elemente im Posteingang abzurufen. 
  
Um die Elementsynchronisierung mithilfe von EWS durchzuführen, fordern Sie nach [dem Synchronisieren der Ordnerhierarchie](how-to-synchronize-folders-by-using-ews-in-exchange.md)die [anfängliche Liste der Elemente im Posteingang](#bk_ewsexamplea) mithilfe des [SyncFolderItems-Vorgangs](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)an, analysieren die Antwort und rufen dann zu einem bestimmten Zeitpunkt in der Zukunft [die Änderungen an den Elementen im Postfach](#bk_ewsexamplec)ab und analysieren die Antwort. Nachdem der Client die Liste der anfänglichen oder geänderten Elemente erhalten hat, nimmt er [lokal Updates vor.](#bk_nextsteps) Wie und wann Sie änderungen in der Zukunft abrufen, hängt vom [Synchronisierungsentwurfsmuster](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) ab, das Ihre Anwendung verwendet. 
  
## <a name="get-the-list-of-all-items-or-changed-items-by-using-the-ews-managed-api"></a>Abrufen der Liste aller Elemente oder geänderten Elemente mithilfe der verwalteten EWS-API
<a name="bk_cesyncongoingewsma"> </a>

Das folgende Codebeispiel zeigt, wie Sie eine anfängliche Liste aller Elemente im Ordner Posteingang abrufen und dann eine Liste der Änderungen an Elementen im Posteingangsordner abrufen, die seit der vorherigen Synchronisierung aufgetreten sind. Legen Sie während des anfänglichen Aufrufs der [SyncFolderItems-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) den  _cSyncState-Wert_ auf NULL fest. Wenn die Methode abgeschlossen ist, speichern Sie den  _cSyncState-Wert_ lokal, um ihn im nächsten **SyncFolderItems-Methodenaufruf** zu verwenden. Sowohl beim anfänglichen Aufruf als auch bei den nachfolgenden Aufrufen werden die Elemente in Batches von zehn abgerufen, indem aufeinanderfolgende Aufrufe der **SyncFolderItems-Methode** verwendet werden, bis keine weiteren Änderungen verbleiben. 
  
In diesem Beispiel wird der _parameter propertySet_ auf IdOnly festgelegt, um Aufrufe der Exchange Datenbank zu reduzieren, was eine bewährte Methode für die [Synchronisierung](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)ist. In diesem Beispiel wird davon ausgegangen, dass **der Dienst** eine gültige **ExchangeService-Objektbindung** ist und dass cSyncState den  _Synchronisierungsstatus_ darstellt, der von einem vorherigen Aufruf von **SyncFolderItems** zurückgegeben wurde. 
  
```cs
// Track whether there are more items available for download on the server.
bool moreChangesAvailable = false;
do
{
    // Get a list of all items in the Inbox by calling SyncFolderHierarchy repeatedly until no more changes are available.
    // The folderId parameter must be set to the root folder to synchronize,
    // and must be same folder ID as used in previous synchronization calls. 
    // The propertySet parameter is set to IdOnly to reduce calls to the Exchange database,
    // because any additional properties result in additional calls to the Exchange database. 
    // The ignoredItemIds parameter is set to null, so that no items are ignored.
    // The maxChangesReturned parameter is set to return a maximum of 10 items (512 is the maximum).
    // The syncScope parameter is set to Normal items, so that associated items will not be returned.
    // The syncState parameter is set to cSyncState, which should be null in the initial call, 
    // and should be set to the sync state returned by the 
    // previous SyncFolderItems call in subsequent calls.
    ChangeCollection<ItemChange> icc = service.SyncFolderItems(new FolderId(WellKnownFolderName.Inbox), PropertySet.IdOnly, null, 10, SyncFolderItemsScope.NormalItems, cSyncState);
    // If the count of changes is zero, there are no changes to synchronize.
    if (icc.Count == 0)
    {
        Console.WriteLine("There are no item changes to synchronize.");
    }
    // Otherwise, write all the changes included in the response 
    // to the console. 
    else
    {
        foreach (ItemChange ic in icc)
        {
            Console.WriteLine("ChangeType: " + ic.ChangeType.ToString());
            Console.WriteLine("ItemId: " + ic.ItemId);
            Console.WriteLine("===========");
        }
    }
    // Save the sync state for use in future SyncFolderContent requests.
    // The sync state is used by the server to determine what changes to report
    // to the client.
    string sSyncState = icc.SyncState;
   // Determine whether more changes are available on the server.
   moreChangesAvailable = icc.MoreChangesAvailable;
}
while (moreChangesAvailable);

```

Die **SyncFolderItems** -Methode ähnelt der [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methode, da sie keine Eigenschaften wie [Body](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) oder [Attachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx)zurückgeben kann. Wenn Sie Eigenschaften benötigen, die von der **SyncFolderItems-Methode** nicht zurückgegeben werden können, geben Sie den [IdOnly-Eigenschaftensatz](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset.idonly%28v=exchg.80%29.aspx) beim Aufrufen von **SyncFolderItems** an, und verwenden Sie dann die [ExchangeService.LoadPropertiesForItems-Methode,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) um die Eigenschaften abzurufen, die Sie für die elemente benötigen, die von der **SyncFolderItems-Methode** zurückgegeben wurden. 
  
Nachdem Sie die Liste der neuen oder geänderten Elemente auf dem Server abgerufen haben, erstellen oder aktualisieren Sie [die Elemente auf dem Client.](#bk_nextsteps)
  
## <a name="get-the-initial-list-of-items-by-using-ews"></a>Abrufen der anfänglichen Liste von Elementen mithilfe von EWS
<a name="bk_ewsexamplea"> </a>

Das folgende Beispiel zeigt die XML-Anforderung zum Abrufen der anfänglichen Liste der Elemente im Posteingang mithilfe des [SyncFolderItems-Vorgangs.](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn [die Liste der Elemente mithilfe der SyncFolderItems-Methode abgerufen](#bk_cesyncongoingewsma)wird. Das [SyncState-Element](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) des **SyncFolderItems-Vorgangs** ist nicht enthalten, da dies die erste Synchronisierung ist. In diesem Beispiel wird das [BaseShape-Element](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) auf **IdOnly** festgelegt, um Aufrufe der Exchange Datenbank zu reduzieren, was eine bewährte Methode für die [Synchronisierung](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)ist.
  
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
    <m:SyncFolderItems>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:ItemShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:SyncFolderId>
      <m:MaxChangesReturned>10</m:MaxChangesReturned>
      <m:SyncScope>NormalItems</m:SyncScope>
    </m:SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

<a name="bk_responsesyncfolderitems"> </a>

Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die **SyncFolderItems-Vorgangsanforderung** vom Client verarbeitet wurde. Die erste Antwort enthält [Create-Elemente](https://msdn.microsoft.com/library/cb5e64a2-66a5-4447-921e-7c13efb8f6bf%28Office.15%29.aspx) für fünf Elemente, da alle Elemente während einer ersten Synchronisierung als neu betrachtet werden. Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
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
    <m:SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA==</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q04QAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdC"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q07AAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdB"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q1AwAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdA"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AAMkADBh=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVc5"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AAMkADBh=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVc4"/>
              </t:Message>
            </t:Create>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderItemsResponse>
  </s:Body>
</s:Envelope>
```

Nachdem Sie die Liste der neuen Elemente auf dem Server abgerufen haben, [erstellen Sie die Elemente auf dem Client.](#bk_nextsteps)
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a>Abrufen der Änderungen seit der letzten Synchronisierung mithilfe von EWS
<a name="bk_ewsexamplec"> </a>

Das folgende Beispiel zeigt die XML-Anforderung zum Abrufen der Liste der Änderungen an Elementen im Posteingang mithilfe des [SyncFolderItems-Vorgangs.](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn [die Liste der Änderungen an den Posteingang abgerufen](#bk_cesyncongoingewsma)wird. In diesem Beispiel wird der [SyncState-Elementwert](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) auf den Wert festgelegt, der in der [vorherigen Antwort](#bk_responsesyncfolderitems)zurückgegeben wurde. Zu Demonstrationszwecken wird in diesem Beispiel das [BaseShape-Element](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) auf **AllProperties** anstelle von **IdOnly** festgelegt, um die zurückgegebenen zusätzlichen Eigenschaften anzuzeigen. Das Festlegen des [BaseShape-Elements](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) auf **IdOnly** ist eine bewährte Methode für [die Synchronisierung.](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices) Der Wert von **SyncState** wurde zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
      <t:RequestServerVersion Version="Exchange2010_SP2" />
  </soap:Header>
  <soap:Body>
    <m:SyncFolderItems>
      <m:ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:ItemShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:SyncFolderId>
      <m:SyncState>H4sIAAA==</m:SyncState>
      <m:MaxChangesReturned>10</m:MaxChangesReturned>
      <m:SyncScope>NormalItems</m:SyncScope>
    </m:SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die **SyncFolderItems-Vorgangsanforderung** vom Client verarbeitet wurde. Diese Antwort gibt an, dass ein Element aktualisiert wurde, zwei Elemente erstellt wurden, das Lesekennzeichen eines Elements geändert wurde und ein Element seit der vorherigen Synchronisierung gelöscht wurde. Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3"
                 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                 xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAAAAAAEAO29B2AcSZY==</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Update>
                <t:Message>
                  <t:ItemId Id="q04QAAAA==" ChangeKey="CQAAABYAAADZGACZQpSgSpyNkexYe2b7AAAAird/" />
                  <t:ParentFolderId Id=" AgENAAAA" ChangeKey="AQAAAA==" />
                  <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Company Soccer Team</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T15:22:10Z</t:DateTimeReceived>
                  <t:Size>23110</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;8e084ea1a5b64f97b95fa8a863a5869d@CH1SR01MB001.namsdf01.sdf.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T15:22:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:38Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>All Employees</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara  Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T16:53:35Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQACAi+NTh0F5Eg5YDwpJsXPE=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Alfred  Welker </t:Name>
                      <t:EmailAddress>Alfred.Welker@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5V/ZICL41OHQXkSDlgPCkmxc8ZYxA3I4gAAP5UeAANHpbIAAEE+0gAABYhSAACGYTIAAA2+vgAAE81qAkhv0Eg==</t:ConversationIndex>
                  <t:ConversationTopic>Company Soccer Team</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Alfred  Welker </t:Name>
                      <t:EmailAddress>Alfred.Welker@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;e5919a09c8fc4d64b6ffd3542e194fc3@BY2SR01MB609.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>namsdf01.sdf.contoso.com&amp;gt;</t:References>
                </t:Message>
            </t:Update>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AQMkAD+" />
                <t:ParentFolderId Id="AQMkA==" ChangeKey="AQAAAA==" />
                <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Review Proposal for Contoso</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T16:20:10Z</t:DateTimeReceived>
                  <t:Size>32515</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;e52a4de6b98d484887e141da094a2ce6@SN2SR01MB006.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T16:20:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:33Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>Legal Team; Executives</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara  Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T04:07:35Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQAIsBEZp25UpElByLLUQFH6Q=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Hope Gross</t:Name>
                      <t:EmailAddress>Hope.Gross@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5WBRiwERmnblSkSUHIstRAUfpJYw9fbSgAAAdm2AAAB6koAAAHTDgAADl6+AAAbxCYAABm5PgAACSA+AANx034AAEKGQgAAAfsiAAB7m3IAABG+ngAABPZyAAASUzoAAA2DNgAAAfKE=</t:ConversationIndex>
                  <t:ConversationTopic>Review Proposal for Contoso</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Hope Gross</t:Name>
                      <t:EmailAddress>Hope.Gross@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;bcdb185495834370a874a1e7ebedbb96@SN2SR01MB005.namsdf01.sdf.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>&amp;lt;2d4d7d…</t:References>
                </t:Message>
              </t:Create>
              <t:Create>
                <t:Message>
                  <t:ItemId Id="Q04AAAAA==" ChangeKey="AAAirbnd" />
                  <t:ParentFolderId Id="AgENAAAA" ChangeKey="AQAAAA==" />
                  <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Review Proposal for Contoso</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T15:30:10Z</t:DateTimeReceived>
                  <t:Size>29518</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;f0db3ead01db4fe087d98022149aa16f@SN2SR01MB001.namsdf01.sdf.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T15:30:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:36Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>Legal Team; Executives</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T04:07:38Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQAIsBEZp25UpElByLLUQFH6Q=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Mack Chaves</t:Name>
                      <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5WBRiwERmnblSkSUHIstRAUfpJYw9fbSgAAAdm2AAAB6koAAAHTDgAADl6+AAAbxCYAABm5PgAACSA+AANx034AAEKGQgAAAfsiAAB7m3IAABG+ngAABPZyAAASUzoAAA2DN</t:ConversationIndex>
                  <t:ConversationTopic>Review Proposal for Contoso</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Mack Chaves</t:Name>
                      <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;e52a4de6b98d484887e141da094a2ce6@SN2SR01MB006.namsdf01.sdf.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>namsdf01.sdf.contoso.com&amp;gt;</t:References>
                </t:Message>
              </t:Create>
              <t:ReadFlagChange>
                <t:ItemId Id=" q07AAAAA==" ChangeKey="CQAAAA==" />
                <t:IsRead>true</t:IsRead>
              </t:ReadFlagChange>
              <t:Delete>
                <t:ItemId Id=" q1AwAAAA==" ChangeKey="CQAAAA==" />
              </t:Delete>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderItemsResponse>
  </s:Body>
</s:Envelope>
```

Der **SyncFolderItems-Vorgang** ähnelt der [FindItems-Methode,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) da er keine Elemente wie die Elemente ["Body"](https://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) oder ["Attachments"](https://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) zurückgeben kann. Wenn Sie Eigenschaften benötigen, die vom **SyncFolderItems-Vorgang** nicht zurückgegeben werden können, legen Sie den Wert des [BaseShape-Elements](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) auf IdOnly fest, wenn Sie **SyncFolderItems** aufrufen, und verwenden Sie dann den [GetItem-Vorgang,](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) um die Eigenschaften abzurufen, die Sie für die Elemente benötigen, die vom **SyncFolderItems-Vorgang** zurückgegeben wurden. 
  
Nachdem Sie die Liste der geänderten Elemente auf dem Server abgerufen haben, [aktualisieren Sie die Elemente auf dem Client.](#bk_nextsteps)
  
## <a name="update-the-client"></a>Aktualisieren des Clients
<a name="bk_nextsteps"> </a>

Wenn Sie die verwaltete EWS-API verwenden, verwenden Sie nach dem Abrufen der Liste neuer oder geänderter Elemente die [LoadPropertiesForItems-Methode,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) um Eigenschaften für die neuen oder geänderten Elemente abzurufen, die Eigenschaften mit den lokalen Werten zu vergleichen und die Elemente auf dem Client zu aktualisieren. 
  
Wenn Sie EWS verwenden, verwenden Sie den [GetItem-Vorgang,](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) um Eigenschaften für die neuen oder geänderten Elemente abzurufen und die Elemente auf dem Client zu aktualisieren. 
  
## <a name="see-also"></a>Siehe auch


- [Postfachsynchronisierung und EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    
- [Synchronisieren von Ordnern unter Verwendung von EWS in Exchange](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    

