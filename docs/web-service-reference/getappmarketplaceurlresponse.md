---
title: GetAppMarketplaceUrlResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc3368ec-78c2-4f8d-8394-4891e90dafd2
description: Das GetAppMarketplaceUrlResponse-Element gibt die Antwort auf eine GetAppMarketplaceUrl an.
ms.openlocfilehash: 553ebfc4615280c77d4a1ef9e5db3e5d10a0f2a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758576"
---
# <a name="getappmarketplaceurlresponse"></a><span data-ttu-id="61af0-103">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="61af0-103">GetAppMarketplaceUrlResponse</span></span>

<span data-ttu-id="61af0-104">Das **GetAppMarketplaceUrlResponse** -Element gibt die Antwort auf eine **GetAppMarketplaceUrl** an.</span><span class="sxs-lookup"><span data-stu-id="61af0-104">The **GetAppMarketplaceUrlResponse** element specifies the response to a **GetAppMarketplaceUrl** request.</span></span> 
  
```XML
<GetAppMarketplaceUrlResponse ResponseClass=" Success | Warning | Error ">
    <AppMarketplaceUrl/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppMarketplaceUrlResponse>
```

 <span data-ttu-id="61af0-105">**GetAppMarketplaceUrlResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="61af0-105">**GetAppMarketplaceUrlResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61af0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="61af0-106">Attributes and elements</span></span>

<span data-ttu-id="61af0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="61af0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61af0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="61af0-108">Attributes</span></span>

|<span data-ttu-id="61af0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="61af0-109">**Attribute**</span></span>|<span data-ttu-id="61af0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61af0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61af0-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="61af0-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="61af0-112">Gibt die Klasse der Antwort.</span><span class="sxs-lookup"><span data-stu-id="61af0-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="61af0-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="61af0-113">ResponseClass</span></span>

|<span data-ttu-id="61af0-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="61af0-114">**Value**</span></span>|<span data-ttu-id="61af0-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61af0-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61af0-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="61af0-116">Success</span></span>  <br/> |<span data-ttu-id="61af0-117">Gibt Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="61af0-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="61af0-118">Warning</span><span class="sxs-lookup"><span data-stu-id="61af0-118">Warning</span></span>  <br/> |<span data-ttu-id="61af0-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="61af0-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="61af0-120">Fehler</span><span class="sxs-lookup"><span data-stu-id="61af0-120">Error</span></span>  <br/> |<span data-ttu-id="61af0-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="61af0-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="61af0-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61af0-122">Child elements</span></span>

|<span data-ttu-id="61af0-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="61af0-123">**Element**</span></span>|<span data-ttu-id="61af0-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61af0-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61af0-125">AppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="61af0-125">AppMarketplaceUrl</span></span>](appmarketplaceurl.md) <br/> |<span data-ttu-id="61af0-126">Gibt die URL für die app.</span><span class="sxs-lookup"><span data-stu-id="61af0-126">Specifies the URL for the app.</span></span>  <br/> |
|[<span data-ttu-id="61af0-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="61af0-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="61af0-128">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="61af0-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="61af0-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="61af0-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="61af0-130">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="61af0-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="61af0-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="61af0-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="61af0-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="61af0-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="61af0-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="61af0-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="61af0-134">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="61af0-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="61af0-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61af0-135">Parent elements</span></span>

|<span data-ttu-id="61af0-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="61af0-136">**Element**</span></span>|<span data-ttu-id="61af0-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61af0-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61af0-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="61af0-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="61af0-139">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="61af0-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61af0-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="61af0-140">Remarks</span></span>

<span data-ttu-id="61af0-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="61af0-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="61af0-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="61af0-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61af0-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="61af0-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61af0-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="61af0-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="61af0-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="61af0-145">Schema Name</span></span>  <br/> |<span data-ttu-id="61af0-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="61af0-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="61af0-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="61af0-147">Validation File</span></span>  <br/> |<span data-ttu-id="61af0-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="61af0-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="61af0-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="61af0-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="61af0-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61af0-150">See also</span></span>



- [<span data-ttu-id="61af0-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="61af0-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

