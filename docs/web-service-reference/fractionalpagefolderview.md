---
title: FractionalPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageFolderView
api_type:
- schema
ms.assetid: ef681f8a-136a-4c0e-ade6-ddcdbf2d85ad
description: Das FractionalPageFolderView-Element beschreibt, wo die ausgelagerte Ansicht beginnt und die maximale Anzahl von Ordnern, die in einer FindFolder-Anforderung zurückgegeben werden.
ms.openlocfilehash: a8627c6277b49655d3933679128b844118633cda
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463069"
---
# <a name="fractionalpagefolderview"></a>FractionalPageFolderView

Das **FractionalPageFolderView** -Element beschreibt, wo die ausgelagerte Ansicht beginnt und die maximale Anzahl von Ordnern, die in einer [FindFolder](findfolder.md) -Anforderung zurückgegeben werden. 
  
[FindFolder](findfolder.md)
  
[FractionalPageFolderView](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Gibt die maximale Anzahl von Ergebnissen an, die in der [FindFolder](findfolder.md) -Antwort zurückgegeben werden. Dieses Attribut ist optional.  <br/> |
|**Zähler** <br/> |Stellt den Zaehler des Bruchs Offsets vom Anfang des Resultsets dar. Dieses Attribut ist erforderlich. Der Zähler muss gleich oder kleiner als der Nenner sein. Dieses Attribut muss einen ganzzahligen Wert darstellen, der größer oder gleich NULL ist. Weitere Informationen finden Sie weiter unten in diesem Thema unter Hinweise.  <br/> |
|**Nenner** <br/> |Stellt den Nenner des Bruchs Offsets vom Anfang der Gesamtzahl der Ordner im Resultset dar. Dieses Attribut ist erforderlich. Dieses Attribut muss einen ganzzahligen Wert darstellen, der größer als 1 ist. Weitere Informationen finden Sie weiter unten in diesem Thema unter Hinweise.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Identifizieren von Ordnern in einem Postfach.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Offset der Seitenansicht vom Anfang der Gruppe gefundener Ordner wird durch einen Bruch beschrieben. Der Bruch, der durch die Attribute **Zaehler** und **Nenner** definiert ist, beschreibt, wo die Informationsseite beginnt. Wenn der **Zähler** beispielsweise vier und der **Nenner** gleich fünf ist, beginnt die Seite mit den zurückgegebenen Informationen bei einem Eintrag, der sich auf vier Fünftel der Methode in der Ergebnismenge befand. 
  
Wenn der Bruch auf 0 (null) ausgewertet wird, wird der Anfang des Resultsets angegeben. Wenn der Bruch zu 1 ausgewertet wird, gibt dies das Ende der Ergebnismenge an.
  
> [!NOTE]
> Der Bruch stellt den Startpunkt der Seite dar, nicht wie viele Ergebnisse in der Ergebnismenge zurückgegeben werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindFolder-Vorgang](findfolder-operation.md)


[Suchen von Ordnern](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

