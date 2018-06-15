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
description: Das AlternateMailbox-Element stellt ein alternative-Postfach.
ms.openlocfilehash: 8eb53e4846ad55916e2c5876606c00c0f2e371ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19757309"
---
# <a name="alternatemailbox-soap"></a>AlternateMailbox (SOAP)

Das **AlternateMailbox** -Element stellt ein alternative-Postfach. 
  
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
|[Typ (SOAP)](type-soap.md) <br/> |Stellt die alternative Postfachtyp.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Stellt den Anzeigenamen alternative Postfach an.  <br/> |
|[LegacyDN (SOAP)](legacydn-soap.md) <br/> |Alternative Postfach legacy-DN darstellt.  <br/> |
|[Server (SOAP)](server-soap.md) <br/> |Stellt den alternative Postfachserver.  <br/> |
|[SmtpAddress (SOAP)](smtpaddress-soap.md) <br/> |Stellt das alternative Postfach SMTP-Adresse dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AlternateMailboxes (SOAP)](alternatemailboxes-soap.md) <br/> |Stellt eine Auflistung von alternativen Postfächern.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md)

