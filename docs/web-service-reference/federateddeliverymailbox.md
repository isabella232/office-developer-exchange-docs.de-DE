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
ms.openlocfilehash: d493ed81e82237b7257e8c469f4552d931b73aa6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461947"
---
# <a name="federateddeliverymailbox"></a><span data-ttu-id="0526b-103">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="0526b-103">FederatedDeliveryMailbox</span></span>

<span data-ttu-id="0526b-104">Das **FederatedDeliveryMailbox** -Element darstellt, das Postfach, das eine lokale Cross-Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0526b-104">The **FederatedDeliveryMailbox** element represents the mailbox to which a cross-premise message was sent.</span></span> 
  
```XML
<FederatedDeliveryMailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</FederatedDeliveryMailbox>
```

 <span data-ttu-id="0526b-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="0526b-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0526b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0526b-106">Attributes and elements</span></span>

<span data-ttu-id="0526b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0526b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0526b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0526b-108">Attributes</span></span>

<span data-ttu-id="0526b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0526b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0526b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0526b-110">Child elements</span></span>

|<span data-ttu-id="0526b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0526b-111">**Element**</span></span>|<span data-ttu-id="0526b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0526b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0526b-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="0526b-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="0526b-p101">Definiert den Namen des Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="0526b-p101">Defines the name of the mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0526b-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="0526b-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="0526b-p102">Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="0526b-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0526b-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="0526b-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="0526b-p103">Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="0526b-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0526b-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="0526b-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="0526b-p104">Definiert den Postfachtyp eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="0526b-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0526b-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="0526b-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="0526b-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="0526b-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0526b-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0526b-129">Parent elements</span></span>

|<span data-ttu-id="0526b-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="0526b-130">**Element**</span></span>|<span data-ttu-id="0526b-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0526b-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0526b-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="0526b-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="0526b-133">Enthält die Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="0526b-133">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0526b-134">Textwert</span><span class="sxs-lookup"><span data-stu-id="0526b-134">Text value</span></span>

<span data-ttu-id="0526b-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="0526b-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0526b-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0526b-136">Remarks</span></span>

<span data-ttu-id="0526b-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0526b-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0526b-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0526b-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0526b-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="0526b-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0526b-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0526b-140">Schema Name</span></span>  <br/> |<span data-ttu-id="0526b-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0526b-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0526b-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0526b-142">Validation File</span></span>  <br/> |<span data-ttu-id="0526b-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0526b-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0526b-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0526b-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="0526b-145">False</span><span class="sxs-lookup"><span data-stu-id="0526b-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0526b-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0526b-146">See also</span></span>



- [<span data-ttu-id="0526b-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0526b-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

