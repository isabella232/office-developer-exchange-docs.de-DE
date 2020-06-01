---
title: PurportedSender
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PurportedSender
api_type:
- schema
ms.assetid: eb7a54ec-2e48-4030-bbcf-50a31609691b
description: Das PurportedSender-Element enthält Kontaktinformationen für den mutmaßlichen Absender einer e-Mail-Nachricht.
ms.openlocfilehash: 5ecf352484a423e3955736620bf5a65c4e98099a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468334"
---
# <a name="purportedsender"></a><span data-ttu-id="68bf1-103">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="68bf1-103">PurportedSender</span></span>

<span data-ttu-id="68bf1-104">Das **PurportedSender** -Element enthält Kontaktinformationen für den mutmaßlichen Absender einer e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="68bf1-104">The **PurportedSender** element contains contact information for the alleged sender of an e-mail message.</span></span> 
  
```XML
<PurportedSender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</PurportedSender>
```

 <span data-ttu-id="68bf1-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="68bf1-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="68bf1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="68bf1-106">Attributes and elements</span></span>

<span data-ttu-id="68bf1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="68bf1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68bf1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="68bf1-108">Attributes</span></span>

<span data-ttu-id="68bf1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="68bf1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="68bf1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68bf1-110">Child elements</span></span>

|<span data-ttu-id="68bf1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="68bf1-111">**Element**</span></span>|<span data-ttu-id="68bf1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68bf1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68bf1-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="68bf1-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="68bf1-114">Stellt den Namen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="68bf1-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="68bf1-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="68bf1-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="68bf1-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="68bf1-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="68bf1-p102">Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="68bf1-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="68bf1-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="68bf1-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="68bf1-120">Stellt das Routingprotokoll für den Empfänger dar.</span><span class="sxs-lookup"><span data-stu-id="68bf1-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="68bf1-121">Der Standardwert ist SMTP.</span><span class="sxs-lookup"><span data-stu-id="68bf1-121">The default value is SMTP.</span></span> <span data-ttu-id="68bf1-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="68bf1-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="68bf1-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="68bf1-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="68bf1-124">Stellt den Typ des Postfachs dar, der durch die e-Mail-Adresse dargestellt wird..</span><span class="sxs-lookup"><span data-stu-id="68bf1-124">Represents the type of mailbox that is represented by the e-mail address..</span></span> <span data-ttu-id="68bf1-125">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="68bf1-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="68bf1-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="68bf1-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="68bf1-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="68bf1-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="68bf1-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68bf1-129">Parent elements</span></span>

|<span data-ttu-id="68bf1-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="68bf1-130">**Element**</span></span>|<span data-ttu-id="68bf1-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68bf1-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68bf1-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="68bf1-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="68bf1-133">Gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="68bf1-133">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="68bf1-134">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="68bf1-134">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="68bf1-135">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="68bf1-135">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="68bf1-136">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="68bf1-136">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="68bf1-137">Enthält ein einzelnes Nachrichten Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="68bf1-137">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="68bf1-138">Textwert</span><span class="sxs-lookup"><span data-stu-id="68bf1-138">Text value</span></span>

<span data-ttu-id="68bf1-139">Keine.</span><span class="sxs-lookup"><span data-stu-id="68bf1-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="68bf1-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68bf1-140">Remarks</span></span>

<span data-ttu-id="68bf1-141">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="68bf1-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68bf1-142">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="68bf1-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68bf1-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="68bf1-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="68bf1-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="68bf1-144">Schema Name</span></span>  <br/> |<span data-ttu-id="68bf1-145">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="68bf1-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="68bf1-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="68bf1-146">Validation File</span></span>  <br/> |<span data-ttu-id="68bf1-147">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="68bf1-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="68bf1-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="68bf1-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="68bf1-149">False</span><span class="sxs-lookup"><span data-stu-id="68bf1-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68bf1-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68bf1-150">See also</span></span>



[<span data-ttu-id="68bf1-151">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="68bf1-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="68bf1-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="68bf1-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

