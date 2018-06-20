---
title: Übergang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Transition
api_type:
- schema
ms.assetid: 23ce171a-a9c9-47ed-a366-822777048eea
description: Transition-Element stellt einen Übergang Zeitzone dar.
ms.openlocfilehash: 5dcd2f0dae7c3df2dcf660d6fe1a41b216c67b59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839263"
---
# <a name="transition"></a><span data-ttu-id="78af3-103">Übergang</span><span class="sxs-lookup"><span data-stu-id="78af3-103">Transition</span></span>

<span data-ttu-id="78af3-104">**Transition** -Element stellt einen Übergang Zeitzone dar.</span><span class="sxs-lookup"><span data-stu-id="78af3-104">The **Transition** element represents a time zone transition.</span></span> 
  
```xml
<Transition>
   <To/>
</Transition>
```

 <span data-ttu-id="78af3-105">**TransitionType**</span><span class="sxs-lookup"><span data-stu-id="78af3-105">**TransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="78af3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="78af3-106">Attributes and elements</span></span>

<span data-ttu-id="78af3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="78af3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78af3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="78af3-108">Attributes</span></span>

<span data-ttu-id="78af3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="78af3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78af3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78af3-110">Child elements</span></span>

|<span data-ttu-id="78af3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="78af3-111">**Element**</span></span>|<span data-ttu-id="78af3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78af3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78af3-113">To</span><span class="sxs-lookup"><span data-stu-id="78af3-113">To</span></span>](to.md) <br/> |<span data-ttu-id="78af3-114">Gibt den [Zeitraum](period.md) oder [TransitionsGroup](transitionsgroup.md) , das das Ziel des Übergangs Zeitzone ist.</span><span class="sxs-lookup"><span data-stu-id="78af3-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="78af3-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78af3-115">Parent elements</span></span>

|<span data-ttu-id="78af3-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="78af3-116">**Element**</span></span>|<span data-ttu-id="78af3-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78af3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78af3-118">Übergänge</span><span class="sxs-lookup"><span data-stu-id="78af3-118">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="78af3-119">Stellt eine Auflistung der Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="78af3-119">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78af3-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="78af3-120">Remarks</span></span>

<span data-ttu-id="78af3-121">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="78af3-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78af3-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="78af3-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78af3-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="78af3-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="78af3-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="78af3-124">Schema Name</span></span>  <br/> |<span data-ttu-id="78af3-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="78af3-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="78af3-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="78af3-126">Validation File</span></span>  <br/> |<span data-ttu-id="78af3-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="78af3-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="78af3-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="78af3-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="78af3-129">False</span><span class="sxs-lookup"><span data-stu-id="78af3-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78af3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78af3-130">See also</span></span>



- [<span data-ttu-id="78af3-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="78af3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

