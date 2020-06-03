---
title: MovedItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7d5425ab-1e75-43d1-b801-802ff5139df6
description: Das MovedItemId-Element gibt den Bezeichner des Elements an, das von der MarkAsJunk-Operation verschoben wurde.
ms.openlocfilehash: 5cf8800ec672278691348bbcd8c6c8cc7a12905b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468614"
---
# <a name="moveditemid"></a><span data-ttu-id="2efdd-103">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="2efdd-103">MovedItemId</span></span>

<span data-ttu-id="2efdd-104">Das **MovedItemId** -Element gibt den Bezeichner des Elements an, das von der **MarkAsJunk** -Operation verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="2efdd-104">The **MovedItemId** element specifies the identifier of the item that was moved by the **MarkAsJunk** operation.</span></span> 
  
```XML
<MovedItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="2efdd-105">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="2efdd-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2efdd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2efdd-106">Attributes and elements</span></span>

<span data-ttu-id="2efdd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2efdd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2efdd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2efdd-108">Attributes</span></span>

|<span data-ttu-id="2efdd-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2efdd-109">**Attribute**</span></span>|<span data-ttu-id="2efdd-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2efdd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2efdd-111">Id</span><span class="sxs-lookup"><span data-stu-id="2efdd-111">Id</span></span>  <br/> |<span data-ttu-id="2efdd-112">Der Wert des **ID-** Attributs ist der Elementbezeichner des Elements, das von der **MarkAsJunk** -Operation verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="2efdd-112">The value of the **Id** attribute is the item identifier of the item that is moved by the **MarkAsJunk** operation.</span></span> <span data-ttu-id="2efdd-113">Die Element-ID bleibt nach dem Wechsel unverändert.</span><span class="sxs-lookup"><span data-stu-id="2efdd-113">The item identifier will remain the same after the move.</span></span>  <br/> |
|<span data-ttu-id="2efdd-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="2efdd-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="2efdd-115">Der Wert des **ChangeKey** -Attributs ist der Änderungsschlüssel des verschobenen Elements.</span><span class="sxs-lookup"><span data-stu-id="2efdd-115">The value of the **ChangeKey** attribute is the change key of the moved item.</span></span> <span data-ttu-id="2efdd-116">Der Änderungsschlüssel ändert sich, nachdem das Element vom **MarkAsJunk** -Vorgang verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="2efdd-116">The change key changes after the item is moved by the **MarkAsJunk** operation.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2efdd-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2efdd-117">Child elements</span></span>

<span data-ttu-id="2efdd-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="2efdd-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2efdd-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2efdd-119">Parent elements</span></span>

[<span data-ttu-id="2efdd-120">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2efdd-120">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="2efdd-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2efdd-121">Remarks</span></span>

<span data-ttu-id="2efdd-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2efdd-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2efdd-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2efdd-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2efdd-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2efdd-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2efdd-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="2efdd-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2efdd-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2efdd-126">Schema name</span></span>  <br/> |<span data-ttu-id="2efdd-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2efdd-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2efdd-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2efdd-128">Validation file</span></span>  <br/> |<span data-ttu-id="2efdd-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2efdd-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2efdd-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2efdd-130">Can be empty</span></span>  <br/> ||
   

