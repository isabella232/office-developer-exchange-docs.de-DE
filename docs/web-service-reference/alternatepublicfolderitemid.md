---
title: AlternatePublicFolderItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternatePublicFolderItemId
api_type:
- schema
ms.assetid: a67df9b9-8fdb-42de-b9c5-8377b71fa3d9
description: Das Element AlternatePublicFolderItemId beschreibt einen Bezeichner für Öffentliche Ordner in einer anderen Bezeichner Format umwandeln. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 2240f3ff80c2c5b705611c3cf9286faa62d204cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757260"
---
# <a name="alternatepublicfolderitemid"></a><span data-ttu-id="4fcf1-104">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="4fcf1-104">AlternatePublicFolderItemId</span></span>

<span data-ttu-id="4fcf1-105">Das Element **AlternatePublicFolderItemId** beschreibt einen Bezeichner für Öffentliche Ordner in einer anderen Bezeichner Format umwandeln.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-105">The **AlternatePublicFolderItemId** element describes a public folder item identifier to convert to another identifier format.</span></span> <span data-ttu-id="4fcf1-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
- [<span data-ttu-id="4fcf1-107">ConvertId</span><span class="sxs-lookup"><span data-stu-id="4fcf1-107">ConvertId</span></span>](convertid.md)
  
- [<span data-ttu-id="4fcf1-108">SourceIds</span><span class="sxs-lookup"><span data-stu-id="4fcf1-108">SourceIds</span></span>](sourceids.md)
  
- [<span data-ttu-id="4fcf1-109">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="4fcf1-109">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md)
  
```xml
<AlternatePublicFolderItemId FolderId="" Format="" ItemId=""/>
```

 <span data-ttu-id="4fcf1-110">**AlternatePublicFolderItemIdType**</span><span class="sxs-lookup"><span data-stu-id="4fcf1-110">**AlternatePublicFolderItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4fcf1-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4fcf1-111">Attributes and elements</span></span>

<span data-ttu-id="4fcf1-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4fcf1-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="4fcf1-113">Attributes</span></span>

|<span data-ttu-id="4fcf1-114">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4fcf1-114">**Attribute**</span></span>|<span data-ttu-id="4fcf1-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4fcf1-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4fcf1-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="4fcf1-116">FolderId</span></span>  <br/> |<span data-ttu-id="4fcf1-117">Identifiziert den öffentlichen Ordner, der das öffentliche Ordner-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-117">Identifies the public folder that contains the public folder item.</span></span> <span data-ttu-id="4fcf1-118">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-118">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="4fcf1-119">Format</span><span class="sxs-lookup"><span data-stu-id="4fcf1-119">Format</span></span>  <br/> |<span data-ttu-id="4fcf1-120">Gibt das Format, das der Öffentliche Ordner Elementbezeichner konvertieren beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-120">Identifies the format that describes the public folder item identifier to convert.</span></span> <span data-ttu-id="4fcf1-121">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-121">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="4fcf1-122">ItemId</span><span class="sxs-lookup"><span data-stu-id="4fcf1-122">ItemId</span></span>  <br/> |<span data-ttu-id="4fcf1-123">Bezeichner zu konvertierenden Elements für Öffentliche Ordner.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-123">Identifier the public folder item to convert.</span></span> <span data-ttu-id="4fcf1-124">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-124">This attribute is required.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="4fcf1-125">Format-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="4fcf1-125">Format attribute values</span></span>

|<span data-ttu-id="4fcf1-126">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4fcf1-126">**Value**</span></span>|<span data-ttu-id="4fcf1-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4fcf1-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4fcf1-128">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="4fcf1-128">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="4fcf1-129">Beschreibt Bezeichner, die in der ursprünglich freigegebenen Version von Exchange 2007 von Exchange-Webdienste erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-129">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="4fcf1-130">EwsId</span><span class="sxs-lookup"><span data-stu-id="4fcf1-130">EwsId</span></span>  <br/> |<span data-ttu-id="4fcf1-131">Beschreibt Bezeichner, die von der Exchange-Webdienste beginnend mit Exchange 2007 SP1 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-131">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="4fcf1-132">EntryId</span><span class="sxs-lookup"><span data-stu-id="4fcf1-132">EntryId</span></span>  <br/> |<span data-ttu-id="4fcf1-133">MAPI-IDs, wie in der PR_ENTRYID-Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-133">Describes MAPI identifiers, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="4fcf1-134">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="4fcf1-134">HexEntryId</span></span>  <br/> |<span data-ttu-id="4fcf1-135">Beschreibt eine hexadezimal-codierte Darstellung der PR_ENTRYID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-135">Describes a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span> <span data-ttu-id="4fcf1-136">Dies ist das Format der Verfügbarkeit Kalender-Ereignis-IDs.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-136">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="4fcf1-137">StoreId</span><span class="sxs-lookup"><span data-stu-id="4fcf1-137">StoreId</span></span>  <br/> |<span data-ttu-id="4fcf1-138">Beschreibt die Exchange-Speicher-IDs.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-138">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="4fcf1-139">OwaId</span><span class="sxs-lookup"><span data-stu-id="4fcf1-139">OwaId</span></span>  <br/> |<span data-ttu-id="4fcf1-140">Beschreibt einen Outlook Web Access-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-140">Describes an Outlook Web Access identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4fcf1-141">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4fcf1-141">Child elements</span></span>

<span data-ttu-id="4fcf1-142">Keine.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-142">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4fcf1-143">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4fcf1-143">Parent elements</span></span>

|<span data-ttu-id="4fcf1-144">**Element**</span><span class="sxs-lookup"><span data-stu-id="4fcf1-144">**Element**</span></span>|<span data-ttu-id="4fcf1-145">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4fcf1-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fcf1-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="4fcf1-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="4fcf1-147">Enthält die Bezeichner der Quelle zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-147">Contains the source identifiers to convert.</span></span> <span data-ttu-id="4fcf1-148">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fcf1-149">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4fcf1-149">Remarks</span></span>

<span data-ttu-id="4fcf1-150">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4fcf1-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4fcf1-151">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4fcf1-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fcf1-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="4fcf1-152">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4fcf1-153">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4fcf1-153">Schema Name</span></span>  <br/> |<span data-ttu-id="4fcf1-154">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4fcf1-154">Types schema</span></span>  <br/> |
|<span data-ttu-id="4fcf1-155">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4fcf1-155">Validation File</span></span>  <br/> |<span data-ttu-id="4fcf1-156">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4fcf1-156">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4fcf1-157">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4fcf1-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="4fcf1-158">True</span><span class="sxs-lookup"><span data-stu-id="4fcf1-158">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4fcf1-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fcf1-159">See also</span></span>

- [<span data-ttu-id="4fcf1-160">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4fcf1-160">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="4fcf1-161">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4fcf1-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="4fcf1-162">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="4fcf1-162">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

