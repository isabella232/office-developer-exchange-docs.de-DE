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
description: Das IndexedPageFolderView-Element beschreibt, wie Informationen zum ausgelagerten Element in einer FindFolder-Antwort zurückgegeben werden.
ms.openlocfilehash: 6e9e2796c0bdcd9a15487f0e1bc7cbdf09d0a492
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457200"
---
# <a name="indexedpagefolderview"></a>IndexedPageFolderView

Das **IndexedPageFolderView** -Element beschreibt, wie Informationen zum ausgelagerten Element in einer [FindFolder](findfolder.md) -Antwort zurückgegeben werden. 
  
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
|**Offset** <br/> |Beschreibt den Offset aus dem **Basepoint**. Offset muss größer als oder gleich NULL sein. Wenn **Basepoint** gleich dem Anfang ist, ist der Offset positiv. Wenn **Basepoint** gleich End ist, wird der Offset so behandelt, als wäre er negativ.  <br/> Dadurch wird angegeben, welcher Ordner der erste in der Antwort zugestellte Ordner ist. Dieses Attribut ist erforderlich.  <br/> |
|**Basepoint** <br/> |Beschreibt, ob die Seite von Ordnern am Anfang oder am Ende der Ordnergruppe beginnt, die mit den Suchkriterien gefunden werden. Suche von Ende aus sucht immer rückwärts. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="basepoint-attribute"></a>Basepoint-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Anfang  <br/> |Die ausgelagerte Ansicht beginnt am Anfang der gefundenen Ordnergruppe.  <br/> |
|Ende  <br/> |Die ausgelagerte Ansicht beginnt am Ende der gefundenen Ordnergruppe.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Suchen von Ordnern in einem Postfach.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Bei der Suche von Ende wird der vom Offset angegebene Ursprung verschoben. Darüber hinaus wird der Zeiger nach der Anzahl der angeforderten Datensätze zurück verschoben. Wenn beispielsweise 100 Datensätze vorhanden sind und der Offset 25 vom Ende ist, beginnt die Suche von 75. Wenn 10 Datensätze zurückgegeben werden, wird der Zeiger rückwärts um weitere 10 Datensätze nach 65 verschoben und gibt Datensätze 65 bis 75 zurück. Der nächste Index lautet 64. Der nächste Offset vom Ende für eine Seite ist 100 minus 64, was 36 entspricht. Der Wert für den nächsten Offset vom Ende zum Abrufen der nächsten indizierten Seite lautet 36.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

