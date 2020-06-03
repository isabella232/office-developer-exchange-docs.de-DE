---
title: DelegationState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegationState
api_type:
- schema
ms.assetid: 9dbb83ed-1ded-48f3-8e06-2489fc8b28d5
description: Das DelegationState-Element stellt den Status einer Delegierten Aufgabe dar.
ms.openlocfilehash: b938b5a2240283c265006dd47cd6ff475ad80978
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457368"
---
# <a name="delegationstate"></a><span data-ttu-id="5c610-103">DelegationState</span><span class="sxs-lookup"><span data-stu-id="5c610-103">DelegationState</span></span>

<span data-ttu-id="5c610-104">Das **DelegationState** -Element stellt den Status einer Delegierten Aufgabe dar.</span><span class="sxs-lookup"><span data-stu-id="5c610-104">The **DelegationState** element represents the status of a delegated task.</span></span> 
  
```xml
<DelegationState/>
```

<span data-ttu-id="5c610-105">**TaskDelegateStateType**</span><span class="sxs-lookup"><span data-stu-id="5c610-105">**TaskDelegateStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5c610-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5c610-106">Attributes and elements</span></span>

<span data-ttu-id="5c610-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5c610-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c610-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5c610-108">Attributes</span></span>

<span data-ttu-id="5c610-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5c610-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c610-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c610-110">Child elements</span></span>

<span data-ttu-id="5c610-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5c610-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5c610-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c610-112">Parent elements</span></span>

|<span data-ttu-id="5c610-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c610-113">**Element**</span></span>|<span data-ttu-id="5c610-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c610-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c610-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5c610-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="5c610-116">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5c610-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5c610-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="5c610-117">Text value</span></span>

<span data-ttu-id="5c610-118">Dies ist eine schreibgeschützte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5c610-118">This is a read-only property.</span></span> <span data-ttu-id="5c610-119">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="5c610-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="5c610-120">NoMatch</span><span class="sxs-lookup"><span data-stu-id="5c610-120">NoMatch</span></span>
    
- <span data-ttu-id="5c610-121">OwnNew</span><span class="sxs-lookup"><span data-stu-id="5c610-121">OwnNew</span></span>
    
- <span data-ttu-id="5c610-122">Im Besitz</span><span class="sxs-lookup"><span data-stu-id="5c610-122">Owned</span></span>
    
- <span data-ttu-id="5c610-123">Akzeptiert</span><span class="sxs-lookup"><span data-stu-id="5c610-123">Accepted</span></span>
    
- <span data-ttu-id="5c610-124">Abgelehnt</span><span class="sxs-lookup"><span data-stu-id="5c610-124">Declined</span></span>
    
- <span data-ttu-id="5c610-125">Max</span><span class="sxs-lookup"><span data-stu-id="5c610-125">Max</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5c610-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c610-126">Remarks</span></span>

<span data-ttu-id="5c610-127">Exchange Webdienste in Microsoft Exchange Server 2007 unterstützt keine Vorgangszuordnungen.</span><span class="sxs-lookup"><span data-stu-id="5c610-127">Exchange Web Services in Microsoft Exchange Server 2007 does not support task assignments.</span></span>
  
<span data-ttu-id="5c610-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange 2007 ausgeführt wird, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5c610-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c610-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5c610-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c610-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c610-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5c610-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5c610-131">Schema Name</span></span>  <br/> |<span data-ttu-id="5c610-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5c610-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="5c610-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5c610-133">Validation File</span></span>  <br/> |<span data-ttu-id="5c610-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5c610-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5c610-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5c610-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c610-136">False</span><span class="sxs-lookup"><span data-stu-id="5c610-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c610-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c610-137">See also</span></span>

- [<span data-ttu-id="5c610-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5c610-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

