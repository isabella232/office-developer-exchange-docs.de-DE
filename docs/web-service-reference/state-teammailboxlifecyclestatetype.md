---
title: State (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: Das State-Element enthält den Lebenszyklusstatus, der für ein websitepostfach festgelegt wird.
ms.openlocfilehash: 597946b48649d997f8dd57823b4e0fcc091a6f84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465163"
---
# <a name="state-teammailboxlifecyclestatetype"></a><span data-ttu-id="a3250-103">State (TeamMailboxLifecycleStateType)</span><span class="sxs-lookup"><span data-stu-id="a3250-103">State (TeamMailboxLifecycleStateType)</span></span>

<span data-ttu-id="a3250-104">Das **State** -Element enthält den Lebenszyklusstatus, der für ein websitepostfach festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a3250-104">The **State** element contains the lifecycle state that is set on a site mailbox.</span></span> 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

<span data-ttu-id="a3250-105">**TeamMailboxLifecycleStateType**</span><span class="sxs-lookup"><span data-stu-id="a3250-105">**TeamMailboxLifecycleStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a3250-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a3250-106">Attributes and elements</span></span>

<span data-ttu-id="a3250-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a3250-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3250-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a3250-108">Attributes</span></span>

<span data-ttu-id="a3250-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a3250-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a3250-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3250-110">Child elements</span></span>

<span data-ttu-id="a3250-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a3250-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a3250-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3250-112">Parent elements</span></span>

[<span data-ttu-id="a3250-113">SetTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="a3250-113">SetTeamMailbox</span></span>](setteammailbox.md)
  
## <a name="text-value"></a><span data-ttu-id="a3250-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="a3250-114">Text value</span></span>

<span data-ttu-id="a3250-115">Der Textwert des **State** -Elements ist der Lebenszyklusstatus, der für ein websitepostfach festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a3250-115">The text value of the **State** element is the lifecycle state that is set on a site mailbox.</span></span> <span data-ttu-id="a3250-116">Der Textwert **aktiv** gibt an, dass ein websitepostfach aktiv verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3250-116">A text value of **Active** indicates that a site mailbox is in active use.</span></span> <span data-ttu-id="a3250-117">Der Textwert **Closed** gibt an, dass ein websitepostfach geschlossen wurde und nicht aktiv verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3250-117">A text value of **Closed** indicates that a site mailbox has been closed and is not in active use.</span></span> <span data-ttu-id="a3250-118">Ein Textwert von **unlinked** gibt an, dass ein websitepostfach nicht mit einer webbasierten Zusammenarbeitsumgebung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a3250-118">A text value of **Unlinked** indicates that a site mailbox is not linked to a web-based collaboration environment.</span></span> <span data-ttu-id="a3250-119">Die Werte " **aktiv**", " **Closed**" und " **" PendingDelete "** " schließen sich gegenseitig aus, aber der nicht **verlinkte** Wert schließt sich nicht gegenseitig aus den anderen Werten aus.</span><span class="sxs-lookup"><span data-stu-id="a3250-119">The **Active**, **Closed**, and **PendingDelete** values are mutually exclusive, but the **Unlinked** value is not mutually exclusive of the other values.</span></span> <span data-ttu-id="a3250-120">Der Textwert **"PendingDelete"** gibt an, dass ein websitepostfach aussteht, das gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a3250-120">A text value of **PendingDelete** indicates that a site mailbox is pending deletion.</span></span> <span data-ttu-id="a3250-121">Ein websitepostfach muss geschlossen werden, bevor es als **"PendingDelete"** festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a3250-121">A site mailbox has to be closed before it can be set as **PendingDelete**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3250-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3250-122">Remarks</span></span>

<span data-ttu-id="a3250-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a3250-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a3250-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a3250-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3250-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a3250-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3250-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3250-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a3250-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a3250-127">Schema name</span></span>  <br/> |<span data-ttu-id="a3250-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a3250-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a3250-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a3250-129">Validation file</span></span>  <br/> |<span data-ttu-id="a3250-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a3250-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a3250-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a3250-131">Can be empty</span></span>  <br/> ||
   

