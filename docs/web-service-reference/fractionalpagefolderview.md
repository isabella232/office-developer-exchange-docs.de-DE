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
description: Das FractionalPageFolderView-Element wird beschrieben, in der Seitenansicht startet und die maximale Anzahl von Ordnern in einer Anforderung FindFolder zurückgegeben.
ms.openlocfilehash: 3cb5f8333634a0c484ae3ce6a6256631cff57cc5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758531"
---
# <a name="fractionalpagefolderview"></a>FractionalPageFolderView

Das **FractionalPageFolderView** -Element wird beschrieben, in der Seitenansicht startet und die maximale Anzahl von Ordnern in einer Anforderung [FindFolder](findfolder.md) zurückgegeben. 
  
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
|**"MaxEntriesReturned"** <br/> |Gibt die maximale Anzahl der in der Antwort [FindFolder](findfolder.md) zurückzugebender Ergebnisse an. Dieses Attribut ist optional.  <br/> |
|**Zähler** <br/> |Stellt den Zähler für den Bruch Offset vom Anfang des Resultsets dar. Dieses Attribut ist erforderlich. Der Zähler muss kleiner oder gleich der Nenner. Dieses Attribut muss es sich um einen ganzzahligen Wert darstellen, der gleich oder größer als 0 (null) ist. Weitere Informationen finden Sie unter "Hinweise" weiter unten in diesem Thema.  <br/> |
|**Nenner** <br/> |Stellt dar, die als Nenner für den Bruch Offset ab dem Anfang der Gesamtzahl der Ordner im Resultset. Dieses Attribut ist erforderlich. Dieses Attribut muss auf einen ganzzahligen Wert darstellen, der größer als 1 ist. Weitere Informationen finden Sie unter "Hinweise" weiter unten in diesem Thema.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Ordner in einem Postfach zu identifizieren.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>Hinweise

Der Seitenansicht Offset vom Beginn des Satzes mit gefundenen Ordnern wird durch eine Bruchzahl beschrieben. Der Anteil, die durch die **Zähler** und **Nenner** Attribute definiert ist, beschreibt, an die Seite mit Informationen beginnt. Wenn **Zähler** vier und **Nenner** fünf entspricht, befindet die Seite der zurückgegebenen Informationen beginnt am einen Eintrag vier Fünftel die Art und Weise in der Ergebnismenge. 
  
Wenn die Teiler gleich 0 (null) ausgewertet wird, gibt an, dass den Anfang des die Ergebnisse festzulegen. Wenn der Bruchteil eines ergibt, gibt an, dass das Ende des Resultsets.
  
> [!NOTE]
> Der Anteil den Anfangspunkt der Seite darstellt, werden nicht wie viele Ergebnisse im Resultset zurückgegeben. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindFolder Operation](findfolder-operation.md)


[Suchen nach Ordnern](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

