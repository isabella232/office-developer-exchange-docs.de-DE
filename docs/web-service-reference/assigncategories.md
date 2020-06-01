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
description: Das AssignCategories-Element stellt die Kategorien dar, die auf e-Mail-Nachrichten gestempelt werden.
ms.openlocfilehash: e2dad0e2ef46421ae92a0d2826d161e5e2af3b93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464742"
---
# <a name="assigncategories"></a><span data-ttu-id="932f6-103">AssignCategories</span><span class="sxs-lookup"><span data-stu-id="932f6-103">AssignCategories</span></span>

<span data-ttu-id="932f6-104">Das **AssignCategories** -Element stellt die Kategorien dar, die auf e-Mail-Nachrichten gestempelt werden.</span><span class="sxs-lookup"><span data-stu-id="932f6-104">The **AssignCategories** element represents the categories that are stamped on e-mail messages.</span></span> 
  
- [<span data-ttu-id="932f6-105">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="932f6-105">Rule (RuleType)</span></span>](rule-ruletype.md)
  
- [<span data-ttu-id="932f6-106">Aktionen</span><span class="sxs-lookup"><span data-stu-id="932f6-106">Actions</span></span>](actions.md)
  
```XML
<AssignCategories>
   <String/>
</AssignCategories>
```

 <span data-ttu-id="932f6-107">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="932f6-107">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="932f6-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="932f6-108">Attributes and elements</span></span>

<span data-ttu-id="932f6-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="932f6-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="932f6-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="932f6-110">Attributes</span></span>

<span data-ttu-id="932f6-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="932f6-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="932f6-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="932f6-112">Child elements</span></span>

|<span data-ttu-id="932f6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="932f6-113">**Element**</span></span>|<span data-ttu-id="932f6-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="932f6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="932f6-115">String</span><span class="sxs-lookup"><span data-stu-id="932f6-115">String</span></span>](string.md) <br/> |<span data-ttu-id="932f6-116">Enthält eine Zeichenfolge, die eine einzelne Kategorie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="932f6-116">Contains a string that identifies a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="932f6-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="932f6-117">Parent elements</span></span>

|<span data-ttu-id="932f6-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="932f6-118">**Element**</span></span>|<span data-ttu-id="932f6-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="932f6-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="932f6-120">Aktionen</span><span class="sxs-lookup"><span data-stu-id="932f6-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="932f6-121">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="932f6-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="932f6-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="932f6-122">Text value</span></span>

<span data-ttu-id="932f6-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="932f6-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="932f6-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="932f6-124">Remarks</span></span>

<span data-ttu-id="932f6-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="932f6-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="932f6-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="932f6-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="932f6-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="932f6-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="932f6-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="932f6-128">Schema Name</span></span>  <br/> |<span data-ttu-id="932f6-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="932f6-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="932f6-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="932f6-130">Validation File</span></span>  <br/> |<span data-ttu-id="932f6-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="932f6-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="932f6-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="932f6-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="932f6-133">True</span><span class="sxs-lookup"><span data-stu-id="932f6-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="932f6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="932f6-134">See also</span></span>

- [<span data-ttu-id="932f6-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="932f6-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

