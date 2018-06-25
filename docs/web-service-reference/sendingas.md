---
title: SendingAs
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
description: Das SendingAs-Element darstellt, eine e-Mail-Adresse, der ein Benutzer versucht, als zu senden.
ms.openlocfilehash: a5468ddb8facf99038d319252f7e1c780a888ca1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831338"
---
# <a name="sendingas"></a><span data-ttu-id="5c420-103">SendingAs</span><span class="sxs-lookup"><span data-stu-id="5c420-103">SendingAs</span></span>

<span data-ttu-id="5c420-104">Das **SendingAs** -Element darstellt, eine e-Mail-Adresse, der ein Benutzer versucht, als zu senden.</span><span class="sxs-lookup"><span data-stu-id="5c420-104">The **SendingAs** element represents an e-mail address that a user is trying to send as.</span></span> 
  
```XML
<SendingAs>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</SendingAs>
```

 <span data-ttu-id="5c420-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="5c420-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c420-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5c420-106">Attributes and elements</span></span>

<span data-ttu-id="5c420-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5c420-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c420-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5c420-108">Attributes</span></span>

<span data-ttu-id="5c420-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5c420-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c420-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c420-110">Child elements</span></span>

|<span data-ttu-id="5c420-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c420-111">**Element**</span></span>|<span data-ttu-id="5c420-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c420-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c420-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="5c420-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="5c420-114">Stellt den Namen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="5c420-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="5c420-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="5c420-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="5c420-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="5c420-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="5c420-117">Definiert die primäre Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="5c420-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="5c420-118">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="5c420-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="5c420-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="5c420-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="5c420-120">Definiert den Adresstyp für das Postfach an.</span><span class="sxs-lookup"><span data-stu-id="5c420-120">Defines the address type for the mailbox.</span></span> <span data-ttu-id="5c420-121">Der Standard lautet SMTP.</span><span class="sxs-lookup"><span data-stu-id="5c420-121">The default is SMTP.</span></span> <span data-ttu-id="5c420-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="5c420-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="5c420-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="5c420-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="5c420-124">Stellt den Typ des Postfachs an, die von einem e-Mail-Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5c420-124">Represents the type of mailbox that is represented by an e-mail user.</span></span> <span data-ttu-id="5c420-125">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="5c420-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="5c420-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="5c420-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="5c420-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="5c420-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5c420-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c420-129">Parent elements</span></span>

|<span data-ttu-id="5c420-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c420-130">**Element**</span></span>|<span data-ttu-id="5c420-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c420-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c420-132">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="5c420-132">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="5c420-133">Enthält die Empfänger und Typen von e-Mail-Infos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5c420-133">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5c420-134">Textwert</span><span class="sxs-lookup"><span data-stu-id="5c420-134">Text value</span></span>

<span data-ttu-id="5c420-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="5c420-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c420-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5c420-136">Remarks</span></span>

<span data-ttu-id="5c420-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5c420-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c420-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5c420-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c420-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c420-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5c420-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5c420-140">Schema Name</span></span>  <br/> |<span data-ttu-id="5c420-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5c420-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5c420-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5c420-142">Validation File</span></span>  <br/> |<span data-ttu-id="5c420-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5c420-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5c420-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5c420-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c420-145">False</span><span class="sxs-lookup"><span data-stu-id="5c420-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c420-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c420-146">See also</span></span>



- [<span data-ttu-id="5c420-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5c420-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

