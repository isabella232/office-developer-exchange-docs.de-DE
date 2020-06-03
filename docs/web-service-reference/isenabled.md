---
title: IsEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsEnabled
api_type:
- schema
ms.assetid: c7e3035e-a4ef-4c11-8cb0-214790a554ff
description: Das IsEnabled-Element gibt an, ob die Regel aktiviert ist.
ms.openlocfilehash: 7a150dc4a27cf4ff7da9825d1daae2b747088539
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455310"
---
# <a name="isenabled"></a><span data-ttu-id="4b196-103">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="4b196-103">IsEnabled</span></span>

<span data-ttu-id="4b196-104">Das **IsEnabled** -Element gibt an, ob die Regel aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4b196-104">The **IsEnabled** element indicates whether the rule is enabled.</span></span> 
  
```XML
<IsEnabled/>
```

 <span data-ttu-id="4b196-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="4b196-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4b196-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4b196-106">Attributes and elements</span></span>

<span data-ttu-id="4b196-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4b196-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b196-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4b196-108">Attributes</span></span>

<span data-ttu-id="4b196-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4b196-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4b196-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4b196-110">Child elements</span></span>

<span data-ttu-id="4b196-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4b196-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4b196-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4b196-112">Parent elements</span></span>

|<span data-ttu-id="4b196-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4b196-113">**Element**</span></span>|<span data-ttu-id="4b196-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4b196-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b196-115">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="4b196-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="4b196-116">Stellt eine Regel im Postfach des Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="4b196-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4b196-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="4b196-117">Text value</span></span>

<span data-ttu-id="4b196-118">Der Textwert **true** gibt an, dass die Regel aktiviert ist und ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4b196-118">A text value of **true** indicates that the rule is enabled and can be executed.</span></span> <span data-ttu-id="4b196-119">Der Wert **false** gibt an, dass die Regel nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4b196-119">A value of **false** indicates that the rule cannot be executed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4b196-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b196-120">Remarks</span></span>

<span data-ttu-id="4b196-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4b196-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b196-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4b196-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b196-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b196-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4b196-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4b196-124">Schema Name</span></span>  <br/> |<span data-ttu-id="4b196-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4b196-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4b196-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4b196-126">Validation File</span></span>  <br/> |<span data-ttu-id="4b196-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4b196-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4b196-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4b196-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="4b196-129">True</span><span class="sxs-lookup"><span data-stu-id="4b196-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b196-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b196-130">See also</span></span>



- [<span data-ttu-id="4b196-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4b196-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

