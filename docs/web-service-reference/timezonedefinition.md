---
title: Zeitzonendefinition
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
description: Das Zeitzonendefinition-Element gibt die Zeiträume und Übergänge, die eine Zeitzone definiert.
ms.openlocfilehash: ffd5ed0c862af794e4aff2387f508849b1d5fd5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839224"
---
# <a name="timezonedefinition"></a>Zeitzonendefinition

Das **Zeitzonendefinition** -Element gibt die Zeiträume und Übergänge, die eine Zeitzone definiert. 
  
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
|Id  <br/> |Den eindeutigen Bezeichner der Zeitzone darstellt.  <br/> |
|Name  <br/> |Stellt den beschreibenden Namen der Zeitzone.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Perioden](periods.md) <br/> |Stellt ein Array von [Periode](period.md) -Elementen, die den Uhrzeit-Offset in verschiedenen Phasen der Zeitzone definieren.  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |Stellt ein Array von [TransitionsGroup](transitionsgroup.md) -Elementen, die Zeitzone Übergänge angeben.  <br/> |
|[Übergänge](transitions.md) <br/> |Stellt ein Array von Zeitzone Übergänge.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TimeZoneDefinitions](timezonedefinitions.md) <br/> |Stellt ein Array von Zeitzonendefinitionen.  <br/> |
|[TimeZoneContext](timezonecontext.md) <br/> |Stellt die Definition der Standard-Zeitzone, die verwendet werden soll, für das Festlegen des Gültigkeitsbereichs der DateTime-Eigenschaft der Objekte, die erstellt, aktualisiert und mithilfe der Exchange-Webdienste (EWS) abgerufen werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

