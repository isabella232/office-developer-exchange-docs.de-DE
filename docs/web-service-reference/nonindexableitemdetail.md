---
title: NonIndexableItemDetail
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a26d4c02-f1bd-40c4-9257-5db45e839f17
description: Das NonIndexableItemDetail-Element gibt Detailinformationen zu einem Element an, das nicht indiziert werden kann.
ms.openlocfilehash: 4fc4324501570402d22aa303d6af2a60b50b3cc6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466738"
---
# <a name="nonindexableitemdetail"></a><span data-ttu-id="a7c77-103">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="a7c77-103">NonIndexableItemDetail</span></span>

<span data-ttu-id="a7c77-104">Das **NonIndexableItemDetail** -Element gibt Detailinformationen zu einem Element an, das nicht indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7c77-104">The **NonIndexableItemDetail** element specifies detail information about an item that cannot be indexed.</span></span> 
  
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

 <span data-ttu-id="a7c77-105">**NonIndexableItemDetailType**</span><span class="sxs-lookup"><span data-stu-id="a7c77-105">**NonIndexableItemDetailType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a7c77-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a7c77-106">Attributes and elements</span></span>

<span data-ttu-id="a7c77-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a7c77-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7c77-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a7c77-108">Attributes</span></span>

<span data-ttu-id="a7c77-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7c77-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7c77-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7c77-110">Child elements</span></span>

<span data-ttu-id="a7c77-111">[ItemID](itemid.md)  |  [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md)  |  [ErrorDescription](errordescription.md)  |  [IsPartiallyIndexed](ispartiallyindexed.md)  |  [IsPermanentFailure](ispermanentfailure.md)  |  [Sortvalue](sortvalue.md)  |  [AttemptCount](attemptcount.md)  |  [LastAttemptTime](lastattempttime.md)  |  [AdditionalInfo](additionalinfo.md)</span><span class="sxs-lookup"><span data-stu-id="a7c77-111">[ItemId](itemid.md) | [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md) | [ErrorDescription](errordescription.md) | [IsPartiallyIndexed](ispartiallyindexed.md) | [IsPermanentFailure](ispermanentfailure.md) | [SortValue](sortvalue.md) | [AttemptCount](attemptcount.md) | [LastAttemptTime](lastattempttime.md) | [AdditionalInfo](additionalinfo.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a7c77-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7c77-112">Parent elements</span></span>

[<span data-ttu-id="a7c77-113">Elemente (ArrayOfNonIndexableItemDetailsType)</span><span class="sxs-lookup"><span data-stu-id="a7c77-113">Items (ArrayOfNonIndexableItemDetailsType)</span></span>](items-arrayofnonindexableitemdetailstype.md)
  
## <a name="remarks"></a><span data-ttu-id="a7c77-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7c77-114">Remarks</span></span>

<span data-ttu-id="a7c77-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a7c77-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a7c77-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a7c77-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7c77-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a7c77-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7c77-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7c77-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a7c77-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a7c77-119">Schema name</span></span>  <br/> |<span data-ttu-id="a7c77-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a7c77-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="a7c77-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a7c77-121">Validation file</span></span>  <br/> |<span data-ttu-id="a7c77-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a7c77-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a7c77-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a7c77-123">Can be empty</span></span>  <br/> ||
   

