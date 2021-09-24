---
title: Bedingung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Condition
api_type:
- schema
ms.assetid: 0790a3f2-cb31-4036-a757-7821aa0722cb
description: Das Condition-Element identifiziert die Bedingung, die erfüllt werden muss, damit der Aktionsteil der Regel ausgeführt wird.
ms.openlocfilehash: 80efb2121e813a966faf419233cac4d23e971bc6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512007"
---
# <a name="condition"></a>Bedingung

Das **Condition-Element** identifiziert die Bedingung, die erfüllt werden muss, damit der Aktionsteil der Regel ausgeführt wird. 
  
```xml
<Condition>
   <AllInternal/>
</Condition>
```

```xml
<Condition> 
    <SenderDepartments/> 
</Condition>
```

```xml
<Condition> 
    <True/> 
</Condition>
```

```xml
<Condition> 
    <Recipients/> 
</Condition>
```

```xml
<Condition> 
    <And/> 
</Condition>
```

**ProtectionRuleConditionType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AllInternal](allinternal.md) <br/> |Wird als **"true"** ausgewertet, wenn alle Empfänger einer E-Mail-Nachricht in der Organisation des Absenders intern sind.  <br/> |
|[Und (ProtectionRuleAndType)](and-protectionruleandtype.md) <br/> |Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, um zu **"true"** ausgewertet zu werden. Gibt an, dass mehrere untergeordnete Schutzregelbedingungen vorhanden sein müssen.  <br/> |
|[RecipientIs](recipientis.md) <br/> |Gibt an, dass jeder Empfänger der E-Mail-Nachricht mit einem der angegebenen Empfänger in den untergeordneten [Value-Elementen (ProtectionRuleValueType)](value-protectionrulevaluetype.md) übereinstimmt.  <br/> |
|[SenderDepartments](senderdepartments.md) <br/> |Gibt an, dass die Abteilung des Absenders mit einer der angegebenen Abteilungen in den untergeordneten [Value-Elementen (ProtectionRuleValueType)](value-protectionrulevaluetype.md) übereinstimmt.  <br/> |
|[True](true.md) <br/> |Gibt eine Bedingung an, die immer übereinstimmt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Rule](rule.md) <br/> |Enthält eine einzelne Schutzregel.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
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

