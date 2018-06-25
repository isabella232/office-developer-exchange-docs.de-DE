---
title: Absender (EmailAddressType)
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
description: Das Absender-Element stellt die E-mail-Adresse für den Absender der Nachricht.
ms.openlocfilehash: bac62412caf1044c13015f1d9d7ef63552747c1c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831320"
---
# <a name="sender-emailaddresstype"></a><span data-ttu-id="21a3f-103">Absender (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="21a3f-103">Sender (EmailAddressType)</span></span>

<span data-ttu-id="21a3f-104">Das **Absender** -Element stellt die E-mail-Adresse für den Absender der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="21a3f-104">The **Sender** element represents the e-mail address for the sender of the message.</span></span> 
  
```XML
<Sender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Sender>
```

 <span data-ttu-id="21a3f-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="21a3f-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21a3f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="21a3f-106">Attributes and elements</span></span>

<span data-ttu-id="21a3f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="21a3f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21a3f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="21a3f-108">Attributes</span></span>

<span data-ttu-id="21a3f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="21a3f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21a3f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21a3f-110">Child elements</span></span>

|<span data-ttu-id="21a3f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="21a3f-111">**Element**</span></span>|<span data-ttu-id="21a3f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21a3f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21a3f-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="21a3f-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="21a3f-114">Stellt den Namen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="21a3f-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="21a3f-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="21a3f-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="21a3f-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="21a3f-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="21a3f-117">Definiert die primäre Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="21a3f-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="21a3f-118">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="21a3f-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="21a3f-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="21a3f-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="21a3f-120">Stellt das routing-Protokoll für den Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="21a3f-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="21a3f-121">Der Standardwert ist SMTP.</span><span class="sxs-lookup"><span data-stu-id="21a3f-121">The default value is SMTP.</span></span> <span data-ttu-id="21a3f-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="21a3f-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="21a3f-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="21a3f-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="21a3f-124">Stellt den Typ des Postfachs an, das die e-Mail-Adresse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="21a3f-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="21a3f-125">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="21a3f-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="21a3f-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="21a3f-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="21a3f-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="21a3f-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="21a3f-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21a3f-129">Parent elements</span></span>

|<span data-ttu-id="21a3f-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="21a3f-130">**Element**</span></span>|<span data-ttu-id="21a3f-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21a3f-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21a3f-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="21a3f-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="21a3f-133">Gibt Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="21a3f-133">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="21a3f-134">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="21a3f-134">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="21a3f-135">Ein einzelnes Nachricht Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element enthält.</span><span class="sxs-lookup"><span data-stu-id="21a3f-135">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
|[<span data-ttu-id="21a3f-136">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="21a3f-136">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="21a3f-137">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="21a3f-137">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="21a3f-138">Textwert</span><span class="sxs-lookup"><span data-stu-id="21a3f-138">Text value</span></span>

<span data-ttu-id="21a3f-139">Keine.</span><span class="sxs-lookup"><span data-stu-id="21a3f-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21a3f-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="21a3f-140">Remarks</span></span>

<span data-ttu-id="21a3f-141">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="21a3f-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21a3f-142">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="21a3f-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21a3f-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="21a3f-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21a3f-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="21a3f-144">Schema Name</span></span>  <br/> |<span data-ttu-id="21a3f-145">Schematypen</span><span class="sxs-lookup"><span data-stu-id="21a3f-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="21a3f-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="21a3f-146">Validation File</span></span>  <br/> |<span data-ttu-id="21a3f-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21a3f-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21a3f-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="21a3f-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="21a3f-149">False</span><span class="sxs-lookup"><span data-stu-id="21a3f-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21a3f-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21a3f-150">See also</span></span>



[<span data-ttu-id="21a3f-151">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="21a3f-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="21a3f-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="21a3f-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

