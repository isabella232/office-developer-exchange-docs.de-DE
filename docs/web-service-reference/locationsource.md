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
# <a name="locationsource"></a>LocationSource

Das **LocationSource** -Element gibt Informationen über den Ursprung des zugeordneten Postadresse, beispielsweise einen Kontakt oder eine Telefonbuch. 
  
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

[Wert (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)
  
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die Textwerte für das Element **LocationSource** aufgeführt: 
  
**Text-Elementwerte LocationSource**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Kein Quell-Speicherort ist vorhanden.  <br/> |
|LocationServices  <br/> |Die Informationen wurde Diensten abgerufen.  <br/> |
|PhonebookServices  <br/> |Die Informationen wurde Telefonbuch Services abgerufen.  <br/> |
|Ger?t  <br/> |Die Informationen wurde des Geräts abgerufen.  <br/> |
|Kontakt  <br/> |Die Informationen wurde eines Kontakts abgerufen.  <br/> |
|Ressource  <br/> |Die Informationen wurde einer Ressource abgerufen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  

