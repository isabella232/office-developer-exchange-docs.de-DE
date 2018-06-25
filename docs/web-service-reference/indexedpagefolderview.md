---
title: IndexedPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageFolderView
api_type:
- schema
ms.assetid: c6dac232-244b-4db0-9a15-5e01b8aa7a7d
description: Das IndexedPageFolderView-Element beschreibt, wie ausgelagerten Elementinformationen in einer FindFolder Antwort zurückgegeben wird.
ms.openlocfilehash: f32f778daa6fa3fea93ab2bc1951f2407dcf7f80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829910"
---
# <a name="indexedpagefolderview"></a>IndexedPageFolderView

Das **IndexedPageFolderView** -Element beschreibt, wie ausgelagerten Elementinformationen in einer [FindFolder](findfolder.md) Antwort zurückgegeben wird. 
  
[FindFolder](findfolder.md)
  
[IndexedPageFolderView](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**"MaxEntriesReturned"** <br/> |Beschreibt die maximale Anzahl von Ordnern in der Antwort zurückgegeben. Dieses Attribut ist optional.  <br/> |
|**Offset** <br/> |Beschreibt die **Basispunkt**-Offset. Offset muss größer als oder gleich 0 (null) sein. Wenn **Basispunkt** Anfang gleich ist, ist der Offset positiv. Wenn **Basispunkt** End entspricht, wird der Offset behandelt, als wäre es negative.  <br/> Mit diesen wird identifiziert, welcher Ordner der erste Ordner in der Antwort übermittelt werden. Dieses Attribut ist erforderlich.  <br/> |
|**Basispunkt** <br/> |Beschreibt, ob die Seite Ordner gestartet wird, aus der Anfang oder das Ende des Satzes von Ordnern, die mit den Suchkriterien gefunden werden. Vom Ende immer bemüht sucht rückwärts. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="basepoint-attribute"></a>Basispunkt-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Anfang  <br/> |Die Seitenansicht beginnt am Anfang des Satzes gefundenen Ordner.  <br/> |
|Ende  <br/> |Die Seitenansicht beginnt am Ende des Satzes gefundenen Ordner.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Suchen von Ordnern in einem Postfach an.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>Hinweise

End gesucht umfasst das Verschieben in den Offset identifizierten Ursprung. Darüber hinaus wird der Mauszeiger durch die Anzahl der angeforderten Datensätze zurück verschoben. Beispielsweise wenn 100 Datensätze vorhanden sind und der Offset 25 vom Ende ist, beginnt für die Suche von 75. Wenn 10 Datensätze zurückgegeben werden, wird der Mauszeiger rückwärts verschoben, zusätzlich 10 65 Datensätze und Datensätze 65 bis 75 zurückgibt. Der nächste Index ist 64. Der nächste Offset vom Ende einer Seite wird 100 minus 64 was 36 entspricht. Der Wert für den nächsten Offset vom Ende zum Abrufen der nächsten Seite indizierten ist 36.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

