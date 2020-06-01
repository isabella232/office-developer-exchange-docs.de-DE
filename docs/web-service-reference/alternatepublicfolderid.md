---
title: AlternatePublicFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternatePublicFolderId
api_type:
- schema
ms.assetid: 0a4dc1cc-959e-4b93-aa3a-3020ca8b8a02
description: Das AlternatePublicFolderId-Element beschreibt einen Bezeichner für Öffentliche Ordner, der in ein anderes ID-Format konvertiert werden soll. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 54ad663117839222ea1174cd1c25600f31aa6b43
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464798"
---
# <a name="alternatepublicfolderid"></a><span data-ttu-id="e2389-104">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="e2389-104">AlternatePublicFolderId</span></span>

<span data-ttu-id="e2389-105">Das **AlternatePublicFolderId** -Element beschreibt einen Bezeichner für Öffentliche Ordner, der in ein anderes ID-Format konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2389-105">The **AlternatePublicFolderId** element describes a public folder identifier to convert to another identifier format.</span></span> <span data-ttu-id="e2389-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e2389-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
- [<span data-ttu-id="e2389-107">ConvertId</span><span class="sxs-lookup"><span data-stu-id="e2389-107">ConvertId</span></span>](convertid.md)
  
- [<span data-ttu-id="e2389-108">SourceIds</span><span class="sxs-lookup"><span data-stu-id="e2389-108">SourceIds</span></span>](sourceids.md)
  
- [<span data-ttu-id="e2389-109">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="e2389-109">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md)
  
```xml
<AlternatePublicFolderId FolderId="" Format="" />
```

 <span data-ttu-id="e2389-110">**AlternatePublicFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="e2389-110">**AlternatePublicFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2389-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e2389-111">Attributes and elements</span></span>

<span data-ttu-id="e2389-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e2389-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2389-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="e2389-113">Attributes</span></span>

|<span data-ttu-id="e2389-114">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e2389-114">**Attribute**</span></span>|<span data-ttu-id="e2389-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2389-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2389-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="e2389-116">FolderId</span></span>  <br/> |<span data-ttu-id="e2389-117">Enthält den Bezeichner des öffentlichen Ordners, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2389-117">Contains the public folder identifier to convert.</span></span> <span data-ttu-id="e2389-118">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e2389-118">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="e2389-119">Format</span><span class="sxs-lookup"><span data-stu-id="e2389-119">Format</span></span>  <br/> |<span data-ttu-id="e2389-120">Gibt das Format an, in dem die zu konvertierende öffentliche Ordner-ID beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e2389-120">Identifies the format that describes the public folder identifier to convert.</span></span> <span data-ttu-id="e2389-121">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e2389-121">This attribute is required.</span></span>  <br/> |
   
#### <a name="format-attribute"></a><span data-ttu-id="e2389-122">Format-Attribut</span><span class="sxs-lookup"><span data-stu-id="e2389-122">Format attribute</span></span>

|<span data-ttu-id="e2389-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e2389-123">**Value**</span></span>|<span data-ttu-id="e2389-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2389-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2389-125">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="e2389-125">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="e2389-126">Beschreibt Bezeichner, die von Exchange Webdienste in der ersten Version von Exchange 2007 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e2389-126">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="e2389-127">EwsId</span><span class="sxs-lookup"><span data-stu-id="e2389-127">EwsId</span></span>  <br/> |<span data-ttu-id="e2389-128">Beschreibt Bezeichner, die von Exchange Webdienste ab Exchange 2007 SP1 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e2389-128">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="e2389-129">EntryId</span><span class="sxs-lookup"><span data-stu-id="e2389-129">EntryId</span></span>  <br/> |<span data-ttu-id="e2389-130">Beschreibt MAPI-IDs wie in der PR_ENTRYID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e2389-130">Describes MAPI identifiers, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="e2389-131">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="e2389-131">HexEntryId</span></span>  <br/> |<span data-ttu-id="e2389-132">Beschreibt eine hexadezimal codierte Darstellung der PR_ENTRYID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e2389-132">Describes a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span> <span data-ttu-id="e2389-133">Dies ist das Format der Ereignisbezeichner für den Verfügbarkeitskalender.</span><span class="sxs-lookup"><span data-stu-id="e2389-133">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="e2389-134">StoreId</span><span class="sxs-lookup"><span data-stu-id="e2389-134">StoreId</span></span>  <br/> |<span data-ttu-id="e2389-135">Beschreibt Exchange-Informationsspeicher Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e2389-135">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="e2389-136">OwaId</span><span class="sxs-lookup"><span data-stu-id="e2389-136">OwaId</span></span>  <br/> |<span data-ttu-id="e2389-137">Beschreibt einen Outlook Web Access Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e2389-137">Describes an Outlook Web Access identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e2389-138">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2389-138">Child elements</span></span>

<span data-ttu-id="e2389-139">Keine.</span><span class="sxs-lookup"><span data-stu-id="e2389-139">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e2389-140">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2389-140">Parent elements</span></span>

|<span data-ttu-id="e2389-141">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2389-141">**Element**</span></span>|<span data-ttu-id="e2389-142">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2389-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2389-143">SourceIds</span><span class="sxs-lookup"><span data-stu-id="e2389-143">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="e2389-144">Enthält die Quellbezeichner, die konvertiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e2389-144">Contains the source identifiers to convert.</span></span> <span data-ttu-id="e2389-145">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e2389-145">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="e2389-146">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e2389-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2389-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2389-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e2389-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e2389-148">Schema Name</span></span>  <br/> |<span data-ttu-id="e2389-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e2389-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="e2389-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e2389-150">Validation File</span></span>  <br/> |<span data-ttu-id="e2389-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e2389-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e2389-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e2389-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2389-153">True</span><span class="sxs-lookup"><span data-stu-id="e2389-153">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2389-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2389-154">See also</span></span>

- [<span data-ttu-id="e2389-155">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e2389-155">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="e2389-156">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e2389-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="e2389-157">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="e2389-157">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

