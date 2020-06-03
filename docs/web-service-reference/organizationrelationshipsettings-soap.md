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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462458"
---
# <a name="organizationrelationshipsettings-soap"></a><span data-ttu-id="8befd-105">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-105">OrganizationRelationshipSettings (SOAP)</span></span>

<span data-ttu-id="8befd-106">Das **OrganizationRelationshipSettings** -Element stellt eine Liste von Organisationsbeziehungen für eine einzelne Organisation dar.</span><span class="sxs-lookup"><span data-stu-id="8befd-106">The **OrganizationRelationshipSettings** element represents a list of organization relationships for a single organization.</span></span> <span data-ttu-id="8befd-107">Das **OrganizationRelationshipSettings** -Element ist nur für die interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="8befd-107">The **OrganizationRelationshipSettings** element is for internal use only.</span></span> <span data-ttu-id="8befd-108">Dieses Element wird nicht von Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="8befd-108">This element is not used by clients.</span></span> 
  
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

 <span data-ttu-id="8befd-109">**OrganizationRelationshipSettings**</span><span class="sxs-lookup"><span data-stu-id="8befd-109">**OrganizationRelationshipSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8befd-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8befd-110">Attributes and elements</span></span>

<span data-ttu-id="8befd-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8befd-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8befd-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="8befd-112">Attributes</span></span>

<span data-ttu-id="8befd-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8befd-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8befd-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8befd-114">Child elements</span></span>

|<span data-ttu-id="8befd-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="8befd-115">**Element**</span></span>|<span data-ttu-id="8befd-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8befd-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8befd-117">DeliveryReportEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-117">DeliveryReportEnabled (SOAP)</span></span>](deliveryreportenabled-soap.md) <br/> |<span data-ttu-id="8befd-118">Stellt das [DeliveryReportEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx) -Flag dar.</span><span class="sxs-lookup"><span data-stu-id="8befd-118">Represents the [DeliveryReportEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="8befd-119">Domainnamen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-119">DomainNames (SOAP)</span></span>](domainnames-soap.md) <br/> |<span data-ttu-id="8befd-120">Stellt die Auflistung der Domänennamen dar.</span><span class="sxs-lookup"><span data-stu-id="8befd-120">Represents the domain names collection.</span></span>  <br/> |
|[<span data-ttu-id="8befd-121">FreeBusyAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-121">FreeBusyAccessEnabled (SOAP)</span></span>](freebusyaccessenabled-soap.md) <br/> |<span data-ttu-id="8befd-122">Stellt das [FreeBusyAccessEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx) -Flag dar.</span><span class="sxs-lookup"><span data-stu-id="8befd-122">Represents the [FreeBusyAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="8befd-123">FreeBusyAccessLevel (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-123">FreeBusyAccessLevel (SOAP)</span></span>](freebusyaccesslevel-soap.md) <br/> |<span data-ttu-id="8befd-124">Stellt die [FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx) -Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="8befd-124">Represents the [FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="8befd-125">MailTipsAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-125">MailTipsAccessEnabled (SOAP)</span></span>](mailtipsaccessenabled-soap.md) <br/> |<span data-ttu-id="8befd-126">Stellt das [MailTipsAccessEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx) -Flag dar.</span><span class="sxs-lookup"><span data-stu-id="8befd-126">Represents the [MailTipsAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="8befd-127">MailTipsAccessLevel (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-127">MailTipsAccessLevel (SOAP)</span></span>](mailtipsaccesslevel-soap.md) <br/> |<span data-ttu-id="8befd-128">Stellt die [MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx) -Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="8befd-128">Represents the [MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="8befd-129">MailboxMoveEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-129">MailboxMoveEnabled (SOAP)</span></span>](mailboxmoveenabled-soap.md) <br/> |<span data-ttu-id="8befd-130">Stellt das [MailboxMoveEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx) -Flag dar.</span><span class="sxs-lookup"><span data-stu-id="8befd-130">Represents the [MailboxMoveEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="8befd-131">Name (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-131">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="8befd-132">Stellt den Namen der Organisationsbeziehung dar.</span><span class="sxs-lookup"><span data-stu-id="8befd-132">Represents the name of the organization relationship.</span></span>  <br/> |
|[<span data-ttu-id="8befd-133">TargetApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-133">TargetApplicationUri (SOAP)</span></span>](targetapplicationuri-soap.md) <br/> |<span data-ttu-id="8befd-134">Definiert den URI der Zielanwendung.</span><span class="sxs-lookup"><span data-stu-id="8befd-134">Defines the target application URI.</span></span>  <br/> |
|[<span data-ttu-id="8befd-135">TargetAutodiscoverEpr (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-135">TargetAutodiscoverEpr (SOAP)</span></span>](targetautodiscoverepr-soap.md) <br/> |<span data-ttu-id="8befd-136">Stellt die [TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx) -Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="8befd-136">Represents the [TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="8befd-137">TargetSharingEpr (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-137">TargetSharingEpr (SOAP)</span></span>](targetsharingepr-soap.md) <br/> |<span data-ttu-id="8befd-138">Stellt die [TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx) -Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="8befd-138">Represents the [TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx) property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8befd-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8befd-139">Parent elements</span></span>

|<span data-ttu-id="8befd-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="8befd-140">**Element**</span></span>|<span data-ttu-id="8befd-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8befd-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8befd-142">OrganizationRelationshipSettingsCollection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8befd-142">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="8befd-143">Stellt eine Liste von Organisationsbeziehungen dar, die mit der Abfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8befd-143">Represents a list of organization relationships that match the query.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8befd-144">Textwert</span><span class="sxs-lookup"><span data-stu-id="8befd-144">Text value</span></span>

<span data-ttu-id="8befd-145">Keine.</span><span class="sxs-lookup"><span data-stu-id="8befd-145">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8befd-146">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8befd-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8befd-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="8befd-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="8befd-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8befd-148">Schema Name</span></span>  <br/> |<span data-ttu-id="8befd-149">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="8befd-149">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="8befd-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8befd-150">Validation File</span></span>  <br/> |<span data-ttu-id="8befd-151">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8befd-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8befd-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8befd-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="8befd-153">True</span><span class="sxs-lookup"><span data-stu-id="8befd-153">True</span></span>  <br/> |
   

