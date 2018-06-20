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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839436"
---
# <a name="userconfigurationname"></a><span data-ttu-id="0d9e7-104">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0d9e7-104">UserConfigurationName</span></span>

<span data-ttu-id="0d9e7-105">Das Element **UserConfigurationName** stellt den Namen eines Benutzers Configuration-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-105">The **UserConfigurationName** element represents the name of a user configuration object.</span></span> <span data-ttu-id="0d9e7-106">Der Benutzername des Configuration-Objekt ist der Bezeichner für eine Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-106">The user configuration object name is the identifier for a user configuration object.</span></span> 
  
```XML
<UserConfigurationName Name="">
   <FolderId/>
</UserConfigurationName>
```

 <span data-ttu-id="0d9e7-107">**UserConfigurationNameType**</span><span class="sxs-lookup"><span data-stu-id="0d9e7-107">**UserConfigurationNameType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d9e7-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0d9e7-108">Attributes and elements</span></span>

<span data-ttu-id="0d9e7-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d9e7-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d9e7-110">Attributes</span></span>

|<span data-ttu-id="0d9e7-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0d9e7-111">**Attribute**</span></span>|<span data-ttu-id="0d9e7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d9e7-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0d9e7-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="0d9e7-113">**Name**</span></span> <br/> |<span data-ttu-id="0d9e7-114">Enthält einen String-Wert, der den Namen eines Benutzers Configuration-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-114">Contains a string value that represents the name of a user configuration object.</span></span> <span data-ttu-id="0d9e7-115">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0d9e7-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d9e7-116">Child elements</span></span>

|<span data-ttu-id="0d9e7-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d9e7-117">**Element**</span></span>|<span data-ttu-id="0d9e7-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d9e7-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d9e7-119">FolderId</span><span class="sxs-lookup"><span data-stu-id="0d9e7-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="0d9e7-120">Stellt den Ordner Bezeichner des Ordners, der das Benutzerobjekt Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-120">Represents the folder identifier of the folder that contains the user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="0d9e7-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="0d9e7-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="0d9e7-122">Stellt einen definierten Ordnernamen des Ordners, der das Benutzerobjekt Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-122">Represents a distinguished folder name of the folder that contains the user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d9e7-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d9e7-123">Parent elements</span></span>

|<span data-ttu-id="0d9e7-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d9e7-124">**Element**</span></span>|<span data-ttu-id="0d9e7-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d9e7-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d9e7-126">DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d9e7-126">DeleteUserConfiguration</span></span>](deleteuserconfiguration.md) <br/> |<span data-ttu-id="0d9e7-127">Stellt eine Anforderung zum Löschen einer Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-127">Represents a request to delete a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="0d9e7-128">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d9e7-128">GetUserConfiguration</span></span>](getuserconfiguration.md) <br/> |<span data-ttu-id="0d9e7-129">Eine Anforderung zum Abrufen eines Benutzers Konfiguration-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-129">Represents a request to get a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="0d9e7-130">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d9e7-130">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="0d9e7-131">Definiert einen einzelnen Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-131">Defines a single user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0d9e7-132">Textwert</span><span class="sxs-lookup"><span data-stu-id="0d9e7-132">Text value</span></span>

<span data-ttu-id="0d9e7-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d9e7-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d9e7-134">Remarks</span></span>

<span data-ttu-id="0d9e7-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d9e7-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0d9e7-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d9e7-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d9e7-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0d9e7-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0d9e7-138">Schema Name</span></span>  <br/> |<span data-ttu-id="0d9e7-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0d9e7-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="0d9e7-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0d9e7-140">Validation File</span></span>  <br/> |<span data-ttu-id="0d9e7-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0d9e7-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0d9e7-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0d9e7-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d9e7-143">False</span><span class="sxs-lookup"><span data-stu-id="0d9e7-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d9e7-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d9e7-144">See also</span></span>



- [<span data-ttu-id="0d9e7-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0d9e7-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

