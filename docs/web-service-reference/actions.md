---
title: Aktionen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Actions
api_type:
- schema
ms.assetid: c5aa96b1-2d8b-422f-8c2f-f118572ab23f
description: Das Actions-Element stellt die Gruppe von Aktionen dar, die für eine Nachricht zur Verfügung stehen, wenn die Bedingungen erfüllt sind.
ms.openlocfilehash: 2ac53778b583595fa8be07f2c5110a9e2df16eca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465065"
---
# <a name="actions"></a><span data-ttu-id="7c6fd-103">Aktionen</span><span class="sxs-lookup"><span data-stu-id="7c6fd-103">Actions</span></span>

<span data-ttu-id="7c6fd-104">Das **Actions** -Element stellt die Gruppe von Aktionen dar, die für eine Nachricht zur Verfügung stehen, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-104">The **Actions** element represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span> 
  
[<span data-ttu-id="7c6fd-105">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="7c6fd-105">Rule (RuleType)</span></span>](rule-ruletype.md)
  
```XML
<Actions>
    <AssignCategories>
    <CopyToFolder>
    <Delete>
    <ForwardAsAttachmentToRecipients>
    <ForwardToRecipients>
    <MarkImportance>
    <MarkAsRead>
    <MoveToFolder>
    <PermanentDelete>
    <RedirectToRecipients>
    <SendSMSAlertToRecipients>
    <ServerReplyWithMessage>
    <StopProcessingRules>
</Actions>
```

 <span data-ttu-id="7c6fd-106">**RuleActionsType**</span><span class="sxs-lookup"><span data-stu-id="7c6fd-106">**RuleActionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7c6fd-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7c6fd-107">Attributes and elements</span></span>

<span data-ttu-id="7c6fd-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c6fd-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="7c6fd-109">Attributes</span></span>

<span data-ttu-id="7c6fd-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7c6fd-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7c6fd-111">Child elements</span></span>

|<span data-ttu-id="7c6fd-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c6fd-112">**Element**</span></span>|<span data-ttu-id="7c6fd-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c6fd-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c6fd-114">AssignCategories</span><span class="sxs-lookup"><span data-stu-id="7c6fd-114">AssignCategories</span></span>](assigncategories.md) <br/> |<span data-ttu-id="7c6fd-115">Stellt die Kategorien dar, die auf e-Mail-Nachrichten gestempelt werden.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-115">Represents the categories that are stamped on e-mail messages.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-116">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="7c6fd-116">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="7c6fd-117">Gibt die ID des Ordners an, in den e-Mail-Elemente kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-117">Identifies the ID of the folder that e-mail items will be copied to.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-118">Löschen</span><span class="sxs-lookup"><span data-stu-id="7c6fd-118">Delete</span></span>](delete.md) <br/> |<span data-ttu-id="7c6fd-119">Gibt an, ob Nachrichten in den Ordner "Gelöschte Elemente" verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-119">Indicates whether messages are to be moved to the Deleted Items folder.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-120">ForwardAsAttachmentToRecipients</span><span class="sxs-lookup"><span data-stu-id="7c6fd-120">ForwardAsAttachmentToRecipients</span></span>](forwardasattachmenttorecipients.md) <br/> |<span data-ttu-id="7c6fd-121">Gibt die e-Mail-Adressen an, an die Nachrichten als Anlagen weitergeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-121">Indicates the e-mail addresses to which messages are to be forwarded as attachments.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-122">ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="7c6fd-122">ForwardToRecipients</span></span>](forwardtorecipients.md) <br/> |<span data-ttu-id="7c6fd-123">Gibt die e-Mail-Adressen an, an die Nachrichten weitergeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-123">Indicates the e-mail addresses to which messages are to be forwarded.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-124">MarkImportance</span><span class="sxs-lookup"><span data-stu-id="7c6fd-124">MarkImportance</span></span>](markimportance.md) <br/> |<span data-ttu-id="7c6fd-125">Gibt die Wichtigkeit an, die für Nachrichten gestempelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-125">Specifies the importance that is to be stamped on messages.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-126">MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="7c6fd-126">MarkAsRead</span></span>](markasread.md) <br/> |<span data-ttu-id="7c6fd-127">Gibt an, ob Nachrichten als gelesen markiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-127">Indicates whether messages are to be marked as read.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-128">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="7c6fd-128">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="7c6fd-129">Gibt die ID des Ordners an, in den e-Mail-Elemente verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-129">Identifies the ID of the folder that e-mail items will be moved to.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-130">PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="7c6fd-130">PermanentDelete</span></span>](permanentdelete.md) <br/> |<span data-ttu-id="7c6fd-131">Gibt an, ob Nachrichten endgültig gelöscht und nicht im Ordner "Gelöschte Elemente" gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-131">Indicates whether messages are to be permanently deleted and not saved to the Deleted Items folder.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-132">RedirectToRecipients</span><span class="sxs-lookup"><span data-stu-id="7c6fd-132">RedirectToRecipients</span></span>](redirecttorecipients.md) <br/> |<span data-ttu-id="7c6fd-133">Gibt die e-Mail-Adressen an, an die Nachrichten umgeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-133">Indicates the e-mail addresses to which messages are to be redirected.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-134">SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="7c6fd-134">SendSMSAlertToRecipients</span></span>](sendsmsalerttorecipients.md) <br/> |<span data-ttu-id="7c6fd-135">Gibt die Mobiltelefon Nummern an, an die eine SMS-Benachrichtigung (Short Message Service) gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-135">Indicates the mobile phone numbers to which a Short Message Service (SMS) alert is to be sent.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-136">ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="7c6fd-136">ServerReplyWithMessage</span></span>](serverreplywithmessage.md) <br/> |<span data-ttu-id="7c6fd-137">Gibt an.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-137">Indicates.</span></span> <span data-ttu-id="7c6fd-138">die ID der Vorlagen Nachricht, die als Antwort auf eingehende Nachrichten gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-138">the ID of the template message that is to be sent as a reply to incoming messages.</span></span>  <br/> |
|[<span data-ttu-id="7c6fd-139">StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="7c6fd-139">StopProcessingRules</span></span>](stopprocessingrules.md) <br/> |<span data-ttu-id="7c6fd-140">Gibt an, ob nachfolgende Regeln ausgewertet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-140">Indicates whether subsequent rules are to be evaluated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7c6fd-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7c6fd-141">Parent elements</span></span>

|<span data-ttu-id="7c6fd-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c6fd-142">**Element**</span></span>|<span data-ttu-id="7c6fd-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c6fd-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c6fd-144">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="7c6fd-144">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="7c6fd-145">Stellt eine einzelne Regel im Postfach eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-145">Represents a single rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7c6fd-146">Textwert</span><span class="sxs-lookup"><span data-stu-id="7c6fd-146">Text value</span></span>

<span data-ttu-id="7c6fd-147">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-147">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c6fd-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c6fd-148">Remarks</span></span>

<span data-ttu-id="7c6fd-149">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7c6fd-149">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c6fd-150">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7c6fd-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c6fd-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="7c6fd-151">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7c6fd-152">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7c6fd-152">Schema Name</span></span>  <br/> |<span data-ttu-id="7c6fd-153">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7c6fd-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="7c6fd-154">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7c6fd-154">Validation File</span></span>  <br/> |<span data-ttu-id="7c6fd-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7c6fd-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7c6fd-156">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7c6fd-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="7c6fd-157">True</span><span class="sxs-lookup"><span data-stu-id="7c6fd-157">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c6fd-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c6fd-158">See also</span></span>

- [<span data-ttu-id="7c6fd-159">Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="7c6fd-159">Conditions</span></span>](conditions.md)
- [<span data-ttu-id="7c6fd-160">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7c6fd-160">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

