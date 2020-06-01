---
title: GetConversationItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e930650-7848-4bf2-a975-026309b3ea02
description: Das GetConversationItemsResponseMessage-Element gibt die Antwortnachricht für eine GetConversationItems-Anforderung an.
ms.openlocfilehash: b38bca60bb51c24a7635391c4e23e5426366cd72
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461072"
---
# <a name="getconversationitemsresponsemessage"></a><span data-ttu-id="574f5-103">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="574f5-103">GetConversationItemsResponseMessage</span></span>

<span data-ttu-id="574f5-104">Das **GetConversationItemsResponseMessage** -Element gibt die Antwortnachricht für eine **GetConversationItems** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="574f5-104">The **GetConversationItemsResponseMessage** element specifies the response message for a **GetConversationItems** request.</span></span> 
  
```XML
<GetConversationItemsResponseMessage ResponseClass="Success | Warning | Error">
    <Conversation/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetConversationItemsResponseMessage>
```

 <span data-ttu-id="574f5-105">**GetConversationItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="574f5-105">**GetConversationItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="574f5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="574f5-106">Attributes and elements</span></span>

<span data-ttu-id="574f5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="574f5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="574f5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="574f5-108">Attributes</span></span>

|<span data-ttu-id="574f5-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="574f5-109">**Attribute**</span></span>|<span data-ttu-id="574f5-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="574f5-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="574f5-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="574f5-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="574f5-112">Gibt die Klasse der Antwort an.</span><span class="sxs-lookup"><span data-stu-id="574f5-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="574f5-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="574f5-113">ResponseClass</span></span>

|<span data-ttu-id="574f5-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="574f5-114">**Value**</span></span>|<span data-ttu-id="574f5-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="574f5-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="574f5-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="574f5-116">Success</span></span>  <br/> |<span data-ttu-id="574f5-117">Gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="574f5-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="574f5-118">Warnung</span><span class="sxs-lookup"><span data-stu-id="574f5-118">Warning</span></span>  <br/> |<span data-ttu-id="574f5-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="574f5-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="574f5-120">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="574f5-120">Error</span></span>  <br/> |<span data-ttu-id="574f5-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="574f5-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="574f5-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="574f5-122">Child elements</span></span>

|<span data-ttu-id="574f5-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="574f5-123">**Element**</span></span>|<span data-ttu-id="574f5-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="574f5-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="574f5-125">Unterhaltung (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="574f5-125">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="574f5-126">Stellt eine einzelne Unterhaltung dar, die in einer **GetConversationItems** -Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="574f5-126">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
|[<span data-ttu-id="574f5-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="574f5-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="574f5-128">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="574f5-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="574f5-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="574f5-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="574f5-130">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="574f5-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="574f5-131">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="574f5-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="574f5-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="574f5-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="574f5-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="574f5-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="574f5-134">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="574f5-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="574f5-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="574f5-135">Parent elements</span></span>

|<span data-ttu-id="574f5-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="574f5-136">**Element**</span></span>|<span data-ttu-id="574f5-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="574f5-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="574f5-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="574f5-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="574f5-139">Enthält die Antwortnachrichten für eine Exchange-Webdienste Anforderung.</span><span class="sxs-lookup"><span data-stu-id="574f5-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="574f5-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="574f5-140">Remarks</span></span>

<span data-ttu-id="574f5-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="574f5-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="574f5-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="574f5-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="574f5-143">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="574f5-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="574f5-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="574f5-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="574f5-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="574f5-145">Schema Name</span></span>  <br/> |<span data-ttu-id="574f5-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="574f5-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="574f5-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="574f5-147">Validation File</span></span>  <br/> |<span data-ttu-id="574f5-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="574f5-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="574f5-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="574f5-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="574f5-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="574f5-150">See also</span></span>



- [<span data-ttu-id="574f5-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="574f5-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

