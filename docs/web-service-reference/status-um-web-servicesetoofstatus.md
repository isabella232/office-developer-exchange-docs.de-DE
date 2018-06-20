---
title: Status (UM-Webdienst - SetOofStatus)
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
description: Status-Element definiert den Wert in der Anforderung einer SetOofStatus-Operation (UM-Webdienst) verwenden.
ms.openlocfilehash: 57b4f8fe1a64341b1c2ae0a06bc98f1c9cfd28c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831583"
---
# <a name="status-um-web-service---setoofstatus"></a><span data-ttu-id="e6b29-103">Status (UM-Webdienst - SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="e6b29-103">Status (UM web service - SetOofStatus)</span></span>

<span data-ttu-id="e6b29-104">**Status** -Element definiert den Wert in einer Anforderung [SetOofStatus-Vorgang (UM-Webdienst)](setoofstatus-operation-um-web-service.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6b29-104">The **Status** element defines the value to use in a [SetOofStatus operation (UM web service)](setoofstatus-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="e6b29-105">SetOofStatus (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e6b29-105">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
[<span data-ttu-id="e6b29-106">Status (UM-Webdienst - SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="e6b29-106">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 <span data-ttu-id="e6b29-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e6b29-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6b29-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e6b29-108">Attributes and elements</span></span>

<span data-ttu-id="e6b29-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e6b29-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6b29-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e6b29-110">Attributes</span></span>

<span data-ttu-id="e6b29-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e6b29-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e6b29-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6b29-112">Child elements</span></span>

<span data-ttu-id="e6b29-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="e6b29-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e6b29-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6b29-114">Parent elements</span></span>

|<span data-ttu-id="e6b29-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6b29-115">**Element**</span></span>|<span data-ttu-id="e6b29-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6b29-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6b29-117">SetOofStatus (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e6b29-117">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md) <br/> |<span data-ttu-id="e6b29-118">Definiert eine Anforderung an den Unified Messaging Out of Office (OOF) Status für den Benutzer festlegen, die die Anforderung stellt.</span><span class="sxs-lookup"><span data-stu-id="e6b29-118">Defines a request to set the Unified Messaging Out of Office (OOF) status for the user who makes the request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e6b29-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="e6b29-119">Text value</span></span>

<span data-ttu-id="e6b29-120">Ein boolescher Wert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e6b29-120">A Boolean value is required.</span></span> <span data-ttu-id="e6b29-121">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="e6b29-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="e6b29-122">True</span><span class="sxs-lookup"><span data-stu-id="e6b29-122">True</span></span>
    
- <span data-ttu-id="e6b29-123">False</span><span class="sxs-lookup"><span data-stu-id="e6b29-123">False</span></span>
    
## <a name="element-information"></a><span data-ttu-id="e6b29-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e6b29-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6b29-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6b29-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e6b29-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e6b29-126">Schema Name</span></span>  <br/> |<span data-ttu-id="e6b29-127">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e6b29-127">Messages</span></span>  <br/> |
|<span data-ttu-id="e6b29-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e6b29-128">Validation File</span></span>  <br/> |<span data-ttu-id="e6b29-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e6b29-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e6b29-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e6b29-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="e6b29-131">False</span><span class="sxs-lookup"><span data-stu-id="e6b29-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6b29-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6b29-132">See also</span></span>



[<span data-ttu-id="e6b29-133">SetOofStatus-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e6b29-133">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)

