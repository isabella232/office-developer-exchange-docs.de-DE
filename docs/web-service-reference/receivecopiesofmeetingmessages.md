---
title: ReceiveCopiesOfMeetingMessages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ReceiveCopiesOfMeetingMessages
api_type:
- schema
ms.assetid: 65217ca8-6aea-47eb-a989-e6cce25f5f09
description: Das ReceiveCopiesOfMeetingMessages-Element gibt an, ob ein Stellvertreter Kopien von Besprechungsnachrichten empfängt, die an den Prinzipal adressiert sind. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 0ce5d15fbe5111bf319cfaf3dd7ed520c24ea77b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512555"
---
# <a name="receivecopiesofmeetingmessages"></a>ReceiveCopiesOfMeetingMessages

Das **ReceiveCopiesOfMeetingMessages-Element** gibt an, ob ein Stellvertreter Kopien von Besprechungsnachrichten empfängt, die an den Prinzipal adressiert sind. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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
|[DelegateUser](delegateuser.md) <br/> |Identifiziert einen einzelnen Delegaten, der in einem Postfach hinzugefügt oder aktualisiert werden soll. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **"true"** gibt an, dass ein Stellvertreter eine Kopie von Besprechungsnachrichten empfängt. Der Textwert **"false"** gibt an, dass eine Stellvertretung keine Kopie von Besprechungsnachrichten empfängt. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn **ReceiveCopiesOfMeetingMessages** auf **"false"** festgelegt ist, kann der Delegat weiterhin nachrichten im Namen des Prinzipals senden, empfängt jedoch keine Besprechungsnachrichten.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AddDelegate-Vorgang](adddelegate-operation.md)
  
[UpdateDelegate-Vorgang](updatedelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Hinzufügen von Delegaten](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

