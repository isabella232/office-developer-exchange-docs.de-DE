---
title: GetServerTimeZones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 2a89098b-d89b-4d01-827b-50be00f7cbe9
description: Das GetServerTimeZones-Element ist das Stammelement in einer Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange-Server.
ms.openlocfilehash: 797e4543c94b0628242bcf544fe9a735ebaa5a63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460939"
---
# <a name="getservertimezones"></a>GetServerTimeZones

Das **GetServerTimeZones** -Element ist das Stammelement in einer Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange-Server. 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 **GetServerTimeZonesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ReturnFullTimeZoneData** <br/> |Gibt an, ob der [GetServerTimeZones-Vorgang](getservertimezones-operation.md) die vollständige Definition oder nur den Namen und den Bezeichner für jede Zeitzone zurückgibt. Dieses Attribut ist optional. Der Standardwert ist **true**.  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a>ReturnFullTimeZoneData-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**true** <br/> |Zurückgeben der vollständigen Definitionen für jede Zeitzone.  <br/> |
|**False** <br/> |Geben Sie nur den Namen und den Bezeichner für jede Zeitzone zurück.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[IDs](ids.md) <br/> |Enthält ein Array von Zeit Zonen Definitions Bezeichnern, die die angeforderten Zeitzonendefinitionen angeben. Dieses Element ist optional. Wenn dieses Element nicht in der GetServerTimeZones- [Vorgangs](getservertimezones-operation.md) Anforderung enthalten ist, werden alle auf dem Server verfügbaren Zeitzonendefinitionen in der Antwort zurückgegeben.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetServerTimeZones-Vorgang](getservertimezones-operation.md)
  
[GetServerTimeZonesResponse](getservertimezonesresponse.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

