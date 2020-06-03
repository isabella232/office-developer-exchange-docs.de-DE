---
title: CallState (um-Webdienst)
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
description: Das CallState-Element enthält einen Wert, der den Status eines Anrufs angibt.
ms.openlocfilehash: 44614c460286ff49ebc2373263c1827c6be5cc08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454610"
---
# <a name="callstate-um-web-service"></a><span data-ttu-id="76f36-103">CallState (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="76f36-103">CallState (UM web service)</span></span>

<span data-ttu-id="76f36-104">Das **CallState** -Element enthält einen Wert, der den Status eines Anrufs angibt.</span><span class="sxs-lookup"><span data-stu-id="76f36-104">The **CallState** element contains a value that indicates the status of a call.</span></span> 
  
[<span data-ttu-id="76f36-105">GetCallInfoResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="76f36-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="76f36-106">CallState (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="76f36-106">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 <span data-ttu-id="76f36-107">**UMCallState**</span><span class="sxs-lookup"><span data-stu-id="76f36-107">**UMCallState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76f36-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="76f36-108">Attributes and elements</span></span>

<span data-ttu-id="76f36-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="76f36-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76f36-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="76f36-110">Attributes</span></span>

<span data-ttu-id="76f36-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="76f36-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76f36-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76f36-112">Child elements</span></span>

<span data-ttu-id="76f36-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="76f36-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="76f36-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76f36-114">Parent elements</span></span>

|<span data-ttu-id="76f36-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="76f36-115">**Element**</span></span>|<span data-ttu-id="76f36-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76f36-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76f36-117">GetCallInfoResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="76f36-117">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md) <br/> |<span data-ttu-id="76f36-118">Definiert eine Antwort auf einen [GetCallInfo-Vorgang (um-Webdienst)](getcallinfo-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="76f36-118">Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="76f36-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="76f36-119">Text value</span></span>

<span data-ttu-id="76f36-120">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="76f36-120">A text value is required.</span></span> <span data-ttu-id="76f36-121">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="76f36-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="76f36-122">Leerlauf</span><span class="sxs-lookup"><span data-stu-id="76f36-122">Idle</span></span>
    
- <span data-ttu-id="76f36-123">Verbindung wird hergestellt</span><span class="sxs-lookup"><span data-stu-id="76f36-123">Connecting</span></span>
    
- <span data-ttu-id="76f36-124">Alarmiert</span><span class="sxs-lookup"><span data-stu-id="76f36-124">Alerted</span></span>
    
- <span data-ttu-id="76f36-125">Verbunden</span><span class="sxs-lookup"><span data-stu-id="76f36-125">Connected</span></span>
    
- <span data-ttu-id="76f36-126">Disconnected</span><span class="sxs-lookup"><span data-stu-id="76f36-126">Disconnected</span></span>
    
- <span data-ttu-id="76f36-127">Eingehende</span><span class="sxs-lookup"><span data-stu-id="76f36-127">Incoming</span></span>
    
- <span data-ttu-id="76f36-128">Transfer</span><span class="sxs-lookup"><span data-stu-id="76f36-128">Transferring</span></span>
    
- <span data-ttu-id="76f36-129">Weiterleitungs</span><span class="sxs-lookup"><span data-stu-id="76f36-129">Forwarding</span></span>
    
## <a name="element-information"></a><span data-ttu-id="76f36-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="76f36-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76f36-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="76f36-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|<span data-ttu-id="76f36-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="76f36-132">Schema Name</span></span>  <br/> |<span data-ttu-id="76f36-133">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="76f36-133">Messages</span></span>  <br/> |
|<span data-ttu-id="76f36-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="76f36-134">Validation File</span></span>  <br/> |<span data-ttu-id="76f36-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="76f36-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="76f36-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="76f36-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="76f36-137">False</span><span class="sxs-lookup"><span data-stu-id="76f36-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76f36-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76f36-138">See also</span></span>



[<span data-ttu-id="76f36-139">GetCallInfo-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="76f36-139">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="76f36-140">GetCallInfoResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="76f36-140">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)

