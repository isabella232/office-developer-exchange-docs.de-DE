---
title: ResolveNames-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: 6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb
description: Mit dem ResolveNames-Vorgang werden Mehrdeutige e-Mail-Adressen und Anzeigenamen aufgelöst.
ms.openlocfilehash: 51728addddd2bfb9d35b874ae8c11e83a4c8629b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468278"
---
# <a name="resolvenames-operation"></a><span data-ttu-id="c2fd1-103">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c2fd1-103">ResolveNames operation</span></span>

<span data-ttu-id="c2fd1-104">Mit dem **ResolveNames** -Vorgang werden Mehrdeutige e-Mail-Adressen und Anzeigenamen aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-104">The **ResolveNames** operation resolves ambiguous email addresses and display names.</span></span> 
  
## <a name="using-the-resolvenames-operation"></a><span data-ttu-id="c2fd1-105">Verwenden des ResolveNames-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="c2fd1-105">Using the ResolveNames operation</span></span>

<span data-ttu-id="c2fd1-106">Dieser Vorgang kann verwendet werden, um Aliase zu überprüfen und Anzeigenamen in den entsprechenden Postfachbenutzer aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-106">This operation can be used to verify aliases and resolve display names to the appropriate mailbox user.</span></span> <span data-ttu-id="c2fd1-107">Wenn keine eindeutigen Namen vorhanden sind, enthält die **ResolveNames** -Vorgangs Antwortinformationen zu den einzelnen Postfachbenutzern, sodass die Clientanwendung die Namen auflösen kann.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-107">If ambiguous names exist, the **ResolveNames** operation response provides information about each mailbox user so that the client application can resolve the names.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c2fd1-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2fd1-108">Remarks</span></span>

<span data-ttu-id="c2fd1-109">Die ResolveNames-Antwort gibt maximal 100 Kandidaten zurück.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-109">The ResolveNames response returns a maximum of 100 candidates.</span></span> <span data-ttu-id="c2fd1-110">Die 100 Kandidaten, die zurückgegeben werden, sind die ersten 100, die im Nachschlagevorgang gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-110">The 100 candidates that are returned are the first 100 that are encountered in the lookup operation.</span></span>
  
<span data-ttu-id="c2fd1-111">E-Mail-Adressen mit vorfixierten Routing Typen wie SMTP oder SIP werden in einem mehrwertigen Array gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-111">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="c2fd1-112">Der **ResolveNames** -Vorgang führt eine partielle Übereinstimmung mit jedem Wert dieses Arrays aus, wenn Sie den Routingtyp am Anfang des nicht aufgelösten namens hinzufügen, beispielsweise "SIP:user1@contoso.com".</span><span class="sxs-lookup"><span data-stu-id="c2fd1-112">The **ResolveNames** operation performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="c2fd1-113">Wenn Sie keinen Routingtyp angeben, wird **ResolveNames** standardmäßig mit dem Routingtyp SMTP, mit einer primären SMTP-Adress Eigenschaft übereinstimmen und nicht mit dem mehrwertigen Array durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-113">If you don't specify a routing type, **ResolveNames** will default to the routing type of smtp, match it to a primary smtp address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="c2fd1-114">In einer einzelnen Anforderung kann nur ein eindeutiger Name angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-114">Only one ambiguous name can be specified in a single request.</span></span> <span data-ttu-id="c2fd1-115">Active Directory wird zuerst durchsucht, und dann wird der Kontaktordner des Benutzers durchsucht.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-115">Active Directory is searched first, and then the user's contact folder is searched.</span></span> <span data-ttu-id="c2fd1-116">Aufgelöste Einträge aus dem Kontaktordner eines Benutzers weisen eine **ItemID** -Eigenschaft ungleich NULL auf, die dann in einer GetItem-Anforderung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-116">Resolved entries from a user's contact folder have a non-null **ItemId** property, which can then be used in a GetItem request.</span></span> <span data-ttu-id="c2fd1-117">Wenn es sich um die ID einer privaten Verteilerliste handelt, kann Sie in einem ExpandDL- [Vorgang](expanddl-operation.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-117">If it is the ID of a private distribution list, then it can be used in an [ExpandDL operation](expanddl-operation.md).</span></span> <span data-ttu-id="c2fd1-118">Wenn das **ReturnFullContactData** -Attribut auf **true**festgelegt ist, werden Active Directory Einträge, die mit dem **ResolveNames** -Vorgang gefunden werden, zusätzliche Eigenschaften zurückgegeben, die einen [Kontakt](contact.md)beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-118">If the **ReturnFullContactData** attribute is set to **true**, then Active Directory entries found with the **ResolveNames** operation will return additional properties that describe a [Contact](contact.md).</span></span> <span data-ttu-id="c2fd1-119">Das **ReturnFullContactData** -Attribut wirkt sich nicht auf die Daten aus, die für Kontakte und private Verteilerlisten aus dem Kontaktordner des Benutzers zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-119">The **ReturnFullContactData** attribute does not affect the data that is returned for contacts and private distribution lists from the user's contact folder.</span></span> 
  
## <a name="resolvenames-request-example"></a><span data-ttu-id="c2fd1-120">ResolveNames-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="c2fd1-120">ResolveNames request example</span></span>

### <a name="description"></a><span data-ttu-id="c2fd1-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2fd1-121">Description</span></span>

<span data-ttu-id="c2fd1-122">Das folgende Beispiel einer **ResolveNames** -Anforderung zeigt, wie Sie den Eintrag des Benutzers auflösen.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-122">The following example of a **ResolveNames** request shows how to resolve the entry of User.</span></span>
  
### <a name="code"></a><span data-ttu-id="c2fd1-123">Code</span><span class="sxs-lookup"><span data-stu-id="c2fd1-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="c2fd1-124">Comments</span><span class="sxs-lookup"><span data-stu-id="c2fd1-124">Comments</span></span>

<span data-ttu-id="c2fd1-125">Die Antwort auf diese Anforderung gibt alle Einträge zurück, die mit "Jo" oder "Mi" beginnen.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-125">The response to this request will return all entries that start with "Jo" or "Mi."</span></span> <span data-ttu-id="c2fd1-126">Bei den zurückgegebenen Elementen handelt es sich um öffentliche Postfächer, öffentliche und private Verteilerlisten und Kontakte.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-126">The returned items are public mailboxes, public and private distribution lists, and contacts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c2fd1-127">Es werden nur Kontakte im Standardordner für persönliche Kontakte durchsucht.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-127">Only contacts in the default personal Contacts folder are searched.</span></span> 
  
<span data-ttu-id="c2fd1-128">Es folgen die möglichen Ergebnisse für eine **ResolveNames** -Anforderung:</span><span class="sxs-lookup"><span data-stu-id="c2fd1-128">The following are the possible results for a **ResolveNames** request:</span></span> 
  
- <span data-ttu-id="c2fd1-129">Antworten, die keine aufgelöste Entität enthalten, geben einen **ResponseClass** -Attributwert zurück, der **Error**entspricht.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-129">Responses that do not contain a resolved entity will return a **ResponseClass** attribute value equal to **Error**.</span></span> <span data-ttu-id="c2fd1-130">Das **MessageText** -Element enthält " **keine Ergebnisse werden gefunden**".</span><span class="sxs-lookup"><span data-stu-id="c2fd1-130">The **MessageText** element will contain " **No results are found**."</span></span>
    
- <span data-ttu-id="c2fd1-131">Antworten, die eine einzelne aufgelöste Entität enthalten, geben einen **ResponseClass** -Attributwert zurück, der " **Success**" entspricht.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-131">Responses that contain a single resolved entity will return a **ResponseClass** attribute value equal to **Success**.</span></span>
    
- <span data-ttu-id="c2fd1-132">Antworten, die mehrere mögliche Entitäten enthalten, geben einen **ResponseClass** -Attributwert zurück, der der **Warnung**entspricht.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-132">Responses that contain multiple possible entities will return a **ResponseClass** attribute value equal to **Warning**.</span></span> <span data-ttu-id="c2fd1-133">In diesem Fall konnte die Entität nicht in eine eindeutige Identität aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-133">In this case, the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="c2fd1-134">Das **MessageText** -Element enthält "mehrere Ergebnisse werden gefunden."</span><span class="sxs-lookup"><span data-stu-id="c2fd1-134">The **MessageText** element will contain "Multiple results are found."</span></span> 
    
### <a name="request-elements"></a><span data-ttu-id="c2fd1-135">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="c2fd1-135">Request elements</span></span>

<span data-ttu-id="c2fd1-136">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="c2fd1-136">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="c2fd1-137">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="c2fd1-137">ResolveNames</span></span>](resolvenames.md)
    
- [<span data-ttu-id="c2fd1-138">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="c2fd1-138">UnresolvedEntry</span></span>](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a><span data-ttu-id="c2fd1-139">Beispiel für erfolgreiche ResolveNames-Vorgangs Antwort</span><span class="sxs-lookup"><span data-stu-id="c2fd1-139">Successful ResolveNames operation response example</span></span>

### <a name="description"></a><span data-ttu-id="c2fd1-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2fd1-140">Description</span></span>

<span data-ttu-id="c2fd1-141">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **ResolveNames** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-141">The following example shows a successful response to a **ResolveNames** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c2fd1-142">Code</span><span class="sxs-lookup"><span data-stu-id="c2fd1-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>User2</t:Name>
                <t:EmailAddress>User2@example.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>User2</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:User2@example.com</t:Entry>
                </t:EmailAddresses>
                <t:ContactSource>ActiveDirectory</t:ContactSource>
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-resolvenames-response-elements"></a><span data-ttu-id="c2fd1-143">Erfolgreiche ResolveNames-Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="c2fd1-143">Successful ResolveNames response elements</span></span>

<span data-ttu-id="c2fd1-144">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="c2fd1-144">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="c2fd1-145">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c2fd1-145">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c2fd1-146">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="c2fd1-146">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="c2fd1-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c2fd1-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c2fd1-148">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c2fd1-148">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="c2fd1-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c2fd1-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c2fd1-150">Resolutionset</span><span class="sxs-lookup"><span data-stu-id="c2fd1-150">ResolutionSet</span></span>](resolutionset.md)
    
- [<span data-ttu-id="c2fd1-151">Lösung</span><span class="sxs-lookup"><span data-stu-id="c2fd1-151">Resolution</span></span>](resolution.md)
    
- [<span data-ttu-id="c2fd1-152">Postfach</span><span class="sxs-lookup"><span data-stu-id="c2fd1-152">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="c2fd1-153">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c2fd1-153">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="c2fd1-154">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="c2fd1-154">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="c2fd1-155">Routingtype (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="c2fd1-155">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="c2fd1-156">MailboxType</span><span class="sxs-lookup"><span data-stu-id="c2fd1-156">MailboxType</span></span>](mailboxtype.md)
    
- [<span data-ttu-id="c2fd1-157">Kontakt</span><span class="sxs-lookup"><span data-stu-id="c2fd1-157">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="c2fd1-158">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="c2fd1-158">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="c2fd1-159">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="c2fd1-159">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="c2fd1-160">Eintrag (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="c2fd1-160">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="c2fd1-161">ContactSource</span><span class="sxs-lookup"><span data-stu-id="c2fd1-161">ContactSource</span></span>](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a><span data-ttu-id="c2fd1-162">Fehlerantwort des ResolveNames-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="c2fd1-162">ResolveNames operation error response</span></span>

### <a name="description"></a><span data-ttu-id="c2fd1-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2fd1-163">Description</span></span>

<span data-ttu-id="c2fd1-164">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **ResolveNames** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-164">The following example shows an error response to a **ResolveNames** request.</span></span> <span data-ttu-id="c2fd1-165">Der Fehler wird verursacht, indem versucht wird, einen Namen aufzulösen, der nicht aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="c2fd1-165">The error is caused by trying to resolve a name that cannot be resolved.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c2fd1-166">Code</span><span class="sxs-lookup"><span data-stu-id="c2fd1-166">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Error">
          <m:MessageText>No results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="c2fd1-167">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="c2fd1-167">Error response elements</span></span>

<span data-ttu-id="c2fd1-168">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="c2fd1-168">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="c2fd1-169">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c2fd1-169">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c2fd1-170">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="c2fd1-170">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="c2fd1-171">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c2fd1-171">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c2fd1-172">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c2fd1-172">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="c2fd1-173">MessageText</span><span class="sxs-lookup"><span data-stu-id="c2fd1-173">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c2fd1-174">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c2fd1-174">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c2fd1-175">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c2fd1-175">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="c2fd1-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2fd1-176">See also</span></span>



[<span data-ttu-id="c2fd1-177">ExpandDL-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c2fd1-177">ExpandDL operation</span></span>](expanddl-operation.md)


[<span data-ttu-id="c2fd1-178">Verwenden der Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="c2fd1-178">Using Name Resolution</span></span>](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

