---
title: Fehler
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Error
api_type:
- schema
ms.assetid: b1f54673-578a-496b-99f5-0fde2c669278
description: The Error element represents a single validation error on a particular rule property value, predicate property value, or action property value.
ms.openlocfilehash: aeeda25ccc3e657e99bd6f2fea12322fdd3e720d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530861"
---
# <a name="error"></a>Fehler

The **Error** element represents a single validation error on a particular rule property value, predicate property value, or action property value. 
  
```XML
<Error>
   <FieldUri/>
   <ErrorCode/>
   <ErrorMessage/>
   <FieldValue/>
</Error>
```

 **RuleValidationErrorType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldUri (Rule)](fielduri-rule.md) <br/> |Gibt den URI für das Regelfeld an, das den Überprüfungsfehler verursacht hat.  <br/> |
|[ErrorCode](errorcode.md) <br/> |Stellt einen Fehlercode für die Regelüberprüfung dar, der beschreibt, was bei der Überprüfung für jedes Regelprädikat oder jede Aktion fehlgeschlagen ist.  <br/> |
|[ErrorMessage](errormessage.md) <br/> |Stellt den Grund für die Überprüfungsfehler.  <br/> |
|[FieldValue](fieldvalue.md) <br/> |Stellt den Wert des Felds dar, das den Überprüfungsfehler verursacht hat.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ValidationErrors](validationerrors.md) <br/> |Stellt ein Array von Regelüberprüfungsfehlern für jedes Regelfeld dar, das einen Fehler aufweist.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

