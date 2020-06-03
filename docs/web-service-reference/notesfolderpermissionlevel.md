---
title: NotesFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NotesFolderPermissionLevel
api_type:
- schema
ms.assetid: 76a2520c-f453-4fd7-b3eb-1c5f4666680a
description: Das NotesFolderPermissionLevel-Element enthält die Berechtigungen für den standardmäßigen Notizenordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 205802592a1fc01451b4fc497e9e0c4c66afd478
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462626"
---
# <a name="notesfolderpermissionlevel"></a><span data-ttu-id="548e2-104">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="548e2-104">NotesFolderPermissionLevel</span></span>

<span data-ttu-id="548e2-105">Das **NotesFolderPermissionLevel** -Element enthält die Berechtigungen für den standardmäßigen Notizenordner.</span><span class="sxs-lookup"><span data-stu-id="548e2-105">The **NotesFolderPermissionLevel** element contains the permissions for the default Notes folder.</span></span> <span data-ttu-id="548e2-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="548e2-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<NotesFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</NotesFolderPermissionLevel>
```

 <span data-ttu-id="548e2-107">**DelegateFolderPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="548e2-107">**DelegateFolderPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="548e2-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="548e2-108">Attributes and elements</span></span>

<span data-ttu-id="548e2-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="548e2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="548e2-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="548e2-110">Attributes</span></span>

<span data-ttu-id="548e2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="548e2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="548e2-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="548e2-112">Child elements</span></span>

<span data-ttu-id="548e2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="548e2-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="548e2-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="548e2-114">Parent elements</span></span>

|<span data-ttu-id="548e2-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="548e2-115">**Element**</span></span>|<span data-ttu-id="548e2-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="548e2-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="548e2-117">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="548e2-117">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="548e2-118">Enthält die Einstellungen für die Stell Vertretungs Berechtigungsstufe für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="548e2-118">Contains the delegate permission level settings for a user.</span></span> <span data-ttu-id="548e2-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="548e2-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="548e2-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="548e2-120">Text value</span></span>

<span data-ttu-id="548e2-121">In der folgenden Tabelle sind die Textwerte aufgeführt, die die Berechtigungsstufen darstellen.</span><span class="sxs-lookup"><span data-stu-id="548e2-121">The following table lists the text values that represent the permission levels.</span></span>
  
<span data-ttu-id="548e2-122">**Text Werte für Berechtigungsstufen**</span><span class="sxs-lookup"><span data-stu-id="548e2-122">**Permission level text values**</span></span>

|<span data-ttu-id="548e2-123">**Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="548e2-123">**Permission level**</span></span>|<span data-ttu-id="548e2-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="548e2-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="548e2-125">Keine</span><span class="sxs-lookup"><span data-stu-id="548e2-125">None</span></span>  <br/> |<span data-ttu-id="548e2-126">Der Stellvertreter Benutzer verfügt über keine Zugriffsberechtigungen für den Ordner Notizen.</span><span class="sxs-lookup"><span data-stu-id="548e2-126">The delegate user has no access permissions to the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="548e2-127">Reviewer</span><span class="sxs-lookup"><span data-stu-id="548e2-127">Reviewer</span></span>  <br/> |<span data-ttu-id="548e2-128">Der Stellvertreter kann Elemente im Ordner "Notizen" lesen.</span><span class="sxs-lookup"><span data-stu-id="548e2-128">The delegate user can read items in the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="548e2-129">Ursprung</span><span class="sxs-lookup"><span data-stu-id="548e2-129">Author</span></span>  <br/> |<span data-ttu-id="548e2-130">Der Stellvertreter Benutzer kann Elemente im Ordner "Notizen" lesen und erstellen.</span><span class="sxs-lookup"><span data-stu-id="548e2-130">The delegate user can read and create items in the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="548e2-131">Editor</span><span class="sxs-lookup"><span data-stu-id="548e2-131">Editor</span></span>  <br/> |<span data-ttu-id="548e2-132">Der Stellvertreter Benutzer kann Elemente im Ordner "Notizen" lesen, erstellen und ändern.</span><span class="sxs-lookup"><span data-stu-id="548e2-132">The delegate user can read, create, and modify items in the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="548e2-133">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="548e2-133">Custom</span></span>  <br/> |<span data-ttu-id="548e2-134">Der Stellvertreter Benutzer verfügt über benutzerdefinierte Zugriffsberechtigungen für den Ordner Notizen.</span><span class="sxs-lookup"><span data-stu-id="548e2-134">The delegate user has custom access permissions to the Notes folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="548e2-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="548e2-135">Remarks</span></span>

<span data-ttu-id="548e2-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="548e2-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="548e2-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="548e2-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="548e2-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="548e2-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="548e2-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="548e2-139">Schema Name</span></span>  <br/> |<span data-ttu-id="548e2-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="548e2-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="548e2-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="548e2-141">Validation File</span></span>  <br/> |<span data-ttu-id="548e2-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="548e2-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="548e2-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="548e2-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="548e2-144">False</span><span class="sxs-lookup"><span data-stu-id="548e2-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="548e2-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="548e2-145">See also</span></span>



[<span data-ttu-id="548e2-146">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="548e2-146">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="548e2-147">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="548e2-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="548e2-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="548e2-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="548e2-149">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="548e2-149">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

