---
title: DateTimePrecision
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 822dc5a6-2d57-474b-8a7d-da150898e5b6
description: Das DateTimePrecision-Element gibt die Genauigkeit für zurückgegebenen Datums-/Uhrzeitwerte.
ms.openlocfilehash: 4d11598628228b41adf021adbbaa77e6348534bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757860"
---
# <a name="datetimeprecision"></a><span data-ttu-id="ef307-103">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="ef307-103">DateTimePrecision</span></span>

<span data-ttu-id="ef307-104">Das **DateTimePrecision** -Element gibt die Genauigkeit für zurückgegebenen Datums-/Uhrzeitwerte.</span><span class="sxs-lookup"><span data-stu-id="ef307-104">The **DateTimePrecision** element specifies the precision for returned date/time values.</span></span> 
  
```XML
<DateTimePrecision />
```

<span data-ttu-id="ef307-105">**DateTimePrecisionType**</span><span class="sxs-lookup"><span data-stu-id="ef307-105">**DateTimePrecisionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ef307-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ef307-106">Attributes and elements</span></span>

<span data-ttu-id="ef307-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ef307-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef307-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef307-108">Attributes</span></span>

<span data-ttu-id="ef307-109">Keine</span><span class="sxs-lookup"><span data-stu-id="ef307-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef307-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef307-110">Child elements</span></span>

<span data-ttu-id="ef307-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef307-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef307-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef307-112">Parent elements</span></span>

<span data-ttu-id="ef307-113">Das Element **DateTimePrecision** befindet sich die SOAP-Header.</span><span class="sxs-lookup"><span data-stu-id="ef307-113">The **DateTimePrecision** element is located in the SOAP header.</span></span> 
  
## <a name="text-value"></a><span data-ttu-id="ef307-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="ef307-114">Text value</span></span>

<span data-ttu-id="ef307-115">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ef307-115">A text value is required.</span></span> <span data-ttu-id="ef307-116">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="ef307-116">The following are the possible values:</span></span>
  
- <span data-ttu-id="ef307-117">Sekunden</span><span class="sxs-lookup"><span data-stu-id="ef307-117">Seconds</span></span>
    
- <span data-ttu-id="ef307-118">Millisekunden</span><span class="sxs-lookup"><span data-stu-id="ef307-118">Milliseconds</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef307-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ef307-119">Remarks</span></span>

<span data-ttu-id="ef307-120">Wenn ein SOAP-Header mit dem **DateTimePrecision** -Element "Sekunden" verwendet wird, Datum/Uhrzeit-Werte werden zurückgegeben, auf die nächsten Sekunden (00: 00:00).</span><span class="sxs-lookup"><span data-stu-id="ef307-120">When a SOAP header with the **DateTimePrecision** element set to "Seconds" is used, date/time values are returned to the nearest seconds (00:00:00).</span></span> <span data-ttu-id="ef307-121">Wenn "Millisekunden" verwendet werden, Datum/Uhrzeit-Werte werden auf die nächste Millisekunde (00:00:00.0000) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ef307-121">When "Milliseconds" is used, date/time values are returned to the nearest millisecond (00:00:00.0000).</span></span> 
  
<span data-ttu-id="ef307-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ef307-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="ef307-123">Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ef307-123">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef307-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ef307-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef307-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef307-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef307-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ef307-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ef307-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ef307-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="ef307-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ef307-128">Validation File</span></span>  <br/> |<span data-ttu-id="ef307-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ef307-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef307-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ef307-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef307-131">False</span><span class="sxs-lookup"><span data-stu-id="ef307-131">False</span></span>  <br/> |
   

