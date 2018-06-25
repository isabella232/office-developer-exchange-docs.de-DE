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
description: DelegationState-Element stellt den Status eines delegierten Vorgangs.
ms.openlocfilehash: 00b0e41ae223f1c70f9a3a21662e8858f8690a86
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757898"
---
# <a name="delegationstate"></a><span data-ttu-id="e7c14-103">DelegationState</span><span class="sxs-lookup"><span data-stu-id="e7c14-103">DelegationState</span></span>

<span data-ttu-id="e7c14-104">**DelegationState** -Element stellt den Status eines delegierten Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e7c14-104">The **DelegationState** element represents the status of a delegated task.</span></span> 
  
```xml
<DelegationState/>
```

<span data-ttu-id="e7c14-105">**TaskDelegateStateType**</span><span class="sxs-lookup"><span data-stu-id="e7c14-105">**TaskDelegateStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e7c14-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e7c14-106">Attributes and elements</span></span>

<span data-ttu-id="e7c14-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e7c14-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7c14-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e7c14-108">Attributes</span></span>

<span data-ttu-id="e7c14-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e7c14-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7c14-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e7c14-110">Child elements</span></span>

<span data-ttu-id="e7c14-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e7c14-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e7c14-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e7c14-112">Parent elements</span></span>

|<span data-ttu-id="e7c14-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e7c14-113">**Element**</span></span>|<span data-ttu-id="e7c14-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e7c14-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7c14-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e7c14-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="e7c14-116">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e7c14-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e7c14-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="e7c14-117">Text value</span></span>

<span data-ttu-id="e7c14-118">Dies ist eine schreibgeschützte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e7c14-118">This is a read-only property.</span></span> <span data-ttu-id="e7c14-119">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="e7c14-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="e7c14-120">NoMatch</span><span class="sxs-lookup"><span data-stu-id="e7c14-120">NoMatch</span></span>
    
- <span data-ttu-id="e7c14-121">OwnNew</span><span class="sxs-lookup"><span data-stu-id="e7c14-121">OwnNew</span></span>
    
- <span data-ttu-id="e7c14-122">Gehören</span><span class="sxs-lookup"><span data-stu-id="e7c14-122">Owned</span></span>
    
- <span data-ttu-id="e7c14-123">Akzeptiert</span><span class="sxs-lookup"><span data-stu-id="e7c14-123">Accepted</span></span>
    
- <span data-ttu-id="e7c14-124">Abgelehnt</span><span class="sxs-lookup"><span data-stu-id="e7c14-124">Declined</span></span>
    
- <span data-ttu-id="e7c14-125">Max</span><span class="sxs-lookup"><span data-stu-id="e7c14-125">Max</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7c14-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e7c14-126">Remarks</span></span>

<span data-ttu-id="e7c14-127">Exchange-Webdiensten in Microsoft Exchange Server 2007 unterstützt keine vorgangszuordnungen.</span><span class="sxs-lookup"><span data-stu-id="e7c14-127">Exchange Web Services in Microsoft Exchange Server 2007 does not support task assignments.</span></span>
  
<span data-ttu-id="e7c14-128">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e7c14-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7c14-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e7c14-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7c14-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7c14-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e7c14-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e7c14-131">Schema Name</span></span>  <br/> |<span data-ttu-id="e7c14-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e7c14-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="e7c14-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e7c14-133">Validation File</span></span>  <br/> |<span data-ttu-id="e7c14-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e7c14-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e7c14-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e7c14-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="e7c14-136">False</span><span class="sxs-lookup"><span data-stu-id="e7c14-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7c14-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7c14-137">See also</span></span>

- [<span data-ttu-id="e7c14-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e7c14-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

