---
title: ArchiveItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2ac58d6f-e019-4352-b82f-8ac67a171e63
description: Das ArchiveItemResponseMessage-Element gibt die Antwortnachricht an eine ArchiveItem-Anforderung an.
ms.openlocfilehash: 24d09d63cab6805194e35031d8590290573de0a9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463391"
---
# <a name="archiveitemresponsemessage"></a><span data-ttu-id="5b529-103">ArchiveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5b529-103">ArchiveItemResponseMessage</span></span>

<span data-ttu-id="5b529-104">Das **ArchiveItemResponseMessage** -Element gibt die Antwortnachricht an eine **ArchiveItem** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="5b529-104">The **ArchiveItemResponseMessage** element specifies the response message to an **ArchiveItem** request.</span></span> 
  
```XML
<ArchiveItemResponseMessage ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
    <Items></Items>
</ArchiveItemResponseMessage>
```

 <span data-ttu-id="5b529-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="5b529-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5b529-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5b529-106">Attributes and elements</span></span>

<span data-ttu-id="5b529-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5b529-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b529-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5b529-108">Attributes</span></span>

|<span data-ttu-id="5b529-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5b529-109">**Attribute**</span></span>|<span data-ttu-id="5b529-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b529-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b529-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="5b529-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="5b529-112">Gibt die Klasse der Antwort an.</span><span class="sxs-lookup"><span data-stu-id="5b529-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="5b529-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="5b529-113">ResponseClass</span></span>

|<span data-ttu-id="5b529-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5b529-114">**Value**</span></span>|<span data-ttu-id="5b529-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b529-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b529-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="5b529-116">Success</span></span>  <br/> |<span data-ttu-id="5b529-117">Gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="5b529-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="5b529-118">Warnung</span><span class="sxs-lookup"><span data-stu-id="5b529-118">Warning</span></span>  <br/> |<span data-ttu-id="5b529-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="5b529-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="5b529-120">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="5b529-120">Error</span></span>  <br/> |<span data-ttu-id="5b529-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="5b529-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5b529-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5b529-122">Child elements</span></span>

|<span data-ttu-id="5b529-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b529-123">**Element**</span></span>|<span data-ttu-id="5b529-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b529-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b529-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5b529-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="5b529-126">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5b529-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="5b529-127">Items</span><span class="sxs-lookup"><span data-stu-id="5b529-127">Items</span></span>](items.md) <br/> |<span data-ttu-id="5b529-128">Enthält ein Array von Elementen.</span><span class="sxs-lookup"><span data-stu-id="5b529-128">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="5b529-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="5b529-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="5b529-130">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="5b529-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="5b529-131">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="5b529-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="5b529-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="5b529-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="5b529-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5b529-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="5b529-134">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="5b529-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5b529-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5b529-135">Parent elements</span></span>

|<span data-ttu-id="5b529-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b529-136">**Element**</span></span>|<span data-ttu-id="5b529-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b529-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b529-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5b529-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="5b529-139">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5b529-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b529-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b529-140">Remarks</span></span>

<span data-ttu-id="5b529-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5b529-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5b529-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5b529-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b529-143">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5b529-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b529-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b529-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5b529-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5b529-145">Schema Name</span></span>  <br/> |<span data-ttu-id="5b529-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5b529-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="5b529-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5b529-147">Validation File</span></span>  <br/> |<span data-ttu-id="5b529-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5b529-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5b529-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5b529-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="5b529-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b529-150">See also</span></span>

- [<span data-ttu-id="5b529-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5b529-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

