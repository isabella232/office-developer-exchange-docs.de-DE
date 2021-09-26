---
title: StartDate (Serie)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StartDate
api_type:
- schema
ms.assetid: bd65ac06-b3ac-4c9b-9568-3e4dc94378e7
description: Das StartDate-Element stellt den Anfangstermin einer Terminserie oder eines Kalenderelements dar.
ms.openlocfilehash: 50f83e5c97d346cc3f7dfced1ee71aa3f9f38ed5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545867"
---
# <a name="startdate-recurrence"></a>StartDate (Serie)

Das **StartDate-Element** stellt den Anfangstermin einer Terminserie oder eines Kalenderelements dar. 
  
```xml
<StartDate/>
```

**Date**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EndDateRecurrence](enddaterecurrence.md) <br/> |Beschreibt das Startdatum und das Enddatum eines Elementserienmusters.  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |Beschreibt das Startdatum eines Elementserienmusters, das kein definiertes Enddatum hat.  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |Beschreibt das Startdatum und die Anzahl der Vorkommen einer Terminserie.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der ein Datum darstellt, ist erforderlich, wenn dieses Element verwendet wird. Der Wert darf nicht kleiner als 1. Apr. 1601 00:00:00 sein.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

