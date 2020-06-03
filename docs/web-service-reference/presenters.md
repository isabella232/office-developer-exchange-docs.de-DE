---
title: Referenten
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: Das presenters-Element gibt die Referenten für eine Onlinebesprechung an.
ms.openlocfilehash: 0236457020dfc4684569e84d3d54e357af00d102
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529910"
---
# <a name="presenters"></a>Referenten

Das **Presenters** -Element gibt die Referenten für eine Onlinebesprechung an. 
  
```XML
<Presenters> Disabled | Internal | Everyone </Presenters>
```

 **PresentersType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[OnlineMeetingSettings](onlinemeetingsettings.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **Presenters** -Elements ist der Typ von Benutzern, die als Referent für eine Onlinebesprechung fungieren können. Die Textwerte für das **Presenters** -Element werden in der folgenden Tabelle beschrieben. 
  
**Textwerte des Presenters-Elements**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Deaktiviert  <br/> |Referenten sind deaktiviert.  <br/> |
|Intern  <br/> |Nur interne Teilnehmer können Referenten sein.  <br/> |
|Alle  <br/> |Jeder Teilnehmer kann ein Referent sein.  <br/> |
   
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
   

