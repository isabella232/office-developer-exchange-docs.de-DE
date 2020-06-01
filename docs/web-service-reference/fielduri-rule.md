---
title: FieldUri (Regel)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecdea78-de9c-48be-ae31-03877feafeec
description: Das FieldURI-Element gibt den URI für das Regel Feld an, das den Validierungsfehler verursacht hat.
ms.openlocfilehash: 3d88efdf951af580f81b5e2e7a544dcdf70ea830
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461247"
---
# <a name="fielduri-rule"></a><span data-ttu-id="61f49-103">FieldUri (Regel)</span><span class="sxs-lookup"><span data-stu-id="61f49-103">FieldUri (Rule)</span></span>

<span data-ttu-id="61f49-104">Das **FieldURI** -Element gibt den URI für das Regel Feld an, das den Validierungsfehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="61f49-104">The **FieldURI** element specifies the URI to the rule field that caused the validation error.</span></span> 
  
```XML
<FieldURI/>
```

 <span data-ttu-id="61f49-105">**RuleFieldURIType**</span><span class="sxs-lookup"><span data-stu-id="61f49-105">**RuleFieldURIType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61f49-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="61f49-106">Attributes and elements</span></span>

<span data-ttu-id="61f49-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="61f49-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61f49-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="61f49-108">Attributes</span></span>

<span data-ttu-id="61f49-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="61f49-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61f49-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61f49-110">Child elements</span></span>

<span data-ttu-id="61f49-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="61f49-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="61f49-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61f49-112">Parent elements</span></span>

|<span data-ttu-id="61f49-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="61f49-113">**Element**</span></span>|<span data-ttu-id="61f49-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61f49-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61f49-115">Fehler</span><span class="sxs-lookup"><span data-stu-id="61f49-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="61f49-116">Stellt einen einzelnen Validierungsfehler für einen bestimmten Regel Eigenschaftswert, einen Prädikateigenschaftswert oder einen Action-Eigenschaftswert dar.</span><span class="sxs-lookup"><span data-stu-id="61f49-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="61f49-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="61f49-117">Text value</span></span>

<span data-ttu-id="61f49-118">Der Textwert für dieses Element ist auf eine der folgenden Zeichenfolgen beschränkt:</span><span class="sxs-lookup"><span data-stu-id="61f49-118">The text value for this element is restricted to one of the following strings:</span></span>
  
- <span data-ttu-id="61f49-119">RuleId</span><span class="sxs-lookup"><span data-stu-id="61f49-119">RuleId</span></span>
    
- <span data-ttu-id="61f49-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="61f49-120">DisplayName</span></span>
    
- <span data-ttu-id="61f49-121">Priorität</span><span class="sxs-lookup"><span data-stu-id="61f49-121">Priority</span></span>
    
- <span data-ttu-id="61f49-122">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="61f49-122">IsNotSupported</span></span>
    
- <span data-ttu-id="61f49-123">Aktionen</span><span class="sxs-lookup"><span data-stu-id="61f49-123">Actions</span></span>
    
- <span data-ttu-id="61f49-124">Bedingung: Kategorien</span><span class="sxs-lookup"><span data-stu-id="61f49-124">Condition:Categories</span></span>
    
- <span data-ttu-id="61f49-125">Bedingung: ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-125">Condition:ContainsBodyStrings</span></span>
    
- <span data-ttu-id="61f49-126">Bedingung: ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-126">Condition:ContainsHeaderStrings</span></span>
    
- <span data-ttu-id="61f49-127">Bedingung: ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-127">Condition:ContainsRecipientStrings</span></span>
    
- <span data-ttu-id="61f49-128">Bedingung: ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-128">Condition:ContainsSenderStrings</span></span>
    
- <span data-ttu-id="61f49-129">Bedingung: ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-129">Condition:ContainsSubjectOrBodyStrings</span></span>
    
- <span data-ttu-id="61f49-130">Bedingung: ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-130">Condition:ContainsSubjectStrings</span></span>
    
- <span data-ttu-id="61f49-131">Bedingung: FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="61f49-131">Condition:FlaggedForAction</span></span>
    
- <span data-ttu-id="61f49-132">Bedingung: FromAddresses</span><span class="sxs-lookup"><span data-stu-id="61f49-132">Condition:FromAddresses</span></span>
    
- <span data-ttu-id="61f49-133">Bedingung: FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="61f49-133">Condition:FromConnectedAccounts</span></span>
    
- <span data-ttu-id="61f49-134">Bedingung: hasattachments</span><span class="sxs-lookup"><span data-stu-id="61f49-134">Condition:HasAttachments</span></span>
    
- <span data-ttu-id="61f49-135">Bedingung: Wichtigkeit</span><span class="sxs-lookup"><span data-stu-id="61f49-135">Condition:Importance</span></span>
    
- <span data-ttu-id="61f49-136">Bedingung: IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="61f49-136">Condition:IsApprovalRequest</span></span>
    
- <span data-ttu-id="61f49-137">Bedingung: IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="61f49-137">Condition:IsAutomaticForward</span></span>
    
- <span data-ttu-id="61f49-138">Bedingung: IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="61f49-138">Condition:IsAutomaticReply</span></span>
    
- <span data-ttu-id="61f49-139">Bedingung: IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="61f49-139">Condition:IsEncrypted</span></span>
    
- <span data-ttu-id="61f49-140">Bedingung: IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="61f49-140">Condition:IsMeetingRequest</span></span>
    
- <span data-ttu-id="61f49-141">Bedingung: IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="61f49-141">Condition:IsMeetingResponse</span></span>
    
- <span data-ttu-id="61f49-142">Bedingung: IsNDR</span><span class="sxs-lookup"><span data-stu-id="61f49-142">Condition:IsNDR</span></span>
    
- <span data-ttu-id="61f49-143">Bedingung: IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="61f49-143">Condition:IsPermissionControlled</span></span>
    
- <span data-ttu-id="61f49-144">Bedingung: IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="61f49-144">Condition:IsReadReceipt</span></span>
    
- <span data-ttu-id="61f49-145">Bedingung: IsSigned</span><span class="sxs-lookup"><span data-stu-id="61f49-145">Condition:IsSigned</span></span>
    
- <span data-ttu-id="61f49-146">Bedingung: isvoicemail</span><span class="sxs-lookup"><span data-stu-id="61f49-146">Condition:IsVoicemail</span></span>
    
- <span data-ttu-id="61f49-147">Bedingung: ItemClasses</span><span class="sxs-lookup"><span data-stu-id="61f49-147">Condition:ItemClasses</span></span>
    
- <span data-ttu-id="61f49-148">Bedingung: MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="61f49-148">Condition:MessageClassifications</span></span>
    
- <span data-ttu-id="61f49-149">Bedingung: NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="61f49-149">Condition:NotSentToMe</span></span>
    
- <span data-ttu-id="61f49-150">Bedingung: SentCcMe</span><span class="sxs-lookup"><span data-stu-id="61f49-150">Condition:SentCcMe</span></span>
    
- <span data-ttu-id="61f49-151">Bedingung: SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="61f49-151">Condition:SentOnlyToMe</span></span>
    
- <span data-ttu-id="61f49-152">Bedingung: SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="61f49-152">Condition:SentToAddresses</span></span>
    
- <span data-ttu-id="61f49-153">Bedingung: SentToMe</span><span class="sxs-lookup"><span data-stu-id="61f49-153">Condition:SentToMe</span></span>
    
- <span data-ttu-id="61f49-154">Bedingung: SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="61f49-154">Condition:SentToOrCcMe</span></span>
    
- <span data-ttu-id="61f49-155">Bedingung: Empfindlichkeit</span><span class="sxs-lookup"><span data-stu-id="61f49-155">Condition:Sensitivity</span></span>
    
- <span data-ttu-id="61f49-156">Bedingung: WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="61f49-156">Condition:WithinDateRange</span></span>
    
- <span data-ttu-id="61f49-157">Bedingung: WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="61f49-157">Condition:WithinSizeRange</span></span>
    
- <span data-ttu-id="61f49-158">Ausnahme: Kategorien</span><span class="sxs-lookup"><span data-stu-id="61f49-158">Exception:Categories</span></span>
    
- <span data-ttu-id="61f49-159">Ausnahme: ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-159">Exception:ContainsBodyStrings</span></span>
    
- <span data-ttu-id="61f49-160">Ausnahme: ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-160">Exception:ContainsHeaderStrings</span></span>
    
- <span data-ttu-id="61f49-161">Ausnahme: ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-161">Exception:ContainsRecipientStrings</span></span>
    
- <span data-ttu-id="61f49-162">Ausnahme: ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-162">Exception:ContainsSenderStrings</span></span>
    
- <span data-ttu-id="61f49-163">Ausnahme: ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-163">Exception:ContainsSubjectOrBodyStrings</span></span>
    
- <span data-ttu-id="61f49-164">Ausnahme: ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="61f49-164">Exception:ContainsSubjectStrings</span></span>
    
- <span data-ttu-id="61f49-165">Ausnahme: FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="61f49-165">Exception:FlaggedForAction</span></span>
    
- <span data-ttu-id="61f49-166">Ausnahme: FromAddresses</span><span class="sxs-lookup"><span data-stu-id="61f49-166">Exception:FromAddresses</span></span>
    
- <span data-ttu-id="61f49-167">Ausnahme: FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="61f49-167">Exception:FromConnectedAccounts</span></span>
    
- <span data-ttu-id="61f49-168">Ausnahme: hasattachments</span><span class="sxs-lookup"><span data-stu-id="61f49-168">Exception:HasAttachments</span></span>
    
- <span data-ttu-id="61f49-169">Ausnahme: Wichtigkeit</span><span class="sxs-lookup"><span data-stu-id="61f49-169">Exception:Importance</span></span>
    
- <span data-ttu-id="61f49-170">Ausnahme: IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="61f49-170">Exception:IsApprovalRequest</span></span>
    
- <span data-ttu-id="61f49-171">Ausnahme: IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="61f49-171">Exception:IsAutomaticForward</span></span>
    
- <span data-ttu-id="61f49-172">Ausnahme: IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="61f49-172">Exception:IsAutomaticReply</span></span>
    
- <span data-ttu-id="61f49-173">Ausnahme: IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="61f49-173">Exception:IsEncrypted</span></span>
    
- <span data-ttu-id="61f49-174">Ausnahme: IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="61f49-174">Exception:IsMeetingRequest</span></span>
    
- <span data-ttu-id="61f49-175">Ausnahme: IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="61f49-175">Exception:IsMeetingResponse</span></span>
    
- <span data-ttu-id="61f49-176">Ausnahme: IsNDR</span><span class="sxs-lookup"><span data-stu-id="61f49-176">Exception:IsNDR</span></span>
    
- <span data-ttu-id="61f49-177">Ausnahme: IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="61f49-177">Exception:IsPermissionControlled</span></span>
    
- <span data-ttu-id="61f49-178">Ausnahme: IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="61f49-178">Exception:IsReadReceipt</span></span>
    
- <span data-ttu-id="61f49-179">Ausnahme: IsSigned</span><span class="sxs-lookup"><span data-stu-id="61f49-179">Exception:IsSigned</span></span>
    
- <span data-ttu-id="61f49-180">Ausnahme: isvoicemail</span><span class="sxs-lookup"><span data-stu-id="61f49-180">Exception:IsVoicemail</span></span>
    
- <span data-ttu-id="61f49-181">Ausnahme: ItemClasses</span><span class="sxs-lookup"><span data-stu-id="61f49-181">Exception:ItemClasses</span></span>
    
- <span data-ttu-id="61f49-182">Ausnahme: MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="61f49-182">Exception:MessageClassifications</span></span>
    
- <span data-ttu-id="61f49-183">Ausnahme: NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="61f49-183">Exception:NotSentToMe</span></span>
    
- <span data-ttu-id="61f49-184">Ausnahme: SentCcMe</span><span class="sxs-lookup"><span data-stu-id="61f49-184">Exception:SentCcMe</span></span>
    
- <span data-ttu-id="61f49-185">Ausnahme: SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="61f49-185">Exception:SentOnlyToMe</span></span>
    
- <span data-ttu-id="61f49-186">Ausnahme: SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="61f49-186">Exception:SentToAddresses</span></span>
    
- <span data-ttu-id="61f49-187">Ausnahme: SentToMe</span><span class="sxs-lookup"><span data-stu-id="61f49-187">Exception:SentToMe</span></span>
    
- <span data-ttu-id="61f49-188">Ausnahme: SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="61f49-188">Exception:SentToOrCcMe</span></span>
    
- <span data-ttu-id="61f49-189">Ausnahme: Empfindlichkeit</span><span class="sxs-lookup"><span data-stu-id="61f49-189">Exception:Sensitivity</span></span>
    
- <span data-ttu-id="61f49-190">Ausnahme: WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="61f49-190">Exception:WithinDateRange</span></span>
    
- <span data-ttu-id="61f49-191">Ausnahme: WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="61f49-191">Exception:WithinSizeRange</span></span>
    
- <span data-ttu-id="61f49-192">Aktion: AssignCategories</span><span class="sxs-lookup"><span data-stu-id="61f49-192">Action:AssignCategories</span></span>
    
- <span data-ttu-id="61f49-193">Aktion: CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="61f49-193">Action:CopyToFolder</span></span>
    
- <span data-ttu-id="61f49-194">Aktion: Löschen</span><span class="sxs-lookup"><span data-stu-id="61f49-194">Action:Delete</span></span>
    
- <span data-ttu-id="61f49-195">Aktion: ForwardAsAttachmentToRecipients</span><span class="sxs-lookup"><span data-stu-id="61f49-195">Action:ForwardAsAttachmentToRecipients</span></span>
    
- <span data-ttu-id="61f49-196">Aktion: ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="61f49-196">Action:ForwardToRecipients</span></span>
    
- <span data-ttu-id="61f49-197">Aktion: MarkImportance</span><span class="sxs-lookup"><span data-stu-id="61f49-197">Action:MarkImportance</span></span>
    
- <span data-ttu-id="61f49-198">Aktion: MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="61f49-198">Action:MarkAsRead</span></span>
    
- <span data-ttu-id="61f49-199">Aktion: MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="61f49-199">Action:MoveToFolder</span></span>
    
- <span data-ttu-id="61f49-200">Aktion: PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="61f49-200">Action:PermanentDelete</span></span>
    
- <span data-ttu-id="61f49-201">Aktion: RedirectToRecipients</span><span class="sxs-lookup"><span data-stu-id="61f49-201">Action:RedirectToRecipients</span></span>
    
- <span data-ttu-id="61f49-202">Aktion: SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="61f49-202">Action:SendSMSAlertToRecipients</span></span>
    
- <span data-ttu-id="61f49-203">Aktion: ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="61f49-203">Action:ServerReplyWithMessage</span></span>
    
- <span data-ttu-id="61f49-204">Aktion: StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="61f49-204">Action:StopProcessingRules</span></span>
    
- <span data-ttu-id="61f49-205">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="61f49-205">IsEnabled</span></span>
    
- <span data-ttu-id="61f49-206">IsInError</span><span class="sxs-lookup"><span data-stu-id="61f49-206">IsInError</span></span>
    
- <span data-ttu-id="61f49-207">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="61f49-207">Conditions</span></span>
    
- <span data-ttu-id="61f49-208">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="61f49-208">Exceptions</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61f49-209">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61f49-209">Remarks</span></span>

<span data-ttu-id="61f49-210">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="61f49-210">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61f49-211">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="61f49-211">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61f49-212">Namespace</span><span class="sxs-lookup"><span data-stu-id="61f49-212">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="61f49-213">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="61f49-213">Schema Name</span></span>  <br/> |<span data-ttu-id="61f49-214">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="61f49-214">Messages schema</span></span>  <br/> |
|<span data-ttu-id="61f49-215">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="61f49-215">Validation File</span></span>  <br/> |<span data-ttu-id="61f49-216">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="61f49-216">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="61f49-217">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="61f49-217">Can be Empty</span></span>  <br/> |<span data-ttu-id="61f49-218">False</span><span class="sxs-lookup"><span data-stu-id="61f49-218">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61f49-219">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61f49-219">See also</span></span>



- [<span data-ttu-id="61f49-220">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="61f49-220">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

