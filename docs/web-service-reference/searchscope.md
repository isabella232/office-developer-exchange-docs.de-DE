---
title: SearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4a53989e-eca6-45c4-afac-4d6ac19597d2
description: Das SearchScope-Element gibt den Umfang einer Suche an.
ms.openlocfilehash: d4caa87cd552a633812b99d7e97f2419b156fb78
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523399"
---
# <a name="searchscope"></a>SearchScope

Das **SearchScope-Element** gibt den Umfang einer Suche an. 
  
```XML
<SearchScope> PrimaryOnly | ArchiveOnly | All </SearchScope>
```

 **MailboxSearchLocationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[MailboxSearchScope](mailboxsearchscope.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **SearchScope-Elements** gibt den Postfachtyp an, der nach einer Ermittlungssuche durchsucht wird. Der Textwert **"PrimaryOnly"** gibt an, dass das primäre Postfach durchsucht wird. Der Textwert **"ArchiveOnly"** gibt an, dass das Archivpostfach durchsucht wird. Der Textwert **"Alle"** gibt an, dass sowohl die primären postfächer als auch die Archivpostfächer durchsucht werden. 
  
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
   

