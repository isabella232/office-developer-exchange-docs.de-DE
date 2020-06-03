---
title: SyncFolderItems-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 7f0de089-8876-47ec-a871-df118ceae75d
description: Mit dem SyncFolderItems-Vorgang werden Elemente zwischen dem Exchange-Server und dem Client synchronisiert.
ms.openlocfilehash: 1a28d895eda11dd43f77ec2662a60a426cfc463c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468145"
---
# <a name="syncfolderitems-operation"></a>SyncFolderItems-Vorgang

Mit dem SyncFolderItems-Vorgang werden Elemente zwischen dem Exchange-Server und dem Client synchronisiert.
  
## <a name="remarks"></a>Bemerkungen

Der SyncFolderItems-Vorgang gibt maximal 512 Änderungen zurück. Nachfolgende SyncFolderItems-Anforderungen müssen durchgeführt werden, um weitere Änderungen zu erhalten. 
  
SyncFolderItems ähnelt dem FindItem-Vorgang insofern, als es keine Eigenschaften wie Body oder Attachments zurückgeben kann. Wenn der SyncFolderItems-Vorgang nicht die benötigten Eigenschaften zurückgibt, können Sie den [GetItem-Vorgang](getitem-operation.md) verwenden, um einen bestimmten Eigenschaftentyp für jedes Element abzurufen, das von SyncFolderItems zurückgegeben wurde. 
  
## <a name="syncfolderitems-request-example"></a>SyncFolderItems-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer SyncFolderItems-Anforderung wird gezeigt, wie Elemente in einem Ordner synchronisiert werden. In diesem Beispiel wird die Synchronisierung eines Ordnerelements gezeigt, bei der es sich nicht um die erste Synchronisierung handelt, die für den Ordner "Gesendete Elemente" aufgetreten ist. Das [von "SyncState](syncstate-ex15websvcsotherref.md) -Element ist nicht in der Anforderung für den ersten Versuch, einen Client mit dem Exchange-Server zu synchronisieren, enthalten. Beim ersten Versuch, die Elemente in einer Ordnerhierarchie zu synchronisieren, werden alle Elemente im Postfach zurückgegeben, ausgenommen Elemente, die im [Ignore](ignore.md) -Element angegeben sind. Diese SyncFolderItems-Anforderung versucht, alle Änderungen an den Ordnerelementen seit der letzten Synchronisierung zu synchronisieren. Bei dieser Anforderung wird der Versuch, das eine Element zu synchronisieren, das im [Ignore](ignore.md) -Element identifiziert wird, ignoriert. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SyncFolderItems xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>Default</t:BaseShape>
      </ItemShape>
      <SyncFolderId>
        <t:DistinguishedFolderId Id="sentitems"/>
      </SyncFolderId>
      <SyncState>AEbJ94eMOAAA=</SyncState>
      <Ignore>
        <t:ItemId Id="AQApAHRAA==" ChangeKey="CQAAABY"/>
      </Ignore>
      <MaxChangesReturned>100</MaxChangesReturned>
    </SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Die Base64-codierten Daten des [von "SyncState](syncstate-ex15websvcsotherref.md) -Elements und das [ItemID](itemid.md) -Element- **ID** -Attribut wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [SyncFolderItems](syncfolderitems.md)
    
- [ItemShape](itemshape.md)
    
- [BaseShape](baseshape.md)
    
- [SyncFolderId](syncfolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [Von "SyncState](syncstate-ex15websvcsotherref.md)
    
- [Ignore](ignore.md)
    
- [ItemId](itemid.md)
    
- [MaxChangesReturned](maxchangesreturned.md)
    
## <a name="successful-syncfolderitems-response"></a>Erfolgreiche SyncFolderItems-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die SyncFolderItems-Anforderung. In diesem Beispiel wird eine Besprechungsanfrage aus dem Ordner "Gesendete Elemente" synchronisiert.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAAAA=</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Create>
              <t:MeetingRequest>
                <t:ItemId Id="AQApAHRwA==" ChangeKey="CwAAABYA" />
                <t:Subject>Budget Q3</t:Subject>
                <t:Sensitivity>Normal</t:Sensitivity>
                <t:IsOutOfDate>false</t:IsOutOfDate>
                <t:HasBeenProcessed>true</t:HasBeenProcessed>
                <t:ResponseType>NoResponseReceived</t:ResponseType>
                <t:IntendedFreeBusyStatus>Busy</t:IntendedFreeBusyStatus>
                <t:Start>2006-08-02T17:30:00Z</t:Start>
                <t:End>2006-08-02T19:30:00Z</t:End>
                <t:Location>Conference Room 2</t:Location>
                <t:Organizer>
                  <t:Mailbox>
                    <t:Name>Dan Park</t:Name>
                    <t:EmailAddress>dpark@example.com</t:EmailAddress>
                    <t:RoutingType>SMTP</t:RoutingType>
                  </t:Mailbox>
                </t:Organizer>
              </t:MeetingRequest>
            </t:Create>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </SyncFolderItemsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Die Base64-codierten Daten des [von "SyncState](syncstate-ex15websvcsotherref.md) -Elements und das [ItemID](itemid.md) -Element- **ID** -Attribut wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SyncFolderItemsResponse](syncfolderitemsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Von "SyncState](syncstate-ex15websvcsotherref.md)
    
- [IncludesLastItemInRange](includeslastiteminrange.md)
    
- [Änderungen (Elemente)](changes-items.md)
    
- [Erstellen (ItemSync)](create-itemsync.md)
    
- [MeetingRequest](meetingrequest.md)
    
- [ItemId](itemid.md)
    
- [Betreff](subject.md)
    
- [Sensitivity](sensitivity.md)
    
- [IsOutOfDate](isoutofdate.md)
    
- [HasBeenProcessed](hasbeenprocessed.md)
    
- [ResponseType](responsetype.md)
    
- [IntendedFreeBusyStatus](intendedfreebusystatus.md)
    
- [Start](start.md)
    
- [End](end-ex15websvcsotherref.md)
    
- [Standort](location.md)
    
- [Organisator](organizer.md)
    
- [Postfach](mailbox.md)
    
- [Name (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [Routingtype (e-mailemailtype)](routingtype-emailaddresstype.md)
    
## <a name="syncfolderitems-error-response"></a>SyncFolderItems-Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine SyncFolderItems-Anforderung. Dieser Fehler wurde durch ein ungültiges von "SyncState verursacht.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Error">
          <m:MessageText>Synchronization state data is corrupt or otherwise invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidSyncStateData</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:SyncState />
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </SyncFolderItemsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SyncFolderItemsResponse](syncfolderitemsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Von "SyncState](syncstate-ex15websvcsotherref.md)
    
- [IncludesLastItemInRange](includeslastiteminrange.md)
    
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

