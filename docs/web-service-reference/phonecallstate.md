---
title: PhoneCallState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallState
api_type:
- schema
ms.assetid: ac009eb3-6334-49ce-82be-48fe83577f9c
description: Das PhoneCallState-Element gibt den aktuellen Status für einen Telefonanruf an.
ms.openlocfilehash: d2088b9b2811befe80684188d49c8034c577cc55
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468530"
---
# <a name="phonecallstate"></a>PhoneCallState

Das **PhoneCallState** -Element gibt den aktuellen Status für einen Telefonanruf an. 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 **PhoneCallStateType**
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

In der folgenden Tabelle sind die möglichen Werte für das **PhoneCallState** -Element aufgeführt. 
  
**PhoneCallState-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Leerlauf  <br/> |Anfänglicher Anruf Zustand.  <br/> |
|Verbindung wird hergestellt  <br/> |Das System wählt diesen Anruf aus.  <br/> |
|Alarmiert  <br/> |Der Anruf befindet sich im Warnungsstatus (Telefon klingelt).  <br/> |
|Verbunden  <br/> |Der Anruf befindet sich im Zustand Connected.  <br/> |
|Disconnected  <br/> |Der Anruf wird getrennt.  <br/> |
|Eingehende  <br/> |Der Anruf ist eingehend.  <br/> |
|Transfer  <br/> |Der Anruf wird an ein anderes Ziel übertragen.  <br/> |
|Weiterleitungs  <br/> |Der Anruf wird an ein anderes Ziel weitergeleitet.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis/EWS/"aus des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

