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
description: Das TimeZoneDefinitions-Element stellt ein Array von Zeitzonendefinitionen dar.
ms.openlocfilehash: 16a25eb4fdcad2554ebd19626d0a0bc7f6391ac5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468761"
---
# <a name="timezonedefinitions"></a><span data-ttu-id="90138-103">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="90138-103">TimeZoneDefinitions</span></span>

<span data-ttu-id="90138-104">Das **TimeZoneDefinitions** -Element stellt ein Array von Zeitzonendefinitionen dar.</span><span class="sxs-lookup"><span data-stu-id="90138-104">The **TimeZoneDefinitions** element represents an array of time zone definitions.</span></span> 
  
```XML
<TimeZoneDefinitions>
   <TimeZoneDefinition/>
</TimeZoneDefinitions>
```

 <span data-ttu-id="90138-105">**ArrayOfTimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="90138-105">**ArrayOfTimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90138-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="90138-106">Attributes and elements</span></span>

<span data-ttu-id="90138-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="90138-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90138-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="90138-108">Attributes</span></span>

<span data-ttu-id="90138-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="90138-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="90138-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="90138-110">Child elements</span></span>

|<span data-ttu-id="90138-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="90138-111">**Element**</span></span>|<span data-ttu-id="90138-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90138-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90138-113">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="90138-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="90138-114">Gibt die Punkte und Übergänge an, die eine Zeitzone definieren.</span><span class="sxs-lookup"><span data-stu-id="90138-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="90138-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="90138-115">Parent elements</span></span>

|<span data-ttu-id="90138-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="90138-116">**Element**</span></span>|<span data-ttu-id="90138-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90138-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90138-118">GetServerTimeZonesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="90138-118">GetServerTimeZonesResponseMessage</span></span>](getservertimezonesresponsemessage.md) <br/> |<span data-ttu-id="90138-119">Enthält den Status und das Ergebnis einer [GetServerTimeZones-Vorgangs](getservertimezones-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="90138-119">Contains the status and result of a [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90138-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90138-120">Remarks</span></span>

<span data-ttu-id="90138-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="90138-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90138-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="90138-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90138-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="90138-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="90138-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="90138-124">Schema Name</span></span>  <br/> |<span data-ttu-id="90138-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="90138-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="90138-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="90138-126">Validation File</span></span>  <br/> |<span data-ttu-id="90138-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="90138-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="90138-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="90138-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="90138-129">False</span><span class="sxs-lookup"><span data-stu-id="90138-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90138-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90138-130">See also</span></span>



- [<span data-ttu-id="90138-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="90138-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

