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
description: Das GetServerTimeZones-Element ist das Stammelement im eine Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange-Server.
ms.openlocfilehash: 1ad503ff312497189f57bce9a3670571aedad5ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758804"
---
# <a name="getservertimezones"></a>GetServerTimeZones

Das **GetServerTimeZones** -Element ist das Stammelement im eine Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange-Server. 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 **GetServerTimeZonesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ReturnFullTimeZoneData** <br/> |Gibt an, ob der [Vorgang GetServerTimeZones](getservertimezones-operation.md) die vollständige Definition oder nur die Namen und Bezeichner für jede Zeitzone zurückgegeben. Dieses Attribut ist optional. Der Standardwert ist **true**.  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a>ReturnFullTimeZoneData-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**"true"** <br/> |Die vollständigen Definitionen für jede Zeitzone zurückzugeben.  <br/> |
|**false** <br/> |Zurückgeben Sie nur den Namen und Bezeichner für jede Zeitzone.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[IDs](ids.md) <br/> |Enthält ein Array der Zeitzone Definition Bezeichner, der die angeforderte Zeitzonendefinitionen angibt. Dieses Element ist optional. Wenn dieses Element nicht in der Anforderung [GetServerTimeZones Vorgang](getservertimezones-operation.md) enthalten ist, werden alle Zeitzonendefinitionen auf dem Server zur Verfügung stehen in der Antwort zurückgegeben.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetServerTimeZones-Vorgang](getservertimezones-operation.md)
  
[GetServerTimeZonesResponse](getservertimezonesresponse.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

