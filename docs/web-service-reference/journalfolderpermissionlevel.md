---
title: JournalFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- JournalFolderPermissionLevel
api_type:
- schema
ms.assetid: 564525fa-cd95-4c1a-9d6c-3806be664579
description: Das JournalFolderPermissionLevel-Element enthält die Berechtigungen für den standardmäßigen Journal Ordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 5c0f30932eb3fbbeef1a8e34611deeb1ffef402c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529049"
---
# <a name="journalfolderpermissionlevel"></a><span data-ttu-id="73e0c-104">JournalFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="73e0c-104">JournalFolderPermissionLevel</span></span>

<span data-ttu-id="73e0c-105">Das **JournalFolderPermissionLevel** -Element enthält die Berechtigungen für den standardmäßigen Journal Ordner.</span><span class="sxs-lookup"><span data-stu-id="73e0c-105">The **JournalFolderPermissionLevel** element contains the permissions for the default Journal folder.</span></span> <span data-ttu-id="73e0c-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="73e0c-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<JournalFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</JournalFolderPermissionLevel>
```

 <span data-ttu-id="73e0c-107">**DelegateFolderPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="73e0c-107">**DelegateFolderPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73e0c-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="73e0c-108">Attributes and elements</span></span>

<span data-ttu-id="73e0c-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="73e0c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73e0c-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="73e0c-110">Attributes</span></span>

<span data-ttu-id="73e0c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="73e0c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="73e0c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73e0c-112">Child elements</span></span>

<span data-ttu-id="73e0c-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="73e0c-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="73e0c-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73e0c-114">Parent elements</span></span>

|<span data-ttu-id="73e0c-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="73e0c-115">**Element**</span></span>|<span data-ttu-id="73e0c-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73e0c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73e0c-117">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="73e0c-117">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="73e0c-118">Enthält die Einstellungen für die Stell Vertretungs Berechtigungsstufe für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="73e0c-118">Contains the delegate permission level settings for a user.</span></span> <span data-ttu-id="73e0c-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="73e0c-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="73e0c-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="73e0c-120">Text value</span></span>

<span data-ttu-id="73e0c-121">In der folgenden Tabelle sind die Textwerte aufgeführt, die die Berechtigungsstufen darstellen.</span><span class="sxs-lookup"><span data-stu-id="73e0c-121">The following table lists the text values that represent the permission levels.</span></span>
  
<span data-ttu-id="73e0c-122">**Text Werte für Berechtigungsstufen**</span><span class="sxs-lookup"><span data-stu-id="73e0c-122">**Permission level text values**</span></span>

|<span data-ttu-id="73e0c-123">**Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="73e0c-123">**Permission level**</span></span>|<span data-ttu-id="73e0c-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73e0c-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73e0c-125">Keine</span><span class="sxs-lookup"><span data-stu-id="73e0c-125">None</span></span>  <br/> |<span data-ttu-id="73e0c-126">Der Stellvertreter Benutzer verfügt über keine Zugriffsberechtigungen für den Ordner Journal.</span><span class="sxs-lookup"><span data-stu-id="73e0c-126">The delegate user has no access permissions to the Journal folder.</span></span>  <br/> |
|<span data-ttu-id="73e0c-127">Reviewer</span><span class="sxs-lookup"><span data-stu-id="73e0c-127">Reviewer</span></span>  <br/> |<span data-ttu-id="73e0c-128">Der Stellvertreter-Benutzer kann Elemente im Journal Ordner lesen.</span><span class="sxs-lookup"><span data-stu-id="73e0c-128">The delegate user can read items in the Journal folder.</span></span>  <br/> |
|<span data-ttu-id="73e0c-129">Ursprung</span><span class="sxs-lookup"><span data-stu-id="73e0c-129">Author</span></span>  <br/> |<span data-ttu-id="73e0c-130">Der Stellvertreter Benutzer kann Elemente im Journal Ordner lesen und erstellen.</span><span class="sxs-lookup"><span data-stu-id="73e0c-130">The delegate user can read and create items in the Journal folder.</span></span>  <br/> |
|<span data-ttu-id="73e0c-131">Editor</span><span class="sxs-lookup"><span data-stu-id="73e0c-131">Editor</span></span>  <br/> |<span data-ttu-id="73e0c-132">Der Stellvertreter Benutzer kann Elemente im Journal Ordner lesen, erstellen und ändern.</span><span class="sxs-lookup"><span data-stu-id="73e0c-132">The delegate user can read, create, and modify items in the Journal folder.</span></span>  <br/> |
|<span data-ttu-id="73e0c-133">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="73e0c-133">Custom</span></span>  <br/> |<span data-ttu-id="73e0c-134">Der Stellvertreter Benutzer verfügt über benutzerdefinierte Zugriffsberechtigungen für den Ordner Journal.</span><span class="sxs-lookup"><span data-stu-id="73e0c-134">The delegate user has custom access permissions to the Journal folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73e0c-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73e0c-135">Remarks</span></span>

<span data-ttu-id="73e0c-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="73e0c-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73e0c-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="73e0c-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73e0c-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="73e0c-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="73e0c-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="73e0c-139">Schema Name</span></span>  <br/> |<span data-ttu-id="73e0c-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="73e0c-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="73e0c-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="73e0c-141">Validation File</span></span>  <br/> |<span data-ttu-id="73e0c-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="73e0c-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="73e0c-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="73e0c-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="73e0c-144">False</span><span class="sxs-lookup"><span data-stu-id="73e0c-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73e0c-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73e0c-145">See also</span></span>



[<span data-ttu-id="73e0c-146">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="73e0c-146">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="73e0c-147">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="73e0c-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="73e0c-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="73e0c-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="73e0c-149">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="73e0c-149">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

