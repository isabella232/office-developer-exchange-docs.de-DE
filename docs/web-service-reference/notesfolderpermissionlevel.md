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
description: Das NotesFolderPermissionLevel-Element enthält die Berechtigungen für den Standardordner Notizen. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: dd8644210692e0c342079d055ddf00b8d9283d7d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830552"
---
# <a name="notesfolderpermissionlevel"></a><span data-ttu-id="acbeb-104">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="acbeb-104">NotesFolderPermissionLevel</span></span>

<span data-ttu-id="acbeb-105">Das **NotesFolderPermissionLevel** -Element enthält die Berechtigungen für den Standardordner Notizen.</span><span class="sxs-lookup"><span data-stu-id="acbeb-105">The **NotesFolderPermissionLevel** element contains the permissions for the default Notes folder.</span></span> <span data-ttu-id="acbeb-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="acbeb-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<NotesFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</NotesFolderPermissionLevel>
```

 <span data-ttu-id="acbeb-107">**DelegateFolderPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="acbeb-107">**DelegateFolderPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="acbeb-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="acbeb-108">Attributes and elements</span></span>

<span data-ttu-id="acbeb-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="acbeb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="acbeb-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="acbeb-110">Attributes</span></span>

<span data-ttu-id="acbeb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="acbeb-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="acbeb-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="acbeb-112">Child elements</span></span>

<span data-ttu-id="acbeb-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="acbeb-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="acbeb-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="acbeb-114">Parent elements</span></span>

|<span data-ttu-id="acbeb-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="acbeb-115">**Element**</span></span>|<span data-ttu-id="acbeb-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="acbeb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acbeb-117">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="acbeb-117">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="acbeb-118">Die Stellvertretung die berechtigungseinstellungen auf Poolebene für einen Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="acbeb-118">Contains the delegate permission level settings for a user.</span></span> <span data-ttu-id="acbeb-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="acbeb-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="acbeb-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="acbeb-120">Text value</span></span>

<span data-ttu-id="acbeb-121">Die folgende Tabelle enthält die Textwerte, die die Berechtigungsstufen darstellen.</span><span class="sxs-lookup"><span data-stu-id="acbeb-121">The following table lists the text values that represent the permission levels.</span></span>
  
<span data-ttu-id="acbeb-122">**Ebene Text Berechtigungswerte**</span><span class="sxs-lookup"><span data-stu-id="acbeb-122">**Permission level text values**</span></span>

|<span data-ttu-id="acbeb-123">**Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="acbeb-123">**Permission level**</span></span>|<span data-ttu-id="acbeb-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="acbeb-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="acbeb-125">Keine</span><span class="sxs-lookup"><span data-stu-id="acbeb-125">None</span></span>  <br/> |<span data-ttu-id="acbeb-126">Stellvertretungsbenutzers verfügt über keine Access-Berechtigungen auf den Ordner "Notizen".</span><span class="sxs-lookup"><span data-stu-id="acbeb-126">The delegate user has no access permissions to the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="acbeb-127">Prüfer</span><span class="sxs-lookup"><span data-stu-id="acbeb-127">Reviewer</span></span>  <br/> |<span data-ttu-id="acbeb-128">Stellvertretungsbenutzers kann Elemente im Ordner "Notizen" lesen.</span><span class="sxs-lookup"><span data-stu-id="acbeb-128">The delegate user can read items in the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="acbeb-129">Autor</span><span class="sxs-lookup"><span data-stu-id="acbeb-129">Author</span></span>  <br/> |<span data-ttu-id="acbeb-130">Stellvertretungsbenutzers lesen und Erstellen von Elementen im Ordner "Notizen".</span><span class="sxs-lookup"><span data-stu-id="acbeb-130">The delegate user can read and create items in the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="acbeb-131">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="acbeb-131">Editor</span></span>  <br/> |<span data-ttu-id="acbeb-132">Stellvertretungsbenutzers kann lesen, erstellen und Ändern von Elementen im Ordner "Notizen".</span><span class="sxs-lookup"><span data-stu-id="acbeb-132">The delegate user can read, create, and modify items in the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="acbeb-133">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="acbeb-133">Custom</span></span>  <br/> |<span data-ttu-id="acbeb-134">Stellvertretungsbenutzers verfügt über benutzerdefinierten Zugriff für den Ordner "Notizen".</span><span class="sxs-lookup"><span data-stu-id="acbeb-134">The delegate user has custom access permissions to the Notes folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acbeb-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="acbeb-135">Remarks</span></span>

<span data-ttu-id="acbeb-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="acbeb-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acbeb-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="acbeb-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acbeb-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="acbeb-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="acbeb-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="acbeb-139">Schema Name</span></span>  <br/> |<span data-ttu-id="acbeb-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="acbeb-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="acbeb-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="acbeb-141">Validation File</span></span>  <br/> |<span data-ttu-id="acbeb-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="acbeb-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="acbeb-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="acbeb-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="acbeb-144">False</span><span class="sxs-lookup"><span data-stu-id="acbeb-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="acbeb-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acbeb-145">See also</span></span>



[<span data-ttu-id="acbeb-146">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="acbeb-146">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="acbeb-147">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="acbeb-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="acbeb-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="acbeb-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="acbeb-149">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="acbeb-149">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

