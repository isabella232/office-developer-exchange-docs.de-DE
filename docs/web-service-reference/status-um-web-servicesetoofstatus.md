---
title: Status (um-Webdienst – SetOofStatus)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 893bcff1-ccdc-493f-b366-ce8a68c813bd
description: Das Status-Element definiert den Wert, der in einer SetOofStatus-Vorgangsanforderung (um-Webdienst) verwendet werden soll.
ms.openlocfilehash: 865152baf28c22578664e16db2dcd5f82a04af98
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459980"
---
# <a name="status-um-web-service---setoofstatus"></a><span data-ttu-id="da0eb-103">Status (um-Webdienst – SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="da0eb-103">Status (UM web service - SetOofStatus)</span></span>

<span data-ttu-id="da0eb-104">Das **Status** -Element definiert den Wert, der in einer [SetOofStatus-Vorgangsanforderung (um-Webdienst)](setoofstatus-operation-um-web-service.md) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da0eb-104">The **Status** element defines the value to use in a [SetOofStatus operation (UM web service)](setoofstatus-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="da0eb-105">SetOofStatus (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="da0eb-105">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
[<span data-ttu-id="da0eb-106">Status (um-Webdienst – SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="da0eb-106">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 <span data-ttu-id="da0eb-107">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="da0eb-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da0eb-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="da0eb-108">Attributes and elements</span></span>

<span data-ttu-id="da0eb-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="da0eb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da0eb-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="da0eb-110">Attributes</span></span>

<span data-ttu-id="da0eb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="da0eb-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da0eb-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da0eb-112">Child elements</span></span>

<span data-ttu-id="da0eb-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="da0eb-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="da0eb-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da0eb-114">Parent elements</span></span>

|<span data-ttu-id="da0eb-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="da0eb-115">**Element**</span></span>|<span data-ttu-id="da0eb-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da0eb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da0eb-117">SetOofStatus (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="da0eb-117">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md) <br/> |<span data-ttu-id="da0eb-118">Definiert eine Anforderung zum Festlegen des Status von Unified Messaging Abwesenheit (Out of Office, OOF) für den Benutzer, der die Anforderung stellt.</span><span class="sxs-lookup"><span data-stu-id="da0eb-118">Defines a request to set the Unified Messaging Out of Office (OOF) status for the user who makes the request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="da0eb-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="da0eb-119">Text value</span></span>

<span data-ttu-id="da0eb-120">Ein boolescher Wert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="da0eb-120">A Boolean value is required.</span></span> <span data-ttu-id="da0eb-121">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="da0eb-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="da0eb-122">Wahr</span><span class="sxs-lookup"><span data-stu-id="da0eb-122">True</span></span>
    
- <span data-ttu-id="da0eb-123">Falsch</span><span class="sxs-lookup"><span data-stu-id="da0eb-123">False</span></span>
    
## <a name="element-information"></a><span data-ttu-id="da0eb-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="da0eb-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da0eb-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="da0eb-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="da0eb-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="da0eb-126">Schema Name</span></span>  <br/> |<span data-ttu-id="da0eb-127">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="da0eb-127">Messages</span></span>  <br/> |
|<span data-ttu-id="da0eb-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="da0eb-128">Validation File</span></span>  <br/> |<span data-ttu-id="da0eb-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="da0eb-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="da0eb-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="da0eb-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="da0eb-131">False</span><span class="sxs-lookup"><span data-stu-id="da0eb-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da0eb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da0eb-132">See also</span></span>



[<span data-ttu-id="da0eb-133">SetOofStatus-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="da0eb-133">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)

