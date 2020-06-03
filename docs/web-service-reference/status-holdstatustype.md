---
title: Status (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: Das Status-Element gibt den Aufbewahrungs Status für ein Postfach an.
ms.openlocfilehash: cecfdfaf67b00b6f8cf02188e7a4df7062a732e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459987"
---
# <a name="status-holdstatustype"></a><span data-ttu-id="167be-103">Status (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="167be-103">Status (HoldStatusType)</span></span>

<span data-ttu-id="167be-104">Das **Status** -Element gibt den Aufbewahrungs Status für ein Postfach an.</span><span class="sxs-lookup"><span data-stu-id="167be-104">The **Status** element specifies the hold status for a mailbox.</span></span> 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 <span data-ttu-id="167be-105">**HoldStatusType**</span><span class="sxs-lookup"><span data-stu-id="167be-105">**HoldStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="167be-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="167be-106">Attributes and elements</span></span>

<span data-ttu-id="167be-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="167be-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="167be-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="167be-108">Attributes</span></span>

<span data-ttu-id="167be-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="167be-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="167be-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="167be-110">Child elements</span></span>

<span data-ttu-id="167be-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="167be-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="167be-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="167be-112">Parent elements</span></span>

[<span data-ttu-id="167be-113">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="167be-113">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
  
## <a name="text-value"></a><span data-ttu-id="167be-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="167be-114">Text value</span></span>

<span data-ttu-id="167be-115">Der Textwert des **Status** -Elements ist der Aufbewahrungs Status eines Postfachs.</span><span class="sxs-lookup"><span data-stu-id="167be-115">The text value of the **Status** element is the hold status of a mailbox.</span></span> <span data-ttu-id="167be-116">Das **Status** -Element kann die Werte in der folgenden Liste aufweisen.</span><span class="sxs-lookup"><span data-stu-id="167be-116">The **Status** element can have the values in the following list.</span></span> 
  
> <span data-ttu-id="167be-117">NotOnHold – das Postfach ist nicht in der Warteschleife.</span><span class="sxs-lookup"><span data-stu-id="167be-117">NotOnHold - The mailbox is not on hold.</span></span>
    
> <span data-ttu-id="167be-118">Ausstehend – das Postfach wird ausstehend oder in der Warteschleife freigegeben.</span><span class="sxs-lookup"><span data-stu-id="167be-118">Pending - The mailbox is pending either being placed or released on hold.</span></span> 
    
> <span data-ttu-id="167be-119">OnHold – der Aufbewahrungsort wurde erfolgreich auf das Postfach angewendet.</span><span class="sxs-lookup"><span data-stu-id="167be-119">OnHold - The hold was successfully applied to the mailbox.</span></span> 
    
> <span data-ttu-id="167be-120">PartialHold – der Aufbewahrungsort wurde erfolgreich auf einige Postfächer angewendet, jedoch nicht auf alle Postfächer.</span><span class="sxs-lookup"><span data-stu-id="167be-120">PartialHold - The hold was successfully applied to some mailboxes but not to all mailboxes.</span></span>
    
> <span data-ttu-id="167be-121">Fehler: der Haltestatus konnte nicht auf das Postfach angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="167be-121">Failed - The hold failed to apply to the mailbox.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="167be-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="167be-122">Remarks</span></span>

<span data-ttu-id="167be-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="167be-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="167be-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="167be-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="167be-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="167be-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="167be-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="167be-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="167be-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="167be-127">Schema name</span></span>  <br/> |<span data-ttu-id="167be-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="167be-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="167be-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="167be-129">Validation file</span></span>  <br/> |<span data-ttu-id="167be-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="167be-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="167be-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="167be-131">Can be empty</span></span>  <br/> ||
   

