---
title: IndexedPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IndexedPageFolderView
api_type:
- schema
ms.assetid: c6dac232-244b-4db0-9a15-5e01b8aa7a7d
description: Das IndexedPageFolderView-Element beschreibt, wie Seitenelementinformationen in einer FindFolder-Antwort zurückgegeben werden.
ms.openlocfilehash: 0a5d0f7e63549b7a851862d957ff32dff4333ce3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542239"
---
# <a name="indexedpagefolderview"></a>IndexedPageFolderView

Das **IndexedPageFolderView-Element** beschreibt, wie Seitenelementinformationen in einer [FindFolder-Antwort](findfolder.md) zurückgegeben werden. 
  
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
|**MaxEntriesReturned** <br/> |Beschreibt die maximale Anzahl von Ordnern, die in der Antwort zurückgegeben werden sollen. Dieses Attribut ist optional.  <br/> |
|**Offset** <br/> |Beschreibt den Offset vom **BasePoint**. Der Offset muss größer oder gleich Null sein. Wenn **BasePoint** gleich Anfang ist, ist der Offset positiv. Wenn **BasePoint** gleich Ende ist, wird der Offset so behandelt, als wäre er negativ.  <br/> Dadurch wird angegeben, welcher Ordner der erste Ordner ist, der in der Antwort übermittelt wird. Dieses Attribut ist erforderlich.  <br/> |
|**Basispunkt** <br/> |Beschreibt, ob die Seite der Ordner von Anfang oder Ende der Gruppe von Ordnern beginnt, die mit den Suchkriterien gefunden werden. Wenn Sie vom Ende aus suchen, wird immer rückwärts gesucht. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="basepoint-attribute"></a>BasePoint-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Anfang  <br/> |Die seitenseitige Ansicht beginnt am Anfang des Ordnersatzes "Gefunden".  <br/> |
|Ende  <br/> |Die seitenierte Ansicht beginnt am Ende des Ordnersatzes "Gefunden".  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Suchen von Ordnern in einem Postfach.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Suchen von Ende umfasst den Wechsel zu dem durch den Offset identifizierten Ursprung. Darüber hinaus wird der Zeiger um die Anzahl der angeforderten Datensätze zurück verschoben. Wenn beispielsweise 100 Datensätze vorhanden sind und der Offset 25 vom Ende entfernt ist, beginnt die Suche bei 75. Wenn 10 Datensätze zurückgegeben werden, wird der Zeiger um weitere 10 Datensätze nach hinten auf 65 verschoben und die Datensätze 65 bis 75 zurückgegeben. Der nächste Index ist 64. Der nächste Offset vom Ende einer Seite ist 100 minus 64, was 36 entspricht. Der Wert für den nächsten Offset vom Ende, um die nächste indizierte Seite abzurufen, ist 36.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

