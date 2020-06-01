---
title: RemoveOutlookRuleBlob
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveOutlookRuleBlob
api_type:
- schema
ms.assetid: 69614475-8bd3-4475-b988-614fe9cad8ef
description: Das RemoveOutlookRuleBlob-Element gibt an, ob das Microsoft Outlook Regel-BLOB entfernt werden soll.
ms.openlocfilehash: b4202ab52bf16d1ad1546ec963cd8b9dacd2bd63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467669"
---
# <a name="removeoutlookruleblob"></a>RemoveOutlookRuleBlob

Das **RemoveOutlookRuleBlob** -Element gibt an, ob das Microsoft Outlook Regel-BLOB entfernt werden soll. 
  
[UpdateInboxRules](updateinboxrules.md)
  
[RemoveOutlookRuleBlob](removeoutlookruleblob.md)
  
```XML
<RemoveOutlookRuleBlob>true | false</RemoveOutlookRuleBlob>
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
|[UpdateInboxRules](updateinboxrules.md) <br/> |Definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Server Speicher.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** gibt an, dass das Outlook-Regel-BLOB entfernt werden soll. Der Textwert **false** gibt an, dass das Outlook-Regel-BLOB nicht entfernt werden soll. 
  
## <a name="remarks"></a>Bemerkungen

Legen Sie dieses Element auf **true** fest, um eine Regel Aktualisierung für Posteingangsregeln zuzulassen. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateInboxRules-Vorgang](updateinboxrules-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

