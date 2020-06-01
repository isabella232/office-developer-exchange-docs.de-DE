---
title: PostalAddress (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 075f7d65-9d05-47cb-af26-0dd6d5593439
description: Das PostalAddress-Element gibt die Postadresse für eine Rolle an.
ms.openlocfilehash: 9e316e5e0135c2d18fab4067241988c65eceec66
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465387"
---
# <a name="postaladdress-personapostaladdresstype"></a><span data-ttu-id="27475-103">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="27475-103">PostalAddress (PersonaPostalAddressType)</span></span>

<span data-ttu-id="27475-104">Das **PostalAddress** -Element gibt die Postadresse für eine Rolle an.</span><span class="sxs-lookup"><span data-stu-id="27475-104">The **PostalAddress** element specifies the postal address for a persona.</span></span> 
  
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

 <span data-ttu-id="27475-105">**PersonaPostalAddressType**</span><span class="sxs-lookup"><span data-stu-id="27475-105">**PersonaPostalAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27475-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="27475-106">Attributes and elements</span></span>

<span data-ttu-id="27475-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="27475-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27475-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="27475-108">Attributes</span></span>

<span data-ttu-id="27475-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="27475-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27475-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27475-110">Child elements</span></span>

<span data-ttu-id="27475-111">[Straße](street.md)  |  [Stadt](city.md)  |  [Status](state-ex15websvcsotherref.md)  |  [Land](country.md)  |  [PostalCode](postalcode.md)  |  [PostOfficeBox](postofficebox.md)  |  [Typ (Zeichenfolge)](type-string.md)  |  [Latitude](latitude.md)  |  [Länge](longitude.md)  |  [Genauigkeit](accuracy.md)  |  [Höhe](altitude.md)  |  [AltitudeAccuracy](altitudeaccuracy.md)  |  [FormattedAddress](formattedaddress.md)  |  [LocationUri](locationuri.md)  |  [LocationSource](locationsource.md)</span><span class="sxs-lookup"><span data-stu-id="27475-111">[Street](street.md) | [City](city.md) | [State](state-ex15websvcsotherref.md) | [Country](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Type (string)](type-string.md) | [Latitude](latitude.md) | [Longitude](longitude.md) | [Accuracy](accuracy.md) | [Altitude](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="27475-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27475-112">Parent elements</span></span>

[<span data-ttu-id="27475-113">EnhancedLocation</span><span class="sxs-lookup"><span data-stu-id="27475-113">EnhancedLocation</span></span>](enhancedlocation.md)
  
## <a name="remarks"></a><span data-ttu-id="27475-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27475-114">Remarks</span></span>

<span data-ttu-id="27475-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="27475-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="27475-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="27475-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27475-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="27475-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27475-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="27475-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27475-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="27475-119">Schema name</span></span>  <br/> |<span data-ttu-id="27475-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="27475-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="27475-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="27475-121">Validation file</span></span>  <br/> |<span data-ttu-id="27475-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="27475-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="27475-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="27475-123">Can be empty</span></span>  <br/> ||
   

