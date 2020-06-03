---
title: Absender
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendingAs
api_type:
- schema
ms.assetid: b43ce19f-9ab0-4946-acb2-c5aafead9d35
description: Das Sendings-Element stellt eine e-Mail-Adresse dar, die ein Benutzer zu senden versucht.
ms.openlocfilehash: cd11bd60cbbe3434fcc1b0b9a1cfe0de9f0b1e21
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462136"
---
# <a name="sendingas"></a><span data-ttu-id="fb182-103">Absender</span><span class="sxs-lookup"><span data-stu-id="fb182-103">SendingAs</span></span>

<span data-ttu-id="fb182-104">Das **Sendings** -Element stellt eine e-Mail-Adresse dar, die ein Benutzer zu senden versucht.</span><span class="sxs-lookup"><span data-stu-id="fb182-104">The **SendingAs** element represents an e-mail address that a user is trying to send as.</span></span> 
  
```XML
<SendingAs>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</SendingAs>
```

 <span data-ttu-id="fb182-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="fb182-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fb182-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fb182-106">Attributes and elements</span></span>

<span data-ttu-id="fb182-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fb182-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb182-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fb182-108">Attributes</span></span>

<span data-ttu-id="fb182-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fb182-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fb182-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb182-110">Child elements</span></span>

|<span data-ttu-id="fb182-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="fb182-111">**Element**</span></span>|<span data-ttu-id="fb182-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb182-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb182-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="fb182-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="fb182-114">Stellt den Namen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="fb182-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="fb182-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb182-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="fb182-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="fb182-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="fb182-117">Definiert die primäre Simple Mail Transfer Protocol (SMTP) Adresse eines Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="fb182-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="fb182-118">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb182-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="fb182-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="fb182-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="fb182-120">Definiert den Adresstyp für das Postfach.</span><span class="sxs-lookup"><span data-stu-id="fb182-120">Defines the address type for the mailbox.</span></span> <span data-ttu-id="fb182-121">Der Standard lautet SMTP.</span><span class="sxs-lookup"><span data-stu-id="fb182-121">The default is SMTP.</span></span> <span data-ttu-id="fb182-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb182-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="fb182-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="fb182-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="fb182-124">Stellt den Typ des Postfachs dar, der von einem e-Mail-Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fb182-124">Represents the type of mailbox that is represented by an e-mail user.</span></span> <span data-ttu-id="fb182-125">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb182-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="fb182-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="fb182-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="fb182-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb182-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fb182-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb182-129">Parent elements</span></span>

|<span data-ttu-id="fb182-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="fb182-130">**Element**</span></span>|<span data-ttu-id="fb182-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb182-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb182-132">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="fb182-132">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="fb182-133">Enthält die Empfänger und Typen von e-Mail-Tipps, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fb182-133">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fb182-134">Textwert</span><span class="sxs-lookup"><span data-stu-id="fb182-134">Text value</span></span>

<span data-ttu-id="fb182-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="fb182-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb182-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb182-136">Remarks</span></span>

<span data-ttu-id="fb182-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fb182-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fb182-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fb182-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb182-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb182-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fb182-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fb182-140">Schema Name</span></span>  <br/> |<span data-ttu-id="fb182-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fb182-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fb182-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fb182-142">Validation File</span></span>  <br/> |<span data-ttu-id="fb182-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fb182-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fb182-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fb182-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="fb182-145">False</span><span class="sxs-lookup"><span data-stu-id="fb182-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fb182-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb182-146">See also</span></span>



- [<span data-ttu-id="fb182-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fb182-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

