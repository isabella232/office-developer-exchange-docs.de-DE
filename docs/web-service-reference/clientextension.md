---
title: ClientExtension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: Das ClientExtension-Element enthält die Benutzer- und Konfigurationsdaten Informationen zu einer app.
ms.openlocfilehash: 5051248a2c8e664d82666bd7b42ee3c3046f43fe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757568"
---
# <a name="clientextension"></a><span data-ttu-id="042f0-103">ClientExtension</span><span class="sxs-lookup"><span data-stu-id="042f0-103">ClientExtension</span></span>

<span data-ttu-id="042f0-104">Das **ClientExtension** -Element enthält die Benutzer- und Konfigurationsdaten Informationen zu einer app.</span><span class="sxs-lookup"><span data-stu-id="042f0-104">The **ClientExtension** element contains user and configuration information about an app.</span></span> 
  
```XML
<ClientExtension IsAvailable=" true | false " IsMandatory=" true | false " IsEnabledByDefault=" true | false " Type="" Scope="" MarketplaceAssetId="" MarketplaceContentMarket="" AppStatus="" Etoken="">
    <SpecificUsers></SpecificUsers>
    <Manifest></Manifest>
</ClientExtension>
```

 <span data-ttu-id="042f0-105">**ClientExtensionType**</span><span class="sxs-lookup"><span data-stu-id="042f0-105">**ClientExtensionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="042f0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="042f0-106">Attributes and elements</span></span>

<span data-ttu-id="042f0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="042f0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="042f0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="042f0-108">Attributes</span></span>

|<span data-ttu-id="042f0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="042f0-109">**Attribute**</span></span>|<span data-ttu-id="042f0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="042f0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="042f0-111">IsAvailable</span><span class="sxs-lookup"><span data-stu-id="042f0-111">IsAvailable</span></span>  <br/> |<span data-ttu-id="042f0-112">Gibt an, ob die app verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-112">Specifies whether the app is available.</span></span> <span data-ttu-id="042f0-113">Der Textwert **true** für das **IsAvailable** -Attribut gibt an, dass die app zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="042f0-113">A text value of **true** for the **IsAvailable** attribute indicates that the app is available.</span></span> <span data-ttu-id="042f0-114">Der Wert **false** gibt an, dass die app nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-114">A value of **false** indicates that the app is not available.</span></span> <span data-ttu-id="042f0-115">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="042f0-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="042f0-116">IsMandatory</span><span class="sxs-lookup"><span data-stu-id="042f0-116">IsMandatory</span></span>  <br/> |<span data-ttu-id="042f0-117">Gibt an, ob die app zwingend erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-117">Specifies whether the app is mandatory.</span></span> <span data-ttu-id="042f0-118">Der Textwert **true** für das **IsMandatory** -Attribut gibt an, dass die app für das Postfach zwingend erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-118">A text value of **true** for the **IsMandatory** attribute indicates that the app is mandatory for the mailbox.</span></span> <span data-ttu-id="042f0-119">Der Wert **false** gibt an, dass die app nicht zwingend erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-119">A value of **false** indicates that the app is not mandatory.</span></span> <span data-ttu-id="042f0-120">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="042f0-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="042f0-121">IsEnabledByDefault</span><span class="sxs-lookup"><span data-stu-id="042f0-121">IsEnabledByDefault</span></span>  <br/> |<span data-ttu-id="042f0-122">Gibt an, ob die app standardmäßig aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-122">Specifies whether the app is enabled by default.</span></span> <span data-ttu-id="042f0-123">Der Textwert **true** für das **IsEnabledByDefault** -Attribut gibt an, dass die app standardmäßig aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-123">A text value of **true** for the **IsEnabledByDefault** attribute indicates that the app is enabled by default.</span></span> <span data-ttu-id="042f0-124">Der Wert **false** gibt an, dass die app standardmäßig nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-124">A value of **false** indicates that the app is not enabled by default.</span></span> <span data-ttu-id="042f0-125">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="042f0-125">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="042f0-126">ProvidedTo</span><span class="sxs-lookup"><span data-stu-id="042f0-126">ProvidedTo</span></span>  <br/> |<span data-ttu-id="042f0-127">Gibt an, auf denen die app bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="042f0-127">Specifies to whom the app is provided.</span></span> <span data-ttu-id="042f0-128">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="042f0-128">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="042f0-129">Typ</span><span class="sxs-lookup"><span data-stu-id="042f0-129">Type</span></span>  <br/> |<span data-ttu-id="042f0-130">Gibt den Typ der app.</span><span class="sxs-lookup"><span data-stu-id="042f0-130">Specifies the type of the app.</span></span>  <br/> |
|<span data-ttu-id="042f0-131">Umfang</span><span class="sxs-lookup"><span data-stu-id="042f0-131">Scope</span></span>  <br/> |<span data-ttu-id="042f0-132">Gibt den Umfang der app.</span><span class="sxs-lookup"><span data-stu-id="042f0-132">Specifies the scope of the app.</span></span>  <br/> |
|<span data-ttu-id="042f0-133">MarketplaceAssetId</span><span class="sxs-lookup"><span data-stu-id="042f0-133">MarketplaceAssetId</span></span>  <br/> |<span data-ttu-id="042f0-134">Gibt die Marketplace-Anlage-ID der app.</span><span class="sxs-lookup"><span data-stu-id="042f0-134">Specifies the marketplace asset identifier of the app.</span></span>  <br/> |
|<span data-ttu-id="042f0-135">MarketplaceContentMarket</span><span class="sxs-lookup"><span data-stu-id="042f0-135">MarketplaceContentMarket</span></span>  <br/> |<span data-ttu-id="042f0-136">Gibt den Marketplace-Inhalt, den ein Benutzer sieht ausführliche und über eine app überprüft.</span><span class="sxs-lookup"><span data-stu-id="042f0-136">Specifies the marketplace content that a user sees for details and reviews about an app.</span></span>  <br/> |
|<span data-ttu-id="042f0-137">AppStatus</span><span class="sxs-lookup"><span data-stu-id="042f0-137">AppStatus</span></span>  <br/> |<span data-ttu-id="042f0-138">Gibt den Statuscode einer Mail-App in einem unerwarteten Zustand.</span><span class="sxs-lookup"><span data-stu-id="042f0-138">Specifies the status code of a mail app in an unexpected state.</span></span>  <br/> |
|<span data-ttu-id="042f0-139">Etoken</span><span class="sxs-lookup"><span data-stu-id="042f0-139">Etoken</span></span>  <br/> |<span data-ttu-id="042f0-140">Gibt das Lizenztoken für kostenpflichtige oder Testversion Mail-apps.</span><span class="sxs-lookup"><span data-stu-id="042f0-140">Specifies the license token for paid or trial mail apps.</span></span>  <br/> |
   
#### <a name="type"></a><span data-ttu-id="042f0-141">Typ</span><span class="sxs-lookup"><span data-stu-id="042f0-141">Type</span></span>

|<span data-ttu-id="042f0-142">**Wert**</span><span class="sxs-lookup"><span data-stu-id="042f0-142">**Value**</span></span>|<span data-ttu-id="042f0-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="042f0-143">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="042f0-144">Standard</span><span class="sxs-lookup"><span data-stu-id="042f0-144">Default</span></span>  <br/> |<span data-ttu-id="042f0-145">Gibt an, dass die app standardmäßig verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-145">Indicates that the app is available by default.</span></span>  <br/> |
|<span data-ttu-id="042f0-146">Privat</span><span class="sxs-lookup"><span data-stu-id="042f0-146">Private</span></span>  <br/> |<span data-ttu-id="042f0-147">Gibt an, dass die app privat ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-147">Indicates that the app is private.</span></span>  <br/> |
|<span data-ttu-id="042f0-148">MarketPlace</span><span class="sxs-lookup"><span data-stu-id="042f0-148">MarketPlace</span></span>  <br/> |<span data-ttu-id="042f0-149">Gibt an, dass die app eine app Marketplace ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-149">Indicates that the app is a marketplace app.</span></span>  <br/> |
   
#### <a name="scope"></a><span data-ttu-id="042f0-150">Umfang</span><span class="sxs-lookup"><span data-stu-id="042f0-150">Scope</span></span>

|<span data-ttu-id="042f0-151">**Wert**</span><span class="sxs-lookup"><span data-stu-id="042f0-151">**Value**</span></span>|<span data-ttu-id="042f0-152">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="042f0-152">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="042f0-153">Keine</span><span class="sxs-lookup"><span data-stu-id="042f0-153">None</span></span>  <br/> |<span data-ttu-id="042f0-154">Gibt an, dass die app keine Bereich verfügt.</span><span class="sxs-lookup"><span data-stu-id="042f0-154">Indicates that the app has no scope.</span></span>  <br/> |
|<span data-ttu-id="042f0-155">Benutzer</span><span class="sxs-lookup"><span data-stu-id="042f0-155">User</span></span>  <br/> |<span data-ttu-id="042f0-156">Gibt an, dass die app pro Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-156">Indicates that the app is per user.</span></span>  <br/> |
|<span data-ttu-id="042f0-157">Organisation</span><span class="sxs-lookup"><span data-stu-id="042f0-157">Organization</span></span>  <br/> |<span data-ttu-id="042f0-158">Gibt an, dass die app für eine Organisation ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-158">Indicates that the app is for an organization.</span></span>  <br/> |
|<span data-ttu-id="042f0-159">Standard</span><span class="sxs-lookup"><span data-stu-id="042f0-159">Default</span></span>  <br/> |<span data-ttu-id="042f0-160">Gibt an, dass die app eine app Standard ist.</span><span class="sxs-lookup"><span data-stu-id="042f0-160">Indicates that the app is a default app.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="042f0-161">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="042f0-161">Child elements</span></span>

|<span data-ttu-id="042f0-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="042f0-162">**Element**</span></span>|<span data-ttu-id="042f0-163">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="042f0-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="042f0-164">SpecificUsers</span><span class="sxs-lookup"><span data-stu-id="042f0-164">SpecificUsers</span></span>](specificusers.md) <br/> |<span data-ttu-id="042f0-165">Gibt die e-Mail-Konten, die die app zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="042f0-165">Specifies the email accounts that can access the app.</span></span>  <br/> |
|[<span data-ttu-id="042f0-166">Manifest</span><span class="sxs-lookup"><span data-stu-id="042f0-166">Manifest</span></span>](manifest.md) <br/> |<span data-ttu-id="042f0-167">Enthält die Base64-codierte app-Manifestdatei.</span><span class="sxs-lookup"><span data-stu-id="042f0-167">Contains the base-64 encoded app manifest file.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="042f0-168">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="042f0-168">Parent elements</span></span>

|<span data-ttu-id="042f0-169">**Element**</span><span class="sxs-lookup"><span data-stu-id="042f0-169">**Element**</span></span>|<span data-ttu-id="042f0-170">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="042f0-170">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="042f0-171">ClientExtensions</span><span class="sxs-lookup"><span data-stu-id="042f0-171">ClientExtensions</span></span>](clientextensions.md) <br/> |<span data-ttu-id="042f0-172">Gibt ein Array von **ClientExtension** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="042f0-172">Specifies an array of **ClientExtension** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="042f0-173">Hinweise</span><span class="sxs-lookup"><span data-stu-id="042f0-173">Remarks</span></span>

<span data-ttu-id="042f0-174">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="042f0-174">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="042f0-175">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="042f0-175">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="042f0-176">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="042f0-176">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="042f0-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="042f0-177">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="042f0-178">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="042f0-178">Schema Name</span></span>  <br/> |<span data-ttu-id="042f0-179">Typschema</span><span class="sxs-lookup"><span data-stu-id="042f0-179">Type schema</span></span>  <br/> |
|<span data-ttu-id="042f0-180">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="042f0-180">Validation File</span></span>  <br/> |<span data-ttu-id="042f0-181">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="042f0-181">types.xsd</span></span>  <br/> |
|<span data-ttu-id="042f0-182">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="042f0-182">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="042f0-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="042f0-183">See also</span></span>



- [<span data-ttu-id="042f0-184">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="042f0-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

