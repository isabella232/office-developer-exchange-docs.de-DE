---
title: FederatedDeliveryMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FederatedDeliveryMailbox
api_type:
- schema
ms.assetid: cd56bcc0-d24a-4e8b-87bd-999bf69234b7
description: Das FederatedDeliveryMailbox -Element darstellt, das Postfach, das eine lokale Cross-Nachricht gesendet wurde.
ms.openlocfilehash: 4a9250455f8de3ede25f2b5ba9433690137ca1d3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758409"
---
# <a name="federateddeliverymailbox"></a><span data-ttu-id="49bbf-103">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="49bbf-103">FederatedDeliveryMailbox</span></span>

<span data-ttu-id="49bbf-104">Das **FederatedDeliveryMailbox** -Element darstellt, das Postfach, das eine lokale Cross-Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="49bbf-104">The **FederatedDeliveryMailbox** element represents the mailbox to which a cross-premise message was sent.</span></span> 
  
```XML
<FederatedDeliveryMailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</FederatedDeliveryMailbox>
```

 <span data-ttu-id="49bbf-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="49bbf-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="49bbf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="49bbf-106">Attributes and elements</span></span>

<span data-ttu-id="49bbf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="49bbf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49bbf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="49bbf-108">Attributes</span></span>

<span data-ttu-id="49bbf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="49bbf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49bbf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="49bbf-110">Child elements</span></span>

|<span data-ttu-id="49bbf-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="49bbf-111">**Element**</span></span>|<span data-ttu-id="49bbf-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="49bbf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49bbf-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="49bbf-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="49bbf-p101">Definiert den Namen des Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="49bbf-p101">Defines the name of the mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="49bbf-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="49bbf-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="49bbf-p102">Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="49bbf-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="49bbf-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="49bbf-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="49bbf-p103">Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="49bbf-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="49bbf-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="49bbf-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="49bbf-p104">Definiert den Postfachtyp eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="49bbf-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="49bbf-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="49bbf-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="49bbf-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="49bbf-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="49bbf-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="49bbf-129">Parent elements</span></span>

|<span data-ttu-id="49bbf-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="49bbf-130">**Element**</span></span>|<span data-ttu-id="49bbf-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="49bbf-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49bbf-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="49bbf-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="49bbf-133">Enthält die Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="49bbf-133">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="49bbf-134">Textwert</span><span class="sxs-lookup"><span data-stu-id="49bbf-134">Text value</span></span>

<span data-ttu-id="49bbf-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="49bbf-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="49bbf-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="49bbf-136">Remarks</span></span>

<span data-ttu-id="49bbf-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="49bbf-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49bbf-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="49bbf-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49bbf-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="49bbf-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="49bbf-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="49bbf-140">Schema Name</span></span>  <br/> |<span data-ttu-id="49bbf-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="49bbf-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="49bbf-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="49bbf-142">Validation File</span></span>  <br/> |<span data-ttu-id="49bbf-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="49bbf-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="49bbf-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="49bbf-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="49bbf-145">False</span><span class="sxs-lookup"><span data-stu-id="49bbf-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49bbf-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49bbf-146">See also</span></span>



- [<span data-ttu-id="49bbf-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="49bbf-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

