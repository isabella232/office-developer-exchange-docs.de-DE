---
title: IsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsRead
api_type:
- schema
ms.assetid: 161455d5-a870-4c99-b2eb-c759c538f1bc
description: Das IsRead-Element gibt an, ob eine Nachricht gelesen wurde.
ms.openlocfilehash: bfa44eab1831b519aa7b515aaad456683e580299
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830096"
---
# <a name="isread"></a>IsRead

Das **IsRead** -Element gibt an, ob eine Nachricht gelesen wurde. 
  
```XML
<IsRead/>
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
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[PostItem-Objekt](postitem.md) <br/> |Stellt ein Post-Element im Exchange-Speicher. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
|[ConversationAction](conversationaction.md) <br/> |Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** gibt an, dass die Nachricht gelesen wurde. Der Textwert **false** gibt an, dass die Nachricht nicht gelesen wurde. 
  
## <a name="remarks"></a>Hinweise

[IsReadReceiptRequested](isreadreceiptrequested.md) auf **true**festgelegt ist, sendet eine lesebestätigung **IsRead** auf **true** festlegen. Der Empfänger kann lesebestätigungen unterdrücken, durch das Senden von [SuppressReadReceipt](suppressreadreceipt.md) -Response-Objekt vor dem Festlegen der **IsRead** -Eigenschaft. 
  
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

