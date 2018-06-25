---
title: SharingEffectiveRights (CalendarPermissionReadAccessType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: b519f642-a9ef-4300-92e6-ed8202855fde
description: Das SharingEffectiveRights-Element gibt an, die Berechtigungen, die der Benutzer für die Kalenderdaten verfügt, die gemeinsam genutzt wird.
ms.openlocfilehash: e7d2aa061650c33d27de042ae8a6348f9a7d3430
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831480"
---
# <a name="sharingeffectiverights-calendarpermissionreadaccesstype"></a>SharingEffectiveRights (CalendarPermissionReadAccessType)

Das **SharingEffectiveRights** -Element gibt an, die Berechtigungen, die der Benutzer für die Kalenderdaten verfügt, die gemeinsam genutzt wird. 
  
```XML
<SharingEffectiveRights>None | TimeOnly | TimeAndSubjectAndLocation | FullDetails</SharingEffectiveRights>
```

 **CalendarPermissionReadAccessType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für das **SharingEffectiveRights** -Element. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Gibt an, dass der Benutzer die Berechtigung zum Anzeigen von Elementen im Kalender nicht vorhanden ist.  <br/> |
|TimeOnly  <br/> |Gibt an, dass der Benutzer die Berechtigung zum Anzeigen der nur Frei/Gebucht-Zeit im Kalender hat.  <br/> |
|TimeAndSubjectAndLocation  <br/> |Gibt an, dass der Benutzer über die Berechtigung zum Anzeigen von Frei/Gebucht-Zeit in den Kalender und den Betreff und Ort von Terminen verfügt.  <br/> |
|FullDetails  <br/> |Gibt an, dass der Benutzer die Berechtigung zum Anzeigen aller Elemente im Kalender, einschließlich der Frei/Gebucht-Zeit und Betreff, Ort und Details von Terminen verfügt.  <br/> |
   
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

