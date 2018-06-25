---
title: MarkAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MarkAsRead
api_type:
- schema
ms.assetid: 404842e1-fbdb-480d-a1d8-ba1ab2c9fb1e
description: Das MarkAsRead-Element gibt an, ob Nachrichten sind, als gelesen markiert werden soll.
ms.openlocfilehash: b453ad73912e99b6fd3aed84b03a7d2fc2b6a294
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830355"
---
# <a name="markasread"></a>MarkAsRead

Das **MarkAsRead** -Element gibt an, ob Nachrichten sind, als gelesen markiert werden soll. 
  
```XML
<MarkAsRead>true | false</MarkAsRead>
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
|[Aktionen](actions.md) <br/> |Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** gibt an, dass die Nachricht als gelesen markiert werden muss. Der Wert **false** gibt an, dass Nachrichten nicht als gelesen markiert werden müssen. 
  
## <a name="remarks"></a>Hinweise

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

