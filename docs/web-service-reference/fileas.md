---
title: FileAs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAs
api_type:
- schema
ms.assetid: df50524e-471c-49d2-89fe-b2d0f61a1365
description: FileAs-Element darstellt, wie einen Kontakt oder Verteilerliste aus in den Ordner Kontakte eingereicht wird.
ms.openlocfilehash: dab9142eebf7691862e7970a7d1e8f5874393b94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758423"
---
# <a name="fileas"></a><span data-ttu-id="f52e1-103">FileAs</span><span class="sxs-lookup"><span data-stu-id="f52e1-103">FileAs</span></span>

<span data-ttu-id="f52e1-104">**FileAs** -Element darstellt, wie einen Kontakt oder Verteilerliste aus in den Ordner Kontakte eingereicht wird.</span><span class="sxs-lookup"><span data-stu-id="f52e1-104">The **FileAs** element represents how a contact or distribution list is filed in the Contacts folder.</span></span> 
  
```xml
<FileAs/>
```

 <span data-ttu-id="f52e1-105">**string**</span><span class="sxs-lookup"><span data-stu-id="f52e1-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f52e1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f52e1-106">Attributes and elements</span></span>

<span data-ttu-id="f52e1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f52e1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f52e1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f52e1-108">Attributes</span></span>

<span data-ttu-id="f52e1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f52e1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f52e1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f52e1-110">Child elements</span></span>

<span data-ttu-id="f52e1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f52e1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f52e1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f52e1-112">Parent elements</span></span>

|<span data-ttu-id="f52e1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f52e1-113">**Element**</span></span>|<span data-ttu-id="f52e1-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f52e1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f52e1-115">DistributionList</span><span class="sxs-lookup"><span data-stu-id="f52e1-115">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="f52e1-116">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="f52e1-116">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="f52e1-117">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="f52e1-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="f52e1-118">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="f52e1-118">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f52e1-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="f52e1-119">Text value</span></span>

<span data-ttu-id="f52e1-120">Ein Textwert, der eine Zeichenfolge darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f52e1-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f52e1-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f52e1-121">Remarks</span></span>

<span data-ttu-id="f52e1-122">**FileAs** -Element wird zum Sortieren der Kontakte und Verteilerlisten durch einen anderen Namen als den vollständigen Namen oder Firmenname verwendet.</span><span class="sxs-lookup"><span data-stu-id="f52e1-122">The **FileAs** element is used to sort contacts and distribution lists by a name other than a full name or company name.</span></span> 
  
<span data-ttu-id="f52e1-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f52e1-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f52e1-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f52e1-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f52e1-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f52e1-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f52e1-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f52e1-126">Schema name</span></span>  <br/> |<span data-ttu-id="f52e1-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f52e1-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="f52e1-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f52e1-128">Validation file</span></span>  <br/> |<span data-ttu-id="f52e1-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f52e1-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f52e1-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f52e1-130">Can be empty</span></span>  <br/> |<span data-ttu-id="f52e1-131">False</span><span class="sxs-lookup"><span data-stu-id="f52e1-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f52e1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f52e1-132">See also</span></span>



- [<span data-ttu-id="f52e1-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f52e1-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

