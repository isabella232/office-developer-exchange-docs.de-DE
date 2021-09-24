---
title: IndexedPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IndexedPageItemView
api_type:
- schema
ms.assetid: 6d1b0b04-cc35-4a57-bd7a-824136d14fda
description: Das IndexedPageItemView-Element beschreibt, wie Seitenunterhaltungs- oder Elementinformationen für einen FindItem-Vorgang oder eine FindConversation-Vorgangsanforderung zurückgegeben werden.
ms.openlocfilehash: bf46bdbd457c4f4fa47e6b575d3b797b74f58995
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541126"
---
# <a name="indexedpageitemview"></a>IndexedPageItemView

Das **IndexedPageItemView-Element** beschreibt, wie Seitenunterhaltungs- oder Elementinformationen für einen [FindItem-Vorgang](finditem-operation.md) oder eine [FindConversation-Vorgangsanforderung](findconversation-operation.md) zurückgegeben werden. 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Beschreibt die maximale Anzahl von Elementen oder Unterhaltungen, die in der Antwort zurückgegeben werden sollen. Dieses Attribut ist optional.  <br/> |
|**Offset** <br/> |Beschreibt den Offset vom **BasePoint**. Wenn **BasePoint** gleich Anfang ist, ist der Offset positiv. Wenn **BasePoint** gleich Ende ist, wird der Offset so behandelt, als wäre er negativ. Dadurch wird angegeben, welches Element oder welche Unterhaltung als erstes in der Antwort übermittelt wird. Dieses Attribut ist erforderlich.  <br/> |
|**Basispunkt** <br/> |Beschreibt, ob die Seite von Elementen oder Unterhaltungen am Anfang oder am Ende der Gruppe von Elementen oder Unterhaltungen beginnt, die mithilfe der Suchkriterien gefunden werden. Wenn Sie vom Ende aus suchen, wird immer rückwärts gesucht. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="basepoint-attribute"></a>BasePoint-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Anfang  <br/> |Die seitenseitige Ansicht beginnt am Anfang der gefundenen Unterhaltung oder des Elementsatzes.  <br/> |
|Ende  <br/> |Die seitenseitige Ansicht beginnt am Ende der gefundenen Unterhaltung oder des Elementsatzes.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |Definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Suchen vom Ende umfasst den Wechsel zu dem durch den Offset identifizierten Ursprung. Darüber hinaus wird der Zeiger um die Anzahl der angeforderten Datensätze zurück verschoben. Wenn beispielsweise 100 Datensätze vorhanden sind und der Offset 25 vom Ende entfernt ist, beginnt die Suche bei 75. Wenn 10 Datensätze zurückgegeben werden, wird der Zeiger um weitere 10 Datensätze nach hinten auf 65 verschoben und die Datensätze 65 bis 75 zurückgegeben. Der nächste Index ist 64. Der nächste Offset vom Ende einer Seite ist 100 minus 64, was 36 entspricht. 36 ist der Wert für den nächsten Offset vom Ende, um die nächste indizierte Seite abzurufen.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine [FindItem-Vorgangsanforderung.](finditem-operation.md) Jedes Element wird mit seiner ID und seinem Betreff zurückgegeben. In der Antwort werden maximal sechs Elemente zurückgegeben, wie durch das **MaxEntriesReturned-Attribut** angegeben. Die Elemente werden in aufsteigender Reihenfolge nach Wichtigkeit gruppiert aufgelistet. Elemente in einer Gruppe werden nach Betreff aggregiert. 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)
  
[FindConversation-Vorgang](findconversation-operation.md)


[Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

