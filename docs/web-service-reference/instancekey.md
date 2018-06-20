---
title: InstanceKey
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb4dbe9b-aea0-4527-b7d6-e928066caf38
description: Das InstanceKey-Element gibt einen Instanzschlüssel für ein Element oder eine Unterhaltung.
ms.openlocfilehash: a0e4f9390d5dc368388b5a20e38796c6c0157a40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829943"
---
# <a name="instancekey"></a><span data-ttu-id="dc411-103">InstanceKey</span><span class="sxs-lookup"><span data-stu-id="dc411-103">InstanceKey</span></span>

<span data-ttu-id="dc411-104">Das **InstanceKey** -Element gibt einen Instanzschlüssel für ein Element oder eine Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="dc411-104">The **InstanceKey** element specifies an instance key for an item or conversation.</span></span> 
  
```XML
<InstanceKey></InstanceKey>
```

 <span data-ttu-id="dc411-105">**base64Binary**</span><span class="sxs-lookup"><span data-stu-id="dc411-105">**base64Binary**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc411-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dc411-106">Attributes and elements</span></span>

<span data-ttu-id="dc411-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dc411-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc411-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dc411-108">Attributes</span></span>

<span data-ttu-id="dc411-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dc411-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc411-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc411-110">Child elements</span></span>

<span data-ttu-id="dc411-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="dc411-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc411-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc411-112">Parent elements</span></span>

|<span data-ttu-id="dc411-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dc411-113">**Element**</span></span>|<span data-ttu-id="dc411-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc411-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc411-115">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="dc411-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="dc411-116">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="dc411-116">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="dc411-117">Element</span><span class="sxs-lookup"><span data-stu-id="dc411-117">Item</span></span>](item.md) <br/> |<span data-ttu-id="dc411-118">Stellt ein generisches Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="dc411-118">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dc411-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="dc411-119">Text value</span></span>

<span data-ttu-id="dc411-120">Der Textwert des **InstanceKey** -Elements ist die Instanzschlüssel für ein Element oder eine Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="dc411-120">The text value of the **InstanceKey** element is the instance key for an item or conversation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dc411-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc411-121">Remarks</span></span>

<span data-ttu-id="dc411-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dc411-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dc411-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dc411-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc411-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dc411-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc411-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc411-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc411-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dc411-126">Schema Name</span></span>  <br/> |<span data-ttu-id="dc411-127">Typschema</span><span class="sxs-lookup"><span data-stu-id="dc411-127">Type schema</span></span>  <br/> |
|<span data-ttu-id="dc411-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dc411-128">Validation File</span></span>  <br/> |<span data-ttu-id="dc411-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc411-129">types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc411-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="dc411-130">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="dc411-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc411-131">See also</span></span>



- [<span data-ttu-id="dc411-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dc411-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

