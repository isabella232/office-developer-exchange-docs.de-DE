---
title: Aktionen (RuleActionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2afba70c-65f7-458c-a4e6-a2cd9bccc0f9
description: Das Actions-Element enthält eine Liste der Aktionen Posteingangsregeln zugeordnet.
ms.openlocfilehash: 8ed8095ca8b41e037c2c0dad319c9c4ab99ed2bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757303"
---
# <a name="actions-ruleactionstype"></a><span data-ttu-id="9a911-103">Aktionen (RuleActionsType)</span><span class="sxs-lookup"><span data-stu-id="9a911-103">Actions (RuleActionsType)</span></span>

<span data-ttu-id="9a911-104">Das **Actions** -Element enthält eine Liste der Aktionen Posteingangsregeln zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9a911-104">The **Actions** element contains a list of actions associated with Inbox rules.</span></span> 
  
```XML
<Actions>
   <AssignCategories/>
   <CopyToFolder/>
   <Delete/>
   <ForwardAsAttachmentToRecipients/>
   <ForwardToRecipients/>
   <MarkImportance/>
   <MarkAsRead/>
   <MoveToFolder/>
   <PermanentDelete/>
   <RedirectToRecipients/>
   <SendSMSAlertToRecipients/>
   <ServerReplyWithMessage/>
   <StopProcessingRules/>
</Actions>
```

 <span data-ttu-id="9a911-105">**RuleActionsType**</span><span class="sxs-lookup"><span data-stu-id="9a911-105">**RuleActionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9a911-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9a911-106">Attributes and elements</span></span>

<span data-ttu-id="9a911-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9a911-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a911-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9a911-108">Attributes</span></span>

<span data-ttu-id="9a911-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9a911-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9a911-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9a911-110">Child elements</span></span>

<span data-ttu-id="9a911-111">[AssignCategories](assigncategories.md) | [CopyToFolder](copytofolder.md) | [Löschen](delete.md) | [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) | [ForwardToRecipients](forwardtorecipients.md) | [MarkImportance](markimportance.md) | [MarkAsRead ](markasread.md)  |  [MoveToFolder](movetofolder.md) | [PermanentDelete](permanentdelete.md) | [RedirectToRecipients](redirecttorecipients.md) | [SendSMSAlertToRecipients](sendsmsalerttorecipients.md) | [ServerReplyWithMessage](serverreplywithmessage.md)  |  [ StopProcessingRules](stopprocessingrules.md)</span><span class="sxs-lookup"><span data-stu-id="9a911-111">[AssignCategories](assigncategories.md) | [CopyToFolder](copytofolder.md) | [Delete](delete.md) | [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) | [ForwardToRecipients](forwardtorecipients.md) | [MarkImportance](markimportance.md) | [MarkAsRead](markasread.md) | [MoveToFolder](movetofolder.md) | [PermanentDelete](permanentdelete.md) | [RedirectToRecipients](redirecttorecipients.md) | [SendSMSAlertToRecipients](sendsmsalerttorecipients.md) | [ServerReplyWithMessage](serverreplywithmessage.md) | [StopProcessingRules](stopprocessingrules.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9a911-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9a911-112">Parent elements</span></span>

[<span data-ttu-id="9a911-113">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="9a911-113">Rule (RuleType)</span></span>](rule-ruletype.md)
  
## <a name="remarks"></a><span data-ttu-id="9a911-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a911-114">Remarks</span></span>

<span data-ttu-id="9a911-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9a911-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9a911-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9a911-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a911-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9a911-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a911-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="9a911-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9a911-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9a911-119">Schema name</span></span>  <br/> |<span data-ttu-id="9a911-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9a911-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="9a911-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9a911-121">Validation file</span></span>  <br/> |<span data-ttu-id="9a911-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9a911-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9a911-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9a911-123">Can be empty</span></span>  <br/> |<span data-ttu-id="9a911-124">false</span><span class="sxs-lookup"><span data-stu-id="9a911-124">false</span></span>  <br/> |
   

