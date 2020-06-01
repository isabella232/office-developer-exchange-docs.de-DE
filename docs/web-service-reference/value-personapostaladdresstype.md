---
title: Wert (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be838fc2-cfcb-4856-b095-a8e5366bb6c6
description: Das Value-Element gibt Informationen an, die einer Postadresse zugeordnet sind.
ms.openlocfilehash: 2d644ff45fe89061ccd90279773f3a5a5b7fe7cc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466472"
---
# <a name="value-personapostaladdresstype"></a><span data-ttu-id="7a672-103">Wert (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="7a672-103">Value (PersonaPostalAddressType)</span></span>

<span data-ttu-id="7a672-104">Das **value** -Element gibt Informationen an, die einer Postadresse zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7a672-104">The **Value** element specifies information associated with a postal address.</span></span> 
  
```XML
<Value>
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
</Value>
```

<span data-ttu-id="7a672-105">**PersonaPostalAddressType**</span><span class="sxs-lookup"><span data-stu-id="7a672-105">**PersonaPostalAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7a672-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7a672-106">Attributes and elements</span></span>

<span data-ttu-id="7a672-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7a672-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a672-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a672-108">Attributes</span></span>

<span data-ttu-id="7a672-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a672-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a672-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a672-110">Child elements</span></span>

<span data-ttu-id="7a672-111">[Straße](street.md)  |  [Stadt](city.md)  |  [Status](state-ex15websvcsotherref.md)  |  [Land](country.md)  |  [PostalCode](postalcode.md)  |  [PostOfficeBox](postofficebox.md)  |  [Typ (Zeichenfolge)](type-string.md)  |  [Latitude](latitude.md)  |  [Länge](longitude.md)  |  [Genauigkeit](accuracy.md)  |  [Höhe](altitude.md)  |  [AltitudeAccuracy](altitudeaccuracy.md)  |  [FormattedAddress](formattedaddress.md)  |  [LocationUri](locationuri.md)  |  [LocationSource](locationsource.md)</span><span class="sxs-lookup"><span data-stu-id="7a672-111">[Street](street.md) | [City](city.md) | [State](state-ex15websvcsotherref.md) | [Country](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Type (string)](type-string.md) | [Latitude](latitude.md) | [Longitude](longitude.md) | [Accuracy](accuracy.md) | [Altitude](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7a672-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a672-112">Parent elements</span></span>

[<span data-ttu-id="7a672-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="7a672-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md)
  
## <a name="remarks"></a><span data-ttu-id="7a672-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a672-114">Remarks</span></span>

<span data-ttu-id="7a672-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7a672-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7a672-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7a672-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a672-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7a672-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a672-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a672-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a672-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7a672-119">Schema name</span></span>  <br/> |<span data-ttu-id="7a672-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7a672-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="7a672-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7a672-121">Validation file</span></span>  <br/> |<span data-ttu-id="7a672-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7a672-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a672-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7a672-123">Can be empty</span></span>  <br/> ||
   

