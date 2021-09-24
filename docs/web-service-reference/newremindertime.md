---
title: NewReminderTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ff1b6b1c-3557-41d4-8aa6-9528fdb3a21a
description: Das NewReminderTime-Element gibt eine neue Uhrzeit für eine Erinnerung an.
ms.openlocfilehash: 9e6cb75396f35f606bcd974e374f24957ee5d1ec
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515446"
---
# <a name="newremindertime"></a>NewReminderTime

Das **NewReminderTime-Element** gibt eine neue Uhrzeit für eine Erinnerung an. 
  
```XML
<NewReminderTime/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ReminderItemAction](reminderitemaction.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **NewReminderTime-Elements** ist eine neue Uhrzeit für die Erinnerung. Das **NewReminderTime-Element** wird verwendet, wenn das [ActionType-Element](actiontype-reminderactiontype.md) auf **"Erneut erinnern"** festgelegt ist, um die Erinnerung zu verzögern. Der Wert der **NewReminderTime** muss größer als die [ReminderTime](remindertime.md) sein, die vom [GetReminders -Vorgang](getreminders-operation.md)zurückgegeben wird.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ReminderItemAction](reminderitemaction.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

