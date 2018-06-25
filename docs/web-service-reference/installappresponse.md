---
title: InstallAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5e0582d-c1e1-453b-93ed-c31165c82697
description: Das InstallAppResponse-Element gibt die Antwort auf eine Anforderung InstallApp.
ms.openlocfilehash: 8e8da720b3a38e979b3d83810bb798350822146c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829942"
---
# <a name="installappresponse"></a><span data-ttu-id="ffb52-103">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="ffb52-103">InstallAppResponse</span></span>

<span data-ttu-id="ffb52-104">Das **InstallAppResponse** -Element gibt die Antwort auf eine Anforderung **InstallApp** .</span><span class="sxs-lookup"><span data-stu-id="ffb52-104">The **InstallAppResponse** element specifies the response to an **InstallApp** request.</span></span> 
  
```xml
<InstallAppResponse ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</InstallAppResponse>
```

 <span data-ttu-id="ffb52-105">**InstallAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="ffb52-105">**InstallAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ffb52-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ffb52-106">Attributes and elements</span></span>

<span data-ttu-id="ffb52-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ffb52-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ffb52-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ffb52-108">Attributes</span></span>

|<span data-ttu-id="ffb52-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ffb52-109">**Attribute**</span></span>|<span data-ttu-id="ffb52-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffb52-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffb52-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ffb52-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="ffb52-112">Gibt die Klasse der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ffb52-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="ffb52-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ffb52-113">ResponseClass</span></span>

|<span data-ttu-id="ffb52-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ffb52-114">**Value**</span></span>|<span data-ttu-id="ffb52-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffb52-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffb52-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="ffb52-116">Success</span></span>  <br/> |<span data-ttu-id="ffb52-117">Gibt Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="ffb52-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="ffb52-118">Warning</span><span class="sxs-lookup"><span data-stu-id="ffb52-118">Warning</span></span>  <br/> |<span data-ttu-id="ffb52-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="ffb52-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="ffb52-120">Fehler</span><span class="sxs-lookup"><span data-stu-id="ffb52-120">Error</span></span>  <br/> |<span data-ttu-id="ffb52-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="ffb52-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ffb52-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ffb52-122">Child elements</span></span>

|<span data-ttu-id="ffb52-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="ffb52-123">**Element**</span></span>|<span data-ttu-id="ffb52-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffb52-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffb52-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ffb52-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ffb52-126">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ffb52-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="ffb52-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="ffb52-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ffb52-128">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ffb52-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ffb52-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ffb52-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ffb52-130">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="ffb52-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ffb52-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ffb52-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ffb52-132">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ffb52-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ffb52-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ffb52-133">Parent elements</span></span>

|<span data-ttu-id="ffb52-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="ffb52-134">**Element**</span></span>|<span data-ttu-id="ffb52-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffb52-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffb52-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ffb52-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ffb52-137">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ffb52-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ffb52-138">Textwert</span><span class="sxs-lookup"><span data-stu-id="ffb52-138">Text value</span></span>

<span data-ttu-id="ffb52-139">Keine.</span><span class="sxs-lookup"><span data-stu-id="ffb52-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffb52-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffb52-140">Remarks</span></span>

<span data-ttu-id="ffb52-141">Das **GetAppManifestsResponseMessage** -Element ist für Clients, die Exchange Online und Versionen von Microsoft Exchange Server beginnend mit Exchange 2013 abzielen.</span><span class="sxs-lookup"><span data-stu-id="ffb52-141">The **GetAppManifestsResponseMessage** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ffb52-142">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ffb52-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffb52-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffb52-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ffb52-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ffb52-144">Schema Name</span></span>  <br/> |<span data-ttu-id="ffb52-145">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ffb52-145">Message schema</span></span>  <br/> |
|<span data-ttu-id="ffb52-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ffb52-146">Validation File</span></span>  <br/> |<span data-ttu-id="ffb52-147">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ffb52-147">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ffb52-148">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ffb52-148">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ffb52-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffb52-149">See also</span></span>



- [<span data-ttu-id="ffb52-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ffb52-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

