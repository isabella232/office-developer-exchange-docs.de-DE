---
title: FreeBusyAccessEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8d2d3276-b180-424e-a707-7256d14a1776
description: Das FreeBusyAccessEnabled-Element darstellt, das FreeBusyAccessEnabled()-Flag. Das FreeBusyAccessEnabled-Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: 4727e7054c02a4b5d454cb880691ecc01a075327
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758541"
---
# <a name="freebusyaccessenabled-soap"></a><span data-ttu-id="7da59-105">FreeBusyAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7da59-105">FreeBusyAccessEnabled (SOAP)</span></span>

<span data-ttu-id="7da59-106">Das **FreeBusyAccessEnabled** -Element darstellt, das **FreeBusyAccessEnabled()** -Flag.</span><span class="sxs-lookup"><span data-stu-id="7da59-106">The **FreeBusyAccessEnabled** element represents the **FreeBusyAccessEnabled()** flag.</span></span> <span data-ttu-id="7da59-107">Das **FreeBusyAccessEnabled** -Element ist nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="7da59-107">The **FreeBusyAccessEnabled** element is for internal use only.</span></span> <span data-ttu-id="7da59-108">Dieses Element wird von Clients nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7da59-108">This element is not used by clients.</span></span> 
  
```XML
<FreeBusyAccessEnabled>true | false</FreeBusyAccessEnabled>
```

 <span data-ttu-id="7da59-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7da59-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7da59-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7da59-110">Attributes and elements</span></span>

<span data-ttu-id="7da59-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7da59-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7da59-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="7da59-112">Attributes</span></span>

<span data-ttu-id="7da59-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="7da59-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7da59-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7da59-114">Child elements</span></span>

<span data-ttu-id="7da59-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="7da59-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7da59-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7da59-116">Parent elements</span></span>

|<span data-ttu-id="7da59-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7da59-117">**Element**</span></span>|<span data-ttu-id="7da59-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7da59-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7da59-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7da59-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="7da59-120">Stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation.</span><span class="sxs-lookup"><span data-stu-id="7da59-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7da59-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="7da59-121">Text value</span></span>

<span data-ttu-id="7da59-122">Der Textwert **true** für das Element **FreeBusyAccessEnabled** gibt an, dass die Beziehung zum Abrufen von Frei/Gebucht-Informationen von Benutzern in der Organisation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7da59-122">A text value of **true** for the **FreeBusyAccessEnabled** element indicates that the sharing relationship should be used to retrieve free busy information from users in the organization.</span></span> <span data-ttu-id="7da59-123">Der Wert **false** gibt an, dass die Beziehung unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7da59-123">A value of **false** indicates that the sharing relationship should be suppressed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7da59-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7da59-124">Remarks</span></span>

<span data-ttu-id="7da59-125">Verwenden Sie dieses Element zulassen oder Unterdrücken von Frei/Gebucht-Informationen vom Server.</span><span class="sxs-lookup"><span data-stu-id="7da59-125">Use this element to allow or suppress free/busy information from the server.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7da59-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7da59-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7da59-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="7da59-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7da59-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7da59-128">Schema Name</span></span>  <br/> |<span data-ttu-id="7da59-129">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="7da59-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7da59-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7da59-130">Validation File</span></span>  <br/> |<span data-ttu-id="7da59-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7da59-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7da59-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7da59-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="7da59-133">True</span><span class="sxs-lookup"><span data-stu-id="7da59-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7da59-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7da59-134">See also</span></span>



[<span data-ttu-id="7da59-135">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7da59-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

