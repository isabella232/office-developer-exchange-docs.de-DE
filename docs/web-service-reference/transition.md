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
description: Das Transition-Element stellt einen Zeitzonenübergang dar.
ms.openlocfilehash: 05495eb4a493feedc88532cc4bc8b949493481f5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467494"
---
# <a name="transition"></a><span data-ttu-id="80e53-103">Übergang</span><span class="sxs-lookup"><span data-stu-id="80e53-103">Transition</span></span>

<span data-ttu-id="80e53-104">Das **Transition** -Element stellt einen Zeitzonenübergang dar.</span><span class="sxs-lookup"><span data-stu-id="80e53-104">The **Transition** element represents a time zone transition.</span></span> 
  
```xml
<Transition>
   <To/>
</Transition>
```

 <span data-ttu-id="80e53-105">**Transitiontype**</span><span class="sxs-lookup"><span data-stu-id="80e53-105">**TransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80e53-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="80e53-106">Attributes and elements</span></span>

<span data-ttu-id="80e53-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="80e53-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80e53-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="80e53-108">Attributes</span></span>

<span data-ttu-id="80e53-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="80e53-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80e53-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80e53-110">Child elements</span></span>

|<span data-ttu-id="80e53-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="80e53-111">**Element**</span></span>|<span data-ttu-id="80e53-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80e53-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80e53-113">To</span><span class="sxs-lookup"><span data-stu-id="80e53-113">To</span></span>](to.md) <br/> |<span data-ttu-id="80e53-114">Gibt den [Zeitraum](period.md) oder die [Transitions](transitionsgroup.md) an, der das Ziel des Zeit Zonen Übergangs darstellt.</span><span class="sxs-lookup"><span data-stu-id="80e53-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="80e53-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80e53-115">Parent elements</span></span>

|<span data-ttu-id="80e53-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="80e53-116">**Element**</span></span>|<span data-ttu-id="80e53-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80e53-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80e53-118">Übergänge</span><span class="sxs-lookup"><span data-stu-id="80e53-118">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="80e53-119">Stellt eine Auflistung von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="80e53-119">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80e53-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80e53-120">Remarks</span></span>

<span data-ttu-id="80e53-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="80e53-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80e53-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="80e53-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80e53-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="80e53-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="80e53-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="80e53-124">Schema Name</span></span>  <br/> |<span data-ttu-id="80e53-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="80e53-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="80e53-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="80e53-126">Validation File</span></span>  <br/> |<span data-ttu-id="80e53-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="80e53-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="80e53-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="80e53-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="80e53-129">False</span><span class="sxs-lookup"><span data-stu-id="80e53-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80e53-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80e53-130">See also</span></span>



- [<span data-ttu-id="80e53-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="80e53-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

