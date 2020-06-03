---
title: DateTimePrecision
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 822dc5a6-2d57-474b-8a7d-da150898e5b6
description: Das DateTimePrecision-Element gibt die Genauigkeit für zurückgegebene Datum/Uhrzeit-Werte an.
ms.openlocfilehash: 9d245dfb0123daae42ba9b9b4e98aff872b67d80
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529224"
---
# <a name="datetimeprecision"></a><span data-ttu-id="c9d53-103">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="c9d53-103">DateTimePrecision</span></span>

<span data-ttu-id="c9d53-104">Das **DateTimePrecision** -Element gibt die Genauigkeit für zurückgegebene Datum/Uhrzeit-Werte an.</span><span class="sxs-lookup"><span data-stu-id="c9d53-104">The **DateTimePrecision** element specifies the precision for returned date/time values.</span></span> 
  
```XML
<DateTimePrecision />
```

<span data-ttu-id="c9d53-105">**DateTimePrecisionType**</span><span class="sxs-lookup"><span data-stu-id="c9d53-105">**DateTimePrecisionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c9d53-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c9d53-106">Attributes and elements</span></span>

<span data-ttu-id="c9d53-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c9d53-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9d53-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c9d53-108">Attributes</span></span>

<span data-ttu-id="c9d53-109">Keine</span><span class="sxs-lookup"><span data-stu-id="c9d53-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9d53-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9d53-110">Child elements</span></span>

<span data-ttu-id="c9d53-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c9d53-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c9d53-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9d53-112">Parent elements</span></span>

<span data-ttu-id="c9d53-113">Das **DateTimePrecision** -Element befindet sich im SOAP-Header.</span><span class="sxs-lookup"><span data-stu-id="c9d53-113">The **DateTimePrecision** element is located in the SOAP header.</span></span> 
  
## <a name="text-value"></a><span data-ttu-id="c9d53-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="c9d53-114">Text value</span></span>

<span data-ttu-id="c9d53-115">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c9d53-115">A text value is required.</span></span> <span data-ttu-id="c9d53-116">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="c9d53-116">The following are the possible values:</span></span>
  
- <span data-ttu-id="c9d53-117">Sekunden</span><span class="sxs-lookup"><span data-stu-id="c9d53-117">Seconds</span></span>
    
- <span data-ttu-id="c9d53-118">Millisekunden</span><span class="sxs-lookup"><span data-stu-id="c9d53-118">Milliseconds</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9d53-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9d53-119">Remarks</span></span>

<span data-ttu-id="c9d53-120">Wenn ein SOAP-Header mit dem **DateTimePrecision** -Element auf "seconds" festgelegt wird, werden Datum/Uhrzeit-Werte an die nächsten Sekunden zurückgegeben (00:00:00).</span><span class="sxs-lookup"><span data-stu-id="c9d53-120">When a SOAP header with the **DateTimePrecision** element set to "Seconds" is used, date/time values are returned to the nearest seconds (00:00:00).</span></span> <span data-ttu-id="c9d53-121">Wenn "Millisekunden" verwendet wird, werden die Werte für Datum/Uhrzeit an die nächste Millisekunde zurückgegeben (00:00:00.0000).</span><span class="sxs-lookup"><span data-stu-id="c9d53-121">When "Milliseconds" is used, date/time values are returned to the nearest millisecond (00:00:00.0000).</span></span> 
  
<span data-ttu-id="c9d53-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c9d53-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="c9d53-123">Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c9d53-123">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9d53-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c9d53-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9d53-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9d53-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c9d53-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c9d53-126">Schema Name</span></span>  <br/> |<span data-ttu-id="c9d53-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c9d53-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="c9d53-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c9d53-128">Validation File</span></span>  <br/> |<span data-ttu-id="c9d53-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c9d53-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c9d53-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c9d53-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="c9d53-131">False</span><span class="sxs-lookup"><span data-stu-id="c9d53-131">False</span></span>  <br/> |
   

