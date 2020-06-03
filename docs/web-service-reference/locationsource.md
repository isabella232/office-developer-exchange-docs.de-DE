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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467102"
---
# <a name="locationsource"></a>LocationSource

Das **LocationSource** -Element gibt Informationen über den Ursprung der zugeordneten Postadresse an, beispielsweise einen Kontakt oder ein Telefonbuch. 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 **LocationSourceType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Wert (PersonaPostalAddressType)](value-personapostaladdresstype.md)  |  [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)
  
## <a name="text-value"></a>Textwert

Die Textwerte für das **LocationSource** -Element sind in der folgenden Tabelle aufgeführt: 
  
**LocationSource-Element Text Werte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Es gibt keine Standort Quelle.  <br/> |
|LocationServices  <br/> |Die Informationen wurden von den Standortdiensten abgerufen.  <br/> |
|PhonebookServices  <br/> |Die Informationen wurden in Telefonbuch Diensten abgerufen.  <br/> |
|Gerät  <br/> |Die Informationen wurden vom Gerät abgerufen.  <br/> |
|Kontakt  <br/> |Die Informationen wurden von einem Kontakt abgerufen.  <br/> |
|Ressource  <br/> |Die Informationen wurden aus einer Ressource abgerufen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  

