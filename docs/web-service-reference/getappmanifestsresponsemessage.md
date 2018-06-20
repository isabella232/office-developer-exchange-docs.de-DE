---
title: GetAppManifestsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 815908f1-4223-42d8-92dc-f8bdfc6b5df8
description: Das GetAppManifestsResponseMessage-Element gibt die Antwortnachricht für eine Anforderung GetAppManifests.
ms.openlocfilehash: 05eeef7f7194c1dc05be93ed13ebff93d5013e94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758574"
---
# <a name="getappmanifestsresponsemessage"></a><span data-ttu-id="76331-103">GetAppManifestsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="76331-103">GetAppManifestsResponseMessage</span></span>

<span data-ttu-id="76331-104">Das **GetAppManifestsResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **GetAppManifests** .</span><span class="sxs-lookup"><span data-stu-id="76331-104">The **GetAppManifestsResponseMessage** element specifies the response message for a **GetAppManifests** request.</span></span> 
  
```XML
<GetAppManifestsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppManifestsResponseMessage>
```

 <span data-ttu-id="76331-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="76331-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76331-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="76331-106">Attributes and elements</span></span>

<span data-ttu-id="76331-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="76331-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76331-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="76331-108">Attributes</span></span>

|<span data-ttu-id="76331-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="76331-109">**Attribute**</span></span>|<span data-ttu-id="76331-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76331-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="76331-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="76331-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="76331-112">Gibt die Klasse der Antwort.</span><span class="sxs-lookup"><span data-stu-id="76331-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="76331-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="76331-113">ResponseClass</span></span>

|<span data-ttu-id="76331-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="76331-114">**Value**</span></span>|<span data-ttu-id="76331-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76331-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="76331-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="76331-116">Success</span></span>  <br/> |<span data-ttu-id="76331-117">Gibt Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="76331-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="76331-118">Warning</span><span class="sxs-lookup"><span data-stu-id="76331-118">Warning</span></span>  <br/> |<span data-ttu-id="76331-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="76331-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="76331-120">Fehler</span><span class="sxs-lookup"><span data-stu-id="76331-120">Error</span></span>  <br/> |<span data-ttu-id="76331-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="76331-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="76331-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76331-122">Child elements</span></span>

|<span data-ttu-id="76331-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="76331-123">**Element**</span></span>|<span data-ttu-id="76331-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76331-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76331-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="76331-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="76331-126">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="76331-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="76331-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="76331-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="76331-128">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="76331-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="76331-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="76331-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="76331-130">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="76331-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="76331-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="76331-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="76331-132">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="76331-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="76331-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76331-133">Parent elements</span></span>

|<span data-ttu-id="76331-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="76331-134">**Element**</span></span>|<span data-ttu-id="76331-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76331-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76331-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="76331-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="76331-137">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="76331-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76331-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="76331-138">Remarks</span></span>

<span data-ttu-id="76331-139">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="76331-139">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="76331-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="76331-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76331-141">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="76331-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76331-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="76331-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="76331-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="76331-143">Schema Name</span></span>  <br/> |<span data-ttu-id="76331-144">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="76331-144">Message schema</span></span>  <br/> |
|<span data-ttu-id="76331-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="76331-145">Validation File</span></span>  <br/> |<span data-ttu-id="76331-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="76331-146">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="76331-147">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="76331-147">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="76331-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76331-148">See also</span></span>



- [<span data-ttu-id="76331-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="76331-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

