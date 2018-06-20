---
title: DeliveryReportEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ab522bc-40ea-4e43-aa57-6d2562db35e9
description: Das DeliveryReportEnabled-Element darstellt, das DeliveryReportEnabled()-Flag. Das DeliveryReportEnabled-Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: 089256a5f75ad92a4f11c5aaf3d175382eeee456
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757949"
---
# <a name="deliveryreportenabled-soap"></a><span data-ttu-id="da846-105">DeliveryReportEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="da846-105">DeliveryReportEnabled (SOAP)</span></span>

<span data-ttu-id="da846-106">Das **DeliveryReportEnabled** -Element darstellt, das **DeliveryReportEnabled()** -Flag.</span><span class="sxs-lookup"><span data-stu-id="da846-106">The **DeliveryReportEnabled** element represents the **DeliveryReportEnabled()** flag.</span></span> <span data-ttu-id="da846-107">Das **DeliveryReportEnabled** -Element ist nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="da846-107">The **DeliveryReportEnabled** element is for internal use only.</span></span> <span data-ttu-id="da846-108">Dieses Element wird von Clients nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="da846-108">This element is not used by clients.</span></span> 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
```

 <span data-ttu-id="da846-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="da846-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da846-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="da846-110">Attributes and elements</span></span>

<span data-ttu-id="da846-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="da846-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da846-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="da846-112">Attributes</span></span>

<span data-ttu-id="da846-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="da846-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da846-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da846-114">Child elements</span></span>

<span data-ttu-id="da846-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="da846-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="da846-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da846-116">Parent elements</span></span>

|<span data-ttu-id="da846-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="da846-117">**Element**</span></span>|<span data-ttu-id="da846-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da846-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da846-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="da846-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="da846-120">Stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation.</span><span class="sxs-lookup"><span data-stu-id="da846-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="da846-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="da846-121">Text value</span></span>

<span data-ttu-id="da846-122">Der Textwert True für das Element DeliveryReportEnabled gibt an, dass die Übermittlungsberichte von Benutzern in der Organisation verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="da846-122">A text value of true for the DeliveryReportEnabled element indicates that the delivery reports from users in the organization can be used.</span></span> <span data-ttu-id="da846-123">Der Wert False gibt an, dass die Übermittlungsberichte unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="da846-123">A value of false indicates that the delivery reports should suppressed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da846-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="da846-124">Remarks</span></span>

<span data-ttu-id="da846-125">Verwenden Sie dieses Element zulassen oder unterdrücken Übermittlungsberichte vom Server.</span><span class="sxs-lookup"><span data-stu-id="da846-125">Use this element to allow or suppress delivery reports from the server.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da846-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="da846-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da846-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="da846-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="da846-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="da846-128">Schema Name</span></span>  <br/> |<span data-ttu-id="da846-129">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="da846-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="da846-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="da846-130">Validation File</span></span>  <br/> |<span data-ttu-id="da846-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="da846-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="da846-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="da846-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="da846-133">True</span><span class="sxs-lookup"><span data-stu-id="da846-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da846-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da846-134">See also</span></span>

- [<span data-ttu-id="da846-135">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="da846-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

