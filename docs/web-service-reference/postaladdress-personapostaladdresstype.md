---
title: PostalAddress (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 075f7d65-9d05-47cb-af26-0dd6d5593439
description: Das PostalAddress-Element gibt die Adresse für eine Rolle.
ms.openlocfilehash: fb418154867aebb4d284e75be579003c0ddc88f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830855"
---
# <a name="postaladdress-personapostaladdresstype"></a><span data-ttu-id="501c8-103">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="501c8-103">PostalAddress (PersonaPostalAddressType)</span></span>

<span data-ttu-id="501c8-104">Das **PostalAddress** -Element gibt die Adresse für eine Rolle.</span><span class="sxs-lookup"><span data-stu-id="501c8-104">The **PostalAddress** element specifies the postal address for a persona.</span></span> 
  
```XML
<PostalAddress>
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
   <PostOfficeBox/>
   <Type/>
   <Latitude/>
   <Longitude/>
   <Accuracy/>
   <Altitude/>
   <AltitudeAccuracy/>
   <FormattedAddress/>
   <LocationUri/>
   <LocationSource/>
</PostalAddress>
```

 <span data-ttu-id="501c8-105">**PersonaPostalAddressType**</span><span class="sxs-lookup"><span data-stu-id="501c8-105">**PersonaPostalAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="501c8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="501c8-106">Attributes and elements</span></span>

<span data-ttu-id="501c8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="501c8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="501c8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="501c8-108">Attributes</span></span>

<span data-ttu-id="501c8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="501c8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="501c8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="501c8-110">Child elements</span></span>

<span data-ttu-id="501c8-111">[Straße](street.md) | [City](city.md) | [Zustand](state-ex15websvcsotherref.md) | [Land](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Typ (String)](type-string.md) | [Breitengrad](latitude.md)  |  [ Längengrad](longitude.md) | [Genauigkeit](accuracy.md) | [Höhe](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span><span class="sxs-lookup"><span data-stu-id="501c8-111">[Street](street.md) | [City](city.md) | [State](state-ex15websvcsotherref.md) | [Country](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Type (string)](type-string.md) | [Latitude](latitude.md) | [Longitude](longitude.md) | [Accuracy](accuracy.md) | [Altitude](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="501c8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="501c8-112">Parent elements</span></span>

[<span data-ttu-id="501c8-113">EnhancedLocation</span><span class="sxs-lookup"><span data-stu-id="501c8-113">EnhancedLocation</span></span>](enhancedlocation.md)
  
## <a name="remarks"></a><span data-ttu-id="501c8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="501c8-114">Remarks</span></span>

<span data-ttu-id="501c8-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="501c8-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="501c8-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="501c8-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="501c8-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="501c8-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="501c8-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="501c8-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="501c8-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="501c8-119">Schema name</span></span>  <br/> |<span data-ttu-id="501c8-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="501c8-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="501c8-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="501c8-121">Validation file</span></span>  <br/> |<span data-ttu-id="501c8-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="501c8-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="501c8-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="501c8-123">Can be empty</span></span>  <br/> ||
   

