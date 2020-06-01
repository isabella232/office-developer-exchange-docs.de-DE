---
title: AlternateMailbox (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d913a70d-5a85-4b6e-becc-2fb9334b6088
description: Das AlternateMailbox-Element stellt ein alternatives Postfach dar.
ms.openlocfilehash: 9019f85a373cc186cc9dadddceee3dc9d11b3854
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466157"
---
# <a name="alternatemailbox-soap"></a>AlternateMailbox (SOAP)

Das **AlternateMailbox** -Element stellt ein alternatives Postfach dar. 
  
```XML
<AlternateMailbox>
   <Type/>
   <DisplayName/>
   <LegacyDN/>
   <Server/>
   <SmtpAddress/>
</AlternateMailbox>
```

 **AlternateMailbox**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Type (SOAP)](type-soap.md) <br/> |Stellt den alternativen Postfachtyp dar.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Stellt den Anzeigenamen des alternativen Postfachs dar.  <br/> |
|[LegacyDN (SOAP)](legacydn-soap.md) <br/> |Stellt den Distinguished Name des alternativen Post Fach Legacy dar.  <br/> |
|[Server (SOAP)](server-soap.md) <br/> |Stellt den alternativen Postfachserver dar.  <br/> |
|[SmtpAddress (SOAP)](smtpaddress-soap.md) <br/> |Stellt die Alternative Post Fach SMTP-Adresse dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AlternateMailboxes (SOAP)](alternatemailboxes-soap.md) <br/> |Stellt eine Auflistung von alternativen Postfächern dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md)

