---
title: CallState (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- CallState
api_type:
- schema
ms.assetid: 88670707-12f7-41c5-ac81-dda0c354a2cb
description: Das CallState-Element enthält einen Wert, der den Status eines Aufrufs angibt.
ms.openlocfilehash: e751c2e38783c6634a44d8e1b830a9224cdf300a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757547"
---
# <a name="callstate-um-web-service"></a><span data-ttu-id="ed767-103">CallState (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ed767-103">CallState (UM web service)</span></span>

<span data-ttu-id="ed767-104">Das **CallState** -Element enthält einen Wert, der den Status eines Aufrufs angibt.</span><span class="sxs-lookup"><span data-stu-id="ed767-104">The **CallState** element contains a value that indicates the status of a call.</span></span> 
  
[<span data-ttu-id="ed767-105">GetCallInfoResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ed767-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="ed767-106">CallState (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ed767-106">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 <span data-ttu-id="ed767-107">**UMCallState**</span><span class="sxs-lookup"><span data-stu-id="ed767-107">**UMCallState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed767-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ed767-108">Attributes and elements</span></span>

<span data-ttu-id="ed767-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ed767-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed767-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ed767-110">Attributes</span></span>

<span data-ttu-id="ed767-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ed767-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed767-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed767-112">Child elements</span></span>

<span data-ttu-id="ed767-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ed767-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ed767-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed767-114">Parent elements</span></span>

|<span data-ttu-id="ed767-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ed767-115">**Element**</span></span>|<span data-ttu-id="ed767-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ed767-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed767-117">GetCallInfoResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ed767-117">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md) <br/> |<span data-ttu-id="ed767-118">Definiert eine Antwort auf eine [GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="ed767-118">Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ed767-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="ed767-119">Text value</span></span>

<span data-ttu-id="ed767-120">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ed767-120">A text value is required.</span></span> <span data-ttu-id="ed767-121">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="ed767-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="ed767-122">Im Leerlauf</span><span class="sxs-lookup"><span data-stu-id="ed767-122">Idle</span></span>
    
- <span data-ttu-id="ed767-123">Connecting</span><span class="sxs-lookup"><span data-stu-id="ed767-123">Connecting</span></span>
    
- <span data-ttu-id="ed767-124">Benachrichtigt</span><span class="sxs-lookup"><span data-stu-id="ed767-124">Alerted</span></span>
    
- <span data-ttu-id="ed767-125">Verbunden</span><span class="sxs-lookup"><span data-stu-id="ed767-125">Connected</span></span>
    
- <span data-ttu-id="ed767-126">Verbindung getrennt</span><span class="sxs-lookup"><span data-stu-id="ed767-126">Disconnected</span></span>
    
- <span data-ttu-id="ed767-127">Eingehend</span><span class="sxs-lookup"><span data-stu-id="ed767-127">Incoming</span></span>
    
- <span data-ttu-id="ed767-128">Übertragen von</span><span class="sxs-lookup"><span data-stu-id="ed767-128">Transferring</span></span>
    
- <span data-ttu-id="ed767-129">Weiterleitung</span><span class="sxs-lookup"><span data-stu-id="ed767-129">Forwarding</span></span>
    
## <a name="element-information"></a><span data-ttu-id="ed767-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ed767-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed767-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed767-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|<span data-ttu-id="ed767-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ed767-132">Schema Name</span></span>  <br/> |<span data-ttu-id="ed767-133">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="ed767-133">Messages</span></span>  <br/> |
|<span data-ttu-id="ed767-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ed767-134">Validation File</span></span>  <br/> |<span data-ttu-id="ed767-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ed767-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed767-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ed767-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed767-137">False</span><span class="sxs-lookup"><span data-stu-id="ed767-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed767-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed767-138">See also</span></span>



[<span data-ttu-id="ed767-139">GetCallInfo-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ed767-139">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="ed767-140">GetCallInfoResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ed767-140">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)

