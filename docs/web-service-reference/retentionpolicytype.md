---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: Das RetentionPolicyType-Element gibt den Aufbewahrungsrichtlinientyp an, der auf Elemente in einer Unterhaltung angewendet wird.
ms.openlocfilehash: 961f72c35443e9f265e9313166fa77c8cd93d654
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509385"
---
# <a name="retentionpolicytype"></a>RetentionPolicyType

Das **RetentionPolicyType-Element** gibt den Aufbewahrungsrichtlinientyp an, der auf Elemente in einer Unterhaltung angewendet wird. 
  
```XML
<RetentionPolicyType> Delete | Archive </RetentionPolicyType>
```

 **RetentionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ConversationAction](conversationaction.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **RetentionPolicyType-Elements** ist der Aufbewahrungstyp, der auf Elemente in einer Unterhaltung angewendet wird. Der Textwert **"Löschen"** gibt an, dass die Elemente in der Unterhaltung gelöscht werden, wenn die Aufbewahrungszeit abgelaufen ist. Der Textwert des **Archivs** gibt an, dass die Elemente in der Unterhaltung in das Archivpostfach verschoben werden, wenn die Aufbewahrungssperre abläuft. 
  
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
   

