---
title: ReminderType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: Das ReminderType-Element gibt den Typ der zurückzugebenden Erinnerungen an.
ms.openlocfilehash: ab10db372efb935b335868f5d212ded84b29e6eb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518001"
---
# <a name="remindertype"></a>ReminderType

Das **ReminderType-Element** gibt den Typ der zurückzugebenden Erinnerungen an. 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetReminders](getreminders.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **ReminderType-Elements** ist der Typ der zurückzugebenden Erinnerungen, entweder **All**, **Current** oder **Old**. **Alles** ist der empfohlene Wert für dieses Element. Weitere Informationen zur Beziehung zwischen dem **ReminderType-Element** und den [BeginTime-](begintime.md) und [EndTime-Elementen](endtime-remindermessagedatatype.md) finden Sie unter [GetReminders-Vorgang.](getreminders-operation.md)
  
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



[GetReminders](getreminders.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

