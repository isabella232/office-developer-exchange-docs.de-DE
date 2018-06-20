---
title: TasksFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TasksFolderPermissionLevel
api_type:
- schema
ms.assetid: 0f70b79b-3443-4048-b410-692d4e2464fc
description: Das TasksFolderPermissionLevel-Element enthält die Berechtigungen für den Standardordner Aufgaben. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 49807896f9175bafbef106c41d1c9dff8f6178c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839161"
---
# <a name="tasksfolderpermissionlevel"></a><span data-ttu-id="d732d-104">TasksFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="d732d-104">TasksFolderPermissionLevel</span></span>

<span data-ttu-id="d732d-105">Das **TasksFolderPermissionLevel** -Element enthält die Berechtigungen für den Standardordner Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="d732d-105">The **TasksFolderPermissionLevel** element contains the permissions for the default Tasks folder.</span></span> <span data-ttu-id="d732d-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d732d-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<TasksFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</TasksFolderPermissionLevel>
```

<span data-ttu-id="d732d-107">**DelegateFolderPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="d732d-107">**DelegateFolderPermissionLevelType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d732d-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d732d-108">Attributes and elements</span></span>

<span data-ttu-id="d732d-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d732d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d732d-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d732d-110">Attributes</span></span>

<span data-ttu-id="d732d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d732d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d732d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d732d-112">Child elements</span></span>

<span data-ttu-id="d732d-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d732d-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d732d-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d732d-114">Parent elements</span></span>

|<span data-ttu-id="d732d-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d732d-115">**Element**</span></span>|<span data-ttu-id="d732d-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d732d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d732d-117">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="d732d-117">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="d732d-118">Die Stellvertretung die berechtigungseinstellungen auf Poolebene für einen Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="d732d-118">Contains the delegate permission level settings for a user.</span></span> <span data-ttu-id="d732d-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d732d-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d732d-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="d732d-120">Text value</span></span>

<span data-ttu-id="d732d-121">Die folgende Tabelle enthält die Textwerte, die die Berechtigungsstufen darstellen.</span><span class="sxs-lookup"><span data-stu-id="d732d-121">The following table lists the text values that represent the permission levels.</span></span>
  
<span data-ttu-id="d732d-122">**Ebene Text Berechtigungswerte**</span><span class="sxs-lookup"><span data-stu-id="d732d-122">**Permission level text values**</span></span>

|<span data-ttu-id="d732d-123">**Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="d732d-123">**Permission level**</span></span>|<span data-ttu-id="d732d-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d732d-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d732d-125">Keine</span><span class="sxs-lookup"><span data-stu-id="d732d-125">None</span></span>  <br/> |<span data-ttu-id="d732d-126">Stellvertretungsbenutzers verfügt über keine Access-Berechtigungen für den Ordner Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="d732d-126">The delegate user has no access permissions to the Tasks folder.</span></span>  <br/> |
|<span data-ttu-id="d732d-127">Prüfer</span><span class="sxs-lookup"><span data-stu-id="d732d-127">Reviewer</span></span>  <br/> |<span data-ttu-id="d732d-128">Stellvertretungsbenutzers kann Elemente im Ordner "Aufgaben" lesen.</span><span class="sxs-lookup"><span data-stu-id="d732d-128">The delegate user can read items in the Tasks folder.</span></span>  <br/> |
|<span data-ttu-id="d732d-129">Autor</span><span class="sxs-lookup"><span data-stu-id="d732d-129">Author</span></span>  <br/> |<span data-ttu-id="d732d-130">Stellvertretungsbenutzers lesen und Erstellen von Elementen im Ordner Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="d732d-130">The delegate user can read and create items in the Tasks folder.</span></span>  <br/> |
|<span data-ttu-id="d732d-131">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="d732d-131">Editor</span></span>  <br/> |<span data-ttu-id="d732d-132">Stellvertretungsbenutzers kann lesen, erstellen und Ändern von Elementen in den Ordner Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="d732d-132">The delegate user can read, create, and modify items in the Tasks folder.</span></span>  <br/> |
|<span data-ttu-id="d732d-133">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="d732d-133">Custom</span></span>  <br/> |<span data-ttu-id="d732d-134">Stellvertretungsbenutzers hat benutzerdefinierte Zugriffsberechtigungen für den Ordner Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="d732d-134">The delegate user has custom access permissions to the Tasks folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d732d-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d732d-135">Remarks</span></span>

<span data-ttu-id="d732d-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d732d-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d732d-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d732d-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d732d-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="d732d-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d732d-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d732d-139">Schema Name</span></span>  <br/> |<span data-ttu-id="d732d-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d732d-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="d732d-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d732d-141">Validation File</span></span>  <br/> |<span data-ttu-id="d732d-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d732d-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d732d-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d732d-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="d732d-144">False</span><span class="sxs-lookup"><span data-stu-id="d732d-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d732d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d732d-145">See also</span></span>

- [<span data-ttu-id="d732d-146">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d732d-146">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="d732d-147">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d732d-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="d732d-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d732d-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="d732d-149">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="d732d-149">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

