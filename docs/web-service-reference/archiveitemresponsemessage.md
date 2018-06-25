---
title: ArchiveItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2ac58d6f-e019-4352-b82f-8ac67a171e63
description: Das ArchiveItemResponseMessage-Element gibt die Antwortnachricht als auf eine Anforderung ArchiveItem.
ms.openlocfilehash: a7832e2cb4ec91a0871de5979fd1b418c0626aa6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757376"
---
# <a name="archiveitemresponsemessage"></a><span data-ttu-id="72f92-103">ArchiveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="72f92-103">ArchiveItemResponseMessage</span></span>

<span data-ttu-id="72f92-104">Das **ArchiveItemResponseMessage** -Element gibt die Antwortnachricht als auf eine Anforderung **ArchiveItem** .</span><span class="sxs-lookup"><span data-stu-id="72f92-104">The **ArchiveItemResponseMessage** element specifies the response message to an **ArchiveItem** request.</span></span> 
  
```XML
<ArchiveItemResponseMessage ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
    <Items></Items>
</ArchiveItemResponseMessage>
```

 <span data-ttu-id="72f92-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="72f92-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="72f92-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="72f92-106">Attributes and elements</span></span>

<span data-ttu-id="72f92-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="72f92-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="72f92-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="72f92-108">Attributes</span></span>

|<span data-ttu-id="72f92-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="72f92-109">**Attribute**</span></span>|<span data-ttu-id="72f92-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="72f92-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="72f92-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="72f92-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="72f92-112">Gibt die Klasse der Antwort.</span><span class="sxs-lookup"><span data-stu-id="72f92-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="72f92-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="72f92-113">ResponseClass</span></span>

|<span data-ttu-id="72f92-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="72f92-114">**Value**</span></span>|<span data-ttu-id="72f92-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="72f92-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="72f92-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="72f92-116">Success</span></span>  <br/> |<span data-ttu-id="72f92-117">Gibt Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="72f92-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="72f92-118">Warning</span><span class="sxs-lookup"><span data-stu-id="72f92-118">Warning</span></span>  <br/> |<span data-ttu-id="72f92-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="72f92-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="72f92-120">Fehler</span><span class="sxs-lookup"><span data-stu-id="72f92-120">Error</span></span>  <br/> |<span data-ttu-id="72f92-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="72f92-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="72f92-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="72f92-122">Child elements</span></span>

|<span data-ttu-id="72f92-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="72f92-123">**Element**</span></span>|<span data-ttu-id="72f92-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="72f92-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72f92-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="72f92-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="72f92-126">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="72f92-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="72f92-127">Elemente</span><span class="sxs-lookup"><span data-stu-id="72f92-127">Items</span></span>](items.md) <br/> |<span data-ttu-id="72f92-128">Enthält ein Array von Elementen an.</span><span class="sxs-lookup"><span data-stu-id="72f92-128">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="72f92-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="72f92-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="72f92-130">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="72f92-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="72f92-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="72f92-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="72f92-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="72f92-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="72f92-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="72f92-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="72f92-134">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="72f92-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="72f92-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="72f92-135">Parent elements</span></span>

|<span data-ttu-id="72f92-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="72f92-136">**Element**</span></span>|<span data-ttu-id="72f92-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="72f92-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72f92-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="72f92-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="72f92-139">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="72f92-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72f92-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72f92-140">Remarks</span></span>

<span data-ttu-id="72f92-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="72f92-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="72f92-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="72f92-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="72f92-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="72f92-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72f92-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="72f92-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="72f92-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="72f92-145">Schema Name</span></span>  <br/> |<span data-ttu-id="72f92-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="72f92-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="72f92-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="72f92-147">Validation File</span></span>  <br/> |<span data-ttu-id="72f92-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="72f92-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="72f92-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="72f92-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="72f92-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72f92-150">See also</span></span>

- [<span data-ttu-id="72f92-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="72f92-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

