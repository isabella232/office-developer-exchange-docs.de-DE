---
title: Recipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recipient
api_type:
- schema
ms.assetid: 52adbb30-3bfd-48aa-9ea8-9f7d3b4bee44
description: Das Recipient-Element darstellt, den Empfänger für den das Ereignis aufgetreten ist.
ms.openlocfilehash: e8e8f9d6031d27c7441017c85eb26a143258b183
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830971"
---
# <a name="recipient"></a><span data-ttu-id="31e33-103">Recipient</span><span class="sxs-lookup"><span data-stu-id="31e33-103">Recipient</span></span>

<span data-ttu-id="31e33-104">Das **Recipient** -Element darstellt, den Empfänger für den das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="31e33-104">The **Recipient** element represents the recipient for whom the event occurred.</span></span> 
  
```XML
<Recipient>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Recipient>
```

 <span data-ttu-id="31e33-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="31e33-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31e33-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="31e33-106">Attributes and elements</span></span>

<span data-ttu-id="31e33-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="31e33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31e33-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="31e33-108">Attributes</span></span>

<span data-ttu-id="31e33-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="31e33-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31e33-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31e33-110">Child elements</span></span>

|<span data-ttu-id="31e33-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="31e33-111">**Element**</span></span>|<span data-ttu-id="31e33-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31e33-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31e33-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="31e33-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="31e33-114">Stellt den Namen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="31e33-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="31e33-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="31e33-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="31e33-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="31e33-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="31e33-117">Definiert die primäre Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="31e33-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="31e33-118">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="31e33-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="31e33-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="31e33-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="31e33-120">Definiert die Weiterleitung, die für das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31e33-120">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="31e33-121">Der Standardwert ist SMTP.</span><span class="sxs-lookup"><span data-stu-id="31e33-121">The default value is SMTP.</span></span> <span data-ttu-id="31e33-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="31e33-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="31e33-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="31e33-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="31e33-124">Stellt den Typ des Postfachs an, das die e-Mail-Adresse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="31e33-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="31e33-125">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="31e33-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="31e33-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="31e33-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="31e33-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="31e33-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="31e33-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31e33-129">Parent elements</span></span>

|<span data-ttu-id="31e33-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="31e33-130">**Element**</span></span>|<span data-ttu-id="31e33-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31e33-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31e33-132">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="31e33-132">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="31e33-133">Enthält Informationen für ein einzelnes Ereignis für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="31e33-133">Contains information for a single event for a recipient.</span></span>  <br/> |
|[<span data-ttu-id="31e33-134">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="31e33-134">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="31e33-135">Gibt Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="31e33-135">Specifies criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="31e33-136">Textwert</span><span class="sxs-lookup"><span data-stu-id="31e33-136">Text value</span></span>

<span data-ttu-id="31e33-137">Keine.</span><span class="sxs-lookup"><span data-stu-id="31e33-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31e33-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31e33-138">Remarks</span></span>

<span data-ttu-id="31e33-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="31e33-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31e33-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="31e33-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31e33-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="31e33-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31e33-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="31e33-142">Schema Name</span></span>  <br/> |<span data-ttu-id="31e33-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="31e33-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="31e33-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="31e33-144">Validation File</span></span>  <br/> |<span data-ttu-id="31e33-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="31e33-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="31e33-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="31e33-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="31e33-147">False</span><span class="sxs-lookup"><span data-stu-id="31e33-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31e33-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31e33-148">See also</span></span>



- [<span data-ttu-id="31e33-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="31e33-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

