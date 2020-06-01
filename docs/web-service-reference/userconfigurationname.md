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
description: Das UserConfigurationName-Element stellt den Namen eines Benutzer Konfigurationsobjekts dar. Der Benutzer Konfigurationsobjekt Name ist der Bezeichner für ein Benutzer Konfigurationsobjekt.
ms.openlocfilehash: 020b55919f7f81602a5eb072652d82168607d306
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466031"
---
# <a name="userconfigurationname"></a><span data-ttu-id="30e19-104">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="30e19-104">UserConfigurationName</span></span>

<span data-ttu-id="30e19-105">Das **UserConfigurationName** -Element stellt den Namen eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="30e19-105">The **UserConfigurationName** element represents the name of a user configuration object.</span></span> <span data-ttu-id="30e19-106">Der Benutzer Konfigurationsobjekt Name ist der Bezeichner für ein Benutzer Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="30e19-106">The user configuration object name is the identifier for a user configuration object.</span></span> 
  
```XML
<UserConfigurationName Name="">
   <FolderId/>
</UserConfigurationName>
```

```XML
<UserConfigurationName Name="">
   <DistinguishedFolderId/> 
</UserConfigurationName>
```

<span data-ttu-id="30e19-107">**UserConfigurationNameType**</span><span class="sxs-lookup"><span data-stu-id="30e19-107">**UserConfigurationNameType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="30e19-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="30e19-108">Attributes and elements</span></span>

<span data-ttu-id="30e19-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="30e19-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30e19-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="30e19-110">Attributes</span></span>

|<span data-ttu-id="30e19-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="30e19-111">**Attribute**</span></span>|<span data-ttu-id="30e19-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30e19-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30e19-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="30e19-113">**Name**</span></span> <br/> |<span data-ttu-id="30e19-114">Enthält einen String-Wert, der den Namen eines Benutzer Konfigurationsobjekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="30e19-114">Contains a string value that represents the name of a user configuration object.</span></span> <span data-ttu-id="30e19-115">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="30e19-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="30e19-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30e19-116">Child elements</span></span>

|<span data-ttu-id="30e19-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="30e19-117">**Element**</span></span>|<span data-ttu-id="30e19-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30e19-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30e19-119">FolderId</span><span class="sxs-lookup"><span data-stu-id="30e19-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="30e19-120">Stellt den Ordner Bezeichner des Ordners dar, der das Benutzer Konfigurationsobjekt enthält.</span><span class="sxs-lookup"><span data-stu-id="30e19-120">Represents the folder identifier of the folder that contains the user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="30e19-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="30e19-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="30e19-122">Stellt einen Distinguished Folder-Namen des Ordners dar, der das Benutzer Konfigurationsobjekt enthält.</span><span class="sxs-lookup"><span data-stu-id="30e19-122">Represents a distinguished folder name of the folder that contains the user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="30e19-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30e19-123">Parent elements</span></span>

|<span data-ttu-id="30e19-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="30e19-124">**Element**</span></span>|<span data-ttu-id="30e19-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30e19-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30e19-126">DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="30e19-126">DeleteUserConfiguration</span></span>](deleteuserconfiguration.md) <br/> |<span data-ttu-id="30e19-127">Stellt eine Anforderung zum Löschen eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="30e19-127">Represents a request to delete a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="30e19-128">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="30e19-128">GetUserConfiguration</span></span>](getuserconfiguration.md) <br/> |<span data-ttu-id="30e19-129">Stellt eine Anforderung zum Abrufen eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="30e19-129">Represents a request to get a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="30e19-130">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="30e19-130">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="30e19-131">Definiert ein einzelnes Benutzer Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="30e19-131">Defines a single user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="30e19-132">Textwert</span><span class="sxs-lookup"><span data-stu-id="30e19-132">Text value</span></span>

<span data-ttu-id="30e19-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="30e19-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30e19-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30e19-134">Remarks</span></span>

<span data-ttu-id="30e19-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="30e19-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30e19-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="30e19-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30e19-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="30e19-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="30e19-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="30e19-138">Schema Name</span></span>  <br/> |<span data-ttu-id="30e19-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="30e19-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="30e19-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="30e19-140">Validation File</span></span>  <br/> |<span data-ttu-id="30e19-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="30e19-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="30e19-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="30e19-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="30e19-143">False</span><span class="sxs-lookup"><span data-stu-id="30e19-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30e19-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30e19-144">See also</span></span>

- [<span data-ttu-id="30e19-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="30e19-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

