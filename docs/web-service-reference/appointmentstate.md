---
title: AppointmentState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppointmentState
api_type:
- schema
ms.assetid: ab3f5d04-ace1-4a15-9107-cefa6c41abc7
description: Das AppointmentState-Element gibt den Status des Termins.
ms.openlocfilehash: 05e92a3fea10a84518b0680c425011a91bc43d93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757364"
---
# <a name="appointmentstate"></a>AppointmentState

Das **AppointmentState** -Element gibt den Status des Termins. 
  
```XML
<AppointmentState/>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Dieses Element enthält einen Textwert, dass stellt Bits festgelegt. Dies ist Integer-Formular. Dieses Element ist schreibgeschützt. Es wird nur in einer Antwort zurückgegeben werden.
  
## <a name="remarks"></a>Hinweise

Der Ganzzahlwert, der zurückgegeben wird, stellt die Termin Zustand Bitmaske dar. Die folgende Tabelle beschreibt jedes Bit.
  
|**Name**|**Bit**|**Beschreibung**|
|:-----|:-----|:-----|
|Keine  <br/> |0x0000  <br/> |Keine Flags es wurden festgelegt. Dies ist nur für einen Termin verwendet, die nicht Teilnehmer enthalten ist.  <br/> |
|Besprechung  <br/> |0x0001  <br/> |Dieser Termin ist eine Besprechung.  <br/> |
|Auszahlung  <br/> |0x0002  <br/> |Dieser Termin wurde empfangen.  <br/> |
|Abgebrochen  <br/> |0x0004  <br/> |Dieser Termin wurde abgebrochen.  <br/> |
   
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

