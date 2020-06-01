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
description: Das ConnectionTimeout-Element gibt die Anzahl der Minuten an, die eine Verbindung geöffnet bleiben soll.
ms.openlocfilehash: 671e3cf5466ee8b3543036811708bd7f54afdcce
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463853"
---
# <a name="connectiontimeout"></a><span data-ttu-id="fbc19-103">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="fbc19-103">ConnectionTimeout</span></span>

<span data-ttu-id="fbc19-104">Das **ConnectionTimeout** -Element gibt die Anzahl der Minuten an, die eine Verbindung geöffnet bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="fbc19-104">The **ConnectionTimeout** element specifies the number of minutes to keep a connection open.</span></span> 
  
[<span data-ttu-id="fbc19-105">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fbc19-105">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="fbc19-106">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="fbc19-106">ConnectionTimeout</span></span>](connectiontimeout.md)
  
```xml
<ConnectionTimeout/>
```

 <span data-ttu-id="fbc19-107">**int**</span><span class="sxs-lookup"><span data-stu-id="fbc19-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fbc19-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fbc19-108">Attributes and elements</span></span>

<span data-ttu-id="fbc19-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fbc19-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbc19-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="fbc19-110">Attributes</span></span>

<span data-ttu-id="fbc19-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fbc19-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fbc19-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbc19-112">Child elements</span></span>

<span data-ttu-id="fbc19-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="fbc19-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fbc19-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbc19-114">Parent elements</span></span>

|<span data-ttu-id="fbc19-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="fbc19-115">**Element**</span></span>|<span data-ttu-id="fbc19-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fbc19-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbc19-117">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="fbc19-117">GetStreamingEvents</span></span>](getstreamingevents.md) <br/> |<span data-ttu-id="fbc19-118">Definiert eine Anforderung zum Abrufen von Ereignisbenachrichtigungen aus einer streamingverbindung.</span><span class="sxs-lookup"><span data-stu-id="fbc19-118">Defines a request to get event notifications from a streaming connection.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fbc19-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="fbc19-119">Text value</span></span>

<span data-ttu-id="fbc19-120">Der Textwert stellt eine ganze Zahl dar, die die maximale Anzahl von Minuten beschreibt, die eine streamingverbindung geöffnet bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="fbc19-120">The text value represents an integer that describes the maximum number of minutes to keep a streaming connection open.</span></span> <span data-ttu-id="fbc19-121">Der Wert muss zwischen 1 und 30 einschließlich sein.</span><span class="sxs-lookup"><span data-stu-id="fbc19-121">The value must be between 1 and 30, inclusive.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fbc19-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbc19-122">Remarks</span></span>

<span data-ttu-id="fbc19-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fbc19-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbc19-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fbc19-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbc19-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbc19-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fbc19-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fbc19-126">Schema name</span></span>  <br/> |<span data-ttu-id="fbc19-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="fbc19-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="fbc19-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fbc19-128">Validation file</span></span>  <br/> |<span data-ttu-id="fbc19-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fbc19-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fbc19-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="fbc19-130">Can be empty</span></span>  <br/> |<span data-ttu-id="fbc19-131">False</span><span class="sxs-lookup"><span data-stu-id="fbc19-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbc19-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbc19-132">See also</span></span>



[<span data-ttu-id="fbc19-133">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fbc19-133">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="fbc19-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fbc19-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

