---
title: UserParameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bad7311f-7ecd-4f0c-b8e7-dd8f7d378f55
description: Das UserParameters-Element enthält eine Liste der aktivierten und deaktivierten Clienterweiterungen.
ms.openlocfilehash: 1d93ec0f4e44b238fcb9aca23672c262795290a6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510729"
---
# <a name="userparameters"></a>UserParameters

Das **UserParameters-Element** enthält eine Liste der aktivierten und deaktivierten Clienterweiterungen. 
  
```XML
<UserParameters UserId="" EnabledOnly="">
   <UserEnabledExtensions/>
   <UserDisabledExtensions/>
</UserParameters>
```

 **GetClientExtensionUserParametersType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|UserId  <br/> |Der Textwert des **UserId-Attributs** ist der Bezeichner des Benutzers.  <br/> |
|EnabledOnly  <br/> |Der Textwert von **EnabledOnly** gibt an, ob die Antwort nur die aktivierten Erweiterungen enthält.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[UserEnabledExtensions](userenabledextensions.md)  |  [UserDisabledExtensions](userdisabledextensions.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetClientExtension](getclientextension.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

