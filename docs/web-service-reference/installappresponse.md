---
title: InstallAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5e0582d-c1e1-453b-93ed-c31165c82697
description: Das InstallAppResponse-Element gibt die Antwort auf eine InstallApp-Anforderung an.
ms.openlocfilehash: 0f7690e2df7e71c4e478dec191671af24f96294b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465667"
---
# <a name="installappresponse"></a><span data-ttu-id="f5b12-103">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="f5b12-103">InstallAppResponse</span></span>

<span data-ttu-id="f5b12-104">Das **InstallAppResponse** -Element gibt die Antwort auf eine **InstallApp** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="f5b12-104">The **InstallAppResponse** element specifies the response to an **InstallApp** request.</span></span> 
  
```xml
<InstallAppResponse ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</InstallAppResponse>
```

 <span data-ttu-id="f5b12-105">**InstallAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="f5b12-105">**InstallAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f5b12-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f5b12-106">Attributes and elements</span></span>

<span data-ttu-id="f5b12-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f5b12-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5b12-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f5b12-108">Attributes</span></span>

|<span data-ttu-id="f5b12-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f5b12-109">**Attribute**</span></span>|<span data-ttu-id="f5b12-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f5b12-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5b12-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="f5b12-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="f5b12-112">Gibt die Klasse der Antwort an.</span><span class="sxs-lookup"><span data-stu-id="f5b12-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="f5b12-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="f5b12-113">ResponseClass</span></span>

|<span data-ttu-id="f5b12-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f5b12-114">**Value**</span></span>|<span data-ttu-id="f5b12-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f5b12-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5b12-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="f5b12-116">Success</span></span>  <br/> |<span data-ttu-id="f5b12-117">Gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="f5b12-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="f5b12-118">Warnung</span><span class="sxs-lookup"><span data-stu-id="f5b12-118">Warning</span></span>  <br/> |<span data-ttu-id="f5b12-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="f5b12-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="f5b12-120">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="f5b12-120">Error</span></span>  <br/> |<span data-ttu-id="f5b12-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="f5b12-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f5b12-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f5b12-122">Child elements</span></span>

|<span data-ttu-id="f5b12-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="f5b12-123">**Element**</span></span>|<span data-ttu-id="f5b12-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f5b12-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5b12-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f5b12-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f5b12-126">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f5b12-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="f5b12-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="f5b12-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f5b12-128">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="f5b12-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f5b12-129">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="f5b12-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f5b12-130">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="f5b12-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="f5b12-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f5b12-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f5b12-132">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="f5b12-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f5b12-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f5b12-133">Parent elements</span></span>

|<span data-ttu-id="f5b12-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="f5b12-134">**Element**</span></span>|<span data-ttu-id="f5b12-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f5b12-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5b12-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f5b12-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="f5b12-137">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f5b12-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f5b12-138">Textwert</span><span class="sxs-lookup"><span data-stu-id="f5b12-138">Text value</span></span>

<span data-ttu-id="f5b12-139">Keine.</span><span class="sxs-lookup"><span data-stu-id="f5b12-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f5b12-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5b12-140">Remarks</span></span>

<span data-ttu-id="f5b12-141">Das **GetAppManifestsResponseMessage** -Element gilt für Clients, die auf Exchange Online und Versionen von Exchange Server, beginnend mit Exchange 2013, abzielen.</span><span class="sxs-lookup"><span data-stu-id="f5b12-141">The **GetAppManifestsResponseMessage** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f5b12-142">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f5b12-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5b12-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5b12-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f5b12-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f5b12-144">Schema Name</span></span>  <br/> |<span data-ttu-id="f5b12-145">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f5b12-145">Message schema</span></span>  <br/> |
|<span data-ttu-id="f5b12-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f5b12-146">Validation File</span></span>  <br/> |<span data-ttu-id="f5b12-147">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f5b12-147">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f5b12-148">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f5b12-148">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f5b12-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5b12-149">See also</span></span>



- [<span data-ttu-id="f5b12-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f5b12-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

