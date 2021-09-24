---
title: TimeZoneDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeZoneDefinition
api_type:
- schema
ms.assetid: b005a80c-addb-4409-beff-e5162076752c
description: Das TimeZoneDefinition-Element gibt die Zeiträume und Übergänge an, die eine Zeitzone definieren.
ms.openlocfilehash: 6f2b580d2c3e31826ca74034cfda938cff71ee53
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538814"
---
# <a name="timezonedefinition"></a>TimeZoneDefinition

Das **TimeZoneDefinition-Element** gibt die Zeiträume und Übergänge an, die eine Zeitzone definieren. 
  
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
|[Zeiten](periods.md) <br/> |Stellt ein Array von [Period-Elementen](period.md) dar, die den Zeitversatz in verschiedenen Phasen der Zeitzone definieren.  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |Stellt ein Array von [TransitionsGroup-Elementen](transitionsgroup.md) dar, die Zeitzonenübergänge angeben.  <br/> |
|[Übergänge](transitions.md) <br/> |Stellt ein Array von Zeitzonenübergängen dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TimeZoneDefinitions](timezonedefinitions.md) <br/> |Stellt ein Array von Zeitzonendefinitionen dar.  <br/> |
|[TimeZoneContext](timezonecontext.md) <br/> |Stellt die Standardmäßige Zeitzonendefinition dar, die für die Bereichsdefinition der DateTime-Eigenschaften von Objekten verwendet werden soll, die mithilfe von Exchange Webdienste (Web Services, EWS) erstellt, aktualisiert und abgerufen werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

