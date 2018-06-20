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
description: Conditions-Element identifiziert die Bedingungen, die beim erfüllt, Regelaktionen für eine Regel ausgelöst wird.
ms.openlocfilehash: f66777e82892122c4c7dac45bdef3c42f5c4a577
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757592"
---
# <a name="conditions"></a><span data-ttu-id="51ec1-103">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="51ec1-103">Conditions</span></span>

<span data-ttu-id="51ec1-104">**Conditions** -Element identifiziert die Bedingungen, die beim erfüllt, Regelaktionen für eine Regel ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="51ec1-104">The **Conditions** element identifies the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span> 
  
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

 <span data-ttu-id="51ec1-105">**RulePredicatesType**</span><span class="sxs-lookup"><span data-stu-id="51ec1-105">**RulePredicatesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="51ec1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="51ec1-106">Attributes and elements</span></span>

<span data-ttu-id="51ec1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="51ec1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="51ec1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="51ec1-108">Attributes</span></span>

<span data-ttu-id="51ec1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="51ec1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="51ec1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="51ec1-110">Child elements</span></span>

|<span data-ttu-id="51ec1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="51ec1-111">**Element**</span></span>|<span data-ttu-id="51ec1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="51ec1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51ec1-113">Categories</span><span class="sxs-lookup"><span data-stu-id="51ec1-113">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="51ec1-114">Enthält die Kategorien, die auf eine eingehende Nachricht in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-114">Contains the categories that must be applied to an incoming message in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-115">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="51ec1-115">ContainsBodyStrings</span></span>](containsbodystrings.md) <br/> |<span data-ttu-id="51ec1-116">Gibt die Zeichenfolgen, die im Textkörper der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende angezeigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-116">Indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-117">ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="51ec1-117">ContainsHeaderStrings</span></span>](containsheaderstrings.md) <br/> |<span data-ttu-id="51ec1-118">Gibt die Zeichenfolgen, die in den Kopfzeilen der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende angezeigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-118">Indicates the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-119">ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="51ec1-119">ContainsRecipientStrings</span></span>](containsrecipientstrings.md) <br/> |<span data-ttu-id="51ec1-120">Gibt die Zeichenfolgen, die die **ToRecipients** oder **CcRecipients** Eigenschaften der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende vorhanden sein müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-120">Indicates the strings that must appear in either the **ToRecipients** or **CcRecipients** properties of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-121">ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="51ec1-121">ContainsSenderStrings</span></span>](containssenderstrings.md) <br/> |<span data-ttu-id="51ec1-122">Gibt die Zeichenfolgen, die in der Eigenschaft **aus** der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende angezeigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-122">Indicates the strings that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-123">ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="51ec1-123">ContainsSubjectOrBodyStrings</span></span>](containssubjectorbodystrings.md) <br/> |<span data-ttu-id="51ec1-124">Gibt die Zeichenfolgen, die im Text oder den Betreff der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende angezeigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-124">Indicates the strings that must appear in either the body or the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-125">ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="51ec1-125">ContainsSubjectStrings</span></span>](containssubjectstrings.md) <br/> |<span data-ttu-id="51ec1-126">Gibt die Zeichenfolgen, die den Betreff der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende vorhanden sein müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-126">Indicates the strings that must appear in the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-127">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="51ec1-127">FlaggedForAction</span></span>](flaggedforaction.md) <br/> |<span data-ttu-id="51ec1-128">Gibt die Kennzeichen für den Aktionswert, die angezeigt werden, muss auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anwenden.</span><span class="sxs-lookup"><span data-stu-id="51ec1-128">Specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-129">FromAddresses</span><span class="sxs-lookup"><span data-stu-id="51ec1-129">FromAddresses</span></span>](fromaddresses.md) <br/> |<span data-ttu-id="51ec1-130">Gibt die E-mail-Adressen aus denen eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gesendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-130">Indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-131">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="51ec1-131">FromConnectedAccounts</span></span>](fromconnectedaccounts.md) <br/> |<span data-ttu-id="51ec1-132">Stellt die Namen der e-Mail-Konten aus denen eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende zusammengefasst wurden verfügen müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-132">Represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-133">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="51ec1-133">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="51ec1-134">Gibt an, ob eingehende Nachrichten mit Anlagen in der Reihenfolge für die Bedingung oder Ausnahme angewendet haben.</span><span class="sxs-lookup"><span data-stu-id="51ec1-134">Indicates whether incoming messages have to have attachments in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-135">Importance</span><span class="sxs-lookup"><span data-stu-id="51ec1-135">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="51ec1-136">Gibt die Bedeutung, die versehen ist in eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anwenden.</span><span class="sxs-lookup"><span data-stu-id="51ec1-136">Specifies the importance that is stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-137">IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="51ec1-137">IsApprovalRequest</span></span>](isapprovalrequest.md) <br/> |<span data-ttu-id="51ec1-138">Gibt an, ob eingehende Nachrichten Genehmigung Anforderungen in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-138">Indicates whether incoming messages must be approval requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-139">IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="51ec1-139">IsAutomaticForward</span></span>](isautomaticforward.md) <br/> |<span data-ttu-id="51ec1-140">Gibt an, ob eingehende Nachrichten automatische Weiterleitungen in Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-140">Indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-141">IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="51ec1-141">IsAutomaticReply</span></span>](isautomaticreply.md) <br/> |<span data-ttu-id="51ec1-142">Gibt an, ob eingehende Nachrichten automatische Antworten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-142">Indicates whether incoming messages must be automatic replies in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-143">IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="51ec1-143">IsEncrypted</span></span>](isencrypted.md) <br/> |<span data-ttu-id="51ec1-144">Gibt an, ob eingehende Nachrichten S/MIME verschlüsselt in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-144">Indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-145">IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="51ec1-145">IsMeetingRequest</span></span>](ismeetingrequest.md) <br/> |<span data-ttu-id="51ec1-146">Gibt an, ob eingehende Nachrichten Anforderungen in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende meeting werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-146">Indicates whether incoming messages must be meeting requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-147">IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="51ec1-147">IsMeetingResponse</span></span>](ismeetingresponse.md) <br/> |<span data-ttu-id="51ec1-148">Gibt an, ob eingehende Nachrichten Antworten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende meeting werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-148">Indicates whether incoming messages must be meeting responses in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-149">IsNDR</span><span class="sxs-lookup"><span data-stu-id="51ec1-149">IsNDR</span></span>](isndr.md) <br/> |<span data-ttu-id="51ec1-150">Gibt an, ob eingehende Nachrichten Unzustellbarkeitsberichte (NDR) müssen in der Reihenfolge für die Bedingung oder Ausnahme anwenden.</span><span class="sxs-lookup"><span data-stu-id="51ec1-150">Indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-151">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="51ec1-151">IsPermissionControlled</span></span>](ispermissioncontrolled.md) <br/> |<span data-ttu-id="51ec1-152">Gibt an, ob eingehende Nachrichten Berechtigung gesteuert (RMS geschützte) in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-152">Indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-153">IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="51ec1-153">IsReadReceipt</span></span>](isreadreceipt.md) <br/> |<span data-ttu-id="51ec1-154">Gibt an, ob eingehende Nachrichten Empfangsbestätigungen in Reihenfolge für die Bedingung oder Ausnahme anzuwendende gelesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-154">Indicates whether incoming messages must be read receipts in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-155">IsSigned</span><span class="sxs-lookup"><span data-stu-id="51ec1-155">IsSigned</span></span>](issigned.md) <br/> |<span data-ttu-id="51ec1-156">Gibt an, ob eingehende Nachrichten, dass in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende S/MIME signiert sein müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-156">Indicates whether incoming messages must be S/MIME signed in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-157">IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="51ec1-157">IsVoicemail</span></span>](isvoicemail.md) <br/> |<span data-ttu-id="51ec1-158">Gibt an, ob eingehende Nachrichten Voicemailnachrichten in Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-158">Indicates whether incoming messages must be voice mail messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-159">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="51ec1-159">ItemClasses</span></span>](itemclasses.md) <br/> |<span data-ttu-id="51ec1-160">Stellt die Element-Klassen, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-160">Represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-161">MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="51ec1-161">MessageClassifications</span></span>](messageclassifications.md) <br/> |<span data-ttu-id="51ec1-162">Stellt die Nachrichtenklassifikationen, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-162">Represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-163">NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="51ec1-163">NotSentToMe</span></span>](notsenttome.md) <br/> |<span data-ttu-id="51ec1-164">Gibt an, ob der Besitzer des Postfachs nicht in der **ToRecipients** -Eigenschaft der eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="51ec1-164">Indicates whether the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-165">SentCcMe</span><span class="sxs-lookup"><span data-stu-id="51ec1-165">SentCcMe</span></span>](sentccme.md) <br/> |<span data-ttu-id="51ec1-166">Gibt an, ob der Besitzer des Postfachs in die **CcRecipients** -Eigenschaft des eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="51ec1-166">Indicates whether the owner of the mailbox has to be in the **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-167">SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="51ec1-167">SentOnlyToMe</span></span>](sentonlytome.md) <br/> |<span data-ttu-id="51ec1-168">Gibt an, ob der Besitzer des Postfachs das einzige Objekt in der **ToRecipients** -Eigenschaft des eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="51ec1-168">Indicates whether the owner of the mailbox has to be the only one in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-169">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="51ec1-169">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="51ec1-170">Gibt die E-mail-Adressen, die eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende an gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="51ec1-170">Indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-171">SentToMe</span><span class="sxs-lookup"><span data-stu-id="51ec1-171">SentToMe</span></span>](senttome.md) <br/> |<span data-ttu-id="51ec1-172">Gibt an, ob der Besitzer des Postfachs in die **ToRecipients** -Eigenschaft des eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="51ec1-172">Indicates whether the owner of the mailbox has to be in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-173">SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="51ec1-173">SentToOrCcMe</span></span>](senttoorccme.md) <br/> |<span data-ttu-id="51ec1-174">Gibt an, ob der Besitzer des Postfachs in einem **ToRecipients** oder **CcRecipients** -Eigenschaft des eingehenden Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="51ec1-174">Indicates whether the owner of the mailbox has to be in either a **ToRecipients** or **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-175">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="51ec1-175">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="51ec1-176">Gibt an, die Vertraulichkeit, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein muss.</span><span class="sxs-lookup"><span data-stu-id="51ec1-176">Indicates the sensitivity that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-177">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="51ec1-177">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="51ec1-178">Gibt den Datumsbereich, in dem eingehende Nachrichten müssen in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="51ec1-178">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="51ec1-179">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="51ec1-179">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="51ec1-180">Gibt die minimale und maximale Größe, die eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="51ec1-180">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="51ec1-181">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="51ec1-181">Parent elements</span></span>

|<span data-ttu-id="51ec1-182">**Element**</span><span class="sxs-lookup"><span data-stu-id="51ec1-182">**Element**</span></span>|<span data-ttu-id="51ec1-183">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="51ec1-183">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51ec1-184">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="51ec1-184">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="51ec1-185">Enthält eine einzelne Regel und stellt eine Regel in dem Postfach eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="51ec1-185">Contains a single rule and represents a rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="51ec1-186">Textwert</span><span class="sxs-lookup"><span data-stu-id="51ec1-186">Text value</span></span>

<span data-ttu-id="51ec1-187">Keine.</span><span class="sxs-lookup"><span data-stu-id="51ec1-187">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51ec1-188">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51ec1-188">Remarks</span></span>

<span data-ttu-id="51ec1-189">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="51ec1-189">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="51ec1-190">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="51ec1-190">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51ec1-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="51ec1-191">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="51ec1-192">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="51ec1-192">Schema Name</span></span>  <br/> |<span data-ttu-id="51ec1-193">Schematypen</span><span class="sxs-lookup"><span data-stu-id="51ec1-193">Types schema</span></span>  <br/> |
|<span data-ttu-id="51ec1-194">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="51ec1-194">Validation File</span></span>  <br/> |<span data-ttu-id="51ec1-195">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="51ec1-195">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="51ec1-196">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="51ec1-196">Can be Empty</span></span>  <br/> |<span data-ttu-id="51ec1-197">True</span><span class="sxs-lookup"><span data-stu-id="51ec1-197">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51ec1-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51ec1-198">See also</span></span>



[<span data-ttu-id="51ec1-199">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="51ec1-199">Exceptions</span></span>](exceptions.md)


- [<span data-ttu-id="51ec1-200">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="51ec1-200">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

