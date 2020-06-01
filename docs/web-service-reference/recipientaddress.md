---
title: RecipientAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientAddress
api_type:
- schema
ms.assetid: 9ae6351a-2c60-4715-a489-5681a13641f9
description: Das RecipientAddress-Element stellt das Postfach des Empfängers dar.
ms.openlocfilehash: f4b6edd034dd91471e6496f6b0cca65bd3ffb69a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465849"
---
# <a name="recipientaddress"></a><span data-ttu-id="cd875-103">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="cd875-103">RecipientAddress</span></span>

<span data-ttu-id="cd875-104">Das **RecipientAddress** -Element stellt das Postfach des Empfängers dar.</span><span class="sxs-lookup"><span data-stu-id="cd875-104">The **RecipientAddress** element represents the mailbox of the recipient.</span></span> 
  
```xml
<RecipientAddress>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RecipientAddress>
```

 <span data-ttu-id="cd875-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="cd875-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd875-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cd875-106">Attributes and elements</span></span>

<span data-ttu-id="cd875-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cd875-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd875-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cd875-108">Attributes</span></span>

<span data-ttu-id="cd875-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cd875-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd875-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd875-110">Child elements</span></span>

|<span data-ttu-id="cd875-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd875-111">**Element**</span></span>|<span data-ttu-id="cd875-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd875-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd875-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cd875-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="cd875-114">Stellt den Namen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="cd875-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="cd875-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cd875-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="cd875-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="cd875-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="cd875-p102">Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cd875-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="cd875-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="cd875-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="cd875-120">Stellt das Routingprotokoll für den Empfänger dar.</span><span class="sxs-lookup"><span data-stu-id="cd875-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="cd875-121">Der Standard lautet SMTP.</span><span class="sxs-lookup"><span data-stu-id="cd875-121">The default is SMTP.</span></span> <span data-ttu-id="cd875-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cd875-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="cd875-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="cd875-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="cd875-124">Stellt den Typ des Postfachs dar, der durch die e-Mail-Adresse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cd875-124">Represents the type of mailbox that is represented by the e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="cd875-125">ItemId</span><span class="sxs-lookup"><span data-stu-id="cd875-125">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="cd875-p104">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cd875-p104">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cd875-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd875-128">Parent elements</span></span>

|<span data-ttu-id="cd875-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd875-129">**Element**</span></span>|<span data-ttu-id="cd875-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd875-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd875-131">E-Mail-Info</span><span class="sxs-lookup"><span data-stu-id="cd875-131">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="cd875-132">Stellt Werte für verschiedene Arten von e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="cd875-132">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd875-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd875-133">Remarks</span></span>

<span data-ttu-id="cd875-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="cd875-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd875-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cd875-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd875-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd875-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cd875-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cd875-137">Schema Name</span></span>  <br/> |<span data-ttu-id="cd875-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cd875-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="cd875-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cd875-139">Validation File</span></span>  <br/> |<span data-ttu-id="cd875-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cd875-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cd875-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cd875-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd875-142">False</span><span class="sxs-lookup"><span data-stu-id="cd875-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd875-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd875-143">See also</span></span>



- [<span data-ttu-id="cd875-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cd875-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

