---
title: EndDateTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndDateTime
api_type:
- schema
ms.assetid: 54d14e47-a8f7-400b-a859-c7ea7ce4c6a4
description: Das EndDateTime-Element gibt das Enddatum und die Uhrzeit für eine Regel oder eine Suche.
ms.openlocfilehash: ad596c6441e7bdb10b4e886a8d0f3ba183c43c3e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758235"
---
# <a name="enddatetime"></a><span data-ttu-id="80be8-103">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="80be8-103">EndDateTime</span></span>

<span data-ttu-id="80be8-104">Das **EndDateTime** -Element gibt das Enddatum und die Uhrzeit für eine Regel oder eine Suche.</span><span class="sxs-lookup"><span data-stu-id="80be8-104">The **EndDateTime** element specifies the end date and time for a rule or a search.</span></span> 
  
```XML
<EndDateTime/>
```

 <span data-ttu-id="80be8-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="80be8-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80be8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="80be8-106">Attributes and elements</span></span>

<span data-ttu-id="80be8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="80be8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80be8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="80be8-108">Attributes</span></span>

<span data-ttu-id="80be8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="80be8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80be8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80be8-110">Child elements</span></span>

<span data-ttu-id="80be8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="80be8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="80be8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80be8-112">Parent elements</span></span>

|<span data-ttu-id="80be8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="80be8-113">**Element**</span></span>|<span data-ttu-id="80be8-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80be8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80be8-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="80be8-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="80be8-116">Enthält die Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="80be8-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="80be8-117">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="80be8-117">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="80be8-118">Gibt den Datumsbereich, in dem eingehende Nachrichten müssen in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="80be8-118">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="80be8-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="80be8-119">Text value</span></span>

<span data-ttu-id="80be8-120">Ein Textwert, der einen Datum/Uhrzeit darstellt ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="80be8-120">A text value that represents a date/time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="80be8-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80be8-121">Remarks</span></span>

<span data-ttu-id="80be8-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="80be8-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80be8-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="80be8-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80be8-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="80be8-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="80be8-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="80be8-125">Schema Name</span></span>  <br/> |<span data-ttu-id="80be8-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="80be8-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="80be8-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="80be8-127">Validation File</span></span>  <br/> |<span data-ttu-id="80be8-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="80be8-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="80be8-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="80be8-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="80be8-130">False</span><span class="sxs-lookup"><span data-stu-id="80be8-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80be8-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80be8-131">See also</span></span>



- [<span data-ttu-id="80be8-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="80be8-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

