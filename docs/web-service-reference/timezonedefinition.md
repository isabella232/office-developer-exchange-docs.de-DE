---
title: TimeZoneDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneDefinition
api_type:
- schema
ms.assetid: b005a80c-addb-4409-beff-e5162076752c
description: Das TimeZoneDefinition-Element gibt die Punkte und Übergänge an, die eine Zeitzone definieren.
ms.openlocfilehash: 58d34556686bfc77244b5829798eada51a1df843
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466066"
---
# <a name="timezonedefinition"></a>TimeZoneDefinition

Das **TimeZoneDefinition** -Element gibt die Punkte und Übergänge an, die eine Zeitzone definieren. 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 **TimeZoneDefinitionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Stellt den eindeutigen Bezeichner der Zeitzone dar.  <br/> |
|Name  <br/> |Stellt den beschreibenden Namen der Zeitzone dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Zeiten](periods.md) <br/> |Stellt ein Array von [Period](period.md) -Elementen dar, die den Zeit Offset in unterschiedlichen Phasen der Zeitzone definieren.  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |Stellt ein Array von [transitiongroup](transitionsgroup.md) -Elementen dar, die Zeit zonenübergänge angeben.  <br/> |
|[Übergänge](transitions.md) <br/> |Stellt ein Array von Zeit Zonen Übergängen dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TimeZoneDefinitions](timezonedefinitions.md) <br/> |Stellt ein Array von Zeitzonendefinitionen dar.  <br/> |
|[TimeZoneContext](timezonecontext.md) <br/> |Stellt die standardmäßige Zeitzonendefinition dar, die zum Festlegen der DateTime-Eigenschaften von Objekten verwendet werden soll, die mithilfe von Exchange-Webdienste erstellt, aktualisiert und abgerufen werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

