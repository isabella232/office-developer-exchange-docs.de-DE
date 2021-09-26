---
title: AccessLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 09475586-00fa-4e82-a915-5ca263ab4d1c
description: Das AccessLevel-Element gibt die Zugriffsebene für eine Onlinebesprechung an.
ms.openlocfilehash: f1c85579affe7d1142b22a890808bceeb8f82d38
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544416"
---
# <a name="accesslevel"></a>AccessLevel

Das **AccessLevel-Element** gibt die Zugriffsebene für eine Onlinebesprechung an. 
  
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

In der folgenden Tabelle sind die Textwerte für das **AccessLevel-Element** aufgeführt. 
  
**AccessLevel-Elementtextwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Jeder  <br/> |Die Zugriffsebene ist für alle offen.  <br/> |
|Intern  <br/> |Die Zugriffsebene ist nur intern.  <br/> |
|Eingeladen  <br/> |Die Zugriffsebene ist nur eingeladene Teilnehmer.  <br/> |
|Gesperrt  <br/> |Die Zugriffsebene ist gesperrt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

