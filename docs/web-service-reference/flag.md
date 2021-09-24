---
title: Flag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7b47bc74-a60d-4308-8674-5d52444a1753
description: Das Flag-Element gibt ein Flag für ein Postfachelement an.
ms.openlocfilehash: dffc550dc4235c2121b6641f3a6eac30594f75b3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513696"
---
# <a name="flag"></a>Flag

Das **Flag-Element** gibt ein Flag für ein Postfachelement an. 
  
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
|[FlagStatus](flagstatus.md) <br/> |Enthält den aggregierten Flagstatus für Elemente im aktuellen Ordner.  <br/> |
|[StartDate](startdate.md) <br/> |Stellt das Startdatum eines Elements dar.  <br/> |
|[DueDate](duedate.md) <br/> |Stellt das Datum dar, an dem ein Element fällig ist.  <br/> |
|[CompleteDate](completedate.md) <br/> |Stellt das Datum dar, an dem ein Element abgeschlossen wurde.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.  <br/> |
|[Aspekt](item.md) <br/> |Stellt ein generisches Element im Exchange Speicher dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

