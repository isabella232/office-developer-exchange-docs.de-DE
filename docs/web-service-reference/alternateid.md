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
description: Das Alternate-ID-Element beschreibt einen Bezeichner, der in einer Anforderung konvertiert werden soll, sowie die Ergebnisse eines konvertierten Bezeichners in der Antwort.
ms.openlocfilehash: 26df68bd814c2d323630c6bb40b4c31745017c71
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527453"
---
# <a name="alternateid"></a><span data-ttu-id="7a81e-103">AlternateId</span><span class="sxs-lookup"><span data-stu-id="7a81e-103">AlternateId</span></span>

<span data-ttu-id="7a81e-104">Das **Alternate** -ID-Element beschreibt einen Bezeichner, der in einer Anforderung konvertiert werden soll, sowie die Ergebnisse eines konvertierten Bezeichners in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="7a81e-104">The **AlternateId** element describes an identifier to convert in a request and the results of a converted identifier in the response.</span></span> 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 <span data-ttu-id="7a81e-105">**AlternateIdType**</span><span class="sxs-lookup"><span data-stu-id="7a81e-105">**AlternateIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a81e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7a81e-106">Attributes and elements</span></span>

<span data-ttu-id="7a81e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7a81e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a81e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a81e-108">Attributes</span></span>

|<span data-ttu-id="7a81e-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7a81e-109">**Attribute**</span></span>|<span data-ttu-id="7a81e-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a81e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a81e-111">Id</span><span class="sxs-lookup"><span data-stu-id="7a81e-111">Id</span></span>  <br/> |<span data-ttu-id="7a81e-112">Beschreibt den Quellbezeichner in einer [Konvertierungs](convertid-operation.md) -ID-Vorgangsanforderung und beschreibt den Zielbezeichner in einer [converto-Vorgangs](convertid-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="7a81e-112">Describes the source identifier in a [ConvertId operation](convertid-operation.md) request and describes the destination identifier in a [ConvertId operation](convertid-operation.md) response.</span></span>  <br/> |
|<span data-ttu-id="7a81e-113">Format</span><span class="sxs-lookup"><span data-stu-id="7a81e-113">Format</span></span>  <br/> |<span data-ttu-id="7a81e-114">Beschreibt das Quellformat in einer Anforderung für den [Konvertierungsvorgang](convertid-operation.md) und beschreibt das Zielformat in einer [Convert-Vorgangs](convertid-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="7a81e-114">Describes the source format in a [ConvertId operation](convertid-operation.md) request and describes the destination format in a [ConvertId operation](convertid-operation.md) response.</span></span> <span data-ttu-id="7a81e-115">Das Zielformat wird durch das **DestinationFormat** -Attribut des [Convert](convertid.md) -Elements in der Anforderung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7a81e-115">The destination format is described by the **DestinationFormat** attribute of the [ConvertId](convertid.md) element in the request.</span></span> <span data-ttu-id="7a81e-116">Dieses Attribut ist vom Typ **IdFormatType**.</span><span class="sxs-lookup"><span data-stu-id="7a81e-116">This attribute is of type **IdFormatType**.</span></span>  <br/> |
|<span data-ttu-id="7a81e-117">Postfach</span><span class="sxs-lookup"><span data-stu-id="7a81e-117">Mailbox</span></span>  <br/> |<span data-ttu-id="7a81e-118">Beschreibt die primäre Simple Mail Transfer Protocol (SMTP) Adresse des Postfachs, die die zu übersetzenden Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="7a81e-118">Describes the mailbox primary Simple Mail Transfer Protocol (SMTP) address that contains the identifiers to translate.</span></span>  <br/> |
|<span data-ttu-id="7a81e-119">IsArchive</span><span class="sxs-lookup"><span data-stu-id="7a81e-119">IsArchive</span></span>  <br/> |<span data-ttu-id="7a81e-120">Gibt an, ob der Bezeichner ein archiviertes Element oder einen Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="7a81e-120">Indicates whether the identifier represents an archived item or folder.</span></span> <span data-ttu-id="7a81e-121">Der Wert **true** gibt an, dass der Bezeichner ein archiviertes Element oder einen archivierten Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="7a81e-121">A value of **true** indicates that the identifier represents an archived item or folder.</span></span> <span data-ttu-id="7a81e-122">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="7a81e-122">This attribute is optional.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="7a81e-123">Formatieren von Attributwerten</span><span class="sxs-lookup"><span data-stu-id="7a81e-123">Format attribute values</span></span>

|<span data-ttu-id="7a81e-124">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7a81e-124">**Value**</span></span>|<span data-ttu-id="7a81e-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a81e-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a81e-126">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="7a81e-126">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="7a81e-127">Beschreibt Bezeichner, die von Exchange Webdienste in der ersten Version von Exchange 2007 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7a81e-127">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="7a81e-128">EwsId</span><span class="sxs-lookup"><span data-stu-id="7a81e-128">EwsId</span></span>  <br/> |<span data-ttu-id="7a81e-129">Beschreibt Bezeichner, die von Exchange Webdienste ab Exchange 2007 SP1 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7a81e-129">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="7a81e-130">EntryId</span><span class="sxs-lookup"><span data-stu-id="7a81e-130">EntryId</span></span>  <br/> |<span data-ttu-id="7a81e-131">Beschreibt MAPI-IDs wie in der **PR_ENTRYID** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7a81e-131">Describes MAPI identifiers, as in the **PR_ENTRYID** property.</span></span>  <br/> |
|<span data-ttu-id="7a81e-132">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="7a81e-132">HexEntryId</span></span>  <br/> |<span data-ttu-id="7a81e-133">Beschreibt eine hexadezimal codierte Darstellung der **PR_ENTRYID** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7a81e-133">Describes a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="7a81e-134">Dies ist das Format der Ereignisbezeichner für den Verfügbarkeitskalender.</span><span class="sxs-lookup"><span data-stu-id="7a81e-134">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="7a81e-135">StoreId</span><span class="sxs-lookup"><span data-stu-id="7a81e-135">StoreId</span></span>  <br/> |<span data-ttu-id="7a81e-136">Beschreibt Exchange-Informationsspeicher Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7a81e-136">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="7a81e-137">OwaId</span><span class="sxs-lookup"><span data-stu-id="7a81e-137">OwaId</span></span>  <br/> |<span data-ttu-id="7a81e-138">Beschreibt einen Outlook Web App Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7a81e-138">Describes an Outlook Web App identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7a81e-139">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a81e-139">Child elements</span></span>

<span data-ttu-id="7a81e-140">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a81e-140">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7a81e-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a81e-141">Parent elements</span></span>

|<span data-ttu-id="7a81e-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a81e-142">**Element**</span></span>|<span data-ttu-id="7a81e-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a81e-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a81e-144">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7a81e-144">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md) <br/> |<span data-ttu-id="7a81e-145">Enthält den Status und das Ergebnis einer [Konvertierungsvorgangs](convertid-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="7a81e-145">Contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="7a81e-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="7a81e-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="7a81e-147">Enthält die Quellbezeichner, die konvertiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a81e-147">Contains the source identifiers to convert.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7a81e-148">Textwert</span><span class="sxs-lookup"><span data-stu-id="7a81e-148">Text value</span></span>

<span data-ttu-id="7a81e-149">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a81e-149">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7a81e-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a81e-150">Remarks</span></span>

<span data-ttu-id="7a81e-151">Das **Alternate** -ID-Element beschreibt zwei Bezeichner, den Quellbezeichner, der in der Anforderung für den [Konvertierungsvorgang](convertid-operation.md) konvertiert werden soll, und den konvertierten Bezeichner im [ConvertIdResponse](convertidresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="7a81e-151">The **AlternateId** element describes two identifiers, the source identifier that is to be converted in the [ConvertId operation](convertid-operation.md) request, and the converted identifier in the [ConvertIdResponse](convertidresponse.md) element.</span></span> 
  
<span data-ttu-id="7a81e-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7a81e-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a81e-153">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7a81e-153">Element information</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="7a81e-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a81e-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a81e-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7a81e-155">Schema Name</span></span>  <br/> |<span data-ttu-id="7a81e-156">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7a81e-156">Messages schema</span></span>  <br/> |<span data-ttu-id="7a81e-157">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7a81e-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="7a81e-158">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7a81e-158">Validation File</span></span>  <br/> |<span data-ttu-id="7a81e-159">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7a81e-159">Messages.xsd</span></span>  <br/> |<span data-ttu-id="7a81e-160">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7a81e-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a81e-161">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7a81e-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a81e-162">False</span><span class="sxs-lookup"><span data-stu-id="7a81e-162">False</span></span>  <br/> |<span data-ttu-id="7a81e-163">False</span><span class="sxs-lookup"><span data-stu-id="7a81e-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a81e-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a81e-164">See also</span></span>

- [<span data-ttu-id="7a81e-165">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7a81e-165">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="7a81e-166">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a81e-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="7a81e-167">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="7a81e-167">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

