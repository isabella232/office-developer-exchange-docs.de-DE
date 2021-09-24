---
title: UserConfigurationProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UserConfigurationProperties
api_type:
- schema
ms.assetid: c143a6ec-62ad-4d48-b844-b1ad88054bc1
description: Das UserConfigurationProperties-Element gibt die Eigenschaftstypen an, die in einem GetUserConfiguration-Vorgang abgerufen werden sollen.
ms.openlocfilehash: 0aed3ffc680ac881410469fe762349739ba924a1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515005"
---
# <a name="userconfigurationproperties"></a>UserConfigurationProperties

Das **UserConfigurationProperties-Element** gibt die Eigenschaftstypen an, die in einem GetUserConfiguration-Vorgang abgerufen werden sollen. 
  
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
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Gibt eine Anforderung zum Abrufen eines Benutzerkonfigurationsobjekts an.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **UserConfigurationProperties-Element** aufgeführt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Gibt die Bezeichnereigenschaft an.  <br/> |
|Wörterbuch  <br/> |Gibt Wörterbucheigenschaftentypen an.  <br/> |
|XmlData  <br/> |Gibt XML-Dateneigenschaftentypen an.  <br/> |
|BinaryData  <br/> |Gibt binäre Datentypen an.  <br/> |
|Alle  <br/> |Gibt den Bezeichner, das Wörterbuch, XML-Daten und binäre Datentypen an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

