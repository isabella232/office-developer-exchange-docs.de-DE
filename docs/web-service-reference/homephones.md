---
title: HomePhones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8ea43d5a-4bcf-497e-a559-6efe94fa604b
description: Das HomePhones-Element gibt ein Array von privaten Telefonnummern und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: 487d37e6a18bbd480a814de7570b0789f148096e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829844"
---
# <a name="homephones"></a><span data-ttu-id="2fb02-103">HomePhones</span><span class="sxs-lookup"><span data-stu-id="2fb02-103">HomePhones</span></span>

<span data-ttu-id="2fb02-104">Das **HomePhones** -Element gibt ein Array von privaten Telefonnummern und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="2fb02-104">The **HomePhones** element specifies an array of home phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomePhones>
    <PhoneNumberAttributedValue/>
</HomePhones>
```

 <span data-ttu-id="2fb02-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="2fb02-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2fb02-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2fb02-106">Attributes and elements</span></span>

<span data-ttu-id="2fb02-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2fb02-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2fb02-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2fb02-108">Attributes</span></span>

<span data-ttu-id="2fb02-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2fb02-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2fb02-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2fb02-110">Child elements</span></span>

|<span data-ttu-id="2fb02-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2fb02-111">**Element**</span></span>|<span data-ttu-id="2fb02-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2fb02-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2fb02-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="2fb02-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="2fb02-114">Enthält eine einzelne attributierten Telefonnummer für eine Rolle.</span><span class="sxs-lookup"><span data-stu-id="2fb02-114">Contains a single attributed phone number for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2fb02-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2fb02-115">Parent elements</span></span>

|<span data-ttu-id="2fb02-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2fb02-116">**Element**</span></span>|<span data-ttu-id="2fb02-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2fb02-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2fb02-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="2fb02-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="2fb02-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2fb02-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fb02-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2fb02-120">Remarks</span></span>

<span data-ttu-id="2fb02-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2fb02-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2fb02-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2fb02-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2fb02-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2fb02-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2fb02-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2fb02-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2fb02-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2fb02-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2fb02-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="2fb02-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="2fb02-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2fb02-127">Validation File</span></span>  <br/> |<span data-ttu-id="2fb02-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2fb02-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2fb02-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2fb02-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2fb02-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fb02-130">See also</span></span>



- [<span data-ttu-id="2fb02-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2fb02-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

