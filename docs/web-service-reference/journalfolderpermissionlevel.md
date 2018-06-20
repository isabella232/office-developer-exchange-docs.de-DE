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
description: Das JournalFolderPermissionLevel-Element enthält die Berechtigungen für den Standardordner Journal. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 030c2682fd6eaaf46c8be04e8357c285296816cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830184"
---
# <a name="journalfolderpermissionlevel"></a><span data-ttu-id="bbc36-104">JournalFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="bbc36-104">JournalFolderPermissionLevel</span></span>

<span data-ttu-id="bbc36-105">Das **JournalFolderPermissionLevel** -Element enthält die Berechtigungen für den Standardordner Journal.</span><span class="sxs-lookup"><span data-stu-id="bbc36-105">The **JournalFolderPermissionLevel** element contains the permissions for the default Journal folder.</span></span> <span data-ttu-id="bbc36-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bbc36-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<JournalFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</JournalFolderPermissionLevel>
```

 <span data-ttu-id="bbc36-107">**DelegateFolderPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="bbc36-107">**DelegateFolderPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bbc36-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bbc36-108">Attributes and elements</span></span>

<span data-ttu-id="bbc36-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bbc36-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bbc36-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="bbc36-110">Attributes</span></span>

<span data-ttu-id="bbc36-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bbc36-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bbc36-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bbc36-112">Child elements</span></span>

<span data-ttu-id="bbc36-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="bbc36-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bbc36-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bbc36-114">Parent elements</span></span>

|<span data-ttu-id="bbc36-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="bbc36-115">**Element**</span></span>|<span data-ttu-id="bbc36-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bbc36-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bbc36-117">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="bbc36-117">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="bbc36-118">Die Stellvertretung die berechtigungseinstellungen auf Poolebene für einen Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="bbc36-118">Contains the delegate permission level settings for a user.</span></span> <span data-ttu-id="bbc36-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bbc36-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bbc36-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="bbc36-120">Text value</span></span>

<span data-ttu-id="bbc36-121">Die folgende Tabelle enthält die Textwerte, die die Berechtigungsstufen darstellen.</span><span class="sxs-lookup"><span data-stu-id="bbc36-121">The following table lists the text values that represent the permission levels.</span></span>
  
<span data-ttu-id="bbc36-122">**Ebene Text Berechtigungswerte**</span><span class="sxs-lookup"><span data-stu-id="bbc36-122">**Permission level text values**</span></span>

|<span data-ttu-id="bbc36-123">**Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="bbc36-123">**Permission level**</span></span>|<span data-ttu-id="bbc36-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bbc36-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bbc36-125">Keine</span><span class="sxs-lookup"><span data-stu-id="bbc36-125">None</span></span>  <br/> |<span data-ttu-id="bbc36-126">Stellvertretungsbenutzers verfügt über keine Access-Berechtigungen für den Ordner Journal.</span><span class="sxs-lookup"><span data-stu-id="bbc36-126">The delegate user has no access permissions to the Journal folder.</span></span>  <br/> |
|<span data-ttu-id="bbc36-127">Prüfer</span><span class="sxs-lookup"><span data-stu-id="bbc36-127">Reviewer</span></span>  <br/> |<span data-ttu-id="bbc36-128">Stellvertretungsbenutzers kann Elemente im Ordner "Journal" lesen.</span><span class="sxs-lookup"><span data-stu-id="bbc36-128">The delegate user can read items in the Journal folder.</span></span>  <br/> |
|<span data-ttu-id="bbc36-129">Autor</span><span class="sxs-lookup"><span data-stu-id="bbc36-129">Author</span></span>  <br/> |<span data-ttu-id="bbc36-130">Stellvertretungsbenutzers lesen und Erstellen von Elementen im Ordner "Journal".</span><span class="sxs-lookup"><span data-stu-id="bbc36-130">The delegate user can read and create items in the Journal folder.</span></span>  <br/> |
|<span data-ttu-id="bbc36-131">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="bbc36-131">Editor</span></span>  <br/> |<span data-ttu-id="bbc36-132">Stellvertretungsbenutzers kann lesen, erstellen und Ändern von Elementen im Ordner "Journal".</span><span class="sxs-lookup"><span data-stu-id="bbc36-132">The delegate user can read, create, and modify items in the Journal folder.</span></span>  <br/> |
|<span data-ttu-id="bbc36-133">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="bbc36-133">Custom</span></span>  <br/> |<span data-ttu-id="bbc36-134">Stellvertretungsbenutzers hat benutzerdefinierte Zugriffsberechtigungen für den Ordner Journal.</span><span class="sxs-lookup"><span data-stu-id="bbc36-134">The delegate user has custom access permissions to the Journal folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbc36-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bbc36-135">Remarks</span></span>

<span data-ttu-id="bbc36-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bbc36-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bbc36-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bbc36-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bbc36-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="bbc36-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bbc36-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bbc36-139">Schema Name</span></span>  <br/> |<span data-ttu-id="bbc36-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bbc36-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="bbc36-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bbc36-141">Validation File</span></span>  <br/> |<span data-ttu-id="bbc36-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bbc36-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bbc36-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bbc36-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="bbc36-144">False</span><span class="sxs-lookup"><span data-stu-id="bbc36-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bbc36-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbc36-145">See also</span></span>



[<span data-ttu-id="bbc36-146">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bbc36-146">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="bbc36-147">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bbc36-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="bbc36-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bbc36-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="bbc36-149">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="bbc36-149">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

