---
title: EndDateTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EndDateTime
api_type:
- schema
ms.assetid: 54d14e47-a8f7-400b-a859-c7ea7ce4c6a4
description: Das EndDateTime-Element gibt das Enddatum und die Endzeit für eine Regel oder eine Suche an.
ms.openlocfilehash: 19f2e64e37323f90f5c576acd5551675105f3bd3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517091"
---
# <a name="enddatetime"></a>EndDateTime

Das **EndDateTime-Element** gibt das Enddatum und die Endzeit für eine Regel oder eine Suche an. 
  
```XML
<EndDateTime/>
```

 **dateTime**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Enthält die Kriterien für die Typen von Nachrichten suchen.  <br/> |
|[WithinDateRange](withindaterange.md) <br/> |Gibt den Datumsbereich an, in dem eingehende Nachrichten empfangen werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
   
## <a name="text-value"></a>Textwert

Wenn dieses Element verwendet wird, ist ein Textwert erforderlich, der ein Datum/eine Uhrzeit darstellt.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

