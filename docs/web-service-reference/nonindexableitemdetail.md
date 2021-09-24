---
title: NonIndexableItemDetail
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a26d4c02-f1bd-40c4-9257-5db45e839f17
description: Das NonIndexableItemDetail-Element gibt Detailinformationen zu einem Element an, das nicht indiziert werden kann.
ms.openlocfilehash: 2c3dae9276bee4800352c74acca37fe85ddbf223
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515439"
---
# <a name="nonindexableitemdetail"></a>NonIndexableItemDetail

Das **NonIndexableItemDetail-Element** gibt Detailinformationen zu einem Element an, das nicht indiziert werden kann. 
  
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

[ItemId](itemid.md)  |  [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md)  |  [ErrorDescription](errordescription.md)  |  [IsPartiallyIndexed](ispartiallyindexed.md)  |  [IsPermanentFailure](ispermanentfailure.md)  |  [SortValue](sortvalue.md)  |  [AttemptCount](attemptcount.md)  |  [LastAttemptTime](lastattempttime.md)  |  [AdditionalInfo](additionalinfo.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Items (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

