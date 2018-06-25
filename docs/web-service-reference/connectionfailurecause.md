---
title: ConnectionFailureCause
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionFailureCause
api_type:
- schema
ms.assetid: d2160c8a-015c-4964-b7f7-93478764a173
description: Das ConnectionFailureCause-Element gibt den Grund für eine Trennung der Verbindung mit einem Anruf.
ms.openlocfilehash: 54b4f5b89efdb42ef82dbef8f1af14a39c0ccc6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757600"
---
# <a name="connectionfailurecause"></a>ConnectionFailureCause

Das **ConnectionFailureCause** -Element gibt den Grund für eine Trennung der Verbindung mit einem Anruf. 
  
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

Die folgende Tabelle enthält die möglichen Werte für das **ConnectionFailureCause** -Element. 
  
**ConnectionFailureCause-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Anrufstatus nicht getrennt ist, oder der Disconnect Grund ist nicht bekannt.  <br/> |
|UserBusy  <br/> |Die gewählte Partei Zeile war ausgelastet.  <br/> |
|NoAnswer  <br/> |Der angerufene hat nicht geantwortet.  <br/> |
|Nicht verfügbar  <br/> |Die Anzahl der angerufenen war nicht verfügbar.  <br/> |
|Andere  <br/> |Catch-All anderen Gründen trennen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

