---
title: ImAddresses (ArrayOfStringAttributedValuesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b95d0a8b-15a6-4711-b014-55698dbd679c
description: Das ImAddresses-Element gibt ein Array von instant Messaging-Adressen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: 6f238e26083366320ba04b187e3e41771cbd14ba
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829863"
---
# <a name="imaddresses-arrayofstringattributedvaluestype"></a>ImAddresses (ArrayOfStringAttributedValuesType)

Das **ImAddresses** -Element gibt ein Array von instant Messaging-Adressen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle. 
  
```XML
<ImAddresses>
    <StringAttributedValue/>
</ImAddresses>
```

 **ArrayOfStringAttributedValuesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StringAttributedValue](stringattributedvalue.md) <br/> |Gibt eine Instanz in ein Array von Attributen, die einer Rolle-Element zugeordnet ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Rolle](persona.md) <br/> |Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.  <br/> |
   
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

