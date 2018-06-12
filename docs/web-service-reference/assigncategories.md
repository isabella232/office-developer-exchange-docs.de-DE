---
title: AssignCategories
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AssignCategories
api_type:
- schema
ms.assetid: f5c73fed-7b00-446d-8296-71a0c86e7fc6
description: Das Element AssignCategories stellt die Kategorien, die auf E-mail-Nachrichten gekennzeichnet sind.
ms.openlocfilehash: 96c77306d649677c1be745e8cadc2886e4a84c8a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757383"
---
# <a name="assigncategories"></a><span data-ttu-id="d9ac1-103">AssignCategories</span><span class="sxs-lookup"><span data-stu-id="d9ac1-103">AssignCategories</span></span>

<span data-ttu-id="d9ac1-104">Das Element **AssignCategories** stellt die Kategorien, die auf E-mail-Nachrichten gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="d9ac1-104">The **AssignCategories** element represents the categories that are stamped on e-mail messages.</span></span> 
  
- [<span data-ttu-id="d9ac1-105">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="d9ac1-105">Rule (RuleType)</span></span>](rule-ruletype.md)
  
- [<span data-ttu-id="d9ac1-106">Aktionen</span><span class="sxs-lookup"><span data-stu-id="d9ac1-106">Actions</span></span>](actions.md)
  
```XML
<AssignCategories>
   <String/>
</AssignCategories>
```

 <span data-ttu-id="d9ac1-107">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="d9ac1-107">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9ac1-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d9ac1-108">Attributes and elements</span></span>

<span data-ttu-id="d9ac1-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d9ac1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9ac1-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d9ac1-110">Attributes</span></span>

<span data-ttu-id="d9ac1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9ac1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9ac1-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9ac1-112">Child elements</span></span>

|<span data-ttu-id="d9ac1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d9ac1-113">**Element**</span></span>|<span data-ttu-id="d9ac1-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9ac1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9ac1-115">String</span><span class="sxs-lookup"><span data-stu-id="d9ac1-115">String</span></span>](string.md) <br/> |<span data-ttu-id="d9ac1-116">Enthält eine Zeichenfolge, die eine einzelne Kategorie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d9ac1-116">Contains a string that identifies a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9ac1-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9ac1-117">Parent elements</span></span>

|<span data-ttu-id="d9ac1-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="d9ac1-118">**Element**</span></span>|<span data-ttu-id="d9ac1-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9ac1-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9ac1-120">Aktionen</span><span class="sxs-lookup"><span data-stu-id="d9ac1-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="d9ac1-121">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="d9ac1-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d9ac1-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="d9ac1-122">Text value</span></span>

<span data-ttu-id="d9ac1-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9ac1-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9ac1-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9ac1-124">Remarks</span></span>

<span data-ttu-id="d9ac1-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d9ac1-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9ac1-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d9ac1-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9ac1-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9ac1-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d9ac1-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d9ac1-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d9ac1-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d9ac1-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d9ac1-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d9ac1-130">Validation File</span></span>  <br/> |<span data-ttu-id="d9ac1-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d9ac1-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9ac1-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d9ac1-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9ac1-133">True</span><span class="sxs-lookup"><span data-stu-id="d9ac1-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9ac1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9ac1-134">See also</span></span>

- [<span data-ttu-id="d9ac1-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d9ac1-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

