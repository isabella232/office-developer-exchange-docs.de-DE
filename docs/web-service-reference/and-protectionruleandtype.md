---
title: Und (ProtectionRuleAndType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- And
api_type:
- schema
ms.assetid: 7fafd1c8-cd29-43a0-b383-f6595f934f48
description: Das And-Element gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, um "true" auszuwerten.
ms.openlocfilehash: 01721b460d87d3282a1a793966b0259e0f1342dd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518938"
---
# <a name="and-protectionruleandtype"></a>Und (ProtectionRuleAndType)

The **And** element specifies that all child elements must match to evaluate to **true**.
  
```xml
<And>
   <AllInternal/>
   <And/>
   <RecipientIs/>
   <SenderDepartments/>
   <True/>
</And>
```

 **ProtectionRuleAndType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AllInternal](allinternal.md) <br/> |Wird als **"true"** ausgewertet, wenn alle Empfänger einer E-Mail-Nachricht in der Organisation des Absenders intern sind.  <br/> |
|**Und** <br/> |Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, um zu **"true"** ausgewertet zu werden.  <br/> |
|[RecipientIs](recipientis.md) <br/> |Gibt an, dass jeder Empfänger der E-Mail-Nachricht mit einem der angegebenen Empfänger in den untergeordneten [Value-Elementen (ProtectionRuleValueType)](value-protectionrulevaluetype.md) übereinstimmt.  <br/> |
|[SenderDepartments](senderdepartments.md) <br/> |Gibt an, dass die Abteilung des Absenders mit einer der angegebenen Abteilungen in den untergeordneten [Value-Elementen (ProtectionRuleValueType)](value-protectionrulevaluetype.md) übereinstimmt.  <br/> |
|[True](true.md) <br/> |Gibt eine Bedingung an, die immer übereinstimmt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bedingung](condition.md) <br/> |Gibt die Bedingung an, die erfüllt sein muss, damit der Aktionsteil der Regel ausgeführt wird.  <br/> |
|**Und** <br/> |Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, um zu **"true"** ausgewertet zu werden.  <br/> |
   
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

