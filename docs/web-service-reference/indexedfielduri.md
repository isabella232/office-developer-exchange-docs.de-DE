---
title: IndexedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedFieldURI
api_type:
- schema
ms.assetid: 5c9cd0b5-7eca-480a-8730-fe98b1779afa
description: Das IndexedFieldURI -Element identifiziert einzelne Elemente eines Wörterbuchs.
ms.openlocfilehash: f794d9970590417d916925f7258b28d4f0920d0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467018"
---
# <a name="indexedfielduri"></a><span data-ttu-id="e8499-103">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e8499-103">IndexedFieldURI</span></span>

<span data-ttu-id="e8499-104">Das **IndexedFieldURI** -Element identifiziert einzelne Elemente eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="e8499-104">The **IndexedFieldURI** element identifies individual members of a dictionary.</span></span> 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 <span data-ttu-id="e8499-105">**PathToIndexedFieldType**</span><span class="sxs-lookup"><span data-stu-id="e8499-105">**PathToIndexedFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8499-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e8499-106">Attributes and elements</span></span>

<span data-ttu-id="e8499-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e8499-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8499-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e8499-108">Attributes</span></span>

|<span data-ttu-id="e8499-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e8499-109">**Attribute**</span></span>|<span data-ttu-id="e8499-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8499-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8499-111">**FieldURI**</span><span class="sxs-lookup"><span data-stu-id="e8499-111">**FieldURI**</span></span> <br/> |<span data-ttu-id="e8499-p101">Identifiziert das Wörterbuch, das Element zurückzugebenden enthält. Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e8499-p101">Identifies the dictionary that contains the member to return. This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="e8499-114">**FieldIndex**</span><span class="sxs-lookup"><span data-stu-id="e8499-114">**FieldIndex**</span></span> <br/> |<span data-ttu-id="e8499-p102">Bezeichnet den Member des Wörterbuchs zurückgegeben. Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e8499-p102">Identifies the member of the dictionary to return. This attribute is required.</span></span>  <br/> |
   
#### <a name="fielduri-attribute"></a><span data-ttu-id="e8499-117">FieldURI Attribute</span><span class="sxs-lookup"><span data-stu-id="e8499-117">FieldURI Attribute</span></span>

|<span data-ttu-id="e8499-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e8499-118">**Value**</span></span>|<span data-ttu-id="e8499-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8499-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8499-120">Element: InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="e8499-120">item:InternetMessageHeader</span></span>  <br/> |<span data-ttu-id="e8499-121">Der Nachrichtenkopf eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="e8499-121">Represents the message header of an item.</span></span>  <br/> |
|<span data-ttu-id="e8499-122">Kontakte: imaddresse</span><span class="sxs-lookup"><span data-stu-id="e8499-122">contacts:ImAddress</span></span>  <br/> |<span data-ttu-id="e8499-123">Stellt die Instant messaging-Adresse eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="e8499-123">Represents the instant messaging address of a contact.</span></span>  <br/> |
|<span data-ttu-id="e8499-124">Kontakte: PhysicalAddress: Street</span><span class="sxs-lookup"><span data-stu-id="e8499-124">contacts:PhysicalAddress:Street</span></span>  <br/> |<span data-ttu-id="e8499-125">Stellt die Straße eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="e8499-125">Represents the street address of a contact.</span></span>  <br/> |
|<span data-ttu-id="e8499-126">Kontakte: PhysicalAddress: City</span><span class="sxs-lookup"><span data-stu-id="e8499-126">contacts:PhysicalAddress:City</span></span>  <br/> |<span data-ttu-id="e8499-127">Stellt den Ort eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="e8499-127">Represents the city of a contact.</span></span>  <br/> |
|<span data-ttu-id="e8499-128">Kontakte: PhysicalAddress: State</span><span class="sxs-lookup"><span data-stu-id="e8499-128">contacts:PhysicalAddress:State</span></span>  <br/> |<span data-ttu-id="e8499-129">Stellt den Status eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="e8499-129">Represents the state of a contact.</span></span>  <br/> |
|<span data-ttu-id="e8499-130">Kontakte: PhysicalAddress: Country</span><span class="sxs-lookup"><span data-stu-id="e8499-130">contacts:PhysicalAddress:Country</span></span>  <br/> |<span data-ttu-id="e8499-131">Stellt das Land/Region eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="e8499-131">Represents the country/region of a contact.</span></span>  <br/> |
|<span data-ttu-id="e8499-132">Kontakte: PhysicalAddress: PostalCode</span><span class="sxs-lookup"><span data-stu-id="e8499-132">contacts:PhysicalAddress:PostalCode</span></span>  <br/> |<span data-ttu-id="e8499-133">Stellt die Postleitzahl des Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="e8499-133">Represents the postal code of a contact.</span></span>  <br/> |
|<span data-ttu-id="e8499-134">Kontakte: Faxnummer</span><span class="sxs-lookup"><span data-stu-id="e8499-134">contacts:PhoneNumber</span></span>  <br/> |<span data-ttu-id="e8499-135">Stellt die Rufnummer eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="e8499-135">Represents the phone number of a contact.</span></span>  <br/> |
|<span data-ttu-id="e8499-136">Kontakte: Email Adressbuch</span><span class="sxs-lookup"><span data-stu-id="e8499-136">contacts:EmailAddress</span></span>  <br/> |<span data-ttu-id="e8499-137">Stellt die e-Mail-Adresse eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="e8499-137">Represents the e-mail address of a contact.</span></span>  <br/> |
|<span data-ttu-id="e8499-138">DistributionList:Members:Member</span><span class="sxs-lookup"><span data-stu-id="e8499-138">distributionlist:Members:Member</span></span>  <br/> |<span data-ttu-id="e8499-139">Stellt ein Element einer Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="e8499-139">Represents a member of a distribution list.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e8499-140">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8499-140">Child elements</span></span>

<span data-ttu-id="e8499-141">Keine.</span><span class="sxs-lookup"><span data-stu-id="e8499-141">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e8499-142">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8499-142">Parent elements</span></span>

|<span data-ttu-id="e8499-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8499-143">**Element**</span></span>|<span data-ttu-id="e8499-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8499-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8499-145">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="e8499-145">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="e8499-146">Identifiziert zusätzliche Eigenschaften zum Abrufen, Festlegen oder Erstellen.</span><span class="sxs-lookup"><span data-stu-id="e8499-146">Identifies additional properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="e8499-147">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="e8499-147">AggregateOn</span></span>](aggregateon.md) <br/> |<span data-ttu-id="e8499-148">Stellt die Eigenschaft dar, die zum Ermitteln der Reihenfolge gruppierter Elemente für einen gruppierten FindItem-Ergebnissatz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8499-148">Represents the property that is used to determine the order of grouped items for a grouped FindItem result set.</span></span>  <br/> |
|[<span data-ttu-id="e8499-149">GroupBy</span><span class="sxs-lookup"><span data-stu-id="e8499-149">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="e8499-150">Gibt eine beliebige Gruppierung für FindItem-Abfragen an.</span><span class="sxs-lookup"><span data-stu-id="e8499-150">Specifies an arbitrary grouping for FindItem queries.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8499-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8499-151">Remarks</span></span>

<span data-ttu-id="e8499-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e8499-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8499-153">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e8499-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8499-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8499-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e8499-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e8499-155">Schema Name</span></span>  <br/> |<span data-ttu-id="e8499-156">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e8499-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="e8499-157">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e8499-157">Validation File</span></span>  <br/> |<span data-ttu-id="e8499-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e8499-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e8499-159">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e8499-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="e8499-160">False</span><span class="sxs-lookup"><span data-stu-id="e8499-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8499-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8499-161">See also</span></span>



- [<span data-ttu-id="e8499-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e8499-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

