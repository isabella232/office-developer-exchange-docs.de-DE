---
title: FindConversation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 94b7083c-60cf-478b-a9af-a88f7acb30fb
description: Das FindConversation-Element definiert eine Anforderung an Unterhaltungen in einem Postfach suchen.
ms.openlocfilehash: 990e15f468f836d51977329c524acb439014da95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758439"
---
# <a name="findconversation"></a><span data-ttu-id="48d23-103">FindConversation</span><span class="sxs-lookup"><span data-stu-id="48d23-103">FindConversation</span></span>

<span data-ttu-id="48d23-104">Das **FindConversation** -Element definiert eine Anforderung an Unterhaltungen in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="48d23-104">The **FindConversation** element defines a request to find conversations in a mailbox.</span></span> 
  
[<span data-ttu-id="48d23-105">FindConversation</span><span class="sxs-lookup"><span data-stu-id="48d23-105">FindConversation</span></span>](findconversation.md)
  
```XML
<FindConversation Traversal="" ViewFilter="">
   <IndexedPageItemView/>
   <SeekToConditionPageItemView/>
   <SortOrder/>
   <ParentFolderId/>
   <MailboxScope/>
   <QueryString/>
   <ConversationShape/>
</FindConversation>
```

 <span data-ttu-id="48d23-106">**FindConversationType**</span><span class="sxs-lookup"><span data-stu-id="48d23-106">**FindConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="48d23-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="48d23-107">Attributes and elements</span></span>

<span data-ttu-id="48d23-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="48d23-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48d23-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="48d23-109">Attributes</span></span>

****

|<span data-ttu-id="48d23-110">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="48d23-110">**Attribute**</span></span>|<span data-ttu-id="48d23-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48d23-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48d23-112">Durchqueren</span><span class="sxs-lookup"><span data-stu-id="48d23-112">Traversal</span></span>  <br/> |<span data-ttu-id="48d23-113">Identifiziert die Typen der Teilstruktur durchqueren.</span><span class="sxs-lookup"><span data-stu-id="48d23-113">Identifies the types of sub-tree traversal.</span></span> <span data-ttu-id="48d23-114">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="48d23-114">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="48d23-115">ViewFilter</span><span class="sxs-lookup"><span data-stu-id="48d23-115">ViewFilter</span></span>  <br/> |<span data-ttu-id="48d23-116">Identifiziert die Typen Ansichtsfilter.</span><span class="sxs-lookup"><span data-stu-id="48d23-116">Identifies the types view filters.</span></span> <span data-ttu-id="48d23-117">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="48d23-117">This attribute is optional.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="48d23-118">Traversal Attributwerte</span><span class="sxs-lookup"><span data-stu-id="48d23-118">Traversal attribute values</span></span>

****

|<span data-ttu-id="48d23-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="48d23-119">**Value**</span></span>|<span data-ttu-id="48d23-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48d23-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48d23-121">Flach</span><span class="sxs-lookup"><span data-stu-id="48d23-121">Shallow</span></span>  <br/> |<span data-ttu-id="48d23-122">Gibt eine flache durchqueren an.</span><span class="sxs-lookup"><span data-stu-id="48d23-122">Indicates a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="48d23-123">Tief</span><span class="sxs-lookup"><span data-stu-id="48d23-123">Deep</span></span>  <br/> |<span data-ttu-id="48d23-124">Gibt eine Tiefe durchqueren an.</span><span class="sxs-lookup"><span data-stu-id="48d23-124">Indicates a deep traversal.</span></span>  <br/> |
   
#### <a name="viewfilter-attribute-values"></a><span data-ttu-id="48d23-125">Attributwerte ViewFilter</span><span class="sxs-lookup"><span data-stu-id="48d23-125">ViewFilter attribute values</span></span>

****

|<span data-ttu-id="48d23-126">**Wert**</span><span class="sxs-lookup"><span data-stu-id="48d23-126">**Value**</span></span>|<span data-ttu-id="48d23-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48d23-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48d23-128">Alle</span><span class="sxs-lookup"><span data-stu-id="48d23-128">All</span></span>  <br/> |<span data-ttu-id="48d23-129">Hier finden Sie alle Unterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="48d23-129">Find all conversations.</span></span>  <br/> |
|<span data-ttu-id="48d23-130">Gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="48d23-130">Flagged</span></span>  <br/> |<span data-ttu-id="48d23-131">Hier finden Sie gekennzeichnete Unterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="48d23-131">Find flagged conversations.</span></span>  <br/> |
|<span data-ttu-id="48d23-132">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="48d23-132">HasAttachment</span></span>  <br/> |<span data-ttu-id="48d23-133">Hier finden Sie Unterhaltungen mit Anlagen.</span><span class="sxs-lookup"><span data-stu-id="48d23-133">Find conversations with attachments.</span></span>  <br/> |
|<span data-ttu-id="48d23-134">ToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="48d23-134">ToOrCcMe</span></span>  <br/> |<span data-ttu-id="48d23-135">Hier finden Sie Unterhaltungen adressierte oder "Cc" mir würde.</span><span class="sxs-lookup"><span data-stu-id="48d23-135">Find conversations addressed or cc'd to me.</span></span>  <br/> |
|<span data-ttu-id="48d23-136">Unread</span><span class="sxs-lookup"><span data-stu-id="48d23-136">Unread</span></span>  <br/> |<span data-ttu-id="48d23-137">Hier finden Sie ungelesene Unterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="48d23-137">Find unread conversations.</span></span>  <br/> |
|<span data-ttu-id="48d23-138">TaskActive</span><span class="sxs-lookup"><span data-stu-id="48d23-138">TaskActive</span></span>  <br/> |<span data-ttu-id="48d23-139">Suchen Sie nach aktiven Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="48d23-139">Find active tasks.</span></span>  <br/> |
|<span data-ttu-id="48d23-140">TaskOverdue</span><span class="sxs-lookup"><span data-stu-id="48d23-140">TaskOverdue</span></span>  <br/> |<span data-ttu-id="48d23-141">Hier finden Sie überfällige Aufgaben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48d23-141">Find overdue tasks.</span></span>  <br/> |
|<span data-ttu-id="48d23-142">Aufruft</span><span class="sxs-lookup"><span data-stu-id="48d23-142">TaskCompleted</span></span>  <br/> |<span data-ttu-id="48d23-143">Suchen Sie nach abgeschlossenen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="48d23-143">Find completed tasks.</span></span>  <br/> |
|<span data-ttu-id="48d23-144">NoClutter</span><span class="sxs-lookup"><span data-stu-id="48d23-144">NoClutter</span></span>  <br/> |<span data-ttu-id="48d23-145">Nur für internen Gebrauch.</span><span class="sxs-lookup"><span data-stu-id="48d23-145">For internal use only.</span></span>  <br/> |
|<span data-ttu-id="48d23-146">Unübersichtlichkeit</span><span class="sxs-lookup"><span data-stu-id="48d23-146">Clutter</span></span>  <br/> |<span data-ttu-id="48d23-147">Nur für internen Gebrauch.</span><span class="sxs-lookup"><span data-stu-id="48d23-147">For internal use only.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="48d23-148">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48d23-148">Child elements</span></span>

|<span data-ttu-id="48d23-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="48d23-149">**Element**</span></span>|<span data-ttu-id="48d23-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48d23-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48d23-151">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="48d23-151">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="48d23-152">Beschreibt, wie ausgelagerten Unterhaltung Informationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48d23-152">Describes how paged conversation information is returned.</span></span>  <br/> |
|[<span data-ttu-id="48d23-153">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="48d23-153">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="48d23-154">Gibt die Bedingung an, die zur Identifizierung der am Ende von einer Suche, der Startindex für eine Suche, die maximale Einträge zurückgegeben und die Suche erfahren Sie, wie eine Suche **FindItem** oder **FindConversation** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="48d23-154">Specifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span>  <br/> |
|[<span data-ttu-id="48d23-155">SortOrder</span><span class="sxs-lookup"><span data-stu-id="48d23-155">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="48d23-156">Definiert, wie Elemente in einer Anforderung [FindConversation Vorgang](findconversation-operation.md) sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="48d23-156">Defines how items are sorted in a [FindConversation operation](findconversation-operation.md) request.</span></span> <span data-ttu-id="48d23-157">Die **Unterhaltung: LastDeliveryTime** -Eigenschaft ist die einzige Eigenschaft, die unterstützt werden, für die Sortierung, wenn der Vorgang **FindConversation** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="48d23-157">The **conversation:LastDeliveryTime** property is the only property that is supported for sorting when the **FindConversation** operation is used.</span></span>  <br/> |
|[<span data-ttu-id="48d23-158">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="48d23-158">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="48d23-159">Identifiziert den Ordner nach Unterhaltungen suchen.</span><span class="sxs-lookup"><span data-stu-id="48d23-159">Identifies the folder to search for conversations.</span></span>  <br/> |
|[<span data-ttu-id="48d23-160">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="48d23-160">MailboxScope</span></span>](mailboxscope.md) <br/> |<span data-ttu-id="48d23-161">Gibt an, ob eine Suche oder Fetch für eine Unterhaltung das primäre Postfach, Archivpostfach oder den Primär-umfassen und Postfach archivieren soll.</span><span class="sxs-lookup"><span data-stu-id="48d23-161">Specifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="48d23-162">QueryString (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="48d23-162">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="48d23-163">Gibt ein Postfach Abfragezeichenfolge basierend auf Erweiterte Query Syntax (AQS) an.</span><span class="sxs-lookup"><span data-stu-id="48d23-163">Specifies a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
|[<span data-ttu-id="48d23-164">ConversationShape</span><span class="sxs-lookup"><span data-stu-id="48d23-164">ConversationShape</span></span>](conversationshape.md) <br/> |<span data-ttu-id="48d23-165">Bezeichnet die Eigenschaft festgelegt, dass in einer Antwort [FindConversation Vorgang](findconversation-operation.md) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48d23-165">Identifies the property set to return in a [FindConversation operation](findconversation-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="48d23-166">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48d23-166">Parent elements</span></span>

<span data-ttu-id="48d23-167">Keine.</span><span class="sxs-lookup"><span data-stu-id="48d23-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48d23-168">Hinweise</span><span class="sxs-lookup"><span data-stu-id="48d23-168">Remarks</span></span>

<span data-ttu-id="48d23-169">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="48d23-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48d23-170">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="48d23-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48d23-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="48d23-171">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="48d23-172">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="48d23-172">Schema Name</span></span>  <br/> |<span data-ttu-id="48d23-173">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="48d23-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="48d23-174">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="48d23-174">Validation File</span></span>  <br/> |<span data-ttu-id="48d23-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="48d23-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="48d23-176">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="48d23-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="48d23-177">False</span><span class="sxs-lookup"><span data-stu-id="48d23-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48d23-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48d23-178">See also</span></span>



[<span data-ttu-id="48d23-179">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="48d23-179">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="48d23-180">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="48d23-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="48d23-181">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="48d23-181">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

