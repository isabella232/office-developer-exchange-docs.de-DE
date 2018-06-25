---
title: FreeBusyAccessLevel (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a287b9c3-7fb6-4f2f-a8dc-15d4bc32394c
description: Das Element FreeBusyAccessLevel stellt die FreeBusyAccessLevel-Eigenschaft. Das FreeBusyAccessLevel-Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: c978608982a2795af1683b4b2121435a02149935
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758540"
---
# <a name="freebusyaccesslevel-soap"></a><span data-ttu-id="1f52e-105">FreeBusyAccessLevel (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1f52e-105">FreeBusyAccessLevel (SOAP)</span></span>

<span data-ttu-id="1f52e-106">Das Element **FreeBusyAccessLevel** stellt die **FreeBusyAccessLevel** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1f52e-106">The **FreeBusyAccessLevel** element represents the **FreeBusyAccessLevel** property.</span></span> <span data-ttu-id="1f52e-107">Das **FreeBusyAccessLevel** -Element ist nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="1f52e-107">The **FreeBusyAccessLevel** element is for internal use only.</span></span> <span data-ttu-id="1f52e-108">Dieses Element wird von Clients nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f52e-108">This element is not used by clients.</span></span> 
  
```XML
<FreeBusyAccessLevel/>
```

 <span data-ttu-id="1f52e-109">**string**</span><span class="sxs-lookup"><span data-stu-id="1f52e-109">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f52e-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1f52e-110">Attributes and elements</span></span>

<span data-ttu-id="1f52e-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1f52e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f52e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f52e-112">Attributes</span></span>

<span data-ttu-id="1f52e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f52e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f52e-114">Child elements</span></span>

<span data-ttu-id="1f52e-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f52e-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f52e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f52e-116">Parent elements</span></span>

|<span data-ttu-id="1f52e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f52e-117">**Element**</span></span>|<span data-ttu-id="1f52e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f52e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f52e-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1f52e-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="1f52e-120">Stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation.</span><span class="sxs-lookup"><span data-stu-id="1f52e-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f52e-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f52e-121">Remarks</span></span>

<span data-ttu-id="1f52e-122">Dieses Element gibt die maximale Größe der Frei/Gebucht-Informationen Details, die in der Antwort zurückgegeben werden, und gibt den Umfang der Frei/Gebucht-Daten, die extern gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="1f52e-122">This element specifies the maximum amount of free/busy detail that will be returned in the response and indicates the level of free/busy data that is externally shared.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1f52e-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1f52e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f52e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f52e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="1f52e-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1f52e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1f52e-126">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="1f52e-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="1f52e-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1f52e-127">Validation File</span></span>  <br/> |<span data-ttu-id="1f52e-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1f52e-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1f52e-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1f52e-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="1f52e-130">True</span><span class="sxs-lookup"><span data-stu-id="1f52e-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f52e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f52e-131">See also</span></span>



[<span data-ttu-id="1f52e-132">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1f52e-132">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

