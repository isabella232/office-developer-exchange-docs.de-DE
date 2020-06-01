---
title: Adresse (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Address
api_type:
- schema
ms.assetid: 518641c8-7f6f-496c-86f9-341e7c1bb44c
description: Das Address-Element stellt eine vollständig aufgelöste e-Mail-Adresse dar.
ms.openlocfilehash: 591bc675165ec80f69407bd8ee19d16c9ddff15a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464903"
---
# <a name="address-emailaddresstype"></a><span data-ttu-id="3fd86-103">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="3fd86-103">Address (EmailAddressType)</span></span>

<span data-ttu-id="3fd86-104">Das **Address** -Element stellt eine vollständig aufgelöste e-Mail-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="3fd86-104">The **Address** element represents a fully resolved e-mail address.</span></span> 
  
```XML
<Address>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Address >
```

 <span data-ttu-id="3fd86-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="3fd86-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3fd86-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3fd86-106">Attributes and elements</span></span>

<span data-ttu-id="3fd86-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3fd86-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3fd86-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3fd86-108">Attributes</span></span>

<span data-ttu-id="3fd86-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3fd86-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3fd86-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3fd86-110">Child elements</span></span>

|<span data-ttu-id="3fd86-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3fd86-111">**Element**</span></span>|<span data-ttu-id="3fd86-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3fd86-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3fd86-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="3fd86-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="3fd86-p101">Definiert den Namen des Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3fd86-p101">Defines the name of the mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3fd86-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="3fd86-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="3fd86-p102">Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3fd86-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3fd86-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="3fd86-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="3fd86-p103">Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3fd86-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3fd86-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="3fd86-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="3fd86-p104">Definiert den Postfachtyp eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3fd86-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3fd86-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="3fd86-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="3fd86-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3fd86-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3fd86-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3fd86-129">Parent elements</span></span>

|<span data-ttu-id="3fd86-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="3fd86-130">**Element**</span></span>|<span data-ttu-id="3fd86-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3fd86-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3fd86-132">Element originalrecipients</span><span class="sxs-lookup"><span data-stu-id="3fd86-132">OriginalRecipients</span></span>](originalrecipients.md) <br/> |<span data-ttu-id="3fd86-133">Enthält eine Auflistung von e-Mail-Adressen, die die ursprünglichen Empfänger einer nachverfolgten Nachricht darstellen.</span><span class="sxs-lookup"><span data-stu-id="3fd86-133">Contains a collection of e-mail addresses that represent the original recipients of a tracked message.</span></span>  <br/> |
|[<span data-ttu-id="3fd86-134">RoomLists</span><span class="sxs-lookup"><span data-stu-id="3fd86-134">RoomLists</span></span>](roomlists.md) <br/> |<span data-ttu-id="3fd86-135">Enthält eine Liste der Besprechungsräume in einer Organisation.</span><span class="sxs-lookup"><span data-stu-id="3fd86-135">Contains a list of meeting rooms in an organization.</span></span>  <br/> |
|[<span data-ttu-id="3fd86-136">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="3fd86-136">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="3fd86-137">Enthält eine Liste der e-Mail-Adressen, an die eingehende Nachrichten gesendet werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="3fd86-137">Contains a list of e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3fd86-138">Textwert</span><span class="sxs-lookup"><span data-stu-id="3fd86-138">Text value</span></span>

<span data-ttu-id="3fd86-139">Keine.</span><span class="sxs-lookup"><span data-stu-id="3fd86-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3fd86-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fd86-140">Remarks</span></span>

<span data-ttu-id="3fd86-141">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3fd86-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3fd86-142">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3fd86-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fd86-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="3fd86-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3fd86-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3fd86-144">Schema Name</span></span>  <br/> |<span data-ttu-id="3fd86-145">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3fd86-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="3fd86-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3fd86-146">Validation File</span></span>  <br/> |<span data-ttu-id="3fd86-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3fd86-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3fd86-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3fd86-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="3fd86-149">False</span><span class="sxs-lookup"><span data-stu-id="3fd86-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3fd86-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fd86-150">See also</span></span>

- [<span data-ttu-id="3fd86-151">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3fd86-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md) 
- [<span data-ttu-id="3fd86-152">GetRoomLists-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3fd86-152">GetRoomLists operation</span></span>](getroomlists-operation.md)
- [<span data-ttu-id="3fd86-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3fd86-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

