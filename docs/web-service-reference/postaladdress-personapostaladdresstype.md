---
title: PostalAddress (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 075f7d65-9d05-47cb-af26-0dd6d5593439
description: Das PostalAddress-Element gibt die Postanschrift für eine Persona an.
ms.openlocfilehash: 4e95a94c5a7ce917a0a4b9abf7b7ef120301ae6c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523902"
---
# <a name="postaladdress-personapostaladdresstype"></a>PostalAddress (PersonaPostalAddressType)

Das **PostalAddress-Element** gibt die Postanschrift für eine Persona an. 
  
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

 **PersonaPostalAddressType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Straße](street.md)  |  [Ort](city.md)  |  [Status](state-ex15websvcsotherref.md)  |  [Land](country.md)  |  [Postleitzahl](postalcode.md)  |  [PostOfficeBox](postofficebox.md)  |  [Typ (Zeichenfolge)](type-string.md)  |  [Breitengrad](latitude.md)  |  [Längengrad](longitude.md)  |  [Genauigkeit](accuracy.md)  |  [Höhe](altitude.md)  |  [AltitudeAccuracy](altitudeaccuracy.md)  |  [FormattedAddress](formattedaddress.md)  |  [LocationUri](locationuri.md)  |  [LocationSource](locationsource.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[EnhancedLocation](enhancedlocation.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

