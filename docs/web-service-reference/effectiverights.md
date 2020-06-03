---
title: EffectiveRights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EffectiveRights
api_type:
- schema
ms.assetid: bf5278eb-3a1a-4d27-9d16-b8be043bb023
description: Das EffectiveRights-Element enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: 3055eb73056750508b48ead29136b56e7ce97ee9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459244"
---
# <a name="effectiverights"></a><span data-ttu-id="0fd28-104">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="0fd28-104">EffectiveRights</span></span>

<span data-ttu-id="0fd28-105">Das **EffectiveRights** -Element enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="0fd28-105">The **EffectiveRights** element contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="0fd28-106">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0fd28-106">This element is read-only.</span></span> 
  
```XML
<EffectiveRights>
   <CreateAssociated/>
   <CreateContents/>
   <CreateHierarchy/>
   <Delete/>
   <Modify/>
   <Read/>
   <ViewPrivateItems/>
</EffectiveRights>
```

 <span data-ttu-id="0fd28-107">**EffectiveRightsType**</span><span class="sxs-lookup"><span data-stu-id="0fd28-107">**EffectiveRightsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0fd28-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0fd28-108">Attributes and elements</span></span>

<span data-ttu-id="0fd28-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0fd28-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0fd28-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0fd28-110">Attributes</span></span>

<span data-ttu-id="0fd28-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0fd28-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0fd28-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0fd28-112">Child elements</span></span>

|<span data-ttu-id="0fd28-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0fd28-113">**Element**</span></span>|<span data-ttu-id="0fd28-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0fd28-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fd28-115">Createassociated</span><span class="sxs-lookup"><span data-stu-id="0fd28-115">CreateAssociated</span></span>](createassociated.md) <br/> |<span data-ttu-id="0fd28-116">Gibt an, ob ein Client eine zugeordnete Inhaltstabelle erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="0fd28-116">Indicates whether a client can create an associated contents table.</span></span> <span data-ttu-id="0fd28-117">Diese Eigenschaft wird nur für Folder-Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fd28-117">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-118">Createcontents</span><span class="sxs-lookup"><span data-stu-id="0fd28-118">CreateContents</span></span>](createcontents.md) <br/> |<span data-ttu-id="0fd28-119">Gibt an, ob ein Client eine Inhaltstabelle erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="0fd28-119">Indicates whether a client can create a contents table.</span></span> <span data-ttu-id="0fd28-120">Diese Eigenschaft wird nur für Folder-Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fd28-120">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-121">Createhierarchy</span><span class="sxs-lookup"><span data-stu-id="0fd28-121">CreateHierarchy</span></span>](createhierarchy.md) <br/> |<span data-ttu-id="0fd28-122">Gibt an, ob ein Client eine Hierarchietabelle erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="0fd28-122">Indicates whether a client can create a hierarchy table.</span></span> <span data-ttu-id="0fd28-123">Diese Eigenschaft wird nur für Folder-Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fd28-123">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-124">Löschen</span><span class="sxs-lookup"><span data-stu-id="0fd28-124">Delete</span></span>](delete.md) <br/> |<span data-ttu-id="0fd28-125">Gibt an, ob ein Client einen Ordner oder ein Element löschen kann.</span><span class="sxs-lookup"><span data-stu-id="0fd28-125">Indicates whether a client can delete a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-126">Modify</span><span class="sxs-lookup"><span data-stu-id="0fd28-126">Modify</span></span>](modify.md) <br/> |<span data-ttu-id="0fd28-127">Gibt an, ob ein Client einen Ordner oder ein Element ändern kann.</span><span class="sxs-lookup"><span data-stu-id="0fd28-127">Indicates whether a client can modify a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-128">Lesen</span><span class="sxs-lookup"><span data-stu-id="0fd28-128">Read</span></span>](read.md) <br/> |<span data-ttu-id="0fd28-129">Gibt an, ob ein Client einen Ordner oder ein Element lesen kann.</span><span class="sxs-lookup"><span data-stu-id="0fd28-129">Indicates whether a client can read a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-130">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="0fd28-130">ViewPrivateItems</span></span>](viewprivateitems.md) <br/> |<span data-ttu-id="0fd28-131">Gibt an, ob ein privates Element angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0fd28-131">Indicates whether a private item can be viewed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0fd28-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0fd28-132">Parent elements</span></span>

|<span data-ttu-id="0fd28-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="0fd28-133">**Element**</span></span>|<span data-ttu-id="0fd28-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0fd28-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fd28-135">Folder</span><span class="sxs-lookup"><span data-stu-id="0fd28-135">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="0fd28-136">Stellt einen Ordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-136">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-137">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="0fd28-137">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="0fd28-138">Stellt einen Aufgabenordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-138">Represents a tasks folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-139">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="0fd28-139">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="0fd28-140">Stellt einen Ordner Kontakte in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-140">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-141">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="0fd28-141">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="0fd28-142">Stellt einen Kalenderordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-142">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-143">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="0fd28-143">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="0fd28-144">Stellt einen Suchordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-144">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-145">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="0fd28-145">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="0fd28-146">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-146">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-147">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="0fd28-147">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="0fd28-148">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-148">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-149">DistributionList</span><span class="sxs-lookup"><span data-stu-id="0fd28-149">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="0fd28-150">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-150">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-151">Element</span><span class="sxs-lookup"><span data-stu-id="0fd28-151">Item</span></span>](item.md) <br/> |<span data-ttu-id="0fd28-152">Stellt ein generisches Exchange-Element dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-152">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-153">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="0fd28-153">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="0fd28-154">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-154">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-155">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="0fd28-155">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="0fd28-156">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-156">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-157">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="0fd28-157">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="0fd28-158">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-158">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-159">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="0fd28-159">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="0fd28-160">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-160">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-161">Message</span><span class="sxs-lookup"><span data-stu-id="0fd28-161">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0fd28-162">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-162">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-163">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0fd28-163">Task</span></span>](task.md) <br/> |<span data-ttu-id="0fd28-164">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-164">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0fd28-165">PostItem</span><span class="sxs-lookup"><span data-stu-id="0fd28-165">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="0fd28-166">Stellt ein Post-Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0fd28-166">Represents a post item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0fd28-167">Textwert</span><span class="sxs-lookup"><span data-stu-id="0fd28-167">Text value</span></span>

<span data-ttu-id="0fd28-168">Keine.</span><span class="sxs-lookup"><span data-stu-id="0fd28-168">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0fd28-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fd28-169">Remarks</span></span>

<span data-ttu-id="0fd28-170">**EffectiveRights** wird in den Antworten GetFolder, GetItem, FindFolder, FindItem, SyncFolderHierarchy und SyncFolderItems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0fd28-170">**EffectiveRights** is supported in the GetFolder, GetItem, FindFolder, FindItem, SyncFolderHierarchy, and SyncFolderItems responses.</span></span> <span data-ttu-id="0fd28-171">Die **EffectiveRights** -Eigenschaft wird in der **allproperties** -Form für Ordner und Elemente verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="0fd28-171">The **EffectiveRights** property is exposed in the **AllProperties** shape for folders and items.</span></span> 
  
<span data-ttu-id="0fd28-172">Diese **EffectiveRights** -Eigenschaft ermöglicht den Zugriff auf dieselben Informationen, die in der **MAPI** -Eigenschaft PR_ACCESS bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0fd28-172">This **EffectiveRights** property provides access to the same information that is provided in the **PR_ACCESS MAPI** property.</span></span> 
  
<span data-ttu-id="0fd28-173">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0fd28-173">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0fd28-174">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0fd28-174">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0fd28-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fd28-175">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0fd28-176">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0fd28-176">Schema Name</span></span>  <br/> |<span data-ttu-id="0fd28-177">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0fd28-177">Types schema</span></span>  <br/> |
|<span data-ttu-id="0fd28-178">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0fd28-178">Validation File</span></span>  <br/> |<span data-ttu-id="0fd28-179">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0fd28-179">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0fd28-180">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0fd28-180">Can be Empty</span></span>  <br/> |<span data-ttu-id="0fd28-181">False</span><span class="sxs-lookup"><span data-stu-id="0fd28-181">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0fd28-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fd28-182">See also</span></span>

- [<span data-ttu-id="0fd28-183">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0fd28-183">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="0fd28-184">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="0fd28-184">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

