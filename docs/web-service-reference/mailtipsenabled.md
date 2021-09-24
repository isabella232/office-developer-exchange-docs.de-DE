---
title: MailTipsEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailTipsEnabled
api_type:
- schema
ms.assetid: 737388b3-7b73-42af-94d3-3dbb0659718f
description: Das MailTipsEnabled-Element gibt an, ob der E-Mail-Tipps-Dienst verfügbar ist.
ms.openlocfilehash: 7444ba7218ebfed85b02dafb0358af9781b22059
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511145"
---
# <a name="mailtipsenabled"></a>MailTipsEnabled

Das **MailTipsEnabled-Element** gibt an, ob der E-Mail-Tipps-Dienst verfügbar ist. 
  
```xml
<MailTipsEnabled>true | false</MailTipsEnabled>
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
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |Enthält Dienstkonfigurationsinformationen für den E-Mail-Tipps-Dienst.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert dieses Elements ist **"true",** wenn der E-Mail-Tipps-Dienst verfügbar ist. Der Wert ist **"false",** wenn der E-Mail-Tipps-Dienst nicht verfügbar ist. 
  
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

