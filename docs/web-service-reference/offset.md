---
title: Offset
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
description: Das Offset-Element beschreibt den Offset aus dem BaseOffset. Zusammen mit dem BaseOffset-Element gibt das Offset-Element an, ob es sich um eine Standard-oder Sommerzeit handelt.
ms.openlocfilehash: 74ad87026c2cb89f3b0c35218c91f81380029963
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459756"
---
# <a name="offset"></a><span data-ttu-id="d2fdc-104">Offset</span><span class="sxs-lookup"><span data-stu-id="d2fdc-104">Offset</span></span>

<span data-ttu-id="d2fdc-105">Das **Offset** -Element beschreibt den Offset aus dem [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="d2fdc-105">The **Offset** element describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="d2fdc-106">Zusammen mit dem **BaseOffset** -Element gibt das **Offset** -Element an, ob es sich um eine Standard-oder Sommerzeit handelt.</span><span class="sxs-lookup"><span data-stu-id="d2fdc-106">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard or daylight saving time.</span></span> 
  
```xml
<Offset/>
```

 <span data-ttu-id="d2fdc-107">**duration**</span><span class="sxs-lookup"><span data-stu-id="d2fdc-107">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d2fdc-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d2fdc-108">Attributes and elements</span></span>

<span data-ttu-id="d2fdc-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d2fdc-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2fdc-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d2fdc-110">Attributes</span></span>

<span data-ttu-id="d2fdc-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d2fdc-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d2fdc-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2fdc-112">Child elements</span></span>

<span data-ttu-id="d2fdc-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d2fdc-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d2fdc-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2fdc-114">Parent elements</span></span>

|<span data-ttu-id="d2fdc-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2fdc-115">**Element**</span></span>|<span data-ttu-id="d2fdc-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2fdc-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2fdc-117">Sommer</span><span class="sxs-lookup"><span data-stu-id="d2fdc-117">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="d2fdc-118">Stellt das Datum und die Uhrzeit dar, zu der sich die Zeit von Sommerzeit zu Standardzeit ändert.</span><span class="sxs-lookup"><span data-stu-id="d2fdc-118">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="d2fdc-119">Standard</span><span class="sxs-lookup"><span data-stu-id="d2fdc-119">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="d2fdc-120">Stellt das Datum und die Uhrzeit dar, zu der sich die Zeit von Sommerzeit zu Standardzeit ändert.</span><span class="sxs-lookup"><span data-stu-id="d2fdc-120">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d2fdc-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="d2fdc-121">Text value</span></span>

<span data-ttu-id="d2fdc-122">Der Textwert stellt den Offset aus koordinierter Weltzeit (Coordinated Universal Time, UTC) dar.</span><span class="sxs-lookup"><span data-stu-id="d2fdc-122">The text value represents the offset from Coordinated Universal Time (UTC).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2fdc-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2fdc-123">Remarks</span></span>

<span data-ttu-id="d2fdc-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d2fdc-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2fdc-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d2fdc-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2fdc-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2fdc-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d2fdc-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d2fdc-127">Schema Name</span></span>  <br/> |<span data-ttu-id="d2fdc-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d2fdc-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="d2fdc-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d2fdc-129">Validation File</span></span>  <br/> |<span data-ttu-id="d2fdc-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d2fdc-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d2fdc-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d2fdc-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="d2fdc-132">False</span><span class="sxs-lookup"><span data-stu-id="d2fdc-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2fdc-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2fdc-133">See also</span></span>



- [<span data-ttu-id="d2fdc-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d2fdc-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

