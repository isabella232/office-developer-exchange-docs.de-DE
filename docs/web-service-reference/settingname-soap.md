---
title: SettingName (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8bcb0411-58b0-4e37-b97e-00c07dcbecb1
description: Das SettingName-Element gibt den Namen einer Einstellung in der Antwort.
ms.openlocfilehash: 9bf7c8197693bc6887a99ffcbeb2240e1f4c3b20
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831468"
---
# <a name="settingname-soap"></a>SettingName (SOAP)

Das **SettingName** -Element gibt den Namen einer Einstellung in der Antwort. 
  
```XML
<SettingName/>
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
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Stellt einen Fehler, der beim Abrufen einer benutzereinstellung zurückgegeben wird.  <br/> |
|[DomainSettingError (SOAP)](domainsettingerror-soap.md) <br/> |Stellt einen Fehler, die beim Abrufen einer domäneneinstellung dar. Dies stellt einen Fehler aus einer Anforderung **GetDomainSettings** dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert des Elements **SettingName** stellt den Namen einer Einstellung in einer Antwort. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

