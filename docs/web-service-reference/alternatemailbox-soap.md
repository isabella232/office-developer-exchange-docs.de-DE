---
title: AlternateMailbox (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: d913a70d-5a85-4b6e-becc-2fb9334b6088
description: Das AlternateMailbox-Element stellt ein alternatives Postfach dar.
ms.openlocfilehash: 3646efef9b63b2af8dbba41a07a86462e18ac1c1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543723"
---
# <a name="alternatemailbox-soap"></a>AlternateMailbox (SOAP)

Das **AlternateMailbox-Element** stellt ein alternatives Postfach dar. 
  
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
|[Typ (SOAP)](type-soap.md) <br/> |Stellt den alternativen Postfachtyp dar.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Stellt den alternativen Anzeigenamen des Postfachs dar.  <br/> |
|[LegacyDN (SOAP)](legacydn-soap.md) <br/> |Stellt den alternativen Veralteten Namen des Postfachs dar.  <br/> |
|[Server (SOAP)](server-soap.md) <br/> |Stellt den alternativen Postfachserver dar.  <br/> |
|[SmtpAddress (SOAP)](smtpaddress-soap.md) <br/> |Stellt die alternative SMTP-Adresse des Postfachs dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AlternateMailboxes (SOAP)](alternatemailboxes-soap.md) <br/> |Stellt eine Auflistung alternativer Postfächer dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md)

