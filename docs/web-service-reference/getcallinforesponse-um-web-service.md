---
title: GetCallInfoResponse (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfoResponse
api_type:
- schema
ms.assetid: aa5196bf-f5f3-455c-94ea-304fb7920c79
description: Das GetCallInfoResponse-Element definiert eine Antwort auf eine Anforderung des GetCallInfo-Vorgangs (um-Webdienst).
ms.openlocfilehash: 6e54ec61a9a5ebecd96bbd39dad68f8cc011b8a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461205"
---
# <a name="getcallinforesponse-um-web-service"></a><span data-ttu-id="e698a-103">GetCallInfoResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e698a-103">GetCallInfoResponse (UM web service)</span></span>

<span data-ttu-id="e698a-104">Das **GetCallInfoResponse** -Element definiert eine Antwort auf eine Anforderung des [GetCallInfo-Vorgangs (um-Webdienst)](getcallinfo-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="e698a-104">The **GetCallInfoResponse** element defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="e698a-105">GetCallInfoResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e698a-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <CallState/>
  <EventCause/>
</GetCallInfoResponse>
```

 <span data-ttu-id="e698a-106">**UMCallInfo**</span><span class="sxs-lookup"><span data-stu-id="e698a-106">**UMCallInfo**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e698a-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e698a-107">Attributes and elements</span></span>

<span data-ttu-id="e698a-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e698a-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e698a-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="e698a-109">Attributes</span></span>

<span data-ttu-id="e698a-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="e698a-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e698a-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e698a-111">Child elements</span></span>

|<span data-ttu-id="e698a-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="e698a-112">**Element**</span></span>|<span data-ttu-id="e698a-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e698a-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e698a-114">CallState</span><span class="sxs-lookup"><span data-stu-id="e698a-114">CallState</span></span>  <br/> |<span data-ttu-id="e698a-115">Enthält einen Wert, der den Status eines Anrufs angibt, für den der [GetCallInfo-Vorgang (um-Webdienst)](getcallinfo-operation-um-web-service.md) Informationen angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="e698a-115">Contains a value that indicates the status of a call for which the [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) requested information.</span></span>  <br/> |
|<span data-ttu-id="e698a-116">EventCause</span><span class="sxs-lookup"><span data-stu-id="e698a-116">EventCause</span></span>  <br/> |<span data-ttu-id="e698a-117">Enthält einen Wert, der die Ursache eines Ereignisses für einen Anruf angibt, für den der [GetCallInfo-Vorgang (um-Webdienst)](getcallinfo-operation-um-web-service.md) Informationen angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="e698a-117">Contains a value that indicates the cause of an event for a call for which the [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) requested information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e698a-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e698a-118">Parent elements</span></span>

<span data-ttu-id="e698a-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="e698a-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e698a-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="e698a-120">Text value</span></span>

<span data-ttu-id="e698a-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="e698a-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e698a-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e698a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e698a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e698a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e698a-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e698a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e698a-125">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e698a-125">Messages</span></span>  <br/> |
|<span data-ttu-id="e698a-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e698a-126">Validation File</span></span>  <br/> |<span data-ttu-id="e698a-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e698a-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e698a-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e698a-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="e698a-129">False</span><span class="sxs-lookup"><span data-stu-id="e698a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e698a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e698a-130">See also</span></span>



[<span data-ttu-id="e698a-131">GetCallInfo-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e698a-131">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="e698a-132">CallState (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e698a-132">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
[<span data-ttu-id="e698a-133">EventCause (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e698a-133">EventCause (UM web service)</span></span>](eventcause-um-web-service.md)

