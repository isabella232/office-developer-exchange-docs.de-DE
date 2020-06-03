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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461198"
---
# <a name="fileas"></a><span data-ttu-id="28218-103">FileAs</span><span class="sxs-lookup"><span data-stu-id="28218-103">FileAs</span></span>

<span data-ttu-id="28218-104">Das **Files** -Element stellt dar, wie ein Kontakt oder eine Verteilerliste im Ordner Kontakte gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="28218-104">The **FileAs** element represents how a contact or distribution list is filed in the Contacts folder.</span></span> 
  
```xml
<FileAs/>
```

 <span data-ttu-id="28218-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="28218-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28218-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="28218-106">Attributes and elements</span></span>

<span data-ttu-id="28218-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="28218-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28218-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="28218-108">Attributes</span></span>

<span data-ttu-id="28218-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="28218-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28218-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28218-110">Child elements</span></span>

<span data-ttu-id="28218-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="28218-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="28218-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28218-112">Parent elements</span></span>

|<span data-ttu-id="28218-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="28218-113">**Element**</span></span>|<span data-ttu-id="28218-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28218-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28218-115">DistributionList</span><span class="sxs-lookup"><span data-stu-id="28218-115">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="28218-116">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="28218-116">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="28218-117">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="28218-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="28218-118">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="28218-118">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="28218-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="28218-119">Text value</span></span>

<span data-ttu-id="28218-120">Ein Textwert, der eine Zeichenfolge darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="28218-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28218-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28218-121">Remarks</span></span>

<span data-ttu-id="28218-122">Das **Files** -Element wird verwendet, um Kontakte und Verteilerlisten nach einem Namen zu sortieren, der nicht vollständiger Name oder Firmenname ist.</span><span class="sxs-lookup"><span data-stu-id="28218-122">The **FileAs** element is used to sort contacts and distribution lists by a name other than a full name or company name.</span></span> 
  
<span data-ttu-id="28218-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="28218-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28218-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="28218-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28218-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="28218-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="28218-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="28218-126">Schema name</span></span>  <br/> |<span data-ttu-id="28218-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="28218-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="28218-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="28218-128">Validation file</span></span>  <br/> |<span data-ttu-id="28218-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="28218-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="28218-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="28218-130">Can be empty</span></span>  <br/> |<span data-ttu-id="28218-131">False</span><span class="sxs-lookup"><span data-stu-id="28218-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28218-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28218-132">See also</span></span>



- [<span data-ttu-id="28218-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="28218-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

