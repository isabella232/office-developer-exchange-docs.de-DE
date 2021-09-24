---
title: Attribution (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: Das Attribution-Element gibt eine Instanz in einem Array von Attributen für ein PersonaType-Element an.
ms.openlocfilehash: eb2fe66042b6c7f52732be20195f0f4b94ab867c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524378"
---
# <a name="attribution-personaattributiontype"></a>Attribution (PersonaAttributionType)

Das **Attribution-Element** gibt eine Instanz in einem Array von Attributen für ein **PersonaType-Element an.** 
  
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
|[ID (Zeichenfolge)](id-string.md) <br/> |Gibt eine Zeichenfolge an, die eine App oder eine Zuschreibung in einer Persona eindeutig identifiziert.  <br/> |
|[SourceId](sourceid.md) <br/> |Gibt den Bezeichner des Kontakts oder Active Directory-Empfängers an.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Definiert den Anzeigenamen eines Ordners, Kontakts, einer Verteilerliste, eines Stellvertreterbenutzers oder einer Regel.  <br/> |
|[IsWritable](iswritable.md) <br/> |Gibt an, ob der zugrunde liegende Kontakt oder Active Directory-Empfänger geschrieben werden kann.  <br/> |
|[IsQuickContact](isquickcontact.md) <br/> |Gibt einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt oder Active Directory-Empfänger ein Schnellkontakt ist.  <br/> |
|[IsHidden](ishidden.md) <br/> |Enthält einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt oder Active Directory-Empfänger als Teil der Persona ausgeblendet oder angezeigt werden soll.  <br/> |
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Attributions (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) <br/> |Gibt ein Array von Attributionsinformationen für einen oder mehrere kontakte oder Active Directory (AD)-Empfänger an, die in der zugeordneten Persona aggregiert werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

