---
title: AggregateOn
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AggregateOn
api_type:
- schema
ms.assetid: 9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb
description: Das AggregateOn-Element stellt die Eigenschaft dar, die verwendet wird, um die Reihenfolge gruppierter Elemente für ein gruppiertes FindItem-Resultset zu bestimmen.
ms.openlocfilehash: 4fa46837cc794bc6c4b23a6b5627d95509d60d70
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541553"
---
# <a name="aggregateon"></a>AggregateOn

Das **AggregateOn-Element** stellt die Eigenschaft dar, die verwendet wird, um die Reihenfolge gruppierter Elemente für ein gruppiertes FindItem-Resultset zu bestimmen. 
  
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
|**Aggregate** <br/> | Gibt den Maximal- oder Minimalwert der Eigenschaft an, die durch das [FieldURI-Element](fielduri.md) identifiziert wird, das zum Sortieren der Elementgruppen verwendet wird.<br/><br/>Im Folgenden sind die möglichen Werte aufgeführt:  <br/><br/>- Minimum  <br/>- Maximum  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifiziert einzelne Mitglieder eines Wörterbuchs.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifiziert erweiterte MAPI-Eigenschaften, die abgerufen, festgelegt oder erstellt werden sollen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GroupBy](groupby.md) <br/> |Gibt beliebige Gruppierungen für FindItem-Abfragen an.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  `/FindItem/GroupBy` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der [FindItem-Vorgang](finditem-operation.md) kann gruppierte Ergebnisse zurückgeben. Innerhalb gruppierter Ergebnisse werden alle Elemente, die denselben Wert für eine bestimmte Gruppierungseigenschaft haben, gesammelt und als untergeordnete Elemente dieser Gruppe dargestellt. Wenn Sie z. B. nach Absender gruppieren, werden alle E-Mails in separate Gruppen unterteilt, je nachdem, ob sie von Absender A, Absender B usw. stammen. Diese Gruppen sind untergeordnete Elemente der Absendergruppe. 
  
Jede der Gruppen innerhalb der Absendergruppe enthält eine Sammlung von Elementen, z. B. die tatsächlichen E-Mails, die von jedem Absender stammen. Sie können das [SortOrder-Element](sortorder.md) verwenden, um die Elemente innerhalb einer Gruppe zu sortieren. Um die Gruppen basierend auf den Eigenschaftswerten eines Elements zu sortieren, müssen Sie jedoch aggregation verwenden. 
  
Bei der Aggregation basiert die Reihenfolge der Gruppen auf einer bestimmten Eigenschaft der Elemente innerhalb der Gruppe. Wenn Sie aggregation zum Sortieren von Elementen innerhalb einer Gruppe verwenden, müssen Sie eine repräsentative Eigenschaft identifizieren, nach der die Gruppen sortiert werden sollen. Sie können das **AggregateOn-Element** verwenden, um die repräsentative Eigenschaft anzugeben. 
  
Wenn eine repräsentative Eigenschaft identifiziert wird, wird das **Aggregatattribut** verwendet, um anzugeben, ob die Gruppen nach dem Maximal- oder Mindestwert der identifizierten Eigenschaft sortiert werden. Wenn das **Aggregate-Attribut** auf Maximum festgelegt ist, werden die Gruppen beginnend mit dem größten Wert für die **AggregateOn-Eigenschaft** sortiert. Wenn das **Aggregate-Attribut** auf Minimum festgelegt ist, werden die Gruppen beginnend mit dem kleinsten Wert für die **AggregateOn-Eigenschaft** sortiert. 
  
Wenn Sie z. B. eine gruppierte FindItem-Abfrage ausgeben möchten, die nach Absender gruppiert ist, Sie die Gruppen jedoch so sortieren möchten, dass die Gruppe mit der neuesten E-Mail-Nachricht oben ist, können Sie nach Absender gruppieren und das Datum/die Uhrzeit aggregieren, das mit dem **Aggregatattribut** Maximum empfangen wurde. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine gruppierte FindItem-Anforderung und -Antwort. Das Beispiel zeigt eine Anforderung zum Zurückgeben von Elementen, die nach der **ConversationTopic-Eigenschaft** gruppiert sind. Zwei Gruppen, A und B, werden basierend auf dem Maximalwert der [DateTimeReceived-Eigenschaft](datetimereceived.md) in absteigender Reihenfolge zurückgegeben. 
  
```XML
<!-- EXAMPLE REQUEST -->
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Verwenden Sie das [SortOrder-Element,](sortorder.md) um die Elemente in einer Gruppe zu sortieren. 
  
> [!NOTE]
> Die Elementbezeichner und Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

