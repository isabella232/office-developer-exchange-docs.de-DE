---
title: ReadItems (CalendarPermissionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReadItems
api_type:
- schema
ms.assetid: bec01982-26a1-4373-b1e6-2e0c838d83c4
description: Das ReadItems-Element gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Kalenderordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: e040b643016781f9f890050f189191356f8d4f0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468299"
---
# <a name="readitems-calendarpermissiontype"></a><span data-ttu-id="b27f9-104">ReadItems (CalendarPermissionType)</span><span class="sxs-lookup"><span data-stu-id="b27f9-104">ReadItems (CalendarPermissionType)</span></span>

<span data-ttu-id="b27f9-105">Das **ReadItems** -Element gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Kalenderordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="b27f9-105">The **ReadItems** element indicates whether a user has permission to read items within a Calendar folder.</span></span> <span data-ttu-id="b27f9-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b27f9-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReadItems>None or TimeOnly or TimeAndSubjectAndLocation or FullDetails</ReadItems>
```

 <span data-ttu-id="b27f9-107">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="b27f9-107">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b27f9-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b27f9-108">Attributes and elements</span></span>

<span data-ttu-id="b27f9-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b27f9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b27f9-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="b27f9-110">Attributes</span></span>

<span data-ttu-id="b27f9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b27f9-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b27f9-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b27f9-112">Child elements</span></span>

<span data-ttu-id="b27f9-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b27f9-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b27f9-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b27f9-114">Parent elements</span></span>

|<span data-ttu-id="b27f9-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="b27f9-115">**Element**</span></span>|<span data-ttu-id="b27f9-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b27f9-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b27f9-117">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="b27f9-117">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="b27f9-p103">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b27f9-p103">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b27f9-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="b27f9-120">Text value</span></span>

<span data-ttu-id="b27f9-121">In der folgenden Tabelle sind die möglichen Werte für das **ReadItems** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b27f9-121">The following table lists the possible values for the **ReadItems** element.</span></span> 
  
<span data-ttu-id="b27f9-122">**ReadItems-Element Text Werte**</span><span class="sxs-lookup"><span data-stu-id="b27f9-122">**ReadItems element text values**</span></span>

|<span data-ttu-id="b27f9-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b27f9-123">**Value**</span></span>|<span data-ttu-id="b27f9-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b27f9-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b27f9-125">Keine</span><span class="sxs-lookup"><span data-stu-id="b27f9-125">None</span></span>  <br/> |<span data-ttu-id="b27f9-126">Gibt an, dass der Benutzer nicht über die Berechtigung zum Anzeigen von Elementen im Kalender verfügt.</span><span class="sxs-lookup"><span data-stu-id="b27f9-126">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="b27f9-127">Nur einmal</span><span class="sxs-lookup"><span data-stu-id="b27f9-127">TimeOnly</span></span>  <br/> |<span data-ttu-id="b27f9-128">Gibt an, dass der Benutzer berechtigt ist, nur die Frei/Gebucht-Zeit im Kalender anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b27f9-128">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="b27f9-129">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="b27f9-129">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="b27f9-130">Gibt an, dass der Benutzer über die Berechtigung zum Anzeigen der Frei/Gebucht-Zeit im Kalender sowie Betreff und Ort von Terminen verfügt.</span><span class="sxs-lookup"><span data-stu-id="b27f9-130">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="b27f9-131">FullDetails</span><span class="sxs-lookup"><span data-stu-id="b27f9-131">FullDetails</span></span>  <br/> |<span data-ttu-id="b27f9-132">Gibt an, dass der Benutzer über die Berechtigung zum Anzeigen aller Elemente im Kalender verfügt, einschließlich Frei/Gebucht-Zeit und Betreff, Ort und Details von Terminen.</span><span class="sxs-lookup"><span data-stu-id="b27f9-132">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b27f9-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b27f9-133">Remarks</span></span>

<span data-ttu-id="b27f9-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b27f9-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b27f9-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b27f9-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b27f9-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="b27f9-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b27f9-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b27f9-137">Schema Name</span></span>  <br/> |<span data-ttu-id="b27f9-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b27f9-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="b27f9-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b27f9-139">Validation File</span></span>  <br/> |<span data-ttu-id="b27f9-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b27f9-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b27f9-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b27f9-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="b27f9-142">False</span><span class="sxs-lookup"><span data-stu-id="b27f9-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b27f9-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b27f9-143">See also</span></span>



- [<span data-ttu-id="b27f9-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b27f9-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b27f9-145">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="b27f9-145">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

