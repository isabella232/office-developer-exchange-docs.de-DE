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
description: Die ResolveNames Vorgang löst keine eindeutige e-Mail-Adressen und Anzeigenamen.
ms.openlocfilehash: 8443cf834dfdf104daeaaa92fdee3742c3fa3719
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831162"
---
# <a name="resolvenames-operation"></a><span data-ttu-id="2b98f-103">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2b98f-103">ResolveNames operation</span></span>

<span data-ttu-id="2b98f-104">Die **ResolveNames** Vorgang löst keine eindeutige e-Mail-Adressen und Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="2b98f-104">The **ResolveNames** operation resolves ambiguous email addresses and display names.</span></span> 
  
## <a name="using-the-resolvenames-operation"></a><span data-ttu-id="2b98f-105">Verwenden des Vorgangs ResolveNames</span><span class="sxs-lookup"><span data-stu-id="2b98f-105">Using the ResolveNames operation</span></span>

<span data-ttu-id="2b98f-106">Dieser Vorgang kann Aliase überprüfen und beheben Anzeigenamen auf den entsprechenden Postfachbenutzer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b98f-106">This operation can be used to verify aliases and resolve display names to the appropriate mailbox user.</span></span> <span data-ttu-id="2b98f-107">Wenn mehrdeutige Namen vorhanden ist, enthält die Antwort auf einen Vorgang **ResolveNames** Informationen zu jedem Postfachbenutzer, damit die Namen die Clientanwendung aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b98f-107">If ambiguous names exist, the **ResolveNames** operation response provides information about each mailbox user so that the client application can resolve the names.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2b98f-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b98f-108">Remarks</span></span>

<span data-ttu-id="2b98f-109">Die Antwort ResolveNames gibt maximal 100 Kandidaten zurück.</span><span class="sxs-lookup"><span data-stu-id="2b98f-109">The ResolveNames response returns a maximum of 100 candidates.</span></span> <span data-ttu-id="2b98f-110">Die 100 Kandidaten, die zurückgegeben werden, sind die ersten 100, die bei der Suche Konflikte auftreten.</span><span class="sxs-lookup"><span data-stu-id="2b98f-110">The 100 candidates that are returned are the first 100 that are encountered in the lookup operation.</span></span>
  
<span data-ttu-id="2b98f-111">E-Mail-Adressen mit vorangestellter routing Typen, wie die SMTP- oder Sip, werden in einem mehrwertigen Array gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2b98f-111">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="2b98f-112">Der **ResolveNames** Vorgang ausführt eine teilweise Übereinstimmung mit jeder Wert eines Arrays aus, wenn Sie den Routingtyp am Anfang der aufgelöste Name, beispielsweise "sip:User1@Contoso.com" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2b98f-112">The **ResolveNames** operation performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="2b98f-113">Wenn Sie eine Routingtyp nicht angeben, wird **ResolveNames** standardmäßig auf den Routingtyp von smtp, es zu einer primären SMTP-Adresse-Eigenschaft entspricht und nicht durchsucht das mehrwertige Array.</span><span class="sxs-lookup"><span data-stu-id="2b98f-113">If you don't specify a routing type, **ResolveNames** will default to the routing type of smtp, match it to a primary smtp address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="2b98f-114">In einer einzelnen Anforderung kann nur ein mehrdeutiger Name angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2b98f-114">Only one ambiguous name can be specified in a single request.</span></span> <span data-ttu-id="2b98f-115">Active Directory wird zuerst durchsucht, und dann Kontaktordner des Benutzers gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="2b98f-115">Active Directory is searched first, and then the user's contact folder is searched.</span></span> <span data-ttu-id="2b98f-116">Aufgelösten Einträge aus Kontaktordner eines Benutzers haben eine ungleich Null- **ItemId** -Eigenschaft, die dann in einer GetItem-Anforderung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b98f-116">Resolved entries from a user's contact folder have a non-null **ItemId** property, which can then be used in a GetItem request.</span></span> <span data-ttu-id="2b98f-117">Wenn es sich um die ID einer privaten Verteilerliste handelt, kann sie in einem [der ExpandDL-Vorgang](expanddl-operation.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b98f-117">If it is the ID of a private distribution list, then it can be used in an [ExpandDL operation](expanddl-operation.md).</span></span> <span data-ttu-id="2b98f-118">Wenn das **ReturnFullContactData** -Attribut auf **true**festgelegt ist, gibt Active Directory-Einträge mit dem Vorgang **ResolveNames** gefunden zusätzliche Eigenschaften zurück, die einem [Kontakt](contact.md)zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2b98f-118">If the **ReturnFullContactData** attribute is set to **true**, then Active Directory entries found with the **ResolveNames** operation will return additional properties that describe a [Contact](contact.md).</span></span> <span data-ttu-id="2b98f-119">Das Attribut **ReturnFullContactData** wirkt sich nicht auf die Daten, die für Kontakte und Private zurückgegeben wird Verteilerlisten aus Kontaktordner des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="2b98f-119">The **ReturnFullContactData** attribute does not affect the data that is returned for contacts and private distribution lists from the user's contact folder.</span></span> 
  
## <a name="resolvenames-request-example"></a><span data-ttu-id="2b98f-120">ResolveNames anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="2b98f-120">ResolveNames request example</span></span>

### <a name="description"></a><span data-ttu-id="2b98f-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b98f-121">Description</span></span>

<span data-ttu-id="2b98f-122">Im folgenden Beispiel wird eine Anforderung **ResolveNames** veranschaulicht den Eintrag des Benutzers zu beheben.</span><span class="sxs-lookup"><span data-stu-id="2b98f-122">The following example of a **ResolveNames** request shows how to resolve the entry of User.</span></span>
  
### <a name="code"></a><span data-ttu-id="2b98f-123">Code</span><span class="sxs-lookup"><span data-stu-id="2b98f-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="2b98f-124">Kommentare</span><span class="sxs-lookup"><span data-stu-id="2b98f-124">Comments</span></span>

<span data-ttu-id="2b98f-125">Die Antwort auf diese Anforderung werden alle Einträge zurückgegeben, die beginnen mit "Jo" oder "Mi".</span><span class="sxs-lookup"><span data-stu-id="2b98f-125">The response to this request will return all entries that start with "Jo" or "Mi."</span></span> <span data-ttu-id="2b98f-126">Die zurückgegebenen Elemente sind öffentliche Postfächer, öffentliche und private Verteilerlisten und Kontakte.</span><span class="sxs-lookup"><span data-stu-id="2b98f-126">The returned items are public mailboxes, public and private distribution lists, and contacts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2b98f-127">Es werden nur Kontakte in den Standardordner für persönliche Kontakte durchsucht.</span><span class="sxs-lookup"><span data-stu-id="2b98f-127">Only contacts in the default personal Contacts folder are searched.</span></span> 
  
<span data-ttu-id="2b98f-128">Im folgenden sind die möglichen Ergebnisse für eine Anforderung **ResolveNames** :</span><span class="sxs-lookup"><span data-stu-id="2b98f-128">The following are the possible results for a **ResolveNames** request:</span></span> 
  
- <span data-ttu-id="2b98f-129">Antworten, die eine aufgelöste Entität nicht enthalten, gibt einen Attributwert **ResponseClass** **Fehler**gleich zurück.</span><span class="sxs-lookup"><span data-stu-id="2b98f-129">Responses that do not contain a resolved entity will return a **ResponseClass** attribute value equal to **Error**.</span></span> <span data-ttu-id="2b98f-130">Das Element **MessageText** enthält " **keine Ergebnisse gefunden werden**."</span><span class="sxs-lookup"><span data-stu-id="2b98f-130">The **MessageText** element will contain " **No results are found**."</span></span>
    
- <span data-ttu-id="2b98f-131">Antworten mit einer einzelnen aufgelöst Entität gibt den Attributwert **ResponseClass** **Erfolg**gleich zurück.</span><span class="sxs-lookup"><span data-stu-id="2b98f-131">Responses that contain a single resolved entity will return a **ResponseClass** attribute value equal to **Success**.</span></span>
    
- <span data-ttu-id="2b98f-132">Antworten, die mehrere mögliche Entitäten enthalten, gibt einen Attributwert **ResponseClass** **Warnung**gleich zurück.</span><span class="sxs-lookup"><span data-stu-id="2b98f-132">Responses that contain multiple possible entities will return a **ResponseClass** attribute value equal to **Warning**.</span></span> <span data-ttu-id="2b98f-133">In diesem Fall konnte die Entität nicht in eine eindeutige Identität aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="2b98f-133">In this case, the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="2b98f-134">Das Element **MessageText** enthält "mehrere Ergebnisse gefunden werden."</span><span class="sxs-lookup"><span data-stu-id="2b98f-134">The **MessageText** element will contain "Multiple results are found."</span></span> 
    
### <a name="request-elements"></a><span data-ttu-id="2b98f-135">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="2b98f-135">Request elements</span></span>

<span data-ttu-id="2b98f-136">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="2b98f-136">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="2b98f-137">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="2b98f-137">ResolveNames</span></span>](resolvenames.md)
    
- [<span data-ttu-id="2b98f-138">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="2b98f-138">UnresolvedEntry</span></span>](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a><span data-ttu-id="2b98f-139">Erfolgreiche ResolveNames Vorgang antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="2b98f-139">Successful ResolveNames operation response example</span></span>

### <a name="description"></a><span data-ttu-id="2b98f-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b98f-140">Description</span></span>

<span data-ttu-id="2b98f-141">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="2b98f-141">The following example shows a successful response to a **ResolveNames** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2b98f-142">Code</span><span class="sxs-lookup"><span data-stu-id="2b98f-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-resolvenames-response-elements"></a><span data-ttu-id="2b98f-143">Erfolgreiche ResolveNames Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="2b98f-143">Successful ResolveNames response elements</span></span>

<span data-ttu-id="2b98f-144">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="2b98f-144">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="2b98f-145">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2b98f-145">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="2b98f-146">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="2b98f-146">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="2b98f-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2b98f-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2b98f-148">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2b98f-148">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="2b98f-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2b98f-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2b98f-150">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="2b98f-150">ResolutionSet</span></span>](resolutionset.md)
    
- [<span data-ttu-id="2b98f-151">Lösung</span><span class="sxs-lookup"><span data-stu-id="2b98f-151">Resolution</span></span>](resolution.md)
    
- [<span data-ttu-id="2b98f-152">Postfach</span><span class="sxs-lookup"><span data-stu-id="2b98f-152">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="2b98f-153">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="2b98f-153">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="2b98f-154">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="2b98f-154">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="2b98f-155">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="2b98f-155">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="2b98f-156">MailboxType</span><span class="sxs-lookup"><span data-stu-id="2b98f-156">MailboxType</span></span>](mailboxtype.md)
    
- [<span data-ttu-id="2b98f-157">Contact</span><span class="sxs-lookup"><span data-stu-id="2b98f-157">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="2b98f-158">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="2b98f-158">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="2b98f-159">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="2b98f-159">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="2b98f-160">Eintrag (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="2b98f-160">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="2b98f-161">ContactSource</span><span class="sxs-lookup"><span data-stu-id="2b98f-161">ContactSource</span></span>](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a><span data-ttu-id="2b98f-162">ResolveNames Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="2b98f-162">ResolveNames operation error response</span></span>

### <a name="description"></a><span data-ttu-id="2b98f-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b98f-163">Description</span></span>

<span data-ttu-id="2b98f-164">Das folgende Beispiel zeigt eine Fehlerantwort an eine Anforderung **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="2b98f-164">The following example shows an error response to a **ResolveNames** request.</span></span> <span data-ttu-id="2b98f-165">Durch den Versuch, einen Namen aufzulösen, der nicht aufgelöst werden kann, wird der Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="2b98f-165">The error is caused by trying to resolve a name that cannot be resolved.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2b98f-166">Code</span><span class="sxs-lookup"><span data-stu-id="2b98f-166">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="2b98f-167">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="2b98f-167">Error response elements</span></span>

<span data-ttu-id="2b98f-168">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="2b98f-168">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="2b98f-169">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2b98f-169">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="2b98f-170">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="2b98f-170">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="2b98f-171">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2b98f-171">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2b98f-172">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2b98f-172">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="2b98f-173">MessageText</span><span class="sxs-lookup"><span data-stu-id="2b98f-173">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2b98f-174">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2b98f-174">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2b98f-175">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2b98f-175">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="2b98f-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b98f-176">See also</span></span>



[<span data-ttu-id="2b98f-177">Der ExpandDL-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2b98f-177">ExpandDL operation</span></span>](expanddl-operation.md)


[<span data-ttu-id="2b98f-178">Verwenden von namensauflösung</span><span class="sxs-lookup"><span data-stu-id="2b98f-178">Using Name Resolution</span></span>](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

