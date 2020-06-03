---
title: Action Type (HoldActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f50449b9-e73b-43c5-af96-6433bf434dce
description: Das Action Type-Element gibt den Typ der Aktion für den Haltebereich an.
ms.openlocfilehash: 8f2796df818dac2bd285b055aa44fbcecd0de5e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457858"
---
# <a name="actiontype-holdactiontype"></a><span data-ttu-id="ba1f2-103">Action Type (HoldActionType)</span><span class="sxs-lookup"><span data-stu-id="ba1f2-103">ActionType (HoldActionType)</span></span>

<span data-ttu-id="ba1f2-104">Das **Action** Type-Element gibt den Typ der Aktion für den Haltebereich an.</span><span class="sxs-lookup"><span data-stu-id="ba1f2-104">The **ActionType** element indicates the type of action for the hold.</span></span> 
  
```XML
<ActionType> Create | Update | Remove </ActionType>
```

 <span data-ttu-id="ba1f2-105">**HoldActionType**</span><span class="sxs-lookup"><span data-stu-id="ba1f2-105">**HoldActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba1f2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ba1f2-106">Attributes and elements</span></span>

<span data-ttu-id="ba1f2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ba1f2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba1f2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ba1f2-108">Attributes</span></span>

<span data-ttu-id="ba1f2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba1f2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba1f2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba1f2-110">Child elements</span></span>

<span data-ttu-id="ba1f2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba1f2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba1f2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba1f2-112">Parent elements</span></span>

[<span data-ttu-id="ba1f2-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="ba1f2-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="ba1f2-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="ba1f2-114">Text value</span></span>

<span data-ttu-id="ba1f2-115">Der Textwert des **Action** Type-Elements ist der für ein Postfach festgelegte haltetyp.</span><span class="sxs-lookup"><span data-stu-id="ba1f2-115">The text value of the **ActionType** element is the type of hold set on a mailbox.</span></span> <span data-ttu-id="ba1f2-116">Der Textwert **Create** gibt an, dass ein Postfachspeicher erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ba1f2-116">A text value of **Create** indicates that a mailbox hold will be created.</span></span> <span data-ttu-id="ba1f2-117">Der Textwert **Update** gibt an, dass ein Postfachspeicher aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba1f2-117">A text value of **Update** indicates that a mailbox hold will be updated.</span></span> <span data-ttu-id="ba1f2-118">Der Textwert **Remove** gibt an, dass ein Post Fach Haltestatus entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ba1f2-118">A text value of **Remove** indicates that a mailbox hold will be removed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ba1f2-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba1f2-119">Remarks</span></span>

<span data-ttu-id="ba1f2-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ba1f2-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ba1f2-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ba1f2-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba1f2-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ba1f2-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba1f2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba1f2-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba1f2-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ba1f2-124">Schema name</span></span>  <br/> |<span data-ttu-id="ba1f2-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ba1f2-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="ba1f2-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ba1f2-126">Validation file</span></span>  <br/> |<span data-ttu-id="ba1f2-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ba1f2-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba1f2-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ba1f2-128">Can be empty</span></span>  <br/> |<span data-ttu-id="ba1f2-129">False</span><span class="sxs-lookup"><span data-stu-id="ba1f2-129">false</span></span>  <br/> |
   

