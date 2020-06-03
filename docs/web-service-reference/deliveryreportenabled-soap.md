---
title: DeliveryReportEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ab522bc-40ea-4e43-aa57-6d2562db35e9
description: Das DeliveryReportEnabled-Element stellt das DeliveryReportEnabled ()-Flag dar. Das DeliveryReportEnabled-Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet.
ms.openlocfilehash: 2a163b3e6ceaa169cc8f76f395b7d501419a31ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458474"
---
# <a name="deliveryreportenabled-soap"></a><span data-ttu-id="692b0-105">DeliveryReportEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="692b0-105">DeliveryReportEnabled (SOAP)</span></span>

<span data-ttu-id="692b0-106">Das **DeliveryReportEnabled** -Element stellt das **DeliveryReportEnabled ()** -Flag dar.</span><span class="sxs-lookup"><span data-stu-id="692b0-106">The **DeliveryReportEnabled** element represents the **DeliveryReportEnabled()** flag.</span></span> <span data-ttu-id="692b0-107">Das **DeliveryReportEnabled** -Element ist nur für die interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="692b0-107">The **DeliveryReportEnabled** element is for internal use only.</span></span> <span data-ttu-id="692b0-108">Dieses Element wird nicht von Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="692b0-108">This element is not used by clients.</span></span> 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
```

 <span data-ttu-id="692b0-109">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="692b0-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="692b0-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="692b0-110">Attributes and elements</span></span>

<span data-ttu-id="692b0-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="692b0-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="692b0-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="692b0-112">Attributes</span></span>

<span data-ttu-id="692b0-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="692b0-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="692b0-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="692b0-114">Child elements</span></span>

<span data-ttu-id="692b0-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="692b0-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="692b0-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="692b0-116">Parent elements</span></span>

|<span data-ttu-id="692b0-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="692b0-117">**Element**</span></span>|<span data-ttu-id="692b0-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="692b0-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="692b0-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="692b0-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="692b0-120">Stellt eine Liste von Organisationsbeziehungen für eine einzelne Organisation dar.</span><span class="sxs-lookup"><span data-stu-id="692b0-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="692b0-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="692b0-121">Text value</span></span>

<span data-ttu-id="692b0-122">Der Textwert true für das DeliveryReportEnabled-Element gibt an, dass die Zustellungsberichte von Benutzern in der Organisation verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="692b0-122">A text value of true for the DeliveryReportEnabled element indicates that the delivery reports from users in the organization can be used.</span></span> <span data-ttu-id="692b0-123">Der Wert false gibt an, dass die Zustellungsberichte unterdrückt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="692b0-123">A value of false indicates that the delivery reports should suppressed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="692b0-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="692b0-124">Remarks</span></span>

<span data-ttu-id="692b0-125">Verwenden Sie dieses Element, um Zustellungsberichte vom Server zuzulassen oder zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="692b0-125">Use this element to allow or suppress delivery reports from the server.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="692b0-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="692b0-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="692b0-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="692b0-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="692b0-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="692b0-128">Schema Name</span></span>  <br/> |<span data-ttu-id="692b0-129">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="692b0-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="692b0-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="692b0-130">Validation File</span></span>  <br/> |<span data-ttu-id="692b0-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="692b0-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="692b0-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="692b0-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="692b0-133">True</span><span class="sxs-lookup"><span data-stu-id="692b0-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="692b0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="692b0-134">See also</span></span>

- [<span data-ttu-id="692b0-135">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="692b0-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

