---
title: ConnectionFailureCause
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConnectionFailureCause
api_type:
- schema
ms.assetid: d2160c8a-015c-4964-b7f7-93478764a173
description: Das ConnectionFailureCause-Element gibt den Grund für eine Trennung von einem Telefonanruf an.
ms.openlocfilehash: de2f06ae89577b0141b8555f98dba1671a228d45
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543534"
---
# <a name="connectionfailurecause"></a>ConnectionFailureCause

Das **ConnectionFailureCause-Element** gibt den Grund für eine Trennung von einem Telefonanruf an. 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 **ConnectionFailureCauseType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PhoneCallInformation](phonecallinformation.md) <br/> |Gibt die Statusinformationen für einen Telefonanruf an.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **ConnectionFailureCause-Element** aufgeführt. 
  
**ConnectionFailureCause-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Der Anrufstatus wird nicht getrennt, oder der Grund für die Verbindung ist nicht bekannt.  <br/> |
|UserBusy  <br/> |Die angerufene Partyzeile war ausgelastet.  <br/> |
|NoAnswer  <br/> |Die angerufene Partei hat nicht reagiert.  <br/> |
|Verfügbar  <br/> |Die nummer der angerufenen Partei war nicht verfügbar.  <br/> |
|Sonstiges  <br/> |Catch-all for other disconnect reasons.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

