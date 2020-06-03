---
title: Actions (RuleActionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2afba70c-65f7-458c-a4e6-a2cd9bccc0f9
description: Das Actions-Element enthält eine Liste von Aktionen, die Posteingangsregeln zugeordnet sind.
ms.openlocfilehash: fbef3b69b1688d7c612af018d6a19f9ec1728066
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529679"
---
# <a name="actions-ruleactionstype"></a><span data-ttu-id="8eec6-103">Actions (RuleActionsType)</span><span class="sxs-lookup"><span data-stu-id="8eec6-103">Actions (RuleActionsType)</span></span>

<span data-ttu-id="8eec6-104">Das **Actions** -Element enthält eine Liste von Aktionen, die Posteingangsregeln zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8eec6-104">The **Actions** element contains a list of actions associated with Inbox rules.</span></span> 
  
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

 <span data-ttu-id="8eec6-105">**RuleActionsType**</span><span class="sxs-lookup"><span data-stu-id="8eec6-105">**RuleActionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8eec6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8eec6-106">Attributes and elements</span></span>

<span data-ttu-id="8eec6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8eec6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8eec6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8eec6-108">Attributes</span></span>

<span data-ttu-id="8eec6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8eec6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8eec6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8eec6-110">Child elements</span></span>

<span data-ttu-id="8eec6-111">[AssignCategories](assigncategories.md)  |  [CopyToFolder](copytofolder.md)  |  [Löschen](delete.md)  |  Sie [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md)  |  [ForwardToRecipients](forwardtorecipients.md)  |  [MarkImportance](markimportance.md)  |  [MarkAsRead](markasread.md)  |  [MoveToFolder](movetofolder.md)  |  [PermanentDelete](permanentdelete.md)  |  [RedirectToRecipients](redirecttorecipients.md)  |  [SendSMSAlertToRecipients](sendsmsalerttorecipients.md)  |  [ServerReplyWithMessage](serverreplywithmessage.md)  |  [StopProcessingRules](stopprocessingrules.md)</span><span class="sxs-lookup"><span data-stu-id="8eec6-111">[AssignCategories](assigncategories.md) | [CopyToFolder](copytofolder.md) | [Delete](delete.md) | [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) | [ForwardToRecipients](forwardtorecipients.md) | [MarkImportance](markimportance.md) | [MarkAsRead](markasread.md) | [MoveToFolder](movetofolder.md) | [PermanentDelete](permanentdelete.md) | [RedirectToRecipients](redirecttorecipients.md) | [SendSMSAlertToRecipients](sendsmsalerttorecipients.md) | [ServerReplyWithMessage](serverreplywithmessage.md) | [StopProcessingRules](stopprocessingrules.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8eec6-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8eec6-112">Parent elements</span></span>

[<span data-ttu-id="8eec6-113">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="8eec6-113">Rule (RuleType)</span></span>](rule-ruletype.md)
  
## <a name="remarks"></a><span data-ttu-id="8eec6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8eec6-114">Remarks</span></span>

<span data-ttu-id="8eec6-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8eec6-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8eec6-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8eec6-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8eec6-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8eec6-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8eec6-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="8eec6-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8eec6-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8eec6-119">Schema name</span></span>  <br/> |<span data-ttu-id="8eec6-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8eec6-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="8eec6-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8eec6-121">Validation file</span></span>  <br/> |<span data-ttu-id="8eec6-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8eec6-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8eec6-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8eec6-123">Can be empty</span></span>  <br/> |<span data-ttu-id="8eec6-124">False</span><span class="sxs-lookup"><span data-stu-id="8eec6-124">false</span></span>  <br/> |
   

