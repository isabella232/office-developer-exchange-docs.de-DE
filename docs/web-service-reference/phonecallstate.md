---
title: PhoneCallState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PhoneCallState
api_type:
- schema
ms.assetid: ac009eb3-6334-49ce-82be-48fe83577f9c
description: Das PhoneCallState-Element gibt den aktuellen Status für einen Telefonanruf an.
ms.openlocfilehash: 8c0b8357b58826f18f05eb0fedc0865be1623c2b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528302"
---
# <a name="phonecallstate"></a>PhoneCallState

Das **PhoneCallState-Element** gibt den aktuellen Status für einen Telefonanruf an. 
  
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

In der folgenden Tabelle sind die möglichen Werte für das **PhoneCallState-Element** aufgeführt. 
  
**PhoneCallState-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Im leerlauf  <br/> |Anfänglicher Anrufstatus.  <br/> |
|Verbindung wird hergestellt  <br/> |Das System wählt diesen Anruf.  <br/> |
|Alarmiert  <br/> |Der Anruf befindet sich im Warnungszustand (das Telefon klingelt).  <br/> |
|Verbunden  <br/> |Der Anruf befindet sich im verbundenen Zustand.  <br/> |
|Disconnected  <br/> |Der Anruf wird getrennt.  <br/> |
|Eingehende  <br/> |Der Anruf ist eingehend.  <br/> |
|Übertragen  <br/> |Der Anruf wird an ein anderes Ziel weitergeleitet.  <br/> |
|Weiterleitung  <br/> |Der Anruf wird an ein anderes Ziel weitergeleitet.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis /ews/ des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

