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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758473"
---
# <a name="findpeople"></a><span data-ttu-id="1c304-104">FindPeople</span><span class="sxs-lookup"><span data-stu-id="1c304-104">FindPeople</span></span>

<span data-ttu-id="1c304-105">Das **FindPeople** -Element gibt einen Satz von Daten in einer Anforderung FindPeople verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c304-105">The **FindPeople** element specifies a set of data used in a FindPeople request.</span></span> <span data-ttu-id="1c304-106">Die Daten enthalten, 0 (null) oder mehrere der folgenden Elemente: eine Rolle Form (optional), einem indizierten Element Seitenansicht, eine Einschränkung (optional), eine Aggregation Einschränkung (optional), eine Sortierreihenfolge (optional), eine Id des übergeordneten Ordners und eine Abfragezeichenfolge (optional).</span><span class="sxs-lookup"><span data-stu-id="1c304-106">The data includes zero or more of the following elements: a persona shape (optional), an indexed page item view, a restriction (optional), an aggregation restriction (optional), a sort order (optional), a parent folder Id, and a query string (optional).</span></span> 
  
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

 <span data-ttu-id="1c304-107">**FindPeopleType**</span><span class="sxs-lookup"><span data-stu-id="1c304-107">**FindPeopleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c304-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1c304-108">Attributes and elements</span></span>

<span data-ttu-id="1c304-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1c304-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c304-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="1c304-110">Attributes</span></span>

<span data-ttu-id="1c304-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1c304-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c304-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c304-112">Child elements</span></span>

<span data-ttu-id="1c304-113">[PersonaShape](personashape.md) | [IndexedPageItemView](indexedpageitemview.md) | [Einschränkung](restriction.md) | [AggregationRestriction](aggregationrestriction.md) | [SortOrder](sortorder.md) | [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [ QueryString (QueryStringType)](querystring-querystringtype.md)</span><span class="sxs-lookup"><span data-stu-id="1c304-113">[PersonaShape](personashape.md) | [IndexedPageItemView](indexedpageitemview.md) | [Restriction](restriction.md) | [AggregationRestriction](aggregationrestriction.md) | [SortOrder](sortorder.md) | [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [QueryString (QueryStringType)](querystring-querystringtype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1c304-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c304-114">Parent elements</span></span>

<span data-ttu-id="1c304-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="1c304-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1c304-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c304-116">Remarks</span></span>

<span data-ttu-id="1c304-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1c304-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1c304-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1c304-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c304-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1c304-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c304-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c304-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1c304-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1c304-121">Schema name</span></span>  <br/> |<span data-ttu-id="1c304-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1c304-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1c304-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1c304-123">Validation file</span></span>  <br/> |<span data-ttu-id="1c304-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1c304-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1c304-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1c304-125">Can be empty</span></span>  <br/> |<span data-ttu-id="1c304-126">false</span><span class="sxs-lookup"><span data-stu-id="1c304-126">false</span></span>  <br/> |
   

