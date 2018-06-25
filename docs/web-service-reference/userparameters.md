---
title: UserParameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bad7311f-7ecd-4f0c-b8e7-dd8f7d378f55
description: Das UserParameters-Element enthält eine Liste der Clienterweiterungen aktiviert und deaktiviert.
ms.openlocfilehash: e0a72fe13255380ee56b32c863fb3bffb2e1ac5e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839458"
---
# <a name="userparameters"></a>UserParameters

Das **UserParameters** -Element enthält eine Liste der Clienterweiterungen aktiviert und deaktiviert. 
  
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
|UserId  <br/> |Der Textwert des **Benutzer-ID** -Attributs ist der Bezeichner des Benutzers.  <br/> |
|EnabledOnly  <br/> |Der Textwert der der **EnabledOnly** gibt an, ob die Antwort nur die aktivierten Erweiterungen enthält.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[UserEnabledExtensions](userenabledextensions.md) | [UserDisabledExtensions](userdisabledextensions.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetClientExtension](getclientextension.md)
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

