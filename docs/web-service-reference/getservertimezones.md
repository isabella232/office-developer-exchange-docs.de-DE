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
description: Das GetServerTimeZones-Element ist das Stammelement im eine Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange-Server.
ms.openlocfilehash: 1ad503ff312497189f57bce9a3670571aedad5ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758804"
---
# <a name="getservertimezones"></a><span data-ttu-id="cf0c7-103">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="cf0c7-103">GetServerTimeZones</span></span>

<span data-ttu-id="cf0c7-104">Das **GetServerTimeZones** -Element ist das Stammelement im eine Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-104">The **GetServerTimeZones** element is the root element in a request to retrieve time zone definitions from the Exchange server.</span></span> 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 <span data-ttu-id="cf0c7-105">**GetServerTimeZonesType**</span><span class="sxs-lookup"><span data-stu-id="cf0c7-105">**GetServerTimeZonesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf0c7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cf0c7-106">Attributes and elements</span></span>

<span data-ttu-id="cf0c7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf0c7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cf0c7-108">Attributes</span></span>

|<span data-ttu-id="cf0c7-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cf0c7-109">**Attribute**</span></span>|<span data-ttu-id="cf0c7-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf0c7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf0c7-111">**ReturnFullTimeZoneData**</span><span class="sxs-lookup"><span data-stu-id="cf0c7-111">**ReturnFullTimeZoneData**</span></span> <br/> |<span data-ttu-id="cf0c7-112">Gibt an, ob der [Vorgang GetServerTimeZones](getservertimezones-operation.md) die vollständige Definition oder nur die Namen und Bezeichner für jede Zeitzone zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-112">Specifies whether the [GetServerTimeZones operation](getservertimezones-operation.md) returns the complete definition or only the name and identifier for each time zone.</span></span> <span data-ttu-id="cf0c7-113">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-113">This attribute is optional.</span></span> <span data-ttu-id="cf0c7-114">Der Standardwert ist **true**.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-114">The default value is **true**.</span></span>  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a><span data-ttu-id="cf0c7-115">ReturnFullTimeZoneData-Attribut</span><span class="sxs-lookup"><span data-stu-id="cf0c7-115">ReturnFullTimeZoneData Attribute</span></span>

|<span data-ttu-id="cf0c7-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cf0c7-116">**Value**</span></span>|<span data-ttu-id="cf0c7-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf0c7-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf0c7-118">**"true"**</span><span class="sxs-lookup"><span data-stu-id="cf0c7-118">**true**</span></span> <br/> |<span data-ttu-id="cf0c7-119">Die vollständigen Definitionen für jede Zeitzone zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-119">Return the complete definitions for each time zone.</span></span>  <br/> |
|<span data-ttu-id="cf0c7-120">**false**</span><span class="sxs-lookup"><span data-stu-id="cf0c7-120">**false**</span></span> <br/> |<span data-ttu-id="cf0c7-121">Zurückgeben Sie nur den Namen und Bezeichner für jede Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-121">Return only the name and identifier for each time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cf0c7-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cf0c7-122">Child elements</span></span>

|<span data-ttu-id="cf0c7-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="cf0c7-123">**Element**</span></span>|<span data-ttu-id="cf0c7-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf0c7-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf0c7-125">IDs</span><span class="sxs-lookup"><span data-stu-id="cf0c7-125">Ids</span></span>](ids.md) <br/> |<span data-ttu-id="cf0c7-126">Enthält ein Array der Zeitzone Definition Bezeichner, der die angeforderte Zeitzonendefinitionen angibt.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-126">Contains an array of time zone definition identifiers that specifies the requested time zone definitions.</span></span> <span data-ttu-id="cf0c7-127">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-127">This element is optional.</span></span> <span data-ttu-id="cf0c7-128">Wenn dieses Element nicht in der Anforderung [GetServerTimeZones Vorgang](getservertimezones-operation.md) enthalten ist, werden alle Zeitzonendefinitionen auf dem Server zur Verfügung stehen in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-128">If this element is not included in the [GetServerTimeZones operation](getservertimezones-operation.md) request, all time zone definitions that are available on the server are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf0c7-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cf0c7-129">Parent elements</span></span>

<span data-ttu-id="cf0c7-130">Keine.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf0c7-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cf0c7-131">Remarks</span></span>

<span data-ttu-id="cf0c7-132">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="cf0c7-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf0c7-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cf0c7-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf0c7-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf0c7-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cf0c7-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cf0c7-135">Schema Name</span></span>  <br/> |<span data-ttu-id="cf0c7-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cf0c7-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cf0c7-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cf0c7-137">Validation File</span></span>  <br/> |<span data-ttu-id="cf0c7-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cf0c7-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cf0c7-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cf0c7-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf0c7-140">False</span><span class="sxs-lookup"><span data-stu-id="cf0c7-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf0c7-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf0c7-141">See also</span></span>



[<span data-ttu-id="cf0c7-142">GetServerTimeZones-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cf0c7-142">GetServerTimeZones operation</span></span>](getservertimezones-operation.md)
  
[<span data-ttu-id="cf0c7-143">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="cf0c7-143">GetServerTimeZonesResponse</span></span>](getservertimezonesresponse.md)


- [<span data-ttu-id="cf0c7-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cf0c7-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

