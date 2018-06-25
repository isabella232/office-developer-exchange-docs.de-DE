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
description: Das UserConfigurationProperties-Element gibt die Eigenschaftentypen in einem Vorgang GetUserConfiguration abgerufen.
ms.openlocfilehash: 4f993765bb7c36f28a41a3f2fa7e28698a3f709e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839440"
---
# <a name="userconfigurationproperties"></a>UserConfigurationProperties

Das **UserConfigurationProperties** -Element gibt die Eigenschaftentypen in einem Vorgang GetUserConfiguration abgerufen. 
  
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
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Gibt eine Anforderung zum Abrufen einer Benutzer-Konfigurationsobjekt.  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für das **UserConfigurationProperties** -Element. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Gibt die ID-Eigenschaft an.  <br/> |
|Dictionary  <br/> |Gibt die Eigenschaftentypen Wörterbuch an.  <br/> |
|XmlData  <br/> |Gibt die Typen von XML-Daten an.  <br/> |
|BinaryData  <br/> |Gibt Binärdaten Eigenschaftentypen.  <br/> |
|Alle  <br/> |Gibt den Bezeichner, Wörterbuch, XML-Daten und Eigenschaftentypen Binärdaten.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

