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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462227"
---
# <a name="carphones"></a><span data-ttu-id="f600c-103">CarPhones</span><span class="sxs-lookup"><span data-stu-id="f600c-103">CarPhones</span></span>

<span data-ttu-id="f600c-104">Das **CarPhone** -Element gibt ein Array von Autotelefon Nummern und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.</span><span class="sxs-lookup"><span data-stu-id="f600c-104">The **CarPhone** element specifies an array of car phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<CarPhones>
    <Value></Value>
    <Attributions></Attributions>
</CarPhones>
```

 <span data-ttu-id="f600c-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="f600c-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f600c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f600c-106">Attributes and elements</span></span>

<span data-ttu-id="f600c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f600c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f600c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f600c-108">Attributes</span></span>

<span data-ttu-id="f600c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f600c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f600c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f600c-110">Child elements</span></span>

|<span data-ttu-id="f600c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f600c-111">**Element**</span></span>|<span data-ttu-id="f600c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f600c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f600c-113">Wert (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="f600c-113">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md) <br/> |<span data-ttu-id="f600c-114">Gibt eine Telefonnummer und Typinformationen an und ist einer Gruppe von Attributes zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f600c-114">Specifies a phone number and type information and is associated with a set of attributions.</span></span>  <br/> |
|[<span data-ttu-id="f600c-115">Zuordnungen (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="f600c-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="f600c-116">Gibt ein Array von Attributes für das zugehörige **value** -Element an.</span><span class="sxs-lookup"><span data-stu-id="f600c-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f600c-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f600c-117">Parent elements</span></span>

|<span data-ttu-id="f600c-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="f600c-118">**Element**</span></span>|<span data-ttu-id="f600c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f600c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f600c-120">Persona</span><span class="sxs-lookup"><span data-stu-id="f600c-120">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="f600c-121">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f600c-121">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f600c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f600c-122">Remarks</span></span>

<span data-ttu-id="f600c-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f600c-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f600c-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f600c-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f600c-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f600c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f600c-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="f600c-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f600c-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f600c-127">Schema Name</span></span>  <br/> |<span data-ttu-id="f600c-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="f600c-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="f600c-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f600c-129">Validation File</span></span>  <br/> |<span data-ttu-id="f600c-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f600c-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f600c-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f600c-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f600c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f600c-132">See also</span></span>



- [<span data-ttu-id="f600c-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f600c-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

