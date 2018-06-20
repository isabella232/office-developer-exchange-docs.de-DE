---
title: Referenten
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: Das Referenten-Element gibt die Referenten für eine onlinebesprechung umwandeln.
ms.openlocfilehash: f62b458759e0d8199c98827602d6c3fe16aebeea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830875"
---
# <a name="presenters"></a>Referenten

Das **Referenten** -Element gibt die Referenten für eine onlinebesprechung umwandeln. 
  
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

Der Textwert der **Referenten** -Element ist der Typ der Benutzer, die für eine onlinebesprechung umwandeln Referent sein kann. In der folgenden Tabelle werden die Textwerte für das Element **Referenten** beschrieben. 
  
**Text-Elementwerte Referenten**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Deaktiviert  <br/> |Referenten sind deaktiviert.  <br/> |
|Interne  <br/> |Nur interne Teilnehmer können als Referenten.  <br/> |
|Jeder  <br/> |Alle Teilnehmer kann als Referenten fungieren.  <br/> |
   
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
   

