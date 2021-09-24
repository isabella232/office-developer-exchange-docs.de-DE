---
title: Moderatoren
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: Das Presenters-Element gibt die Referenten für eine Onlinebesprechung an.
ms.openlocfilehash: 1c9bf9093450e675245b647c98d7b1d00101ce9e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519142"
---
# <a name="presenters"></a>Moderatoren

Das **Presenters-Element** gibt die Referenten für eine Onlinebesprechung an. 
  
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

Der Textwert des **Presenters-Elements** ist der Typ der Benutzer, die ein Referent für eine Onlinebesprechung sein können. Die Textwerte für das **Presenters-Element** werden in der folgenden Tabelle beschrieben. 
  
**Textwerte des Presenters-Elements**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Deaktiviert  <br/> |Referenten sind deaktiviert.  <br/> |
|Intern  <br/> |Nur interne Teilnehmer können Referenten sein.  <br/> |
|Jeder  <br/> |Jeder Teilnehmer kann ein Referent sein.  <br/> |
   
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
   

