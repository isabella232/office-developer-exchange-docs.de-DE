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
description: Das ConvertId-Element definiert eine Anforderung zum Element und Ordner Bezeichner zwischen Exchange-Formate konvertieren. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 956f6464fd9013f9e72d2915f21c3b011d0add5b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757709"
---
# <a name="convertid"></a><span data-ttu-id="0705c-104">ConvertId</span><span class="sxs-lookup"><span data-stu-id="0705c-104">ConvertId</span></span>

<span data-ttu-id="0705c-105">Das **ConvertId** -Element definiert eine Anforderung zum Element und Ordner Bezeichner zwischen Exchange-Formate konvertieren.</span><span class="sxs-lookup"><span data-stu-id="0705c-105">The **ConvertId** element defines a request to convert item and folder identifiers between supported Exchange formats.</span></span> <span data-ttu-id="0705c-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0705c-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ConvertId DestinationFormat="">
   <SourceIds/>
</ConvertId>
```

 <span data-ttu-id="0705c-107">**ConvertIdType**</span><span class="sxs-lookup"><span data-stu-id="0705c-107">**ConvertIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0705c-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0705c-108">Attributes and elements</span></span>

<span data-ttu-id="0705c-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0705c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0705c-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0705c-110">Attributes</span></span>

|<span data-ttu-id="0705c-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0705c-111">**Attribute**</span></span>|<span data-ttu-id="0705c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0705c-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0705c-113">**DestinationFormat**</span><span class="sxs-lookup"><span data-stu-id="0705c-113">**DestinationFormat**</span></span> <br/> |<span data-ttu-id="0705c-114">Beschreibt das ID-Format, das für alle konvertierten Bezeichner zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0705c-114">Describes the identifier format that will be returned for all the converted identifiers.</span></span> <span data-ttu-id="0705c-115">Die DestinationFormat wird durch die IdFormatType beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0705c-115">The DestinationFormat is described by the IdFormatType.</span></span>  <br/> |
   
#### <a name="destinationformat-attribute"></a><span data-ttu-id="0705c-116">DestinationFormat-Attribut</span><span class="sxs-lookup"><span data-stu-id="0705c-116">DestinationFormat Attribute</span></span>

|<span data-ttu-id="0705c-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0705c-117">**Value**</span></span>|<span data-ttu-id="0705c-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0705c-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0705c-119">**EwsLegacyId**</span><span class="sxs-lookup"><span data-stu-id="0705c-119">**EwsLegacyId**</span></span> <br/> |<span data-ttu-id="0705c-120">Stellt das ID-Format, das für Exchange-Webdienste-Bezeichner verwendet wird, die in der ursprünglich freigegebenen Version von Exchange 2007 bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0705c-120">Represents the identifier format that is used for Exchange Web Services identifiers that are provided in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="0705c-121">**EwsId**</span><span class="sxs-lookup"><span data-stu-id="0705c-121">**EwsId**</span></span> <br/> |<span data-ttu-id="0705c-122">Stellt das ID-Format, das für Exchange-Webdienste-Bezeichner beginnend mit Exchange Server 2007 SP1 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0705c-122">Represents the identifier format that is used for Exchange Web Services identifiers starting with Exchange Server 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="0705c-123">**EntryId**</span><span class="sxs-lookup"><span data-stu-id="0705c-123">**EntryId**</span></span> <br/> |<span data-ttu-id="0705c-124">Stellt die MAPI-ID wie die PR_ENTRYID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0705c-124">Represents the MAPI identifier, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="0705c-125">**HexEntryId**</span><span class="sxs-lookup"><span data-stu-id="0705c-125">**HexEntryId**</span></span> <br/> |<span data-ttu-id="0705c-126">Stellt die Verfügbarkeit Kalender-Ereignis-ID an.</span><span class="sxs-lookup"><span data-stu-id="0705c-126">Represents the availability calendar event identifier.</span></span> <span data-ttu-id="0705c-127">Dies ist eine Hexadezimalzahl-codierte Darstellung der PR_ENTRYID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0705c-127">This is a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="0705c-128">**StoreId**</span><span class="sxs-lookup"><span data-stu-id="0705c-128">**StoreId**</span></span> <br/> |<span data-ttu-id="0705c-129">Stellt den Exchange-Speicher-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="0705c-129">Represents the Exchange store identifier.</span></span>  <br/> |
|<span data-ttu-id="0705c-130">**OwaId**</span><span class="sxs-lookup"><span data-stu-id="0705c-130">**OwaId**</span></span> <br/> |<span data-ttu-id="0705c-131">Stellt das Format von Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="0705c-131">Represents the Outlook Web Access identifier format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0705c-132">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0705c-132">Child elements</span></span>

|<span data-ttu-id="0705c-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="0705c-133">**Element**</span></span>|<span data-ttu-id="0705c-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0705c-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0705c-135">SourceIds</span><span class="sxs-lookup"><span data-stu-id="0705c-135">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="0705c-136">Enthält die Bezeichner der Quelle zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="0705c-136">Contains the source identifiers to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0705c-137">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0705c-137">Parent elements</span></span>

<span data-ttu-id="0705c-138">Keine.</span><span class="sxs-lookup"><span data-stu-id="0705c-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0705c-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0705c-139">Remarks</span></span>

<span data-ttu-id="0705c-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0705c-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0705c-141">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0705c-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0705c-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="0705c-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0705c-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0705c-143">Schema Name</span></span>  <br/> |<span data-ttu-id="0705c-144">Nachrichten-schema</span><span class="sxs-lookup"><span data-stu-id="0705c-144">messages schema</span></span>  <br/> |
|<span data-ttu-id="0705c-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0705c-145">Validation File</span></span>  <br/> |<span data-ttu-id="0705c-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0705c-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0705c-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0705c-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="0705c-148">False</span><span class="sxs-lookup"><span data-stu-id="0705c-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0705c-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0705c-149">See also</span></span>



[<span data-ttu-id="0705c-150">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0705c-150">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="0705c-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0705c-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="0705c-152">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="0705c-152">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

