---
title: Operations
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Operations
api_type:
- schema
ms.assetid: d8cd41b1-28ae-4c95-9ff6-8b25c8e18306
description: Das Operations-Element enthält ein Array von Regelvorgängen, die für einen Posteingang ausgeführt werden können.
ms.openlocfilehash: 48679c9c7c0482ab53d3af5c661dc6efe513e637
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518071"
---
# <a name="operations"></a>Operations

Das **Operations-Element** enthält ein Array von Regelvorgängen, die für einen Posteingang ausgeführt werden können. 
  
[UpdateInboxRules](updateinboxrules.md)
  
```XML
<Operations>
    <CreateRuleOperation/>
    <SetRuleOperation/>
    <DeleteRuleOperation/>
</Operations>
```

 **ArrayOfRuleOperationsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |Stellt einen Vorgang zum Erstellen einer neuen Posteingangsregel dar.  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |Stellt einen Vorgang zum Aktualisieren einer Posteingangsregel dar.  <br/> |
|[DeleteRuleOperation](deleteruleoperation.md) <br/> |Stellt einen Vorgang zum Löschen einer Posteingangsregel dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UpdateInboxRules](updateinboxrules.md) <br/> |Definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Serverspeicher.  <br/> |
   
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



[UpdateInboxRules-Vorgang](updateinboxrules-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

