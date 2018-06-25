---
title: GetItem-Vorgang (Aufgabe)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: 8265dd06-1752-4470-8074-5f0e3e970f52
description: Die GetItem Operation wird verwendet, um Aufgaben aus dem Exchange-Speicher abzurufen.
ms.openlocfilehash: 412710f32ed8702e1a28a596833c3a7e47e3ed76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758724"
---
# <a name="getitem-operation-task"></a>GetItem-Vorgang (Aufgabe)

Die GetItem Operation wird verwendet, um Aufgaben aus dem Exchange-Speicher abzurufen.
  
## <a name="remarks"></a>Hinweise

Das Format der Anforderung GetItem für Aufgaben ist identisch mit GetItem für jeden anderen Elementtyp. Der einzige Unterschied ist, in denen zusätzliche Eigenschaften in der Antwort Form angefordert werden können. Zusätzlichen Eigenschaften muss entweder aufgabenbezogenen Eigenschaften oder erweiterte Eigenschaften.
  
## <a name="task-getitem-request-example"></a>Aufgabe GetItem-anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung GetItem zeigt, wie ein Aufgabenelement abgerufen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAtAEFkb..."/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

> [!NOTE]
> Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [GetItem](getitem.md)
    
- [ItemShape](itemshape.md)
    
- [BaseShape](baseshape.md)
    
- [Artikelnummern ein.](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="task-getitem-response-example"></a>Aufgabe GetItem antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung GetItem.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Task>
              <t:ItemId Id="AAAtAEA=" ChangeKey="EwAAAB"/>
              <t:ParentFolderId Id="AAAtAEFkbWl=" ChangeKey="AQAAAA=="/>
              <t:ItemClass>IPM.Task</t:ItemClass>
              <t:Subject>Buy new shoes</t:Subject>
              <t:Sensitivity>Normal</t:Sensitivity>
              <t:Body BodyType="Text"/>
              <t:DateTimeReceived>2006-09-15T15:23:08Z</t:DateTimeReceived>
              <t:Size>153</t:Size>
              <t:Importance>Normal</t:Importance>
              <t:IsSubmitted>false</t:IsSubmitted>
              <t:IsDraft>true</t:IsDraft>
              <t:IsFromMe>false</t:IsFromMe>
              <t:IsResend>false</t:IsResend>
              <t:IsUnmodified>false</t:IsUnmodified>
              <t:DateTimeSent>2006-09-15T15:23:08Z</t:DateTimeSent>
              <t:DateTimeCreated>2006-09-15T15:23:08Z</t:DateTimeCreated>
              <t:HasAttachments>false</t:HasAttachments>
              <t:Culture>en-US</t:Culture>
              <t:ChangeCount>1</t:ChangeCount>
              <t:IsComplete>false</t:IsComplete>
              <t:IsRecurring>false</t:IsRecurring>
              <t:PercentComplete>0</t:PercentComplete>
              <t:Status>NotStarted</t:Status>
              <t:StatusDescription>Not Started</t:StatusDescription>
            </t:Task>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

> [!NOTE]
> Das Element und Ordner-IDs und Ändern von Schlüsseln wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetItemResponse](getitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetItemResponseMessage](getitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Elemente](items.md)
    
- [Aufgabe](task.md)
    
- [ItemId](itemid.md)
    
- [ParentFolderId](parentfolderid.md)
    
- [ItemClass](itemclass.md)
    
- [Betreff](subject.md)
    
- [Vertraulichkeit](sensitivity.md)
    
- [Body](body.md)
    
- [DateTimeReceived](datetimereceived.md)
    
- [Size](size.md)
    
- [Importance](importance.md)
    
- [IsSubmitted](issubmitted.md)
    
- [IsDraft](isdraft.md)
    
- [IsFromMe](isfromme.md)
    
- [IsResend](isresend.md)
    
- [IsUnmodified](isunmodified.md)
    
- [DateTimeSent](datetimesent.md)
    
- ["Datetimecreated"](datetimecreated.md)
    
- [HasAttachments](hasattachments.md)
    
- [Kultur](culture.md)
    
- [ChangeCount](changecount.md)
    
- [IsComplete](iscomplete.md)
    
- [IsRecurring](isrecurring.md)
    
- [PercentComplete](percentcomplete.md)
    
- [Status](status.md)
    
- [StatusDescription](statusdescription.md)
    
## <a name="see-also"></a>Siehe auch



[GetItem Operation](getitem-operation.md)


[Erstellen von Aufgaben](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Aktualisieren der Vorgänge](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[Deleting Tasks](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

