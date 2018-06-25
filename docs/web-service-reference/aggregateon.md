---
title: AggregateOn
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AggregateOn
api_type:
- schema
ms.assetid: 9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb
description: Das AggregateOn-Element darstellt, die Eigenschaft, die verwendet wird, um die Reihenfolge der gruppierten Elemente für eine gruppierte FindItem Resultset zu bestimmen.
ms.openlocfilehash: fe14de23e6a4c90d826200cae927427acfccc3c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757247"
---
# <a name="aggregateon"></a>AggregateOn

Das **AggregateOn** -Element darstellt, die Eigenschaft, die verwendet wird, um die Reihenfolge der gruppierten Elemente für eine gruppierte FindItem Resultset zu bestimmen. 
  
- [FindItem](finditem.md)  
- [GroupBy](groupby.md)
- [AggregateOn](aggregateon.md)
  
```xml
<AggregateOn>
   <FieldURI/>
</AggregateOn>
```

```xml
<AggregateOn>
   <IndexedFieldURI/>
</AggregateOn>
```

```xml
<AggregateOn>
   <ExtendedFieldURI/>
</AggregateOn>
```
 
**AggregateOnType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Aggregate** <br/> | Gibt den maximalen oder den minimalen Wert der Eigenschaft identifiziert durch das [FieldURI](fielduri.md) -Element, das für die Reihenfolge der Gruppen von Elementen verwendet wird.<br/><br/>Im Folgenden sind die möglichen Werte aufgeführt:  <br/><br/>-Minimum  <br/>-Maximum  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifiziert die Eigenschaften von URI häufig verwiesen wird.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Einzelne Elemente eines Wörterbuchs identifiziert.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Bezeichnet die extended MAPI-Eigenschaften zum Abrufen oder festlegen, oder erstellen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GroupBy](groupby.md) <br/> |Gibt beliebige Gruppen für FindItem Abfragen an.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:`/FindItem/GroupBy` <br/> |
   
## <a name="remarks"></a>Hinweise

Der [Vorgang FindItem](finditem-operation.md) können gruppierte Ergebnisse zurück. Innerhalb einer gruppierten Ergebnisse werden alle Elemente, die den gleichen Wert für einen bestimmten Gruppierungseigenschaft aufweisen zusammengefasst und als untergeordnete Elemente dieser Gruppe vorgelegt. Wenn Sie nach Absender gruppiert, sind beispielsweise alle E-mails organisiert, separate basierend auf in Gruppen, ob sie vom Absender A, B Absender usw. sind. Diese Gruppen sind untergeordnete Elemente der Gruppe der Absender. 
  
Jede dieser Gruppen innerhalb der Gruppe Absender enthält eine Auflistung von Elementen, wie die tatsächlichen e-Mail-Nachrichten, die von einem einzelnen Absender stammt. Sie können das [SortOrder](sortorder.md) -Element zum Sortieren der Elemente in einer Gruppe verwenden. Sortieren Sie die Eigenschaftswerte eines Elements auf der Grundlage Gruppen müssen Sie jedoch Aggregation verwenden. 
  
Mit Aggregation basiert die Reihenfolge der Gruppen auf eine bestimmte Eigenschaft der Elemente in der Gruppe. Wenn Sie zum Sortieren der Elemente in einer Gruppe Aggregation verwenden, müssen Sie eine repräsentative-Eigenschaft, um die Gruppen sortieren identifizieren. Das **AggregateOn** -Element können Sie die repräsentative-Eigenschaft angeben. 
  
Wenn eine repräsentative Eigenschaft identifiziert wird, wird das **aggregierte** Attribut verwendet, um anzugeben, ob die Gruppen nach die maximale oder den minimalen Wert der angegebenen Eigenschaft sortiert werden. Wenn das **Aggregate** -Attribut auf Maximum festgelegt ist, werden die Gruppen sortiert beginnend mit dem größten Wert für die **AggregateOn** -Eigenschaft. Wenn das **Aggregate** -Attribut auf mindestens festgelegt ist, werden die Gruppen sortiert beginnend mit dem kleinsten Wert für die **AggregateOn** -Eigenschaft. 
  
Angenommen, wenn Sie eine gruppierte Abfrage FindItem, ausstellen, Gruppieren nach Absender möchten, aber Sie die Gruppen, damit die Gruppe mit den neuesten e-Mail-Nachricht im Vordergrund ist bestellen möchten, Sie können Gruppieren nach Absender und Aggregat auf Datum/Uhrzeit mit **aggregierte** empfangen -Attribut des Maximum. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen gruppierten FindItem Anforderung und Antwort. Das Beispiel zeigt eine Anforderung zum Zurückgeben von Elementen, die von der **ConversationTopic** -Eigenschaft gruppiert. Zwei Gruppen, A und B werden in absteigender Reihenfolge basierend auf den Höchstwert der [DateTimeReceived](datetimereceived.md) -Eigenschaft zurückgegeben. 
  
```XML
<!-- EXAMPLE REQUEST -->
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="message:ConversationTopic"/>
          <t:FieldURI FieldURI="item:DateTimeReceived"/>
        </t:AdditionalProperties>    
      </ItemShape>
      <IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="20" Offset="0"/>
      <GroupBy Order="Ascending">
        <t:FieldURI FieldURI="message:ConversationTopic"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:DateTimeReceived"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
<!-- EXAMPLE RESPONSE -->
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="8" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Groups>
              <t:GroupedItems>
                <t:GroupIndex>B</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AQAnAH=" ChangeKey="CQAAABY" />
                    <t:DateTimeReceived>2006-09-14T23:59:18Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQAnAHR=" ChangeKey="CQAAAw" />
                    <t:DateTimeReceived>2006-09-15T00:00:24Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQAnA==" ChangeKey="CQAAJXT" />
                    <t:DateTimeReceived>2006-09-15T00:22:45Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
              <t:GroupedItems>
                <t:GroupIndex>A</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AQAnAAA==" ChangeKey="CQCJNe" />
                    <t:DateTimeReceived>2006-09-14T23:56:12Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQWgAA==" ChangeKey="CQAACJV6" />
                    <t:DateTimeReceived>2006-09-14T23:57:33Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAAA==" ChangeKey="CQA6CJXw" />
                    <t:DateTimeReceived>2006-09-15T00:23:31Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
            </t:Groups>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

Verwenden Sie zum Sortieren der Elemente in einer Gruppe das [SortOrder](sortorder.md) -Element ein. 
  
> [!NOTE]
> Die Element-IDs und Ändern von Schlüsseln wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Finding Items](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

