---
title: Wert (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: be838fc2-cfcb-4856-b095-a8e5366bb6c6
description: Das Value-Element gibt Informationen an, die einer Postanschrift zugeordnet sind.
ms.openlocfilehash: 2f017cfc513b9c22d65f8437565646506f3be1ab
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517343"
---
# <a name="value-personapostaladdresstype"></a>Wert (PersonaPostalAddressType)

Das **Value-Element** gibt Informationen an, die einer Postanschrift zugeordnet sind. 
  
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

**PersonaPostalAddressType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Straße](street.md)  |  [Ort](city.md)  |  [Status](state-ex15websvcsotherref.md)  |  [Land](country.md)  |  [Postleitzahl](postalcode.md)  |  [PostOfficeBox](postofficebox.md)  |  [Typ (Zeichenfolge)](type-string.md)  |  [Breitengrad](latitude.md)  |  [Längengrad](longitude.md)  |  [Genauigkeit](accuracy.md)  |  [Höhe](altitude.md)  |  [AltitudeAccuracy](altitudeaccuracy.md)  |  [FormattedAddress](formattedaddress.md)  |  [LocationUri](locationuri.md)  |  [LocationSource](locationsource.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[PostalAddressAttributedValue](postaladdressattributedvalue.md)
  
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
   

