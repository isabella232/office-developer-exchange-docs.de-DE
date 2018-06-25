---
title: SubmitTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubmitTime
api_type:
- schema
ms.assetid: 97e4b71e-f45c-4bdb-80f9-805934916c0f
description: Das SubmitTime-Element darstellt, die Zeit, zu der die Nachricht an den Server gesendet wurde.
ms.openlocfilehash: 3f19e2ac14b412ef8d1ab59eb069f0223cf782ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831617"
---
# <a name="submittime"></a><span data-ttu-id="05392-103">SubmitTime</span><span class="sxs-lookup"><span data-stu-id="05392-103">SubmitTime</span></span>

<span data-ttu-id="05392-104">Das **SubmitTime** -Element darstellt, die Zeit, zu der die Nachricht an den Server gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="05392-104">The **SubmitTime** element represents the time at which the message was sent to the server.</span></span> 
  
```XML
<SubmitTime/>
```

 <span data-ttu-id="05392-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="05392-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05392-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="05392-106">Attributes and elements</span></span>

<span data-ttu-id="05392-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="05392-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05392-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="05392-108">Attributes</span></span>

<span data-ttu-id="05392-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="05392-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05392-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05392-110">Child elements</span></span>

<span data-ttu-id="05392-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="05392-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="05392-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05392-112">Parent elements</span></span>

|<span data-ttu-id="05392-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="05392-113">**Element**</span></span>|<span data-ttu-id="05392-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05392-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05392-115">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="05392-115">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="05392-116">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="05392-116">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="05392-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="05392-117">Text value</span></span>

<span data-ttu-id="05392-118">Ein Textwert, der einen Datum/Uhrzeit darstellt ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="05392-118">A text value that represents a date/time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05392-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05392-119">Remarks</span></span>

<span data-ttu-id="05392-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="05392-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05392-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="05392-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05392-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="05392-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="05392-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="05392-123">Schema Name</span></span>  <br/> |<span data-ttu-id="05392-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="05392-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="05392-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="05392-125">Validation File</span></span>  <br/> |<span data-ttu-id="05392-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="05392-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="05392-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="05392-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="05392-128">False</span><span class="sxs-lookup"><span data-stu-id="05392-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05392-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05392-129">See also</span></span>



[<span data-ttu-id="05392-130">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="05392-130">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="05392-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="05392-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

