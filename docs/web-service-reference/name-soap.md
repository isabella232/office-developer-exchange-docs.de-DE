---
title: Name (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: dce6d823-dc33-4a47-babe-6370a15ac7b4
description: Das Name-Element stellt den Namen einer Einstellung dar.
ms.openlocfilehash: 39bb2b6bbf7e29dedb13a9bf828f130c076dfb6b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541994"
---
# <a name="name-soap"></a>Name (SOAP)

Das **Name-Element** stellt den Namen einer Einstellung dar. 
  
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
|[DomainSetting (SOAP)](domainsetting-soap.md) <br/> |Enthält Domäneneinstellungen, die von der [SOAP-Anforderung (GetDomainSettings-Vorgang)](getdomainsettings-operation-soap.md) zurückgegeben werden.  <br/> |
|[DomainStringSetting (SOAP)](domainstringsetting-soap.md) <br/> |Stellt eine Domäne dar, deren Wert vom Typ String ist.  <br/> |
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Stellt eine Liste der Organisationsbeziehungen für eine einzelne Organisation dar.  <br/> |
|[UserSetting (SOAP)](usersetting-soap.md) <br/> |Stellt eine einzelne Benutzereinstellung dar.  <br/> |
|[ProtocolConnectionCollectionSetting (SOAP)](protocolconnectioncollectionsetting-soap.md) <br/> |Stellt eine Auflistung von Serverprotokollverbindungseinstellungen dar.  <br/> |
|[StringSetting (SOAP)](stringsetting-soap.md) <br/> |Stellt einen Benutzer dar, der den Wert vom Typ String festlegt.  <br/> |
|[WebClientUrlCollectionSetting (SOAP)](webclienturlcollectionsetting-soap.md) <br/> |Stellt eine Benutzereinstellung dar, bei der es sich um eine Auflistung Exchange Webclient-URLs handelt.  <br/> |
|[AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md) <br/> |Enthält eine Auflistung alternativer Postfacheinstellungen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **Name-Elements** ist der Name einer Einstellung. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)
- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)
- [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

