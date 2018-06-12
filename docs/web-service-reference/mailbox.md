---
title: Postfach
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mailbox
api_type:
- schema
ms.assetid: befc70fd-51cb-4258-884c-80c9050f0e82
description: Das Mailbox-Element bezeichnet ein E-Mail-aktiviertes Active Directory-Objekt.
ms.openlocfilehash: e9fa21f3678249a9ac13d567b88beaf0177f989f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830258"
---
# <a name="mailbox"></a><span data-ttu-id="57c02-103">Postfach</span><span class="sxs-lookup"><span data-stu-id="57c02-103">Mailbox</span></span>

<span data-ttu-id="57c02-104">Das **Mailbox**-Element bezeichnet ein E-Mail-aktiviertes Active Directory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="57c02-104">The **Mailbox** element identifies a mail-enabled Active Directory object.</span></span> 
  
```XML
<Mailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Mailbox>
```

<span data-ttu-id="57c02-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="57c02-105">**EmailAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="57c02-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="57c02-106">Attributes and elements</span></span>

<span data-ttu-id="57c02-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="57c02-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57c02-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="57c02-108">Attributes</span></span>

<span data-ttu-id="57c02-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="57c02-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="57c02-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="57c02-110">Child elements</span></span>

|<span data-ttu-id="57c02-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="57c02-111">**Element**</span></span>|<span data-ttu-id="57c02-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="57c02-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57c02-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="57c02-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="57c02-p101">Definiert den Namen des Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="57c02-p101">Defines the name of the mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="57c02-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="57c02-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="57c02-p102">Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="57c02-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="57c02-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="57c02-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="57c02-p103">Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="57c02-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="57c02-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="57c02-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="57c02-p104">Definiert den Postfachtyp eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="57c02-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="57c02-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="57c02-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="57c02-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="57c02-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="57c02-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="57c02-129">Parent elements</span></span>

|<span data-ttu-id="57c02-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="57c02-130">**Element**</span></span>|<span data-ttu-id="57c02-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="57c02-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57c02-132">Der ExpandDL</span><span class="sxs-lookup"><span data-stu-id="57c02-132">ExpandDL</span></span>](expanddl.md) <br/> |<span data-ttu-id="57c02-133">Definiert eine Anforderung zum Erweitern einer Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="57c02-133">Defines a request to expand a distribution list.</span></span> <br/> <br/> <span data-ttu-id="57c02-134">Für dieses Element wird folgender XPath-Ausdruck verwendet: ` /ExpandDL `</span><span class="sxs-lookup"><span data-stu-id="57c02-134">The following is the XPath expression to this element: ` /ExpandDL `</span></span> <br/> |
|[<span data-ttu-id="57c02-135">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="57c02-135">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="57c02-136">Enthält eine Reihe von Benutzern eines Elements.</span><span class="sxs-lookup"><span data-stu-id="57c02-136">Contains an array of recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="57c02-137">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="57c02-137">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="57c02-138">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="57c02-138">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="57c02-139">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="57c02-139">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="57c02-140">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="57c02-140">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="57c02-141">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="57c02-141">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="57c02-142">Bezeichnet eine Reihe von E-Mail-Adressen, an die Antworten gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="57c02-142">Identifies an array of e-mail addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="57c02-143">Absender</span><span class="sxs-lookup"><span data-stu-id="57c02-143">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="57c02-144">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="57c02-144">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="57c02-145">Von</span><span class="sxs-lookup"><span data-stu-id="57c02-145">From</span></span>](from.md) <br/> |<span data-ttu-id="57c02-146">Stellt den Adressat dar, der die Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="57c02-146">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="57c02-147">Organisator</span><span class="sxs-lookup"><span data-stu-id="57c02-147">Organizer</span></span>](organizer.md) <br/> |<span data-ttu-id="57c02-148">Stellt den Organisator einer Besprechung dar.</span><span class="sxs-lookup"><span data-stu-id="57c02-148">Represents the organizer of a meeting.</span></span>  <br/> |
|[<span data-ttu-id="57c02-149">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="57c02-149">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> | <span data-ttu-id="57c02-150">Bezeichnet die standarmäßigen Microsoft Exchange Server 2007-Ordner.</span><span class="sxs-lookup"><span data-stu-id="57c02-150">Identifies default Microsoft Exchange Server 2007 folders.</span></span>  <br/><br/>  <span data-ttu-id="57c02-151">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="57c02-151">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/CreateItem/ParentFolderId/DistinguishedFolderId` <br/>  `/CreateFolder/ParentFolderId/DistinguishedFolderId` <br/> |
|[<span data-ttu-id="57c02-152">Lösung</span><span class="sxs-lookup"><span data-stu-id="57c02-152">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="57c02-153">Enthält eine einzelne aufgelöste Entität.</span><span class="sxs-lookup"><span data-stu-id="57c02-153">Contains a single resolved entity.</span></span>  <br/> |
|[<span data-ttu-id="57c02-154">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="57c02-154">DLExpansion</span></span>](dlexpansion.md) <br/> |<span data-ttu-id="57c02-155">Enthält eine Reihe von Postfächern, die in einer Verteilerliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="57c02-155">Contains an array of mailboxes that are contained in a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="57c02-156">Attendee</span><span class="sxs-lookup"><span data-stu-id="57c02-156">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="57c02-157">Stellt Teilnehmer und Ressourcen für ein Kalenderelement dar.</span><span class="sxs-lookup"><span data-stu-id="57c02-157">Represents attendees and resources for a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="57c02-158">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="57c02-158">CreateManagedFolder</span></span>](createmanagedfolder.md) <br/> |<span data-ttu-id="57c02-159">Definiert eine Anforderung zum Hinzufügen verwalteter Ordner für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="57c02-159">Defines a request to add managed folders to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="57c02-160">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="57c02-160">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="57c02-161">Definiert eine Anforderung zum Hinzufügen von Stellvertretern für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="57c02-161">Defines a request to add delegates to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="57c02-162">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="57c02-162">GetDelegate</span></span>](getdelegate.md) <br/> |<span data-ttu-id="57c02-163">Definiert eine Anforderung zum Abrufen von Informationen zu Stellvertretern für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="57c02-163">Defines a request to get information about delegates to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="57c02-164">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="57c02-164">RemoveDelegate</span></span>](removedelegate.md) <br/> |<span data-ttu-id="57c02-165">Definiert eine Anforderung zum Entfernen von Stellvertretern aus einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="57c02-165">Defines a request to remove delegates from a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="57c02-166">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="57c02-166">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="57c02-167">Definiert eine Anforderung zum Aktualisieren von Stellvertretern in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="57c02-167">Defines a request to update delegates in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="57c02-168">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="57c02-168">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="57c02-169">Erläutert den Stellvertreter anhand eines Stellvertreterzugriffsszenarios.</span><span class="sxs-lookup"><span data-stu-id="57c02-169">Describes the delegate in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="57c02-170">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="57c02-170">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="57c02-171">Erläutert den Prinzipal anhand eines Stellvertreterzugriffsszenarios.</span><span class="sxs-lookup"><span data-stu-id="57c02-171">Describes the principal in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="57c02-172">Member</span><span class="sxs-lookup"><span data-stu-id="57c02-172">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="57c02-173">Stellt ein Element einer Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="57c02-173">Represents a member of a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="57c02-174">Textwert</span><span class="sxs-lookup"><span data-stu-id="57c02-174">Text value</span></span>

<span data-ttu-id="57c02-175">Keine.</span><span class="sxs-lookup"><span data-stu-id="57c02-175">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57c02-176">Hinweise</span><span class="sxs-lookup"><span data-stu-id="57c02-176">Remarks</span></span>

<span data-ttu-id="57c02-177">Das [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)- und [ItemId](itemid.md)-Element bezeichnen ein Postfach oder eine Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="57c02-177">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) and [ItemId](itemid.md) elements identify a mailbox or distribution list.</span></span> 

<span data-ttu-id="57c02-178">Das [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)-Element bezeichnet ein Postfach oder eine Verteilerliste anhand der SMTP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="57c02-178">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element identifies a mailbox or distribution list by SMTP address.</span></span> 

<span data-ttu-id="57c02-179">Das [ItemId](itemid.md)-Element bezeichnet ein Postfach anhand eines Elementbezeichners, der einem bestimmten Postfach zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="57c02-179">The [ItemId](itemid.md) element identifies a mailbox by an item identifier, which is associated with a particular mailbox.</span></span> 

<span data-ttu-id="57c02-180">Das [ItemId](itemid.md)-Element kann nicht zum Senden einer Nachricht an eine Verteilerliste oder einen Kontakt in einem öffentlichen Kontaktordner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57c02-180">The [ItemId](itemid.md) element cannot be used for sending a message to a distribution list or a contact in a public contacts folder.</span></span> <span data-ttu-id="57c02-181">Wenn es in einem CreateItem-, UpdateItem- oder SendItem-Vorgang verwendet wird, wird beim Versuch eine Nachricht an eine Verteilerliste oder einen öffentlichen Kontaktordner zu senden ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="57c02-181">An error will be thrown if this is used in a CreateItem, UpdateItem, or SendItem operation when an attempt is made to send a message to a distribution list or contact in a contacts public folder.</span></span> <span data-ttu-id="57c02-182">Verwenden Sie zum Abrufen der SMTP-Adresse den ExpandDL-Vorgang und senden Sie die Nachricht anschließend mit dem [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)-Element, statt das [ItemId](itemid.md)-Element zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="57c02-182">Use the ExpandDL operation to get the SMTP address and then send the message by using the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element instead of the [ItemId](itemid.md) element.</span></span> 
  
<span data-ttu-id="57c02-183">Ein anderes Element, [Postfach (Verfügbarkeit)](mailbox-availability.md), stellt Informationen zu Verfügbarkeitsvorgängen bereit.</span><span class="sxs-lookup"><span data-stu-id="57c02-183">Another element, [Mailbox (Availability)](mailbox-availability.md), provides information for availability operations.</span></span> 
  
<span data-ttu-id="57c02-184">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="57c02-184">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57c02-185">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="57c02-185">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57c02-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="57c02-186">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="57c02-187">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="57c02-187">Schema Name</span></span>  <br/> |<span data-ttu-id="57c02-188">Schematypen</span><span class="sxs-lookup"><span data-stu-id="57c02-188">Types schema</span></span>  <br/> |
|<span data-ttu-id="57c02-189">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="57c02-189">Validation File</span></span>  <br/> |<span data-ttu-id="57c02-190">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="57c02-190">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="57c02-191">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="57c02-191">Can be Empty</span></span>  <br/> |<span data-ttu-id="57c02-192">False</span><span class="sxs-lookup"><span data-stu-id="57c02-192">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57c02-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57c02-193">See also</span></span>

- [<span data-ttu-id="57c02-194">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="57c02-194">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

