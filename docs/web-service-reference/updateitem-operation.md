---
title: UpdateItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4
description: Der Vorgang UpdateItem wird verwendet, um die Eigenschaften eines vorhandenen Elements im Exchange-Speicher zu ändern.
ms.openlocfilehash: 009ba16315017c4418fbd71d49744015c4d6d1b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839377"
---
# <a name="updateitem-operation"></a>UpdateItem Operation

Der Vorgang **UpdateItem** wird verwendet, um die Eigenschaften eines vorhandenen Elements im Exchange-Speicher zu ändern. 
  
## <a name="remarks"></a>Hinweise

Sie können drei grundlegende Update-Aktionen für ein Element ausführen. In der folgenden Tabelle sind die Aktionen aufgelistet, die Sie ausführen können.
  
|**Aktion**|**Beschreibung**|
|:-----|:-----|
|Anfügeabfrage  <br/> |Daten hinzugefügt auf eine vorhandene Eigenschaft. Diese Aktion wird die aktuellen Daten beibehalten. Fügen Sie gilt nicht für alle Eigenschaften.  <br/> |
|Gruppe  <br/> |Daten für eine Eigenschaft ersetzt, wenn die Eigenschaft Daten enthält, oder die Eigenschaft erstellt und legt deren Wert fest, wenn die Eigenschaft nicht vorhanden ist. Die Set-Aktion gilt nur für schreibbaren Eigenschaften.  <br/> |
|Löschen  <br/> |Entfernt eine Eigenschaft eines Elements. Dies unterscheidet sich von einer Eigenschaft auf einen leeren Wert festlegen. Wenn diese Aktion abgeschlossen ist, ist die Eigenschaft für das Element nicht vorhanden. Delete gilt nur für schreibbaren Eigenschaften.  <br/> |
   
Ein Aufruf **UpdateItem** kann verwendet werden, um ein oder mehrere Elemente und eine oder mehrere Eigenschaften für jedes Element zu ändern. Das [ItemChanges](itemchanges.md) -Element enthält alle Änderungen, die im Rahmen dieses Anrufs ausgeführt werden sollen. Das [ItemChange](itemchange.md) -Element ein untergeordnetes Element des Elements [ItemChanges](itemchanges.md) stellt die Änderungen in ein einzelnes Element ausgeführt werden. Das [ItemChange](itemchange.md) -Element enthält eine Reihe von Update-Aktionen, die für ein einzelnes Element ausgeführt werden kann. Diese Änderungen werden in der [Updates (Element)](updates-item.md) -Element enthalten. Das [ItemId](itemid.md) -Element identifiziert das Element zu aktualisieren. Um mehr als eine Eigenschaft für ein Element zu aktualisieren, muss ein [SetItemField](setitemfield.md), [AppendToItemField](appendtoitemfield.md)oder [DeleteItemField](deleteitemfield.md) für jede Eigenschaft angegeben werden, die das Update erforderlich sind. 
  
> [!NOTE]
> Update-Aktionen werden in der Reihenfolge angewendet, in denen sie angegeben sind. 
  
Für jede Änderung müssen Sie den Pfad der Eigenschaft, die geändert und einer Darstellung des betreffenden Elements mit den neuen Wert angeben. Die Löschaktion wird geringfügig, nur der Pfad der Eigenschaft, die gelöscht werden sollen, erforderlich sind. Für ein und Aktionen anfügen, der angegebenen Pfad muss verweisen auf dieselbe Eigenschaft, die in der Darstellung des Elements festgelegt wird. Wenn sich diese unterscheiden, wird ein Fehler zurückgegeben.
  
**UpdateItem** -Vorgang kann die Zeit [Start](start.md) und [End](end-ex15websvcsotherref.md) eines Exchange-Speicher-Elements festgelegt. In einer Anforderung **UpdateItem** kann [die Startzeit](start.md) festgelegt werden, ohne auch [die Endzeit](end-ex15websvcsotherref.md) festzulegen. Dies kann einen Fehler verursachen, wenn [die Startzeit](start.md) [die Endzeit](end-ex15websvcsotherref.md) liegt. Beachten Sie, dass Clientanwendungen [die Endzeit](end-ex15websvcsotherref.md) anpassen müssen, wenn [die Startzeit](start.md) geändert wird, um die Dauer beibehalten. 
  
Wenn ein einzelnes Kalenderelement ein wiederkehrendes master Kalenderelement vertraut aktualisiert wird, muss die [MeetingTimeZone](meetingtimezone.md) -Eigenschaft, um das Kalenderelement ursprüngliche Zeitzone beibehalten durch den Vorgang **UpdateItem** festgelegt werden. 
  
## <a name="setitemfield-request-example"></a>Anforderungsbeispiel SetItemField

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird einer Anforderung **UpdateItem** veranschaulicht, wie die Sensitivity-Eigenschaft für ein Element festgelegt. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkb..." ChangeKey="CQAAABYAAAB..."/>
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Sensitivity"/>
              <t:Message>
                <t:Sensitivity>Normal</t:Sensitivity>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.
  
### <a name="setitemfield-request-elements"></a>SetItemField Anforderung Elemente

In der Anforderung werden folgende Elemente verwendet:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Element)](updates-item.md)
    
- [SetItemField](setitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [Vertraulichkeit](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a>Anforderungsbeispiel AppendToItemField

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird einer Anforderung **UpdateItem** veranschaulicht, wie Text an die Body-Eigenschaft für ein Element angefügt. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYA..."/>
          <t:Updates>
            <t:AppendToItemField>
              <t:FieldURI FieldURI="item:Body"/>
              <t:Message>
                <t:Body BodyType="Text">Some additional text to append</t:Body>
              </t:Message>
            </t:AppendToItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Die folgenden Eigenschaften unterstützen die Append-Aktion:
  
- **Meldung: ReplyTo**
    
- **Textkörper:**
    
- Alle Empfänger und Teilnehmer-Auflistungseigenschaften
    
Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.
  
### <a name="appendtoitemfield-request-elements"></a>AppendToItemField Anforderung Elemente

In der Anforderung werden folgende Elemente verwendet:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Element)](updates-item.md)
    
- [AppendToItemField](appendtoitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [Body](body.md)
    
## <a name="deleteitemfield-request-example"></a>Anforderungsbeispiel DeleteItemField

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird einer Anforderung **UpdateItem** veranschaulicht, wie eine Eigenschaft für ein Element zu löschen. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbWluaXN0cm..." ChangeKey="CQAAABYAA..."/>
          <t:Updates>
            <t:DeleteItemField>
              <t:FieldURI FieldURI="item:Body"/>
            </t:DeleteItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.
  
### <a name="deleteitemfield-request-elements"></a>DeleteItemField Anforderung Elemente

In der Anforderung werden folgende Elemente verwendet:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Element)](updates-item.md)
    
- [DeleteItemField](deleteitemfield.md)
    
- [FieldURI](fielduri.md)
    
## <a name="successful-response-example"></a>Beispiel einer erfolgreichen Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **UpdateItem** . 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="664" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYAAA..."/>
            </t:Message>
          </m:Items>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </UpdateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.
  
### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateItemResponse](updateitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateItemResponseMessage](updateitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Elemente](items.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>Siehe auch



[UpdateItem-Vorgang (Aufgabe)](updateitem-operation-task.md)
  
[UpdateItem-Vorgang (Kontakt)](updateitem-operation-contact.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Aktualisierung von Kontakten](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Aktualisieren der Vorgänge](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

