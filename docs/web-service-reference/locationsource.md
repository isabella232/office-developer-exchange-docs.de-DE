---
title: LocationSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: Das LocationSource-Element gibt Informationen über den Ursprung der zugeordneten Postadresse an, beispielsweise einen Kontakt oder ein Telefonbuch.
ms.openlocfilehash: ceba52c43d1c798bb8f5492b779c7c45d7d00b0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467102"
---
# <a name="locationsource"></a><span data-ttu-id="115fa-103">LocationSource</span><span class="sxs-lookup"><span data-stu-id="115fa-103">LocationSource</span></span>

<span data-ttu-id="115fa-104">Das **LocationSource** -Element gibt Informationen über den Ursprung der zugeordneten Postadresse an, beispielsweise einen Kontakt oder ein Telefonbuch.</span><span class="sxs-lookup"><span data-stu-id="115fa-104">The **LocationSource** element specifies information about the origin of the associated postal address, for example, a contact or a telephone book.</span></span> 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 <span data-ttu-id="115fa-105">**LocationSourceType**</span><span class="sxs-lookup"><span data-stu-id="115fa-105">**LocationSourceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="115fa-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="115fa-106">Attributes and elements</span></span>

<span data-ttu-id="115fa-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="115fa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="115fa-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="115fa-108">Attributes</span></span>

<span data-ttu-id="115fa-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="115fa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="115fa-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="115fa-110">Child elements</span></span>

<span data-ttu-id="115fa-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="115fa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="115fa-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="115fa-112">Parent elements</span></span>

<span data-ttu-id="115fa-113">[Wert (PersonaPostalAddressType)](value-personapostaladdresstype.md)  |  [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span><span class="sxs-lookup"><span data-stu-id="115fa-113">[Value (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="115fa-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="115fa-114">Text value</span></span>

<span data-ttu-id="115fa-115">Die Textwerte für das **LocationSource** -Element sind in der folgenden Tabelle aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="115fa-115">The text values for the **LocationSource** element are listed in the following table:</span></span> 
  
<span data-ttu-id="115fa-116">**LocationSource-Element Text Werte**</span><span class="sxs-lookup"><span data-stu-id="115fa-116">**LocationSource element text values**</span></span>

|<span data-ttu-id="115fa-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="115fa-117">**Value**</span></span>|<span data-ttu-id="115fa-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="115fa-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="115fa-119">Keine</span><span class="sxs-lookup"><span data-stu-id="115fa-119">None</span></span>  <br/> |<span data-ttu-id="115fa-120">Es gibt keine Standort Quelle.</span><span class="sxs-lookup"><span data-stu-id="115fa-120">There is no location source.</span></span>  <br/> |
|<span data-ttu-id="115fa-121">LocationServices</span><span class="sxs-lookup"><span data-stu-id="115fa-121">LocationServices</span></span>  <br/> |<span data-ttu-id="115fa-122">Die Informationen wurden von den Standortdiensten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="115fa-122">The information was obtained from location services.</span></span>  <br/> |
|<span data-ttu-id="115fa-123">PhonebookServices</span><span class="sxs-lookup"><span data-stu-id="115fa-123">PhonebookServices</span></span>  <br/> |<span data-ttu-id="115fa-124">Die Informationen wurden in Telefonbuch Diensten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="115fa-124">The information was obtained from phonebook services.</span></span>  <br/> |
|<span data-ttu-id="115fa-125">Gerät</span><span class="sxs-lookup"><span data-stu-id="115fa-125">Device</span></span>  <br/> |<span data-ttu-id="115fa-126">Die Informationen wurden vom Gerät abgerufen.</span><span class="sxs-lookup"><span data-stu-id="115fa-126">The information was obtained from the device.</span></span>  <br/> |
|<span data-ttu-id="115fa-127">Kontakt</span><span class="sxs-lookup"><span data-stu-id="115fa-127">Contact</span></span>  <br/> |<span data-ttu-id="115fa-128">Die Informationen wurden von einem Kontakt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="115fa-128">The information was obtained from a contact.</span></span>  <br/> |
|<span data-ttu-id="115fa-129">Ressource</span><span class="sxs-lookup"><span data-stu-id="115fa-129">Resource</span></span>  <br/> |<span data-ttu-id="115fa-130">Die Informationen wurden aus einer Ressource abgerufen.</span><span class="sxs-lookup"><span data-stu-id="115fa-130">The information was obtained from a resource.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="115fa-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="115fa-131">Remarks</span></span>

<span data-ttu-id="115fa-132">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="115fa-132">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="115fa-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="115fa-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

