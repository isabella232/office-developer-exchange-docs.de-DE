---
title: GetAppMarketplaceUrlResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc3368ec-78c2-4f8d-8394-4891e90dafd2
description: Das GetAppMarketplaceUrlResponse-Element gibt die Antwort auf eine GetAppMarketplaceUrl-Anforderung an.
ms.openlocfilehash: 7ff000908a2f73f41575cae8a7795644dd60565d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530853"
---
# <a name="getappmarketplaceurlresponse"></a><span data-ttu-id="ff158-103">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="ff158-103">GetAppMarketplaceUrlResponse</span></span>

<span data-ttu-id="ff158-104">Das **GetAppMarketplaceUrlResponse** -Element gibt die Antwort auf eine **GetAppMarketplaceUrl** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="ff158-104">The **GetAppMarketplaceUrlResponse** element specifies the response to a **GetAppMarketplaceUrl** request.</span></span> 
  
```XML
<GetAppMarketplaceUrlResponse ResponseClass=" Success | Warning | Error ">
    <AppMarketplaceUrl/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppMarketplaceUrlResponse>
```

 <span data-ttu-id="ff158-105">**GetAppMarketplaceUrlResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ff158-105">**GetAppMarketplaceUrlResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff158-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ff158-106">Attributes and elements</span></span>

<span data-ttu-id="ff158-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ff158-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff158-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ff158-108">Attributes</span></span>

|<span data-ttu-id="ff158-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ff158-109">**Attribute**</span></span>|<span data-ttu-id="ff158-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff158-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ff158-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ff158-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="ff158-112">Gibt die Klasse der Antwort an.</span><span class="sxs-lookup"><span data-stu-id="ff158-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="ff158-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ff158-113">ResponseClass</span></span>

|<span data-ttu-id="ff158-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ff158-114">**Value**</span></span>|<span data-ttu-id="ff158-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff158-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ff158-116">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="ff158-116">Success</span></span>  <br/> |<span data-ttu-id="ff158-117">Gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="ff158-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="ff158-118">Warnung</span><span class="sxs-lookup"><span data-stu-id="ff158-118">Warning</span></span>  <br/> |<span data-ttu-id="ff158-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="ff158-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="ff158-120">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="ff158-120">Error</span></span>  <br/> |<span data-ttu-id="ff158-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="ff158-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ff158-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff158-122">Child elements</span></span>

|<span data-ttu-id="ff158-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff158-123">**Element**</span></span>|<span data-ttu-id="ff158-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff158-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff158-125">AppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="ff158-125">AppMarketplaceUrl</span></span>](appmarketplaceurl.md) <br/> |<span data-ttu-id="ff158-126">Gibt die URL für die APP an.</span><span class="sxs-lookup"><span data-stu-id="ff158-126">Specifies the URL for the app.</span></span>  <br/> |
|[<span data-ttu-id="ff158-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ff158-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ff158-128">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ff158-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="ff158-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="ff158-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ff158-130">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ff158-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ff158-131">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="ff158-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ff158-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="ff158-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ff158-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ff158-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ff158-134">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="ff158-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ff158-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff158-135">Parent elements</span></span>

|<span data-ttu-id="ff158-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff158-136">**Element**</span></span>|<span data-ttu-id="ff158-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff158-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff158-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ff158-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ff158-139">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ff158-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff158-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff158-140">Remarks</span></span>

<span data-ttu-id="ff158-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ff158-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ff158-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ff158-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff158-143">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ff158-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff158-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff158-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ff158-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ff158-145">Schema Name</span></span>  <br/> |<span data-ttu-id="ff158-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ff158-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="ff158-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ff158-147">Validation File</span></span>  <br/> |<span data-ttu-id="ff158-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ff158-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ff158-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ff158-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ff158-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff158-150">See also</span></span>



- [<span data-ttu-id="ff158-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ff158-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

