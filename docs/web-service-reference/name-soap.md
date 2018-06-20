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
description: Das Name-Element gibt den Namen einer Einstellung.
ms.openlocfilehash: 4689c306bb805a40fea0d58c9e04a5a47d3bb14d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830506"
---
# <a name="name-soap"></a>Name (SOAP)

Das **Name** -Element gibt den Namen einer Einstellung. 
  
```XML
<Name/>
```

**string**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainSetting (SOAP)](domainsetting-soap.md) <br/> |Enthält domäneneinstellungen für die, die von der Anforderung [(SOAP) GetDomainSettings-Vorgang](getdomainsettings-operation-soap.md) zurückgegeben werden.  <br/> |
|[DomainStringSetting (SOAP)](domainstringsetting-soap.md) <br/> |Stellt eine Einstellung für dessen, die Wert vom Typ String ist.  <br/> |
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation.  <br/> |
|[UserSetting (SOAP)](usersetting-soap.md) <br/> |Stellt eine Einstellung für die einzelnen Benutzer dar.  <br/> |
|[ProtocolConnectionCollectionSetting (SOAP)](protocolconnectioncollectionsetting-soap.md) <br/> |Stellt eine Auflistung von Einstellungen für die Server Protocol-Verbindung dar.  <br/> |
|[StringSetting (SOAP)](stringsetting-soap.md) <br/> |Stellt eine benutzereinstellung für der, die Wert für die vom Typ String ist.  <br/> |
|[WebClientUrlCollectionSetting (SOAP)](webclienturlcollectionsetting-soap.md) <br/> |Repräsentiert einen Benutzer festlegen, d. h. eine Auflistung von Exchange Web-Client-URLs.  <br/> |
|[AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md) <br/> |Enthält eine Auflistung von postfacheinstellungen für alternative an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert der **Name** -Elements ist der Name einer Einstellung. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)
- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)
- [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

