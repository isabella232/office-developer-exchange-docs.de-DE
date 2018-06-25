---
title: FlaggedForAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FlaggedForAction
api_type:
- schema
ms.assetid: 6a08c48a-7b32-4754-8940-adbda55e8133
description: Das FlaggedForAction-Element gibt die Kennzeichen für den Aktionswert, die angezeigt werden, muss auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anwenden.
ms.openlocfilehash: 5b6e714512edcf12ded2c04f414d047b8622d305
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758497"
---
# <a name="flaggedforaction"></a>FlaggedForAction

Das **FlaggedForAction** -Element gibt die Kennzeichen für den Aktionswert, die angezeigt werden, muss auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anwenden. 
  
```XML
<FlaggedForAction/>
```

 **FlaggedForActionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bedingungen](conditions.md) <br/> |Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.  <br/> |
|[Ausnahmen](exceptions.md) <br/> |Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Es folgen die möglichen Textwerte für dieses Element:
  
- Jede
    
- Aufruf
    
- DoNotForward
    
- Nachverfolgung
    
- FYI
    
- Forward
    
- NoResponseNecessary
    
- Lesen
    
- Antworten
    
- ReplyToAll
    
- Überprüfung
    
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

