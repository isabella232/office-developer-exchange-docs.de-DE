---
title: FindPeople
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12c70441-77b9-4619-8e66-1b7e3a63ba48
description: 'Das FindPeople-Element gibt einen Satz von Daten in einer Anforderung FindPeople verwendet. Die Daten enthalten, 0 (null) oder mehrere der folgenden Elemente: eine Rolle Form (optional), einem indizierten Element Seitenansicht, eine Einschränkung (optional), eine Aggregation Einschränkung (optional), eine Sortierreihenfolge (optional), eine Id des übergeordneten Ordners und eine Abfragezeichenfolge (optional).'
ms.openlocfilehash: 79c8a4324cd217232442b781c33223296d8015e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758473"
---
# <a name="findpeople"></a>FindPeople

Das **FindPeople** -Element gibt einen Satz von Daten in einer Anforderung FindPeople verwendet. Die Daten enthalten, 0 (null) oder mehrere der folgenden Elemente: eine Rolle Form (optional), einem indizierten Element Seitenansicht, eine Einschränkung (optional), eine Aggregation Einschränkung (optional), eine Sortierreihenfolge (optional), eine Id des übergeordneten Ordners und eine Abfragezeichenfolge (optional). 
  
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

[PersonaShape](personashape.md) | [IndexedPageItemView](indexedpageitemview.md) | [Einschränkung](restriction.md) | [AggregationRestriction](aggregationrestriction.md) | [SortOrder](sortorder.md) | [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [ QueryString (QueryStringType)](querystring-querystringtype.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

