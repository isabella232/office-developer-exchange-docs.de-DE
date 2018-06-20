---
title: AlternateId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternateId
api_type:
- schema
ms.assetid: 9c01fdc3-4adf-4e23-bc33-45d2a45ea08b
description: AlternateId-Element beschreibt einen Bezeichner für die Konvertierung in einer Anforderung und die Ergebnisse einer konvertierten-ID in der Antwort.
ms.openlocfilehash: e4d29087b63b52638dd93e4e3b643cdee39a5b97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757254"
---
# <a name="alternateid"></a><span data-ttu-id="44c6e-103">AlternateId</span><span class="sxs-lookup"><span data-stu-id="44c6e-103">AlternateId</span></span>

<span data-ttu-id="44c6e-104">**AlternateId** -Element beschreibt einen Bezeichner für die Konvertierung in einer Anforderung und die Ergebnisse einer konvertierten-ID in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="44c6e-104">The **AlternateId** element describes an identifier to convert in a request and the results of a converted identifier in the response.</span></span> 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 <span data-ttu-id="44c6e-105">**AlternateIdType**</span><span class="sxs-lookup"><span data-stu-id="44c6e-105">**AlternateIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44c6e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="44c6e-106">Attributes and elements</span></span>

<span data-ttu-id="44c6e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="44c6e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44c6e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="44c6e-108">Attributes</span></span>

|<span data-ttu-id="44c6e-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="44c6e-109">**Attribute**</span></span>|<span data-ttu-id="44c6e-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44c6e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="44c6e-111">Id</span><span class="sxs-lookup"><span data-stu-id="44c6e-111">Id</span></span>  <br/> |<span data-ttu-id="44c6e-112">Beschreibt den Quellbezeichner in einer Anforderung [ConvertId Vorgang](convertid-operation.md) und die Ziel-ID in eine Antwort [ConvertId Vorgang](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="44c6e-112">Describes the source identifier in a [ConvertId operation](convertid-operation.md) request and describes the destination identifier in a [ConvertId operation](convertid-operation.md) response.</span></span>  <br/> |
|<span data-ttu-id="44c6e-113">Format</span><span class="sxs-lookup"><span data-stu-id="44c6e-113">Format</span></span>  <br/> |<span data-ttu-id="44c6e-114">Beschreibt das Format der Quelle in einer Anforderung [ConvertId Vorgang](convertid-operation.md) und das Zielformat in einer Antwort [ConvertId Vorgang](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="44c6e-114">Describes the source format in a [ConvertId operation](convertid-operation.md) request and describes the destination format in a [ConvertId operation](convertid-operation.md) response.</span></span> <span data-ttu-id="44c6e-115">Das Zielformat wird vom **DestinationFormat** -Attribut des [ConvertId](convertid.md) -Elements in der Anforderung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="44c6e-115">The destination format is described by the **DestinationFormat** attribute of the [ConvertId](convertid.md) element in the request.</span></span> <span data-ttu-id="44c6e-116">Dieses Attribut ist vom Typ **IdFormatType**.</span><span class="sxs-lookup"><span data-stu-id="44c6e-116">This attribute is of type **IdFormatType**.</span></span>  <br/> |
|<span data-ttu-id="44c6e-117">Postfach</span><span class="sxs-lookup"><span data-stu-id="44c6e-117">Mailbox</span></span>  <br/> |<span data-ttu-id="44c6e-118">Beschreibt die Postfach der primäre Simple Mail Transfer Protocol (SMTP)-Adresse, die die Bezeichner übersetzen enthält.</span><span class="sxs-lookup"><span data-stu-id="44c6e-118">Describes the mailbox primary Simple Mail Transfer Protocol (SMTP) address that contains the identifiers to translate.</span></span>  <br/> |
|<span data-ttu-id="44c6e-119">IsArchive</span><span class="sxs-lookup"><span data-stu-id="44c6e-119">IsArchive</span></span>  <br/> |<span data-ttu-id="44c6e-120">Gibt an, ob der Bezeichner eines archivierten Elements oder Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="44c6e-120">Indicates whether the identifier represents an archived item or folder.</span></span> <span data-ttu-id="44c6e-121">Der Wert **true** gibt an, dass der Bezeichner eines archivierten Elements oder Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="44c6e-121">A value of **true** indicates that the identifier represents an archived item or folder.</span></span> <span data-ttu-id="44c6e-122">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="44c6e-122">This attribute is optional.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="44c6e-123">Format-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="44c6e-123">Format attribute values</span></span>

|<span data-ttu-id="44c6e-124">**Wert**</span><span class="sxs-lookup"><span data-stu-id="44c6e-124">**Value**</span></span>|<span data-ttu-id="44c6e-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44c6e-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="44c6e-126">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="44c6e-126">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="44c6e-127">Beschreibt Bezeichner, die in der ursprünglich freigegebenen Version von Exchange 2007 von Exchange-Webdienste erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="44c6e-127">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="44c6e-128">EwsId</span><span class="sxs-lookup"><span data-stu-id="44c6e-128">EwsId</span></span>  <br/> |<span data-ttu-id="44c6e-129">Beschreibt Bezeichner, die von der Exchange-Webdienste beginnend mit Exchange 2007 SP1 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="44c6e-129">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="44c6e-130">EntryId</span><span class="sxs-lookup"><span data-stu-id="44c6e-130">EntryId</span></span>  <br/> |<span data-ttu-id="44c6e-131">MAPI-IDs, wie in der **PR_ENTRYID** -Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="44c6e-131">Describes MAPI identifiers, as in the **PR_ENTRYID** property.</span></span>  <br/> |
|<span data-ttu-id="44c6e-132">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="44c6e-132">HexEntryId</span></span>  <br/> |<span data-ttu-id="44c6e-133">Beschreibt eine hexadezimal-codierte Darstellung der **PR_ENTRYID** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="44c6e-133">Describes a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="44c6e-134">Dies ist das Format der Verfügbarkeit Kalender-Ereignis-IDs.</span><span class="sxs-lookup"><span data-stu-id="44c6e-134">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="44c6e-135">StoreId</span><span class="sxs-lookup"><span data-stu-id="44c6e-135">StoreId</span></span>  <br/> |<span data-ttu-id="44c6e-136">Beschreibt die Exchange-Speicher-IDs.</span><span class="sxs-lookup"><span data-stu-id="44c6e-136">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="44c6e-137">OwaId</span><span class="sxs-lookup"><span data-stu-id="44c6e-137">OwaId</span></span>  <br/> |<span data-ttu-id="44c6e-138">Beschreibt einen Outlook Web App-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="44c6e-138">Describes an Outlook Web App identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="44c6e-139">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44c6e-139">Child elements</span></span>

<span data-ttu-id="44c6e-140">Keine.</span><span class="sxs-lookup"><span data-stu-id="44c6e-140">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="44c6e-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44c6e-141">Parent elements</span></span>

|<span data-ttu-id="44c6e-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="44c6e-142">**Element**</span></span>|<span data-ttu-id="44c6e-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44c6e-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44c6e-144">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="44c6e-144">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md) <br/> |<span data-ttu-id="44c6e-145">Enthält den Status und das Ergebnis einer Anforderung [ConvertId Vorgang](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="44c6e-145">Contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="44c6e-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="44c6e-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="44c6e-147">Enthält die Bezeichner der Quelle zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="44c6e-147">Contains the source identifiers to convert.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="44c6e-148">Textwert</span><span class="sxs-lookup"><span data-stu-id="44c6e-148">Text value</span></span>

<span data-ttu-id="44c6e-149">Keine.</span><span class="sxs-lookup"><span data-stu-id="44c6e-149">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44c6e-150">Hinweise</span><span class="sxs-lookup"><span data-stu-id="44c6e-150">Remarks</span></span>

<span data-ttu-id="44c6e-151">**AlternateId** -Element werden zwei Bezeichner, der Source-Bezeichner, der in der Anforderung [ConvertId Vorgang](convertid-operation.md) konvertiert werden soll und der konvertierten Bezeichner im [ConvertIdResponse](convertidresponse.md) -Element beschrieben.</span><span class="sxs-lookup"><span data-stu-id="44c6e-151">The **AlternateId** element describes two identifiers, the source identifier that is to be converted in the [ConvertId operation](convertid-operation.md) request, and the converted identifier in the [ConvertIdResponse](convertidresponse.md) element.</span></span> 
  
<span data-ttu-id="44c6e-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="44c6e-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44c6e-153">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="44c6e-153">Element information</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="44c6e-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="44c6e-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="44c6e-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="44c6e-155">Schema Name</span></span>  <br/> |<span data-ttu-id="44c6e-156">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="44c6e-156">Messages schema</span></span>  <br/> |<span data-ttu-id="44c6e-157">Schematypen</span><span class="sxs-lookup"><span data-stu-id="44c6e-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="44c6e-158">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="44c6e-158">Validation File</span></span>  <br/> |<span data-ttu-id="44c6e-159">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="44c6e-159">Messages.xsd</span></span>  <br/> |<span data-ttu-id="44c6e-160">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="44c6e-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="44c6e-161">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="44c6e-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="44c6e-162">False</span><span class="sxs-lookup"><span data-stu-id="44c6e-162">False</span></span>  <br/> |<span data-ttu-id="44c6e-163">False</span><span class="sxs-lookup"><span data-stu-id="44c6e-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44c6e-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44c6e-164">See also</span></span>

- [<span data-ttu-id="44c6e-165">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="44c6e-165">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="44c6e-166">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="44c6e-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="44c6e-167">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="44c6e-167">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

