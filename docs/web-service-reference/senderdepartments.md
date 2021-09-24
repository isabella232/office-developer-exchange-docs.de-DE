---
title: SenderDepartments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SenderDepartments
api_type:
- schema
ms.assetid: b016cdde-d597-40ac-87c4-63ca68bd539d
description: Das SenderDepartments-Element gibt an, dass die Abteilung des Absenders mit einer der angegebenen Abteilungen in den untergeordneten Value-Elementen (ProtectionRuleValueType) übereinstimmt.
ms.openlocfilehash: 20feef066646cff988c1a26ee90da7dcade07e90
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527529"
---
# <a name="senderdepartments"></a>SenderDepartments

Das **SenderDepartments-Element** gibt an, dass die Abteilung des Absenders mit einer der angegebenen Abteilungen in den untergeordneten [Value-Elementen (ProtectionRuleValueType)](value-protectionrulevaluetype.md) übereinstimmt. 
  
```XML
<SenderDepartments>
   <Value/>
</SenderDepartments>
```

 **ProtectionRuleSenderDepartmentsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) <br/> |Identifiziert eine einzelne Absenderabteilung.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bedingung](condition.md) <br/> |Gibt die Bedingung an, die erfüllt sein muss, damit der Aktionsteil der Regel ausgeführt wird.  <br/> |
|[Und (ProtectionRuleAndType)](and-protectionruleandtype.md) <br/> |Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, um zu **"true"** ausgewertet zu werden. Gibt an, dass mehrere untergeordnete Schutzregelbedingungen vorhanden sein müssen.  <br/> |
   
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

