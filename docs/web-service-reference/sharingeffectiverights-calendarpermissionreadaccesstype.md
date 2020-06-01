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
description: Das SharingEffectiveRights-Element gibt die Berechtigungen an, die der Benutzer für die Kalenderdaten verwendet, die freigegeben werden.
ms.openlocfilehash: 5581e9cc001608a124ae94e69eba836f6fd98520
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458579"
---
# <a name="sharingeffectiverights-calendarpermissionreadaccesstype"></a><span data-ttu-id="e71b6-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="e71b6-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span></span>

<span data-ttu-id="e71b6-104">Das **SharingEffectiveRights** -Element gibt die Berechtigungen an, die der Benutzer für die Kalenderdaten verwendet, die freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e71b6-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the calendar data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | TimeOnly | TimeAndSubjectAndLocation | FullDetails</SharingEffectiveRights>
```

 <span data-ttu-id="e71b6-105">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="e71b6-105">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e71b6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e71b6-106">Attributes and elements</span></span>

<span data-ttu-id="e71b6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e71b6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e71b6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e71b6-108">Attributes</span></span>

<span data-ttu-id="e71b6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e71b6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e71b6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e71b6-110">Child elements</span></span>

<span data-ttu-id="e71b6-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e71b6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e71b6-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e71b6-112">Parent elements</span></span>

|<span data-ttu-id="e71b6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e71b6-113">**Element**</span></span>|<span data-ttu-id="e71b6-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e71b6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e71b6-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="e71b6-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="e71b6-116">Stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="e71b6-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e71b6-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="e71b6-117">Text value</span></span>

<span data-ttu-id="e71b6-118">In der folgenden Tabelle sind die möglichen Werte für das **SharingEffectiveRights** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e71b6-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
|<span data-ttu-id="e71b6-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e71b6-119">**Value**</span></span>|<span data-ttu-id="e71b6-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e71b6-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e71b6-121">Keine</span><span class="sxs-lookup"><span data-stu-id="e71b6-121">None</span></span>  <br/> |<span data-ttu-id="e71b6-122">Gibt an, dass der Benutzer nicht über die Berechtigung zum Anzeigen von Elementen im Kalender verfügt.</span><span class="sxs-lookup"><span data-stu-id="e71b6-122">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="e71b6-123">Nur einmal</span><span class="sxs-lookup"><span data-stu-id="e71b6-123">TimeOnly</span></span>  <br/> |<span data-ttu-id="e71b6-124">Gibt an, dass der Benutzer berechtigt ist, nur die Frei/Gebucht-Zeit im Kalender anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e71b6-124">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="e71b6-125">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="e71b6-125">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="e71b6-126">Gibt an, dass der Benutzer über die Berechtigung zum Anzeigen der Frei/Gebucht-Zeit im Kalender sowie Betreff und Ort von Terminen verfügt.</span><span class="sxs-lookup"><span data-stu-id="e71b6-126">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="e71b6-127">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e71b6-127">FullDetails</span></span>  <br/> |<span data-ttu-id="e71b6-128">Gibt an, dass der Benutzer über die Berechtigung zum Anzeigen aller Elemente im Kalender verfügt, einschließlich Frei/Gebucht-Zeit und Betreff, Ort und Details von Terminen.</span><span class="sxs-lookup"><span data-stu-id="e71b6-128">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e71b6-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e71b6-129">Remarks</span></span>

<span data-ttu-id="e71b6-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e71b6-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e71b6-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e71b6-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e71b6-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e71b6-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e71b6-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e71b6-133">Schema Name</span></span>  <br/> |<span data-ttu-id="e71b6-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e71b6-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="e71b6-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e71b6-135">Validation File</span></span>  <br/> |<span data-ttu-id="e71b6-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e71b6-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e71b6-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e71b6-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="e71b6-138">False</span><span class="sxs-lookup"><span data-stu-id="e71b6-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e71b6-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e71b6-139">See also</span></span>



- [<span data-ttu-id="e71b6-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e71b6-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

