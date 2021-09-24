---
title: ForwardAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bc32e0f4-61e9-4c9f-9a03-90a07eb51c53
description: Das ForwardAllowed-Element gibt an, ob die Weiterleitung von E-Mails aktiviert ist.
ms.openlocfilehash: 8c9b2319ed6b3665e5d59d9f07b93fb78043042c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528665"
---
# <a name="forwardallowed"></a>ForwardAllowed

Das **ForwardAllowed-Element** gibt an, ob die Weiterleitung von E-Mails aktiviert ist. 
  
```XML
<ForwardAllowed>true | false</ForwardAllowed>
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
|[RightsManagementLicenseData](rightsmanagementlicensedata.md) <br/> |Gibt Informationen zur Rechteverwaltungslizenz an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **ForwardAllowed-Element** gibt an, dass weiterleitungs-E-Mails zulässig sind. Der Wert **"false"** gibt an, dass die Weiterleitung nicht zulässig ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

