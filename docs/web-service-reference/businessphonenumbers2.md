---
title: BusinessPhoneNumbers2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f335ea74-9b5b-4224-9475-40ef33fe76bd
description: Das BusinessPhoneNumbers2-Element gibt ein Array von BusinessPhoneNumber2-Elementen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.
ms.openlocfilehash: c8879e3f7ab996d7e761a72b7ce5f332a9006aed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461604"
---
# <a name="businessphonenumbers2"></a><span data-ttu-id="6fdcf-103">BusinessPhoneNumbers2</span><span class="sxs-lookup"><span data-stu-id="6fdcf-103">BusinessPhoneNumbers2</span></span>

<span data-ttu-id="6fdcf-104">Das **BusinessPhoneNumbers2** -Element gibt ein Array von **BusinessPhoneNumber2** -Elementen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-104">The **BusinessPhoneNumbers2** element specifies an array of **BusinessPhoneNumber2** elements and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessPhoneNumbers2>
    <Value></Value>
    <Attributions></Attributions>
</BusinessPhoneNumbers2>
```

 <span data-ttu-id="6fdcf-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6fdcf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6fdcf-106">Attributes and elements</span></span>

<span data-ttu-id="6fdcf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6fdcf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6fdcf-108">Attributes</span></span>

<span data-ttu-id="6fdcf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6fdcf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fdcf-110">Child elements</span></span>

|<span data-ttu-id="6fdcf-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-111">**Element**</span></span>|<span data-ttu-id="6fdcf-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6fdcf-113">Wert (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="6fdcf-113">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md) <br/> |<span data-ttu-id="6fdcf-114">Gibt eine Telefonnummer und Typinformationen an und ist einer Gruppe von Attributes zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-114">Specifies a phone number and type information and is associated with a set of attributions.</span></span>  <br/> |
|[<span data-ttu-id="6fdcf-115">Zuordnungen (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="6fdcf-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="6fdcf-116">Gibt ein Array von Attributes für das zugehörige **value** -Element an.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6fdcf-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fdcf-117">Parent elements</span></span>

|<span data-ttu-id="6fdcf-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-118">**Element**</span></span>|<span data-ttu-id="6fdcf-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6fdcf-120">Persona</span><span class="sxs-lookup"><span data-stu-id="6fdcf-120">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="6fdcf-121">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-121">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fdcf-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fdcf-122">Remarks</span></span>

<span data-ttu-id="6fdcf-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6fdcf-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6fdcf-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6fdcf-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fdcf-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="6fdcf-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6fdcf-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6fdcf-127">Schema Name</span></span>  <br/> |<span data-ttu-id="6fdcf-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="6fdcf-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="6fdcf-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6fdcf-129">Validation File</span></span>  <br/> |<span data-ttu-id="6fdcf-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6fdcf-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="6fdcf-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6fdcf-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="6fdcf-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fdcf-132">See also</span></span>



- [<span data-ttu-id="6fdcf-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6fdcf-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

