---
title: Hobbys
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f771b066-e42e-4880-bf18-709ad033d2af
description: Das Hobbies-Element gibt ein Array von Hobbies und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.
ms.openlocfilehash: c76f4fc0463928814c61b8d1fb63e4255d6be63d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460953"
---
# <a name="hobbies"></a>Hobbys

Das **Hobbies** -Element gibt ein Array von Hobbies und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an. 
  
```XML
<Hobbies>
    <StringAttributedValue/>
</Hobbies>
```

 **ArrayOfStringAttributedValuesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StringAttributedValue](stringattributedvalue.md) <br/> |Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Persona](persona.md) <br/> |Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

