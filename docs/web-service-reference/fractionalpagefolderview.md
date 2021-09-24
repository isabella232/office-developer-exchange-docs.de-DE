---
title: FractionalPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FractionalPageFolderView
api_type:
- schema
ms.assetid: ef681f8a-136a-4c0e-ade6-ddcdbf2d85ad
description: Das FractionalPageFolderView-Element beschreibt, wo die Seitenansicht beginnt, und die maximale Anzahl von Ordnern, die in einer FindFolder-Anforderung zurückgegeben werden.
ms.openlocfilehash: b3d4bd63f94c2db7761dabfad1e32558ceb30be5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530253"
---
# <a name="fractionalpagefolderview"></a>FractionalPageFolderView

Das **FractionalPageFolderView-Element** beschreibt, wo die Seitenansicht beginnt, und die maximale Anzahl von Ordnern, die in einer [FindFolder-Anforderung](findfolder.md) zurückgegeben werden. 
  
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
|**MaxEntriesReturned** <br/> |Gibt die maximale Anzahl von Ergebnissen an, die in der [FindFolder-Antwort](findfolder.md) zurückgegeben werden sollen. Dieses Attribut ist optional.  <br/> |
|**Zähler** <br/> |Stellt den Zähler des Bruchoffsets vom Anfang des Resultsets dar. Dieses Attribut ist erforderlich. Der Zähler muss gleich oder kleiner als der Nenner sein. Dieses Attribut muss einen ganzzahligen Wert darstellen, der gleich oder größer als Null ist. Weitere Informationen finden Sie in den Anmerkungen weiter unten in diesem Thema.  <br/> |
|**Nenner** <br/> |Stellt den Nenner des Bruchoffsets ab dem Anfang der Gesamtzahl der Ordner im Resultset dar. Dieses Attribut ist erforderlich. Dieses Attribut muss einen integralen Wert darstellen, der größer als ein Wert ist. Weitere Informationen finden Sie in den Anmerkungen weiter unten in diesem Thema.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Identifizieren von Ordnern in einem Postfach.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Seitenansichtsversatz vom Anfang der Gruppe gefundener Ordner wird durch einen Bruch beschrieben. Der Bruch, der durch die Attribute **"Numerator"** und **"Denominator"** definiert wird, beschreibt, wo die Informationsseite beginnt. Wenn der **Zähler** beispielsweise gleich vier und der **Nenner** gleich fünf ist, beginnt die Seite mit den zurückgegebenen Informationen bei einem Eintrag, der vier Fünftel des Wegs in das Resultset enthält. 
  
Wenn der Bruch mit 0 ausgewertet wird, gibt dies den Anfang des Resultsets an. Wenn der Bruch zu einem Ausgewerteten ausgewertet wird, gibt dies das Ende des Resultsets an.
  
> [!NOTE]
> Der Bruch stellt den Anfangspunkt der Seite dar, nicht wie viele Ergebnisse im Resultset zurückgegeben werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindFolder-Vorgang](findfolder-operation.md)


[Suchen von Ordnern](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

