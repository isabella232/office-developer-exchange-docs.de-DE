---
title: GetConversationItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e930650-7848-4bf2-a975-026309b3ea02
description: Das GetConversationItemsResponseMessage-Element gibt die Antwortnachricht für eine Anforderung GetConversationItems.
ms.openlocfilehash: 997319193311ef9267d8f6ff14c70bfe40e2634b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758617"
---
# <a name="getconversationitemsresponsemessage"></a><span data-ttu-id="e1b3c-103">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e1b3c-103">GetConversationItemsResponseMessage</span></span>

<span data-ttu-id="e1b3c-104">Das **GetConversationItemsResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="e1b3c-104">The **GetConversationItemsResponseMessage** element specifies the response message for a **GetConversationItems** request.</span></span> 
  
```XML
<GetConversationItemsResponseMessage ResponseClass="Success | Warning | Error">
    <Conversation/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetConversationItemsResponseMessage>
```

 <span data-ttu-id="e1b3c-105">**GetConversationItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e1b3c-105">**GetConversationItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e1b3c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e1b3c-106">Attributes and elements</span></span>

<span data-ttu-id="e1b3c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e1b3c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e1b3c-108">Attributes</span></span>

|<span data-ttu-id="e1b3c-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e1b3c-109">**Attribute**</span></span>|<span data-ttu-id="e1b3c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e1b3c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1b3c-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e1b3c-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="e1b3c-112">Gibt die Klasse der Antwort.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="e1b3c-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e1b3c-113">ResponseClass</span></span>

|<span data-ttu-id="e1b3c-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e1b3c-114">**Value**</span></span>|<span data-ttu-id="e1b3c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e1b3c-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1b3c-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="e1b3c-116">Success</span></span>  <br/> |<span data-ttu-id="e1b3c-117">Gibt Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="e1b3c-118">Warning</span><span class="sxs-lookup"><span data-stu-id="e1b3c-118">Warning</span></span>  <br/> |<span data-ttu-id="e1b3c-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="e1b3c-120">Fehler</span><span class="sxs-lookup"><span data-stu-id="e1b3c-120">Error</span></span>  <br/> |<span data-ttu-id="e1b3c-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e1b3c-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e1b3c-122">Child elements</span></span>

|<span data-ttu-id="e1b3c-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="e1b3c-123">**Element**</span></span>|<span data-ttu-id="e1b3c-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e1b3c-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1b3c-125">Unterhaltung (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="e1b3c-125">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="e1b3c-126">Stellt eine einzelne Unterhaltung in einer Antwort **GetConversationItems** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-126">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
|[<span data-ttu-id="e1b3c-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e1b3c-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e1b3c-128">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="e1b3c-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="e1b3c-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e1b3c-130">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e1b3c-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e1b3c-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e1b3c-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="e1b3c-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e1b3c-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e1b3c-134">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e1b3c-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e1b3c-135">Parent elements</span></span>

|<span data-ttu-id="e1b3c-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="e1b3c-136">**Element**</span></span>|<span data-ttu-id="e1b3c-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e1b3c-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1b3c-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e1b3c-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e1b3c-139">Enthält die Antwortnachrichten für eine Exchange-Webdienste (EWS)-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1b3c-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e1b3c-140">Remarks</span></span>

<span data-ttu-id="e1b3c-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e1b3c-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e1b3c-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e1b3c-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e1b3c-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1b3c-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1b3c-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e1b3c-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e1b3c-145">Schema Name</span></span>  <br/> |<span data-ttu-id="e1b3c-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e1b3c-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="e1b3c-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e1b3c-147">Validation File</span></span>  <br/> |<span data-ttu-id="e1b3c-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e1b3c-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e1b3c-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e1b3c-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e1b3c-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1b3c-150">See also</span></span>



- [<span data-ttu-id="e1b3c-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e1b3c-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

