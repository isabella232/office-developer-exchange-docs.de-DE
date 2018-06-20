---
title: EventCause (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EventCause
api_type:
- schema
ms.assetid: 7b3c1db8-cad4-4050-a50d-b06f065db530
description: Das EventCause-Element enthält einen Wert, der angibt, die Ursache für ein Aufrufereignis in eine Antwort auf eine GetCallInfo-Vorgang (UM-Webdienst) an.
ms.openlocfilehash: dd73d93527bebb3b522ad0a6cdae5b9faee1a6a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758277"
---
# <a name="eventcause-um-web-service"></a><span data-ttu-id="cbfe3-103">EventCause (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="cbfe3-103">EventCause (UM web service)</span></span>

<span data-ttu-id="cbfe3-104">Das **EventCause** -Element enthält einen Wert, der die Ursache für einen Anruf-Ereignis in einer Antwort auf eine Anforderung [GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md) angibt.</span><span class="sxs-lookup"><span data-stu-id="cbfe3-104">The **EventCause** element contains a value that indicates the cause for a call event in a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="cbfe3-105">GetCallInfoResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="cbfe3-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="cbfe3-106">EventCause (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="cbfe3-106">EventCause (UM web service)</span></span>](eventcause-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <EventCause/>
</GetCallInfoResponse>
```

 <span data-ttu-id="cbfe3-107">**UMEventCause**</span><span class="sxs-lookup"><span data-stu-id="cbfe3-107">**UMEventCause**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cbfe3-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cbfe3-108">Attributes and elements</span></span>

<span data-ttu-id="cbfe3-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cbfe3-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbfe3-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="cbfe3-110">Attributes</span></span>

<span data-ttu-id="cbfe3-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cbfe3-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cbfe3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cbfe3-112">Child elements</span></span>

<span data-ttu-id="cbfe3-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="cbfe3-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cbfe3-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cbfe3-114">Parent elements</span></span>

|<span data-ttu-id="cbfe3-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="cbfe3-115">**Element**</span></span>|<span data-ttu-id="cbfe3-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cbfe3-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbfe3-117">GetCallInfoResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="cbfe3-117">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md) <br/> |<span data-ttu-id="cbfe3-118">Definiert eine Antwort auf eine [GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md) an.</span><span class="sxs-lookup"><span data-stu-id="cbfe3-118">Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cbfe3-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="cbfe3-119">Text value</span></span>

<span data-ttu-id="cbfe3-120">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cbfe3-120">A text value is required.</span></span> <span data-ttu-id="cbfe3-121">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="cbfe3-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="cbfe3-122">Keine</span><span class="sxs-lookup"><span data-stu-id="cbfe3-122">None</span></span>
    
- <span data-ttu-id="cbfe3-123">UserBusy</span><span class="sxs-lookup"><span data-stu-id="cbfe3-123">UserBusy</span></span>
    
- <span data-ttu-id="cbfe3-124">NoAnswer</span><span class="sxs-lookup"><span data-stu-id="cbfe3-124">NoAnswer</span></span>
    
- <span data-ttu-id="cbfe3-125">Andere</span><span class="sxs-lookup"><span data-stu-id="cbfe3-125">Other</span></span>
    
## <a name="element-information"></a><span data-ttu-id="cbfe3-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cbfe3-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbfe3-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="cbfe3-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cbfe3-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cbfe3-128">Schema Name</span></span>  <br/> |<span data-ttu-id="cbfe3-129">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="cbfe3-129">Messages</span></span>  <br/> |
|<span data-ttu-id="cbfe3-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cbfe3-130">Validation File</span></span>  <br/> |<span data-ttu-id="cbfe3-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cbfe3-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cbfe3-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cbfe3-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="cbfe3-133">False</span><span class="sxs-lookup"><span data-stu-id="cbfe3-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cbfe3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbfe3-134">See also</span></span>



[<span data-ttu-id="cbfe3-135">GetCallInfo-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="cbfe3-135">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="cbfe3-136">GetCallInfoResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="cbfe3-136">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)

