---
title: Fehler (ungefährer Wortlaut)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Error
api_type:
- schema
ms.assetid: b1f54673-578a-496b-99f5-0fde2c669278
description: Das Error-Element stellt einen einzelnen Validierungsfehler für einen bestimmten Regel Eigenschaftswert, einen Prädikateigenschaftswert oder einen Action-Eigenschaftswert dar.
ms.openlocfilehash: 9c28f63aa79446d89152868c81c85ffa7b3a8b39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460680"
---
# <a name="error"></a>Fehler (ungefährer Wortlaut)

Das **Error** -Element stellt einen einzelnen Validierungsfehler für einen bestimmten Regel Eigenschaftswert, einen Prädikateigenschaftswert oder einen Action-Eigenschaftswert dar. 
  
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
|[FieldUri (Regel)](fielduri-rule.md) <br/> |Gibt den URI für das Regel Feld an, das den Validierungsfehler verursacht hat.  <br/> |
|[ErrorCode](errorcode.md) <br/> |Stellt einen Fehlercode für die Regelüberprüfung dar, der die fehlgeschlagene Überprüfung der einzelnen Regelprädikate oder Aktionen beschreibt.  <br/> |
|[ErrorMessage](errormessage.md) <br/> |Stellt den Grund für die Überprüfungsfehler.  <br/> |
|[FieldValue](fieldvalue.md) <br/> |Stellt den Wert des Felds dar, das den Validierungsfehler verursacht hat.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ValidationErrors](validationerrors.md) <br/> |Stellt ein Array von Regel Validierungsfehlern für jedes Regel Feld dar, das einen Fehler aufweist.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

