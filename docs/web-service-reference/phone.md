---
title: Telefon
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9381d8e0-b705-49fd-a822-00fb485bdbab
description: Das Phone-Element gibt eine einzelne Telefonnummer an, die aus einer Extraktion von Kontaktentitäten resultiert.
ms.openlocfilehash: 7b0047eda90f2e2bb94fd7d0b8d317715ac5d2c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459707"
---
# <a name="phone"></a>Telefon

Das **Phone** -Element gibt eine einzelne Telefonnummer an, die aus einer Extraktion von Kontaktentitäten resultiert. 
  
```XML
<Phone>
   <OriginalPhoneString/>
   <PhoneString/>
   <Type/>
</Phone>
```

 **PhoneType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[OriginalPhoneString](originalphonestring.md)  |  [Telefonnummer](phonestring.md)  |  [Typ (Zeichenfolge)](type-string.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[PhoneNumbers (ArrayOfPhonesType)](phonenumbers-arrayofphonestype.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

