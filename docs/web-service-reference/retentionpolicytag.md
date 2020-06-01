---
title: RetentionPolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f46679d0-9236-41e2-8624-72300079c67c
description: Das RetentionPolicyTag-Element gibt die Aufbewahrungsrichtlinie für ein Postfachelement an.
ms.openlocfilehash: 3ece841e14e6cf11ab15e4a4d8b83a778ae32e46
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465177"
---
# <a name="retentionpolicytag"></a>RetentionPolicyTag

Das **RetentionPolicyTag** -Element gibt die Aufbewahrungsrichtlinie für ein Postfachelement an. 
  
```XML
<RetentionPolicyTag>
   <DisplayName/>
   <RetentionId/>
   <RetentionPeriod/>
   <Type/>
   <RetentionAction/>
   <Description/>
   <IsVisible/>
   <OptedInto/>
   <IsArchive/>
</RetentionPolicyTag>
```

 **RetentionPolicyTagType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[DisplayName (Zeichenfolge)](displayname-string.md)  |  [Aufbewahrungs-Nr](retentionid.md)  |  [RetentionPeriod](retentionperiod.md)  |  [Typ (ElcFolderType)](type-elcfoldertype.md)  |  [Aufbewahrungszeit](retentionaction.md)  |  [Beschreibung](description.md)  |  [IsVisible](isvisible.md)  |  [OptedInto](optedinto.md)  |  [Isarchive](isarchive.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[RetentionPolicyTags](retentionpolicytags.md)
  
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
   

