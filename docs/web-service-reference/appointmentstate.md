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
description: Das AppointmentState-Element gibt den Status des Termins an.
ms.openlocfilehash: 8b0e827d02e9051f31d43199503dc286c50e2125
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463475"
---
# <a name="appointmentstate"></a>AppointmentState

Das **AppointmentState** -Element gibt den Status des Termins an. 
  
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

Dieses Element enthält einen Textwert, der festgelegte Bits darstellt. Dies ist eine ganzzahlige Form. Dieses Element ist schreibgeschützt. Sie wird nur in einer Antwort zurückgegeben.
  
## <a name="remarks"></a>Bemerkungen

Der zurückgegebene ganzzahlige Wert stellt die Bitmaske des Terminstatus dar. In der folgenden Tabelle werden die einzelnen Bit beschrieben.
  
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

