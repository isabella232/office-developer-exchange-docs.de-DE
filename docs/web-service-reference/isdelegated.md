---
title: Isdelegated wurde
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsDelegated
api_type:
- schema
ms.assetid: c12907db-be80-4924-9469-8e58612cf42c
description: Das isdelegated-Element gibt an, ob eine Besprechung von einem Konto verarbeitet wurde, das über Stellvertretungszugriff verfügt.
ms.openlocfilehash: 2c62b59665431d5ea203e972a506aa90afc76601
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456444"
---
# <a name="isdelegated"></a><span data-ttu-id="515ca-103">Isdelegated wurde</span><span class="sxs-lookup"><span data-stu-id="515ca-103">IsDelegated</span></span>

<span data-ttu-id="515ca-104">Das **isdelegated** -Element gibt an, ob eine Besprechung von einem Konto verarbeitet wurde, das über Stellvertretungszugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="515ca-104">The **IsDelegated** element indicates whether a meeting was handled by an account that has delegate access.</span></span> 
  
```xml
<IsDelegated/>
```

 <span data-ttu-id="515ca-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="515ca-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="515ca-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="515ca-106">Attributes and elements</span></span>

<span data-ttu-id="515ca-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="515ca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="515ca-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="515ca-108">Attributes</span></span>

<span data-ttu-id="515ca-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="515ca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="515ca-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="515ca-110">Child elements</span></span>

<span data-ttu-id="515ca-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="515ca-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="515ca-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="515ca-112">Parent elements</span></span>

|<span data-ttu-id="515ca-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="515ca-113">**Element**</span></span>|<span data-ttu-id="515ca-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="515ca-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="515ca-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="515ca-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="515ca-116">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="515ca-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="515ca-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="515ca-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="515ca-118">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="515ca-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="515ca-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="515ca-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="515ca-120">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="515ca-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="515ca-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="515ca-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="515ca-122">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="515ca-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="515ca-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="515ca-123">Text value</span></span>

<span data-ttu-id="515ca-124">Der Textwert **true** gibt an, dass die Besprechung von einem Konto verarbeitet wurde, das über Stellvertretungszugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="515ca-124">A text value of **true** indicates that the meeting was handled by an account that has delegate access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="515ca-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="515ca-125">Remarks</span></span>

<span data-ttu-id="515ca-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="515ca-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="515ca-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="515ca-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="515ca-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="515ca-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="515ca-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="515ca-129">Schema Name</span></span>  <br/> |<span data-ttu-id="515ca-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="515ca-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="515ca-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="515ca-131">Validation File</span></span>  <br/> |<span data-ttu-id="515ca-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="515ca-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="515ca-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="515ca-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="515ca-134">False</span><span class="sxs-lookup"><span data-stu-id="515ca-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="515ca-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="515ca-135">See also</span></span>



- [<span data-ttu-id="515ca-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="515ca-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

