---
title: EventCause (um-Webdienst)
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
description: Das EventCause-Element enthält einen Wert, der die Ursache für ein Anruf Ereignis in einer Antwort auf eine Anforderung des GetCallInfo-Vorgangs (um-Webdienst) angibt.
ms.openlocfilehash: 9d49fd4b16236d0dd87889fbbd039f2e271a5968
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458677"
---
# <a name="eventcause-um-web-service"></a><span data-ttu-id="3063e-103">EventCause (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3063e-103">EventCause (UM web service)</span></span>

<span data-ttu-id="3063e-104">Das **EventCause** -Element enthält einen Wert, der die Ursache für ein Anruf Ereignis in einer Antwort auf eine Anforderung des [GetCallInfo-Vorgangs (um-Webdienst)](getcallinfo-operation-um-web-service.md) angibt.</span><span class="sxs-lookup"><span data-stu-id="3063e-104">The **EventCause** element contains a value that indicates the cause for a call event in a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="3063e-105">GetCallInfoResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3063e-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="3063e-106">EventCause (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3063e-106">EventCause (UM web service)</span></span>](eventcause-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <EventCause/>
</GetCallInfoResponse>
```

 <span data-ttu-id="3063e-107">**UMEventCause**</span><span class="sxs-lookup"><span data-stu-id="3063e-107">**UMEventCause**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3063e-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3063e-108">Attributes and elements</span></span>

<span data-ttu-id="3063e-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3063e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3063e-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="3063e-110">Attributes</span></span>

<span data-ttu-id="3063e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3063e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3063e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3063e-112">Child elements</span></span>

<span data-ttu-id="3063e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="3063e-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3063e-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3063e-114">Parent elements</span></span>

|<span data-ttu-id="3063e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="3063e-115">**Element**</span></span>|<span data-ttu-id="3063e-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3063e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3063e-117">GetCallInfoResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3063e-117">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md) <br/> |<span data-ttu-id="3063e-118">Definiert eine Antwort auf eine [GetCallInfo-Vorgangsanforderung (um-Webdienst)](getcallinfo-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="3063e-118">Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3063e-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="3063e-119">Text value</span></span>

<span data-ttu-id="3063e-120">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3063e-120">A text value is required.</span></span> <span data-ttu-id="3063e-121">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="3063e-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="3063e-122">Keine</span><span class="sxs-lookup"><span data-stu-id="3063e-122">None</span></span>
    
- <span data-ttu-id="3063e-123">UserBusy</span><span class="sxs-lookup"><span data-stu-id="3063e-123">UserBusy</span></span>
    
- <span data-ttu-id="3063e-124">Noanswer</span><span class="sxs-lookup"><span data-stu-id="3063e-124">NoAnswer</span></span>
    
- <span data-ttu-id="3063e-125">Andere</span><span class="sxs-lookup"><span data-stu-id="3063e-125">Other</span></span>
    
## <a name="element-information"></a><span data-ttu-id="3063e-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3063e-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3063e-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="3063e-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3063e-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3063e-128">Schema Name</span></span>  <br/> |<span data-ttu-id="3063e-129">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3063e-129">Messages</span></span>  <br/> |
|<span data-ttu-id="3063e-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3063e-130">Validation File</span></span>  <br/> |<span data-ttu-id="3063e-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3063e-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3063e-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3063e-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="3063e-133">False</span><span class="sxs-lookup"><span data-stu-id="3063e-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3063e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3063e-134">See also</span></span>



[<span data-ttu-id="3063e-135">GetCallInfo-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3063e-135">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="3063e-136">GetCallInfoResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3063e-136">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)

