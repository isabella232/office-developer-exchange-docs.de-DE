---
title: UserConfigurationProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationProperties
api_type:
- schema
ms.assetid: c143a6ec-62ad-4d48-b844-b1ad88054bc1
description: Das UserConfigurationProperties-Element gibt die Eigenschaftentypen an, die in einem GetUserConfiguration-Vorgang abgerufen werden sollen.
ms.openlocfilehash: af6bee64516a7410d96ecc7581e8e819f550ddc1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466493"
---
# <a name="userconfigurationproperties"></a>UserConfigurationProperties

Das **UserConfigurationProperties** -Element gibt die Eigenschaftentypen an, die in einem GetUserConfiguration-Vorgang abgerufen werden sollen. 
  
```xml
<UserConfigurationProperties>Id | Dictionary | XmlData | BinaryData | All</UserConfigurationProperties>
```

 **UserConfigurationPropertyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Gibt eine Anforderung zum Abrufen eines Benutzer Konfigurationsobjekts an.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **UserConfigurationProperties** -Element aufgeführt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Gibt die Identifier-Eigenschaft an.  <br/> |
|Wörterbuch  <br/> |Gibt Wörterbucheigenschaften Typen an.  <br/> |
|XMLDATA  <br/> |Gibt XML-Dateneigenschaften Typen an.  <br/> |
|BinaryData  <br/> |Gibt binäre Dateneigenschaften Typen an.  <br/> |
|Alle  <br/> |Gibt die Typenbezeichner, Wörterbuch, XML-Daten und Binärdaten an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

