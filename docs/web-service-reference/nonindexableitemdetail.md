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
# <a name="nonindexableitemdetail"></a><span data-ttu-id="7bb38-103">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="7bb38-103">NonIndexableItemDetail</span></span>

<span data-ttu-id="7bb38-104">Das **NonIndexableItemDetail** -Element gibt detaillierte Informationen zu einem Element, das nicht indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7bb38-104">The **NonIndexableItemDetail** element specifies detail information about an item that cannot be indexed.</span></span> 
  
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

 <span data-ttu-id="7bb38-105">**NonIndexableItemDetailType**</span><span class="sxs-lookup"><span data-stu-id="7bb38-105">**NonIndexableItemDetailType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7bb38-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7bb38-106">Attributes and elements</span></span>

<span data-ttu-id="7bb38-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7bb38-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7bb38-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7bb38-108">Attributes</span></span>

<span data-ttu-id="7bb38-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7bb38-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7bb38-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7bb38-110">Child elements</span></span>

<span data-ttu-id="7bb38-111">[ItemId](itemid.md) | [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md) | [ErrorDescription](errordescription.md) | [IsPartiallyIndexed](ispartiallyindexed.md) | [IsPermanentFailure](ispermanentfailure.md) | [SortValue](sortvalue.md) | [AttemptCount ](attemptcount.md)  |  [LastAttemptTime](lastattempttime.md) | [AdditionalInfo](additionalinfo.md)</span><span class="sxs-lookup"><span data-stu-id="7bb38-111">[ItemId](itemid.md) | [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md) | [ErrorDescription](errordescription.md) | [IsPartiallyIndexed](ispartiallyindexed.md) | [IsPermanentFailure](ispermanentfailure.md) | [SortValue](sortvalue.md) | [AttemptCount](attemptcount.md) | [LastAttemptTime](lastattempttime.md) | [AdditionalInfo](additionalinfo.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7bb38-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7bb38-112">Parent elements</span></span>

[<span data-ttu-id="7bb38-113">Elemente (ArrayOfNonIndexableItemDetailsType)</span><span class="sxs-lookup"><span data-stu-id="7bb38-113">Items (ArrayOfNonIndexableItemDetailsType)</span></span>](items-arrayofnonindexableitemdetailstype.md)
  
## <a name="remarks"></a><span data-ttu-id="7bb38-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7bb38-114">Remarks</span></span>

<span data-ttu-id="7bb38-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7bb38-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7bb38-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7bb38-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7bb38-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7bb38-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bb38-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="7bb38-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7bb38-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7bb38-119">Schema name</span></span>  <br/> |<span data-ttu-id="7bb38-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7bb38-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="7bb38-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7bb38-121">Validation file</span></span>  <br/> |<span data-ttu-id="7bb38-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7bb38-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7bb38-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7bb38-123">Can be empty</span></span>  <br/> ||
   

