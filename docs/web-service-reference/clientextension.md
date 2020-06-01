---
title: Client Extension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: Das Client Extension-Element enthält Benutzer-und Konfigurationsinformationen zu einer App.
ms.openlocfilehash: d3d9ce1d242a63f28da3464f0faff86abde502c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460197"
---
# <a name="clientextension"></a><span data-ttu-id="9311f-103">Client Extension</span><span class="sxs-lookup"><span data-stu-id="9311f-103">ClientExtension</span></span>

<span data-ttu-id="9311f-104">Das **Client Extension** -Element enthält Benutzer-und Konfigurationsinformationen zu einer App.</span><span class="sxs-lookup"><span data-stu-id="9311f-104">The **ClientExtension** element contains user and configuration information about an app.</span></span> 
  
```XML
<ClientExtension IsAvailable=" true | false " IsMandatory=" true | false " IsEnabledByDefault=" true | false " Type="" Scope="" MarketplaceAssetId="" MarketplaceContentMarket="" AppStatus="" Etoken="">
    <SpecificUsers></SpecificUsers>
    <Manifest></Manifest>
</ClientExtension>
```

 <span data-ttu-id="9311f-105">**ClientExtensionType**</span><span class="sxs-lookup"><span data-stu-id="9311f-105">**ClientExtensionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9311f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9311f-106">Attributes and elements</span></span>

<span data-ttu-id="9311f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9311f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9311f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9311f-108">Attributes</span></span>

|<span data-ttu-id="9311f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9311f-109">**Attribute**</span></span>|<span data-ttu-id="9311f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9311f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9311f-111">IsAvailable</span><span class="sxs-lookup"><span data-stu-id="9311f-111">IsAvailable</span></span>  <br/> |<span data-ttu-id="9311f-112">Gibt an, ob die app verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-112">Specifies whether the app is available.</span></span> <span data-ttu-id="9311f-113">Der Textwert **true** für das **IsAvailable** -Attribut gibt an, dass die app verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-113">A text value of **true** for the **IsAvailable** attribute indicates that the app is available.</span></span> <span data-ttu-id="9311f-114">Der Wert **false** gibt an, dass die APP nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-114">A value of **false** indicates that the app is not available.</span></span> <span data-ttu-id="9311f-115">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="9311f-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="9311f-116">Ismandatory</span><span class="sxs-lookup"><span data-stu-id="9311f-116">IsMandatory</span></span>  <br/> |<span data-ttu-id="9311f-117">Gibt an, ob die APP obligatorisch ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-117">Specifies whether the app is mandatory.</span></span> <span data-ttu-id="9311f-118">Der Textwert **true** für das Attribut **ismandatory** gibt an, dass die APP für das Postfach obligatorisch ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-118">A text value of **true** for the **IsMandatory** attribute indicates that the app is mandatory for the mailbox.</span></span> <span data-ttu-id="9311f-119">Der Wert **false** gibt an, dass die APP nicht zwingend ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-119">A value of **false** indicates that the app is not mandatory.</span></span> <span data-ttu-id="9311f-120">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="9311f-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="9311f-121">IsEnabledByDefault</span><span class="sxs-lookup"><span data-stu-id="9311f-121">IsEnabledByDefault</span></span>  <br/> |<span data-ttu-id="9311f-122">Gibt an, ob die App standardmäßig aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-122">Specifies whether the app is enabled by default.</span></span> <span data-ttu-id="9311f-123">Der Textwert **true** für das **IsEnabledByDefault** -Attribut gibt an, dass die App standardmäßig aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-123">A text value of **true** for the **IsEnabledByDefault** attribute indicates that the app is enabled by default.</span></span> <span data-ttu-id="9311f-124">Der Wert **false** gibt an, dass die App standardmäßig nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-124">A value of **false** indicates that the app is not enabled by default.</span></span> <span data-ttu-id="9311f-125">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="9311f-125">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="9311f-126">ProvidedTo</span><span class="sxs-lookup"><span data-stu-id="9311f-126">ProvidedTo</span></span>  <br/> |<span data-ttu-id="9311f-127">Gibt an, wem die APP bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9311f-127">Specifies to whom the app is provided.</span></span> <span data-ttu-id="9311f-128">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="9311f-128">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="9311f-129">Typ</span><span class="sxs-lookup"><span data-stu-id="9311f-129">Type</span></span>  <br/> |<span data-ttu-id="9311f-130">Gibt den Typ der APP an.</span><span class="sxs-lookup"><span data-stu-id="9311f-130">Specifies the type of the app.</span></span>  <br/> |
|<span data-ttu-id="9311f-131">Bereich</span><span class="sxs-lookup"><span data-stu-id="9311f-131">Scope</span></span>  <br/> |<span data-ttu-id="9311f-132">Gibt den Bereich der APP an.</span><span class="sxs-lookup"><span data-stu-id="9311f-132">Specifies the scope of the app.</span></span>  <br/> |
|<span data-ttu-id="9311f-133">MarketplaceAssetId</span><span class="sxs-lookup"><span data-stu-id="9311f-133">MarketplaceAssetId</span></span>  <br/> |<span data-ttu-id="9311f-134">Gibt die Marketplace-Objekt-ID der APP an.</span><span class="sxs-lookup"><span data-stu-id="9311f-134">Specifies the marketplace asset identifier of the app.</span></span>  <br/> |
|<span data-ttu-id="9311f-135">MarketplaceContentMarket</span><span class="sxs-lookup"><span data-stu-id="9311f-135">MarketplaceContentMarket</span></span>  <br/> |<span data-ttu-id="9311f-136">Gibt die Marketplace-Inhalte an, die ein Benutzer für Details und Besprechungen zu einer APP sieht.</span><span class="sxs-lookup"><span data-stu-id="9311f-136">Specifies the marketplace content that a user sees for details and reviews about an app.</span></span>  <br/> |
|<span data-ttu-id="9311f-137">AppStatus</span><span class="sxs-lookup"><span data-stu-id="9311f-137">AppStatus</span></span>  <br/> |<span data-ttu-id="9311f-138">Gibt den Statuscode einer Mail-app in einem unerwarteten Zustand an.</span><span class="sxs-lookup"><span data-stu-id="9311f-138">Specifies the status code of a mail app in an unexpected state.</span></span>  <br/> |
|<span data-ttu-id="9311f-139">EToken</span><span class="sxs-lookup"><span data-stu-id="9311f-139">Etoken</span></span>  <br/> |<span data-ttu-id="9311f-140">Gibt das Lizenztoken für kostenpflichtige oder Test-e-Mail-apps an.</span><span class="sxs-lookup"><span data-stu-id="9311f-140">Specifies the license token for paid or trial mail apps.</span></span>  <br/> |
   
#### <a name="type"></a><span data-ttu-id="9311f-141">Typ</span><span class="sxs-lookup"><span data-stu-id="9311f-141">Type</span></span>

|<span data-ttu-id="9311f-142">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9311f-142">**Value**</span></span>|<span data-ttu-id="9311f-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9311f-143">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9311f-144">Standard</span><span class="sxs-lookup"><span data-stu-id="9311f-144">Default</span></span>  <br/> |<span data-ttu-id="9311f-145">Gibt an, dass die App standardmäßig verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-145">Indicates that the app is available by default.</span></span>  <br/> |
|<span data-ttu-id="9311f-146">Private</span><span class="sxs-lookup"><span data-stu-id="9311f-146">Private</span></span>  <br/> |<span data-ttu-id="9311f-147">Gibt an, dass die APP privat ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-147">Indicates that the app is private.</span></span>  <br/> |
|<span data-ttu-id="9311f-148">Markt</span><span class="sxs-lookup"><span data-stu-id="9311f-148">MarketPlace</span></span>  <br/> |<span data-ttu-id="9311f-149">Gibt an, dass die APP eine Marketplace-APP ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-149">Indicates that the app is a marketplace app.</span></span>  <br/> |
   
#### <a name="scope"></a><span data-ttu-id="9311f-150">Bereich</span><span class="sxs-lookup"><span data-stu-id="9311f-150">Scope</span></span>

|<span data-ttu-id="9311f-151">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9311f-151">**Value**</span></span>|<span data-ttu-id="9311f-152">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9311f-152">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9311f-153">Keine</span><span class="sxs-lookup"><span data-stu-id="9311f-153">None</span></span>  <br/> |<span data-ttu-id="9311f-154">Gibt an, dass die APP keinen Bereich aufweist.</span><span class="sxs-lookup"><span data-stu-id="9311f-154">Indicates that the app has no scope.</span></span>  <br/> |
|<span data-ttu-id="9311f-155">User</span><span class="sxs-lookup"><span data-stu-id="9311f-155">User</span></span>  <br/> |<span data-ttu-id="9311f-156">Gibt an, dass die APP pro Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-156">Indicates that the app is per user.</span></span>  <br/> |
|<span data-ttu-id="9311f-157">Organisation</span><span class="sxs-lookup"><span data-stu-id="9311f-157">Organization</span></span>  <br/> |<span data-ttu-id="9311f-158">Gibt an, dass die APP für eine Organisation ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-158">Indicates that the app is for an organization.</span></span>  <br/> |
|<span data-ttu-id="9311f-159">Standard</span><span class="sxs-lookup"><span data-stu-id="9311f-159">Default</span></span>  <br/> |<span data-ttu-id="9311f-160">Gibt an, dass die APP eine Standard-APP ist.</span><span class="sxs-lookup"><span data-stu-id="9311f-160">Indicates that the app is a default app.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9311f-161">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9311f-161">Child elements</span></span>

|<span data-ttu-id="9311f-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="9311f-162">**Element**</span></span>|<span data-ttu-id="9311f-163">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9311f-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9311f-164">SpecificUsers</span><span class="sxs-lookup"><span data-stu-id="9311f-164">SpecificUsers</span></span>](specificusers.md) <br/> |<span data-ttu-id="9311f-165">Gibt die e-Mail-Konten an, die auf die App zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="9311f-165">Specifies the email accounts that can access the app.</span></span>  <br/> |
|[<span data-ttu-id="9311f-166">Manifest</span><span class="sxs-lookup"><span data-stu-id="9311f-166">Manifest</span></span>](manifest.md) <br/> |<span data-ttu-id="9311f-167">Enthält die codierte App-Manifestdatei von Base-64.</span><span class="sxs-lookup"><span data-stu-id="9311f-167">Contains the base-64 encoded app manifest file.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9311f-168">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9311f-168">Parent elements</span></span>

|<span data-ttu-id="9311f-169">**Element**</span><span class="sxs-lookup"><span data-stu-id="9311f-169">**Element**</span></span>|<span data-ttu-id="9311f-170">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9311f-170">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9311f-171">ClientExtensions</span><span class="sxs-lookup"><span data-stu-id="9311f-171">ClientExtensions</span></span>](clientextensions.md) <br/> |<span data-ttu-id="9311f-172">Gibt ein Array von **Client Extension** -Elementen an.</span><span class="sxs-lookup"><span data-stu-id="9311f-172">Specifies an array of **ClientExtension** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9311f-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9311f-173">Remarks</span></span>

<span data-ttu-id="9311f-174">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9311f-174">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9311f-175">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9311f-175">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9311f-176">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9311f-176">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9311f-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="9311f-177">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9311f-178">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9311f-178">Schema Name</span></span>  <br/> |<span data-ttu-id="9311f-179">Typschema</span><span class="sxs-lookup"><span data-stu-id="9311f-179">Type schema</span></span>  <br/> |
|<span data-ttu-id="9311f-180">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9311f-180">Validation File</span></span>  <br/> |<span data-ttu-id="9311f-181">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9311f-181">types.xsd</span></span>  <br/> |
|<span data-ttu-id="9311f-182">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9311f-182">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="9311f-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9311f-183">See also</span></span>



- [<span data-ttu-id="9311f-184">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9311f-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

