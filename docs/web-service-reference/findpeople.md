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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462901"
---
# <a name="findpeople"></a><span data-ttu-id="b40b1-104">FindPeople</span><span class="sxs-lookup"><span data-stu-id="b40b1-104">FindPeople</span></span>

<span data-ttu-id="b40b1-105">Das **FindPeople** -Element gibt eine Gruppe von Daten an, die in einer FindPeople-Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b40b1-105">The **FindPeople** element specifies a set of data used in a FindPeople request.</span></span> <span data-ttu-id="b40b1-106">Die Daten enthalten keine oder mehrere der folgenden Elemente: eine persona-Form (optional), eine indizierte Seitenelement Ansicht, eine Einschränkung (optional), eine Aggregations Einschränkung (optional), eine Sortierreihenfolge (optional), eine übergeordnete Ordner-ID und eine Abfragezeichenfolge (optional).</span><span class="sxs-lookup"><span data-stu-id="b40b1-106">The data includes zero or more of the following elements: a persona shape (optional), an indexed page item view, a restriction (optional), an aggregation restriction (optional), a sort order (optional), a parent folder Id, and a query string (optional).</span></span> 
  
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

 <span data-ttu-id="b40b1-107">**FindPeopleType**</span><span class="sxs-lookup"><span data-stu-id="b40b1-107">**FindPeopleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b40b1-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b40b1-108">Attributes and elements</span></span>

<span data-ttu-id="b40b1-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b40b1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b40b1-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="b40b1-110">Attributes</span></span>

<span data-ttu-id="b40b1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b40b1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b40b1-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b40b1-112">Child elements</span></span>

<span data-ttu-id="b40b1-113">[PersonaShape](personashape.md)  |  [IndexedPageItemView](indexedpageitemview.md)  |  [Einschränkung](restriction.md)  |  [AggregationRestriction](aggregationrestriction.md)  |  [Sortierreihenfolge](sortorder.md)  |  [Parentfolderid (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [QueryString (](querystring-querystringtype.md) querystringtype)</span><span class="sxs-lookup"><span data-stu-id="b40b1-113">[PersonaShape](personashape.md) | [IndexedPageItemView](indexedpageitemview.md) | [Restriction](restriction.md) | [AggregationRestriction](aggregationrestriction.md) | [SortOrder](sortorder.md) | [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [QueryString (QueryStringType)](querystring-querystringtype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b40b1-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b40b1-114">Parent elements</span></span>

<span data-ttu-id="b40b1-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="b40b1-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b40b1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b40b1-116">Remarks</span></span>

<span data-ttu-id="b40b1-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b40b1-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b40b1-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b40b1-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b40b1-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b40b1-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b40b1-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="b40b1-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b40b1-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b40b1-121">Schema name</span></span>  <br/> |<span data-ttu-id="b40b1-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b40b1-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b40b1-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b40b1-123">Validation file</span></span>  <br/> |<span data-ttu-id="b40b1-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b40b1-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b40b1-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b40b1-125">Can be empty</span></span>  <br/> |<span data-ttu-id="b40b1-126">False</span><span class="sxs-lookup"><span data-stu-id="b40b1-126">false</span></span>  <br/> |
   

