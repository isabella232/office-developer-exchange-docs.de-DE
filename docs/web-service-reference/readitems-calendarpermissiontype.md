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
description: Das ReadItems-Element gibt an, ob ein Benutzer über Berechtigungen zum Lesen von Elementen in einem Kalenderordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 532b90c47cca7117a89d59e7012436268be9ebb0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830964"
---
# <a name="readitems-calendarpermissiontype"></a><span data-ttu-id="610e8-104">ReadItems (CalendarPermissionType)</span><span class="sxs-lookup"><span data-stu-id="610e8-104">ReadItems (CalendarPermissionType)</span></span>

<span data-ttu-id="610e8-105">Das **ReadItems** -Element gibt an, ob ein Benutzer über Berechtigungen zum Lesen von Elementen in einem Kalenderordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="610e8-105">The **ReadItems** element indicates whether a user has permission to read items within a Calendar folder.</span></span> <span data-ttu-id="610e8-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="610e8-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReadItems>None or TimeOnly or TimeAndSubjectAndLocation or FullDetails</ReadItems>
```

 <span data-ttu-id="610e8-107">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="610e8-107">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="610e8-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="610e8-108">Attributes and elements</span></span>

<span data-ttu-id="610e8-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="610e8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="610e8-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="610e8-110">Attributes</span></span>

<span data-ttu-id="610e8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="610e8-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="610e8-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="610e8-112">Child elements</span></span>

<span data-ttu-id="610e8-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="610e8-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="610e8-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="610e8-114">Parent elements</span></span>

|<span data-ttu-id="610e8-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="610e8-115">**Element**</span></span>|<span data-ttu-id="610e8-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="610e8-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="610e8-117">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="610e8-117">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="610e8-p103">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="610e8-p103">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="610e8-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="610e8-120">Text value</span></span>

<span data-ttu-id="610e8-121">Die folgende Tabelle enthält die möglichen Werte für das **ReadItems** -Element.</span><span class="sxs-lookup"><span data-stu-id="610e8-121">The following table lists the possible values for the **ReadItems** element.</span></span> 
  
<span data-ttu-id="610e8-122">**ReadItems Elementwerte text**</span><span class="sxs-lookup"><span data-stu-id="610e8-122">**ReadItems element text values**</span></span>

|<span data-ttu-id="610e8-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="610e8-123">**Value**</span></span>|<span data-ttu-id="610e8-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="610e8-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="610e8-125">Keine</span><span class="sxs-lookup"><span data-stu-id="610e8-125">None</span></span>  <br/> |<span data-ttu-id="610e8-126">Gibt an, dass der Benutzer die Berechtigung zum Anzeigen von Elementen im Kalender nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="610e8-126">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="610e8-127">TimeOnly</span><span class="sxs-lookup"><span data-stu-id="610e8-127">TimeOnly</span></span>  <br/> |<span data-ttu-id="610e8-128">Gibt an, dass der Benutzer die Berechtigung zum Anzeigen der nur Frei/Gebucht-Zeit im Kalender hat.</span><span class="sxs-lookup"><span data-stu-id="610e8-128">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="610e8-129">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="610e8-129">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="610e8-130">Gibt an, dass der Benutzer über die Berechtigung zum Anzeigen von Frei/Gebucht-Zeit in den Kalender und den Betreff und Ort von Terminen verfügt.</span><span class="sxs-lookup"><span data-stu-id="610e8-130">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="610e8-131">FullDetails</span><span class="sxs-lookup"><span data-stu-id="610e8-131">FullDetails</span></span>  <br/> |<span data-ttu-id="610e8-132">Gibt an, dass der Benutzer die Berechtigung zum Anzeigen aller Elemente im Kalender, einschließlich der Frei/Gebucht-Zeit und Betreff, Ort und Details von Terminen verfügt.</span><span class="sxs-lookup"><span data-stu-id="610e8-132">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="610e8-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="610e8-133">Remarks</span></span>

<span data-ttu-id="610e8-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="610e8-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="610e8-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="610e8-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="610e8-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="610e8-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="610e8-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="610e8-137">Schema Name</span></span>  <br/> |<span data-ttu-id="610e8-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="610e8-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="610e8-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="610e8-139">Validation File</span></span>  <br/> |<span data-ttu-id="610e8-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="610e8-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="610e8-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="610e8-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="610e8-142">False</span><span class="sxs-lookup"><span data-stu-id="610e8-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="610e8-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="610e8-143">See also</span></span>



- [<span data-ttu-id="610e8-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="610e8-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="610e8-145">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="610e8-145">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

