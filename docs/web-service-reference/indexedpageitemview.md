---
title: IndexedPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageItemView
api_type:
- schema
ms.assetid: 6d1b0b04-cc35-4a57-bd7a-824136d14fda
description: Das IndexedPageItemView-Element wird beschrieben, wie ausgelagerten Unterhaltung oder Element Informationen für einen FindItem oder FindConversation Vorgang Anforderung zurückgegeben.
ms.openlocfilehash: f1743e22087158c1889977f03774fccbc5577390
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829919"
---
# <a name="indexedpageitemview"></a>IndexedPageItemView

Das **IndexedPageItemView** -Element wird beschrieben, wie ausgelagerten Unterhaltung oder Element Informationen für eine Anforderung [FindItem](finditem-operation.md) oder [FindConversation-Operation](findconversation-operation.md) zurückgegeben wird. 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**"MaxEntriesReturned"** <br/> |Beschreibt die maximale Anzahl von Elementen oder Unterhaltungen in der Antwort zurückgegeben. Dieses Attribut ist optional.  <br/> |
|**Offset** <br/> |Beschreibt die **Basispunkt**-Offset. Wenn **Basispunkt** Anfang gleich ist, ist der Offset positiv. Wenn **Basispunkt** End entspricht, wird der Offset behandelt, als wäre es negative. Dies bezeichnet, welches Element oder Unterhaltung werden zuerst in der Antwort übermittelt werden. Dieses Attribut ist erforderlich.  <br/> |
|**Basispunkt** <br/> |Beschreibt, ob die Seite Elemente oder Unterhaltungen gestartet wird, aus der Anfang oder das Ende des Satzes von Elementen oder Unterhaltungen, die mithilfe der Suchkriterien gefunden werden. Vom Ende immer bemüht sucht rückwärts. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="basepoint-attribute"></a>Basispunkt-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Anfang  <br/> |Die Seitenansicht beginnt am Anfang des gefundenen Unterhaltung oder Element.  <br/> |
|Ende  <br/> |Die Seitenansicht beginnt am Ende der Unterhaltung oder Element gefundenen Menge.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |Definiert eine Anforderung an Unterhaltungen in einem Postfach suchen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Suchvorgänge vom Ende umfasst das Verschieben in den Offset identifizierten Ursprung. Darüber hinaus wird der Mauszeiger durch die Anzahl der angeforderten Datensätze zurück verschoben. Beispielsweise wenn 100 Datensätze vorhanden sind und der Offset 25 vom Ende ist, beginnt für die Suche von 75. Wenn 10 Datensätze zurückgegeben werden, wird der Mauszeiger rückwärts verschoben, zusätzlich 10 65 Datensätze und Datensätze 65 bis 75 zurückgibt. Der nächste Index ist 64. Der nächste Offset vom Ende einer Seite wird 100 minus 64 was 36 entspricht. 36 ist der Wert für den nächsten Offset vom Ende zum Abrufen der nächsten Seite indizierten.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine Anforderung [FindItem Vorgang](finditem-operation.md) . Jedes Element wird mit dem-ID und der Betreff zurückgegeben. Maximal sechs Elemente werden in der Antwort, gemäß dem Attribut **"MaxEntriesReturned"** zurückgegeben. Die Elemente werden in aufsteigender Reihenfolge gruppiert nach Priorität aufgeführt. Nach Betreff werden Elemente in einer Gruppe zusammengefasst. 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <IndexedPageItemView MaxEntriesReturned="6" BasePoint="Beginning" Offset="0" />
      <GroupBy Order="Ascending">
        <t:FieldURI FieldURI="item:Importance"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)
  
[FindConversation Operation](findconversation-operation.md)


[Finding Items](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

