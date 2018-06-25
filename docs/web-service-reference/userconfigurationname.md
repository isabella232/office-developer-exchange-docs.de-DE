---
title: UserConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationName
api_type:
- schema
ms.assetid: 6947dd03-9727-4379-9b9d-42373fa120c7
description: Das Element UserConfigurationName stellt den Namen eines Benutzers Configuration-Objekts. Der Benutzername des Configuration-Objekt ist der Bezeichner für eine Benutzer-Konfigurationsobjekt.
ms.openlocfilehash: 40580343e92493c3d39b090371708269ec3274b9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839436"
---
# <a name="userconfigurationname"></a><span data-ttu-id="ddb42-104">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ddb42-104">UserConfigurationName</span></span>

<span data-ttu-id="ddb42-105">Das Element **UserConfigurationName** stellt den Namen eines Benutzers Configuration-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ddb42-105">The **UserConfigurationName** element represents the name of a user configuration object.</span></span> <span data-ttu-id="ddb42-106">Der Benutzername des Configuration-Objekt ist der Bezeichner für eine Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ddb42-106">The user configuration object name is the identifier for a user configuration object.</span></span> 
  
```XML
<UserConfigurationName Name="">
   <FolderId/>
</UserConfigurationName>
```

 <span data-ttu-id="ddb42-107">**UserConfigurationNameType**</span><span class="sxs-lookup"><span data-stu-id="ddb42-107">**UserConfigurationNameType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ddb42-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ddb42-108">Attributes and elements</span></span>

<span data-ttu-id="ddb42-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ddb42-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ddb42-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ddb42-110">Attributes</span></span>

|<span data-ttu-id="ddb42-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ddb42-111">**Attribute**</span></span>|<span data-ttu-id="ddb42-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddb42-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ddb42-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="ddb42-113">**Name**</span></span> <br/> |<span data-ttu-id="ddb42-114">Enthält einen String-Wert, der den Namen eines Benutzers Configuration-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="ddb42-114">Contains a string value that represents the name of a user configuration object.</span></span> <span data-ttu-id="ddb42-115">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ddb42-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ddb42-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ddb42-116">Child elements</span></span>

|<span data-ttu-id="ddb42-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ddb42-117">**Element**</span></span>|<span data-ttu-id="ddb42-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddb42-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ddb42-119">FolderId</span><span class="sxs-lookup"><span data-stu-id="ddb42-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="ddb42-120">Stellt den Ordner Bezeichner des Ordners, der das Benutzerobjekt Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="ddb42-120">Represents the folder identifier of the folder that contains the user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ddb42-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="ddb42-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="ddb42-122">Stellt einen definierten Ordnernamen des Ordners, der das Benutzerobjekt Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="ddb42-122">Represents a distinguished folder name of the folder that contains the user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ddb42-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ddb42-123">Parent elements</span></span>

|<span data-ttu-id="ddb42-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ddb42-124">**Element**</span></span>|<span data-ttu-id="ddb42-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddb42-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ddb42-126">DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddb42-126">DeleteUserConfiguration</span></span>](deleteuserconfiguration.md) <br/> |<span data-ttu-id="ddb42-127">Stellt eine Anforderung zum Löschen einer Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ddb42-127">Represents a request to delete a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ddb42-128">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddb42-128">GetUserConfiguration</span></span>](getuserconfiguration.md) <br/> |<span data-ttu-id="ddb42-129">Eine Anforderung zum Abrufen eines Benutzers Konfiguration-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="ddb42-129">Represents a request to get a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ddb42-130">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddb42-130">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="ddb42-131">Definiert einen einzelnen Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ddb42-131">Defines a single user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ddb42-132">Textwert</span><span class="sxs-lookup"><span data-stu-id="ddb42-132">Text value</span></span>

<span data-ttu-id="ddb42-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="ddb42-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ddb42-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ddb42-134">Remarks</span></span>

<span data-ttu-id="ddb42-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ddb42-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ddb42-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ddb42-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddb42-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ddb42-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ddb42-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ddb42-138">Schema Name</span></span>  <br/> |<span data-ttu-id="ddb42-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ddb42-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="ddb42-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ddb42-140">Validation File</span></span>  <br/> |<span data-ttu-id="ddb42-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ddb42-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ddb42-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ddb42-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="ddb42-143">False</span><span class="sxs-lookup"><span data-stu-id="ddb42-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ddb42-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddb42-144">See also</span></span>



- [<span data-ttu-id="ddb42-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ddb42-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

