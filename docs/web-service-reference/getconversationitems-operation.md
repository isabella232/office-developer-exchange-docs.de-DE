---
title: GetConversationItems operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8ae00a99-b37b-4194-829c-fe300db6ab99
description: Hier finden Sie Informationen zum Vorgang GetConversationItems.
ms.openlocfilehash: 9d9fb9cc04bcbb5846162c77c852defa51dff98b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758614"
---
# <a name="getconversationitems-operation"></a><span data-ttu-id="4e537-103">GetConversationItems operation</span><span class="sxs-lookup"><span data-stu-id="4e537-103">GetConversationItems operation</span></span>

<span data-ttu-id="4e537-104">Hier finden Sie Informationen zum Vorgang **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="4e537-104">Find information about the **GetConversationItems** operation.</span></span> 
  
<span data-ttu-id="4e537-105">Der Vorgang **GetConversationItems** Ruft einen oder mehrere Sätze von Elementen, die Knoten in einer Unterhaltung in angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4e537-105">The **GetConversationItems** operation gets one or more sets of items that are organized in to nodes in a conversation.</span></span> 
  
<span data-ttu-id="4e537-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4e537-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getconversationitems-operation"></a><span data-ttu-id="4e537-107">Verwenden des GetConversationItems-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="4e537-107">Using the GetConversationItems operation</span></span>

<span data-ttu-id="4e537-108">Den **GetConversationItems** -Vorgang können Sie Elemente in Unterhaltungen für Primär- und archivpostfächer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4e537-108">You can use the **GetConversationItems** operation to get items in conversations for both primary and archive mailboxes.</span></span> 
  
### <a name="getconversationitems-operation-soap-headers"></a><span data-ttu-id="4e537-109">GetConversationItems Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="4e537-109">GetConversationItems operation SOAP headers</span></span>

<span data-ttu-id="4e537-110">Der Vorgang **GetConversationItems** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="4e537-110">The **GetConversationItems** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="4e537-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="4e537-111">**Header name**</span></span>|<span data-ttu-id="4e537-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="4e537-112">**Element**</span></span>|<span data-ttu-id="4e537-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4e537-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4e537-114">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="4e537-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="4e537-115">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="4e537-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="4e537-116">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="4e537-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="4e537-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4e537-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4e537-118">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="4e537-118">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="4e537-119">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="4e537-119">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="4e537-120">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="4e537-120">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="4e537-121">Der Mindestwert für dieses Element ist **Exchange2013**.</span><span class="sxs-lookup"><span data-stu-id="4e537-121">The minimum value for this element is **Exchange2013**.</span></span> <span data-ttu-id="4e537-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4e537-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4e537-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="4e537-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="4e537-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4e537-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="4e537-125">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="4e537-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="4e537-126">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="4e537-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getconversationitems-operation-request-example-get-items-in-a-single-conversation"></a><span data-ttu-id="4e537-127">GetConversationItems Vorgang-anforderungsbeispiel: Abrufen von Elementen in einem einzelnen Gespräch</span><span class="sxs-lookup"><span data-stu-id="4e537-127">GetConversationItems operation request example: Get items in a single conversation</span></span>

<span data-ttu-id="4e537-128">Im folgenden Beispiel wird eine **GetConversationItems** Vorgang Anforderung veranschaulicht, wie alle Unterhaltungselemente in einem einzelnen Gespräch, mit Ausnahme von Elementen befindet sich im Ordner Entwürfe und gelöschte Objekte abrufen.</span><span class="sxs-lookup"><span data-stu-id="4e537-128">The following example of a **GetConversationItems** operation request shows how to get all conversation items in a single conversation, with the exception of items located in the Deleted Items and Drafts folders.</span></span> <span data-ttu-id="4e537-129">Jedes Element in der Antwort zurückgegebenen enthält eine Element-ID, einen Betreff und die Zeit, die das Element im Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="4e537-129">Each item returned in the response will contain an item identifier, a subject, and the time that the item was received in the mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4e537-130">Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e537-130">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="4e537-131">In diesem Beispiel wird eine Anforderung **GetConversationItems** enthält keinen die folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="4e537-131">This example of a **GetConversationItems** request does not include the following options:</span></span> 
  
- <span data-ttu-id="4e537-132">Das Element [MaxItemsToReturn](maxitemstoreturn.md) , das die maximale Anzahl der Elemente in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4e537-132">The [MaxItemsToReturn](maxitemstoreturn.md) element, which sets the maximum number of items to return in the response.</span></span> 
    
- <span data-ttu-id="4e537-133">Das [MailboxScope](mailboxscope.md) -Element, das festgelegt, dass den Postfach-Bereich durch zurück, der angibt, ob die **GetConversationItems** durchgeführt wird, auf das primäre Postfach, das Archivpostfach oder beide Postfächer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4e537-133">The [MailboxScope](mailboxscope.md) element, which sets the mailbox scope by indicating whether the **GetConversationItems** operation is to be performed on the primary mailbox, the archive mailbox, or both mailboxes.</span></span> 
    
- <span data-ttu-id="4e537-134">Das Element [Synchronisierungsstatus (base64Binary)](syncstate-base64binary.md) , das den Synchronisierungsstatus nur Unterhaltungselementen abgerufen, die neue oder aktualisierte in der Unterhaltung sind festlegt.</span><span class="sxs-lookup"><span data-stu-id="4e537-134">The [SyncState (base64Binary)](syncstate-base64binary.md) element, which sets the synchronization state to only get conversation items that are new or updated in the conversation.</span></span> <span data-ttu-id="4e537-135">Dieses Element wird für jede Unterhaltung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4e537-135">This element is set for each conversation.</span></span> 
    
<span data-ttu-id="4e537-136">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="4e537-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4e537-137">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="4e537-137">GetConversationItems</span></span>](getconversationitems.md)
    
- [<span data-ttu-id="4e537-138">ItemShape</span><span class="sxs-lookup"><span data-stu-id="4e537-138">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="4e537-139">BaseShape</span><span class="sxs-lookup"><span data-stu-id="4e537-139">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="4e537-140">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="4e537-140">AdditionalProperties</span></span>](additionalproperties.md)
    
- [<span data-ttu-id="4e537-141">FieldURI</span><span class="sxs-lookup"><span data-stu-id="4e537-141">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="4e537-142">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="4e537-142">FoldersToIgnore</span></span>](folderstoignore.md)
    
- [<span data-ttu-id="4e537-143">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="4e537-143">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="4e537-144">SortOrder (ConversationNodeSortOrder)</span><span class="sxs-lookup"><span data-stu-id="4e537-144">SortOrder (ConversationNodeSortOrder)</span></span>](sortorder-conversationnodesortorder.md)
    
- [<span data-ttu-id="4e537-145">Conversations</span><span class="sxs-lookup"><span data-stu-id="4e537-145">Conversations</span></span>](conversations-ex15websvcsotherref.md)
    
- [<span data-ttu-id="4e537-146">Unterhaltung (ConversationRequestType)</span><span class="sxs-lookup"><span data-stu-id="4e537-146">Conversation (ConversationRequestType)</span></span>](conversation-conversationrequesttype.md)
    
- [<span data-ttu-id="4e537-147">ConversationId</span><span class="sxs-lookup"><span data-stu-id="4e537-147">ConversationId</span></span>](conversationid.md)
    
## <a name="successful-getconversationitems-operation-response"></a><span data-ttu-id="4e537-148">Erfolgreiche GetConversationItems Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="4e537-148">Successful GetConversationItems operation response</span></span>

<span data-ttu-id="4e537-149">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung des **GetConversationItems** -Vorgang zum Abrufen von Elementen in einem einzelnen Gespräch.</span><span class="sxs-lookup"><span data-stu-id="4e537-149">The following example shows a successful response to a **GetConversationItems** operation request to get items in a single conversation.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15"
                           MinorVersion="0"
                           MajorBuildNumber="545"
                           MinorBuildNumber="11"
                           Version="Exchange2013"
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetConversationItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="4e537-150">Es wird empfohlen, dass Sie den Synchronisierungsstatus für nachfolgende **GetConversationItems** Vorgang Anforderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="4e537-150">We recommend that you save the SyncState for subsequent **GetConversationItems** operation requests.</span></span> 
  
<span data-ttu-id="4e537-151">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="4e537-151">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4e537-152">GetConversationItemsResponse</span><span class="sxs-lookup"><span data-stu-id="4e537-152">GetConversationItemsResponse</span></span>](getconversationitemsresponse.md)
    
- [<span data-ttu-id="4e537-153">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4e537-153">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="4e537-154">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4e537-154">GetConversationItemsResponseMessage</span></span>](getconversationitemsresponsemessage.md)
    
- [<span data-ttu-id="4e537-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4e537-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="4e537-156">Unterhaltung (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="4e537-156">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md)
    
- [<span data-ttu-id="4e537-157">ConversationId</span><span class="sxs-lookup"><span data-stu-id="4e537-157">ConversationId</span></span>](conversationid.md)
    
- [<span data-ttu-id="4e537-158">Synchronisierungsstatus (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="4e537-158">SyncState (base64Binary)</span></span>](syncstate-base64binary.md)
    
- [<span data-ttu-id="4e537-159">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="4e537-159">ConversationNodes</span></span>](conversationnodes.md)
    
- [<span data-ttu-id="4e537-160">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="4e537-160">ConversationNode</span></span>](conversationnode.md)
    
- [<span data-ttu-id="4e537-161">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="4e537-161">InternetMessageId</span></span>](internetmessageid.md)
    
- [<span data-ttu-id="4e537-162">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="4e537-162">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="4e537-163">Message</span><span class="sxs-lookup"><span data-stu-id="4e537-163">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="4e537-164">ItemId</span><span class="sxs-lookup"><span data-stu-id="4e537-164">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="4e537-165">Betreff</span><span class="sxs-lookup"><span data-stu-id="4e537-165">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="4e537-166">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="4e537-166">DateTimeReceived</span></span>](datetimereceived.md)
    
## <a name="getconversationitems-operation-error-response"></a><span data-ttu-id="4e537-167">GetConversationItems Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="4e537-167">GetConversationItems operation error response</span></span>

<span data-ttu-id="4e537-168">Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetConversationItems** Vorgang Anforderung zum Abrufen von Elementen in einer Unterhaltung, die entweder nicht mehr vorhanden ist, im Postfach oder für die alle Unterhaltungselemente im Ordner gespeichert sind, die ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="4e537-168">The following example shows an error response to a **GetConversationItems** operation request to get items in a conversation that either no longer exists in the mailbox, or for which all the conversation items are located in folders that are ignored.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="556" MinorBuildNumber="8" Version="Exchange2013" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetConversationItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a><span data-ttu-id="4e537-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e537-169">See also</span></span>

- [<span data-ttu-id="4e537-170">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="4e537-170">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="4e537-171">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4e537-171">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
    
- [<span data-ttu-id="4e537-172">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="4e537-172">FindConversation operation</span></span>](findconversation-operation.md)
    

