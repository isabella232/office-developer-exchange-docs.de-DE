---
title: ModifyRecipientsAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f25e673-0df0-4285-bf03-a083a395cdab
description: Das ModifyRecipientsAllowed-Element gibt an, ob die Änderung der Empfänger aktiviert ist.
ms.openlocfilehash: 4366f9ed0a6843f9a297718cb999fb8c3a02ee17
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520395"
---
# <a name="modifyrecipientsallowed"></a>ModifyRecipientsAllowed

Das **ModifyRecipientsAllowed-Element** gibt an, ob die Änderung der Empfänger aktiviert ist. 
  
```XML
<ModifyRecipientsAllowed> true | false </ModifyRecipientsAllowed>
```

 **boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[RightsManagementLicenseData](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **ModifyRecipientsAllowed-Element** gibt an, dass die Elementempfängerliste für ein Element mit aktivierter Rechteverwaltung geändert werden kann. Der Wert **"false"** gibt an, dass die Empfängerliste nicht geändert werden kann. 
  
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
   

