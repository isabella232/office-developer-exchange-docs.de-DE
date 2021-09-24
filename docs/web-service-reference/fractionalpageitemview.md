---
title: FractionalPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FractionalPageItemView
api_type:
- schema
ms.assetid: 4111afec-35e7-4c6f-b291-9bbba603f633
description: Das FractionalPageItemView-Element beschreibt, wo die Seitenansicht beginnt und wie viele Elemente in einer FindItem-Anforderung maximal zurückgegeben werden.
ms.openlocfilehash: 0d948bad0ba24c4a105be32daa645d1864cb4f3b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530246"
---
# <a name="fractionalpageitemview"></a>FractionalPageItemView

Das **FractionalPageItemView-Element** beschreibt, wo die Seitenansicht beginnt und wie viele Elemente in einer [FindItem-Anforderung](finditem.md) maximal zurückgegeben werden. 
  
[FindItem](finditem.md)
  
[FractionalPageItemView](fractionalpageitemview.md)
  
```xml
<FractionalPageItemView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Gibt die maximale Anzahl von Ergebnissen an, die in der [FindItem-Antwort](finditem.md) zurückgegeben werden sollen. Dieses Attribut ist optional. Wenn dieses Attribut nicht angegeben ist, gibt der Aufruf alle verfügbaren Elemente zurück.  <br/> |
|**Zähler** <br/> |Stellt den Zähler des Bruchoffsets vom Anfang des Resultsets dar. Dieses Attribut ist erforderlich. Der Zähler muss gleich oder kleiner als der Nenner sein. Dieses Attribut muss einen ganzzahligen Wert darstellen, der gleich oder größer als Null ist.  <br/> Weitere Informationen finden Sie in den Anmerkungen weiter unten in diesem Thema.  <br/> |
|**Nenner** <br/> |Stellt den Nenner des Bruchoffsets ab dem Anfang der Gesamtzahl der Elemente im Resultset dar. Dieses Attribut ist erforderlich. Dieses Attribut muss einen integralen Wert darstellen, der größer als ein Wert ist.  <br/> Weitere Informationen finden Sie in den Anmerkungen weiter unten in diesem Thema.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Seitenansichtsversatz vom Anfang der Gruppe gefundener Elemente wird durch einen Bruch beschrieben. Der Bruch, der durch die Attribute **"Numerator"** und **"Denominator"** definiert wird, beschreibt, wo die Informationsseite beginnt. Wenn der **Zähler** beispielsweise gleich vier und der **Nenner** gleich fünf ist, beginnt die Seite mit den zurückgegebenen Informationen bei einem Eintrag, der vier Fünftel des Wegs in das Resultset enthält. 
  
Wenn der Bruch mit 0 ausgewertet wird, gibt dies den Anfang des Resultsets an. Wenn der Bruch zu einem Ausgewerteten ausgewertet wird, gibt dies das Ende des Resultsets an.
  
> [!NOTE]
> Der Bruch stellt den Anfangspunkt der Seite dar, nicht wie viele Ergebnisse im Resultset zurückgegeben werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine [FindItem-Anforderung.](finditem.md) Die Anforderung gibt Elemente aus den Suchergebnissen zurück, die nach dem zweiten Drittel aller Elemente im Resultset beginnen. 
  
```
<?xml version="1.0" encoding="utf-8"?>
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
      <FractionalPageItemView MaxEntriesReturned="12" Numerator="2" Denominator="3"/>
      <GroupBy Order="Descending">
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

Wenn das Resultset beispielsweise neun Elemente enthält, gibt die Seitenansicht bis zu 12 Elemente zurück, beginnend mit dem Element, das zwei Drittel des Wegs in das Resultset gefunden hat. In diesem Fall beginnt die Seite mit dem siebten Element. Die Seite enthält die siebenten, achten und neunten Elemente. Wenn der Zähler auf Null festgelegt ist, gibt die Seitenansicht alle Elemente im Resultset zurück, solange die Zahl kleiner als das **MaxEntriesReturned-Attribut** ist. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)


[Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

