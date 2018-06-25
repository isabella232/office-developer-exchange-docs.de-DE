---
title: ReceiveCopiesOfMeetingMessages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceiveCopiesOfMeetingMessages
api_type:
- schema
ms.assetid: 65217ca8-6aea-47eb-a989-e6cce25f5f09
description: Das ReceiveCopiesOfMeetingMessages-Element gibt an, ob eine Stellvertretung Kopien der Nachrichten empfängt, die dem Prinzipal adressiert sind. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: e39a5d3255268b418fa956959da5ae0ea062d831
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830967"
---
# <a name="receivecopiesofmeetingmessages"></a>ReceiveCopiesOfMeetingMessages

Das **ReceiveCopiesOfMeetingMessages** -Element gibt an, ob eine Stellvertretung Kopien der Nachrichten empfängt, die dem Prinzipal adressiert sind. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<ReceiveCopiesOfMeetingMessages>true or false</ReceiveCopiesOfMeetingMessages>
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
|[Beauftragte Benutzer](delegateuser.md) <br/> |Identifiziert einen einzelnen Delegaten hinzufügen oder aktualisieren in einem Postfach. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** gibt an, dass eine Stellvertretung eine Kopie des meeting-Nachrichten empfängt. Der Textwert **false** gibt an, dass eine Stellvertretung keine Kopie der Besprechung Nachrichten erhält. 
  
## <a name="remarks"></a>Hinweise

**ReceiveCopiesOfMeetingMessages** auf **false**festgelegt ist, die Stellvertretung kann weiterhin Senden im Auftrag der Prinzipal, aber erhalten keine Fehlermeldungen bezüglich Besprechungen.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AddDelegate-Vorgang](adddelegate-operation.md)
  
[UpdateDelegate-Vorgang](updatedelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Hinzufügen von Stellvertretungen](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

