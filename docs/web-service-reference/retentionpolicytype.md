---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: Das RetentionPolicyType-Element gibt an, welche Richtlinie Aufbewahrung auf Elemente in einer Unterhaltung angewendet wird.
ms.openlocfilehash: dacb3fa75611cbd6e6e29eab7c791dfd8964c9ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831229"
---
# <a name="retentionpolicytype"></a>RetentionPolicyType

Das **RetentionPolicyType** -Element gibt an, welche Richtlinie Aufbewahrung auf Elemente in einer Unterhaltung angewendet wird. 
  
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

Der Textwert des **RetentionPolicyType** -Elements ist die Aufbewahrung auf Elemente in einer Unterhaltung angewendet. Der Textwert der **Löschen** gibt an, dass die Elemente in der Unterhaltung gelöscht werden, wenn das Anhalten der Aufbewahrungszeit läuft ab. Der Textwert der **Archive** gibt an, dass die Elemente in der Unterhaltung in das Archivpostfach verschoben werden, wenn das Anhalten der Aufbewahrungszeit läuft ab. 
  
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
   

