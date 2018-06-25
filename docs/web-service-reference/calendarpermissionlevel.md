---
title: CalendarPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermissionLevel
api_type:
- schema
ms.assetid: 6ac2b792-4326-4a3f-b6cb-977bf523b5b2
description: Das CalendarPermissionLevel-Element darstellt, die Berechtigungsstufe, die ein Benutzer für einen Kalenderordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 646e4df3b70350a16cdd1f3e134260c2984a5161
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757538"
---
# <a name="calendarpermissionlevel"></a><span data-ttu-id="ec840-104">CalendarPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="ec840-104">CalendarPermissionLevel</span></span>

<span data-ttu-id="ec840-105">Das **CalendarPermissionLevel** -Element darstellt, die Berechtigungsstufe, die ein Benutzer für einen Kalenderordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="ec840-105">The **CalendarPermissionLevel** element represents the permission level that a user has on a Calendar folder.</span></span> <span data-ttu-id="ec840-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ec840-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CalendarPermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or FreeBusyTimeOnly or FreeBusyTimeAndSubjectAndLocation or Custom</CalendarPermissionLevel>
```

 <span data-ttu-id="ec840-107">**CalendarPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="ec840-107">**CalendarPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec840-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ec840-108">Attributes and elements</span></span>

<span data-ttu-id="ec840-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ec840-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec840-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ec840-110">Attributes</span></span>

<span data-ttu-id="ec840-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec840-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec840-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec840-112">Child elements</span></span>

<span data-ttu-id="ec840-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec840-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ec840-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec840-114">Parent elements</span></span>

|<span data-ttu-id="ec840-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec840-115">**Element**</span></span>|<span data-ttu-id="ec840-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec840-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec840-117">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="ec840-117">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="ec840-p103">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ec840-p103">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ec840-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="ec840-120">Text value</span></span>

<span data-ttu-id="ec840-121">Die folgende Tabelle enthält die möglichen Werte für das **CalendarPermissionLevel** -Element.</span><span class="sxs-lookup"><span data-stu-id="ec840-121">The following table lists the possible values for the **CalendarPermissionLevel** element.</span></span> 
  
<span data-ttu-id="ec840-122">**Text-Elementwerte CalendarPermissionLevel**</span><span class="sxs-lookup"><span data-stu-id="ec840-122">**CalendarPermissionLevel element text values**</span></span>

|<span data-ttu-id="ec840-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ec840-123">**Value**</span></span>|<span data-ttu-id="ec840-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec840-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec840-125">Keine</span><span class="sxs-lookup"><span data-stu-id="ec840-125">None</span></span>  <br/> |<span data-ttu-id="ec840-126">Gibt an, dass der Benutzer keine Berechtigungen für den Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="ec840-126">Indicates that the user has no permissions on the folder.</span></span>  <br/> |
|<span data-ttu-id="ec840-127">Besitzer</span><span class="sxs-lookup"><span data-stu-id="ec840-127">Owner</span></span>  <br/> |<span data-ttu-id="ec840-128">Gibt an, dass der Benutzer kann erstellen, lesen, bearbeiten und löschen alle Elemente im Ordner und Unterordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec840-128">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span> <span data-ttu-id="ec840-129">Der Benutzer ist Besitzer des Ordners und Ordner Kontakt.</span><span class="sxs-lookup"><span data-stu-id="ec840-129">The user is both folder owner and folder contact.</span></span>  <br/> |
|<span data-ttu-id="ec840-130">Vom Typ PublishingEditor</span><span class="sxs-lookup"><span data-stu-id="ec840-130">PublishingEditor</span></span>  <br/> |<span data-ttu-id="ec840-131">Gibt an, dass der Benutzer kann erstellen, lesen, bearbeiten und löschen alle Elemente im Ordner und Unterordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec840-131">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="ec840-132">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="ec840-132">Editor</span></span>  <br/> |<span data-ttu-id="ec840-133">Gibt an, dass der Benutzer erstellen, lesen, bearbeiten und löschen kann alle Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="ec840-133">Indicates that the user can create, read, edit and delete all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="ec840-134">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="ec840-134">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="ec840-135">Gibt an, dass der Benutzer kann erstellen und Lesen aller Elemente im Ordner, bearbeiten und Löschen nur Elemente, die der Benutzer erstellt und Unterordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec840-135">Indicates that the user can create and read all items in the folder, edit and delete only items that the user creates, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="ec840-136">Autor</span><span class="sxs-lookup"><span data-stu-id="ec840-136">Author</span></span>  <br/> |<span data-ttu-id="ec840-137">Gibt an, dass der Benutzer erstellen und aller Elemente in den Ordner lesen und bearbeiten und löschen kann nur Elemente, die der Benutzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="ec840-137">Indicates that the user can create and read all items in the folder, and edit and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="ec840-138">NoneditingAuthor</span><span class="sxs-lookup"><span data-stu-id="ec840-138">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="ec840-139">Gibt an, dass der Benutzer kann erstellen und alle Elemente im Ordner lesen und nur Elemente löschen, die der Benutzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="ec840-139">Indicates that the user can create and read all items in the folder, and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="ec840-140">Prüfer</span><span class="sxs-lookup"><span data-stu-id="ec840-140">Reviewer</span></span>  <br/> |<span data-ttu-id="ec840-141">Gibt an, dass der Benutzer alle Elemente im Ordner lesen kann.</span><span class="sxs-lookup"><span data-stu-id="ec840-141">Indicates that the user can read all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="ec840-142">Mitwirkender</span><span class="sxs-lookup"><span data-stu-id="ec840-142">Contributor</span></span>  <br/> |<span data-ttu-id="ec840-143">Gibt an, dass der Benutzer Elemente im Ordner erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ec840-143">Indicates that the user can create items in the folder.</span></span> <span data-ttu-id="ec840-144">Der Inhalt des Ordners wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ec840-144">The contents of the folder do not appear.</span></span>  <br/> |
|<span data-ttu-id="ec840-145">FreeBusyTimeOnly</span><span class="sxs-lookup"><span data-stu-id="ec840-145">FreeBusyTimeOnly</span></span>  <br/> |<span data-ttu-id="ec840-146">Gibt an, dass der Benutzer nur Frei/Gebucht-Zeit im Kalender anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="ec840-146">Indicates that the user can view only free/busy time within the calendar.</span></span>  <br/> |
|<span data-ttu-id="ec840-147">FreeBusyTimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="ec840-147">FreeBusyTimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="ec840-148">Gibt an, dass der Benutzer die Frei/Gebucht-Zeiten in den Kalender und den Betreff und Ort von Terminen anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="ec840-148">Indicates that the user can view free/busy time within the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="ec840-149">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="ec840-149">Custom</span></span>  <br/> |<span data-ttu-id="ec840-150">Gibt an, dass der Benutzer benutzerdefinierte Zugriffsberechtigungen für den Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="ec840-150">Indicates that the user has custom access permissions on the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec840-151">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec840-151">Remarks</span></span>

<span data-ttu-id="ec840-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ec840-152">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec840-153">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ec840-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec840-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec840-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ec840-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ec840-155">Schema Name</span></span>  <br/> |<span data-ttu-id="ec840-156">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ec840-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="ec840-157">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ec840-157">Validation File</span></span>  <br/> |<span data-ttu-id="ec840-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ec840-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ec840-159">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ec840-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec840-160">False</span><span class="sxs-lookup"><span data-stu-id="ec840-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec840-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec840-161">See also</span></span>



- [<span data-ttu-id="ec840-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec840-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ec840-163">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="ec840-163">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

