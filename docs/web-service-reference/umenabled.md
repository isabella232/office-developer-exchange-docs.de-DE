---
title: UmEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UmEnabled
api_type:
- schema
ms.assetid: 87382d9b-0c02-49ec-85dc-3f5918df3195
description: Das UmEnabled-Element gibt an, ob Unified Messaging für ein Konto aktiviert ist.
ms.openlocfilehash: 9ff6432324e3a15b9ae805a7d6d836c9c895059c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527153"
---
# <a name="umenabled"></a>UmEnabled

Das **UmEnabled-Element** gibt an, ob Unified Messaging für ein Konto aktiviert ist. 
  
```XML
<UmEnabled>true | false</UmEnabled>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UnifiedMessagingConfiguration](unifiedmessagingconfiguration.md) <br/> |Enthält Dienstkonfigurationsinformationen für den Unified Messaging-Dienst.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **UmEnabled-Elements** ist **"true",** wenn Unified Messaging für das Konto aktiviert ist. andernfalls ist der Wert **false**.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist erforderlich.
  
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

