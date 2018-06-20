---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: Das SeekToConditionPageItemView-Element identifiziert die Bedingung, die zur Identifizierung der am Ende von einer Suche, der Startindex für eine Suche, die maximale Einträge zurückgegeben und die Suche erfahren Sie, wie eine Suche FindItem oder FindConversation verwendet wird.
ms.openlocfilehash: e95246079f8c6e7acffac1dabb278895265767d9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831328"
---
# <a name="seektoconditionpageitemview"></a><span data-ttu-id="c1f62-103">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="c1f62-103">SeekToConditionPageItemView</span></span>

<span data-ttu-id="c1f62-104">Das **SeekToConditionPageItemView** -Element identifiziert die Bedingung, die das Ende einer Suche, der Startindex für eine Suche, die maximale Einträge zurückgegeben und die Richtung der Suche für einen **FindItem** oder **FindConversation identifiziert **suchen.</span><span class="sxs-lookup"><span data-stu-id="c1f62-104">The **SeekToConditionPageItemView** element identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span> 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 <span data-ttu-id="c1f62-105">**SeekToConditionPageViewType**</span><span class="sxs-lookup"><span data-stu-id="c1f62-105">**SeekToConditionPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1f62-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c1f62-106">Attributes and elements</span></span>

<span data-ttu-id="c1f62-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1f62-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1f62-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1f62-108">Attributes</span></span>

|<span data-ttu-id="c1f62-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c1f62-109">**Attribute**</span></span>|<span data-ttu-id="c1f62-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1f62-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1f62-111">Basispunkt</span><span class="sxs-lookup"><span data-stu-id="c1f62-111">BasePoint</span></span>  <br/> |<span data-ttu-id="c1f62-112">Der Textwert des **Basispunkt** -Attributs ist der Basiskalender aus, in dem die Suche beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="c1f62-112">The text value of the **BasePoint** attribute is the base point from where the search will start.</span></span> <span data-ttu-id="c1f62-113">Der **Anfang** ein Textwerts gibt an, dass die Suche am Anfang des Resultsets gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c1f62-113">A text value of **Beginning** indicates that the search will start at the beginning of the result set.</span></span> <span data-ttu-id="c1f62-114">**Ende** ein Textwerts gibt an, dass die Suche am Ende des Resultsets gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c1f62-114">A text value of **End** indicates that the search will start at the end of the result set.</span></span>  <br/> |
|<span data-ttu-id="c1f62-115">"MaxEntriesReturned"</span><span class="sxs-lookup"><span data-stu-id="c1f62-115">MaxEntriesReturned</span></span>  <br/> |<span data-ttu-id="c1f62-116">Der Textwert des Attributs **"MaxEntriesReturned"** ist die maximale Anzahl der Elemente, die in einem Resultset zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="c1f62-116">The text value of the **MaxEntriesReturned** attribute is the maximum number of items that can be returned in a result set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1f62-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1f62-117">Child elements</span></span>

[<span data-ttu-id="c1f62-118">Bedingung (RestrictionType)</span><span class="sxs-lookup"><span data-stu-id="c1f62-118">Condition (RestrictionType)</span></span>](condition-restrictiontype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="c1f62-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1f62-119">Parent elements</span></span>

<span data-ttu-id="c1f62-120">[FindConversation](findconversation.md) | [FindItem](finditem.md)</span><span class="sxs-lookup"><span data-stu-id="c1f62-120">[FindConversation](findconversation.md) | [FindItem](finditem.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1f62-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1f62-121">Remarks</span></span>

<span data-ttu-id="c1f62-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c1f62-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c1f62-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c1f62-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1f62-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c1f62-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1f62-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1f62-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c1f62-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c1f62-126">Schema name</span></span>  <br/> |<span data-ttu-id="c1f62-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c1f62-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c1f62-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c1f62-128">Validation file</span></span>  <br/> |<span data-ttu-id="c1f62-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c1f62-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c1f62-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c1f62-130">Can be empty</span></span>  <br/> |<span data-ttu-id="c1f62-131">false</span><span class="sxs-lookup"><span data-stu-id="c1f62-131">false</span></span>  <br/> |
   

