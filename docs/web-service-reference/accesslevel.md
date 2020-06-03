---
title: Access Level
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 09475586-00fa-4e82-a915-5ca263ab4d1c
description: Das Access Level-Element gibt die Zugriffsebene für eine Onlinebesprechung an.
ms.openlocfilehash: 3c1375ef37ea666c6c4fafce7daa46ae0d0a2696
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462339"
---
# <a name="accesslevel"></a>Access Level

Das **Access Level** -Element gibt die Zugriffsebene für eine Onlinebesprechung an. 
  
```XML
<AccessLevel/>
```

 **OnlineMeetingSettingsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OnlineMeetingSettings](onlinemeetingsettings.md) <br/> |Gibt die Einstellungen für Onlinebesprechungen an.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die Text Werte für das **Access Level** -Element aufgeführt. 
  
**Access Level-Element Text Werte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Alle  <br/> |Die Zugriffsebene ist für alle geöffnet.  <br/> |
|Intern  <br/> |Die Zugriffsebene ist nur intern.  <br/> |
|Eingeladen  <br/> |Die Zugriffsebene wird nur von Teilnehmern eingeladen.  <br/> |
|Gesperrt  <br/> |Die Zugriffsebene ist gesperrt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Dieses Element wurde in Exchange Server 2013 eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

