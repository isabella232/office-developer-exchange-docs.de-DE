---
title: Der ExpandDL-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: Der Vorgang der ExpandDL werden sämtliche Mitglieder von Verteilerlisten verfügbar gemacht.
ms.openlocfilehash: e4654120881f81a79358e0e7c0ab016f94db3288
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758321"
---
# <a name="expanddl-operation"></a><span data-ttu-id="7b86f-103">Der ExpandDL-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7b86f-103">ExpandDL operation</span></span>

<span data-ttu-id="7b86f-104">Der Vorgang der ExpandDL werden sämtliche Mitglieder von Verteilerlisten verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="7b86f-104">The ExpandDL operation exposes the full membership of distribution lists.</span></span>
  
## <a name="using-the-expanddl-web-method"></a><span data-ttu-id="7b86f-105">Verwenden der Web der ExpandDL-Methode</span><span class="sxs-lookup"><span data-stu-id="7b86f-105">Using the ExpandDL Web Method</span></span>

<span data-ttu-id="7b86f-106">Der Vorgang der ExpandDL verwendet den Webdienst, der sich in besteht befindet.</span><span class="sxs-lookup"><span data-stu-id="7b86f-106">The ExpandDL operation uses the Web service that is located in Exchange.asmx.</span></span> <span data-ttu-id="7b86f-107">Diese Webdienstmethode akzeptiert ein [Postfach](mailbox.md) -Element, das entweder ein untergeordnetes Element [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) , für eine Erweiterung von Verteilerlisten öffentlichen oder ein untergeordnetes Element [ItemId](itemid.md) , für die Erweiterung von einem privaten enthalten kann Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="7b86f-107">This Web service method accepts a [Mailbox](mailbox.md) element that can contain either an [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) child element for an expansion of a public distribution list or an [ItemId](itemid.md) child element for the expansion of a private distribution list.</span></span> 
  
<span data-ttu-id="7b86f-108">Öffentliche Verteilerlisten können mithilfe einer der folgenden erweitert werden:</span><span class="sxs-lookup"><span data-stu-id="7b86f-108">Public distribution lists can be expanded by using one of the following:</span></span>
  
1. <span data-ttu-id="7b86f-109">Verteilung Liste alias</span><span class="sxs-lookup"><span data-stu-id="7b86f-109">Distribution list alias</span></span>
    
2. <span data-ttu-id="7b86f-110">Die Adresse des Simple Mail Transfer Protocol (SMTP)</span><span class="sxs-lookup"><span data-stu-id="7b86f-110">The Simple Mail Transfer Protocol (SMTP) address</span></span>
    
3. <span data-ttu-id="7b86f-111">X400</span><span class="sxs-lookup"><span data-stu-id="7b86f-111">X400</span></span>
    
4. <span data-ttu-id="7b86f-112">X500</span><span class="sxs-lookup"><span data-stu-id="7b86f-112">X500</span></span>
    
5. <span data-ttu-id="7b86f-113">Exchange-Legacy-Adresse</span><span class="sxs-lookup"><span data-stu-id="7b86f-113">Exchange Legacy address</span></span>
    
6. <span data-ttu-id="7b86f-114">Der Name der Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="7b86f-114">The distribution list name</span></span>
    
7. <span data-ttu-id="7b86f-115">Der Anzeigename</span><span class="sxs-lookup"><span data-stu-id="7b86f-115">The display name</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="7b86f-116">Anzeigenamen sind nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="7b86f-116">Display names are not unique.</span></span> <span data-ttu-id="7b86f-117">Mehrere Konten können demselben Anzeigenamen freigeben.</span><span class="sxs-lookup"><span data-stu-id="7b86f-117">Multiple accounts can share the same display name.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7b86f-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7b86f-118">Remarks</span></span>

<span data-ttu-id="7b86f-119">Rekursive Erweiterung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b86f-119">Recursive expansion is not supported.</span></span> <span data-ttu-id="7b86f-120">In einem einzigen Aufruf kann nur eine Verteilerliste erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="7b86f-120">Only one distribution list can be expanded in a single call.</span></span> <span data-ttu-id="7b86f-121">Wenn mehr als eine Verteilerliste die Kriterien übereinstimmen, meldet der Webdienst einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="7b86f-121">If more than one distribution list match the criteria, the Web service reports an error.</span></span> <span data-ttu-id="7b86f-122">Eine Clientanwendung können Auflösung nicht eindeutiger Namen (ANR), um mehrdeutige Verteilung aufgelistet und ausgewählt haben die richtige E-mail-Adresse der erforderlichen Verteilerliste als Parameter für den [Vorgang der ExpandDL](expanddl-operation.md)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7b86f-122">A client application can use ambiguous name resolution (ANR) to find ambiguous distribution lists and then chose the correct e-mail address of the required distribution list as a parameter for the [ExpandDL operation](expanddl-operation.md).</span></span> <span data-ttu-id="7b86f-123">Weitere Informationen finden Sie unter [ResolveNames Vorgang](resolvenames-operation.md).</span><span class="sxs-lookup"><span data-stu-id="7b86f-123">For more information, see [ResolveNames operation](resolvenames-operation.md).</span></span>
  
<span data-ttu-id="7b86f-124">Öffentliche Verteilerlisten befinden sich in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7b86f-124">Public distribution lists are located in Active Directory.</span></span> <span data-ttu-id="7b86f-125">Sie können eine beliebige e-Mail-aktivierten oder dynamische Verteilergruppe sein.</span><span class="sxs-lookup"><span data-stu-id="7b86f-125">They can be any mail-enabled or dynamic distribution group.</span></span> <span data-ttu-id="7b86f-126">Die Gruppe aus der Liste nicht ausgeblendet werden sollen, und jedes Element eine nicht leere E-mail-Adresse haben.</span><span class="sxs-lookup"><span data-stu-id="7b86f-126">The group should not be hidden from the address list and each member should have a non-empty e-mail address.</span></span> <span data-ttu-id="7b86f-127">Mitglieder der Verteilerliste können e-Mail-aktivierte Benutzer und Kontakte, öffentlichen Ordnern und e-Mail-aktivierten Verteilerlisten und dynamische Gruppen sein.</span><span class="sxs-lookup"><span data-stu-id="7b86f-127">Members of the distribution list can be mail-enabled users and contacts, public folders, and mail-enabled distribution lists and dynamic groups.</span></span>
  
<span data-ttu-id="7b86f-128">Private Verteilerlisten befinden sich im Ordner Kontakte des Postfachs eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7b86f-128">Private distribution lists are located in the Contacts folder of a user's mailbox.</span></span> <span data-ttu-id="7b86f-129">Private Verteilerlisten haben keine e-Mail-Adressen, so dass ihre Store Element-IDs in einer Anforderung der ExpandDL verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b86f-129">Private distribution lists do not have e-mail addresses so their store item identifiers are used in an ExpandDL request.</span></span> <span data-ttu-id="7b86f-130">Mitglieder von Verteilerlisten private können eine beliebige e-Mail-aktivierten Benutzer, Kontakte oder Verteilerlisten aus Active Directory oder Kontakte oder private Verteilerlisten aus Kontakteordner eines Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="7b86f-130">Members of a private distribution list can be any mail-enabled user, contacts or distribution lists from Active Directory, or contacts or private distribution lists from a user's Contacts folder.</span></span>
  
<span data-ttu-id="7b86f-131">Element-IDs werden für Kontakte oder private Verteilerlisten in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7b86f-131">For contacts or private distribution lists, the item identifiers are returned in the response.</span></span> <span data-ttu-id="7b86f-132">Dies kann zum Abrufen von Informationen über das Objekt oder die Mitgliedschaft in einer privaten Verteilerliste erweitern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b86f-132">This can be used to get information about the object or to expand membership in a private distribution list.</span></span>
  
## <a name="expanddl-private-distribution-list-request-example"></a><span data-ttu-id="7b86f-133">Anforderungsbeispiel der ExpandDL Private Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="7b86f-133">ExpandDL Private Distribution List request example</span></span>

### <a name="description"></a><span data-ttu-id="7b86f-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b86f-134">Description</span></span>

<span data-ttu-id="7b86f-135">Im folgenden Beispiel wird einer der ExpandDL Anforderung veranschaulicht eine Anforderung an eine Verteilerliste privat erweitert bilden.</span><span class="sxs-lookup"><span data-stu-id="7b86f-135">The following example of an ExpandDL request shows how to form a request to expand a private distribution list.</span></span>
  
### <a name="code"></a><span data-ttu-id="7b86f-136">Code</span><span class="sxs-lookup"><span data-stu-id="7b86f-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:ItemId Id="xASUAd==" ChangeKey="AAts0Q=="/>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="7b86f-137">Kommentare</span><span class="sxs-lookup"><span data-stu-id="7b86f-137">Comments</span></span>

<span data-ttu-id="7b86f-138">Um eine private Verteilerliste zu erweitern, wird das [Postfach](mailbox.md) -Element das [ItemId](itemid.md) -Element enthalten, das eine private Verteilerliste in das Postfach des Benutzers bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7b86f-138">To expand a private distribution list, the [Mailbox](mailbox.md) element will contain the [ItemId](itemid.md) element that identifies a private distribution list in the user's mailbox.</span></span> 
  
## <a name="expanddl-public-distribution-list-request-example"></a><span data-ttu-id="7b86f-139">Öffentliche Verteilerliste der ExpandDL anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="7b86f-139">ExpandDL Public Distribution List request example</span></span>

### <a name="description"></a><span data-ttu-id="7b86f-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b86f-140">Description</span></span>

<span data-ttu-id="7b86f-141">Im folgenden Beispiel wird einer der ExpandDL Anforderung veranschaulicht eine Anforderung an eine öffentliche Verteilerliste erweitern bilden.</span><span class="sxs-lookup"><span data-stu-id="7b86f-141">The following example of an ExpandDL request shows how to form a request to expand a public distribution list.</span></span> <span data-ttu-id="7b86f-142">Im Beispiel wird die Verwendung eines Anzeigenamens erweitern eine Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="7b86f-142">The example shows the use of a display name to expand a distribution list.</span></span>
  
### <a name="code"></a><span data-ttu-id="7b86f-143">Code</span><span class="sxs-lookup"><span data-stu-id="7b86f-143">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="7b86f-144">Kommentare</span><span class="sxs-lookup"><span data-stu-id="7b86f-144">Comments</span></span>

<span data-ttu-id="7b86f-145">Die Antwort auf diese Anforderung wird **Postfach** Elemente enthalten, die jedes Postfach in der Verteilerliste zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7b86f-145">The response to this request will contain **Mailbox** elements that identify each mailbox in the distribution list.</span></span> <span data-ttu-id="7b86f-146">Wenn eine Verteilerliste in einer Verteilerliste enthalten ist, muss eine separate Verteilerlistenerweiterung auf die eingebettete Verteilerliste ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7b86f-146">If a distribution list is contained within a distribution list, a separate distribution list expansion must be performed on the embedded distribution list.</span></span> <span data-ttu-id="7b86f-147">Wenn die Verteilerliste keine Mitglieder enthält, oder die angeforderte Verteilerliste ist nicht vorhanden, wird das Attribut **ResponseClass** einen Erfolg gleich Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="7b86f-147">If the distribution list has no members or the requested distribution list does not exist, the **ResponseClass** attribute will contain a value equal to Success.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="7b86f-148">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="7b86f-148">Request elements</span></span>

<span data-ttu-id="7b86f-149">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="7b86f-149">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="7b86f-150">Der ExpandDL</span><span class="sxs-lookup"><span data-stu-id="7b86f-150">ExpandDL</span></span>](expanddl.md)
    
- [<span data-ttu-id="7b86f-151">Postfach</span><span class="sxs-lookup"><span data-stu-id="7b86f-151">Mailbox</span></span>](mailbox.md)
    
- <span data-ttu-id="7b86f-152">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) wird verwendet, um öffentliche Verteilerlisten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7b86f-152">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) is used to identify public distribution lists.</span></span> <span data-ttu-id="7b86f-153">Das [ItemId](itemid.md) -Element wird verwendet, um private Verteilerlisten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7b86f-153">The [ItemId](itemid.md) element is used to identify private distribution lists.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="7b86f-154">Das Schema, das diese Elemente beschreibt, befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7b86f-154">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="successful-expanddl-response-example"></a><span data-ttu-id="7b86f-155">Erfolgreiche der ExpandDL antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="7b86f-155">Successful ExpandDL response example</span></span>

### <a name="description"></a><span data-ttu-id="7b86f-156">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b86f-156">Description</span></span>

<span data-ttu-id="7b86f-157">Das folgende Beispiel für eine Antwort der ExpandDL zeigt eine Antwort auf die oben beschriebenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="7b86f-157">The following example of an ExpandDL response shows a response to the request described above.</span></span> <span data-ttu-id="7b86f-158">Die Erweiterung der Verteilerliste wird Folgendes beschrieben:</span><span class="sxs-lookup"><span data-stu-id="7b86f-158">The distribution list expansion describes the following:</span></span> 
  
- <span data-ttu-id="7b86f-159">Die Anzahl der Mitglieder der Verteilerliste, die in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7b86f-159">The number of members of the distribution list that are returned in the response.</span></span>
    
- <span data-ttu-id="7b86f-160">Gibt an, ob die Antwort alle Mitglieder der Verteilerliste enthält.</span><span class="sxs-lookup"><span data-stu-id="7b86f-160">Whether the response contains all the members of the distribution list.</span></span>
    
- <span data-ttu-id="7b86f-161">Der Name des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="7b86f-161">The name of the mailbox.</span></span>
    
- <span data-ttu-id="7b86f-162">Die e-Mail-Adresse des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="7b86f-162">The e-mail address of the mailbox.</span></span>
    
- <span data-ttu-id="7b86f-163">Der Routingtyp für das Postfach.</span><span class="sxs-lookup"><span data-stu-id="7b86f-163">The routing type for the mailbox.</span></span>
    
- <span data-ttu-id="7b86f-164">Der Typ des Postfachs.</span><span class="sxs-lookup"><span data-stu-id="7b86f-164">The type of mailbox.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7b86f-165">Der Name der Verteilerliste ist nicht in der Antwort enthalten; aus diesem Grund, Sie müssen den Namen aus der Anforderung mitverfolgen.</span><span class="sxs-lookup"><span data-stu-id="7b86f-165">The distribution list name is not included in the response; therefore, you must keep track of the name from the request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="7b86f-166">Code</span><span class="sxs-lookup"><span data-stu-id="7b86f-166">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a><span data-ttu-id="7b86f-167">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="7b86f-167">Successful response elements</span></span>

<span data-ttu-id="7b86f-168">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="7b86f-168">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="7b86f-169">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7b86f-169">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="7b86f-170">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="7b86f-170">ExpandDLResponse</span></span>](expanddlresponse.md)
    
- [<span data-ttu-id="7b86f-171">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7b86f-171">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="7b86f-172">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7b86f-172">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
    
- [<span data-ttu-id="7b86f-173">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7b86f-173">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7b86f-174">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="7b86f-174">DLExpansion</span></span>](dlexpansion.md)
    
- [<span data-ttu-id="7b86f-175">Postfach</span><span class="sxs-lookup"><span data-stu-id="7b86f-175">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="7b86f-176">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="7b86f-176">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="7b86f-177">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="7b86f-177">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="7b86f-178">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="7b86f-178">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="7b86f-179">MailboxType</span><span class="sxs-lookup"><span data-stu-id="7b86f-179">MailboxType</span></span>](mailboxtype.md)
    
<span data-ttu-id="7b86f-180">Wenn andere Optionen für die Antwortnachricht des Vorgangs der ExpandDL suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="7b86f-180">To find other options for the response message of the ExpandDL operation, explore the schema hierarchy.</span></span> <span data-ttu-id="7b86f-181">Starten Sie das [ExpandDLResponse](expanddlresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="7b86f-181">Start at the [ExpandDLResponse](expanddlresponse.md) element.</span></span> 
  
## <a name="expanddl-error-response"></a><span data-ttu-id="7b86f-182">Der ExpandDL Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="7b86f-182">ExpandDL error response</span></span>

### <a name="description"></a><span data-ttu-id="7b86f-183">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b86f-183">Description</span></span>

<span data-ttu-id="7b86f-184">Das folgende Beispiel zeigt eine Fehlerantwort auf eine Anforderung der ExpandDL.</span><span class="sxs-lookup"><span data-stu-id="7b86f-184">The following example shows an error response to an ExpandDL request.</span></span>
  
### <a name="code"></a><span data-ttu-id="7b86f-185">Code</span><span class="sxs-lookup"><span data-stu-id="7b86f-185">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="7b86f-186">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="7b86f-186">Error response elements</span></span>

<span data-ttu-id="7b86f-187">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="7b86f-187">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="7b86f-188">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7b86f-188">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="7b86f-189">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="7b86f-189">ExpandDLResponse</span></span>](expanddlresponse.md)
    
- [<span data-ttu-id="7b86f-190">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7b86f-190">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="7b86f-191">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7b86f-191">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
    
- [<span data-ttu-id="7b86f-192">MessageText</span><span class="sxs-lookup"><span data-stu-id="7b86f-192">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="7b86f-193">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7b86f-193">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7b86f-194">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7b86f-194">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="7b86f-195">Wenn andere Optionen für die Antwortnachricht des Vorgangs der ExpandDL suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="7b86f-195">To find other options for the response message of the ExpandDL operation, explore the schema hierarchy.</span></span> <span data-ttu-id="7b86f-196">Starten Sie das [ExpandDLResponse](expanddlresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="7b86f-196">Start at the [ExpandDLResponse](expanddlresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7b86f-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b86f-197">See also</span></span>

- [<span data-ttu-id="7b86f-198">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7b86f-198">ResolveNames operation</span></span>](resolvenames-operation.md)
- [<span data-ttu-id="7b86f-199">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7b86f-199">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

