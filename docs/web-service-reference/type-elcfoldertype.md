---
title: Typ (ElcFolderType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6faad98f-1a92-4373-bde5-dd12af61765f
description: Das Type-Element gibt den Typ des Ordners an, der in einer Aufbewahrungsrichtlinie verwendet wird.
ms.openlocfilehash: f6fcc7942a530ada2d6e72c3e38286a7595b09ec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465107"
---
# <a name="type-elcfoldertype"></a><span data-ttu-id="2dea1-103">Typ (ElcFolderType)</span><span class="sxs-lookup"><span data-stu-id="2dea1-103">Type (ElcFolderType)</span></span>

<span data-ttu-id="2dea1-104">Das **Type** -Element gibt den Typ des Ordners an, der in einer Aufbewahrungsrichtlinie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dea1-104">The **Type** element specifies the type of folder used in a retention policy.</span></span> 
  
```XML
<Type> Calendar | Contacts | DeletedItems | Drafts | Inbox | JunkEmail | Journal | Notes | Outbox | SentItems | Tasks | All | ManagedCustomFolder | RssSubscriptions | SyncIssues | ConversationHistory | Personal | RecoverableItems | NonIpmRoot <Type>
```

 <span data-ttu-id="2dea1-105">**ElcFolderType**</span><span class="sxs-lookup"><span data-stu-id="2dea1-105">**ElcFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2dea1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2dea1-106">Attributes and elements</span></span>

<span data-ttu-id="2dea1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2dea1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2dea1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2dea1-108">Attributes</span></span>

<span data-ttu-id="2dea1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2dea1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2dea1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2dea1-110">Child elements</span></span>

<span data-ttu-id="2dea1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2dea1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2dea1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2dea1-112">Parent elements</span></span>

[<span data-ttu-id="2dea1-113">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="2dea1-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="2dea1-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="2dea1-114">Text value</span></span>

<span data-ttu-id="2dea1-115">Der Textwert des **Type** -Elements ist der Ordnertyp, der in einer Aufbewahrungsrichtlinie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dea1-115">The text value of the **Type** element is the folder type used in a retention policy.</span></span> <span data-ttu-id="2dea1-116">Der Textwert kann einer der folgenden Werte sein, die einen Standardordnertyp darstellen: Kalender, Kontakte, DeletedItems, Entwürfe, Posteingang, JunkEmail, Journal, Notizen, Postausgang, gesendete Elemente, Aufgaben, alle, ManagedCustomFolder, RssSubscriptions, SyncIssues, ConversationHistory, persönlich, RecoverableItems oder NonIpmRoot</span><span class="sxs-lookup"><span data-stu-id="2dea1-116">The text value can be one of the following values that represent a default folder type: Calendar, Contacts, DeletedItems, Drafts, Inbox, JunkEmail, Journal, Notes, Outbox, SentItems, Tasks, All, ManagedCustomFolder, RssSubscriptions, SyncIssues, ConversationHistory, Personal, RecoverableItems, or NonIpmRoot</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2dea1-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2dea1-117">Remarks</span></span>

<span data-ttu-id="2dea1-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2dea1-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2dea1-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2dea1-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2dea1-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2dea1-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2dea1-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2dea1-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2dea1-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2dea1-122">Schema name</span></span>  <br/> |<span data-ttu-id="2dea1-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2dea1-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="2dea1-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2dea1-124">Validation file</span></span>  <br/> |<span data-ttu-id="2dea1-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2dea1-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2dea1-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2dea1-126">Can be empty</span></span>  <br/> |<span data-ttu-id="2dea1-127">false</span><span class="sxs-lookup"><span data-stu-id="2dea1-127">false</span></span>  <br/> |
   

