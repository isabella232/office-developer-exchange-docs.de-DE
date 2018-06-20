---
title: PendingMailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PendingMailTips
api_type:
- schema
ms.assetid: 0cd70eea-8d36-4b1b-bf80-5edf359e7ba7
description: Das PendingMailTips-Element gibt an, dass die e-Mail-Infos in diesem Element nicht ausgewertet werden konnte, bevor die Verarbeitung der Servertimeout abgelaufen.
ms.openlocfilehash: 73d597f6534ea29f7d26d6526c48631251521ae5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830704"
---
# <a name="pendingmailtips"></a><span data-ttu-id="c1868-103">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="c1868-103">PendingMailTips</span></span>

<span data-ttu-id="c1868-104">Das **PendingMailTips** -Element gibt an, dass die e-Mail-Infos in diesem Element nicht ausgewertet werden konnte, bevor die Verarbeitung der Servertimeout abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="c1868-104">The **PendingMailTips** element indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span> 
  
```XML
<PendingMailTips>All | OutOfOfficeMessage | MailboxFullStatus | CustomMailTip | ExternalMemberCount | TotalMemberCount | MaxMessageSize | DeliveryRestriction | ModerateStatus | InvalidRecipient</PendingMailTips>
```

 <span data-ttu-id="c1868-105">**MailTipTypes**</span><span class="sxs-lookup"><span data-stu-id="c1868-105">**MailTipTypes**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1868-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c1868-106">Attributes and elements</span></span>

<span data-ttu-id="c1868-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1868-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1868-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1868-108">Attributes</span></span>

<span data-ttu-id="c1868-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1868-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1868-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1868-110">Child elements</span></span>

<span data-ttu-id="c1868-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1868-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1868-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1868-112">Parent elements</span></span>

|<span data-ttu-id="c1868-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1868-113">**Element**</span></span>|<span data-ttu-id="c1868-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1868-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1868-115">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="c1868-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="c1868-116">Stellt Werte für verschiedene Arten von e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="c1868-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1868-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="c1868-117">Text value</span></span>

<span data-ttu-id="c1868-118">Die folgende Tabelle enthält die möglichen Werte für das **PendingMailTips** -Element.</span><span class="sxs-lookup"><span data-stu-id="c1868-118">The following table lists the possible values for the **PendingMailTips** element.</span></span> 
  
|<span data-ttu-id="c1868-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c1868-119">**Value**</span></span>|<span data-ttu-id="c1868-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1868-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1868-121">Alle</span><span class="sxs-lookup"><span data-stu-id="c1868-121">All</span></span>  <br/> |<span data-ttu-id="c1868-122">Stellt alle verfügbaren e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="c1868-122">Represents all available mail tips.</span></span>  <br/> |
|<span data-ttu-id="c1868-123">OutOfOfficeMessage</span><span class="sxs-lookup"><span data-stu-id="c1868-123">OutOfOfficeMessage</span></span>  <br/> |<span data-ttu-id="c1868-124">Stellt die Nachricht Out of Office (OOF) dar.</span><span class="sxs-lookup"><span data-stu-id="c1868-124">Represents the Out of Office (OOF) message.</span></span>  <br/> |
|<span data-ttu-id="c1868-125">MailboxFullStatus</span><span class="sxs-lookup"><span data-stu-id="c1868-125">MailboxFullStatus</span></span>  <br/> |<span data-ttu-id="c1868-126">Stellt den Status für ein volles Postfach an.</span><span class="sxs-lookup"><span data-stu-id="c1868-126">Represents the status for a mailbox being full.</span></span>  <br/> |
|<span data-ttu-id="c1868-127">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="c1868-127">CustomMailTip</span></span>  <br/> |<span data-ttu-id="c1868-128">Stellt eine benutzerdefinierte e-Mail-Info.</span><span class="sxs-lookup"><span data-stu-id="c1868-128">Represents a custom mail tip.</span></span>  <br/> |
|<span data-ttu-id="c1868-129">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="c1868-129">ExternalMemberCount</span></span>  <br/> |<span data-ttu-id="c1868-130">Die Anzahl der externen Elemente darstellt.</span><span class="sxs-lookup"><span data-stu-id="c1868-130">Represents the count of external members.</span></span>  <br/> |
|<span data-ttu-id="c1868-131">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="c1868-131">TotalMemberCount</span></span>  <br/> |<span data-ttu-id="c1868-132">Stellt die Anzahl aller Elemente.</span><span class="sxs-lookup"><span data-stu-id="c1868-132">Represents the count of all members.</span></span>  <br/> |
|<span data-ttu-id="c1868-133">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="c1868-133">MaxMessageSize</span></span>  <br/> |<span data-ttu-id="c1868-134">Stellt die maximale Größe von Nachrichten, die ein Empfänger akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="c1868-134">Represents the maximum message size a recipient can accept.</span></span>  <br/> |
|<span data-ttu-id="c1868-135">DeliveryRestriction</span><span class="sxs-lookup"><span data-stu-id="c1868-135">DeliveryRestriction</span></span>  <br/> |<span data-ttu-id="c1868-136">Gibt an, ob Einschränkungen Übermittlung des Absenders der Nachricht verhindern Erreichen des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="c1868-136">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|<span data-ttu-id="c1868-137">ModerationStatus</span><span class="sxs-lookup"><span data-stu-id="c1868-137">ModerationStatus</span></span>  <br/> |<span data-ttu-id="c1868-138">Gibt an, ob der Absender der Nachricht von einem Moderator überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="c1868-138">Indicates whether the sender's message will be reviewed by a moderator.</span></span>  <br/> |
|<span data-ttu-id="c1868-139">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="c1868-139">InvalidRecipient</span></span>  <br/> |<span data-ttu-id="c1868-140">Gibt an, ob der Empfänger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="c1868-140">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1868-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1868-141">Remarks</span></span>

<span data-ttu-id="c1868-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c1868-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1868-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c1868-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1868-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1868-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1868-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c1868-145">Schema Name</span></span>  <br/> |<span data-ttu-id="c1868-146">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c1868-146">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1868-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c1868-147">Validation File</span></span>  <br/> |<span data-ttu-id="c1868-148">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1868-148">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1868-149">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c1868-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1868-150">False</span><span class="sxs-lookup"><span data-stu-id="c1868-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1868-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1868-151">See also</span></span>



- [<span data-ttu-id="c1868-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1868-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

