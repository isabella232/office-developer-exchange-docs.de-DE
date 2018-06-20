---
title: DisplayNameFirstLast
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 013c17c9-cb37-4028-9fe6-c3f47441d0f7
description: Das DisplayNameFirstLast-Element gibt den Anzeigenamen der zugeordneten Rolle im Format, Vorname, Nachname.
ms.openlocfilehash: 7a8c269c7e1b03448d176a630fbcae979926bdf4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758056"
---
# <a name="displaynamefirstlast"></a>DisplayNameFirstLast

Das **DisplayNameFirstLast** -Element gibt den Anzeigenamen der zugeordneten Rolle im Format "First Name", "Nachname". 
  
```XML
<DisplayNameFirstLast>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Rolle](persona.md) <br/> |Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert der **DisplayNameFirstLast** -Element ist ein String-Wert, der den Anzeigenamen, mit dem angegebenen Namen zuerst enthält. 
  
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

