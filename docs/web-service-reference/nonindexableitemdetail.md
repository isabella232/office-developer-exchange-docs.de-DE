---
title: NonIndexableItemDetail
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a26d4c02-f1bd-40c4-9257-5db45e839f17
description: Das NonIndexableItemDetail-Element gibt detaillierte Informationen zu einem Element, das nicht indiziert werden kann.
ms.openlocfilehash: ef1bd072a44b42b501a3016c394b89fe6ab25bf0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830543"
---
# <a name="nonindexableitemdetail"></a>NonIndexableItemDetail

Das **NonIndexableItemDetail** -Element gibt detaillierte Informationen zu einem Element, das nicht indiziert werden kann. 
  
```XML
<NonIndexableItemDetail>
   <ItemId/>
   <ErrorCode/>
   <ErrorDescription/>
   <IsPartiallyIndexed/>
   <IsPermanentFailure/>
   <SortValue/>
   <AttemptCount/>
   <LastAttemptTime/>
   <AdditionalInfo/>
</NonIndexableItemDetail>
```

 **NonIndexableItemDetailType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[ItemId](itemid.md) | [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md) | [ErrorDescription](errordescription.md) | [IsPartiallyIndexed](ispartiallyindexed.md) | [IsPermanentFailure](ispermanentfailure.md) | [SortValue](sortvalue.md) | [AttemptCount ](attemptcount.md)  |  [LastAttemptTime](lastattempttime.md) | [AdditionalInfo](additionalinfo.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Elemente (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md)
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

