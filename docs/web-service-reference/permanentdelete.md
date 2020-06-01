---
title: PermanentDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermanentDelete
api_type:
- schema
ms.assetid: 1a0e0f46-1472-4eb7-bb54-f193a2603587
description: Das PermanentDelete-Element gibt an, ob Nachrichten endgültig gelöscht und nicht im Ordner "Gelöschte Elemente" gespeichert werden sollen.
ms.openlocfilehash: da7680eefca9ad359948af38eac49d18e9055988
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467767"
---
# <a name="permanentdelete"></a>PermanentDelete

Das **PermanentDelete** -Element gibt an, ob Nachrichten endgültig gelöscht und nicht im Ordner "Gelöschte Elemente" gespeichert werden sollen. 
  
```XML
<PermanentDelete>true | false</PermanentDelete>
```

 **Boolescher Wert**
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

Der Textwert **true** gibt an, dass die Nachricht als dauerhaft gelöscht gekennzeichnet werden muss. Der Wert **false** gibt an, dass die Nachricht nicht als dauerhaft gelöscht gekennzeichnet werden darf. 
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

