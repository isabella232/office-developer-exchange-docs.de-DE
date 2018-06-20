---
title: BusinessPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ecbe4f1c-1c9e-44e0-a8f7-08c160a0fddb
description: Das BusinessPhoneNumbers-Element gibt ein Array von geschäftlichen Telefonnummer und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: 692c38a00241da9f753c431612f4a8fcf26cc7ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757511"
---
# <a name="businessphonenumbers"></a><span data-ttu-id="eb956-103">BusinessPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="eb956-103">BusinessPhoneNumbers</span></span>

<span data-ttu-id="eb956-104">Das **BusinessPhoneNumbers** -Element gibt ein Array von geschäftlichen Telefonnummer und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="eb956-104">The **BusinessPhoneNumbers** element specifies an array of business phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessPhoneNumbers>
    <Value></Value>
    <Attributions></Attributions>
</BusinessPhoneNumbers>
```

 <span data-ttu-id="eb956-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="eb956-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb956-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="eb956-106">Attributes and elements</span></span>

<span data-ttu-id="eb956-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="eb956-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb956-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="eb956-108">Attributes</span></span>

<span data-ttu-id="eb956-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="eb956-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb956-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb956-110">Child elements</span></span>

|<span data-ttu-id="eb956-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb956-111">**Element**</span></span>|<span data-ttu-id="eb956-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eb956-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb956-113">Wert (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="eb956-113">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md) <br/> |<span data-ttu-id="eb956-114">Gibt eine Telefoninformationen Anzahl und Typ und eine Reihe von Marken zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="eb956-114">Specifies a phone number and type information and is associated with a set of attributions.</span></span>  <br/> |
|[<span data-ttu-id="eb956-115">Hinweise (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="eb956-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="eb956-116">Gibt ein Array von Marken für zugeordneten **Wert** Elements an.</span><span class="sxs-lookup"><span data-stu-id="eb956-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eb956-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb956-117">Parent elements</span></span>

|<span data-ttu-id="eb956-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb956-118">**Element**</span></span>|<span data-ttu-id="eb956-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eb956-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb956-120">Rolle</span><span class="sxs-lookup"><span data-stu-id="eb956-120">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="eb956-121">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eb956-121">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb956-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eb956-122">Remarks</span></span>

<span data-ttu-id="eb956-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eb956-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="eb956-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="eb956-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb956-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="eb956-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb956-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb956-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eb956-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="eb956-127">Schema Name</span></span>  <br/> |<span data-ttu-id="eb956-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="eb956-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="eb956-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="eb956-129">Validation File</span></span>  <br/> |<span data-ttu-id="eb956-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eb956-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="eb956-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="eb956-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="eb956-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb956-132">See also</span></span>



- [<span data-ttu-id="eb956-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="eb956-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

