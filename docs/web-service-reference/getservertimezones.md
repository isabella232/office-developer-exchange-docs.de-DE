---
title: GetServerTimeZones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 2a89098b-d89b-4d01-827b-50be00f7cbe9
description: Das GetServerTimeZones-Element ist das Stammelement in einer Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange Server.
ms.openlocfilehash: b710334e5778f8bc27ba7ac07c6bf9c2e2d3392e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533539"
---
# <a name="getservertimezones"></a>GetServerTimeZones

Das **GetServerTimeZones-Element** ist das Stammelement in einer Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange Server. 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 **GetServerTimeZonesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ReturnFullTimeZoneData** <br/> |Gibt an, ob der [GetServerTimeZones-Vorgang](getservertimezones-operation.md) die vollständige Definition oder nur den Namen und bezeichner für jede Zeitzone zurückgibt. Dieses Attribut ist optional. Der Standardwert ist **true**.  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a>ReturnFullTimeZoneData-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**STIMMT** <br/> |Gibt die vollständigen Definitionen für jede Zeitzone zurück.  <br/> |
|**FALSE** <br/> |Gibt nur den Namen und bezeichner für jede Zeitzone zurück.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Ids](ids.md) <br/> |Enthält ein Array von Zeitzonendefinitionsbezeichnern, die die angeforderten Zeitzonendefinitionen angeben. Dieses Element ist optional. Wenn dieses Element nicht in der [GetServerTimeZones-Vorgangsanforderung](getservertimezones-operation.md) enthalten ist, werden alle auf dem Server verfügbaren Zeitzonendefinitionen in der Antwort zurückgegeben.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetServerTimeZones-Vorgang](getservertimezones-operation.md)
  
[GetServerTimeZonesResponse](getservertimezonesresponse.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

