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
description: Das Files-Element stellt dar, wie ein Kontakt oder eine Verteilerliste im Ordner Kontakte gespeichert wird.
ms.openlocfilehash: be756d86d7608fcb758dd54f2ada9f03a04343e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461198"
---
# <a name="fileas"></a><span data-ttu-id="6d4f7-103">FileAs</span><span class="sxs-lookup"><span data-stu-id="6d4f7-103">FileAs</span></span>

<span data-ttu-id="6d4f7-104">Das **Files** -Element stellt dar, wie ein Kontakt oder eine Verteilerliste im Ordner Kontakte gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="6d4f7-104">The **FileAs** element represents how a contact or distribution list is filed in the Contacts folder.</span></span> 
  
```xml
<FileAs/>
```

 <span data-ttu-id="6d4f7-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6d4f7-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d4f7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6d4f7-106">Attributes and elements</span></span>

<span data-ttu-id="6d4f7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6d4f7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d4f7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6d4f7-108">Attributes</span></span>

<span data-ttu-id="6d4f7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6d4f7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d4f7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6d4f7-110">Child elements</span></span>

<span data-ttu-id="6d4f7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6d4f7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6d4f7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6d4f7-112">Parent elements</span></span>

|<span data-ttu-id="6d4f7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d4f7-113">**Element**</span></span>|<span data-ttu-id="6d4f7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6d4f7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d4f7-115">DistributionList</span><span class="sxs-lookup"><span data-stu-id="6d4f7-115">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="6d4f7-116">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="6d4f7-116">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="6d4f7-117">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="6d4f7-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="6d4f7-118">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="6d4f7-118">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6d4f7-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="6d4f7-119">Text value</span></span>

<span data-ttu-id="6d4f7-120">Ein Textwert, der eine Zeichenfolge darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d4f7-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d4f7-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d4f7-121">Remarks</span></span>

<span data-ttu-id="6d4f7-122">Das **Files** -Element wird verwendet, um Kontakte und Verteilerlisten nach einem Namen zu sortieren, der nicht vollständiger Name oder Firmenname ist.</span><span class="sxs-lookup"><span data-stu-id="6d4f7-122">The **FileAs** element is used to sort contacts and distribution lists by a name other than a full name or company name.</span></span> 
  
<span data-ttu-id="6d4f7-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6d4f7-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d4f7-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6d4f7-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d4f7-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d4f7-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6d4f7-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6d4f7-126">Schema name</span></span>  <br/> |<span data-ttu-id="6d4f7-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6d4f7-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="6d4f7-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6d4f7-128">Validation file</span></span>  <br/> |<span data-ttu-id="6d4f7-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6d4f7-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6d4f7-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6d4f7-130">Can be empty</span></span>  <br/> |<span data-ttu-id="6d4f7-131">False</span><span class="sxs-lookup"><span data-stu-id="6d4f7-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d4f7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d4f7-132">See also</span></span>



- [<span data-ttu-id="6d4f7-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6d4f7-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

