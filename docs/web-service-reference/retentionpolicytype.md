---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: Das RetentionPolicyType-Element gibt den Aufbewahrungs Richtlinientyp an, der auf Elemente in einer Unterhaltung angewendet wird.
ms.openlocfilehash: 3900718f10e1e11d5864ebf7e64a3e1e22aa45c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462871"
---
# <a name="retentionpolicytype"></a>RetentionPolicyType

Das **RetentionPolicyType** -Element gibt den Aufbewahrungs Richtlinientyp an, der auf Elemente in einer Unterhaltung angewendet wird. 
  
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

[Unterhaltung](conversationaction.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **RetentionPolicyType** -Elements ist der Aufbewahrungs, der auf Elemente in einer Unterhaltung angewendet wird. Der Textwert von **Delete** gibt an, dass die Elemente in der Unterhaltung gelöscht werden, wenn die Aufbewahrungsdauer abläuft. Der Textwert von **Archive** gibt an, dass die Elemente in der Unterhaltung nach Ablauf der Aufbewahrungsdauer in das Archivpostfach verschoben werden. 
  
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
   

