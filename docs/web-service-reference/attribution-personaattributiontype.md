---
title: Attribution (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: Das Attribution-Element gibt eine Instanz in einem Array von Attributen für ein personatype-Element an.
ms.openlocfilehash: 05b0d41c116f2ed7b8dbb3ac44108bb879256b5c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464175"
---
# <a name="attribution-personaattributiontype"></a>Attribution (PersonaAttributionType)

Das **Attribution** -Element gibt eine Instanz in einem Array von Attributen für ein **personatype** -Element an. 
  
```XML
<Attribution>
    <Id></Id>
    <SourceId></SourceId>
    <DisplayName></DisplayName>
    <IsWritable></IsWritable>
    <IsQuickContact></IsQuickContact>
    <IsHidden></IsHidden>
    <FolderId></FolderId>
</Attribution>
```

 **PersonaAttributionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ID (Zeichenfolge)](id-string.md) <br/> |Gibt eine Zeichenfolge an, die eine APP oder eine Attribution in einer Persona eindeutig identifiziert.  <br/> |
|[SourceId](sourceid.md) <br/> |Gibt den Bezeichner des Kontakts oder Active Directory Empfängers an.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Definiert den Anzeigenamen eines Ordners, Kontakts, einer Verteilerliste, eines Stellvertreter Benutzers oder einer Regel.  <br/> |
|[Isschreibbar](iswritable.md) <br/> |Gibt an, ob der zugrunde liegende Kontakt oder Active Directory Empfänger in geschrieben werden kann.  <br/> |
|[IsQuickContact](isquickcontact.md) <br/> |Gibt einen booleschen Wert an, der angibt, ob der zugrunde liegende Kontakt oder Active Directory Empfänger ein schnell Kontakt ist.  <br/> |
|[IsHidden](ishidden.md) <br/> |Enthält einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt oder Active Directory Empfänger ausgeblendet oder als Teil der Rolle angezeigt werden soll.  <br/> |
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Zuordnungen (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) <br/> |Gibt ein Array mit Zuordnungsinformationen für einen oder mehrere der Kontakte oder Active Directory-Empfänger (AD) an, die in der zugeordneten Rolle aggregiert sind.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

