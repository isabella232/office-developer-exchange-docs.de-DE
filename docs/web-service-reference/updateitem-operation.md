---
title: UpdateItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4
description: Der UpdateItem-Vorgang wird verwendet, um die Eigenschaften eines vorhandenen Elements im Exchange Speicher zu ändern.
ms.openlocfilehash: 6ac09c24c13efff8053fc605ec2c0e6cf2957429
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514060"
---
# <a name="updateitem-operation"></a>UpdateItem-Vorgang

Der **UpdateItem-Vorgang** wird verwendet, um die Eigenschaften eines vorhandenen Elements im Exchange Speicher zu ändern. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können drei grundlegende Aktualisierungsaktionen für ein Element ausführen. In der folgenden Tabelle sind die Aktionen aufgeführt, die Sie ausführen können.
  
|**Aktion**|**Beschreibung**|
|:-----|:-----|
|Anfügen  <br/> |Fügt einer vorhandenen Eigenschaft Daten hinzu. Diese Aktion behält die aktuellen Daten bei. Append gilt nicht für alle Eigenschaften.  <br/> |
|Satz  <br/> |Ersetzt Daten für eine Eigenschaft, wenn die Eigenschaft Daten enthält, oder erstellt die Eigenschaft und legt ihren Wert fest, wenn die Eigenschaft nicht vorhanden ist. Die Set-Aktion gilt nur für schreibbare Eigenschaften.  <br/> |
|Löschen  <br/> |Entfernt eine Eigenschaft aus einem Element. Dies unterscheidet sich vom Festlegen einer Eigenschaft auf einen leeren Wert. Wenn diese Aktion abgeschlossen ist, ist die Eigenschaft für das Element nicht vorhanden. Das Löschen gilt nur für beschreibbare Eigenschaften.  <br/> |
   
Ein **UpdateItem-Aufruf** kann verwendet werden, um ein oder mehrere Elemente und eine oder mehrere Eigenschaften für jedes Element zu ändern. Das [ItemChanges-Element](itemchanges.md) enthält alle Änderungen, die im Rahmen dieses Aufrufs ausgeführt werden sollen. Das [ItemChange-Element,](itemchange.md) ein untergeordnetes Element des [ItemChanges-Elements,](itemchanges.md) stellt die Änderungen dar, die für ein einzelnes Element ausgeführt werden sollen. Das [ItemChange-Element](itemchange.md) enthält eine Reihe von Aktualisierungsaktionen, die für ein einzelnes Element ausgeführt werden können. Diese Änderungen sind im [Element Updates (Element)](updates-item.md) enthalten. Das [ItemId-Element](itemid.md) identifiziert das zu aktualisierende Element. Um mehrere Eigenschaften für ein Element zu aktualisieren, muss für jede Eigenschaft, die die Aktualisierung erfordert, ein [SetItemField,](setitemfield.md) [AppendToItemField](appendtoitemfield.md)oder [DeleteItemField](deleteitemfield.md) bereitgestellt werden. 
  
> [!NOTE]
> Aktualisierungsaktionen werden in der Reihenfolge angewendet, in der sie angegeben sind. 
  
Für jede Änderung müssen Sie den Pfad der zu ändernden Eigenschaft und eine Darstellung dieses Elements mit seinem neuen Wert angeben. Die Löschaktion unterscheidet sich geringfügig dadurch, dass nur der Pfad der Eigenschaft erforderlich ist, die gelöscht werden soll. Bei Set- und Append-Aktionen muss sich der angegebene Pfad auf dieselbe Eigenschaft beziehen, die in der Elementdarstellung festgelegt wird. Wenn sich diese unterscheiden, wird ein Fehler zurückgegeben.
  
Der **UpdateItem-Vorgang** kann die [Start-](start.md) und [Endzeit](end-ex15websvcsotherref.md) eines Exchange Speicherelements festlegen. In einer **UpdateItem-Anforderung** kann die [Startzeit](start.md) festgelegt werden, ohne auch die [Endzeit](end-ex15websvcsotherref.md) festzulegen. Dies kann einen Fehler verursachen, wenn die [Startzeit](start.md) später als die [Endzeit ](end-ex15websvcsotherref.md) ist. Beachten Sie, dass Clientanwendungen die [Endzeit ](end-ex15websvcsotherref.md) anpassen müssen, wenn die [Startzeit](start.md) geändert wird, um die Dauer beizubehalten. 
  
Wenn ein einzelnes Kalenderelement aktualisiert wird, um ein wiederkehrendes Masterkalenderelement zu werden, muss die [MeetingTimeZone-Eigenschaft](meetingtimezone.md) durch den **UpdateItem-Vorgang** festgelegt werden, um die ursprüngliche Zeitzone des Kalenderelements beizubehalten. 
  
## <a name="setitemfield-request-example"></a>SetItemField-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer **UpdateItem-Anforderung** zeigt, wie die Vertraulichkeitseigenschaft für ein Element festgelegt wird. 
  
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

Der Elementbezeichner und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten.
  
### <a name="setitemfield-request-elements"></a>SetItemField-Anforderungselemente

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
    
## <a name="appendtoitemfield-request-example"></a>AppendToItemField-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer **UpdateItem-Anforderung** zeigt, wie Text an die Body-Eigenschaft eines Elements angefügt wird. 
  
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

Die folgenden Eigenschaften unterstützen die Anfügeaktion:
  
- **message:ReplyTo**
    
- **item:Body**
    
- Alle Empfänger- und Teilnehmersammlungseigenschaften
    
Der Elementbezeichner und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten.
  
### <a name="appendtoitemfield-request-elements"></a>AppendToItemField-Anforderungselemente

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
    
## <a name="deleteitemfield-request-example"></a>DeleteItemField-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer **UpdateItem-Anforderung** zeigt, wie eine Eigenschaft für ein Element gelöscht wird. 
  
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

Der Elementbezeichner und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten.
  
### <a name="deleteitemfield-request-elements"></a>DeleteItemField-Anforderungselemente

In der Anforderung werden folgende Elemente verwendet:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Element)](updates-item.md)
    
- [DeleteItemField](deleteitemfield.md)
    
- [FieldURI](fielduri.md)
    
## <a name="successful-response-example"></a>Beispiel für erfolgreiche Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **UpdateItem-Anforderung.** 
  
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

Der Elementbezeichner und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten.
  
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



[UpdateItem-Vorgang (Aufgabe)](updateitem-operation-task.md)
  
[UpdateItem-Vorgang (Kontakt)](updateitem-operation-contact.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Aktualisieren von Kontakten](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Aktualisieren von Aufgaben](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

