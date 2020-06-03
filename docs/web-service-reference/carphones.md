---
title: CarPhones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ad096246-113c-42ea-9e63-861b546003e8
description: Das CarPhone-Element gibt ein Array von Autotelefon Nummern und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.
ms.openlocfilehash: 41d0cc264da69ab17b8ebf109759139c4249719e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462227"
---
# <a name="carphones"></a><span data-ttu-id="c4b11-103">CarPhones</span><span class="sxs-lookup"><span data-stu-id="c4b11-103">CarPhones</span></span>

<span data-ttu-id="c4b11-104">Das **CarPhone** -Element gibt ein Array von Autotelefon Nummern und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.</span><span class="sxs-lookup"><span data-stu-id="c4b11-104">The **CarPhone** element specifies an array of car phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<CarPhones>
    <Value></Value>
    <Attributions></Attributions>
</CarPhones>
```

 <span data-ttu-id="c4b11-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="c4b11-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4b11-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c4b11-106">Attributes and elements</span></span>

<span data-ttu-id="c4b11-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c4b11-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4b11-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c4b11-108">Attributes</span></span>

<span data-ttu-id="c4b11-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c4b11-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4b11-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4b11-110">Child elements</span></span>

|<span data-ttu-id="c4b11-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4b11-111">**Element**</span></span>|<span data-ttu-id="c4b11-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4b11-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4b11-113">Wert (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="c4b11-113">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md) <br/> |<span data-ttu-id="c4b11-114">Gibt eine Telefonnummer und Typinformationen an und ist einer Gruppe von Attributes zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c4b11-114">Specifies a phone number and type information and is associated with a set of attributions.</span></span>  <br/> |
|[<span data-ttu-id="c4b11-115">Zuordnungen (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="c4b11-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="c4b11-116">Gibt ein Array von Attributes für das zugehörige **value** -Element an.</span><span class="sxs-lookup"><span data-stu-id="c4b11-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c4b11-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4b11-117">Parent elements</span></span>

|<span data-ttu-id="c4b11-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4b11-118">**Element**</span></span>|<span data-ttu-id="c4b11-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4b11-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4b11-120">Persona</span><span class="sxs-lookup"><span data-stu-id="c4b11-120">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="c4b11-121">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4b11-121">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4b11-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4b11-122">Remarks</span></span>

<span data-ttu-id="c4b11-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c4b11-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c4b11-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c4b11-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4b11-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c4b11-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4b11-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4b11-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4b11-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c4b11-127">Schema Name</span></span>  <br/> |<span data-ttu-id="c4b11-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="c4b11-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="c4b11-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c4b11-129">Validation File</span></span>  <br/> |<span data-ttu-id="c4b11-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c4b11-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4b11-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c4b11-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c4b11-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4b11-132">See also</span></span>



- [<span data-ttu-id="c4b11-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c4b11-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

