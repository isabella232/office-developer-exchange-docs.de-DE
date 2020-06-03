---
title: StartDate (Serie)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartDate
api_type:
- schema
ms.assetid: bd65ac06-b3ac-4c9b-9568-3e4dc94378e7
description: Das startdate-Element stellt das Startdatum eines periodischen Vorgangs oder Kalenderelements dar.
ms.openlocfilehash: 4514f126b1de31c64a2650b9e7cb6b7412a726c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457207"
---
# <a name="startdate-recurrence"></a><span data-ttu-id="2d86c-103">StartDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="2d86c-103">StartDate (Recurrence)</span></span>

<span data-ttu-id="2d86c-104">Das **StartDate** -Element stellt das Startdatum eines periodischen Vorgangs oder Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="2d86c-104">The **StartDate** element represents the start date of a recurring task or calendar item.</span></span> 
  
```xml
<StartDate/>
```

<span data-ttu-id="2d86c-105">**Date**</span><span class="sxs-lookup"><span data-stu-id="2d86c-105">**Date**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2d86c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2d86c-106">Attributes and elements</span></span>

<span data-ttu-id="2d86c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2d86c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d86c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2d86c-108">Attributes</span></span>

<span data-ttu-id="2d86c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2d86c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d86c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d86c-110">Child elements</span></span>

<span data-ttu-id="2d86c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2d86c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d86c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d86c-112">Parent elements</span></span>

|<span data-ttu-id="2d86c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2d86c-113">**Element**</span></span>|<span data-ttu-id="2d86c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2d86c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d86c-115">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="2d86c-115">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="2d86c-116">Beschreibt das Startdatum und das Enddatum eines Element Serienmusters.</span><span class="sxs-lookup"><span data-stu-id="2d86c-116">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="2d86c-117">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="2d86c-117">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="2d86c-118">Beschreibt das Startdatum eines Element Serienmusters, das kein definiertes Enddatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="2d86c-118">Describes the start date of an item recurrence pattern that does not have a defined end date.</span></span>  <br/> |
|[<span data-ttu-id="2d86c-119">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="2d86c-119">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="2d86c-120">Beschreibt das Startdatum und die Anzahl der Vorkommen eines wiederkehrenden Elements.</span><span class="sxs-lookup"><span data-stu-id="2d86c-120">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2d86c-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="2d86c-121">Text value</span></span>

<span data-ttu-id="2d86c-122">Ein Text-Wert, der ein Datum darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d86c-122">A text value that represents a date is required if this element is used.</span></span> <span data-ttu-id="2d86c-123">Der Wert darf nicht kleiner als Apr, 1, 1601 00:00:00 sein.</span><span class="sxs-lookup"><span data-stu-id="2d86c-123">The value cannot be less than Apr, 1, 1601 00:00:00.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2d86c-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d86c-124">Remarks</span></span>

<span data-ttu-id="2d86c-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2d86c-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d86c-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2d86c-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d86c-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d86c-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2d86c-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2d86c-128">Schema name</span></span>  <br/> |<span data-ttu-id="2d86c-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2d86c-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="2d86c-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2d86c-130">Validation file</span></span>  <br/> |<span data-ttu-id="2d86c-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2d86c-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2d86c-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2d86c-132">Can be empty</span></span>  <br/> |<span data-ttu-id="2d86c-133">False</span><span class="sxs-lookup"><span data-stu-id="2d86c-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d86c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d86c-134">See also</span></span>

- [<span data-ttu-id="2d86c-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2d86c-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

