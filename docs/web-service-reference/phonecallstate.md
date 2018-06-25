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
description: Das PhoneCallState-Element gibt den aktuellen Status für einen Telefonanruf.
ms.openlocfilehash: 184a7400810711442e565d1ef37094bd63b00914
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830761"
---
# <a name="phonecallstate"></a>PhoneCallState

Das **PhoneCallState** -Element gibt den aktuellen Status für einen Telefonanruf. 
  
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

Die folgende Tabelle enthält die möglichen Werte für das **PhoneCallState** -Element. 
  
**PhoneCallState-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Im Leerlauf  <br/> |Ersten Aufruf Zustand.  <br/> |
|Connecting  <br/> |Das System wird dieses Anrufs einwählen.  <br/> |
|Benachrichtigt  <br/> |Der Anruf wird im Zustand Warnungen (Telefon klingelt).  <br/> |
|Verbunden  <br/> |Der Anruf wird in den Verbindungsstatus.  <br/> |
|Verbindung getrennt  <br/> |Der Anruf wird beendet.  <br/> |
|Eingehend  <br/> |Der Anruf wird eingehende.  <br/> |
|Übertragen von  <br/> |Der Anruf wird an ein anderes Ziel weitergeleitet wird.  <br/> |
|Weiterleitung  <br/> |Der Anruf wird an ein anderes Ziel weitergeleitet wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /ews/ des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

