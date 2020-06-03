---
title: ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 9684c22c-29d4-4f7f-befc-8cd41da56d38
description: Das Convert-ID-Element definiert eine Anforderung zum Konvertieren von Element-und Ordner Bezeichnern zwischen unterstützten Exchange-Formaten. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: d421baf1f29fb59a8c6eb2b09e1fa0e8a38ffaa4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452538"
---
# <a name="convertid"></a><span data-ttu-id="52e84-104">ConvertId</span><span class="sxs-lookup"><span data-stu-id="52e84-104">ConvertId</span></span>

<span data-ttu-id="52e84-105">Das **Convert** -ID-Element definiert eine Anforderung zum Konvertieren von Element-und Ordner Bezeichnern zwischen unterstützten Exchange-Formaten.</span><span class="sxs-lookup"><span data-stu-id="52e84-105">The **ConvertId** element defines a request to convert item and folder identifiers between supported Exchange formats.</span></span> <span data-ttu-id="52e84-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="52e84-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ConvertId DestinationFormat="">
   <SourceIds/>
</ConvertId>
```

 <span data-ttu-id="52e84-107">**ConvertIdType**</span><span class="sxs-lookup"><span data-stu-id="52e84-107">**ConvertIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52e84-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="52e84-108">Attributes and elements</span></span>

<span data-ttu-id="52e84-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="52e84-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52e84-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="52e84-110">Attributes</span></span>

|<span data-ttu-id="52e84-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="52e84-111">**Attribute**</span></span>|<span data-ttu-id="52e84-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52e84-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52e84-113">**DestinationFormat**</span><span class="sxs-lookup"><span data-stu-id="52e84-113">**DestinationFormat**</span></span> <br/> |<span data-ttu-id="52e84-114">Beschreibt das ID-Format, das für alle konvertierten Bezeichner zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="52e84-114">Describes the identifier format that will be returned for all the converted identifiers.</span></span> <span data-ttu-id="52e84-115">Das DestinationFormat wird von der IdFormatType beschrieben.</span><span class="sxs-lookup"><span data-stu-id="52e84-115">The DestinationFormat is described by the IdFormatType.</span></span>  <br/> |
   
#### <a name="destinationformat-attribute"></a><span data-ttu-id="52e84-116">DestinationFormat-Attribut</span><span class="sxs-lookup"><span data-stu-id="52e84-116">DestinationFormat Attribute</span></span>

|<span data-ttu-id="52e84-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="52e84-117">**Value**</span></span>|<span data-ttu-id="52e84-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52e84-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52e84-119">**EwsLegacyId**</span><span class="sxs-lookup"><span data-stu-id="52e84-119">**EwsLegacyId**</span></span> <br/> |<span data-ttu-id="52e84-120">Stellt das ID-Format dar, das für Exchange Webdienste-Bezeichner verwendet wird, die in der ersten Version von Exchange 2007 bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="52e84-120">Represents the identifier format that is used for Exchange Web Services identifiers that are provided in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="52e84-121">**EwsId**</span><span class="sxs-lookup"><span data-stu-id="52e84-121">**EwsId**</span></span> <br/> |<span data-ttu-id="52e84-122">Stellt das ID-Format dar, das für Exchange Webdienste-IDs verwendet wird, die mit Exchange Server 2007 SP1 beginnen.</span><span class="sxs-lookup"><span data-stu-id="52e84-122">Represents the identifier format that is used for Exchange Web Services identifiers starting with Exchange Server 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="52e84-123">**EntryID**</span><span class="sxs-lookup"><span data-stu-id="52e84-123">**EntryId**</span></span> <br/> |<span data-ttu-id="52e84-124">Stellt den MAPI-Bezeichner dar, wie in der PR_ENTRYID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="52e84-124">Represents the MAPI identifier, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="52e84-125">**HexEntryId**</span><span class="sxs-lookup"><span data-stu-id="52e84-125">**HexEntryId**</span></span> <br/> |<span data-ttu-id="52e84-126">Stellt die Ereignis-ID für den Verfügbarkeitskalender dar.</span><span class="sxs-lookup"><span data-stu-id="52e84-126">Represents the availability calendar event identifier.</span></span> <span data-ttu-id="52e84-127">Dies ist eine hexadezimal codierte Darstellung der PR_ENTRYID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="52e84-127">This is a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="52e84-128">**StoreId**</span><span class="sxs-lookup"><span data-stu-id="52e84-128">**StoreId**</span></span> <br/> |<span data-ttu-id="52e84-129">Stellt den Exchange-Informationsspeicher Bezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="52e84-129">Represents the Exchange store identifier.</span></span>  <br/> |
|<span data-ttu-id="52e84-130">**OwaId**</span><span class="sxs-lookup"><span data-stu-id="52e84-130">**OwaId**</span></span> <br/> |<span data-ttu-id="52e84-131">Stellt das Outlook Web Access-ID-Format dar.</span><span class="sxs-lookup"><span data-stu-id="52e84-131">Represents the Outlook Web Access identifier format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="52e84-132">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52e84-132">Child elements</span></span>

|<span data-ttu-id="52e84-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="52e84-133">**Element**</span></span>|<span data-ttu-id="52e84-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52e84-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52e84-135">SourceIds</span><span class="sxs-lookup"><span data-stu-id="52e84-135">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="52e84-136">Enthält die Quellbezeichner, die konvertiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="52e84-136">Contains the source identifiers to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52e84-137">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52e84-137">Parent elements</span></span>

<span data-ttu-id="52e84-138">Keine.</span><span class="sxs-lookup"><span data-stu-id="52e84-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52e84-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52e84-139">Remarks</span></span>

<span data-ttu-id="52e84-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="52e84-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52e84-141">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="52e84-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52e84-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="52e84-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="52e84-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="52e84-143">Schema Name</span></span>  <br/> |<span data-ttu-id="52e84-144">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="52e84-144">messages schema</span></span>  <br/> |
|<span data-ttu-id="52e84-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="52e84-145">Validation File</span></span>  <br/> |<span data-ttu-id="52e84-146">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="52e84-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52e84-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="52e84-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="52e84-148">False</span><span class="sxs-lookup"><span data-stu-id="52e84-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52e84-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52e84-149">See also</span></span>



[<span data-ttu-id="52e84-150">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="52e84-150">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="52e84-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="52e84-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="52e84-152">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="52e84-152">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

