---
title: GetConversationItems-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8ae00a99-b37b-4194-829c-fe300db6ab99
description: Hier finden Sie Informationen zum GetConversationItems-Vorgang.
ms.openlocfilehash: ddeb5386e56653a32ca2e6d212518704cd0f0c58
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457781"
---
# <a name="getconversationitems-operation"></a><span data-ttu-id="e8d05-103">GetConversationItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e8d05-103">GetConversationItems operation</span></span>

<span data-ttu-id="e8d05-104">Hier finden Sie Informationen zum **GetConversationItems** -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e8d05-104">Find information about the **GetConversationItems** operation.</span></span> 
  
<span data-ttu-id="e8d05-105">Der **GetConversationItems** -Vorgang ruft eine oder mehrere Gruppen von Elementen ab, die in einer Unterhaltung in Knoten organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="e8d05-105">The **GetConversationItems** operation gets one or more sets of items that are organized in to nodes in a conversation.</span></span> 
  
<span data-ttu-id="e8d05-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e8d05-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getconversationitems-operation"></a><span data-ttu-id="e8d05-107">Verwenden des GetConversationItems-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="e8d05-107">Using the GetConversationItems operation</span></span>

<span data-ttu-id="e8d05-108">Sie können den **GetConversationItems** -Vorgang verwenden, um Elemente in Unterhaltungen für primäre und Archivpostfächer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e8d05-108">You can use the **GetConversationItems** operation to get items in conversations for both primary and archive mailboxes.</span></span> 
  
### <a name="getconversationitems-operation-soap-headers"></a><span data-ttu-id="e8d05-109">SOAP-Header des GetConversationItems-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="e8d05-109">GetConversationItems operation SOAP headers</span></span>

<span data-ttu-id="e8d05-110">Der **GetConversationItems** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e8d05-110">The **GetConversationItems** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="e8d05-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="e8d05-111">**Header name**</span></span>|<span data-ttu-id="e8d05-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8d05-112">**Element**</span></span>|<span data-ttu-id="e8d05-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8d05-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e8d05-114">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="e8d05-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="e8d05-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="e8d05-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="e8d05-116">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="e8d05-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="e8d05-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e8d05-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e8d05-118">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="e8d05-118">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="e8d05-119">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="e8d05-119">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="e8d05-120">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="e8d05-120">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="e8d05-121">Der Minimalwert für dieses Element ist **Exchange2013**.</span><span class="sxs-lookup"><span data-stu-id="e8d05-121">The minimum value for this element is **Exchange2013**.</span></span> <span data-ttu-id="e8d05-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e8d05-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e8d05-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="e8d05-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="e8d05-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e8d05-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="e8d05-125">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="e8d05-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="e8d05-126">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="e8d05-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getconversationitems-operation-request-example-get-items-in-a-single-conversation"></a><span data-ttu-id="e8d05-127">GetConversationItems-Vorgangs Anforderungs Beispiel: Abrufen von Elementen in einer einzelnen Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="e8d05-127">GetConversationItems operation request example: Get items in a single conversation</span></span>

<span data-ttu-id="e8d05-128">Im folgenden Beispiel einer **GetConversationItems** -Vorgangsanforderung wird gezeigt, wie alle Unterhaltungselemente in einer einzelnen Unterhaltung abgerufen werden, mit Ausnahme von Elementen, die sich in den Ordnern "Gelöschte Elemente" und "Entwürfe" befinden.</span><span class="sxs-lookup"><span data-stu-id="e8d05-128">The following example of a **GetConversationItems** operation request shows how to get all conversation items in a single conversation, with the exception of items located in the Deleted Items and Drafts folders.</span></span> <span data-ttu-id="e8d05-129">Jedes in der Antwort zurückgegebene Element enthält eine Element-ID, einen Betreff und die Uhrzeit, zu der das Element im Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="e8d05-129">Each item returned in the response will contain an item identifier, a subject, and the time that the item was received in the mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e8d05-130">Alle Element-IDs und Änderungsschlüssel in diesem Artikel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e8d05-130">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:GetConversationItems>
         <m:ItemShape>
            <t:BaseShape>IdOnly</t:BaseShape>
            <t:AdditionalProperties>
               <t:FieldURI FieldURI="item:Subject" />
               <t:FieldURI FieldURI="item:DateTimeReceived" />
            </t:AdditionalProperties>
         </m:ItemShape>
         <m:FoldersToIgnore>
            <t:DistinguishedFolderId Id="deleteditems" />
            <t:DistinguishedFolderId Id="drafts" />
         </m:FoldersToIgnore>
         <m:SortOrder>TreeOrderDescending</m:SortOrder>
         <m:Conversations>
            <t:Conversation>
               <t:ConversationId Id="AAQkADEzOTExYjJkakJCs=" />
            </t:Conversation>
         </m:Conversations>
      </m:GetConversationItems>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e8d05-131">In diesem Beispiel für eine **GetConversationItems** -Anforderung sind die folgenden Optionen nicht enthalten:</span><span class="sxs-lookup"><span data-stu-id="e8d05-131">This example of a **GetConversationItems** request does not include the following options:</span></span> 
  
- <span data-ttu-id="e8d05-132">Das [MaxItemsToReturn](maxitemstoreturn.md) -Element, mit dem die maximale Anzahl von Elementen festgelegt wird, die in der Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e8d05-132">The [MaxItemsToReturn](maxitemstoreturn.md) element, which sets the maximum number of items to return in the response.</span></span> 
    
- <span data-ttu-id="e8d05-133">Das [MailboxScope](mailboxscope.md) -Element, das den Post Fachbereich festlegt, indem er angibt, ob der **GetConversationItems** -Vorgang für das primäre Postfach, das Archivpostfach oder beide Postfächer ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8d05-133">The [MailboxScope](mailboxscope.md) element, which sets the mailbox scope by indicating whether the **GetConversationItems** operation is to be performed on the primary mailbox, the archive mailbox, or both mailboxes.</span></span> 
    
- <span data-ttu-id="e8d05-134">Das [von "SyncState (base64Binary)](syncstate-base64binary.md) -Element, das den Synchronisierungs Zustand so festlegt, dass nur Unterhaltungselemente abgerufen werden, die in der Unterhaltung neu oder aktualisiert sind.</span><span class="sxs-lookup"><span data-stu-id="e8d05-134">The [SyncState (base64Binary)](syncstate-base64binary.md) element, which sets the synchronization state to only get conversation items that are new or updated in the conversation.</span></span> <span data-ttu-id="e8d05-135">Dieses Element wird für jede Unterhaltung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8d05-135">This element is set for each conversation.</span></span> 
    
<span data-ttu-id="e8d05-136">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="e8d05-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e8d05-137">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="e8d05-137">GetConversationItems</span></span>](getconversationitems.md)
    
- [<span data-ttu-id="e8d05-138">ItemShape</span><span class="sxs-lookup"><span data-stu-id="e8d05-138">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="e8d05-139">BaseShape</span><span class="sxs-lookup"><span data-stu-id="e8d05-139">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="e8d05-140">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="e8d05-140">AdditionalProperties</span></span>](additionalproperties.md)
    
- [<span data-ttu-id="e8d05-141">FieldURI</span><span class="sxs-lookup"><span data-stu-id="e8d05-141">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="e8d05-142">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="e8d05-142">FoldersToIgnore</span></span>](folderstoignore.md)
    
- [<span data-ttu-id="e8d05-143">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="e8d05-143">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="e8d05-144">Sortierreihenfolge (ConversationNodeSortOrder)</span><span class="sxs-lookup"><span data-stu-id="e8d05-144">SortOrder (ConversationNodeSortOrder)</span></span>](sortorder-conversationnodesortorder.md)
    
- [<span data-ttu-id="e8d05-145">Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="e8d05-145">Conversations</span></span>](conversations-ex15websvcsotherref.md)
    
- [<span data-ttu-id="e8d05-146">Unterhaltung (ConversationRequestType)</span><span class="sxs-lookup"><span data-stu-id="e8d05-146">Conversation (ConversationRequestType)</span></span>](conversation-conversationrequesttype.md)
    
- [<span data-ttu-id="e8d05-147">ConversationId</span><span class="sxs-lookup"><span data-stu-id="e8d05-147">ConversationId</span></span>](conversationid.md)
    
## <a name="successful-getconversationitems-operation-response"></a><span data-ttu-id="e8d05-148">Erfolgreiche Reaktion des GetConversationItems-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="e8d05-148">Successful GetConversationItems operation response</span></span>

<span data-ttu-id="e8d05-149">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetConversationItems** -Vorgangsanforderung zum Abrufen von Elementen in einer einzelnen Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="e8d05-149">The following example shows a successful response to a **GetConversationItems** operation request to get items in a single conversation.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15"
                           MinorVersion="0"
                           MajorBuildNumber="545"
                           MinorBuildNumber="11"
                           Version="Exchange2013"
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetConversationItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:GetConversationItemsResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Conversation>
                  <t:ConversationId Id="AAQkADEzOTExYjJkakJCs=" />
                  <t:SyncState>AQIAAABNVkUwAgIAAABhHqHUAwIAAABNVkUxBAIAAABhHqHfBAIAAABhHqHV</t:SyncState>
                  <t:ConversationNodes>
                     <t:ConversationNode>
                        <t:InternetMessageId>6a4838fa804045e09d40c1a39b9ea916@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>15a56698d503438fbdaa18186d5b81b7@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkADEzOTQrAABhHqHfAAA=" ChangeKey="CQAAABYAAACYAABhPpaq" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T18:42:27Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>2695d2b837954d68846b0c30491f5af1@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>15a56698d503438fbdaa18186d5b81b7@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkADEzOTExYjJkLTYxZDAt" ChangeKey="CQAAABQrAABhPpaP" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:38:26Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>15a56698d503438fbdaa18186d5b81b7@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>d3113e59c89c4288ae13100d033f8dbc@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkADEzOTFNVkUxAAA=" ChangeKey="CQAAABY4QrAABhPvYK" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:37:00Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>d3113e59c89c4288ae13100d033f8dbc@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>189b712056c2430dbce334b40496ad00@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkm4QrAABhHqHUAAA=" ChangeKey="CQAAABQrAABhPpaN" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:37:05Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>189b712056c2430dbce334b40496ad00@contoso.com</t:InternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkArAABNVkUwAAA=" ChangeKey="CQAAABm4QrAABhPvYJ" />
                              <t:Subject>Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:36:00Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                  </t:ConversationNodes>
               </m:Conversation>
            </m:GetConversationItemsResponseMessage>
         </m:ResponseMessages>
      </m:GetConversationItemsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="e8d05-150">Es wird empfohlen, die von "SyncState für nachfolgende **GetConversationItems** -Vorgangsanforderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e8d05-150">We recommend that you save the SyncState for subsequent **GetConversationItems** operation requests.</span></span> 
  
<span data-ttu-id="e8d05-151">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="e8d05-151">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e8d05-152">GetConversationItemsResponse</span><span class="sxs-lookup"><span data-stu-id="e8d05-152">GetConversationItemsResponse</span></span>](getconversationitemsresponse.md)
    
- [<span data-ttu-id="e8d05-153">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e8d05-153">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e8d05-154">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e8d05-154">GetConversationItemsResponseMessage</span></span>](getconversationitemsresponsemessage.md)
    
- [<span data-ttu-id="e8d05-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e8d05-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e8d05-156">Unterhaltung (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="e8d05-156">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md)
    
- [<span data-ttu-id="e8d05-157">ConversationId</span><span class="sxs-lookup"><span data-stu-id="e8d05-157">ConversationId</span></span>](conversationid.md)
    
- [<span data-ttu-id="e8d05-158">Von "SyncState (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="e8d05-158">SyncState (base64Binary)</span></span>](syncstate-base64binary.md)
    
- [<span data-ttu-id="e8d05-159">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="e8d05-159">ConversationNodes</span></span>](conversationnodes.md)
    
- [<span data-ttu-id="e8d05-160">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="e8d05-160">ConversationNode</span></span>](conversationnode.md)
    
- [<span data-ttu-id="e8d05-161">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="e8d05-161">InternetMessageId</span></span>](internetmessageid.md)
    
- [<span data-ttu-id="e8d05-162">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="e8d05-162">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="e8d05-163">Message</span><span class="sxs-lookup"><span data-stu-id="e8d05-163">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="e8d05-164">ItemId</span><span class="sxs-lookup"><span data-stu-id="e8d05-164">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="e8d05-165">Betreff</span><span class="sxs-lookup"><span data-stu-id="e8d05-165">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="e8d05-166">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="e8d05-166">DateTimeReceived</span></span>](datetimereceived.md)
    
## <a name="getconversationitems-operation-error-response"></a><span data-ttu-id="e8d05-167">Fehlerantwort des GetConversationItems-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="e8d05-167">GetConversationItems operation error response</span></span>

<span data-ttu-id="e8d05-168">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetConversationItems** -Vorgangsanforderung zum Abrufen von Elementen in einer Unterhaltung, die entweder nicht mehr im Postfach vorhanden sind oder für die sich alle Unterhaltungselemente in ignorierten Ordnern befinden.</span><span class="sxs-lookup"><span data-stu-id="e8d05-168">The following example shows an error response to a **GetConversationItems** operation request to get items in a conversation that either no longer exists in the mailbox, or for which all the conversation items are located in folders that are ignored.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="556" MinorBuildNumber="8" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetConversationItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetConversationItemsResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:GetConversationItemsResponseMessage>
      </m:ResponseMessages>
    </m:GetConversationItemsResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="e8d05-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8d05-169">See also</span></span>

- [<span data-ttu-id="e8d05-170">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="e8d05-170">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="e8d05-171">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e8d05-171">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
    
- [<span data-ttu-id="e8d05-172">FindConversation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e8d05-172">FindConversation operation</span></span>](findconversation-operation.md)
    

