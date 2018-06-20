---
title: Versetzt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Offset
api_type:
- schema
ms.assetid: dcbb9d85-d90c-4363-b4c9-d081ad03f407
description: Das Offset-Element beschreibt den Offset aus der BaseOffset. Zusammen mit dem BaseOffset-Element identifiziert das Offset-Element an, ob die Zeit Standard- oder Sommerzeit.
ms.openlocfilehash: d85fef0d67633733f6aa1943d70413ea70a528d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830642"
---
# <a name="offset"></a><span data-ttu-id="672a2-104">Versetzt</span><span class="sxs-lookup"><span data-stu-id="672a2-104">Offset</span></span>

<span data-ttu-id="672a2-105">Das **Offset** -Element beschreibt den Offset aus der [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="672a2-105">The **Offset** element describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="672a2-106">Zusammen mit dem **BaseOffset** -Element identifiziert das **Offset** -Element an, ob die Zeit Standard- oder Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="672a2-106">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard or daylight saving time.</span></span> 
  
```xml
<Offset/>
```

 <span data-ttu-id="672a2-107">**duration**</span><span class="sxs-lookup"><span data-stu-id="672a2-107">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="672a2-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="672a2-108">Attributes and elements</span></span>

<span data-ttu-id="672a2-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="672a2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="672a2-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="672a2-110">Attributes</span></span>

<span data-ttu-id="672a2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="672a2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="672a2-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="672a2-112">Child elements</span></span>

<span data-ttu-id="672a2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="672a2-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="672a2-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="672a2-114">Parent elements</span></span>

|<span data-ttu-id="672a2-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="672a2-115">**Element**</span></span>|<span data-ttu-id="672a2-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="672a2-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="672a2-117">Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="672a2-117">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="672a2-118">Das Datum und Zeitpunkt der Änderung die Zeit von Sommerzeit auf Normalzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="672a2-118">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="672a2-119">Standard</span><span class="sxs-lookup"><span data-stu-id="672a2-119">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="672a2-120">Das Datum und Zeitpunkt der Änderung die Zeit von Sommerzeit auf Normalzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="672a2-120">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="672a2-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="672a2-121">Text value</span></span>

<span data-ttu-id="672a2-122">Der Textwert stellt den Offset von der koordinierten Weltzeit (UTC).</span><span class="sxs-lookup"><span data-stu-id="672a2-122">The text value represents the offset from Coordinated Universal Time (UTC).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="672a2-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="672a2-123">Remarks</span></span>

<span data-ttu-id="672a2-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="672a2-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="672a2-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="672a2-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="672a2-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="672a2-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="672a2-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="672a2-127">Schema Name</span></span>  <br/> |<span data-ttu-id="672a2-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="672a2-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="672a2-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="672a2-129">Validation File</span></span>  <br/> |<span data-ttu-id="672a2-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="672a2-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="672a2-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="672a2-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="672a2-132">False</span><span class="sxs-lookup"><span data-stu-id="672a2-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="672a2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="672a2-133">See also</span></span>



- [<span data-ttu-id="672a2-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="672a2-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

