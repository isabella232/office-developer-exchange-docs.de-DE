---
title: DelegatePermissions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegatePermissions
api_type:
- schema
ms.assetid: 292badc7-bab3-4368-9d7c-9a8b7edb279b
description: Das DelegatePermissions-Element enthält die Stellvertretung Berechtigungsstufe Einstellungen für einen Benutzer. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 319592b6c3386a07b3094115c335c7fb8ffe1130
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757892"
---
# <a name="delegatepermissions"></a><span data-ttu-id="eda21-104">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="eda21-104">DelegatePermissions</span></span>

<span data-ttu-id="eda21-105">Das **DelegatePermissions** -Element enthält die Stellvertretung Berechtigungsstufe Einstellungen für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="eda21-105">The **DelegatePermissions** element contains the delegate permission-level settings for a user.</span></span> <span data-ttu-id="eda21-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eda21-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegatePermissions>
   <CalendarFolderPermissionLevel/>
   <TasksFolderPermissionLevel/>
   <InboxFolderPermissionLevel/>
   <ContactsFolderPermissionLevel/>
   <NotesFolderPermissionLevel/>
   <JournalFolderPermissionLevel/>
</DelegatePermissions>
```

<span data-ttu-id="eda21-107">**DelegatePermissionsType**</span><span class="sxs-lookup"><span data-stu-id="eda21-107">**DelegatePermissionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="eda21-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="eda21-108">Attributes and elements</span></span>

<span data-ttu-id="eda21-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="eda21-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eda21-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="eda21-110">Attributes</span></span>

<span data-ttu-id="eda21-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="eda21-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eda21-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eda21-112">Child elements</span></span>

|<span data-ttu-id="eda21-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="eda21-113">**Element**</span></span>|<span data-ttu-id="eda21-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eda21-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eda21-115">CalendarFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="eda21-115">CalendarFolderPermissionLevel</span></span>](calendarfolderpermissionlevel.md) <br/> |<span data-ttu-id="eda21-116">Enthält die Berechtigungen für den Standardordner Kalender.</span><span class="sxs-lookup"><span data-stu-id="eda21-116">Contains the permissions for the default Calendar folder.</span></span> <span data-ttu-id="eda21-117">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eda21-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="eda21-118">TasksFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="eda21-118">TasksFolderPermissionLevel</span></span>](tasksfolderpermissionlevel.md) <br/> |<span data-ttu-id="eda21-119">Enthält die Berechtigungen für den Standardordner für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="eda21-119">Contains the permissions for the default Task folder.</span></span> <span data-ttu-id="eda21-120">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eda21-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="eda21-121">InboxFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="eda21-121">InboxFolderPermissionLevel</span></span>](inboxfolderpermissionlevel.md) <br/> |<span data-ttu-id="eda21-122">Enthält die Berechtigungen für den Standardordner Posteingang.</span><span class="sxs-lookup"><span data-stu-id="eda21-122">Contains the permissions for the default Inbox folder.</span></span> <span data-ttu-id="eda21-123">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eda21-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="eda21-124">ContactsFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="eda21-124">ContactsFolderPermissionLevel</span></span>](contactsfolderpermissionlevel.md) <br/> |<span data-ttu-id="eda21-125">Enthält die Berechtigungen für den Standardordner Kontakte.</span><span class="sxs-lookup"><span data-stu-id="eda21-125">Contains the permissions for the default Contacts folder.</span></span> <span data-ttu-id="eda21-126">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eda21-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="eda21-127">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="eda21-127">NotesFolderPermissionLevel</span></span>](notesfolderpermissionlevel.md) <br/> |<span data-ttu-id="eda21-128">Enthält die Berechtigungen für den Standardordner Notizen.</span><span class="sxs-lookup"><span data-stu-id="eda21-128">Contains the permissions for the default Notes folder.</span></span> <span data-ttu-id="eda21-129">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eda21-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="eda21-130">JournalFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="eda21-130">JournalFolderPermissionLevel</span></span>](journalfolderpermissionlevel.md) <br/> |<span data-ttu-id="eda21-131">Enthält die Berechtigungen für den Standardordner Journal.</span><span class="sxs-lookup"><span data-stu-id="eda21-131">Contains the permissions for the default Journal folder.</span></span> <span data-ttu-id="eda21-132">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eda21-132">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eda21-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eda21-133">Parent elements</span></span>

|<span data-ttu-id="eda21-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="eda21-134">**Element**</span></span>|<span data-ttu-id="eda21-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eda21-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eda21-136">Beauftragte Benutzer</span><span class="sxs-lookup"><span data-stu-id="eda21-136">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="eda21-137">Identifiziert einen einzelnen Delegaten hinzufügen oder aktualisieren in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="eda21-137">Identifies a single delegate to add or update in a mailbox.</span></span> <span data-ttu-id="eda21-138">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eda21-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eda21-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eda21-139">Remarks</span></span>

<span data-ttu-id="eda21-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="eda21-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eda21-141">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="eda21-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eda21-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="eda21-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eda21-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="eda21-143">Schema Name</span></span>  <br/> |<span data-ttu-id="eda21-144">Schematypen</span><span class="sxs-lookup"><span data-stu-id="eda21-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="eda21-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="eda21-145">Validation File</span></span>  <br/> |<span data-ttu-id="eda21-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eda21-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eda21-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="eda21-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="eda21-148">False</span><span class="sxs-lookup"><span data-stu-id="eda21-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eda21-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eda21-149">See also</span></span>

- [<span data-ttu-id="eda21-150">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="eda21-150">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="eda21-151">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="eda21-151">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="eda21-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="eda21-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="eda21-153">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="eda21-153">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

