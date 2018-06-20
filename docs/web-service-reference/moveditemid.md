---
title: MovedItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7d5425ab-1e75-43d1-b801-802ff5139df6
description: Das MovedItemId-Element gibt den Bezeichner des Elements, das mit einem Vorgang MarkAsJunk verschoben wurde.
ms.openlocfilehash: 17e20e8ca81f97b419fc4a2b413e21322e828ec9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830484"
---
# <a name="moveditemid"></a><span data-ttu-id="323c4-103">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="323c4-103">MovedItemId</span></span>

<span data-ttu-id="323c4-104">Das **MovedItemId** -Element gibt den Bezeichner des Elements, das mit einem Vorgang **MarkAsJunk** verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="323c4-104">The **MovedItemId** element specifies the identifier of the item that was moved by the **MarkAsJunk** operation.</span></span> 
  
```XML
<MovedItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="323c4-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="323c4-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="323c4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="323c4-106">Attributes and elements</span></span>

<span data-ttu-id="323c4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="323c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="323c4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="323c4-108">Attributes</span></span>

|<span data-ttu-id="323c4-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="323c4-109">**Attribute**</span></span>|<span data-ttu-id="323c4-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="323c4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="323c4-111">Id</span><span class="sxs-lookup"><span data-stu-id="323c4-111">Id</span></span>  <br/> |<span data-ttu-id="323c4-112">Der Wert des **Id** -Attributs ist der Elementbezeichner des Elements, das von der Operation **MarkAsJunk** verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="323c4-112">The value of the **Id** attribute is the item identifier of the item that is moved by the **MarkAsJunk** operation.</span></span> <span data-ttu-id="323c4-113">Der Elementbezeichner bleibt unverändert nach dem verschieben.</span><span class="sxs-lookup"><span data-stu-id="323c4-113">The item identifier will remain the same after the move.</span></span>  <br/> |
|<span data-ttu-id="323c4-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="323c4-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="323c4-115">Der Wert des Attributs **ChangeKey** ist der Key ändern, der das verschobene Element.</span><span class="sxs-lookup"><span data-stu-id="323c4-115">The value of the **ChangeKey** attribute is the change key of the moved item.</span></span> <span data-ttu-id="323c4-116">Der Änderungsschlüssel geändert wird, nachdem das Element mit einem Vorgang **MarkAsJunk** verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="323c4-116">The change key changes after the item is moved by the **MarkAsJunk** operation.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="323c4-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="323c4-117">Child elements</span></span>

<span data-ttu-id="323c4-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="323c4-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="323c4-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="323c4-119">Parent elements</span></span>

[<span data-ttu-id="323c4-120">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="323c4-120">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="323c4-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="323c4-121">Remarks</span></span>

<span data-ttu-id="323c4-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="323c4-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="323c4-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="323c4-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="323c4-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="323c4-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="323c4-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="323c4-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="323c4-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="323c4-126">Schema name</span></span>  <br/> |<span data-ttu-id="323c4-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="323c4-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="323c4-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="323c4-128">Validation file</span></span>  <br/> |<span data-ttu-id="323c4-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="323c4-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="323c4-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="323c4-130">Can be empty</span></span>  <br/> ||
   

