---
title: Bedingungen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conditions
api_type:
- schema
ms.assetid: f049a48c-9585-43f7-8549-0b8cb19a5eea
description: Das Conditions-Element gibt die Bedingungen an, die die Regelaktionen für eine Regel auslösen, wenn Sie erfüllt werden.
ms.openlocfilehash: 2c6b4794a87cca79b4c723197b57360ad0ff973d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463202"
---
# <a name="conditions"></a><span data-ttu-id="0a141-103">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="0a141-103">Conditions</span></span>

<span data-ttu-id="0a141-104">Das **Conditions** -Element gibt die Bedingungen an, die die Regelaktionen für eine Regel auslösen, wenn Sie erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="0a141-104">The **Conditions** element identifies the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span> 
  
```XML
<Conditions>
   <Categories/>
   <ContainsBodyStrings/>
   <ContainsHeaderStrings/>
   <ContainsRecipientStrings/>
   <ContainsSenderStrings/>
   <ContainsSubjectOrBodyStrings/>
   <ContainsSubjectStrings/>
   <FlaggedForAction/>
   <FromAddresses/>
   <FromConnectedAccounts/>
   <HasAttachments/>
   <Importance/>
   <IsApprovalRequest/>
   <IsAutomaticForward/>
   <IsAutomaticReply/>
   <IsEncrypted/>
   <IsMeetingRequest/>
   <IsMeetingResponse/>
   <IsNDR/>
   <IsPermissionControlled/>
   <IsReadReceipt/>
   <IsSigned/>
   <IsVoicemail/>
   <ItemClasses/>
   <MessageClassifications/>
   <NotSentToMe/>
   <SentCcMe/>
   <SentOnlyToMe/>
   <SentToAddresses/>
   <SentToMe/>
   <SentToOrCcMe/>
   <Sensitivity/>
   <WithinDateRange/>
   <WithinSizeRange/>
</Conditions>
```

 <span data-ttu-id="0a141-105">**RulePredicatesType**</span><span class="sxs-lookup"><span data-stu-id="0a141-105">**RulePredicatesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0a141-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0a141-106">Attributes and elements</span></span>

<span data-ttu-id="0a141-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0a141-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a141-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0a141-108">Attributes</span></span>

<span data-ttu-id="0a141-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0a141-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0a141-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0a141-110">Child elements</span></span>

|<span data-ttu-id="0a141-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0a141-111">**Element**</span></span>|<span data-ttu-id="0a141-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0a141-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a141-113">Categories</span><span class="sxs-lookup"><span data-stu-id="0a141-113">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0a141-114">Enthält die Kategorien, die auf eine eingehende Nachricht angewendet werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-114">Contains the categories that must be applied to an incoming message in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-115">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="0a141-115">ContainsBodyStrings</span></span>](containsbodystrings.md) <br/> |<span data-ttu-id="0a141-116">Gibt die Zeichenfolgen an, die im Textkörper von eingehenden Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-116">Indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-117">ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="0a141-117">ContainsHeaderStrings</span></span>](containsheaderstrings.md) <br/> |<span data-ttu-id="0a141-118">Gibt die Zeichenfolgen an, die in den Kopfzeilen eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-118">Indicates the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-119">ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="0a141-119">ContainsRecipientStrings</span></span>](containsrecipientstrings.md) <br/> |<span data-ttu-id="0a141-120">Gibt die Zeichenfolgen an, die entweder in der **torecipients** -oder der **CcRecipients** -Eigenschaft der eingehenden Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-120">Indicates the strings that must appear in either the **ToRecipients** or **CcRecipients** properties of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-121">ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="0a141-121">ContainsSenderStrings</span></span>](containssenderstrings.md) <br/> |<span data-ttu-id="0a141-122">Gibt die Zeichenfolgen an, die in der **from** -Eigenschaft eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-122">Indicates the strings that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-123">ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="0a141-123">ContainsSubjectOrBodyStrings</span></span>](containssubjectorbodystrings.md) <br/> |<span data-ttu-id="0a141-124">Gibt die Zeichenfolgen an, die entweder im Textkörper oder im Betreff eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-124">Indicates the strings that must appear in either the body or the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-125">ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="0a141-125">ContainsSubjectStrings</span></span>](containssubjectstrings.md) <br/> |<span data-ttu-id="0a141-126">Gibt die Zeichenfolgen an, die im Betreff eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-126">Indicates the strings that must appear in the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-127">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="0a141-127">FlaggedForAction</span></span>](flaggedforaction.md) <br/> |<span data-ttu-id="0a141-128">Gibt das Flag für Action-Wert an, das in eingehenden Nachrichten angezeigt werden muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-128">Specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-129">FromAddresses</span><span class="sxs-lookup"><span data-stu-id="0a141-129">FromAddresses</span></span>](fromaddresses.md) <br/> |<span data-ttu-id="0a141-130">Gibt die e-Mail-Adressen an, aus denen eingehende Nachrichten gesendet werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-130">Indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-131">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="0a141-131">FromConnectedAccounts</span></span>](fromconnectedaccounts.md) <br/> |<span data-ttu-id="0a141-132">Stellt die e-Mail-Kontonamen dar, aus denen eingehende Nachrichten aggregiert werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-132">Represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-133">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="0a141-133">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="0a141-134">Gibt an, ob eingehende Nachrichten Anlagen aufweisen müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-134">Indicates whether incoming messages have to have attachments in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-135">Importance</span><span class="sxs-lookup"><span data-stu-id="0a141-135">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="0a141-136">Gibt die Wichtigkeit für eingehende Nachrichten an, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-136">Specifies the importance that is stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-137">IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="0a141-137">IsApprovalRequest</span></span>](isapprovalrequest.md) <br/> |<span data-ttu-id="0a141-138">Gibt an, ob eingehende Nachrichten Genehmigungsanforderungen sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-138">Indicates whether incoming messages must be approval requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-139">IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="0a141-139">IsAutomaticForward</span></span>](isautomaticforward.md) <br/> |<span data-ttu-id="0a141-140">Gibt an, ob eingehende Nachrichten automatisch weitergeleitet werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-140">Indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-141">IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="0a141-141">IsAutomaticReply</span></span>](isautomaticreply.md) <br/> |<span data-ttu-id="0a141-142">Gibt an, ob eingehende Nachrichten automatische Antworten sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-142">Indicates whether incoming messages must be automatic replies in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-143">IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="0a141-143">IsEncrypted</span></span>](isencrypted.md) <br/> |<span data-ttu-id="0a141-144">Gibt an, ob eingehende Nachrichten S/MIME verschlüsselt sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-144">Indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-145">IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="0a141-145">IsMeetingRequest</span></span>](ismeetingrequest.md) <br/> |<span data-ttu-id="0a141-146">Gibt an, ob eingehende Nachrichten Besprechungsanfragen sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-146">Indicates whether incoming messages must be meeting requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-147">IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="0a141-147">IsMeetingResponse</span></span>](ismeetingresponse.md) <br/> |<span data-ttu-id="0a141-148">Gibt an, ob eingehende Nachrichten Antworten erfüllen müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-148">Indicates whether incoming messages must be meeting responses in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-149">IsNDR</span><span class="sxs-lookup"><span data-stu-id="0a141-149">IsNDR</span></span>](isndr.md) <br/> |<span data-ttu-id="0a141-150">Gibt an, ob eingehende Nachrichten nicht Zustellungsberichte sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-150">Indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-151">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="0a141-151">IsPermissionControlled</span></span>](ispermissioncontrolled.md) <br/> |<span data-ttu-id="0a141-152">Gibt an, ob eingehende Nachrichten berechtigungsgesteuert (RMS protected) sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-152">Indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-153">IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="0a141-153">IsReadReceipt</span></span>](isreadreceipt.md) <br/> |<span data-ttu-id="0a141-154">Gibt an, ob eingehende Nachrichten Lesebestätigungen sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-154">Indicates whether incoming messages must be read receipts in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-155">IsSigned</span><span class="sxs-lookup"><span data-stu-id="0a141-155">IsSigned</span></span>](issigned.md) <br/> |<span data-ttu-id="0a141-156">Gibt an, ob eingehende Nachrichten S/MIME signiert sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-156">Indicates whether incoming messages must be S/MIME signed in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-157">IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="0a141-157">IsVoicemail</span></span>](isvoicemail.md) <br/> |<span data-ttu-id="0a141-158">Gibt an, ob eingehende Nachrichten Voicemail-Nachrichten sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-158">Indicates whether incoming messages must be voice mail messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-159">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="0a141-159">ItemClasses</span></span>](itemclasses.md) <br/> |<span data-ttu-id="0a141-160">Stellt die Elementklassen dar, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-160">Represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-161">MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="0a141-161">MessageClassifications</span></span>](messageclassifications.md) <br/> |<span data-ttu-id="0a141-162">Stellt die Nachrichtenklassifikationen dar, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-162">Represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-163">NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="0a141-163">NotSentToMe</span></span>](notsenttome.md) <br/> |<span data-ttu-id="0a141-164">Gibt an, ob der Besitzer des Postfachs nicht in der **torecipients** -Eigenschaft der eingehenden Nachrichten sein darf, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-164">Indicates whether the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-165">SentCcMe</span><span class="sxs-lookup"><span data-stu-id="0a141-165">SentCcMe</span></span>](sentccme.md) <br/> |<span data-ttu-id="0a141-166">Gibt an, ob der Besitzer des Postfachs in der **CcRecipients** -Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-166">Indicates whether the owner of the mailbox has to be in the **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-167">SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="0a141-167">SentOnlyToMe</span></span>](sentonlytome.md) <br/> |<span data-ttu-id="0a141-168">Gibt an, ob der Besitzer des Postfachs der einzige in der **torecipients** -Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-168">Indicates whether the owner of the mailbox has to be the only one in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-169">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="0a141-169">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="0a141-170">Gibt die e-Mail-Adressen an, an die eingehende Nachrichten gesendet wurden, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-170">Indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-171">SentToMe</span><span class="sxs-lookup"><span data-stu-id="0a141-171">SentToMe</span></span>](senttome.md) <br/> |<span data-ttu-id="0a141-172">Gibt an, ob der Besitzer des Postfachs in der **torecipients** -Eigenschaft der eingehenden Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-172">Indicates whether the owner of the mailbox has to be in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-173">SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="0a141-173">SentToOrCcMe</span></span>](senttoorccme.md) <br/> |<span data-ttu-id="0a141-174">Gibt an, ob der Besitzer des Postfachs entweder eine **torecipients** -oder eine **CcRecipients** -Eigenschaft eingehender Nachrichten sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-174">Indicates whether the owner of the mailbox has to be in either a **ToRecipients** or **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-175">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="0a141-175">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="0a141-176">Gibt die Empfindlichkeit an, die für eingehende Nachrichten gestempelt werden muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-176">Indicates the sensitivity that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-177">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="0a141-177">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="0a141-178">Gibt den Datumsbereich an, innerhalb dessen eingehende Nachrichten empfangen werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-178">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="0a141-179">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="0a141-179">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="0a141-180">Gibt die Mindest-und Höchstgröße an, die eingehende Nachrichten aufweisen müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="0a141-180">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0a141-181">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0a141-181">Parent elements</span></span>

|<span data-ttu-id="0a141-182">**Element**</span><span class="sxs-lookup"><span data-stu-id="0a141-182">**Element**</span></span>|<span data-ttu-id="0a141-183">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0a141-183">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a141-184">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="0a141-184">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="0a141-185">Enthält eine einzelne Regel und stellt eine Regel im Postfach eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="0a141-185">Contains a single rule and represents a rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0a141-186">Textwert</span><span class="sxs-lookup"><span data-stu-id="0a141-186">Text value</span></span>

<span data-ttu-id="0a141-187">Keine.</span><span class="sxs-lookup"><span data-stu-id="0a141-187">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a141-188">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a141-188">Remarks</span></span>

<span data-ttu-id="0a141-189">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0a141-189">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a141-190">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0a141-190">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a141-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a141-191">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0a141-192">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0a141-192">Schema Name</span></span>  <br/> |<span data-ttu-id="0a141-193">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0a141-193">Types schema</span></span>  <br/> |
|<span data-ttu-id="0a141-194">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0a141-194">Validation File</span></span>  <br/> |<span data-ttu-id="0a141-195">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0a141-195">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0a141-196">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0a141-196">Can be Empty</span></span>  <br/> |<span data-ttu-id="0a141-197">True</span><span class="sxs-lookup"><span data-stu-id="0a141-197">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a141-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a141-198">See also</span></span>



[<span data-ttu-id="0a141-199">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="0a141-199">Exceptions</span></span>](exceptions.md)


- [<span data-ttu-id="0a141-200">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0a141-200">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

