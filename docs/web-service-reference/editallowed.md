---
title: EditAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e63c4f7e-77c0-4826-b4e2-43b795d03914
description: Das EditAllowed-Element gibt an, ob die Verwaltung von Informationsrechten bearbeitet werden kann.
ms.openlocfilehash: 2bd88dd47eb3f1964eae678412a6748ee8d28ec8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540118"
---
# <a name="editallowed"></a>EditAllowed

Das **EditAllowed-Element** gibt an, ob die Verwaltung von Informationsrechten bearbeitet werden kann. 
  
```XML
<EditAllowed> true | false </EditAllowed>
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

Der Textwert  true für das **EditAllowed-Element** gibt an, dass die Verwaltung von Informationsrechten (Information Rights Management, IRM) bearbeitet werden kann. Der Wert **"false"** gibt an, dass IRM nicht bearbeitet werden kann. 
  
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

