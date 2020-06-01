---
title: OrganizationRelationshipSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 917481bb-46fc-4b88-8683-4cf812dcb0ab
description: Das OrganizationRelationshipSettings-Element stellt eine Liste von Organisationsbeziehungen für eine einzelne Organisation dar. Das OrganizationRelationshipSettings-Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet.
ms.openlocfilehash: 383b3635e1435c6597ccf793a7990c411c02d36d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462458"
---
# <a name="organizationrelationshipsettings-soap"></a><span data-ttu-id="07c6f-105">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-105">OrganizationRelationshipSettings (SOAP)</span></span>

<span data-ttu-id="07c6f-106">Das **OrganizationRelationshipSettings** -Element stellt eine Liste von Organisationsbeziehungen für eine einzelne Organisation dar.</span><span class="sxs-lookup"><span data-stu-id="07c6f-106">The **OrganizationRelationshipSettings** element represents a list of organization relationships for a single organization.</span></span> <span data-ttu-id="07c6f-107">Das **OrganizationRelationshipSettings** -Element ist nur für die interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="07c6f-107">The **OrganizationRelationshipSettings** element is for internal use only.</span></span> <span data-ttu-id="07c6f-108">Dieses Element wird nicht von Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="07c6f-108">This element is not used by clients.</span></span> 
  
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

 <span data-ttu-id="07c6f-109">**OrganizationRelationshipSettings**</span><span class="sxs-lookup"><span data-stu-id="07c6f-109">**OrganizationRelationshipSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07c6f-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="07c6f-110">Attributes and elements</span></span>

<span data-ttu-id="07c6f-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="07c6f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07c6f-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="07c6f-112">Attributes</span></span>

<span data-ttu-id="07c6f-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="07c6f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07c6f-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07c6f-114">Child elements</span></span>

|<span data-ttu-id="07c6f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="07c6f-115">**Element**</span></span>|<span data-ttu-id="07c6f-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07c6f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07c6f-117">DeliveryReportEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-117">DeliveryReportEnabled (SOAP)</span></span>](deliveryreportenabled-soap.md) <br/> |<span data-ttu-id="07c6f-118">Stellt das [DeliveryReportEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx) -Flag dar.</span><span class="sxs-lookup"><span data-stu-id="07c6f-118">Represents the [DeliveryReportEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="07c6f-119">Domainnamen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-119">DomainNames (SOAP)</span></span>](domainnames-soap.md) <br/> |<span data-ttu-id="07c6f-120">Stellt die Auflistung der Domänennamen dar.</span><span class="sxs-lookup"><span data-stu-id="07c6f-120">Represents the domain names collection.</span></span>  <br/> |
|[<span data-ttu-id="07c6f-121">FreeBusyAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-121">FreeBusyAccessEnabled (SOAP)</span></span>](freebusyaccessenabled-soap.md) <br/> |<span data-ttu-id="07c6f-122">Stellt das [FreeBusyAccessEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx) -Flag dar.</span><span class="sxs-lookup"><span data-stu-id="07c6f-122">Represents the [FreeBusyAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="07c6f-123">FreeBusyAccessLevel (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-123">FreeBusyAccessLevel (SOAP)</span></span>](freebusyaccesslevel-soap.md) <br/> |<span data-ttu-id="07c6f-124">Stellt die [FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx) -Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="07c6f-124">Represents the [FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="07c6f-125">MailTipsAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-125">MailTipsAccessEnabled (SOAP)</span></span>](mailtipsaccessenabled-soap.md) <br/> |<span data-ttu-id="07c6f-126">Stellt das [MailTipsAccessEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx) -Flag dar.</span><span class="sxs-lookup"><span data-stu-id="07c6f-126">Represents the [MailTipsAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="07c6f-127">MailTipsAccessLevel (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-127">MailTipsAccessLevel (SOAP)</span></span>](mailtipsaccesslevel-soap.md) <br/> |<span data-ttu-id="07c6f-128">Stellt die [MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx) -Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="07c6f-128">Represents the [MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="07c6f-129">MailboxMoveEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-129">MailboxMoveEnabled (SOAP)</span></span>](mailboxmoveenabled-soap.md) <br/> |<span data-ttu-id="07c6f-130">Stellt das [MailboxMoveEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx) -Flag dar.</span><span class="sxs-lookup"><span data-stu-id="07c6f-130">Represents the [MailboxMoveEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="07c6f-131">Name (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-131">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="07c6f-132">Stellt den Namen der Organisationsbeziehung dar.</span><span class="sxs-lookup"><span data-stu-id="07c6f-132">Represents the name of the organization relationship.</span></span>  <br/> |
|[<span data-ttu-id="07c6f-133">TargetApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-133">TargetApplicationUri (SOAP)</span></span>](targetapplicationuri-soap.md) <br/> |<span data-ttu-id="07c6f-134">Definiert den URI der Zielanwendung.</span><span class="sxs-lookup"><span data-stu-id="07c6f-134">Defines the target application URI.</span></span>  <br/> |
|[<span data-ttu-id="07c6f-135">TargetAutodiscoverEpr (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-135">TargetAutodiscoverEpr (SOAP)</span></span>](targetautodiscoverepr-soap.md) <br/> |<span data-ttu-id="07c6f-136">Stellt die [TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx) -Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="07c6f-136">Represents the [TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="07c6f-137">TargetSharingEpr (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-137">TargetSharingEpr (SOAP)</span></span>](targetsharingepr-soap.md) <br/> |<span data-ttu-id="07c6f-138">Stellt die [TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx) -Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="07c6f-138">Represents the [TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx) property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="07c6f-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07c6f-139">Parent elements</span></span>

|<span data-ttu-id="07c6f-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="07c6f-140">**Element**</span></span>|<span data-ttu-id="07c6f-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07c6f-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07c6f-142">OrganizationRelationshipSettingsCollection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="07c6f-142">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="07c6f-143">Stellt eine Liste von Organisationsbeziehungen dar, die mit der Abfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="07c6f-143">Represents a list of organization relationships that match the query.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="07c6f-144">Textwert</span><span class="sxs-lookup"><span data-stu-id="07c6f-144">Text value</span></span>

<span data-ttu-id="07c6f-145">Keine.</span><span class="sxs-lookup"><span data-stu-id="07c6f-145">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07c6f-146">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="07c6f-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07c6f-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="07c6f-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="07c6f-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="07c6f-148">Schema Name</span></span>  <br/> |<span data-ttu-id="07c6f-149">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="07c6f-149">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="07c6f-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="07c6f-150">Validation File</span></span>  <br/> |<span data-ttu-id="07c6f-151">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="07c6f-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="07c6f-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="07c6f-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="07c6f-153">True</span><span class="sxs-lookup"><span data-stu-id="07c6f-153">True</span></span>  <br/> |
   

