---
title: BusinessPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ecbe4f1c-1c9e-44e0-a8f7-08c160a0fddb
description: Das BusinessPhoneNumbers-Element gibt ein Array von Geschäftstelefon Nummern und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.
ms.openlocfilehash: 8713af3ad302a2940cab247ff7188e55e8021ca0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461618"
---
# <a name="businessphonenumbers"></a><span data-ttu-id="da0b9-103">BusinessPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="da0b9-103">BusinessPhoneNumbers</span></span>

<span data-ttu-id="da0b9-104">Das **BusinessPhoneNumbers** -Element gibt ein Array von Geschäftstelefon Nummern und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.</span><span class="sxs-lookup"><span data-stu-id="da0b9-104">The **BusinessPhoneNumbers** element specifies an array of business phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessPhoneNumbers>
    <Value></Value>
    <Attributions></Attributions>
</BusinessPhoneNumbers>
```

 <span data-ttu-id="da0b9-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="da0b9-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da0b9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="da0b9-106">Attributes and elements</span></span>

<span data-ttu-id="da0b9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="da0b9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da0b9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="da0b9-108">Attributes</span></span>

<span data-ttu-id="da0b9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="da0b9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da0b9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da0b9-110">Child elements</span></span>

|<span data-ttu-id="da0b9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="da0b9-111">**Element**</span></span>|<span data-ttu-id="da0b9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da0b9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da0b9-113">Wert (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="da0b9-113">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md) <br/> |<span data-ttu-id="da0b9-114">Gibt eine Telefonnummer und Typinformationen an und ist einer Gruppe von Attributes zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="da0b9-114">Specifies a phone number and type information and is associated with a set of attributions.</span></span>  <br/> |
|[<span data-ttu-id="da0b9-115">Zuordnungen (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="da0b9-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="da0b9-116">Gibt ein Array von Attributes für das zugehörige **value** -Element an.</span><span class="sxs-lookup"><span data-stu-id="da0b9-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="da0b9-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da0b9-117">Parent elements</span></span>

|<span data-ttu-id="da0b9-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="da0b9-118">**Element**</span></span>|<span data-ttu-id="da0b9-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da0b9-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da0b9-120">Persona</span><span class="sxs-lookup"><span data-stu-id="da0b9-120">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="da0b9-121">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="da0b9-121">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da0b9-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da0b9-122">Remarks</span></span>

<span data-ttu-id="da0b9-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="da0b9-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="da0b9-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="da0b9-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da0b9-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="da0b9-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da0b9-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="da0b9-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="da0b9-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="da0b9-127">Schema Name</span></span>  <br/> |<span data-ttu-id="da0b9-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="da0b9-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="da0b9-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="da0b9-129">Validation File</span></span>  <br/> |<span data-ttu-id="da0b9-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="da0b9-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="da0b9-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="da0b9-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="da0b9-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da0b9-132">See also</span></span>



- [<span data-ttu-id="da0b9-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="da0b9-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

