---
title: Absender (e-mailemailtype)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Sender
api_type:
- schema
ms.assetid: 717eb6d0-d167-4b20-92e2-5d08b96186c4
description: Das Sender-Element stellt die e-Mail-Adresse des Absenders der Nachricht dar.
ms.openlocfilehash: 23a487f216a110796d40f3d3e86224c691acc004
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455324"
---
# <a name="sender-emailaddresstype"></a><span data-ttu-id="28a53-103">Absender (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="28a53-103">Sender (EmailAddressType)</span></span>

<span data-ttu-id="28a53-104">Das **Sender** -Element stellt die e-Mail-Adresse des Absenders der Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="28a53-104">The **Sender** element represents the e-mail address for the sender of the message.</span></span> 
  
```XML
<Sender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Sender>
```

 <span data-ttu-id="28a53-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="28a53-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28a53-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="28a53-106">Attributes and elements</span></span>

<span data-ttu-id="28a53-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="28a53-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28a53-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="28a53-108">Attributes</span></span>

<span data-ttu-id="28a53-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="28a53-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28a53-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28a53-110">Child elements</span></span>

|<span data-ttu-id="28a53-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="28a53-111">**Element**</span></span>|<span data-ttu-id="28a53-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28a53-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28a53-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="28a53-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="28a53-114">Stellt den Namen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="28a53-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="28a53-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="28a53-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="28a53-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="28a53-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="28a53-117">Definiert die primäre Simple Mail Transfer Protocol (SMTP) Adresse eines Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="28a53-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="28a53-118">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="28a53-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="28a53-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="28a53-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="28a53-120">Stellt das Routingprotokoll für den Empfänger dar.</span><span class="sxs-lookup"><span data-stu-id="28a53-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="28a53-121">Der Standardwert ist SMTP.</span><span class="sxs-lookup"><span data-stu-id="28a53-121">The default value is SMTP.</span></span> <span data-ttu-id="28a53-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="28a53-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="28a53-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="28a53-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="28a53-124">Stellt den Typ des Postfachs dar, der durch die e-Mail-Adresse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="28a53-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="28a53-125">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="28a53-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="28a53-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="28a53-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="28a53-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="28a53-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="28a53-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28a53-129">Parent elements</span></span>

|<span data-ttu-id="28a53-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="28a53-130">**Element**</span></span>|<span data-ttu-id="28a53-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28a53-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28a53-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="28a53-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="28a53-133">Gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="28a53-133">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="28a53-134">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="28a53-134">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="28a53-135">Enthält ein einzelnes Nachrichten Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="28a53-135">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
|[<span data-ttu-id="28a53-136">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="28a53-136">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="28a53-137">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="28a53-137">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="28a53-138">Textwert</span><span class="sxs-lookup"><span data-stu-id="28a53-138">Text value</span></span>

<span data-ttu-id="28a53-139">Keine.</span><span class="sxs-lookup"><span data-stu-id="28a53-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28a53-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28a53-140">Remarks</span></span>

<span data-ttu-id="28a53-141">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="28a53-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28a53-142">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="28a53-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28a53-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="28a53-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="28a53-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="28a53-144">Schema Name</span></span>  <br/> |<span data-ttu-id="28a53-145">Schematypen</span><span class="sxs-lookup"><span data-stu-id="28a53-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="28a53-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="28a53-146">Validation File</span></span>  <br/> |<span data-ttu-id="28a53-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="28a53-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="28a53-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="28a53-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="28a53-149">False</span><span class="sxs-lookup"><span data-stu-id="28a53-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28a53-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28a53-150">See also</span></span>



[<span data-ttu-id="28a53-151">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="28a53-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="28a53-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="28a53-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

