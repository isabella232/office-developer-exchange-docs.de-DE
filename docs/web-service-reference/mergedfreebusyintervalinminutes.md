---
title: MergedFreeBusyIntervalInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MergedFreeBusyIntervalInMinutes
api_type:
- schema
ms.assetid: 481cdbc6-d5aa-49fa-a3fa-9d119d3dca99
description: Das MergedFreeBusyIntervalInMinutes-Element stellt den Zeitunterschied zwischen zwei aufeinander folgenden Steckplätzen in der FreeBusyMerged-Ansicht dar.
ms.openlocfilehash: 543a631ffe85e50e3efe84fb8109b190a276ed8f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532390"
---
# <a name="mergedfreebusyintervalinminutes"></a>MergedFreeBusyIntervalInMinutes

Das **MergedFreeBusyIntervalInMinutes-Element** stellt den Zeitunterschied zwischen zwei aufeinander folgenden Steckplätzen in der **FreeBusyMerged-Ansicht** dar. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[FreeBusyViewOptions](freebusyviewoptions.md)
  
[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)
  
```xml
<MergedFreeBusyIntervalInMinutes>...</MergedFreeBusyIntervalInMinutes>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |Gibt den Typ der Frei/Gebucht-Informationen an, die in der Antwort zurückgegeben werden.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert stellt die Zeit in Minuten dar. Der Standardwert beträgt 30 Minuten. Sechs Minuten ist das minimale Intervall, und ein Tag (1440 Minuten) ist das maximale Intervall für dieses Element.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieser Wert wird nur verwendet, wenn das [RequestedView](requestedview.md) -Element gleich **MergedOnly**, **FreeBusyMerged** oder **DetailedMerge** ist. Dies ist ein ganzzahliger Datentyp. Der Datenstrom, der die von diesem Element definierten Intervalle enthält, wird im [MergedFreeBusy-Element](mergedfreebusy.md) zurückgegeben. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)


[Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

