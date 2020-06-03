---
title: MailTipsRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsRequested
api_type:
- schema
ms.assetid: 8037bbe5-a37f-4f77-8209-27a94f9095ef
description: Das MailTipsRequested-Element enthält die Typen von e-Mail-Tipps, die vom Dienst angefordert werden.
ms.openlocfilehash: bcb2ebf15e628a04e8507f938d385cf113f2f2a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465898"
---
# <a name="mailtipsrequested"></a><span data-ttu-id="fc77c-103">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="fc77c-103">MailTipsRequested</span></span>

<span data-ttu-id="fc77c-104">Das **MailTipsRequested** -Element enthält die Typen von e-Mail-Tipps, die vom Dienst angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="fc77c-104">The **MailTipsRequested** element contains the types of mail tips requested from the service.</span></span> 
  
```XML
<MailTipsRequested/>
```

 <span data-ttu-id="fc77c-105">**MailTipTypes**</span><span class="sxs-lookup"><span data-stu-id="fc77c-105">**MailTipTypes**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fc77c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fc77c-106">Attributes and elements</span></span>

<span data-ttu-id="fc77c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fc77c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc77c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fc77c-108">Attributes</span></span>

<span data-ttu-id="fc77c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fc77c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc77c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fc77c-110">Child elements</span></span>

<span data-ttu-id="fc77c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fc77c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fc77c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fc77c-112">Parent elements</span></span>

|<span data-ttu-id="fc77c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fc77c-113">**Element**</span></span>|<span data-ttu-id="fc77c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fc77c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc77c-115">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="fc77c-115">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="fc77c-116">Enthält die Empfänger und Typen von e-Mail-Tipps, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc77c-116">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fc77c-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="fc77c-117">Text value</span></span>

<span data-ttu-id="fc77c-118">In der folgenden Tabelle sind die möglichen Werte für das **MailTipsRequested** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc77c-118">The following table lists the possible values for the **MailTipsRequested** element.</span></span> 
  
|<span data-ttu-id="fc77c-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fc77c-119">**Value**</span></span>|<span data-ttu-id="fc77c-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fc77c-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc77c-121">Alle</span><span class="sxs-lookup"><span data-stu-id="fc77c-121">All</span></span>  <br/> |<span data-ttu-id="fc77c-122">Stellt alle verfügbaren e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="fc77c-122">Represents all available mail tips.</span></span>  <br/> |
|<span data-ttu-id="fc77c-123">OutOfOfficeMessage</span><span class="sxs-lookup"><span data-stu-id="fc77c-123">OutOfOfficeMessage</span></span>  <br/> |<span data-ttu-id="fc77c-124">Stellt die Abwesenheit (Out of Office, OOF) Meldung dar.</span><span class="sxs-lookup"><span data-stu-id="fc77c-124">Represents the Out of Office (OOF) message.</span></span>  <br/> |
|<span data-ttu-id="fc77c-125">MailboxFullStatus</span><span class="sxs-lookup"><span data-stu-id="fc77c-125">MailboxFullStatus</span></span>  <br/> |<span data-ttu-id="fc77c-126">Stellt den Status für ein vollständiges Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="fc77c-126">Represents the status for a mailbox that is full.</span></span>  <br/> |
|<span data-ttu-id="fc77c-127">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="fc77c-127">CustomMailTip</span></span>  <br/> |<span data-ttu-id="fc77c-128">Stellt einen benutzerdefinierten e-Mail-Tipp dar.</span><span class="sxs-lookup"><span data-stu-id="fc77c-128">Represents a custom mail tip.</span></span>  <br/> |
|<span data-ttu-id="fc77c-129">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="fc77c-129">ExternalMemberCount</span></span>  <br/> |<span data-ttu-id="fc77c-130">Stellt die Anzahl externer Member dar.</span><span class="sxs-lookup"><span data-stu-id="fc77c-130">Represents the count of external members.</span></span>  <br/> |
|<span data-ttu-id="fc77c-131">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="fc77c-131">TotalMemberCount</span></span>  <br/> |<span data-ttu-id="fc77c-132">Stellt die Anzahl aller Elemente dar.</span><span class="sxs-lookup"><span data-stu-id="fc77c-132">Represents the count of all members.</span></span>  <br/> |
|<span data-ttu-id="fc77c-133">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="fc77c-133">MaxMessageSize</span></span>  <br/> |<span data-ttu-id="fc77c-134">Stellt die maximale Nachrichtengröße dar, die ein Empfänger annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="fc77c-134">Represents the maximum message size a recipient can accept.</span></span>  <br/> |
|<span data-ttu-id="fc77c-135">DeliveryRestriction</span><span class="sxs-lookup"><span data-stu-id="fc77c-135">DeliveryRestriction</span></span>  <br/> |<span data-ttu-id="fc77c-136">Gibt an, ob durch Übermittlungseinschränkungen verhindert wird, dass die Nachricht des Absenders den Empfänger erreicht.</span><span class="sxs-lookup"><span data-stu-id="fc77c-136">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|<span data-ttu-id="fc77c-137">ModerationStatus</span><span class="sxs-lookup"><span data-stu-id="fc77c-137">ModerationStatus</span></span>  <br/> |<span data-ttu-id="fc77c-138">Gibt an, ob die Nachricht des Absenders von einem Moderator überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="fc77c-138">Indicates whether the sender's message will be reviewed by a moderator.</span></span>  <br/> |
|<span data-ttu-id="fc77c-139">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="fc77c-139">InvalidRecipient</span></span>  <br/> |<span data-ttu-id="fc77c-140">Gibt an, ob der Empfänger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="fc77c-140">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc77c-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc77c-141">Remarks</span></span>

<span data-ttu-id="fc77c-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fc77c-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc77c-143">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fc77c-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc77c-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc77c-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fc77c-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fc77c-145">Schema Name</span></span>  <br/> |<span data-ttu-id="fc77c-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fc77c-146">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fc77c-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fc77c-147">Validation File</span></span>  <br/> |<span data-ttu-id="fc77c-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fc77c-148">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fc77c-149">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fc77c-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="fc77c-150">False</span><span class="sxs-lookup"><span data-stu-id="fc77c-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc77c-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc77c-151">See also</span></span>



- [<span data-ttu-id="fc77c-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fc77c-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

