---
title: Erinnerungen
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 19294300-ab84-4784-8aa7-3395a08de640
description: Das Reminders-Element gibt die Erinnerungen in der Antwort auf eine Anforderung GetReminders zurückgegeben.
ms.openlocfilehash: 955fc568dc919d591076271382a8c9bbd1d146ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831071"
---
# <a name="reminders"></a>Erinnerungen

Das **Reminders** -Element gibt die Erinnerungen in der Antwort auf eine Anforderung **GetReminders** zurückgegeben. 
  
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
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetRemindersResponse](getremindersresponse.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

