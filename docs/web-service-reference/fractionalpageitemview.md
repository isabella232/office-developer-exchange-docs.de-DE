---
title: FractionalPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageItemView
api_type:
- schema
ms.assetid: 4111afec-35e7-4c6f-b291-9bbba603f633
description: Das FractionalPageItemView-Element beschreibt, wo die ausgelagerte Ansicht beginnt und die maximale Anzahl von Elementen, die in einer FindItem-Anforderung zurückgegeben werden.
ms.openlocfilehash: cbf45838558873dc5846823c2d1b26cf2c8af514
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461310"
---
# <a name="fractionalpageitemview"></a>FractionalPageItemView

Das **FractionalPageItemView** -Element beschreibt, wo die ausgelagerte Ansicht beginnt und die maximale Anzahl von Elementen, die in einer [FindItem](finditem.md) -Anforderung zurückgegeben werden. 
  
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
|**MaxEntriesReturned** <br/> |Gibt die maximale Anzahl von Ergebnissen an, die in der [FindItem](finditem.md) -Antwort zurückgegeben werden. Dieses Attribut ist optional. Wenn dieses Attribut nicht angegeben wird, gibt der Aufruf alle verfügbaren Elemente zurück.  <br/> |
|**Zähler** <br/> |Stellt den Zaehler des Bruchs Offsets vom Anfang des Resultsets dar. Dieses Attribut ist erforderlich. Der Zähler muss gleich oder kleiner als der Nenner sein. Dieses Attribut muss einen ganzzahligen Wert darstellen, der größer oder gleich NULL ist.  <br/> Weitere Informationen finden Sie weiter unten in diesem Thema unter Hinweise.  <br/> |
|**Nenner** <br/> |Stellt den Nenner des Bruchs Offsets vom Anfang der Gesamtzahl der Elemente in der Ergebnisgruppe dar. Dieses Attribut ist erforderlich. Dieses Attribut muss einen ganzzahligen Wert darstellen, der größer als 1 ist.  <br/> Weitere Informationen finden Sie weiter unten in diesem Thema unter Hinweise.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Offset der Seitenansicht vom Anfang der Gruppe gefundener Elemente wird durch einen Bruch beschrieben. Der Bruch, der durch die Attribute **Zaehler** und **Nenner** definiert ist, beschreibt, wo die Informationsseite beginnt. Wenn der **Zähler** beispielsweise vier und der **Nenner** gleich fünf ist, beginnt die Seite mit den zurückgegebenen Informationen bei einem Eintrag, der sich auf vier Fünftel der Methode in der Ergebnismenge befand. 
  
Wenn der Bruch auf 0 (null) ausgewertet wird, wird der Anfang des Resultsets angegeben. Wenn der Bruch zu 1 ausgewertet wird, gibt dies das Ende der Ergebnismenge an.
  
> [!NOTE]
> Der Bruch stellt den Startpunkt der Seite dar, nicht wie viele Ergebnisse in der Ergebnismenge zurückgegeben werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine [FindItem](finditem.md) -Anforderung. Die Anforderung gibt Elemente aus den Suchergebnissen zurück, die nach dem zweiten Drittel aller Elemente in der Ergebnismenge beginnen. 
  
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

Wenn das Resultset beispielsweise neun Elemente enthält, gibt die ausgelagerte Ansicht bis zu 12 Elemente zurück, beginnend bei dem Element, das zwei Drittel der Methode in zum Resultset gefunden hat. In diesem Fall beginnt die Seite mit dem siebten Element. Die Seite enthält das siebte, achte und neunte Element. Wenn der Zähler auf NULL festgelegt ist, gibt die Seitenansicht alle Elemente in der Ergebnismenge zurück, solange die Zahl kleiner als das **MaxEntriesReturned** -Attribut ist. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)


[Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

