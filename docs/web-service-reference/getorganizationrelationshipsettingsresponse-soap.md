---
title: GetOrganizationRelationshipSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f43b817-92c2-4e04-8095-479d790f768c
description: Das GetOrganizationRelationshipSettingsResponse-Element enthält die GetOrganizationRelationshipSettings-Vorgang (SOAP)-Antwort. Das GetOrganizationRelationshipSettingsResponse-Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet.
ms.openlocfilehash: 0f34fbc6577b379dd0ac379564c5e6bbd940d379
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457921"
---
# <a name="getorganizationrelationshipsettingsresponse-soap"></a><span data-ttu-id="7367d-105">GetOrganizationRelationshipSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7367d-105">GetOrganizationRelationshipSettingsResponse (SOAP)</span></span>

<span data-ttu-id="7367d-106">Das **GetOrganizationRelationshipSettingsResponse** -Element enthält die [GetOrganizationRelationshipSettings-Vorgang (SOAP)-](getorganizationrelationshipsettings-operation-soap.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="7367d-106">The **GetOrganizationRelationshipSettingsResponse** element contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response.</span></span> <span data-ttu-id="7367d-107">Das **GetOrganizationRelationshipSettingsResponse** -Element ist nur für die interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="7367d-107">The **GetOrganizationRelationshipSettingsResponse** element is for internal use only.</span></span> <span data-ttu-id="7367d-108">Dieses Element wird nicht von Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="7367d-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <OrganizationRelationshipSettingsCollection/>
</GetOrganizationRelationshipSettingResponse>
```

 <span data-ttu-id="7367d-109">**GetOrganizationRelationshipSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="7367d-109">**GetOrganizationRelationshipSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7367d-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7367d-110">Attributes and elements</span></span>

<span data-ttu-id="7367d-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7367d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7367d-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="7367d-112">Attributes</span></span>

<span data-ttu-id="7367d-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="7367d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7367d-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7367d-114">Child elements</span></span>

|<span data-ttu-id="7367d-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="7367d-115">**Element**</span></span>|<span data-ttu-id="7367d-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7367d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7367d-117">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7367d-117">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="7367d-118">Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7367d-118">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="7367d-119">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7367d-119">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="7367d-120">Stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7367d-120">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="7367d-121">OrganizationRelationshipSettingsCollection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7367d-121">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="7367d-122">Stellt eine Auflistung von Organisationsbeziehungen dar, die mit der Abfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7367d-122">Represents a collection of organization relationships that match the query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7367d-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7367d-123">Parent elements</span></span>

<span data-ttu-id="7367d-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="7367d-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7367d-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="7367d-125">Text value</span></span>

<span data-ttu-id="7367d-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="7367d-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7367d-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7367d-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7367d-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="7367d-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7367d-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7367d-129">Schema Name</span></span>  <br/> |<span data-ttu-id="7367d-130">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="7367d-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7367d-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7367d-131">Validation File</span></span>  <br/> |<span data-ttu-id="7367d-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7367d-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7367d-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7367d-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="7367d-134">True</span><span class="sxs-lookup"><span data-stu-id="7367d-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7367d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7367d-135">See also</span></span>



[<span data-ttu-id="7367d-136">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7367d-136">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

