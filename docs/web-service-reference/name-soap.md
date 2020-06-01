---
title: Name (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: dce6d823-dc33-4a47-babe-6370a15ac7b4
description: Das Name-Element stellt den Namen einer Einstellung dar.
ms.openlocfilehash: 74e6d6b59d972d7230c23b38cd3f4a8591401bbd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466885"
---
# <a name="name-soap"></a>Name (SOAP)

Das **Name** -Element stellt den Namen einer Einstellung dar. 
  
```XML
<Name/>
```

**Zeichenfolge**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainSetting (SOAP)](domainsetting-soap.md) <br/> |Enthält Domäneneinstellungen, die von der [GetDomainSettings-Vorgangsanforderung (SOAP)](getdomainsettings-operation-soap.md) zurückgegeben werden.  <br/> |
|[DomainStringSetting (SOAP)](domainstringsetting-soap.md) <br/> |Stellt eine Domäneneinstellung dar, deren Wert vom Typ String ist.  <br/> |
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Stellt eine Liste von Organisationsbeziehungen für eine einzelne Organisation dar.  <br/> |
|[UserSetting (SOAP)](usersetting-soap.md) <br/> |Stellt eine Einstellung für einen einzelnen Benutzer dar.  <br/> |
|[ProtocolConnectionCollectionSetting (SOAP)](protocolconnectioncollectionsetting-soap.md) <br/> |Stellt eine Auflistung von Verbindungseinstellungen für das Serverprotokoll dar.  <br/> |
|[StringSetting (SOAP)](stringsetting-soap.md) <br/> |Stellt einen Benutzer dar, der den Wert für den vom Typ String fest legt.  <br/> |
|[WebClientUrlCollectionSetting (SOAP)](webclienturlcollectionsetting-soap.md) <br/> |Stellt eine Benutzereinstellung dar, bei der es sich um eine Sammlung von Exchange-WebClient-URLs handelt.  <br/> |
|[AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md) <br/> |Enthält eine Auflistung von alternativen Postfacheinstellungen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **Name** -Elements ist der Name einer Einstellung. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)
- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)
- [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

