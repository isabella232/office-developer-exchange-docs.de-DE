---
title: StartDateTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartDateTime
api_type:
- schema
ms.assetid: 6fd41b7b-6c83-43b6-8b16-0bdb3d173d73
description: Das StartDateTime-Element gibt das Startdatum und die Uhrzeit für eine Regel oder eine Suche.
ms.openlocfilehash: 4bc32ed5626d692fc73dfa8bd7c46923aba72f9e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831552"
---
# <a name="startdatetime"></a><span data-ttu-id="c8ebe-103">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="c8ebe-103">StartDateTime</span></span>

<span data-ttu-id="c8ebe-104">Das **StartDateTime** -Element gibt das Startdatum und die Uhrzeit für eine Regel oder eine Suche.</span><span class="sxs-lookup"><span data-stu-id="c8ebe-104">The **StartDateTime** element specifies the start date and time for a rule or a search.</span></span> 
  
```XML
<StartDate/>
```

<span data-ttu-id="c8ebe-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="c8ebe-105">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c8ebe-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c8ebe-106">Attributes and elements</span></span>

<span data-ttu-id="c8ebe-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c8ebe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8ebe-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c8ebe-108">Attributes</span></span>

<span data-ttu-id="c8ebe-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c8ebe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8ebe-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c8ebe-110">Child elements</span></span>

<span data-ttu-id="c8ebe-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c8ebe-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c8ebe-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c8ebe-112">Parent elements</span></span>

|<span data-ttu-id="c8ebe-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8ebe-113">**Element**</span></span>|<span data-ttu-id="c8ebe-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8ebe-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8ebe-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c8ebe-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="c8ebe-116">Gibt Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="c8ebe-116">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="c8ebe-117">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="c8ebe-117">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="c8ebe-118">Gibt den Datumsbereich, in dem eingehende Nachrichten müssen in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="c8ebe-118">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c8ebe-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="c8ebe-119">Text value</span></span>

 <span data-ttu-id="c8ebe-120">Ein Textwert, der einen Datum/Uhrzeit darstellt ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8ebe-120">A text value that represents a date/time is required if this element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c8ebe-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8ebe-121">Remarks</span></span>

<span data-ttu-id="c8ebe-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c8ebe-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8ebe-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c8ebe-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8ebe-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8ebe-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c8ebe-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c8ebe-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c8ebe-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c8ebe-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c8ebe-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c8ebe-127">Validation File</span></span>  <br/> |<span data-ttu-id="c8ebe-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c8ebe-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c8ebe-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c8ebe-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="c8ebe-130">False</span><span class="sxs-lookup"><span data-stu-id="c8ebe-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8ebe-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8ebe-131">See also</span></span>

- [<span data-ttu-id="c8ebe-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c8ebe-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

