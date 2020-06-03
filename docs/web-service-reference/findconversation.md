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
description: Das FindConversation-Element definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach.
ms.openlocfilehash: 98d692132ed9375d981c95d24600b0e2c4b1d8c1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462647"
---
# <a name="findconversation"></a><span data-ttu-id="127ac-103">FindConversation</span><span class="sxs-lookup"><span data-stu-id="127ac-103">FindConversation</span></span>

<span data-ttu-id="127ac-104">Das **FindConversation** -Element definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="127ac-104">The **FindConversation** element defines a request to find conversations in a mailbox.</span></span> 
  
[<span data-ttu-id="127ac-105">FindConversation</span><span class="sxs-lookup"><span data-stu-id="127ac-105">FindConversation</span></span>](findconversation.md)
  
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

 <span data-ttu-id="127ac-106">**FindConversationType**</span><span class="sxs-lookup"><span data-stu-id="127ac-106">**FindConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="127ac-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="127ac-107">Attributes and elements</span></span>

<span data-ttu-id="127ac-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="127ac-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="127ac-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="127ac-109">Attributes</span></span>

****

|<span data-ttu-id="127ac-110">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="127ac-110">**Attribute**</span></span>|<span data-ttu-id="127ac-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="127ac-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="127ac-112">Traversal</span><span class="sxs-lookup"><span data-stu-id="127ac-112">Traversal</span></span>  <br/> |<span data-ttu-id="127ac-113">Gibt die Typen der Unterstruktur Traversal an.</span><span class="sxs-lookup"><span data-stu-id="127ac-113">Identifies the types of sub-tree traversal.</span></span> <span data-ttu-id="127ac-114">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="127ac-114">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="127ac-115">ViewFilter</span><span class="sxs-lookup"><span data-stu-id="127ac-115">ViewFilter</span></span>  <br/> |<span data-ttu-id="127ac-116">Identifiziert die Typen Ansichtsfilter.</span><span class="sxs-lookup"><span data-stu-id="127ac-116">Identifies the types view filters.</span></span> <span data-ttu-id="127ac-117">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="127ac-117">This attribute is optional.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="127ac-118">Traversal-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="127ac-118">Traversal attribute values</span></span>

****

|<span data-ttu-id="127ac-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="127ac-119">**Value**</span></span>|<span data-ttu-id="127ac-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="127ac-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="127ac-121">Flachen</span><span class="sxs-lookup"><span data-stu-id="127ac-121">Shallow</span></span>  <br/> |<span data-ttu-id="127ac-122">Gibt eine flache Durchquerung an.</span><span class="sxs-lookup"><span data-stu-id="127ac-122">Indicates a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="127ac-123">Tiefe</span><span class="sxs-lookup"><span data-stu-id="127ac-123">Deep</span></span>  <br/> |<span data-ttu-id="127ac-124">Gibt einen tiefen Durchlauf an.</span><span class="sxs-lookup"><span data-stu-id="127ac-124">Indicates a deep traversal.</span></span>  <br/> |
   
#### <a name="viewfilter-attribute-values"></a><span data-ttu-id="127ac-125">ViewFilter-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="127ac-125">ViewFilter attribute values</span></span>

****

|<span data-ttu-id="127ac-126">**Wert**</span><span class="sxs-lookup"><span data-stu-id="127ac-126">**Value**</span></span>|<span data-ttu-id="127ac-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="127ac-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="127ac-128">Alle</span><span class="sxs-lookup"><span data-stu-id="127ac-128">All</span></span>  <br/> |<span data-ttu-id="127ac-129">Suchen Sie nach allen Unterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="127ac-129">Find all conversations.</span></span>  <br/> |
|<span data-ttu-id="127ac-130">Gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="127ac-130">Flagged</span></span>  <br/> |<span data-ttu-id="127ac-131">Suchen nach gekennzeichneten Unterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="127ac-131">Find flagged conversations.</span></span>  <br/> |
|<span data-ttu-id="127ac-132">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="127ac-132">HasAttachment</span></span>  <br/> |<span data-ttu-id="127ac-133">Unterhaltungen mit Anlagen suchen.</span><span class="sxs-lookup"><span data-stu-id="127ac-133">Find conversations with attachments.</span></span>  <br/> |
|<span data-ttu-id="127ac-134">ToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="127ac-134">ToOrCcMe</span></span>  <br/> |<span data-ttu-id="127ac-135">Hier finden Sie Unterhaltungen, die an mich gerichtet oder CC 'd.</span><span class="sxs-lookup"><span data-stu-id="127ac-135">Find conversations addressed or cc'd to me.</span></span>  <br/> |
|<span data-ttu-id="127ac-136">Ungelesen</span><span class="sxs-lookup"><span data-stu-id="127ac-136">Unread</span></span>  <br/> |<span data-ttu-id="127ac-137">Suchen Sie nach ungelesenen Unterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="127ac-137">Find unread conversations.</span></span>  <br/> |
|<span data-ttu-id="127ac-138">TaskActive</span><span class="sxs-lookup"><span data-stu-id="127ac-138">TaskActive</span></span>  <br/> |<span data-ttu-id="127ac-139">Suchen Sie nach aktiven Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="127ac-139">Find active tasks.</span></span>  <br/> |
|<span data-ttu-id="127ac-140">TaskOverdue</span><span class="sxs-lookup"><span data-stu-id="127ac-140">TaskOverdue</span></span>  <br/> |<span data-ttu-id="127ac-141">Überfällige Vorgänge suchen.</span><span class="sxs-lookup"><span data-stu-id="127ac-141">Find overdue tasks.</span></span>  <br/> |
|<span data-ttu-id="127ac-142">TaskCompleted</span><span class="sxs-lookup"><span data-stu-id="127ac-142">TaskCompleted</span></span>  <br/> |<span data-ttu-id="127ac-143">Finden Sie abgeschlossene Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="127ac-143">Find completed tasks.</span></span>  <br/> |
|<span data-ttu-id="127ac-144">Noclutter</span><span class="sxs-lookup"><span data-stu-id="127ac-144">NoClutter</span></span>  <br/> |<span data-ttu-id="127ac-145">Ausschließlich für interne Zwecke.</span><span class="sxs-lookup"><span data-stu-id="127ac-145">For internal use only.</span></span>  <br/> |
|<span data-ttu-id="127ac-146">Unwichtige Elemente</span><span class="sxs-lookup"><span data-stu-id="127ac-146">Clutter</span></span>  <br/> |<span data-ttu-id="127ac-147">Ausschließlich für interne Zwecke.</span><span class="sxs-lookup"><span data-stu-id="127ac-147">For internal use only.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="127ac-148">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="127ac-148">Child elements</span></span>

|<span data-ttu-id="127ac-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="127ac-149">**Element**</span></span>|<span data-ttu-id="127ac-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="127ac-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="127ac-151">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="127ac-151">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="127ac-152">Beschreibt, wie Informationen zur ausgelagerten Unterhaltung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="127ac-152">Describes how paged conversation information is returned.</span></span>  <br/> |
|[<span data-ttu-id="127ac-153">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="127ac-153">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="127ac-154">Gibt die Bedingung an, die zum Identifizieren des Endes einer Suche, des startIndex einer Suche, der maximal zurückzugebenden Einträge und der Suchanweisungen für eine **FindItem** -oder **FindConversation** -Suche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="127ac-154">Specifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span>  <br/> |
|[<span data-ttu-id="127ac-155">SortOrder</span><span class="sxs-lookup"><span data-stu-id="127ac-155">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="127ac-156">Definiert, wie Elemente in einer [FindConversation-Vorgangs](findconversation-operation.md) Anforderung sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="127ac-156">Defines how items are sorted in a [FindConversation operation](findconversation-operation.md) request.</span></span> <span data-ttu-id="127ac-157">Die **Conversation: LastDeliveryTime** -Eigenschaft ist die einzige Eigenschaft, die beim Verwenden des **FindConversation** -Vorgangs für die Sortierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="127ac-157">The **conversation:LastDeliveryTime** property is the only property that is supported for sorting when the **FindConversation** operation is used.</span></span>  <br/> |
|[<span data-ttu-id="127ac-158">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="127ac-158">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="127ac-159">Gibt den Ordner an, in dem nach Unterhaltungen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="127ac-159">Identifies the folder to search for conversations.</span></span>  <br/> |
|[<span data-ttu-id="127ac-160">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="127ac-160">MailboxScope</span></span>](mailboxscope.md) <br/> |<span data-ttu-id="127ac-161">Gibt an, ob sich eine Suche oder ein Abruf für eine Unterhaltung entweder auf das primäre Postfach, das Archivpostfach oder sowohl auf das primäre als auch auf das Archivpostfach erstrecken soll.</span><span class="sxs-lookup"><span data-stu-id="127ac-161">Specifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="127ac-162">QueryString (querystringtype)</span><span class="sxs-lookup"><span data-stu-id="127ac-162">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="127ac-163">Gibt eine Post Fach Abfragezeichenfolge basierend auf der erweiterten Abfrage Syntax (AQS) an.</span><span class="sxs-lookup"><span data-stu-id="127ac-163">Specifies a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
|[<span data-ttu-id="127ac-164">ConversationShape</span><span class="sxs-lookup"><span data-stu-id="127ac-164">ConversationShape</span></span>](conversationshape.md) <br/> |<span data-ttu-id="127ac-165">Gibt den Eigenschaftensatz an, der in einer [FindConversation-Vorgangs](findconversation-operation.md) Antwort zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="127ac-165">Identifies the property set to return in a [FindConversation operation](findconversation-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="127ac-166">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="127ac-166">Parent elements</span></span>

<span data-ttu-id="127ac-167">Keine.</span><span class="sxs-lookup"><span data-stu-id="127ac-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="127ac-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="127ac-168">Remarks</span></span>

<span data-ttu-id="127ac-169">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="127ac-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="127ac-170">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="127ac-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="127ac-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="127ac-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="127ac-172">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="127ac-172">Schema Name</span></span>  <br/> |<span data-ttu-id="127ac-173">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="127ac-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="127ac-174">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="127ac-174">Validation File</span></span>  <br/> |<span data-ttu-id="127ac-175">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="127ac-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="127ac-176">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="127ac-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="127ac-177">False</span><span class="sxs-lookup"><span data-stu-id="127ac-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="127ac-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="127ac-178">See also</span></span>



[<span data-ttu-id="127ac-179">FindConversation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="127ac-179">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="127ac-180">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="127ac-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="127ac-181">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="127ac-181">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

