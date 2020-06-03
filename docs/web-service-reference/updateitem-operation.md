---
title: UpdateItem-Vorgang
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
description: Der UpdateItem-Vorgang wird verwendet, um die Eigenschaften eines vorhandenen Elements in der Exchange-Informationsspeicher zu ändern.
ms.openlocfilehash: c001b7656862144023e9704cb04e6b4c0030f9df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459391"
---
# <a name="updateitem-operation"></a>UpdateItem-Vorgang

Der **UpdateItem** -Vorgang wird verwendet, um die Eigenschaften eines vorhandenen Elements in der Exchange-Informationsspeicher zu ändern. 
  
## <a name="remarks"></a>Bemerkungen

Sie können drei grundlegende Updateaktionen für ein Element durchführen. In der folgenden Tabelle sind die Aktionen aufgeführt, die Sie ausführen können.
  
|**Aktion**|**Beschreibung**|
|:-----|:-----|
|Append  <br/> |Fügt einer vorhandenen Eigenschaft Daten hinzu. Mit dieser Aktion werden die aktuellen Daten beibehalten. Append gilt nicht für alle Eigenschaften.  <br/> |
|Satz  <br/> |Ersetzt Daten für eine Eigenschaft, wenn die Eigenschaft Daten enthält, oder erstellt die Eigenschaft und legt den Wert fest, wenn die Eigenschaft nicht vorhanden ist. Die Aktion festlegen gilt nur für schreibbare Eigenschaften.  <br/> |
|Löschen  <br/> |Entfernt eine Eigenschaft aus einem Element. Dies unterscheidet sich vom Festlegen einer Eigenschaft auf einen leeren Wert. Wenn diese Aktion abgeschlossen ist, ist die Eigenschaft für das Element nicht vorhanden. DELETE gilt nur für schreibbare Eigenschaften.  <br/> |
   
Ein **UpdateItem** -Aufruf kann verwendet werden, um ein oder mehrere Elemente sowie eine oder mehrere Eigenschaften für jedes Element zu ändern. Das [ItemChanges](itemchanges.md) -Element enthält alle Änderungen, die im Rahmen dieses Aufrufs ausgeführt werden sollen. Das [ItemChange](itemchange.md) -Element, ein untergeordnetes Element des [ItemChanges](itemchanges.md) -Elements, stellt die Änderungen dar, die für ein einzelnes Element ausgeführt werden sollen. Das [ItemChange](itemchange.md) -Element enthält eine Reihe von Updateaktionen, die für ein einzelnes Element ausgeführt werden können. Diese Änderungen sind im Update Element [(Element)](updates-item.md) enthalten. Das Element [ItemID](itemid.md) identifiziert das Element, das aktualisiert werden soll. Wenn Sie mehr als eine Eigenschaft für ein Element aktualisieren möchten, muss für jede Eigenschaft, die das Update erfordert, ein [setitemfield](setitemfield.md), [AppendToItemField](appendtoitemfield.md)oder [DeleteItemField](deleteitemfield.md) angegeben werden. 
  
> [!NOTE]
> Update Aktionen werden in der Reihenfolge angewendet, in der Sie angegeben sind. 
  
Für jede Änderung müssen Sie den Pfad der zu ändernden Eigenschaft und eine Darstellung dieses Elements mit dem neuen Wert angeben. Die DELETE-Aktion unterscheidet sich geringfügig dadurch, dass nur der Pfad der zu löschenden Eigenschaft erforderlich ist. Bei Aktionen zum Festlegen und Anfügen muss der angegebene Pfad auf dieselbe Eigenschaft verwiesen werden, die in der Elementdarstellung festgelegt wird. Wenn sich diese unterscheiden, wird ein Fehler zurückgegeben.
  
Mit dem **UpdateItem** -Vorgang können die [Start](start.md) -und [Endzeit](end-ex15websvcsotherref.md) eines Exchange-Informationsspeicher Elements festgelegt werden. In einer **UpdateItem** -Anforderung kann die [Startzeit](start.md) festgelegt werden, ohne auch die [Endzeit](end-ex15websvcsotherref.md) festzulegen. Dies kann zu einem Fehler führen, wenn die [Startzeit](start.md) später als die [Endzeit](end-ex15websvcsotherref.md) ist. Beachten Sie, dass Clientanwendungen die [Endzeit](end-ex15websvcsotherref.md) anpassen müssen, wenn die [Startzeit](start.md) geändert wird, um die Dauer beizubehalten. 
  
Wenn ein einzelnes Kalenderelement als wiederkehrendes Master Kalenderelement aktualisiert wird, muss die [MeetingTimeZone](meetingtimezone.md) -Eigenschaft durch den **UpdateItem** -Vorgang festgelegt werden, um die ursprüngliche Zeitzone des Kalenderelements beizubehalten. 
  
## <a name="setitemfield-request-example"></a>Setitemfield-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer **UpdateItem** -Anforderung wird gezeigt, wie die Sensitivity-Eigenschaft für ein Element festgelegt wird. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>Comments

Die Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.
  
### <a name="setitemfield-request-elements"></a>Setitemfield-anforderungselemente

In der Anforderung werden folgende Elemente verwendet:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Element)](updates-item.md)
    
- [SetItemField](setitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [Meldung](message-ex15websvcsotherref.md)
    
- [Sensitivity](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a>AppendToItemField-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer **UpdateItem** -Anforderung wird gezeigt, wie Text an die Body-Eigenschaft eines Elements angefügt wird. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>Comments

Die folgenden Eigenschaften unterstützen die Append-Aktion:
  
- **message:ReplyTo**
    
- **Element: Body**
    
- Alle Eigenschaften Recipient und Attendee Collection
    
Die Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.
  
### <a name="appendtoitemfield-request-elements"></a>AppendToItemField-anforderungselemente

In der Anforderung werden folgende Elemente verwendet:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Element)](updates-item.md)
    
- [AppendToItemField](appendtoitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [Meldung](message-ex15websvcsotherref.md)
    
- [Body](body.md)
    
## <a name="deleteitemfield-request-example"></a>DeleteItemField-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer **UpdateItem** -Anforderung wird gezeigt, wie eine Eigenschaft für ein Element gelöscht wird. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>Comments

Die Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.
  
### <a name="deleteitemfield-request-elements"></a>DeleteItemField-anforderungselemente

In der Anforderung werden folgende Elemente verwendet:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Element)](updates-item.md)
    
- [DeleteItemField](deleteitemfield.md)
    
- [FieldURI](fielduri.md)
    
## <a name="successful-response-example"></a>Beispiel für eine erfolgreiche Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **UpdateItem** -Anforderung. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="664" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>Comments

Die Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

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



[UpdateItem-Vorgang (Vorgang)](updateitem-operation-task.md)
  
[UpdateItem-Vorgang (Kontakt)](updateitem-operation-contact.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Aktualisieren von Kontakten](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Aktualisieren von Aufgaben](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

