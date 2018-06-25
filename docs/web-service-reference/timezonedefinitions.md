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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839214"
---
# <a name="timezonedefinitions"></a><span data-ttu-id="783ac-103">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="783ac-103">TimeZoneDefinitions</span></span>

<span data-ttu-id="783ac-104">Das **TimeZoneDefinitions** -Element stellt ein Array von Zeitzonendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="783ac-104">The **TimeZoneDefinitions** element represents an array of time zone definitions.</span></span> 
  
```XML
<TimeZoneDefinitions>
   <TimeZoneDefinition/>
</TimeZoneDefinitions>
```

 <span data-ttu-id="783ac-105">**ArrayOfTimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="783ac-105">**ArrayOfTimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="783ac-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="783ac-106">Attributes and elements</span></span>

<span data-ttu-id="783ac-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="783ac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="783ac-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="783ac-108">Attributes</span></span>

<span data-ttu-id="783ac-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="783ac-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="783ac-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="783ac-110">Child elements</span></span>

|<span data-ttu-id="783ac-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="783ac-111">**Element**</span></span>|<span data-ttu-id="783ac-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="783ac-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="783ac-113">Zeitzonendefinition</span><span class="sxs-lookup"><span data-stu-id="783ac-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="783ac-114">Gibt den Zeiträume und Übergänge, die eine Zeitzone definiert.</span><span class="sxs-lookup"><span data-stu-id="783ac-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="783ac-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="783ac-115">Parent elements</span></span>

|<span data-ttu-id="783ac-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="783ac-116">**Element**</span></span>|<span data-ttu-id="783ac-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="783ac-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="783ac-118">GetServerTimeZonesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="783ac-118">GetServerTimeZonesResponseMessage</span></span>](getservertimezonesresponsemessage.md) <br/> |<span data-ttu-id="783ac-119">Enthält den Status und das Ergebnis einer Anforderung [GetServerTimeZones Vorgang](getservertimezones-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="783ac-119">Contains the status and result of a [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="783ac-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="783ac-120">Remarks</span></span>

<span data-ttu-id="783ac-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="783ac-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="783ac-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="783ac-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="783ac-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="783ac-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="783ac-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="783ac-124">Schema Name</span></span>  <br/> |<span data-ttu-id="783ac-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="783ac-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="783ac-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="783ac-126">Validation File</span></span>  <br/> |<span data-ttu-id="783ac-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="783ac-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="783ac-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="783ac-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="783ac-129">False</span><span class="sxs-lookup"><span data-stu-id="783ac-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="783ac-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="783ac-130">See also</span></span>



- [<span data-ttu-id="783ac-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="783ac-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

