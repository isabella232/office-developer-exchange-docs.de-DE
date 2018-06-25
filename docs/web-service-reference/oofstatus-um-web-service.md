---
title: OofStatus (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: Das OofStatus-Element enthält einem Wert, Indicaties der Unified Messaging nicht im Büro Status für den Benutzer, der eine GetUMProperties-Vorgang (UM-Webdienst) Anforderung gesendet hat.
ms.openlocfilehash: 1fe358a8bfea3c509220d6705a238ae832de37e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830650"
---
# <a name="oofstatus-um-web-service"></a><span data-ttu-id="91d8a-103">OofStatus (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="91d8a-103">OofStatus (UM web service)</span></span>

<span data-ttu-id="91d8a-104">Das **OofStatus** -Element enthält einen Wert, Indicaties der Unified Messaging nicht im Büro Status für den Benutzer, der eine [GetUMProperties-Vorgang (UM-Webdienst)](getumproperties-operation-um-web-service.md) Anforderung gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="91d8a-104">The **OofStatus** element contains a value that indicaties the Unified Messaging Out of Office status for the user who is making a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="91d8a-105">GetUMPropertiesResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="91d8a-105">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)
  
[<span data-ttu-id="91d8a-106">OofStatus (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="91d8a-106">OofStatus (UM web service)</span></span>](oofstatus-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
    <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 <span data-ttu-id="91d8a-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="91d8a-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91d8a-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="91d8a-108">Attributes and elements</span></span>

<span data-ttu-id="91d8a-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="91d8a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91d8a-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="91d8a-110">Attributes</span></span>

<span data-ttu-id="91d8a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="91d8a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91d8a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91d8a-112">Child elements</span></span>

<span data-ttu-id="91d8a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="91d8a-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="91d8a-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91d8a-114">Parent elements</span></span>

|<span data-ttu-id="91d8a-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="91d8a-115">**Element**</span></span>|<span data-ttu-id="91d8a-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91d8a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91d8a-117">GetUMPropertiesResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="91d8a-117">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md) <br/> |<span data-ttu-id="91d8a-118">Definiert eine Antwort auf eine [GetUMProperties-Vorgang (UM-Webdienst)](getumproperties-operation-um-web-service.md) an.</span><span class="sxs-lookup"><span data-stu-id="91d8a-118">Defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="91d8a-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="91d8a-119">Text value</span></span>

<span data-ttu-id="91d8a-120">Ein Boolean-Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="91d8a-120">A Boolean text value is required.</span></span> <span data-ttu-id="91d8a-121">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="91d8a-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="91d8a-122">True</span><span class="sxs-lookup"><span data-stu-id="91d8a-122">True</span></span>
    
- <span data-ttu-id="91d8a-123">False</span><span class="sxs-lookup"><span data-stu-id="91d8a-123">False</span></span>
    
## <a name="element-information"></a><span data-ttu-id="91d8a-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="91d8a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91d8a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="91d8a-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="91d8a-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="91d8a-126">Schema Name</span></span>  <br/> |<span data-ttu-id="91d8a-127">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="91d8a-127">Messages</span></span>  <br/> |
|<span data-ttu-id="91d8a-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="91d8a-128">Validation File</span></span>  <br/> |<span data-ttu-id="91d8a-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="91d8a-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="91d8a-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="91d8a-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="91d8a-131">False</span><span class="sxs-lookup"><span data-stu-id="91d8a-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91d8a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91d8a-132">See also</span></span>



[<span data-ttu-id="91d8a-133">GetUMProperties-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="91d8a-133">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)
  
[<span data-ttu-id="91d8a-134">GetUMPropertiesResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="91d8a-134">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)

