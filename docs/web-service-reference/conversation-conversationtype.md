---
title: Unterhaltung (ConversationType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conversation
api_type:
- schema
ms.assetid: 59d014cd-5886-49ea-8d36-ba5de7e675de
description: Das Unterhaltung-Element darstellt, einem einzelnen Gespräch.
ms.openlocfilehash: e1ae055d6a77fc5a9b483341830b978e0c1a5b5a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757696"
---
# <a name="conversation-conversationtype"></a><span data-ttu-id="d98e7-103">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="d98e7-103">Conversation (ConversationType)</span></span>

<span data-ttu-id="d98e7-104">Das **Unterhaltung** -Element darstellt, einem einzelnen Gespräch.</span><span class="sxs-lookup"><span data-stu-id="d98e7-104">The **Conversation** element represents a single conversation.</span></span> 
  
[<span data-ttu-id="d98e7-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="d98e7-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="d98e7-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="d98e7-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="d98e7-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="d98e7-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
```XML
<Conversation>
   <ConversationId/>
   <ConversationTopic/>
   <UniqueRecipients/>
   <GlobalUniqueRecipients/>
   <UniqueUnreadSenders/>
   <GlobalUniqueUnreadSenders/>
   <UniqueSenders/>
   <GlobalUniqueSenders/>
   <LastDeliveryTime/>
   <GlobalLastDeliveryTime/>
   <Categories/>
   <GlobalCategories/>
   <FlagStatus/>
   <GlobalFlagStatus/>
   <HasAttachments/>
   <GlobalHasAttachments/>
   <MessageCount/>
   <GlobalMessageCount/>
   <UnreadCount/>
   <GlobalUnreadCount/>
   <Size/>   <GlobalSize/>
   <ItemClasses/>
   <GlobalItemClasses/>
   <Importance/>
   <GlobalImportance/>
   <ItemIds/>
   <GlobalItemIds/>
</Conversation>
```

 <span data-ttu-id="d98e7-108">**ConversationType**</span><span class="sxs-lookup"><span data-stu-id="d98e7-108">**ConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d98e7-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d98e7-109">Attributes and elements</span></span>

<span data-ttu-id="d98e7-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d98e7-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d98e7-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="d98e7-111">Attributes</span></span>

<span data-ttu-id="d98e7-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="d98e7-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d98e7-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d98e7-113">Child elements</span></span>

|<span data-ttu-id="d98e7-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="d98e7-114">**Element**</span></span>|<span data-ttu-id="d98e7-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d98e7-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d98e7-116">ConversationId</span><span class="sxs-lookup"><span data-stu-id="d98e7-116">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="d98e7-117">Stellt die ID einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="d98e7-117">Represents the identifier of a conversation.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-118">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="d98e7-118">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="d98e7-119">Stellt das gleichen Thema.</span><span class="sxs-lookup"><span data-stu-id="d98e7-119">Represents the conversation topic.</span></span> <span data-ttu-id="d98e7-120">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d98e7-120">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-121">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="d98e7-121">UniqueRecipients</span></span>](uniquerecipients.md) <br/> |<span data-ttu-id="d98e7-122">Enthält die Empfängerliste einer Unterhaltung aus einem bestimmten Ordner aggregiert.</span><span class="sxs-lookup"><span data-stu-id="d98e7-122">Contains the recipient list of a conversation aggregated from a particular folder.</span></span> <span data-ttu-id="d98e7-123">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d98e7-123">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-124">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="d98e7-124">GlobalUniqueRecipients</span></span>](globaluniquerecipients.md) <br/> |<span data-ttu-id="d98e7-125">Enthält die Empfängerliste einer Unterhaltung über ein Postfach aggregiert.</span><span class="sxs-lookup"><span data-stu-id="d98e7-125">Contains the recipient list of a conversation aggregated across a mailbox.</span></span> <span data-ttu-id="d98e7-126">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d98e7-126">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-127">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="d98e7-127">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md) <br/> |<span data-ttu-id="d98e7-128">Enthält eine Liste aller Personen, die Nachrichten gesendet wurden, die derzeit in dieser Unterhaltung im aktuellen Ordner ungelesen sind.</span><span class="sxs-lookup"><span data-stu-id="d98e7-128">Contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="d98e7-129">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d98e7-129">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-130">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="d98e7-130">GlobalUniqueUnreadSenders</span></span>](globaluniqueunreadsenders.md) <br/> |<span data-ttu-id="d98e7-131">Enthält eine Liste aller Personen, die Nachrichten gesendet wurden, die derzeit in dieser Unterhaltung ungelesen in allen Ordnern im Postfach sind.</span><span class="sxs-lookup"><span data-stu-id="d98e7-131">Contains a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-132">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="d98e7-132">UniqueSenders</span></span>](uniquesenders.md) <br/> |<span data-ttu-id="d98e7-133">Enthält eine Liste von allen Absendern von Unterhaltungselementen im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d98e7-133">Contains a list of all the senders of conversation items in the current folder.</span></span> <span data-ttu-id="d98e7-134">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d98e7-134">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-135">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="d98e7-135">GlobalUniqueSenders</span></span>](globaluniquesenders.md) <br/> |<span data-ttu-id="d98e7-136">Enthält eine Liste von allen Absendern von Unterhaltungselementen im Postfach.</span><span class="sxs-lookup"><span data-stu-id="d98e7-136">Contains a list of all the senders of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-137">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="d98e7-137">LastDeliveryTime</span></span>](lastdeliverytime.md) <br/> |<span data-ttu-id="d98e7-138">Enthält die Uhrzeit der Übermittlung der Nachricht, die in dieser Unterhaltung im aktuellen Ordner zuletzt empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="d98e7-138">Contains the delivery time of the message that was last received in this conversation in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-139">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="d98e7-139">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md) <br/> |<span data-ttu-id="d98e7-140">Enthält die Uhrzeit der Übermittlung der Nachricht, die zuletzt in dieser Unterhaltung in allen Ordnern im Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="d98e7-140">Contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-141">Kategorien</span><span class="sxs-lookup"><span data-stu-id="d98e7-141">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d98e7-142">Enthält eine Auflistung von Zeichenfolgen, die die Kategorien zu identifizieren, die auf alle Unterhaltungselemente im aktuellen Ordner angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d98e7-142">Contains a collection of strings that identify the categories that are applied to all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-143">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="d98e7-143">GlobalCategories</span></span>](globalcategories.md) <br/> |<span data-ttu-id="d98e7-144">Enthält die Kategorieliste für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="d98e7-144">Contains the category list for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-145">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="d98e7-145">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="d98e7-146">Enthält den aggregierten Kennzeichnungsstatus Unterhaltungselementen im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d98e7-146">Contains the aggregated flag status for conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-147">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="d98e7-147">GlobalFlagStatus</span></span>](globalflagstatus.md) <br/> |<span data-ttu-id="d98e7-148">Enthält den aggregierten Kennzeichnungsstatus für alle Unterhaltungselemente in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="d98e7-148">Contains the aggregated flag status for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-149">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="d98e7-149">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="d98e7-150">Enthält einen Wert, der angibt, ob mindestens eine unterhaltungselement im aktuellen Ordner eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="d98e7-150">Contains a value that indicates whether at least one conversation item in the current folder has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-151">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="d98e7-151">GlobalHasAttachments</span></span>](globalhasattachments.md) <br/> |<span data-ttu-id="d98e7-152">Enthält einen Wert, der angibt, ob mindestens eine unterhaltungselement in einem Postfach eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="d98e7-152">Contains a value that indicates whether at least one conversation item in a mailbox has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-153">MessageCount</span><span class="sxs-lookup"><span data-stu-id="d98e7-153">MessageCount</span></span>](messagecount.md) <br/> |<span data-ttu-id="d98e7-154">Enthält die Gesamtanzahl der Unterhaltungselemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d98e7-154">Contains the total number of conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-155">GlobalMessageCount</span><span class="sxs-lookup"><span data-stu-id="d98e7-155">GlobalMessageCount</span></span>](globalmessagecount.md) <br/> |<span data-ttu-id="d98e7-156">Die Gesamtzahl der Unterhaltungselemente im Postfach enthält.</span><span class="sxs-lookup"><span data-stu-id="d98e7-156">Contains the total number of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="d98e7-157">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="d98e7-158">Enthält die Anzahl der ungelesenen Unterhaltungselemente innerhalb eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="d98e7-158">Contains the count of unread conversation items within a folder.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-159">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="d98e7-159">GlobalUnreadCount</span></span>](globalunreadcount.md) <br/> |<span data-ttu-id="d98e7-160">Anzahl der ungelesenen Unterhaltungselemente im Postfach enthält.</span><span class="sxs-lookup"><span data-stu-id="d98e7-160">Contains a count of all the unread conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-161">Size</span><span class="sxs-lookup"><span data-stu-id="d98e7-161">Size</span></span>](size.md) <br/> |<span data-ttu-id="d98e7-162">Enthält die Unterhaltung Größe von der Größe aller Unterhaltung Elemente im aktuellen Ordner berechnet.</span><span class="sxs-lookup"><span data-stu-id="d98e7-162">Contains the conversation size calculated from the size of all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-163">GlobalSize ist</span><span class="sxs-lookup"><span data-stu-id="d98e7-163">GlobalSize</span></span>](globalsize.md) <br/> |<span data-ttu-id="d98e7-164">Enthält die Größe der Unterhaltung von der Größe aller Unterhaltung Elemente im Postfach berechnet.</span><span class="sxs-lookup"><span data-stu-id="d98e7-164">Contains the size of the conversation calculated from the size of all conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-165">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="d98e7-165">ItemClasses (ArrayOfItemClassType)</span></span>](itemclasses-arrayofitemclasstype.md) <br/> |<span data-ttu-id="d98e7-166">Enthält eine Liste der Element-Klassen, die die Element-Klassen der Unterhaltungselemente im aktuellen Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="d98e7-166">Contains a list of item classes that represents all the item classes of the conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-167">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="d98e7-167">GlobalItemClasses</span></span>](globalitemclasses.md) <br/> |<span data-ttu-id="d98e7-168">Enthält eine Liste der Element-Klassen, die die Element-Klassen der Unterhaltungselemente in einem Postfach darstellt.</span><span class="sxs-lookup"><span data-stu-id="d98e7-168">Contains a list of item classes that represents all the item classes of the conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-169">Importance</span><span class="sxs-lookup"><span data-stu-id="d98e7-169">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="d98e7-170">Enthält die aggregierte Bedeutung für alle Unterhaltungselemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d98e7-170">Contains the aggregated importance for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-171">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="d98e7-171">GlobalImportance</span></span>](globalimportance.md) <br/> |<span data-ttu-id="d98e7-172">Enthält die aggregierte Bedeutung für alle Unterhaltungselemente in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="d98e7-172">Contains the aggregated importance for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-173">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="d98e7-173">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="d98e7-174">Enthält die Auflistung der Element-IDs für alle Unterhaltungselemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d98e7-174">Contains the collection of item identifiers for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="d98e7-175">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="d98e7-175">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="d98e7-176">Enthält die Auflistung der Element-IDs für alle Unterhaltungselemente in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="d98e7-176">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d98e7-177">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d98e7-177">Parent elements</span></span>

|<span data-ttu-id="d98e7-178">**Element**</span><span class="sxs-lookup"><span data-stu-id="d98e7-178">**Element**</span></span>|<span data-ttu-id="d98e7-179">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d98e7-179">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d98e7-180">Conversations</span><span class="sxs-lookup"><span data-stu-id="d98e7-180">Conversations</span></span>](conversations-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d98e7-181">Enthält ein Array von Unterhaltungen, die in der Antwort **FindConversation** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d98e7-181">Contains an array of conversations that are returned in the **FindConversation** response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d98e7-182">Textwert</span><span class="sxs-lookup"><span data-stu-id="d98e7-182">Text value</span></span>

<span data-ttu-id="d98e7-183">Keine.</span><span class="sxs-lookup"><span data-stu-id="d98e7-183">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d98e7-184">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d98e7-184">Remarks</span></span>

<span data-ttu-id="d98e7-185">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d98e7-185">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d98e7-186">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d98e7-186">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d98e7-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="d98e7-187">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d98e7-188">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d98e7-188">Schema name</span></span>  <br/> |<span data-ttu-id="d98e7-189">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d98e7-189">Types schema</span></span>  <br/> |
|<span data-ttu-id="d98e7-190">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d98e7-190">Validation file</span></span>  <br/> |<span data-ttu-id="d98e7-191">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d98e7-191">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d98e7-192">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d98e7-192">Can be empty</span></span>  <br/> |<span data-ttu-id="d98e7-193">False</span><span class="sxs-lookup"><span data-stu-id="d98e7-193">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d98e7-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d98e7-194">See also</span></span>



[<span data-ttu-id="d98e7-195">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="d98e7-195">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="d98e7-196">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d98e7-196">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="d98e7-197">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="d98e7-197">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

