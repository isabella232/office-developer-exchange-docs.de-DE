---
title: Status (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: Status-Element gibt den Sperrstatus für ein Postfach an.
ms.openlocfilehash: c40dc865d2b305ac86fa40d536e2d516a14260ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831579"
---
# <a name="status-holdstatustype"></a><span data-ttu-id="65c1f-103">Status (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="65c1f-103">Status (HoldStatusType)</span></span>

<span data-ttu-id="65c1f-104">**Status** -Element gibt den Sperrstatus für ein Postfach an.</span><span class="sxs-lookup"><span data-stu-id="65c1f-104">The **Status** element specifies the hold status for a mailbox.</span></span> 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 <span data-ttu-id="65c1f-105">**HoldStatusType**</span><span class="sxs-lookup"><span data-stu-id="65c1f-105">**HoldStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65c1f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="65c1f-106">Attributes and elements</span></span>

<span data-ttu-id="65c1f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="65c1f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65c1f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="65c1f-108">Attributes</span></span>

<span data-ttu-id="65c1f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="65c1f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65c1f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65c1f-110">Child elements</span></span>

<span data-ttu-id="65c1f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="65c1f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="65c1f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65c1f-112">Parent elements</span></span>

[<span data-ttu-id="65c1f-113">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="65c1f-113">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
  
## <a name="text-value"></a><span data-ttu-id="65c1f-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="65c1f-114">Text value</span></span>

<span data-ttu-id="65c1f-115">Der Textwert der **Status** -Element wird der Sperrstatus eines Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="65c1f-115">The text value of the **Status** element is the hold status of a mailbox.</span></span> <span data-ttu-id="65c1f-116">**Status** -Element kann die Werte in der folgenden Liste haben.</span><span class="sxs-lookup"><span data-stu-id="65c1f-116">The **Status** element can have the values in the following list.</span></span> 
  
> <span data-ttu-id="65c1f-117">NotOnHold - ist das Postfach nicht in der Warteschleife.</span><span class="sxs-lookup"><span data-stu-id="65c1f-117">NotOnHold - The mailbox is not on hold.</span></span>
    
> <span data-ttu-id="65c1f-118">Ausstehende - wurde das Postfach entweder platziert oder in der Warteschleife veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="65c1f-118">Pending - The mailbox is pending either being placed or released on hold.</span></span> 
    
> <span data-ttu-id="65c1f-119">Vortext - Haltebereich wurde erfolgreich an das Postfach angewendet.</span><span class="sxs-lookup"><span data-stu-id="65c1f-119">OnHold - The hold was successfully applied to the mailbox.</span></span> 
    
> <span data-ttu-id="65c1f-120">PartialHold - Haltebereich wurde erfolgreich für Postfächer, jedoch nicht für alle Postfächer angewendet.</span><span class="sxs-lookup"><span data-stu-id="65c1f-120">PartialHold - The hold was successfully applied to some mailboxes but not to all mailboxes.</span></span>
    
> <span data-ttu-id="65c1f-121">Fehler bei - konnte der Haltestatus an das Postfach anwenden.</span><span class="sxs-lookup"><span data-stu-id="65c1f-121">Failed - The hold failed to apply to the mailbox.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65c1f-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="65c1f-122">Remarks</span></span>

<span data-ttu-id="65c1f-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="65c1f-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="65c1f-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="65c1f-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65c1f-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="65c1f-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65c1f-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="65c1f-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="65c1f-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="65c1f-127">Schema name</span></span>  <br/> |<span data-ttu-id="65c1f-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="65c1f-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="65c1f-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="65c1f-129">Validation file</span></span>  <br/> |<span data-ttu-id="65c1f-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="65c1f-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="65c1f-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="65c1f-131">Can be empty</span></span>  <br/> ||
   

