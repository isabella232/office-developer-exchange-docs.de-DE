---
title: IsOutOfDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsOutOfDate
api_type:
- schema
ms.assetid: 2b6005a6-56a9-4848-b998-32908c13e2e2
description: Das IsOutOfDate-Element gibt an, ob eine Besprechungsnachricht, Anforderung, Antwort oder Abbruch veraltet ist.
ms.openlocfilehash: 0a6b2670cc3eb260002821bab31d652177902de1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830110"
---
# <a name="isoutofdate"></a><span data-ttu-id="1e405-103">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="1e405-103">IsOutOfDate</span></span>

<span data-ttu-id="1e405-104">Das **IsOutOfDate** -Element gibt an, ob eine Besprechungsnachricht, Anforderung, Antwort oder Abbruch veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="1e405-104">The **IsOutOfDate** element indicates whether a meeting message, request, response, or cancellation is out-of-date.</span></span> 
  
```xml
<IsOutOfDate/>
```

 <span data-ttu-id="1e405-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1e405-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1e405-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1e405-106">Attributes and elements</span></span>

<span data-ttu-id="1e405-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1e405-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e405-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1e405-108">Attributes</span></span>

<span data-ttu-id="1e405-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1e405-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1e405-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e405-110">Child elements</span></span>

<span data-ttu-id="1e405-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1e405-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1e405-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e405-112">Parent elements</span></span>

|<span data-ttu-id="1e405-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1e405-113">**Element**</span></span>|<span data-ttu-id="1e405-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e405-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e405-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="1e405-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="1e405-116">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="1e405-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1e405-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="1e405-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="1e405-118">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="1e405-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1e405-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="1e405-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="1e405-120">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="1e405-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1e405-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="1e405-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="1e405-122">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="1e405-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1e405-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="1e405-123">Text value</span></span>

<span data-ttu-id="1e405-124">Der Textwert **true** gibt an, dass das Besprechungselement veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="1e405-124">A text value of **true** indicates that the meeting item is out-of-date.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1e405-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e405-125">Remarks</span></span>

<span data-ttu-id="1e405-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1e405-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e405-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1e405-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e405-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e405-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1e405-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1e405-129">Schema Name</span></span>  <br/> |<span data-ttu-id="1e405-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1e405-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="1e405-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1e405-131">Validation File</span></span>  <br/> |<span data-ttu-id="1e405-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1e405-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1e405-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1e405-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="1e405-134">False</span><span class="sxs-lookup"><span data-stu-id="1e405-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e405-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e405-135">See also</span></span>



- [<span data-ttu-id="1e405-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1e405-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

