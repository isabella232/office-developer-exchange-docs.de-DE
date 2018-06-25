---
title: ConnectionTimeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionTimeout
api_type:
- schema
ms.assetid: 14da68a0-bcca-4281-a774-47644baa4ee9
description: ConnectionTimeout-Element gibt die Anzahl der Minuten ein, um eine Verbindung zu halten.
ms.openlocfilehash: 2bb40ba502853c70ef107c4c740fdfe7073abe31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757601"
---
# <a name="connectiontimeout"></a><span data-ttu-id="b5644-103">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="b5644-103">ConnectionTimeout</span></span>

<span data-ttu-id="b5644-104">**ConnectionTimeout** -Element gibt die Anzahl der Minuten ein, um eine Verbindung zu halten.</span><span class="sxs-lookup"><span data-stu-id="b5644-104">The **ConnectionTimeout** element specifies the number of minutes to keep a connection open.</span></span> 
  
[<span data-ttu-id="b5644-105">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b5644-105">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="b5644-106">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="b5644-106">ConnectionTimeout</span></span>](connectiontimeout.md)
  
```xml
<ConnectionTimeout/>
```

 <span data-ttu-id="b5644-107">**int**</span><span class="sxs-lookup"><span data-stu-id="b5644-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5644-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b5644-108">Attributes and elements</span></span>

<span data-ttu-id="b5644-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b5644-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5644-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="b5644-110">Attributes</span></span>

<span data-ttu-id="b5644-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5644-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5644-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5644-112">Child elements</span></span>

<span data-ttu-id="b5644-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5644-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b5644-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5644-114">Parent elements</span></span>

|<span data-ttu-id="b5644-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5644-115">**Element**</span></span>|<span data-ttu-id="b5644-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5644-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5644-117">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="b5644-117">GetStreamingEvents</span></span>](getstreamingevents.md) <br/> |<span data-ttu-id="b5644-118">Definiert eine Anforderung zum Abrufen von ereignisbenachrichtigungen aus einer streaming-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="b5644-118">Defines a request to get event notifications from a streaming connection.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b5644-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="b5644-119">Text value</span></span>

<span data-ttu-id="b5644-120">Der Textwert stellt eine ganze Zahl, die die maximale Anzahl von Minuten ein, um eine streaming Verbindung geöffnet bleiben beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b5644-120">The text value represents an integer that describes the maximum number of minutes to keep a streaming connection open.</span></span> <span data-ttu-id="b5644-121">Der Wert muss zwischen 1 und 30, inklusive.</span><span class="sxs-lookup"><span data-stu-id="b5644-121">The value must be between 1 and 30, inclusive.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5644-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5644-122">Remarks</span></span>

<span data-ttu-id="b5644-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b5644-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5644-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b5644-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5644-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5644-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b5644-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b5644-126">Schema name</span></span>  <br/> |<span data-ttu-id="b5644-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b5644-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="b5644-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b5644-128">Validation file</span></span>  <br/> |<span data-ttu-id="b5644-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b5644-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b5644-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b5644-130">Can be empty</span></span>  <br/> |<span data-ttu-id="b5644-131">False</span><span class="sxs-lookup"><span data-stu-id="b5644-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5644-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5644-132">See also</span></span>



[<span data-ttu-id="b5644-133">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b5644-133">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="b5644-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b5644-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

