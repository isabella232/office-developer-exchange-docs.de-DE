---
title: HomePhones2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ba9bb159-362d-48e0-889d-823cb46ecebf
description: Das HomePhones2-Element gibt ein Array von Werten HomePhone2 und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: 205f2f71421a0dfc7d0057412529bcefdb6636d5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829842"
---
# <a name="homephones2"></a><span data-ttu-id="020f5-103">HomePhones2</span><span class="sxs-lookup"><span data-stu-id="020f5-103">HomePhones2</span></span>

<span data-ttu-id="020f5-104">Das **HomePhones2** -Element gibt ein Array von Werten **HomePhone2** und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="020f5-104">The **HomePhones2** element specifies an array of **HomePhone2** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomePhones2>
    <PhoneNumberAttributedValue/>
</HomePhones2>
```

 <span data-ttu-id="020f5-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="020f5-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="020f5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="020f5-106">Attributes and elements</span></span>

<span data-ttu-id="020f5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="020f5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="020f5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="020f5-108">Attributes</span></span>

<span data-ttu-id="020f5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="020f5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="020f5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="020f5-110">Child elements</span></span>

|<span data-ttu-id="020f5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="020f5-111">**Element**</span></span>|<span data-ttu-id="020f5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="020f5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="020f5-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="020f5-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="020f5-114">Enthält eine einzelne attributierten Telefonnummer für eine Rolle.</span><span class="sxs-lookup"><span data-stu-id="020f5-114">Contains a single attributed phone number for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="020f5-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="020f5-115">Parent elements</span></span>

|<span data-ttu-id="020f5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="020f5-116">**Element**</span></span>|<span data-ttu-id="020f5-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="020f5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="020f5-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="020f5-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="020f5-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="020f5-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="020f5-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="020f5-120">Remarks</span></span>

<span data-ttu-id="020f5-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="020f5-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="020f5-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="020f5-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="020f5-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="020f5-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="020f5-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="020f5-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="020f5-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="020f5-125">Schema Name</span></span>  <br/> |<span data-ttu-id="020f5-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="020f5-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="020f5-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="020f5-127">Validation File</span></span>  <br/> |<span data-ttu-id="020f5-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="020f5-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="020f5-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="020f5-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="020f5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="020f5-130">See also</span></span>



- [<span data-ttu-id="020f5-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="020f5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

