---
title: ExpandDL-Vorgang
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: Der ExpandDL-Vorgang macht die vollständige Mitgliedschaft in Verteilerlisten verfügbar.
ms.openlocfilehash: 8edaf057538e2c1136465f0ff7937c14477b2c47
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44454050"
---
# <a name="expanddl-operation"></a><span data-ttu-id="66a81-103">ExpandDL-Vorgang</span><span class="sxs-lookup"><span data-stu-id="66a81-103">ExpandDL operation</span></span>

<span data-ttu-id="66a81-104">Der ExpandDL-Vorgang macht die vollständige Mitgliedschaft in Verteilerlisten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="66a81-104">The ExpandDL operation exposes the full membership of distribution lists.</span></span>
  
## <a name="using-the-expanddl-web-method"></a><span data-ttu-id="66a81-105">Verwenden der ExpandDL-Webmethode</span><span class="sxs-lookup"><span data-stu-id="66a81-105">Using the ExpandDL Web Method</span></span>

<span data-ttu-id="66a81-106">Der ExpandDL-Vorgang verwendet den Webdienst, der sich in Exchange. asmx befindet.</span><span class="sxs-lookup"><span data-stu-id="66a81-106">The ExpandDL operation uses the Web service that is located in Exchange.asmx.</span></span> <span data-ttu-id="66a81-107">Diese Webdienstmethode akzeptiert ein [Mailbox](mailbox.md) -Element, das entweder ein untergeordnetes e-Mail-Element [(NonEmptyStringType)](emailaddress-nonemptystringtype.md) für eine Erweiterung einer öffentlichen Verteilerliste oder ein untergeordnetes [ItemID](itemid.md) -Element für die Erweiterung einer privaten Verteilerliste enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="66a81-107">This Web service method accepts a [Mailbox](mailbox.md) element that can contain either an [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) child element for an expansion of a public distribution list or an [ItemId](itemid.md) child element for the expansion of a private distribution list.</span></span> 
  
<span data-ttu-id="66a81-108">Öffentliche Verteilerlisten können mithilfe einer der folgenden Optionen erweitert werden:</span><span class="sxs-lookup"><span data-stu-id="66a81-108">Public distribution lists can be expanded by using one of the following:</span></span>
  
1. <span data-ttu-id="66a81-109">Alias für Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="66a81-109">Distribution list alias</span></span>
    
2. <span data-ttu-id="66a81-110">Die SMTP-Adresse (Simple Mail Transfer Protocol)</span><span class="sxs-lookup"><span data-stu-id="66a81-110">The Simple Mail Transfer Protocol (SMTP) address</span></span>
    
3. <span data-ttu-id="66a81-111">X400</span><span class="sxs-lookup"><span data-stu-id="66a81-111">X400</span></span>
    
4. <span data-ttu-id="66a81-112">X500</span><span class="sxs-lookup"><span data-stu-id="66a81-112">X500</span></span>
    
5. <span data-ttu-id="66a81-113">Exchange-Legacy Adresse</span><span class="sxs-lookup"><span data-stu-id="66a81-113">Exchange Legacy address</span></span>
    
6. <span data-ttu-id="66a81-114">Der Name der Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="66a81-114">The distribution list name</span></span>
    
7. <span data-ttu-id="66a81-115">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="66a81-115">The display name</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="66a81-116">Anzeigenamen sind nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="66a81-116">Display names are not unique.</span></span> <span data-ttu-id="66a81-117">Mehrere Konten können denselben Anzeigenamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="66a81-117">Multiple accounts can share the same display name.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="66a81-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66a81-118">Remarks</span></span>

<span data-ttu-id="66a81-119">Die rekursive Erweiterung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="66a81-119">Recursive expansion is not supported.</span></span> <span data-ttu-id="66a81-120">In einem einzigen Aufruf kann nur eine Verteilerliste erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="66a81-120">Only one distribution list can be expanded in a single call.</span></span> <span data-ttu-id="66a81-121">Wenn mehr als eine Verteilerliste den Kriterien entspricht, meldet der Webdienst einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="66a81-121">If more than one distribution list match the criteria, the Web service reports an error.</span></span> <span data-ttu-id="66a81-122">Eine Clientanwendung kann die eindeutige Namensauflösung (ANR) verwenden, um nicht eindeutige Verteilerlisten zu finden, und dann die richtige e-Mail-Adresse der erforderlichen Verteilerliste als Parameter für den [ExpandDL-Vorgang](expanddl-operation.md)ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="66a81-122">A client application can use ambiguous name resolution (ANR) to find ambiguous distribution lists and then chose the correct e-mail address of the required distribution list as a parameter for the [ExpandDL operation](expanddl-operation.md).</span></span> <span data-ttu-id="66a81-123">Weitere Informationen finden Sie unter [ResolveNames-Vorgang](resolvenames-operation.md).</span><span class="sxs-lookup"><span data-stu-id="66a81-123">For more information, see [ResolveNames operation](resolvenames-operation.md).</span></span>
  
<span data-ttu-id="66a81-124">Öffentliche Verteilerlisten befinden sich in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="66a81-124">Public distribution lists are located in Active Directory.</span></span> <span data-ttu-id="66a81-125">Dabei kann es sich um eine beliebige e-Mail-aktivierte oder dynamische Verteilergruppe handeln.</span><span class="sxs-lookup"><span data-stu-id="66a81-125">They can be any mail-enabled or dynamic distribution group.</span></span> <span data-ttu-id="66a81-126">Die Gruppe sollte nicht aus der Adressliste ausgeblendet werden, und jedes Mitglied sollte eine nicht leere e-Mail-Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="66a81-126">The group should not be hidden from the address list and each member should have a non-empty e-mail address.</span></span> <span data-ttu-id="66a81-127">Mitglieder der Verteilerliste können e-Mail-aktivierte Benutzer und Kontakte, öffentliche Ordner und e-Mail-aktivierte Verteilerlisten und dynamische Gruppen sein.</span><span class="sxs-lookup"><span data-stu-id="66a81-127">Members of the distribution list can be mail-enabled users and contacts, public folders, and mail-enabled distribution lists and dynamic groups.</span></span>
  
<span data-ttu-id="66a81-128">Private Verteilerlisten befinden sich im Ordner "Kontakte" des Postfachs eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="66a81-128">Private distribution lists are located in the Contacts folder of a user's mailbox.</span></span> <span data-ttu-id="66a81-129">Private Verteilerlisten verfügen nicht über e-Mail-Adressen, sodass Ihre Store Item Identifier in einer ExpandDL-Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66a81-129">Private distribution lists do not have e-mail addresses so their store item identifiers are used in an ExpandDL request.</span></span> <span data-ttu-id="66a81-130">Mitglieder einer privaten Verteilerliste können beliebige e-Mail-aktivierte Benutzer, Kontakte oder Verteilerlisten aus Active Directory oder Kontakte oder private Verteilerlisten aus dem Ordner Kontakte eines Benutzers sein.</span><span class="sxs-lookup"><span data-stu-id="66a81-130">Members of a private distribution list can be any mail-enabled user, contacts or distribution lists from Active Directory, or contacts or private distribution lists from a user's Contacts folder.</span></span>
  
<span data-ttu-id="66a81-131">Bei Kontakten oder privaten Verteilerlisten werden die Elementbezeichner in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="66a81-131">For contacts or private distribution lists, the item identifiers are returned in the response.</span></span> <span data-ttu-id="66a81-132">Dies kann verwendet werden, um Informationen über das Objekt abzurufen oder um die Mitgliedschaft in einer privaten Verteilerliste zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="66a81-132">This can be used to get information about the object or to expand membership in a private distribution list.</span></span>
  
## <a name="expanddl-private-distribution-list-request-example"></a><span data-ttu-id="66a81-133">ExpandDL-Beispiel für private Verteilerlisten Anforderung</span><span class="sxs-lookup"><span data-stu-id="66a81-133">ExpandDL Private Distribution List request example</span></span>

### <a name="description"></a><span data-ttu-id="66a81-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66a81-134">Description</span></span>

<span data-ttu-id="66a81-135">Im folgenden Beispiel einer ExpandDL-Anforderung wird gezeigt, wie Sie eine Anforderung zum Erweitern einer privaten Verteilerliste bilden.</span><span class="sxs-lookup"><span data-stu-id="66a81-135">The following example of an ExpandDL request shows how to form a request to expand a private distribution list.</span></span>
  
### <a name="code"></a><span data-ttu-id="66a81-136">Code</span><span class="sxs-lookup"><span data-stu-id="66a81-136">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ExpandDL>
      <m:Mailbox>
       <t:EmailAddress>test</t:EmailAddress>
      </m:Mailbox>
    </m:ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="66a81-137">Comments</span><span class="sxs-lookup"><span data-stu-id="66a81-137">Comments</span></span>

<span data-ttu-id="66a81-138">Um eine private Verteilerliste zu erweitern, enthält das [Mailbox](mailbox.md) -Element das [ItemID](itemid.md) -Element, das eine private Verteilerliste im Postfach des Benutzers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="66a81-138">To expand a private distribution list, the [Mailbox](mailbox.md) element will contain the [ItemId](itemid.md) element that identifies a private distribution list in the user's mailbox.</span></span> 
  
## <a name="expanddl-public-distribution-list-request-example"></a><span data-ttu-id="66a81-139">ExpandDL-Beispiel für öffentliche Verteilerlisten Anforderung</span><span class="sxs-lookup"><span data-stu-id="66a81-139">ExpandDL Public Distribution List request example</span></span>

### <a name="description"></a><span data-ttu-id="66a81-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66a81-140">Description</span></span>

<span data-ttu-id="66a81-141">Im folgenden Beispiel einer ExpandDL-Anforderung wird gezeigt, wie Sie eine Anforderung zum Erweitern einer öffentlichen Verteilerliste bilden.</span><span class="sxs-lookup"><span data-stu-id="66a81-141">The following example of an ExpandDL request shows how to form a request to expand a public distribution list.</span></span> <span data-ttu-id="66a81-142">Das Beispiel zeigt die Verwendung eines Anzeigenamens zum Erweitern einer Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="66a81-142">The example shows the use of a display name to expand a distribution list.</span></span>
  
### <a name="code"></a><span data-ttu-id="66a81-143">Code</span><span class="sxs-lookup"><span data-stu-id="66a81-143">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="66a81-144">Comments</span><span class="sxs-lookup"><span data-stu-id="66a81-144">Comments</span></span>

<span data-ttu-id="66a81-145">Die Antwort auf diese Anforderung enthält **Post Fach** Elemente, mit denen jedes Postfach in der Verteilerliste identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="66a81-145">The response to this request will contain **Mailbox** elements that identify each mailbox in the distribution list.</span></span> <span data-ttu-id="66a81-146">Wenn eine Verteilerliste in einer Verteilerliste enthalten ist, muss eine separate Verteilerlistenerweiterung für die eingebettete Verteilerliste ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="66a81-146">If a distribution list is contained within a distribution list, a separate distribution list expansion must be performed on the embedded distribution list.</span></span> <span data-ttu-id="66a81-147">Wenn die Verteilerliste keine Mitglieder enthält oder die angeforderte Verteilerliste nicht vorhanden ist, enthält das **ResponseClass** -Attribut einen Wert, der Success entspricht.</span><span class="sxs-lookup"><span data-stu-id="66a81-147">If the distribution list has no members or the requested distribution list does not exist, the **ResponseClass** attribute will contain a value equal to Success.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="66a81-148">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="66a81-148">Request elements</span></span>

<span data-ttu-id="66a81-149">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="66a81-149">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="66a81-150">ExpandDL</span><span class="sxs-lookup"><span data-stu-id="66a81-150">ExpandDL</span></span>](expanddl.md)
    
- [<span data-ttu-id="66a81-151">Postfach</span><span class="sxs-lookup"><span data-stu-id="66a81-151">Mailbox</span></span>](mailbox.md)
    
- <span data-ttu-id="66a81-152">[Email Adressen (NonEmptyStringType)](emailaddress-nonemptystringtype.md) werden verwendet, um öffentliche Verteilerlisten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="66a81-152">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) is used to identify public distribution lists.</span></span> <span data-ttu-id="66a81-153">Das [ItemID](itemid.md) -Element wird verwendet, um private Verteilerlisten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="66a81-153">The [ItemId](itemid.md) element is used to identify private distribution lists.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="66a81-154">Das Schema, in dem diese Elemente beschrieben werden, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="66a81-154">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="successful-expanddl-response-example"></a><span data-ttu-id="66a81-155">Erfolgreiches ExpandDL-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="66a81-155">Successful ExpandDL response example</span></span>

### <a name="description"></a><span data-ttu-id="66a81-156">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66a81-156">Description</span></span>

<span data-ttu-id="66a81-157">Das folgende Beispiel einer ExpandDL-Antwort zeigt eine Antwort auf die oben beschriebene Anforderung.</span><span class="sxs-lookup"><span data-stu-id="66a81-157">The following example of an ExpandDL response shows a response to the request described above.</span></span> <span data-ttu-id="66a81-158">Die Erweiterung der Verteilerliste beschreibt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="66a81-158">The distribution list expansion describes the following:</span></span> 
  
- <span data-ttu-id="66a81-159">Die Anzahl der Mitglieder der Verteilerliste, die in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="66a81-159">The number of members of the distribution list that are returned in the response.</span></span>
    
- <span data-ttu-id="66a81-160">Gibt an, ob die Antwort alle Mitglieder der Verteilerliste enthält.</span><span class="sxs-lookup"><span data-stu-id="66a81-160">Whether the response contains all the members of the distribution list.</span></span>
    
- <span data-ttu-id="66a81-161">Der Name des Postfachs.</span><span class="sxs-lookup"><span data-stu-id="66a81-161">The name of the mailbox.</span></span>
    
- <span data-ttu-id="66a81-162">Die e-Mail-Adresse des Postfachs.</span><span class="sxs-lookup"><span data-stu-id="66a81-162">The e-mail address of the mailbox.</span></span>
    
- <span data-ttu-id="66a81-163">Der Routingtyp für das Postfach.</span><span class="sxs-lookup"><span data-stu-id="66a81-163">The routing type for the mailbox.</span></span>
    
- <span data-ttu-id="66a81-164">Der Typ des Postfachs.</span><span class="sxs-lookup"><span data-stu-id="66a81-164">The type of mailbox.</span></span>
    
> [!NOTE]
> <span data-ttu-id="66a81-165">Der Name der Verteilerliste ist nicht in der Antwort enthalten; aus diesem Grund müssen Sie den Namen aus der Anforderung weiter verfolgen.</span><span class="sxs-lookup"><span data-stu-id="66a81-165">The distribution list name is not included in the response; therefore, you must keep track of the name from the request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="66a81-166">Code</span><span class="sxs-lookup"><span data-stu-id="66a81-166">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DLExpansion TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Mailbox>
              <t:Name>Dan Park</t:Name>
              <t:EmailAddress>dpark@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Jeff Price</t:Name>
              <t:EmailAddress>jprice@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Tanja Plate</t:Name>
              <t:EmailAddress>tplate@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
          </m:DLExpansion>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="66a81-167">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="66a81-167">Successful response elements</span></span>

<span data-ttu-id="66a81-168">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="66a81-168">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="66a81-169">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="66a81-169">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="66a81-170">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="66a81-170">ExpandDLResponse</span></span>](expanddlresponse.md)
    
- [<span data-ttu-id="66a81-171">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="66a81-171">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="66a81-172">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="66a81-172">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
    
- [<span data-ttu-id="66a81-173">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="66a81-173">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="66a81-174">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="66a81-174">DLExpansion</span></span>](dlexpansion.md)
    
- [<span data-ttu-id="66a81-175">Postfach</span><span class="sxs-lookup"><span data-stu-id="66a81-175">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="66a81-176">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="66a81-176">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="66a81-177">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="66a81-177">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="66a81-178">Routingtype (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="66a81-178">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="66a81-179">MailboxType</span><span class="sxs-lookup"><span data-stu-id="66a81-179">MailboxType</span></span>](mailboxtype.md)
    
<span data-ttu-id="66a81-180">Um andere Optionen für die Antwortnachricht des ExpandDL-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="66a81-180">To find other options for the response message of the ExpandDL operation, explore the schema hierarchy.</span></span> <span data-ttu-id="66a81-181">Beginnen Sie mit dem [ExpandDLResponse](expanddlresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="66a81-181">Start at the [ExpandDLResponse](expanddlresponse.md) element.</span></span> 
  
## <a name="expanddl-error-response"></a><span data-ttu-id="66a81-182">ExpandDL-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="66a81-182">ExpandDL error response</span></span>

### <a name="description"></a><span data-ttu-id="66a81-183">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66a81-183">Description</span></span>

<span data-ttu-id="66a81-184">Das folgende Beispiel zeigt eine Fehlerantwort auf eine ExpandDL-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="66a81-184">The following example shows an error response to an ExpandDL request.</span></span>
  
### <a name="code"></a><span data-ttu-id="66a81-185">Code</span><span class="sxs-lookup"><span data-stu-id="66a81-185">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Error">
          <m:MessageText>No results are found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="66a81-186">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="66a81-186">Error response elements</span></span>

<span data-ttu-id="66a81-187">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="66a81-187">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="66a81-188">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="66a81-188">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="66a81-189">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="66a81-189">ExpandDLResponse</span></span>](expanddlresponse.md)
    
- [<span data-ttu-id="66a81-190">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="66a81-190">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="66a81-191">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="66a81-191">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
    
- [<span data-ttu-id="66a81-192">MessageText</span><span class="sxs-lookup"><span data-stu-id="66a81-192">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="66a81-193">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="66a81-193">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="66a81-194">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="66a81-194">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="66a81-195">Um andere Optionen für die Antwortnachricht des ExpandDL-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="66a81-195">To find other options for the response message of the ExpandDL operation, explore the schema hierarchy.</span></span> <span data-ttu-id="66a81-196">Beginnen Sie mit dem [ExpandDLResponse](expanddlresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="66a81-196">Start at the [ExpandDLResponse](expanddlresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66a81-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66a81-197">See also</span></span>

- [<span data-ttu-id="66a81-198">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="66a81-198">ResolveNames operation</span></span>](resolvenames-operation.md)
- [<span data-ttu-id="66a81-199">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="66a81-199">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

