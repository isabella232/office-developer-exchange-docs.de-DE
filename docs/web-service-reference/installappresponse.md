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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465667"
---
# <a name="installappresponse"></a><span data-ttu-id="cbeab-103">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="cbeab-103">InstallAppResponse</span></span>

<span data-ttu-id="cbeab-104">Das **InstallAppResponse** -Element gibt die Antwort auf eine **InstallApp** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="cbeab-104">The **InstallAppResponse** element specifies the response to an **InstallApp** request.</span></span> 
  
```xml
<InstallAppResponse ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</InstallAppResponse>
```

 <span data-ttu-id="cbeab-105">**InstallAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="cbeab-105">**InstallAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cbeab-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cbeab-106">Attributes and elements</span></span>

<span data-ttu-id="cbeab-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cbeab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbeab-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cbeab-108">Attributes</span></span>

|<span data-ttu-id="cbeab-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cbeab-109">**Attribute**</span></span>|<span data-ttu-id="cbeab-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cbeab-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cbeab-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="cbeab-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="cbeab-112">Gibt die Klasse der Antwort an.</span><span class="sxs-lookup"><span data-stu-id="cbeab-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="cbeab-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="cbeab-113">ResponseClass</span></span>

|<span data-ttu-id="cbeab-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cbeab-114">**Value**</span></span>|<span data-ttu-id="cbeab-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cbeab-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cbeab-116">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="cbeab-116">Success</span></span>  <br/> |<span data-ttu-id="cbeab-117">Gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="cbeab-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="cbeab-118">Warnung</span><span class="sxs-lookup"><span data-stu-id="cbeab-118">Warning</span></span>  <br/> |<span data-ttu-id="cbeab-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="cbeab-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="cbeab-120">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="cbeab-120">Error</span></span>  <br/> |<span data-ttu-id="cbeab-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="cbeab-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cbeab-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cbeab-122">Child elements</span></span>

|<span data-ttu-id="cbeab-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="cbeab-123">**Element**</span></span>|<span data-ttu-id="cbeab-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cbeab-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbeab-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cbeab-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cbeab-126">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="cbeab-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="cbeab-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="cbeab-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cbeab-128">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="cbeab-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cbeab-129">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="cbeab-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cbeab-130">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="cbeab-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="cbeab-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cbeab-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cbeab-132">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="cbeab-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cbeab-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cbeab-133">Parent elements</span></span>

|<span data-ttu-id="cbeab-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="cbeab-134">**Element**</span></span>|<span data-ttu-id="cbeab-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cbeab-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbeab-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cbeab-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="cbeab-137">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cbeab-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cbeab-138">Textwert</span><span class="sxs-lookup"><span data-stu-id="cbeab-138">Text value</span></span>

<span data-ttu-id="cbeab-139">Keine.</span><span class="sxs-lookup"><span data-stu-id="cbeab-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cbeab-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbeab-140">Remarks</span></span>

<span data-ttu-id="cbeab-141">Das **GetAppManifestsResponseMessage** -Element gilt für Clients, die auf Exchange Online und Versionen von Exchange Server, beginnend mit Exchange 2013, abzielen.</span><span class="sxs-lookup"><span data-stu-id="cbeab-141">The **GetAppManifestsResponseMessage** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="cbeab-142">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cbeab-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbeab-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="cbeab-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cbeab-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cbeab-144">Schema Name</span></span>  <br/> |<span data-ttu-id="cbeab-145">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cbeab-145">Message schema</span></span>  <br/> |
|<span data-ttu-id="cbeab-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cbeab-146">Validation File</span></span>  <br/> |<span data-ttu-id="cbeab-147">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cbeab-147">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cbeab-148">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cbeab-148">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="cbeab-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbeab-149">See also</span></span>



- [<span data-ttu-id="cbeab-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cbeab-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

