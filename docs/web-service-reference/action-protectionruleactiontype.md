---
title: Aktion (ProtectionRuleActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Action
api_type:
- schema
ms.assetid: ca090dec-e2c5-49c8-a057-8d1f2409147f
description: Das Action-Element gibt an, welche Aktion ausgeführt werden muss, wenn der Bedingungsteil der Regel übereinstimmt.
ms.openlocfilehash: 6ca051622bb05b2ae2690f6b32ee11662161a4c1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534005"
---
# <a name="action-protectionruleactiontype"></a>Aktion (ProtectionRuleActionType)

Das **Action-Element** gibt an, welche Aktion ausgeführt werden muss, wenn der Bedingungsteil der Regel übereinstimmt. 
  
```xml
<Action Name="">
   <Argument/>
</Action>

```

 **ProtectionRuleActionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Gibt den Namen der Aktion an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Argument](argument.md) <br/> |Gibt Argumente für die Aktion an. Dieses Element tritt nicht auf, wenn für die angegebene Aktion keine Argumente angegeben werden müssen. Dieses Element kann ein oder mehrere Male auftreten, wenn für eine Aktion ein oder mehrere Argumente erforderlich sind. Die **RightsProtectMessage-Aktion** enthält ein einzelnes Argument.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Rule](rule.md) <br/> |Enthält eine einzelne Schutzregel.  <br/> |
   
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

