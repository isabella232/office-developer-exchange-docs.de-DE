---
title: LocationSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: Das LocationSource-Element gibt Informationen über den Ursprung der zugeordneten Postadresse an, z. B. einen Kontakt oder ein Telefonbuch.
ms.openlocfilehash: f3569494d3e662fbc46060944c8bd399b62d656b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543261"
---
# <a name="locationsource"></a>LocationSource

Das **LocationSource-Element** gibt Informationen über den Ursprung der zugeordneten Postadresse an, z. B. einen Kontakt oder ein Telefonbuch. 
  
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

Die Textwerte für das **LocationSource-Element** sind in der folgenden Tabelle aufgeführt: 
  
**Textwerte des LocationSource-Elements**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Es gibt keine Standortquelle.  <br/> |
|LocationServices  <br/> |Die Informationen wurden von Standortdiensten abgerufen.  <br/> |
|PhonebookServices  <br/> |Die Informationen wurden von Telefonbuchdiensten abgerufen.  <br/> |
|Gerät  <br/> |Die Informationen wurden vom Gerät abgerufen.  <br/> |
|Kontakt  <br/> |Die Informationen wurden von einem Kontakt abgerufen.  <br/> |
|Ressource  <br/> |Die Informationen wurden aus einer Ressource abgerufen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  

