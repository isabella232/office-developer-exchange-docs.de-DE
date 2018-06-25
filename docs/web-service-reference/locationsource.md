---
title: LocationSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: Das LocationSource-Element gibt Informationen über den Ursprung des zugeordneten Postadresse, beispielsweise einen Kontakt oder eine Telefonbuch.
ms.openlocfilehash: 7f5cf5fcca0a72287593349fcf5090a74225d012
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830248"
---
# <a name="locationsource"></a><span data-ttu-id="d5009-103">LocationSource</span><span class="sxs-lookup"><span data-stu-id="d5009-103">LocationSource</span></span>

<span data-ttu-id="d5009-104">Das **LocationSource** -Element gibt Informationen über den Ursprung des zugeordneten Postadresse, beispielsweise einen Kontakt oder eine Telefonbuch.</span><span class="sxs-lookup"><span data-stu-id="d5009-104">The **LocationSource** element specifies information about the origin of the associated postal address, for example, a contact or a telephone book.</span></span> 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 <span data-ttu-id="d5009-105">**LocationSourceType**</span><span class="sxs-lookup"><span data-stu-id="d5009-105">**LocationSourceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5009-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d5009-106">Attributes and elements</span></span>

<span data-ttu-id="d5009-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d5009-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5009-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d5009-108">Attributes</span></span>

<span data-ttu-id="d5009-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5009-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5009-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5009-110">Child elements</span></span>

<span data-ttu-id="d5009-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5009-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d5009-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5009-112">Parent elements</span></span>

<span data-ttu-id="d5009-113">[Wert (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span><span class="sxs-lookup"><span data-stu-id="d5009-113">[Value (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d5009-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="d5009-114">Text value</span></span>

<span data-ttu-id="d5009-115">In der folgenden Tabelle sind die Textwerte für das Element **LocationSource** aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d5009-115">The text values for the **LocationSource** element are listed in the following table:</span></span> 
  
<span data-ttu-id="d5009-116">**Text-Elementwerte LocationSource**</span><span class="sxs-lookup"><span data-stu-id="d5009-116">**LocationSource element text values**</span></span>

|<span data-ttu-id="d5009-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d5009-117">**Value**</span></span>|<span data-ttu-id="d5009-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5009-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5009-119">Keine</span><span class="sxs-lookup"><span data-stu-id="d5009-119">None</span></span>  <br/> |<span data-ttu-id="d5009-120">Kein Quell-Speicherort ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d5009-120">There is no location source.</span></span>  <br/> |
|<span data-ttu-id="d5009-121">LocationServices</span><span class="sxs-lookup"><span data-stu-id="d5009-121">LocationServices</span></span>  <br/> |<span data-ttu-id="d5009-122">Die Informationen wurde Diensten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d5009-122">The information was obtained from location services.</span></span>  <br/> |
|<span data-ttu-id="d5009-123">PhonebookServices</span><span class="sxs-lookup"><span data-stu-id="d5009-123">PhonebookServices</span></span>  <br/> |<span data-ttu-id="d5009-124">Die Informationen wurde Telefonbuch Services abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d5009-124">The information was obtained from phonebook services.</span></span>  <br/> |
|<span data-ttu-id="d5009-125">Ger?t</span><span class="sxs-lookup"><span data-stu-id="d5009-125">Device</span></span>  <br/> |<span data-ttu-id="d5009-126">Die Informationen wurde des Geräts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d5009-126">The information was obtained from the device.</span></span>  <br/> |
|<span data-ttu-id="d5009-127">Kontakt</span><span class="sxs-lookup"><span data-stu-id="d5009-127">Contact</span></span>  <br/> |<span data-ttu-id="d5009-128">Die Informationen wurde eines Kontakts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d5009-128">The information was obtained from a contact.</span></span>  <br/> |
|<span data-ttu-id="d5009-129">Ressource</span><span class="sxs-lookup"><span data-stu-id="d5009-129">Resource</span></span>  <br/> |<span data-ttu-id="d5009-130">Die Informationen wurde einer Ressource abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d5009-130">The information was obtained from a resource.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5009-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d5009-131">Remarks</span></span>

<span data-ttu-id="d5009-132">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d5009-132">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d5009-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d5009-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

