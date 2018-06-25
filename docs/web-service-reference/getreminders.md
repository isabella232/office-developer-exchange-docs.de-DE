---
title: GetReminders
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 943c3d5d-7d29-4d70-932c-8a4fe44a0037
description: Das GetReminders-Element gibt eine Anforderung an eine Erinnerung erhalten möchten.
ms.openlocfilehash: f4ecc858af2150bb3f88ebdf9ed541892f2fead1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758782"
---
# <a name="getreminders"></a>GetReminders

Das **GetReminders** -Element gibt eine Anforderung an eine Erinnerung erhalten möchten. 
  
```XML
<GetReminders>
   <BeginTime/>
   <EndTime/>
   <MaxItems/>
   <ReminderType/>
</GetReminders>

```

 **GetRemindersType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[BeginTime](begintime.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [MaxItems wird](maxitems.md) | [ReminderType](remindertype.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

