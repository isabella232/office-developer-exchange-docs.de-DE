---
title: TimeZoneDefinitions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneDefinitions
api_type:
- schema
ms.assetid: 9ca1584e-65b8-49ba-a408-e3e8597e6607
description: Das TimeZoneDefinitions-Element stellt ein Array von Zeitzonendefinitionen.
ms.openlocfilehash: 0bc1b69ef564bb4e239d9845a4b1a0133292ff12
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839214"
---
# <a name="timezonedefinitions"></a><span data-ttu-id="83e56-103">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="83e56-103">TimeZoneDefinitions</span></span>

<span data-ttu-id="83e56-104">Das **TimeZoneDefinitions** -Element stellt ein Array von Zeitzonendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="83e56-104">The **TimeZoneDefinitions** element represents an array of time zone definitions.</span></span> 
  
```XML
<TimeZoneDefinitions>
   <TimeZoneDefinition/>
</TimeZoneDefinitions>
```

 <span data-ttu-id="83e56-105">**ArrayOfTimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="83e56-105">**ArrayOfTimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83e56-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="83e56-106">Attributes and elements</span></span>

<span data-ttu-id="83e56-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="83e56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83e56-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="83e56-108">Attributes</span></span>

<span data-ttu-id="83e56-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="83e56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83e56-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83e56-110">Child elements</span></span>

|<span data-ttu-id="83e56-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="83e56-111">**Element**</span></span>|<span data-ttu-id="83e56-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83e56-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83e56-113">Zeitzonendefinition</span><span class="sxs-lookup"><span data-stu-id="83e56-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="83e56-114">Gibt den Zeiträume und Übergänge, die eine Zeitzone definiert.</span><span class="sxs-lookup"><span data-stu-id="83e56-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83e56-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83e56-115">Parent elements</span></span>

|<span data-ttu-id="83e56-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="83e56-116">**Element**</span></span>|<span data-ttu-id="83e56-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83e56-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83e56-118">GetServerTimeZonesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="83e56-118">GetServerTimeZonesResponseMessage</span></span>](getservertimezonesresponsemessage.md) <br/> |<span data-ttu-id="83e56-119">Enthält den Status und das Ergebnis einer Anforderung [GetServerTimeZones Vorgang](getservertimezones-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="83e56-119">Contains the status and result of a [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83e56-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="83e56-120">Remarks</span></span>

<span data-ttu-id="83e56-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="83e56-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83e56-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="83e56-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83e56-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="83e56-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="83e56-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="83e56-124">Schema Name</span></span>  <br/> |<span data-ttu-id="83e56-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="83e56-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="83e56-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="83e56-126">Validation File</span></span>  <br/> |<span data-ttu-id="83e56-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="83e56-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="83e56-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="83e56-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="83e56-129">False</span><span class="sxs-lookup"><span data-stu-id="83e56-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83e56-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83e56-130">See also</span></span>



- [<span data-ttu-id="83e56-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="83e56-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

