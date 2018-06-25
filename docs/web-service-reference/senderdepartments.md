---
title: SenderDepartments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SenderDepartments
api_type:
- schema
ms.assetid: b016cdde-d597-40ac-87c4-63ca68bd539d
description: Das SenderDepartments-Element gibt an, dass die Abteilung des Absenders einer der angegebenen Abteilungen im untergeordneten Wert (ProtectionRuleValueType) übereinstimmt.
ms.openlocfilehash: d40e6299bd46ede559cc2cce3bcc9d1611e96bd7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831331"
---
# <a name="senderdepartments"></a>SenderDepartments

Das **SenderDepartments** -Element gibt an, dass die Abteilung des Absenders einer der angegebenen Abteilungen im untergeordneten [Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) übereinstimmt. 
  
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
|[Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) <br/> |Eine Abteilung der einzelnen Absender identifiziert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bedingung](condition.md) <br/> |Gibt die Bedingung, die erfüllt sein muss, für die Aktionsteil der Regel ausgeführt werden.  <br/> |
|[Und (ProtectionRuleAndType)](and-protectionruleandtype.md) <br/> |Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit zu **true**ausgewertet werden. Gibt an, dass mehr als ein Protection untergeordneten regelbedingung sein muss.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

