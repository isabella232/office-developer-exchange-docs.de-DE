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
description: Das FractionalPageItemView-Element wird beschrieben, in der Seitenansicht startet und die maximale Anzahl von Elementen in einer Anforderung FindItem zurückgegeben.
ms.openlocfilehash: 38c35d2b68dabfca1a43ab034deaf72c47b0ea66
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758534"
---
# <a name="fractionalpageitemview"></a>FractionalPageItemView

Das **FractionalPageItemView** -Element wird beschrieben, in der Seitenansicht startet und die maximale Anzahl von Elementen in einer Anforderung [FindItem](finditem.md) zurückgegeben. 
  
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
|**"MaxEntriesReturned"** <br/> |Gibt die maximale Anzahl der in der Antwort [FindItem](finditem.md) zurückzugebender Ergebnisse an. Dieses Attribut ist optional. Wenn dieses Attribut nicht angegeben ist, gibt der Aufruf alle verfügbaren Elemente zurück.  <br/> |
|**Zähler** <br/> |Stellt den Zähler für den Bruch Offset vom Anfang des Resultsets dar. Dieses Attribut ist erforderlich. Der Zähler muss kleiner oder gleich der Nenner. Dieses Attribut muss es sich um einen ganzzahligen Wert darstellen, der gleich oder größer als 0 (null) ist.  <br/> Weitere Informationen finden Sie unter "Hinweise" weiter unten in diesem Thema.  <br/> |
|**Nenner** <br/> |Stellt dar, die als Nenner für den Bruch Offset ab dem Anfang der Gesamtanzahl der Elemente im Resultset. Dieses Attribut ist erforderlich. Dieses Attribut muss auf einen ganzzahligen Wert darstellen, der größer als 1 ist.  <br/> Weitere Informationen finden Sie unter "Hinweise" weiter unten in diesem Thema.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Hinweise

Der Seitenansicht Offset vom Beginn des Satzes von gefundenen Elemente wird durch eine Bruchzahl beschrieben. Der Anteil, die durch die **Zähler** und **Nenner** Attribute definiert ist, beschreibt, an die Seite mit Informationen beginnt. Wenn **Zähler** vier und **Nenner** fünf entspricht, befindet die Seite der zurückgegebenen Informationen beginnt am einen Eintrag vier Fünftel die Art und Weise in der Ergebnismenge. 
  
Wenn die Teiler gleich 0 (null) ausgewertet wird, gibt an, dass den Anfang des die Ergebnisse festzulegen. Wenn der Bruchteil eines ergibt, gibt an, dass das Ende des Resultsets.
  
> [!NOTE]
> Der Anteil den Anfangspunkt der Seite darstellt, werden nicht wie viele Ergebnisse im Resultset zurückgegeben. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine [FindItem](finditem.md) -Anforderung. Die Anforderung gibt Elemente zurück, aus den Suchergebnissen aus, die hinter der zweiten dritte der alle Objekte in der Ergebnismenge gestartet. 
  
```
<?xml version="1.0" encoding="utf-8"?>
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

Beispielsweise gibt das Resultset neun Elemente enthält, die Seitenansicht bis zu 12 Elementen, beginnend bei der gefundene Element zwei Drittel der Art und Weise in der Ergebnismenge zurück. In diesem Fall wird die Seite das siebten Element gestartet. Die Seite wird die siebte achten und neunten Elemente enthalten. Wenn der Zähler 0 (null) festgelegt ist, gibt die Seitenansicht alle Elemente zurück, im Resultset als die Anzahl kleiner als das Attribut **"MaxEntriesReturned"** ist. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)


[Finding Items](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

