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
description: Das MailTipsRequested-Element enthält die Arten von e-Mail-Infos aus dem Dienst angefordert.
ms.openlocfilehash: fa2bef394ea8473aa65bdc2f1d39c0794186fdc6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830348"
---
# <a name="mailtipsrequested"></a><span data-ttu-id="c1cd6-103">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="c1cd6-103">MailTipsRequested</span></span>

<span data-ttu-id="c1cd6-104">Das **MailTipsRequested** -Element enthält die Arten von e-Mail-Infos aus dem Dienst angefordert.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-104">The **MailTipsRequested** element contains the types of mail tips requested from the service.</span></span> 
  
```XML
<MailTipsRequested/>
```

 <span data-ttu-id="c1cd6-105">**MailTipTypes**</span><span class="sxs-lookup"><span data-stu-id="c1cd6-105">**MailTipTypes**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1cd6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c1cd6-106">Attributes and elements</span></span>

<span data-ttu-id="c1cd6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1cd6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1cd6-108">Attributes</span></span>

<span data-ttu-id="c1cd6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1cd6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1cd6-110">Child elements</span></span>

<span data-ttu-id="c1cd6-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1cd6-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1cd6-112">Parent elements</span></span>

|<span data-ttu-id="c1cd6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1cd6-113">**Element**</span></span>|<span data-ttu-id="c1cd6-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1cd6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1cd6-115">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="c1cd6-115">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="c1cd6-116">Enthält die Empfänger und Typen von e-Mail-Infos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-116">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1cd6-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="c1cd6-117">Text value</span></span>

<span data-ttu-id="c1cd6-118">Die folgende Tabelle enthält die möglichen Werte für das **MailTipsRequested** -Element.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-118">The following table lists the possible values for the **MailTipsRequested** element.</span></span> 
  
|<span data-ttu-id="c1cd6-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c1cd6-119">**Value**</span></span>|<span data-ttu-id="c1cd6-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1cd6-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1cd6-121">Alle</span><span class="sxs-lookup"><span data-stu-id="c1cd6-121">All</span></span>  <br/> |<span data-ttu-id="c1cd6-122">Stellt alle verfügbaren e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-122">Represents all available mail tips.</span></span>  <br/> |
|<span data-ttu-id="c1cd6-123">OutOfOfficeMessage</span><span class="sxs-lookup"><span data-stu-id="c1cd6-123">OutOfOfficeMessage</span></span>  <br/> |<span data-ttu-id="c1cd6-124">Stellt die Nachricht Out of Office (OOF) dar.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-124">Represents the Out of Office (OOF) message.</span></span>  <br/> |
|<span data-ttu-id="c1cd6-125">MailboxFullStatus</span><span class="sxs-lookup"><span data-stu-id="c1cd6-125">MailboxFullStatus</span></span>  <br/> |<span data-ttu-id="c1cd6-126">Stellt den Status für ein Postfach, das voll ist.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-126">Represents the status for a mailbox that is full.</span></span>  <br/> |
|<span data-ttu-id="c1cd6-127">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="c1cd6-127">CustomMailTip</span></span>  <br/> |<span data-ttu-id="c1cd6-128">Stellt eine benutzerdefinierte e-Mail-Info.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-128">Represents a custom mail tip.</span></span>  <br/> |
|<span data-ttu-id="c1cd6-129">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="c1cd6-129">ExternalMemberCount</span></span>  <br/> |<span data-ttu-id="c1cd6-130">Die Anzahl der externen Elemente darstellt.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-130">Represents the count of external members.</span></span>  <br/> |
|<span data-ttu-id="c1cd6-131">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="c1cd6-131">TotalMemberCount</span></span>  <br/> |<span data-ttu-id="c1cd6-132">Stellt die Anzahl aller Elemente.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-132">Represents the count of all members.</span></span>  <br/> |
|<span data-ttu-id="c1cd6-133">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="c1cd6-133">MaxMessageSize</span></span>  <br/> |<span data-ttu-id="c1cd6-134">Stellt die maximale Größe von Nachrichten, die ein Empfänger akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-134">Represents the maximum message size a recipient can accept.</span></span>  <br/> |
|<span data-ttu-id="c1cd6-135">DeliveryRestriction</span><span class="sxs-lookup"><span data-stu-id="c1cd6-135">DeliveryRestriction</span></span>  <br/> |<span data-ttu-id="c1cd6-136">Gibt an, ob Einschränkungen Übermittlung des Absenders der Nachricht verhindern Erreichen des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-136">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|<span data-ttu-id="c1cd6-137">ModerationStatus</span><span class="sxs-lookup"><span data-stu-id="c1cd6-137">ModerationStatus</span></span>  <br/> |<span data-ttu-id="c1cd6-138">Gibt an, ob der Absender der Nachricht von einem Moderator überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-138">Indicates whether the sender's message will be reviewed by a moderator.</span></span>  <br/> |
|<span data-ttu-id="c1cd6-139">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="c1cd6-139">InvalidRecipient</span></span>  <br/> |<span data-ttu-id="c1cd6-140">Gibt an, ob der Empfänger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-140">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1cd6-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1cd6-141">Remarks</span></span>

<span data-ttu-id="c1cd6-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1cd6-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c1cd6-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1cd6-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1cd6-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c1cd6-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c1cd6-145">Schema Name</span></span>  <br/> |<span data-ttu-id="c1cd6-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c1cd6-146">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c1cd6-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c1cd6-147">Validation File</span></span>  <br/> |<span data-ttu-id="c1cd6-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c1cd6-148">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c1cd6-149">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c1cd6-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1cd6-150">False</span><span class="sxs-lookup"><span data-stu-id="c1cd6-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1cd6-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1cd6-151">See also</span></span>



- [<span data-ttu-id="c1cd6-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1cd6-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

