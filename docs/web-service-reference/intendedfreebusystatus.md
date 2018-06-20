---
title: IntendedFreeBusyStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IntendedFreeBusyStatus
api_type:
- schema
ms.assetid: 0e0fa898-69a4-4c57-8bb2-52f716b5b478
description: Das Element IntendedFreeBusyStatus stellt den gewünschten Status für den Kalenderelement, das die Besprechungsanfrage zugeordnet ist.
ms.openlocfilehash: 3254becf8c6885f7d6dc401ecf31da149e7de2d4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829945"
---
# <a name="intendedfreebusystatus"></a><span data-ttu-id="8cc5b-103">IntendedFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="8cc5b-103">IntendedFreeBusyStatus</span></span>

<span data-ttu-id="8cc5b-104">Das Element **IntendedFreeBusyStatus** stellt den gewünschten Status für den Kalenderelement, das die Besprechungsanfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8cc5b-104">The **IntendedFreeBusyStatus** element represents the intended status for the calendar item that is associated with the meeting request.</span></span> 
  
```xml
<IntendedFreeBusyStatus/>
```

 <span data-ttu-id="8cc5b-105">**LegacyFreeBusyType**</span><span class="sxs-lookup"><span data-stu-id="8cc5b-105">**LegacyFreeBusyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8cc5b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8cc5b-106">Attributes and elements</span></span>

<span data-ttu-id="8cc5b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8cc5b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8cc5b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8cc5b-108">Attributes</span></span>

<span data-ttu-id="8cc5b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8cc5b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8cc5b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8cc5b-110">Child elements</span></span>

<span data-ttu-id="8cc5b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8cc5b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8cc5b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8cc5b-112">Parent elements</span></span>

|<span data-ttu-id="8cc5b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8cc5b-113">**Element**</span></span>|<span data-ttu-id="8cc5b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8cc5b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8cc5b-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8cc5b-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8cc5b-116">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="8cc5b-116">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8cc5b-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="8cc5b-117">Text value</span></span>

<span data-ttu-id="8cc5b-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8cc5b-118">A text value is required.</span></span> <span data-ttu-id="8cc5b-119">Es folgen die möglichen Werte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="8cc5b-119">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="8cc5b-120">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="8cc5b-120">Free</span></span>
    
- <span data-ttu-id="8cc5b-121">Mit Vorbehalt</span><span class="sxs-lookup"><span data-stu-id="8cc5b-121">Tentative</span></span>
    
- <span data-ttu-id="8cc5b-122">Gebucht</span><span class="sxs-lookup"><span data-stu-id="8cc5b-122">Busy</span></span>
    
- <span data-ttu-id="8cc5b-123">ABWESEND</span><span class="sxs-lookup"><span data-stu-id="8cc5b-123">OOF</span></span>
    
- <span data-ttu-id="8cc5b-124">NoData</span><span class="sxs-lookup"><span data-stu-id="8cc5b-124">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8cc5b-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8cc5b-125">Remarks</span></span>

<span data-ttu-id="8cc5b-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8cc5b-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8cc5b-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8cc5b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8cc5b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cc5b-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8cc5b-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8cc5b-129">Schema Name</span></span>  <br/> |<span data-ttu-id="8cc5b-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8cc5b-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="8cc5b-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8cc5b-131">Validation File</span></span>  <br/> |<span data-ttu-id="8cc5b-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8cc5b-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8cc5b-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8cc5b-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="8cc5b-134">False</span><span class="sxs-lookup"><span data-stu-id="8cc5b-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8cc5b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cc5b-135">See also</span></span>



- [<span data-ttu-id="8cc5b-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8cc5b-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

