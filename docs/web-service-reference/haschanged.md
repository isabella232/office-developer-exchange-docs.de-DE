---
title: HasChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 15ff513d-f39e-44ed-a13f-ab3f86fa37e1
description: Das HasChanged-Element gibt an, ob ein Benutzer Foto geändert wurde.
ms.openlocfilehash: b0129e3d3acb43ada16a824e3d21706999d7053c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829802"
---
# <a name="haschanged"></a>HasChanged

Das **HasChanged** -Element gibt an, ob ein Benutzer Foto geändert wurde. 
  
```XML
<HasChanged> true | false </HasChanged>
```

 ****
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetUserPhotoResponse](getuserphotoresponse.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **HasChanged** -Element gibt an, dass das Foto seit dem letzten Speichern geändert wurde, die es zurückgegeben wurde. Der Wert **false** gibt an, dass das Foto nicht seit dem letzten Speichern geändert wurde, die es zurückgegeben wurde. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

