---
title: IsOwner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ea0f0afc-32fe-46cb-8530-62a6ce9490f6
description: Das IsOwner-Element gibt an, ob der angegebene E-Mail-Benutzer der Besitzer ist.
ms.openlocfilehash: 7e3baaf0f3fb2eac028117622eedd57088d71612
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541007"
---
# <a name="isowner"></a>IsOwner

Das **IsOwner-Element** gibt an, ob der angegebene E-Mail-Benutzer der Besitzer ist. 
  
```XML
<IsOwner>true | false</IsOwner>
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

Der Textwert **"true"** für das **IsOwner-Element** gibt an, dass der Benutzer der Besitzer der für ein Element ausgegebenen Rechte ist. Der Wert **"false"** gibt an, dass der Benutzer nicht der Besitzer der für ein Element ausgegebenen Rechte ist. 
  
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

