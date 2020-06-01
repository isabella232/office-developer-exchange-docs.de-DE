---
title: OofStatus (um-Webdienst)
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
description: Das OofStatus-Element enthält einen Wert, der den Abwesenheitsstatus des Unified Messaging-Diensts für den Benutzer angibt, der einen GetUMProperties-Vorgang (um-Webdienst) anfordert.
ms.openlocfilehash: 80b1d5aa508579eec14637ed10c322b5fbb670da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460575"
---
# <a name="oofstatus-um-web-service"></a><span data-ttu-id="ec7e4-103">OofStatus (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ec7e4-103">OofStatus (UM web service)</span></span>

<span data-ttu-id="ec7e4-104">Das **OofStatus** -Element enthält einen Wert, der den Abwesenheitsstatus des Unified Messaging-Diensts für den Benutzer angibt, der einen [GetUMProperties-Vorgang (um-Webdienst)](getumproperties-operation-um-web-service.md) anfordert.</span><span class="sxs-lookup"><span data-stu-id="ec7e4-104">The **OofStatus** element contains a value that indicaties the Unified Messaging Out of Office status for the user who is making a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="ec7e4-105">GetUMPropertiesResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ec7e4-105">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)
  
[<span data-ttu-id="ec7e4-106">OofStatus (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ec7e4-106">OofStatus (UM web service)</span></span>](oofstatus-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
    <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 <span data-ttu-id="ec7e4-107">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="ec7e4-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec7e4-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ec7e4-108">Attributes and elements</span></span>

<span data-ttu-id="ec7e4-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ec7e4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec7e4-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ec7e4-110">Attributes</span></span>

<span data-ttu-id="ec7e4-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec7e4-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec7e4-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec7e4-112">Child elements</span></span>

<span data-ttu-id="ec7e4-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec7e4-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ec7e4-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec7e4-114">Parent elements</span></span>

|<span data-ttu-id="ec7e4-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec7e4-115">**Element**</span></span>|<span data-ttu-id="ec7e4-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec7e4-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec7e4-117">GetUMPropertiesResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ec7e4-117">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md) <br/> |<span data-ttu-id="ec7e4-118">Definiert eine Antwort auf eine [GetUMProperties-Vorgangsanforderung (um-Webdienst)](getumproperties-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="ec7e4-118">Defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ec7e4-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="ec7e4-119">Text value</span></span>

<span data-ttu-id="ec7e4-120">Ein boolescher Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec7e4-120">A Boolean text value is required.</span></span> <span data-ttu-id="ec7e4-121">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="ec7e4-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="ec7e4-122">Wahr</span><span class="sxs-lookup"><span data-stu-id="ec7e4-122">True</span></span>
    
- <span data-ttu-id="ec7e4-123">Falsch</span><span class="sxs-lookup"><span data-stu-id="ec7e4-123">False</span></span>
    
## <a name="element-information"></a><span data-ttu-id="ec7e4-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ec7e4-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec7e4-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec7e4-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ec7e4-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ec7e4-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ec7e4-127">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="ec7e4-127">Messages</span></span>  <br/> |
|<span data-ttu-id="ec7e4-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ec7e4-128">Validation File</span></span>  <br/> |<span data-ttu-id="ec7e4-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ec7e4-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ec7e4-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ec7e4-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec7e4-131">False</span><span class="sxs-lookup"><span data-stu-id="ec7e4-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec7e4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec7e4-132">See also</span></span>



[<span data-ttu-id="ec7e4-133">GetUMProperties-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ec7e4-133">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)
  
[<span data-ttu-id="ec7e4-134">GetUMPropertiesResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ec7e4-134">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)

