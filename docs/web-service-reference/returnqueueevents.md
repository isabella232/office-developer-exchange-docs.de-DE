---
title: ReturnQueueEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReturnQueueEvents
api_type:
- schema
ms.assetid: 69d22417-320c-4c6f-9fb4-2020f2480bb2
description: Das ReturnQueueEvents-Element gibt an, dass die Person, die die Aufgabe ausgeführt wird in einer privilegierten Rolle ist.
ms.openlocfilehash: 02f4ca86ffa14117105ec186ae039065cb626670
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831233"
---
# <a name="returnqueueevents"></a>ReturnQueueEvents

Das **ReturnQueueEvents** -Element gibt an, dass die Person, die die Aufgabe ausgeführt wird in einer privilegierten Rolle ist. 
  
```XML
<ReturnQueueEvents>true | false</ReturnQueueEvents>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |Enthält die Anforderung für den [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) zum Abrufen der vollständigen Nachricht Nachverfolgen der Bericht für den angegebenen ID.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich. Der Wert **true** gibt an, dass die Person, die die Aufgabe ausgeführt wird in einer privilegierten Rolle ist; der Wert **false** gibt an, dass die Person, die die Aufgabe ausgeführt wird nicht in einer privilegierten Rolle ist. 
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

