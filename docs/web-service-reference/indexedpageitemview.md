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
description: Das IndexedPageItemView-Element beschreibt, wie die Seiten Unterhaltung oder Elementinformationen für eine FindItem-Operation oder eine FindConversation-Vorgangsanforderung zurückgegeben werden.
ms.openlocfilehash: 0a66f17855fd425082e3651886d3eeec4f217ac4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456913"
---
# <a name="indexedpageitemview"></a>IndexedPageItemView

Das **IndexedPageItemView** -Element beschreibt, wie die Seiten Unterhaltung oder Elementinformationen für eine [FindItem-Operation](finditem-operation.md) oder eine [FindConversation-Vorgangs](findconversation-operation.md) Anforderung zurückgegeben werden. 
  
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
|**Offset** <br/> |Beschreibt den Offset aus dem **Basepoint**. Wenn **Basepoint** gleich dem Anfang ist, ist der Offset positiv. Wenn **Basepoint** gleich End ist, wird der Offset so behandelt, als wäre er negativ. Dadurch wird angegeben, welches Element oder welche Unterhaltung als erstes in der Antwort zugestellt wird. Dieses Attribut ist erforderlich.  <br/> |
|**Basepoint** <br/> |Beschreibt, ob die Seite von Elementen oder Unterhaltungen am Anfang oder am Ende der Gruppe von Elementen oder Unterhaltungen beginnt, die mit den Suchkriterien gefunden werden. Suche von Ende aus sucht immer rückwärts. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="basepoint-attribute"></a>Basepoint-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Anfang  <br/> |Die ausgelagerte Ansicht beginnt am Anfang der gefundenen Unterhaltung oder des Elementsatzes.  <br/> |
|Ende  <br/> |Die ausgelagerte Ansicht beginnt am Ende der gefundenen Unterhaltung oder des Elementsatzes.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |Definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Bei der Suche ab dem Ende wird der durch den Offset angegebene Ursprung verschoben. Darüber hinaus wird der Zeiger nach der Anzahl der angeforderten Datensätze zurück verschoben. Wenn beispielsweise 100 Datensätze vorhanden sind und der Offset 25 vom Ende ist, beginnt die Suche von 75. Wenn 10 Datensätze zurückgegeben werden, wird der Zeiger rückwärts um weitere 10 Datensätze nach 65 verschoben und gibt Datensätze 65 bis 75 zurück. Der nächste Index lautet 64. Der nächste Offset vom Ende für eine Seite ist 100 minus 64, was 36 entspricht. 36 ist der Wert für den nächsten Offset vom Ende, um die nächste indizierte Seite abzurufen.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine [FindItem-Vorgangs](finditem-operation.md) Anforderung. Jedes Element wird mit seiner ID und seinem Betreff zurückgegeben. Es werden maximal sechs Elemente in der Antwort zurückgegeben, wie im **MaxEntriesReturned** -Attribut angegeben. Die Elemente werden in aufsteigender Reihenfolge nach Wichtigkeit gruppiert aufgelistet. Elemente in einer Gruppe werden nach Betreff aggregiert. 
  
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
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)
  
[FindConversation-Vorgang](findconversation-operation.md)


[Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

