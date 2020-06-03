---
title: Antwort (GetOrganizationRelationship) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e6bbe800-3cbc-48b2-87b3-2043f575e88b
description: Das Response-Element enthält die GetOrganizationRelationshipSettings-Vorgangs (SOAP)-Antwortinformationen. Das Response-Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet.
ms.openlocfilehash: 55f8cd549f40b780b2e7438634a851a2c3854f40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467942"
---
# <a name="response-getorganizationrelationship-soap"></a><span data-ttu-id="0c7d4-105">Antwort (GetOrganizationRelationship) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0c7d4-105">Response (GetOrganizationRelationship) (SOAP)</span></span>

<span data-ttu-id="0c7d4-106">Das **Response** -Element enthält die [GetOrganizationRelationshipSettings-Vorgangs (SOAP)-](getorganizationrelationshipsettings-operation-soap.md) Antwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="0c7d4-106">The **Response** element contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response information.</span></span> <span data-ttu-id="0c7d4-107">Das **Response** -Element ist nur für die interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="0c7d4-107">The **Response** element is for internal use only.</span></span> <span data-ttu-id="0c7d4-108">Dieses Element wird nicht von Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c7d4-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <OrganizationRelationshipSettingsCollection/>
</GetOrganizationRelationshipSettingResponse>
```

 <span data-ttu-id="0c7d4-109">**GetOrganizationRelationshipSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="0c7d4-109">**GetOrganizationRelationshipSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c7d4-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0c7d4-110">Attributes and elements</span></span>

<span data-ttu-id="0c7d4-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0c7d4-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c7d4-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="0c7d4-112">Attributes</span></span>

<span data-ttu-id="0c7d4-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c7d4-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c7d4-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c7d4-114">Child elements</span></span>

|<span data-ttu-id="0c7d4-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c7d4-115">**Element**</span></span>|<span data-ttu-id="0c7d4-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c7d4-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c7d4-117">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0c7d4-117">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="0c7d4-118">Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0c7d4-118">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="0c7d4-119">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0c7d4-119">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="0c7d4-120">Stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0c7d4-120">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="0c7d4-121">OrganizationRelationshipSettingsCollection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0c7d4-121">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="0c7d4-122">Stellt eine Liste von Organisationsbeziehungen dar, die mit der Abfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0c7d4-122">Represents a list of organization relationships that match the query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0c7d4-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c7d4-123">Parent elements</span></span>

<span data-ttu-id="0c7d4-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c7d4-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="0c7d4-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="0c7d4-125">Text value</span></span>

<span data-ttu-id="0c7d4-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c7d4-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c7d4-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0c7d4-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c7d4-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c7d4-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="0c7d4-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0c7d4-129">Schema Name</span></span>  <br/> |<span data-ttu-id="0c7d4-130">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="0c7d4-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="0c7d4-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0c7d4-131">Validation File</span></span>  <br/> |<span data-ttu-id="0c7d4-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0c7d4-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0c7d4-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0c7d4-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="0c7d4-134">True</span><span class="sxs-lookup"><span data-stu-id="0c7d4-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c7d4-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c7d4-135">See also</span></span>



[<span data-ttu-id="0c7d4-136">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0c7d4-136">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

