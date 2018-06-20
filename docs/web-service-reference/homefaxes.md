---
title: HomeFaxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 459ddb1c-8cff-4125-b6fa-dc93c183dee8
description: Das HomeFaxes-Element gibt ein Array von Fax privat Zahlen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: dd2cd8bba2c4cc7d08e88787d648e96ea996a251
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829840"
---
# <a name="homefaxes"></a><span data-ttu-id="6156a-103">HomeFaxes</span><span class="sxs-lookup"><span data-stu-id="6156a-103">HomeFaxes</span></span>

<span data-ttu-id="6156a-104">Das **HomeFaxes** -Element gibt ein Array von Fax privat Zahlen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="6156a-104">The **HomeFaxes** element specifies an array of home fax numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomeFaxes>
    <PhoneNumberAttributedValue/>
</HomeFaxes>
```

 <span data-ttu-id="6156a-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="6156a-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6156a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6156a-106">Attributes and elements</span></span>

<span data-ttu-id="6156a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6156a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6156a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6156a-108">Attributes</span></span>

<span data-ttu-id="6156a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6156a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6156a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6156a-110">Child elements</span></span>

|<span data-ttu-id="6156a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6156a-111">**Element**</span></span>|<span data-ttu-id="6156a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6156a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6156a-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="6156a-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="6156a-114">Enthält eine einzelne attributierten Telefonnummer für eine Rolle.</span><span class="sxs-lookup"><span data-stu-id="6156a-114">Contains a single attributed phone number for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6156a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6156a-115">Parent elements</span></span>

|<span data-ttu-id="6156a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="6156a-116">**Element**</span></span>|<span data-ttu-id="6156a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6156a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6156a-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="6156a-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="6156a-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6156a-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6156a-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6156a-120">Remarks</span></span>

<span data-ttu-id="6156a-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6156a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6156a-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6156a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6156a-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6156a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6156a-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="6156a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6156a-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6156a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="6156a-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="6156a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="6156a-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6156a-127">Validation File</span></span>  <br/> |<span data-ttu-id="6156a-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6156a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="6156a-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6156a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="6156a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6156a-130">See also</span></span>



- [<span data-ttu-id="6156a-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6156a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

