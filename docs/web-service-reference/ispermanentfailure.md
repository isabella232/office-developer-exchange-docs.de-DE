---
title: IsPermanentFailure
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18dc3a97-cc0a-4092-934e-a6e86f52e668
description: Das IsPermanentFailure-Element gibt an, ob es sich bei ein vorherigen Versuch zum Indizieren des Elements nicht erfolgreich war.
ms.openlocfilehash: 39592c15394a57e1c6aa1183ed0ccedeb085e6ea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830085"
---
# <a name="ispermanentfailure"></a>IsPermanentFailure

Das **IsPermanentFailure** -Element gibt an, ob es sich bei ein vorherigen Versuch zum Indizieren des Elements nicht erfolgreich war. 
  
```XML
<IsPermanentFailure>true | false</IsPermanentFailure>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[NonIndexableItemDetail](nonindexableitemdetail.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **IsPermanentFailure** -Element gibt an, dass es sich bei ein vorherigen Versuch zum Indizieren des postfachelements nicht erfolgreich war. Der Wert **false** gibt an, dass es sich bei ein vorherigen Versuch zum Indizieren des postfachelements erfolgreich war. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

