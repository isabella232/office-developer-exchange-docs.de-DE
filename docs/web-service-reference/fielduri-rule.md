---
title: FieldUri (Regel)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecdea78-de9c-48be-ae31-03877feafeec
description: Das FieldURI-Element gibt den URI für die Regel dar, das den Validierungsfehler verursacht hat.
ms.openlocfilehash: 88ba54994625d3a950b58e900f28c986c31eddac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758411"
---
# <a name="fielduri-rule"></a><span data-ttu-id="a6905-103">FieldUri (Regel)</span><span class="sxs-lookup"><span data-stu-id="a6905-103">FieldUri (Rule)</span></span>

<span data-ttu-id="a6905-104">Das **FieldURI** -Element gibt den URI für die Regel dar, das den Validierungsfehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="a6905-104">The **FieldURI** element specifies the URI to the rule field that caused the validation error.</span></span> 
  
```XML
<FieldURI/>
```

 <span data-ttu-id="a6905-105">**RuleFieldURIType**</span><span class="sxs-lookup"><span data-stu-id="a6905-105">**RuleFieldURIType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6905-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a6905-106">Attributes and elements</span></span>

<span data-ttu-id="a6905-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a6905-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6905-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a6905-108">Attributes</span></span>

<span data-ttu-id="a6905-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a6905-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6905-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6905-110">Child elements</span></span>

<span data-ttu-id="a6905-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a6905-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a6905-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6905-112">Parent elements</span></span>

|<span data-ttu-id="a6905-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6905-113">**Element**</span></span>|<span data-ttu-id="a6905-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6905-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6905-115">Fehler</span><span class="sxs-lookup"><span data-stu-id="a6905-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="a6905-116">Stellt einen einzelnen Gültigkeitsprüfungsfehler auf eine bestimmte Regel Eigenschaftswert, Prädikat Eigenschaftswert oder Aktionswert-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a6905-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a6905-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="a6905-117">Text value</span></span>

<span data-ttu-id="a6905-118">Der Textwert für dieses Element ist auf eine der folgenden Zeichenfolgen beschränkt:</span><span class="sxs-lookup"><span data-stu-id="a6905-118">The text value for this element is restricted to one of the following strings:</span></span>
  
- <span data-ttu-id="a6905-119">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="a6905-119">RuleId</span></span>
    
- <span data-ttu-id="a6905-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="a6905-120">DisplayName</span></span>
    
- <span data-ttu-id="a6905-121">Priorität</span><span class="sxs-lookup"><span data-stu-id="a6905-121">Priority</span></span>
    
- <span data-ttu-id="a6905-122">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="a6905-122">IsNotSupported</span></span>
    
- <span data-ttu-id="a6905-123">Aktionen</span><span class="sxs-lookup"><span data-stu-id="a6905-123">Actions</span></span>
    
- <span data-ttu-id="a6905-124">Bedingung: Kategorien</span><span class="sxs-lookup"><span data-stu-id="a6905-124">Condition:Categories</span></span>
    
- <span data-ttu-id="a6905-125">Bedingung: ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-125">Condition:ContainsBodyStrings</span></span>
    
- <span data-ttu-id="a6905-126">Bedingung: ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-126">Condition:ContainsHeaderStrings</span></span>
    
- <span data-ttu-id="a6905-127">Bedingung: ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-127">Condition:ContainsRecipientStrings</span></span>
    
- <span data-ttu-id="a6905-128">Bedingung: ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-128">Condition:ContainsSenderStrings</span></span>
    
- <span data-ttu-id="a6905-129">Bedingung: ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-129">Condition:ContainsSubjectOrBodyStrings</span></span>
    
- <span data-ttu-id="a6905-130">Bedingung: ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-130">Condition:ContainsSubjectStrings</span></span>
    
- <span data-ttu-id="a6905-131">Bedingung: FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="a6905-131">Condition:FlaggedForAction</span></span>
    
- <span data-ttu-id="a6905-132">Bedingung: FromAddresses</span><span class="sxs-lookup"><span data-stu-id="a6905-132">Condition:FromAddresses</span></span>
    
- <span data-ttu-id="a6905-133">Bedingung: FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="a6905-133">Condition:FromConnectedAccounts</span></span>
    
- <span data-ttu-id="a6905-134">Bedingung: HasAttachments</span><span class="sxs-lookup"><span data-stu-id="a6905-134">Condition:HasAttachments</span></span>
    
- <span data-ttu-id="a6905-135">Bedingung: Wichtigkeit</span><span class="sxs-lookup"><span data-stu-id="a6905-135">Condition:Importance</span></span>
    
- <span data-ttu-id="a6905-136">Bedingung: IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="a6905-136">Condition:IsApprovalRequest</span></span>
    
- <span data-ttu-id="a6905-137">Bedingung: IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="a6905-137">Condition:IsAutomaticForward</span></span>
    
- <span data-ttu-id="a6905-138">Bedingung: IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="a6905-138">Condition:IsAutomaticReply</span></span>
    
- <span data-ttu-id="a6905-139">Bedingung: IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="a6905-139">Condition:IsEncrypted</span></span>
    
- <span data-ttu-id="a6905-140">Bedingung: IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a6905-140">Condition:IsMeetingRequest</span></span>
    
- <span data-ttu-id="a6905-141">Bedingung: IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="a6905-141">Condition:IsMeetingResponse</span></span>
    
- <span data-ttu-id="a6905-142">Bedingung: IsNDR</span><span class="sxs-lookup"><span data-stu-id="a6905-142">Condition:IsNDR</span></span>
    
- <span data-ttu-id="a6905-143">Bedingung: IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="a6905-143">Condition:IsPermissionControlled</span></span>
    
- <span data-ttu-id="a6905-144">Bedingung: IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="a6905-144">Condition:IsReadReceipt</span></span>
    
- <span data-ttu-id="a6905-145">Bedingung: IsSigned</span><span class="sxs-lookup"><span data-stu-id="a6905-145">Condition:IsSigned</span></span>
    
- <span data-ttu-id="a6905-146">Bedingung: IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="a6905-146">Condition:IsVoicemail</span></span>
    
- <span data-ttu-id="a6905-147">Bedingung: ItemClasses</span><span class="sxs-lookup"><span data-stu-id="a6905-147">Condition:ItemClasses</span></span>
    
- <span data-ttu-id="a6905-148">Bedingung: MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="a6905-148">Condition:MessageClassifications</span></span>
    
- <span data-ttu-id="a6905-149">Bedingung: NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="a6905-149">Condition:NotSentToMe</span></span>
    
- <span data-ttu-id="a6905-150">Bedingung: SentCcMe</span><span class="sxs-lookup"><span data-stu-id="a6905-150">Condition:SentCcMe</span></span>
    
- <span data-ttu-id="a6905-151">Bedingung: SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="a6905-151">Condition:SentOnlyToMe</span></span>
    
- <span data-ttu-id="a6905-152">Bedingung: SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="a6905-152">Condition:SentToAddresses</span></span>
    
- <span data-ttu-id="a6905-153">Bedingung: SentToMe</span><span class="sxs-lookup"><span data-stu-id="a6905-153">Condition:SentToMe</span></span>
    
- <span data-ttu-id="a6905-154">Bedingung: SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="a6905-154">Condition:SentToOrCcMe</span></span>
    
- <span data-ttu-id="a6905-155">Bedingung: Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="a6905-155">Condition:Sensitivity</span></span>
    
- <span data-ttu-id="a6905-156">Bedingung: WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="a6905-156">Condition:WithinDateRange</span></span>
    
- <span data-ttu-id="a6905-157">Bedingung: WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="a6905-157">Condition:WithinSizeRange</span></span>
    
- <span data-ttu-id="a6905-158">Ausnahme: Kategorien</span><span class="sxs-lookup"><span data-stu-id="a6905-158">Exception:Categories</span></span>
    
- <span data-ttu-id="a6905-159">Ausnahme: ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-159">Exception:ContainsBodyStrings</span></span>
    
- <span data-ttu-id="a6905-160">Ausnahme: ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-160">Exception:ContainsHeaderStrings</span></span>
    
- <span data-ttu-id="a6905-161">Ausnahme: ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-161">Exception:ContainsRecipientStrings</span></span>
    
- <span data-ttu-id="a6905-162">Ausnahme: ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-162">Exception:ContainsSenderStrings</span></span>
    
- <span data-ttu-id="a6905-163">Ausnahme: ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-163">Exception:ContainsSubjectOrBodyStrings</span></span>
    
- <span data-ttu-id="a6905-164">Ausnahme: ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="a6905-164">Exception:ContainsSubjectStrings</span></span>
    
- <span data-ttu-id="a6905-165">Ausnahme: FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="a6905-165">Exception:FlaggedForAction</span></span>
    
- <span data-ttu-id="a6905-166">Ausnahme: FromAddresses</span><span class="sxs-lookup"><span data-stu-id="a6905-166">Exception:FromAddresses</span></span>
    
- <span data-ttu-id="a6905-167">Ausnahme: FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="a6905-167">Exception:FromConnectedAccounts</span></span>
    
- <span data-ttu-id="a6905-168">Ausnahme: HasAttachments</span><span class="sxs-lookup"><span data-stu-id="a6905-168">Exception:HasAttachments</span></span>
    
- <span data-ttu-id="a6905-169">Ausnahme: Wichtigkeit</span><span class="sxs-lookup"><span data-stu-id="a6905-169">Exception:Importance</span></span>
    
- <span data-ttu-id="a6905-170">Ausnahme: IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="a6905-170">Exception:IsApprovalRequest</span></span>
    
- <span data-ttu-id="a6905-171">Ausnahme: IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="a6905-171">Exception:IsAutomaticForward</span></span>
    
- <span data-ttu-id="a6905-172">Ausnahme: IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="a6905-172">Exception:IsAutomaticReply</span></span>
    
- <span data-ttu-id="a6905-173">Ausnahme: IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="a6905-173">Exception:IsEncrypted</span></span>
    
- <span data-ttu-id="a6905-174">Ausnahme: IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a6905-174">Exception:IsMeetingRequest</span></span>
    
- <span data-ttu-id="a6905-175">Ausnahme: IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="a6905-175">Exception:IsMeetingResponse</span></span>
    
- <span data-ttu-id="a6905-176">Ausnahme: IsNDR</span><span class="sxs-lookup"><span data-stu-id="a6905-176">Exception:IsNDR</span></span>
    
- <span data-ttu-id="a6905-177">Ausnahme: IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="a6905-177">Exception:IsPermissionControlled</span></span>
    
- <span data-ttu-id="a6905-178">Ausnahme: IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="a6905-178">Exception:IsReadReceipt</span></span>
    
- <span data-ttu-id="a6905-179">Ausnahme: IsSigned</span><span class="sxs-lookup"><span data-stu-id="a6905-179">Exception:IsSigned</span></span>
    
- <span data-ttu-id="a6905-180">Ausnahme: IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="a6905-180">Exception:IsVoicemail</span></span>
    
- <span data-ttu-id="a6905-181">Ausnahme: ItemClasses</span><span class="sxs-lookup"><span data-stu-id="a6905-181">Exception:ItemClasses</span></span>
    
- <span data-ttu-id="a6905-182">Ausnahme: MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="a6905-182">Exception:MessageClassifications</span></span>
    
- <span data-ttu-id="a6905-183">Ausnahme: NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="a6905-183">Exception:NotSentToMe</span></span>
    
- <span data-ttu-id="a6905-184">Ausnahme: SentCcMe</span><span class="sxs-lookup"><span data-stu-id="a6905-184">Exception:SentCcMe</span></span>
    
- <span data-ttu-id="a6905-185">Ausnahme: SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="a6905-185">Exception:SentOnlyToMe</span></span>
    
- <span data-ttu-id="a6905-186">Ausnahme: SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="a6905-186">Exception:SentToAddresses</span></span>
    
- <span data-ttu-id="a6905-187">Ausnahme: SentToMe</span><span class="sxs-lookup"><span data-stu-id="a6905-187">Exception:SentToMe</span></span>
    
- <span data-ttu-id="a6905-188">Ausnahme: SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="a6905-188">Exception:SentToOrCcMe</span></span>
    
- <span data-ttu-id="a6905-189">Ausnahme: Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="a6905-189">Exception:Sensitivity</span></span>
    
- <span data-ttu-id="a6905-190">Ausnahme: WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="a6905-190">Exception:WithinDateRange</span></span>
    
- <span data-ttu-id="a6905-191">Ausnahme: WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="a6905-191">Exception:WithinSizeRange</span></span>
    
- <span data-ttu-id="a6905-192">Aktion: AssignCategories</span><span class="sxs-lookup"><span data-stu-id="a6905-192">Action:AssignCategories</span></span>
    
- <span data-ttu-id="a6905-193">Aktion: CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="a6905-193">Action:CopyToFolder</span></span>
    
- <span data-ttu-id="a6905-194">Löschen der Aktion:</span><span class="sxs-lookup"><span data-stu-id="a6905-194">Action:Delete</span></span>
    
- <span data-ttu-id="a6905-195">Aktion: ForwardAsAttachmentToRecipients</span><span class="sxs-lookup"><span data-stu-id="a6905-195">Action:ForwardAsAttachmentToRecipients</span></span>
    
- <span data-ttu-id="a6905-196">Aktion: ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="a6905-196">Action:ForwardToRecipients</span></span>
    
- <span data-ttu-id="a6905-197">Aktion: MarkImportance</span><span class="sxs-lookup"><span data-stu-id="a6905-197">Action:MarkImportance</span></span>
    
- <span data-ttu-id="a6905-198">Aktion: MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="a6905-198">Action:MarkAsRead</span></span>
    
- <span data-ttu-id="a6905-199">Aktion: MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="a6905-199">Action:MoveToFolder</span></span>
    
- <span data-ttu-id="a6905-200">Aktion: PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="a6905-200">Action:PermanentDelete</span></span>
    
- <span data-ttu-id="a6905-201">Aktion: RedirectToRecipients</span><span class="sxs-lookup"><span data-stu-id="a6905-201">Action:RedirectToRecipients</span></span>
    
- <span data-ttu-id="a6905-202">Aktion: SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="a6905-202">Action:SendSMSAlertToRecipients</span></span>
    
- <span data-ttu-id="a6905-203">Aktion: ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="a6905-203">Action:ServerReplyWithMessage</span></span>
    
- <span data-ttu-id="a6905-204">Aktion: StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="a6905-204">Action:StopProcessingRules</span></span>
    
- <span data-ttu-id="a6905-205">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="a6905-205">IsEnabled</span></span>
    
- <span data-ttu-id="a6905-206">IsInError</span><span class="sxs-lookup"><span data-stu-id="a6905-206">IsInError</span></span>
    
- <span data-ttu-id="a6905-207">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="a6905-207">Conditions</span></span>
    
- <span data-ttu-id="a6905-208">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="a6905-208">Exceptions</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6905-209">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a6905-209">Remarks</span></span>

<span data-ttu-id="a6905-210">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a6905-210">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6905-211">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a6905-211">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6905-212">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6905-212">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a6905-213">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a6905-213">Schema Name</span></span>  <br/> |<span data-ttu-id="a6905-214">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a6905-214">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a6905-215">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a6905-215">Validation File</span></span>  <br/> |<span data-ttu-id="a6905-216">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a6905-216">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a6905-217">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a6905-217">Can be Empty</span></span>  <br/> |<span data-ttu-id="a6905-218">False</span><span class="sxs-lookup"><span data-stu-id="a6905-218">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6905-219">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6905-219">See also</span></span>



- [<span data-ttu-id="a6905-220">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a6905-220">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

