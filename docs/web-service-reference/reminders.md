---
title: Erinnerungen
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 19294300-ab84-4784-8aa7-3395a08de640
description: Das Reminders-Element gibt die Erinnerungen an, die in der Antwort auf eine GetReminders-Anforderung zurückgegeben werden.
ms.openlocfilehash: 0b760e93bf27f0fdaad9464580fad924367dea32
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513409"
---
# <a name="reminders"></a>Erinnerungen

Das **Reminders-Element** gibt die Erinnerungen an, die in der Antwort auf eine **GetReminders-Anforderung** zurückgegeben werden. 
  
```XML
<Reminders>
   <Reminder></Reminder>
</Reminders>
```

 **ArrayOfRemindersType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Reminder](reminder.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetRemindersResponse](getremindersresponse.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetRemindersResponse](getremindersresponse.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

