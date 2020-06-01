---
title: GetOrganizationRelationshipSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e8aa3b3-4bfc-40c3-b96b-9f7062b09309
description: Das GetOrganizationRelationshipSettingsRequest-Element stellt die Parameter eines Aufrufs an den GetOrganizationRelationshipSettings-Vorgang (SOAP) dar. Das GetOrganizationRelationshipSettingsRequest-Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet.
ms.openlocfilehash: 053bbb8cbe2ccdcf6d544ab1fc92bb81765997e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452734"
---
# <a name="getorganizationrelationshipsettingsrequest-soap"></a><span data-ttu-id="03ba1-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="03ba1-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>

<span data-ttu-id="03ba1-106">Das **GetOrganizationRelationshipSettingsRequest** -Element stellt die Parameter eines Aufrufs an den [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md) dar.</span><span class="sxs-lookup"><span data-stu-id="03ba1-106">The **GetOrganizationRelationshipSettingsRequest** element represents the parameters of a call to the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation.</span></span> <span data-ttu-id="03ba1-107">Das **GetOrganizationRelationshipSettingsRequest** -Element ist nur für die interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="03ba1-107">The **GetOrganizationRelationshipSettingsRequest** element is for internal use only.</span></span> <span data-ttu-id="03ba1-108">Dieses Element wird nicht von Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="03ba1-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsRequest>
   <Domains/>
</GetOrganizationRelationshipSettingsRequest>
```

 <span data-ttu-id="03ba1-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="03ba1-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="03ba1-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="03ba1-110">Attributes and elements</span></span>

<span data-ttu-id="03ba1-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="03ba1-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="03ba1-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="03ba1-112">Attributes</span></span>

<span data-ttu-id="03ba1-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="03ba1-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="03ba1-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="03ba1-114">Child elements</span></span>

|<span data-ttu-id="03ba1-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="03ba1-115">**Element**</span></span>|<span data-ttu-id="03ba1-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03ba1-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="03ba1-117">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="03ba1-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="03ba1-118">Stellt eine Auflistung von Domänen-IDs dar.</span><span class="sxs-lookup"><span data-stu-id="03ba1-118">Represents a collection of domain identifiers.</span></span>  <br/> |
|||
   
### <a name="parent-elements"></a><span data-ttu-id="03ba1-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="03ba1-119">Parent elements</span></span>

<span data-ttu-id="03ba1-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="03ba1-120">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="03ba1-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="03ba1-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03ba1-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="03ba1-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="03ba1-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="03ba1-123">Schema Name</span></span>  <br/> |<span data-ttu-id="03ba1-124">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="03ba1-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="03ba1-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="03ba1-125">Validation File</span></span>  <br/> |<span data-ttu-id="03ba1-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="03ba1-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="03ba1-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="03ba1-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="03ba1-128">True</span><span class="sxs-lookup"><span data-stu-id="03ba1-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03ba1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03ba1-129">See also</span></span>



[<span data-ttu-id="03ba1-130">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="03ba1-130">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

