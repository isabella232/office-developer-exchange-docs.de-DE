---
title: AppointmentState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AppointmentState
api_type:
- schema
ms.assetid: ab3f5d04-ace1-4a15-9107-cefa6c41abc7
description: Das AppointmentState-Element gibt den Status des Termins an.
ms.openlocfilehash: f984bbd5a1319a6051a3394ed04d56deabbb2c5a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544282"
---
# <a name="appointmentstate"></a>AppointmentState

Das **AppointmentState-Element** gibt den Status des Termins an. 
  
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

Dieses Element enthält einen Textwert, der festgelegte Bits darstellt. Dies ist in ganzzahliger Form. Dieses Element ist schreibgeschützt. Sie wird nur in einer Antwort zurückgegeben.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der zurückgegebene ganzzahlige Wert stellt die Bitmaske für den Terminstatus dar. In der folgenden Tabelle werden die einzelnen Bits beschrieben.
  
|**Name**|**Bit**|**Beschreibung**|
|:-----|:-----|:-----|
|Keine  <br/> |0x0000  <br/> |Es wurden keine Flags festgelegt. Dies wird nur für einen Termin verwendet, der keine Teilnehmer enthält.  <br/> |
|Besprechung  <br/> |0x0001  <br/> |Dieser Termin ist eine Besprechung.  <br/> |
|Auszahlung  <br/> |0x0002  <br/> |Dieser Termin wurde empfangen.  <br/> |
|Abgebrochen  <br/> |0x0004  <br/> |Dieser Termin wurde abgebrochen.  <br/> |
   
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

