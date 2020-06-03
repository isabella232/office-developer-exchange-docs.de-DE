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
description: Das AlternatePublicFolderItemId-Element beschreibt einen Elementbezeichner für Öffentliche Ordner, der in ein anderes ID-Format konvertiert werden soll. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 11a9fafec78a9bd14e4d98982fd38954d45e4d1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464770"
---
# <a name="alternatepublicfolderitemid"></a><span data-ttu-id="60abf-104">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="60abf-104">AlternatePublicFolderItemId</span></span>

<span data-ttu-id="60abf-105">Das **AlternatePublicFolderItemId** -Element beschreibt einen Elementbezeichner für Öffentliche Ordner, der in ein anderes ID-Format konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="60abf-105">The **AlternatePublicFolderItemId** element describes a public folder item identifier to convert to another identifier format.</span></span> <span data-ttu-id="60abf-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="60abf-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
- [<span data-ttu-id="60abf-107">ConvertId</span><span class="sxs-lookup"><span data-stu-id="60abf-107">ConvertId</span></span>](convertid.md)
  
- [<span data-ttu-id="60abf-108">SourceIds</span><span class="sxs-lookup"><span data-stu-id="60abf-108">SourceIds</span></span>](sourceids.md)
  
- [<span data-ttu-id="60abf-109">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="60abf-109">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md)
  
```xml
<AlternatePublicFolderItemId FolderId="" Format="" ItemId=""/>
```

 <span data-ttu-id="60abf-110">**AlternatePublicFolderItemIdType**</span><span class="sxs-lookup"><span data-stu-id="60abf-110">**AlternatePublicFolderItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60abf-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="60abf-111">Attributes and elements</span></span>

<span data-ttu-id="60abf-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="60abf-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60abf-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="60abf-113">Attributes</span></span>

|<span data-ttu-id="60abf-114">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="60abf-114">**Attribute**</span></span>|<span data-ttu-id="60abf-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60abf-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60abf-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="60abf-116">FolderId</span></span>  <br/> |<span data-ttu-id="60abf-117">Gibt den öffentlichen Ordner an, der das Element für Öffentliche Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="60abf-117">Identifies the public folder that contains the public folder item.</span></span> <span data-ttu-id="60abf-118">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="60abf-118">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="60abf-119">Format</span><span class="sxs-lookup"><span data-stu-id="60abf-119">Format</span></span>  <br/> |<span data-ttu-id="60abf-120">Gibt das Format an, das den zu konvertierenden Elementbezeichner für Öffentliche Ordner beschreibt.</span><span class="sxs-lookup"><span data-stu-id="60abf-120">Identifies the format that describes the public folder item identifier to convert.</span></span> <span data-ttu-id="60abf-121">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="60abf-121">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="60abf-122">ItemId</span><span class="sxs-lookup"><span data-stu-id="60abf-122">ItemId</span></span>  <br/> |<span data-ttu-id="60abf-123">Bezeichner das Element des öffentlichen Ordners, das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="60abf-123">Identifier the public folder item to convert.</span></span> <span data-ttu-id="60abf-124">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="60abf-124">This attribute is required.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="60abf-125">Formatieren von Attributwerten</span><span class="sxs-lookup"><span data-stu-id="60abf-125">Format attribute values</span></span>

|<span data-ttu-id="60abf-126">**Wert**</span><span class="sxs-lookup"><span data-stu-id="60abf-126">**Value**</span></span>|<span data-ttu-id="60abf-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60abf-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60abf-128">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="60abf-128">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="60abf-129">Beschreibt Bezeichner, die von Exchange Webdienste in der ersten Version von Exchange 2007 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="60abf-129">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="60abf-130">EwsId</span><span class="sxs-lookup"><span data-stu-id="60abf-130">EwsId</span></span>  <br/> |<span data-ttu-id="60abf-131">Beschreibt Bezeichner, die von Exchange Webdienste ab Exchange 2007 SP1 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="60abf-131">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="60abf-132">EntryId</span><span class="sxs-lookup"><span data-stu-id="60abf-132">EntryId</span></span>  <br/> |<span data-ttu-id="60abf-133">Beschreibt MAPI-IDs wie in der PR_ENTRYID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="60abf-133">Describes MAPI identifiers, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="60abf-134">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="60abf-134">HexEntryId</span></span>  <br/> |<span data-ttu-id="60abf-135">Beschreibt eine hexadezimal codierte Darstellung der PR_ENTRYID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="60abf-135">Describes a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span> <span data-ttu-id="60abf-136">Dies ist das Format der Ereignisbezeichner für den Verfügbarkeitskalender.</span><span class="sxs-lookup"><span data-stu-id="60abf-136">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="60abf-137">StoreId</span><span class="sxs-lookup"><span data-stu-id="60abf-137">StoreId</span></span>  <br/> |<span data-ttu-id="60abf-138">Beschreibt Exchange-Informationsspeicher Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="60abf-138">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="60abf-139">OwaId</span><span class="sxs-lookup"><span data-stu-id="60abf-139">OwaId</span></span>  <br/> |<span data-ttu-id="60abf-140">Beschreibt einen Outlook Web Access Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="60abf-140">Describes an Outlook Web Access identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="60abf-141">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60abf-141">Child elements</span></span>

<span data-ttu-id="60abf-142">Keine.</span><span class="sxs-lookup"><span data-stu-id="60abf-142">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="60abf-143">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60abf-143">Parent elements</span></span>

|<span data-ttu-id="60abf-144">**Element**</span><span class="sxs-lookup"><span data-stu-id="60abf-144">**Element**</span></span>|<span data-ttu-id="60abf-145">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60abf-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60abf-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="60abf-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="60abf-147">Enthält die Quellbezeichner, die konvertiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="60abf-147">Contains the source identifiers to convert.</span></span> <span data-ttu-id="60abf-148">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="60abf-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60abf-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60abf-149">Remarks</span></span>

<span data-ttu-id="60abf-150">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="60abf-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60abf-151">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="60abf-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60abf-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="60abf-152">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60abf-153">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="60abf-153">Schema Name</span></span>  <br/> |<span data-ttu-id="60abf-154">Schematypen</span><span class="sxs-lookup"><span data-stu-id="60abf-154">Types schema</span></span>  <br/> |
|<span data-ttu-id="60abf-155">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="60abf-155">Validation File</span></span>  <br/> |<span data-ttu-id="60abf-156">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="60abf-156">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60abf-157">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="60abf-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="60abf-158">True</span><span class="sxs-lookup"><span data-stu-id="60abf-158">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60abf-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60abf-159">See also</span></span>

- [<span data-ttu-id="60abf-160">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="60abf-160">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="60abf-161">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="60abf-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="60abf-162">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="60abf-162">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

