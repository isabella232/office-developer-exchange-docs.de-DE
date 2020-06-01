---
title: GetServerTimeZones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 2a89098b-d89b-4d01-827b-50be00f7cbe9
description: Das GetServerTimeZones-Element ist das Stammelement in einer Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange-Server.
ms.openlocfilehash: 797e4543c94b0628242bcf544fe9a735ebaa5a63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460939"
---
# <a name="getservertimezones"></a><span data-ttu-id="18596-103">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="18596-103">GetServerTimeZones</span></span>

<span data-ttu-id="18596-104">Das **GetServerTimeZones** -Element ist das Stammelement in einer Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="18596-104">The **GetServerTimeZones** element is the root element in a request to retrieve time zone definitions from the Exchange server.</span></span> 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 <span data-ttu-id="18596-105">**GetServerTimeZonesType**</span><span class="sxs-lookup"><span data-stu-id="18596-105">**GetServerTimeZonesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18596-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="18596-106">Attributes and elements</span></span>

<span data-ttu-id="18596-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="18596-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18596-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="18596-108">Attributes</span></span>

|<span data-ttu-id="18596-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="18596-109">**Attribute**</span></span>|<span data-ttu-id="18596-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18596-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18596-111">**ReturnFullTimeZoneData**</span><span class="sxs-lookup"><span data-stu-id="18596-111">**ReturnFullTimeZoneData**</span></span> <br/> |<span data-ttu-id="18596-112">Gibt an, ob der [GetServerTimeZones-Vorgang](getservertimezones-operation.md) die vollständige Definition oder nur den Namen und den Bezeichner für jede Zeitzone zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="18596-112">Specifies whether the [GetServerTimeZones operation](getservertimezones-operation.md) returns the complete definition or only the name and identifier for each time zone.</span></span> <span data-ttu-id="18596-113">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="18596-113">This attribute is optional.</span></span> <span data-ttu-id="18596-114">Der Standardwert ist **true**.</span><span class="sxs-lookup"><span data-stu-id="18596-114">The default value is **true**.</span></span>  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a><span data-ttu-id="18596-115">ReturnFullTimeZoneData-Attribut</span><span class="sxs-lookup"><span data-stu-id="18596-115">ReturnFullTimeZoneData Attribute</span></span>

|<span data-ttu-id="18596-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="18596-116">**Value**</span></span>|<span data-ttu-id="18596-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18596-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18596-118">**true**</span><span class="sxs-lookup"><span data-stu-id="18596-118">**true**</span></span> <br/> |<span data-ttu-id="18596-119">Zurückgeben der vollständigen Definitionen für jede Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="18596-119">Return the complete definitions for each time zone.</span></span>  <br/> |
|<span data-ttu-id="18596-120">**false**</span><span class="sxs-lookup"><span data-stu-id="18596-120">**false**</span></span> <br/> |<span data-ttu-id="18596-121">Geben Sie nur den Namen und den Bezeichner für jede Zeitzone zurück.</span><span class="sxs-lookup"><span data-stu-id="18596-121">Return only the name and identifier for each time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="18596-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18596-122">Child elements</span></span>

|<span data-ttu-id="18596-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="18596-123">**Element**</span></span>|<span data-ttu-id="18596-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18596-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18596-125">IDs</span><span class="sxs-lookup"><span data-stu-id="18596-125">Ids</span></span>](ids.md) <br/> |<span data-ttu-id="18596-126">Enthält ein Array von Zeit Zonen Definitions Bezeichnern, die die angeforderten Zeitzonendefinitionen angeben.</span><span class="sxs-lookup"><span data-stu-id="18596-126">Contains an array of time zone definition identifiers that specifies the requested time zone definitions.</span></span> <span data-ttu-id="18596-127">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="18596-127">This element is optional.</span></span> <span data-ttu-id="18596-128">Wenn dieses Element nicht in der GetServerTimeZones- [Vorgangs](getservertimezones-operation.md) Anforderung enthalten ist, werden alle auf dem Server verfügbaren Zeitzonendefinitionen in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18596-128">If this element is not included in the [GetServerTimeZones operation](getservertimezones-operation.md) request, all time zone definitions that are available on the server are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="18596-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18596-129">Parent elements</span></span>

<span data-ttu-id="18596-130">Keine.</span><span class="sxs-lookup"><span data-stu-id="18596-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18596-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18596-131">Remarks</span></span>

<span data-ttu-id="18596-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="18596-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18596-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="18596-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18596-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="18596-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="18596-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="18596-135">Schema Name</span></span>  <br/> |<span data-ttu-id="18596-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="18596-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="18596-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="18596-137">Validation File</span></span>  <br/> |<span data-ttu-id="18596-138">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="18596-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="18596-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="18596-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="18596-140">False</span><span class="sxs-lookup"><span data-stu-id="18596-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18596-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18596-141">See also</span></span>



[<span data-ttu-id="18596-142">GetServerTimeZones-Vorgang</span><span class="sxs-lookup"><span data-stu-id="18596-142">GetServerTimeZones operation</span></span>](getservertimezones-operation.md)
  
[<span data-ttu-id="18596-143">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="18596-143">GetServerTimeZonesResponse</span></span>](getservertimezonesresponse.md)


- [<span data-ttu-id="18596-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="18596-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

