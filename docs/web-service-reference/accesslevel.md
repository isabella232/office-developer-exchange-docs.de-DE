---
title: AccessLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 09475586-00fa-4e82-a915-5ca263ab4d1c
description: Das Element AccessLevel gibt die Zugriffsebene für eine onlinebesprechung umwandeln.
ms.openlocfilehash: 1bf0a191fad529b555117e4ff992c352615bc79b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758362"
---
# <a name="accesslevel"></a>AccessLevel

Das Element **AccessLevel** gibt die Zugriffsebene für eine onlinebesprechung umwandeln. 
  
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
|[OnlineMeetingSettings](onlinemeetingsettings.md) <br/> |Gibt die Optionen für onlinebesprechungen.  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die Textwerte für das Element **AccessLevel** . 
  
**Text-Elementwerte AccessLevel**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Jeder  <br/> |Die Zugriffsebene ist für alle geöffnet.  <br/> |
|Interne  <br/> |Die Zugriffsebene ist nur intern.  <br/> |
|Eingeladen  <br/> |Die Zugriffsebene ist nur eingeladene Teilnehmer.  <br/> |
|Gesperrt  <br/> |Die Zugriffsebene ist gesperrt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Dieses Element wurde in Exchange Server 2013 eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

