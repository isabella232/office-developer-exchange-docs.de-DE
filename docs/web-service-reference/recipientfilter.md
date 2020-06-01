---
title: RecipientFilter
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientFilter
api_type:
- schema
ms.assetid: 956c287a-a38a-49a7-a877-6d2088dfbc06
description: Das RecipientFilter-Element stellt eine Empfängeradresse dar, die mit dem angegebenen Nachrichtenverfolgungsbericht verwendet werden soll.
ms.openlocfilehash: 945adf9155434e0690debfccc7caf70ba0cb94ec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465807"
---
# <a name="recipientfilter"></a><span data-ttu-id="cd492-103">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="cd492-103">RecipientFilter</span></span>

<span data-ttu-id="cd492-104">Das **RecipientFilter** -Element stellt eine Empfängeradresse dar, die mit dem angegebenen Nachrichtenverfolgungsbericht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd492-104">The **RecipientFilter** element represents a recipient address to use with the specified message tracking report.</span></span> 
  
```XML
 <RecipientFilter>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RecipientFilter>
```

 <span data-ttu-id="cd492-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="cd492-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd492-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cd492-106">Attributes and elements</span></span>

<span data-ttu-id="cd492-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cd492-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd492-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cd492-108">Attributes</span></span>

<span data-ttu-id="cd492-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cd492-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd492-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd492-110">Child elements</span></span>

|<span data-ttu-id="cd492-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd492-111">**Element**</span></span>|<span data-ttu-id="cd492-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd492-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd492-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cd492-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="cd492-114">Stellt den Namen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="cd492-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="cd492-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cd492-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="cd492-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="cd492-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="cd492-117">Definiert die primäre Simple Mail Transfer Protocol (SMTP) Adresse eines Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="cd492-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="cd492-118">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cd492-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="cd492-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="cd492-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="cd492-120">Stellt das Routingprotokoll für diesen Empfänger dar.</span><span class="sxs-lookup"><span data-stu-id="cd492-120">Represents the routing protocol for this recipient.</span></span> <span data-ttu-id="cd492-121">Der Standardwert ist SMTP.</span><span class="sxs-lookup"><span data-stu-id="cd492-121">The default value is SMTP.</span></span> <span data-ttu-id="cd492-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cd492-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="cd492-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="cd492-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="cd492-124">Stellt den Typ des Postfachs dar, der durch die e-Mail-Adresse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cd492-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="cd492-125">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cd492-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="cd492-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="cd492-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="cd492-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cd492-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cd492-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd492-129">Parent elements</span></span>

|<span data-ttu-id="cd492-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd492-130">**Element**</span></span>|<span data-ttu-id="cd492-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd492-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd492-132">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="cd492-132">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="cd492-133">Enthält die Anforderung für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md) zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID.</span><span class="sxs-lookup"><span data-stu-id="cd492-133">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cd492-134">Textwert</span><span class="sxs-lookup"><span data-stu-id="cd492-134">Text value</span></span>

<span data-ttu-id="cd492-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="cd492-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cd492-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd492-136">Remarks</span></span>

<span data-ttu-id="cd492-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="cd492-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd492-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cd492-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd492-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd492-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cd492-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cd492-140">Schema Name</span></span>  <br/> |<span data-ttu-id="cd492-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cd492-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cd492-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cd492-142">Validation File</span></span>  <br/> |<span data-ttu-id="cd492-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cd492-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cd492-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cd492-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd492-145">False</span><span class="sxs-lookup"><span data-stu-id="cd492-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd492-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd492-146">See also</span></span>



[<span data-ttu-id="cd492-147">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cd492-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="cd492-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cd492-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

