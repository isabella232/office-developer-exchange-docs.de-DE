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
description: Das DelegatePermissions-Element enthält die Stell Vertretungs Einstellungen auf Berechtigungsebene für einen Benutzer. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 2cf8c9a8d3c5db8e13d43c207df173c12fca5acb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457410"
---
# <a name="delegatepermissions"></a><span data-ttu-id="67209-104">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="67209-104">DelegatePermissions</span></span>

<span data-ttu-id="67209-105">Das **DelegatePermissions** -Element enthält die Stell Vertretungs Einstellungen auf Berechtigungsebene für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="67209-105">The **DelegatePermissions** element contains the delegate permission-level settings for a user.</span></span> <span data-ttu-id="67209-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="67209-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
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

<span data-ttu-id="67209-107">**DelegatePermissionsType**</span><span class="sxs-lookup"><span data-stu-id="67209-107">**DelegatePermissionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="67209-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="67209-108">Attributes and elements</span></span>

<span data-ttu-id="67209-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="67209-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67209-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="67209-110">Attributes</span></span>

<span data-ttu-id="67209-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="67209-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67209-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67209-112">Child elements</span></span>

|<span data-ttu-id="67209-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="67209-113">**Element**</span></span>|<span data-ttu-id="67209-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67209-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67209-115">CalendarFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="67209-115">CalendarFolderPermissionLevel</span></span>](calendarfolderpermissionlevel.md) <br/> |<span data-ttu-id="67209-116">Enthält die Berechtigungen für den Standardordner Kalender.</span><span class="sxs-lookup"><span data-stu-id="67209-116">Contains the permissions for the default Calendar folder.</span></span> <span data-ttu-id="67209-117">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="67209-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="67209-118">TasksFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="67209-118">TasksFolderPermissionLevel</span></span>](tasksfolderpermissionlevel.md) <br/> |<span data-ttu-id="67209-119">Enthält die Berechtigungen für den Standardaufgabenordner.</span><span class="sxs-lookup"><span data-stu-id="67209-119">Contains the permissions for the default Task folder.</span></span> <span data-ttu-id="67209-120">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="67209-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="67209-121">InboxFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="67209-121">InboxFolderPermissionLevel</span></span>](inboxfolderpermissionlevel.md) <br/> |<span data-ttu-id="67209-122">Enthält die Berechtigungen für den standardmäßigen Posteingangsordner.</span><span class="sxs-lookup"><span data-stu-id="67209-122">Contains the permissions for the default Inbox folder.</span></span> <span data-ttu-id="67209-123">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="67209-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="67209-124">ContactsFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="67209-124">ContactsFolderPermissionLevel</span></span>](contactsfolderpermissionlevel.md) <br/> |<span data-ttu-id="67209-125">Enthält die Berechtigungen für den Standardordner Kontakte.</span><span class="sxs-lookup"><span data-stu-id="67209-125">Contains the permissions for the default Contacts folder.</span></span> <span data-ttu-id="67209-126">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="67209-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="67209-127">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="67209-127">NotesFolderPermissionLevel</span></span>](notesfolderpermissionlevel.md) <br/> |<span data-ttu-id="67209-128">Enthält die Berechtigungen für den standardmäßigen Notizenordner.</span><span class="sxs-lookup"><span data-stu-id="67209-128">Contains the permissions for the default Notes folder.</span></span> <span data-ttu-id="67209-129">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="67209-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="67209-130">JournalFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="67209-130">JournalFolderPermissionLevel</span></span>](journalfolderpermissionlevel.md) <br/> |<span data-ttu-id="67209-131">Enthält die Berechtigungen für den standardmäßigen Journal Ordner.</span><span class="sxs-lookup"><span data-stu-id="67209-131">Contains the permissions for the default Journal folder.</span></span> <span data-ttu-id="67209-132">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="67209-132">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="67209-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67209-133">Parent elements</span></span>

|<span data-ttu-id="67209-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="67209-134">**Element**</span></span>|<span data-ttu-id="67209-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67209-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67209-136">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="67209-136">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="67209-137">Bezeichnet einen einzelnen Delegaten, der in einem Postfach hinzugefügt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="67209-137">Identifies a single delegate to add or update in a mailbox.</span></span> <span data-ttu-id="67209-138">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="67209-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67209-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67209-139">Remarks</span></span>

<span data-ttu-id="67209-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="67209-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67209-141">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="67209-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67209-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="67209-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="67209-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="67209-143">Schema Name</span></span>  <br/> |<span data-ttu-id="67209-144">Schematypen</span><span class="sxs-lookup"><span data-stu-id="67209-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="67209-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="67209-145">Validation File</span></span>  <br/> |<span data-ttu-id="67209-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="67209-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="67209-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="67209-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="67209-148">False</span><span class="sxs-lookup"><span data-stu-id="67209-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67209-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67209-149">See also</span></span>

- [<span data-ttu-id="67209-150">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="67209-150">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="67209-151">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="67209-151">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="67209-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="67209-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="67209-153">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="67209-153">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

