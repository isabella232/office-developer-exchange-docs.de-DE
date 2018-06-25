---
title: OrganizationRelationshipSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 917481bb-46fc-4b88-8683-4cf812dcb0ab
description: Das Element OrganizationRelationshipSettings stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation. Das OrganizationRelationshipSettings-Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: ed6cc0ef1891cd92c02a8e088e913886048623ee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830660"
---
# <a name="organizationrelationshipsettings-soap"></a><span data-ttu-id="ff316-105">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-105">OrganizationRelationshipSettings (SOAP)</span></span>

<span data-ttu-id="ff316-106">Das Element **OrganizationRelationshipSettings** stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation.</span><span class="sxs-lookup"><span data-stu-id="ff316-106">The **OrganizationRelationshipSettings** element represents a list of organization relationships for a single organization.</span></span> <span data-ttu-id="ff316-107">Das **OrganizationRelationshipSettings** -Element ist nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="ff316-107">The **OrganizationRelationshipSettings** element is for internal use only.</span></span> <span data-ttu-id="ff316-108">Dieses Element wird von Clients nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff316-108">This element is not used by clients.</span></span> 
  
```XML
<OrganizationRelationshipSettings>
    <DeliveryReportEnabled/>
    <DomainNames/>
    <FreeBusyAccessEnabled/>
    <FreeBusyAccessLevel/>
    <MailTipsAccessEnabled/>
    <MailTipsAccessLevel/>
    <MailboxMoveEnabled/>
    <Name/>
    <TargetApplicationUri/>
    <TargetAudodiscoverEpr/>
    <TargetSharingEpr/>
</OrganizationRelationshipSettings>
```

 <span data-ttu-id="ff316-109">**OrganizationRelationshipSettings**</span><span class="sxs-lookup"><span data-stu-id="ff316-109">**OrganizationRelationshipSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff316-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ff316-110">Attributes and elements</span></span>

<span data-ttu-id="ff316-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ff316-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff316-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="ff316-112">Attributes</span></span>

<span data-ttu-id="ff316-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ff316-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff316-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff316-114">Child elements</span></span>

|<span data-ttu-id="ff316-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff316-115">**Element**</span></span>|<span data-ttu-id="ff316-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff316-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff316-117">DeliveryReportEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-117">DeliveryReportEnabled (SOAP)</span></span>](deliveryreportenabled-soap.md) <br/> |<span data-ttu-id="ff316-118">Stellt das [DeliveryReportEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx) -Flag.</span><span class="sxs-lookup"><span data-stu-id="ff316-118">Represents the [DeliveryReportEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="ff316-119">DomainNames (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-119">DomainNames (SOAP)</span></span>](domainnames-soap.md) <br/> |<span data-ttu-id="ff316-120">Die Domain Names-Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ff316-120">Represents the domain names collection.</span></span>  <br/> |
|[<span data-ttu-id="ff316-121">FreeBusyAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-121">FreeBusyAccessEnabled (SOAP)</span></span>](freebusyaccessenabled-soap.md) <br/> |<span data-ttu-id="ff316-122">Stellt das [FreeBusyAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx) -Flag.</span><span class="sxs-lookup"><span data-stu-id="ff316-122">Represents the [FreeBusyAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="ff316-123">FreeBusyAccessLevel (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-123">FreeBusyAccessLevel (SOAP)</span></span>](freebusyaccesslevel-soap.md) <br/> |<span data-ttu-id="ff316-124">Stellt die [FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ff316-124">Represents the [FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="ff316-125">MailTipsAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-125">MailTipsAccessEnabled (SOAP)</span></span>](mailtipsaccessenabled-soap.md) <br/> |<span data-ttu-id="ff316-126">Stellt das [MailTipsAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx) -Flag.</span><span class="sxs-lookup"><span data-stu-id="ff316-126">Represents the [MailTipsAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="ff316-127">MailTipsAccessLevel (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-127">MailTipsAccessLevel (SOAP)</span></span>](mailtipsaccesslevel-soap.md) <br/> |<span data-ttu-id="ff316-128">Stellt die [MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ff316-128">Represents the [MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="ff316-129">MailboxMoveEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-129">MailboxMoveEnabled (SOAP)</span></span>](mailboxmoveenabled-soap.md) <br/> |<span data-ttu-id="ff316-130">Stellt das [MailboxMoveEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx) -Flag.</span><span class="sxs-lookup"><span data-stu-id="ff316-130">Represents the [MailboxMoveEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="ff316-131">Name (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-131">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="ff316-132">Stellt den Namen der organisationsbeziehung an.</span><span class="sxs-lookup"><span data-stu-id="ff316-132">Represents the name of the organization relationship.</span></span>  <br/> |
|[<span data-ttu-id="ff316-133">TargetApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-133">TargetApplicationUri (SOAP)</span></span>](targetapplicationuri-soap.md) <br/> |<span data-ttu-id="ff316-134">Definiert die URI-Zielanwendung.</span><span class="sxs-lookup"><span data-stu-id="ff316-134">Defines the target application URI.</span></span>  <br/> |
|[<span data-ttu-id="ff316-135">TargetAutodiscoverEpr (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-135">TargetAutodiscoverEpr (SOAP)</span></span>](targetautodiscoverepr-soap.md) <br/> |<span data-ttu-id="ff316-136">Stellt die [TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ff316-136">Represents the [TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="ff316-137">TargetSharingEpr (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-137">TargetSharingEpr (SOAP)</span></span>](targetsharingepr-soap.md) <br/> |<span data-ttu-id="ff316-138">Stellt die [TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ff316-138">Represents the [TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx) property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ff316-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff316-139">Parent elements</span></span>

|<span data-ttu-id="ff316-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff316-140">**Element**</span></span>|<span data-ttu-id="ff316-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff316-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff316-142">OrganizationRelationshipSettingsCollection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff316-142">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="ff316-143">Stellt eine Liste von organisationsbeziehungen, die mit die Abfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="ff316-143">Represents a list of organization relationships that match the query.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ff316-144">Textwert</span><span class="sxs-lookup"><span data-stu-id="ff316-144">Text value</span></span>

<span data-ttu-id="ff316-145">Keine.</span><span class="sxs-lookup"><span data-stu-id="ff316-145">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff316-146">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ff316-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff316-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff316-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ff316-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ff316-148">Schema Name</span></span>  <br/> |<span data-ttu-id="ff316-149">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="ff316-149">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ff316-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ff316-150">Validation File</span></span>  <br/> |<span data-ttu-id="ff316-151">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ff316-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ff316-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ff316-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff316-153">True</span><span class="sxs-lookup"><span data-stu-id="ff316-153">True</span></span>  <br/> |
   

