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
description: Das PurportedSender-Element enthält Kontaktinformationen für den Absender einer e-Mail-Nachricht.
ms.openlocfilehash: 1e5b74d60d824c06834cf988557ef64fb84d70c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830937"
---
# <a name="purportedsender"></a><span data-ttu-id="a3a74-103">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="a3a74-103">PurportedSender</span></span>

<span data-ttu-id="a3a74-104">Das **PurportedSender** -Element enthält Kontaktinformationen für den Absender einer e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a3a74-104">The **PurportedSender** element contains contact information for the alleged sender of an e-mail message.</span></span> 
  
```XML
<PurportedSender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</PurportedSender>
```

 <span data-ttu-id="a3a74-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="a3a74-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a3a74-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a3a74-106">Attributes and elements</span></span>

<span data-ttu-id="a3a74-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a3a74-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3a74-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a3a74-108">Attributes</span></span>

<span data-ttu-id="a3a74-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a3a74-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a3a74-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3a74-110">Child elements</span></span>

|<span data-ttu-id="a3a74-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3a74-111">**Element**</span></span>|<span data-ttu-id="a3a74-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a3a74-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3a74-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="a3a74-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="a3a74-114">Stellt den Namen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="a3a74-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="a3a74-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a3a74-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a3a74-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="a3a74-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="a3a74-p102">Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a3a74-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a3a74-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="a3a74-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="a3a74-120">Stellt das routing-Protokoll für den Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="a3a74-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="a3a74-121">Der Standardwert ist SMTP.</span><span class="sxs-lookup"><span data-stu-id="a3a74-121">The default value is SMTP.</span></span> <span data-ttu-id="a3a74-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a3a74-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a3a74-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="a3a74-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="a3a74-124">Stellt den Typ des Postfachs an, das die e-Mail-Adresse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a3a74-124">Represents the type of mailbox that is represented by the e-mail address..</span></span> <span data-ttu-id="a3a74-125">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a3a74-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a3a74-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="a3a74-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="a3a74-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a3a74-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a3a74-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3a74-129">Parent elements</span></span>

|<span data-ttu-id="a3a74-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3a74-130">**Element**</span></span>|<span data-ttu-id="a3a74-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a3a74-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3a74-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="a3a74-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="a3a74-133">Gibt Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="a3a74-133">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="a3a74-134">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="a3a74-134">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="a3a74-135">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a3a74-135">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a3a74-136">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="a3a74-136">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="a3a74-137">Ein einzelnes Nachricht Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element enthält.</span><span class="sxs-lookup"><span data-stu-id="a3a74-137">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a3a74-138">Textwert</span><span class="sxs-lookup"><span data-stu-id="a3a74-138">Text value</span></span>

<span data-ttu-id="a3a74-139">Keine.</span><span class="sxs-lookup"><span data-stu-id="a3a74-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3a74-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a3a74-140">Remarks</span></span>

<span data-ttu-id="a3a74-141">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a3a74-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3a74-142">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a3a74-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3a74-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3a74-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a3a74-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a3a74-144">Schema Name</span></span>  <br/> |<span data-ttu-id="a3a74-145">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a3a74-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a3a74-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a3a74-146">Validation File</span></span>  <br/> |<span data-ttu-id="a3a74-147">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a3a74-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a3a74-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a3a74-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="a3a74-149">False</span><span class="sxs-lookup"><span data-stu-id="a3a74-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3a74-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3a74-150">See also</span></span>



[<span data-ttu-id="a3a74-151">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a3a74-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="a3a74-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a3a74-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

