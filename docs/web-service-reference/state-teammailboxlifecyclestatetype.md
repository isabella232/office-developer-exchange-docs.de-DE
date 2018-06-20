---
title: Status (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: Das Status-Element enthält den Lebenszyklusstatus, der für ein websitepostfach festgelegt ist.
ms.openlocfilehash: accd70d36cc34e7364387b98a2e94c56b91f012f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831571"
---
# <a name="state-teammailboxlifecyclestatetype"></a><span data-ttu-id="446ec-103">Status (TeamMailboxLifecycleStateType)</span><span class="sxs-lookup"><span data-stu-id="446ec-103">State (TeamMailboxLifecycleStateType)</span></span>

<span data-ttu-id="446ec-104">Das **Status** -Element enthält den Lebenszyklusstatus, der für ein websitepostfach festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="446ec-104">The **State** element contains the lifecycle state that is set on a site mailbox.</span></span> 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

<span data-ttu-id="446ec-105">**TeamMailboxLifecycleStateType**</span><span class="sxs-lookup"><span data-stu-id="446ec-105">**TeamMailboxLifecycleStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="446ec-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="446ec-106">Attributes and elements</span></span>

<span data-ttu-id="446ec-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="446ec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="446ec-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="446ec-108">Attributes</span></span>

<span data-ttu-id="446ec-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="446ec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="446ec-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="446ec-110">Child elements</span></span>

<span data-ttu-id="446ec-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="446ec-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="446ec-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="446ec-112">Parent elements</span></span>

[<span data-ttu-id="446ec-113">SetTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="446ec-113">SetTeamMailbox</span></span>](setteammailbox.md)
  
## <a name="text-value"></a><span data-ttu-id="446ec-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="446ec-114">Text value</span></span>

<span data-ttu-id="446ec-115">Der Textwert der **State** -Elements ist die Lebenszyklusstatus, der für ein websitepostfach festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="446ec-115">The text value of the **State** element is the lifecycle state that is set on a site mailbox.</span></span> <span data-ttu-id="446ec-116">Ein Textwert der **aktiven** gibt an, dass ein websitepostfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="446ec-116">A text value of **Active** indicates that a site mailbox is in active use.</span></span> <span data-ttu-id="446ec-117">Der Textwert **geschlossen** gibt an, dass ein websitepostfach geschlossen wurde und nicht aktiv verwendet.</span><span class="sxs-lookup"><span data-stu-id="446ec-117">A text value of **Closed** indicates that a site mailbox has been closed and is not in active use.</span></span> <span data-ttu-id="446ec-118">Ein Textwert der **Unverknüpfte** gibt an, dass ein websitepostfach nicht mit einer Umgebung webbasierte Zusammenarbeit verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="446ec-118">A text value of **Unlinked** indicates that a site mailbox is not linked to a web-based collaboration environment.</span></span> <span data-ttu-id="446ec-119">Die Werte **aktiv**, **geschlossen**und **PendingDelete** schließen sich gegenseitig aus, aber der Wert **Unverknüpfte** schließen sich nicht gegenseitig aus anderen Werte.</span><span class="sxs-lookup"><span data-stu-id="446ec-119">The **Active**, **Closed**, and **PendingDelete** values are mutually exclusive, but the **Unlinked** value is not mutually exclusive of the other values.</span></span> <span data-ttu-id="446ec-120">Der Textwert **PendingDelete** gibt an, dass ein websitepostfach Löschen ausstehend ist.</span><span class="sxs-lookup"><span data-stu-id="446ec-120">A text value of **PendingDelete** indicates that a site mailbox is pending deletion.</span></span> <span data-ttu-id="446ec-121">Ein websitepostfach muss geschlossen werden, bevor es als **PendingDelete**festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="446ec-121">A site mailbox has to be closed before it can be set as **PendingDelete**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="446ec-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="446ec-122">Remarks</span></span>

<span data-ttu-id="446ec-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="446ec-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="446ec-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="446ec-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="446ec-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="446ec-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="446ec-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="446ec-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="446ec-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="446ec-127">Schema name</span></span>  <br/> |<span data-ttu-id="446ec-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="446ec-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="446ec-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="446ec-129">Validation file</span></span>  <br/> |<span data-ttu-id="446ec-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="446ec-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="446ec-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="446ec-131">Can be empty</span></span>  <br/> ||
   

