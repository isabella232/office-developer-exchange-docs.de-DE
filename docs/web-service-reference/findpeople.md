---
title: FindPeople
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12c70441-77b9-4619-8e66-1b7e3a63ba48
description: 'Das FindPeople-Element gibt eine Gruppe von Daten an, die in einer FindPeople-Anforderung verwendet werden. Die Daten enthalten keine oder mehrere der folgenden Elemente: eine persona-Form (optional), eine indizierte Seitenelement Ansicht, eine Einschränkung (optional), eine Aggregations Einschränkung (optional), eine Sortierreihenfolge (optional), eine übergeordnete Ordner-ID und eine Abfragezeichenfolge (optional).'
ms.openlocfilehash: 4777601b7146ec857b5c79fa9d4ced59a7247889
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462901"
---
# <a name="findpeople"></a>FindPeople

Das **FindPeople** -Element gibt eine Gruppe von Daten an, die in einer FindPeople-Anforderung verwendet werden. Die Daten enthalten keine oder mehrere der folgenden Elemente: eine persona-Form (optional), eine indizierte Seitenelement Ansicht, eine Einschränkung (optional), eine Aggregations Einschränkung (optional), eine Sortierreihenfolge (optional), eine übergeordnete Ordner-ID und eine Abfragezeichenfolge (optional). 
  
```XML
<FindPeople>
   <PersonaShape/>
   <IndexedPageItemView/>
   <Restriction/>
   <AggregationRestriction/>
   <SortOrder/>
   <ParentFolderId/>
   <QueryString/>
</FindPeople>
```

 **FindPeopleType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[PersonaShape](personashape.md)  |  [IndexedPageItemView](indexedpageitemview.md)  |  [Einschränkung](restriction.md)  |  [AggregationRestriction](aggregationrestriction.md)  |  [Sortierreihenfolge](sortorder.md)  |  [Parentfolderid (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [QueryString (](querystring-querystringtype.md) querystringtype)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

