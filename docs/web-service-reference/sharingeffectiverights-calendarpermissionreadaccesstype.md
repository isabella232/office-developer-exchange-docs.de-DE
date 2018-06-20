---
title: SharingEffectiveRights (CalendarPermissionReadAccessType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: b519f642-a9ef-4300-92e6-ed8202855fde
description: Das SharingEffectiveRights-Element gibt an, die Berechtigungen, die der Benutzer für die Kalenderdaten verfügt, die gemeinsam genutzt wird.
ms.openlocfilehash: e7d2aa061650c33d27de042ae8a6348f9a7d3430
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831480"
---
# <a name="sharingeffectiverights-calendarpermissionreadaccesstype"></a><span data-ttu-id="15728-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="15728-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span></span>

<span data-ttu-id="15728-104">Das **SharingEffectiveRights** -Element gibt an, die Berechtigungen, die der Benutzer für die Kalenderdaten verfügt, die gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="15728-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the calendar data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | TimeOnly | TimeAndSubjectAndLocation | FullDetails</SharingEffectiveRights>
```

 <span data-ttu-id="15728-105">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="15728-105">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15728-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="15728-106">Attributes and elements</span></span>

<span data-ttu-id="15728-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="15728-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15728-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="15728-108">Attributes</span></span>

<span data-ttu-id="15728-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="15728-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15728-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15728-110">Child elements</span></span>

<span data-ttu-id="15728-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="15728-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="15728-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15728-112">Parent elements</span></span>

|<span data-ttu-id="15728-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="15728-113">**Element**</span></span>|<span data-ttu-id="15728-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15728-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15728-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="15728-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="15728-116">Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="15728-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="15728-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="15728-117">Text value</span></span>

<span data-ttu-id="15728-118">Die folgende Tabelle enthält die möglichen Werte für das **SharingEffectiveRights** -Element.</span><span class="sxs-lookup"><span data-stu-id="15728-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
|<span data-ttu-id="15728-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="15728-119">**Value**</span></span>|<span data-ttu-id="15728-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15728-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15728-121">Keine</span><span class="sxs-lookup"><span data-stu-id="15728-121">None</span></span>  <br/> |<span data-ttu-id="15728-122">Gibt an, dass der Benutzer die Berechtigung zum Anzeigen von Elementen im Kalender nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="15728-122">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="15728-123">TimeOnly</span><span class="sxs-lookup"><span data-stu-id="15728-123">TimeOnly</span></span>  <br/> |<span data-ttu-id="15728-124">Gibt an, dass der Benutzer die Berechtigung zum Anzeigen der nur Frei/Gebucht-Zeit im Kalender hat.</span><span class="sxs-lookup"><span data-stu-id="15728-124">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="15728-125">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="15728-125">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="15728-126">Gibt an, dass der Benutzer über die Berechtigung zum Anzeigen von Frei/Gebucht-Zeit in den Kalender und den Betreff und Ort von Terminen verfügt.</span><span class="sxs-lookup"><span data-stu-id="15728-126">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="15728-127">FullDetails</span><span class="sxs-lookup"><span data-stu-id="15728-127">FullDetails</span></span>  <br/> |<span data-ttu-id="15728-128">Gibt an, dass der Benutzer die Berechtigung zum Anzeigen aller Elemente im Kalender, einschließlich der Frei/Gebucht-Zeit und Betreff, Ort und Details von Terminen verfügt.</span><span class="sxs-lookup"><span data-stu-id="15728-128">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15728-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15728-129">Remarks</span></span>

<span data-ttu-id="15728-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="15728-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15728-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="15728-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15728-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="15728-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="15728-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="15728-133">Schema Name</span></span>  <br/> |<span data-ttu-id="15728-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="15728-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="15728-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="15728-135">Validation File</span></span>  <br/> |<span data-ttu-id="15728-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="15728-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="15728-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="15728-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="15728-138">False</span><span class="sxs-lookup"><span data-stu-id="15728-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15728-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15728-139">See also</span></span>



- [<span data-ttu-id="15728-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="15728-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

