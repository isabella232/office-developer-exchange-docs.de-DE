---
title: FindPeople
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 12c70441-77b9-4619-8e66-1b7e3a63ba48
description: 'Das FindPeople-Element gibt einen Satz von Daten an, die in einer FindPeople-Anforderung verwendet werden. Die Daten enthalten null oder mehr der folgenden Elemente: ein Persona-Shape (optional), eine indizierte Seitenelementansicht, eine Einschränkung (optional), eine Aggregationseinschränkung (optional), eine Sortierreihenfolge (optional), eine übergeordnete Ordner-ID und eine Abfragezeichenfolge (optional).'
ms.openlocfilehash: 44070c79ad5d1615929a6169d1808cf365b7cab4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535163"
---
# <a name="findpeople"></a>FindPeople

Das **FindPeople-Element** gibt einen Satz von Daten an, die in einer FindPeople-Anforderung verwendet werden. Die Daten enthalten null oder mehr der folgenden Elemente: ein Persona-Shape (optional), eine indizierte Seitenelementansicht, eine Einschränkung (optional), eine Aggregationseinschränkung (optional), eine Sortierreihenfolge (optional), eine übergeordnete Ordner-ID und eine Abfragezeichenfolge (optional). 
  
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

[PersonaShape](personashape.md)  |  [IndexedPageItemView](indexedpageitemview.md)  |  [Einschränkung](restriction.md)  |  [AggregationRestriction](aggregationrestriction.md)  |  [SortOrder](sortorder.md)  |  [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [QueryString (QueryStringType)](querystring-querystringtype.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

