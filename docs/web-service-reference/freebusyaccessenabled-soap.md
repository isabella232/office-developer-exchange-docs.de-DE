---
title: FreeBusyAccessEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8d2d3276-b180-424e-a707-7256d14a1776
description: Das FreeBusyAccessEnabled-Element stellt das FreeBusyAccessEnabled ()-Flag dar. Das FreeBusyAccessEnabled-Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet.
ms.openlocfilehash: c148d8fa1301339f8579884dc02b6c9e452f3035
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461296"
---
# <a name="freebusyaccessenabled-soap"></a><span data-ttu-id="24fa2-105">FreeBusyAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="24fa2-105">FreeBusyAccessEnabled (SOAP)</span></span>

<span data-ttu-id="24fa2-106">Das **FreeBusyAccessEnabled** -Element stellt das **FreeBusyAccessEnabled ()** -Flag dar.</span><span class="sxs-lookup"><span data-stu-id="24fa2-106">The **FreeBusyAccessEnabled** element represents the **FreeBusyAccessEnabled()** flag.</span></span> <span data-ttu-id="24fa2-107">Das **FreeBusyAccessEnabled** -Element ist nur für die interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="24fa2-107">The **FreeBusyAccessEnabled** element is for internal use only.</span></span> <span data-ttu-id="24fa2-108">Dieses Element wird nicht von Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="24fa2-108">This element is not used by clients.</span></span> 
  
```XML
<FreeBusyAccessEnabled>true | false</FreeBusyAccessEnabled>
```

 <span data-ttu-id="24fa2-109">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="24fa2-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="24fa2-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="24fa2-110">Attributes and elements</span></span>

<span data-ttu-id="24fa2-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="24fa2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24fa2-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="24fa2-112">Attributes</span></span>

<span data-ttu-id="24fa2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="24fa2-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="24fa2-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24fa2-114">Child elements</span></span>

<span data-ttu-id="24fa2-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="24fa2-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="24fa2-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24fa2-116">Parent elements</span></span>

|<span data-ttu-id="24fa2-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="24fa2-117">**Element**</span></span>|<span data-ttu-id="24fa2-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24fa2-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24fa2-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="24fa2-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="24fa2-120">Stellt eine Liste von Organisationsbeziehungen für eine einzelne Organisation dar.</span><span class="sxs-lookup"><span data-stu-id="24fa2-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="24fa2-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="24fa2-121">Text value</span></span>

<span data-ttu-id="24fa2-122">Der Textwert **true** für das **FreeBusyAccessEnabled** -Element gibt an, dass die Freigabebeziehung zum Abrufen von Frei/Gebucht-Informationen von Benutzern in der Organisation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="24fa2-122">A text value of **true** for the **FreeBusyAccessEnabled** element indicates that the sharing relationship should be used to retrieve free busy information from users in the organization.</span></span> <span data-ttu-id="24fa2-123">Der Wert **false** gibt an, dass die Freigabebeziehung unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="24fa2-123">A value of **false** indicates that the sharing relationship should be suppressed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="24fa2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24fa2-124">Remarks</span></span>

<span data-ttu-id="24fa2-125">Verwenden Sie dieses Element, um Frei/Gebucht-Informationen vom Server zuzulassen oder zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="24fa2-125">Use this element to allow or suppress free/busy information from the server.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="24fa2-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="24fa2-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24fa2-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="24fa2-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="24fa2-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="24fa2-128">Schema Name</span></span>  <br/> |<span data-ttu-id="24fa2-129">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="24fa2-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="24fa2-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="24fa2-130">Validation File</span></span>  <br/> |<span data-ttu-id="24fa2-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="24fa2-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="24fa2-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="24fa2-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="24fa2-133">True</span><span class="sxs-lookup"><span data-stu-id="24fa2-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24fa2-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24fa2-134">See also</span></span>



[<span data-ttu-id="24fa2-135">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="24fa2-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

