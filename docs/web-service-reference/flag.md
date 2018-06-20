---
title: Flag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b47bc74-a60d-4308-8674-5d52444a1753
description: Das Element Flag gibt ein Flag für ein Postfach-Element an.
ms.openlocfilehash: f30f435e8f064d7165ae52de737bbd75b0546206
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758491"
---
# <a name="flag"></a>Flag

Das Element **Flag** gibt ein Flag für ein Postfach-Element an. 
  
```XML
<Flag>
    <FlagStatus/>
    <StartDate/>
    <DueDate/>
    <CompleteDate/>
</Flag>
```

 **FlagType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FlagStatus](flagstatus.md) <br/> |Enthält den aggregierten Kennzeichnungsstatus für Elemente im aktuellen Ordner.  <br/> |
|[StartDate](startdate.md) <br/> |Den Anfangstermin eines Elements darstellt.  <br/> |
|[DueDate](duedate.md) <br/> |Stellt das Datum an, wann ein Element fällig ist.  <br/> |
|["CompleteDate" darf](completedate.md) <br/> |Stellt das Datum, an dem ein Element abgeschlossen wurde.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.  <br/> |
|[Element](item.md) <br/> |Stellt ein generisches Element im Exchange-Speicher.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

