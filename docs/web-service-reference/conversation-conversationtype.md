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
description: Das Conversation-Element stellt eine einzelne Unterhaltung dar.
ms.openlocfilehash: 9969a6cfe1f977b1c24e03771f231f4eb03d1ac6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458936"
---
# <a name="conversation-conversationtype"></a><span data-ttu-id="44b72-103">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="44b72-103">Conversation (ConversationType)</span></span>

<span data-ttu-id="44b72-104">Das **Conversation** -Element stellt eine einzelne Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="44b72-104">The **Conversation** element represents a single conversation.</span></span> 
  
[<span data-ttu-id="44b72-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="44b72-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="44b72-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="44b72-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="44b72-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="44b72-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
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

 <span data-ttu-id="44b72-108">**ConversationType**</span><span class="sxs-lookup"><span data-stu-id="44b72-108">**ConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44b72-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="44b72-109">Attributes and elements</span></span>

<span data-ttu-id="44b72-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="44b72-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44b72-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="44b72-111">Attributes</span></span>

<span data-ttu-id="44b72-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="44b72-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44b72-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44b72-113">Child elements</span></span>

|<span data-ttu-id="44b72-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="44b72-114">**Element**</span></span>|<span data-ttu-id="44b72-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44b72-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44b72-116">ConversationId</span><span class="sxs-lookup"><span data-stu-id="44b72-116">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="44b72-117">Stellt den Bezeichner einer Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="44b72-117">Represents the identifier of a conversation.</span></span>  <br/> |
|[<span data-ttu-id="44b72-118">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="44b72-118">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="44b72-119">Stellt das Unterhaltungsthema dar.</span><span class="sxs-lookup"><span data-stu-id="44b72-119">Represents the conversation topic.</span></span> <span data-ttu-id="44b72-120">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="44b72-120">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="44b72-121">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="44b72-121">UniqueRecipients</span></span>](uniquerecipients.md) <br/> |<span data-ttu-id="44b72-122">Enthält die Empfängerliste einer Unterhaltung, die aus einem bestimmten Ordner aggregiert wurde.</span><span class="sxs-lookup"><span data-stu-id="44b72-122">Contains the recipient list of a conversation aggregated from a particular folder.</span></span> <span data-ttu-id="44b72-123">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="44b72-123">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="44b72-124">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="44b72-124">GlobalUniqueRecipients</span></span>](globaluniquerecipients.md) <br/> |<span data-ttu-id="44b72-125">Enthält die Empfängerliste einer Unterhaltung, die über ein Postfach aggregiert wurde.</span><span class="sxs-lookup"><span data-stu-id="44b72-125">Contains the recipient list of a conversation aggregated across a mailbox.</span></span> <span data-ttu-id="44b72-126">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="44b72-126">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="44b72-127">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="44b72-127">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md) <br/> |<span data-ttu-id="44b72-128">Enthält eine Liste aller Personen, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung in dem aktuellen Ordner nicht gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="44b72-128">Contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="44b72-129">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="44b72-129">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="44b72-130">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="44b72-130">GlobalUniqueUnreadSenders</span></span>](globaluniqueunreadsenders.md) <br/> |<span data-ttu-id="44b72-131">Enthält eine Liste aller Personen, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung für alle Ordner im Postfach ungelesen sind.</span><span class="sxs-lookup"><span data-stu-id="44b72-131">Contains a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44b72-132">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="44b72-132">UniqueSenders</span></span>](uniquesenders.md) <br/> |<span data-ttu-id="44b72-133">Enthält eine Liste aller Absender von Unterhaltungselementen im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="44b72-133">Contains a list of all the senders of conversation items in the current folder.</span></span> <span data-ttu-id="44b72-134">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="44b72-134">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="44b72-135">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="44b72-135">GlobalUniqueSenders</span></span>](globaluniquesenders.md) <br/> |<span data-ttu-id="44b72-136">Enthält eine Liste aller Absender von Unterhaltungselementen im Postfach.</span><span class="sxs-lookup"><span data-stu-id="44b72-136">Contains a list of all the senders of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44b72-137">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="44b72-137">LastDeliveryTime</span></span>](lastdeliverytime.md) <br/> |<span data-ttu-id="44b72-138">Enthält die Zustellungszeit der Nachricht, die zuletzt in dieser Unterhaltung im aktuellen Ordner empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="44b72-138">Contains the delivery time of the message that was last received in this conversation in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="44b72-139">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="44b72-139">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md) <br/> |<span data-ttu-id="44b72-140">Enthält die Zustellungszeit der Nachricht, die zuletzt in dieser Unterhaltung über alle Ordner im Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="44b72-140">Contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44b72-141">Kategorien</span><span class="sxs-lookup"><span data-stu-id="44b72-141">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="44b72-142">Enthält eine Auflistung von Zeichenfolgen, die die Kategorien identifizieren, die auf alle Unterhaltungselemente im aktuellen Ordner angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="44b72-142">Contains a collection of strings that identify the categories that are applied to all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="44b72-143">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="44b72-143">GlobalCategories</span></span>](globalcategories.md) <br/> |<span data-ttu-id="44b72-144">Enthält die Kategorienliste für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="44b72-144">Contains the category list for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44b72-145">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="44b72-145">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="44b72-146">Enthält den aggregierten Kennzeichen Status für Unterhaltungselemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="44b72-146">Contains the aggregated flag status for conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="44b72-147">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="44b72-147">GlobalFlagStatus</span></span>](globalflagstatus.md) <br/> |<span data-ttu-id="44b72-148">Enthält den aggregierten Kennzeichen Status für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="44b72-148">Contains the aggregated flag status for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44b72-149">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="44b72-149">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="44b72-150">Enthält einen Wert, der angibt, ob mindestens ein Unterhaltungselement im aktuellen Ordner eine Anlage aufweist.</span><span class="sxs-lookup"><span data-stu-id="44b72-150">Contains a value that indicates whether at least one conversation item in the current folder has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="44b72-151">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="44b72-151">GlobalHasAttachments</span></span>](globalhasattachments.md) <br/> |<span data-ttu-id="44b72-152">Enthält einen Wert, der angibt, ob mindestens ein Unterhaltungselement in einem Postfach eine Anlage aufweist.</span><span class="sxs-lookup"><span data-stu-id="44b72-152">Contains a value that indicates whether at least one conversation item in a mailbox has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="44b72-153">MessageCount</span><span class="sxs-lookup"><span data-stu-id="44b72-153">MessageCount</span></span>](messagecount.md) <br/> |<span data-ttu-id="44b72-154">Enthält die Gesamtzahl der Unterhaltungselemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="44b72-154">Contains the total number of conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="44b72-155">GlobalMessageCount</span><span class="sxs-lookup"><span data-stu-id="44b72-155">GlobalMessageCount</span></span>](globalmessagecount.md) <br/> |<span data-ttu-id="44b72-156">Enthält die Gesamtzahl der Unterhaltungselemente im Postfach.</span><span class="sxs-lookup"><span data-stu-id="44b72-156">Contains the total number of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44b72-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="44b72-157">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="44b72-158">Enthält die Anzahl der ungelesenen Unterhaltungselemente in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="44b72-158">Contains the count of unread conversation items within a folder.</span></span>  <br/> |
|[<span data-ttu-id="44b72-159">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="44b72-159">GlobalUnreadCount</span></span>](globalunreadcount.md) <br/> |<span data-ttu-id="44b72-160">Enthält die Anzahl aller ungelesenen Unterhaltungselemente im Postfach.</span><span class="sxs-lookup"><span data-stu-id="44b72-160">Contains a count of all the unread conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44b72-161">Größe</span><span class="sxs-lookup"><span data-stu-id="44b72-161">Size</span></span>](size.md) <br/> |<span data-ttu-id="44b72-162">Enthält die von der Größe aller Unterhaltungselemente im aktuellen Ordner berechnete Unterhaltungs Größe.</span><span class="sxs-lookup"><span data-stu-id="44b72-162">Contains the conversation size calculated from the size of all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="44b72-163">Globals</span><span class="sxs-lookup"><span data-stu-id="44b72-163">GlobalSize</span></span>](globalsize.md) <br/> |<span data-ttu-id="44b72-164">Enthält die Größe der Unterhaltung, die von der Größe aller Unterhaltungselemente im Postfach berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="44b72-164">Contains the size of the conversation calculated from the size of all conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44b72-165">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="44b72-165">ItemClasses (ArrayOfItemClassType)</span></span>](itemclasses-arrayofitemclasstype.md) <br/> |<span data-ttu-id="44b72-166">Enthält eine Liste von Elementklassen, die alle Elementklassen der Unterhaltungselemente im aktuellen Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="44b72-166">Contains a list of item classes that represents all the item classes of the conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="44b72-167">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="44b72-167">GlobalItemClasses</span></span>](globalitemclasses.md) <br/> |<span data-ttu-id="44b72-168">Enthält eine Liste von Elementklassen, die alle Elementklassen der Unterhaltungselemente in einem Postfach darstellt.</span><span class="sxs-lookup"><span data-stu-id="44b72-168">Contains a list of item classes that represents all the item classes of the conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44b72-169">Importance</span><span class="sxs-lookup"><span data-stu-id="44b72-169">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="44b72-170">Enthält die aggregierte Wichtigkeit für alle Unterhaltungselemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="44b72-170">Contains the aggregated importance for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="44b72-171">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="44b72-171">GlobalImportance</span></span>](globalimportance.md) <br/> |<span data-ttu-id="44b72-172">Enthält die aggregierte Wichtigkeit für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="44b72-172">Contains the aggregated importance for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44b72-173">ItemIds</span><span class="sxs-lookup"><span data-stu-id="44b72-173">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="44b72-174">Enthält die Auflistung von Element-IDs für alle Unterhaltungselemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="44b72-174">Contains the collection of item identifiers for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="44b72-175">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="44b72-175">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="44b72-176">Enthält die Auflistung von Element-IDs für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="44b72-176">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="44b72-177">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44b72-177">Parent elements</span></span>

|<span data-ttu-id="44b72-178">**Element**</span><span class="sxs-lookup"><span data-stu-id="44b72-178">**Element**</span></span>|<span data-ttu-id="44b72-179">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44b72-179">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44b72-180">Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="44b72-180">Conversations</span></span>](conversations-ex15websvcsotherref.md) <br/> |<span data-ttu-id="44b72-181">Enthält ein Array von Unterhaltungen, die in der **FindConversation** -Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="44b72-181">Contains an array of conversations that are returned in the **FindConversation** response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="44b72-182">Textwert</span><span class="sxs-lookup"><span data-stu-id="44b72-182">Text value</span></span>

<span data-ttu-id="44b72-183">Keine.</span><span class="sxs-lookup"><span data-stu-id="44b72-183">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44b72-184">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44b72-184">Remarks</span></span>

<span data-ttu-id="44b72-185">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="44b72-185">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44b72-186">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="44b72-186">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44b72-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="44b72-187">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="44b72-188">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="44b72-188">Schema name</span></span>  <br/> |<span data-ttu-id="44b72-189">Schematypen</span><span class="sxs-lookup"><span data-stu-id="44b72-189">Types schema</span></span>  <br/> |
|<span data-ttu-id="44b72-190">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="44b72-190">Validation file</span></span>  <br/> |<span data-ttu-id="44b72-191">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="44b72-191">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="44b72-192">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="44b72-192">Can be empty</span></span>  <br/> |<span data-ttu-id="44b72-193">False</span><span class="sxs-lookup"><span data-stu-id="44b72-193">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44b72-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44b72-194">See also</span></span>



[<span data-ttu-id="44b72-195">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="44b72-195">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="44b72-196">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="44b72-196">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="44b72-197">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="44b72-197">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

