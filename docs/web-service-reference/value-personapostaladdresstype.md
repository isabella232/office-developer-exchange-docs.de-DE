---
title: Wert (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be838fc2-cfcb-4856-b095-a8e5366bb6c6
description: Das Value-Element gibt eine Postadresse Informationen zugeordnet.
ms.openlocfilehash: 048d3a49552f1a9e89744e4cd16ec1745417e923
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839486"
---
# <a name="value-personapostaladdresstype"></a><span data-ttu-id="a8c91-103">Wert (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="a8c91-103">Value (PersonaPostalAddressType)</span></span>

<span data-ttu-id="a8c91-104">Das **Value** -Element gibt die Informationen im Zusammenhang mit eine Postadresse an.</span><span class="sxs-lookup"><span data-stu-id="a8c91-104">The **Value** element specifies information associated with a postal address.</span></span> 
  
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

<span data-ttu-id="a8c91-105">**PersonaPostalAddressType**</span><span class="sxs-lookup"><span data-stu-id="a8c91-105">**PersonaPostalAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a8c91-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a8c91-106">Attributes and elements</span></span>

<span data-ttu-id="a8c91-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a8c91-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8c91-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a8c91-108">Attributes</span></span>

<span data-ttu-id="a8c91-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8c91-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8c91-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8c91-110">Child elements</span></span>

<span data-ttu-id="a8c91-111">[Straße](street.md) | [City](city.md) | [Zustand](state-ex15websvcsotherref.md) | [Land](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Typ (String)](type-string.md) | [Breitengrad](latitude.md)  |  [ Längengrad](longitude.md) | [Genauigkeit](accuracy.md) | [Höhe](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span><span class="sxs-lookup"><span data-stu-id="a8c91-111">[Street](street.md) | [City](city.md) | [State](state-ex15websvcsotherref.md) | [Country](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Type (string)](type-string.md) | [Latitude](latitude.md) | [Longitude](longitude.md) | [Accuracy](accuracy.md) | [Altitude](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a8c91-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8c91-112">Parent elements</span></span>

[<span data-ttu-id="a8c91-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="a8c91-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md)
  
## <a name="remarks"></a><span data-ttu-id="a8c91-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8c91-114">Remarks</span></span>

<span data-ttu-id="a8c91-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a8c91-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a8c91-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a8c91-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8c91-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a8c91-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8c91-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8c91-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a8c91-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a8c91-119">Schema name</span></span>  <br/> |<span data-ttu-id="a8c91-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a8c91-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="a8c91-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a8c91-121">Validation file</span></span>  <br/> |<span data-ttu-id="a8c91-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a8c91-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a8c91-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a8c91-123">Can be empty</span></span>  <br/> ||
   

