---
title: User Parameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bad7311f-7ecd-4f0c-b8e7-dd8f7d378f55
description: Das User Parameters-Element enthält eine Liste der aktivierten und deaktivierten Clienterweiterungen.
ms.openlocfilehash: 76bf858adfb6d2ef76a25c234117131752c60d7b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526753"
---
# <a name="userparameters"></a>User Parameters

Das **User Parameters** -Element enthält eine Liste der aktivierten und deaktivierten Clienterweiterungen. 
  
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
|UserId  <br/> |Der Textwert des **UserID** -Attributs ist der Bezeichner des Benutzers.  <br/> |
|EnabledOnly  <br/> |Der Textwert des **EnabledOnly** gibt an, ob die Antwort nur die aktivierten Erweiterungen enthält.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[UserEnabledExtensions](userenabledextensions.md)  |  [UserDisabledExtensions](userdisabledextensions.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetClientExtension](getclientextension.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

