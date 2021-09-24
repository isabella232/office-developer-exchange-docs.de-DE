---
title: YearlyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- YearlyRegeneration
api_type:
- schema
ms.assetid: 23538bca-738e-4319-944e-f459ff8a7eba
description: Das YearlyRegeneration-Element beschreibt die Häufigkeit in Jahren, in der eine Aufgabe neu generiert wird.
ms.openlocfilehash: f38460eab5ff53a033d99835f23a128e9dc00d19
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522383"
---
# <a name="yearlyregeneration"></a>YearlyRegeneration

Das **YearlyRegeneration-Element** beschreibt die Häufigkeit in Jahren, in der eine Aufgabe neu generiert wird. 
  
```xml
<YearlyRegeneratingPatternType>
   <Interval/>
</YearlyRegeneratingPatternType>
```

**YearlyRegeneratingPatternType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Intervall](interval.md) <br/> |Definiert das Intervall in Jahren, in dem ein neuer Vorgang nach Abschluss der Aufgabe neu generiert wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Serie (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Enthält Serieninformationen für wiederkehrende Vorgänge.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

