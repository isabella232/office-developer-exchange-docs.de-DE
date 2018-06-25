---
title: Zuweisung (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: Zuweisung-Element gibt eine Instanz in ein Array von Attributen für ein PersonaType-Element.
ms.openlocfilehash: 0e800c92c75bf0c475d4bffd33d6ab49f9ad9a9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757407"
---
# <a name="attribution-personaattributiontype"></a>Zuweisung (PersonaAttributionType)

**Zuweisung** -Element gibt eine Instanz in ein Array von Attributen für ein **PersonaType** -Element. 
  
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
|[ID (Zeichenfolge)](id-string.md) <br/> |Gibt eine Zeichenfolge, die eine app oder eines Attributes in einer Rolle eindeutig identifiziert.  <br/> |
|[SourceId](sourceid.md) <br/> |Gibt den Bezeichner des Kontakts oder der Active Directory-Empfänger.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Der Anzeigename eines Ordners, Kontakt, Verteilerliste, Stellvertretungsbenutzers oder Regel definiert.  <br/> |
|[IsWritable](iswritable.md) <br/> |Gibt an, ob die zugrunde liegende Kontakt oder eine Active Directory-Empfänger geschrieben werden kann.  <br/> |
|[IsQuickContact](isquickcontact.md) <br/> |Gibt einen Boolean-Wert, der angibt, ob die zugrunde liegende Kontakt oder eine Active Directory-Empfänger ein schnelles Kontakt ist.  <br/> |
|[IsHidden](ishidden.md) <br/> |Enthält einen booleschen Wert, der angibt, ob die zugrunde liegende Kontakt oder eine Active Directory-Empfänger ausgeblendet oder als Teil der Rolle angezeigt werden soll.  <br/> |
|[FolderId](folderid.md) <br/> |Enthält den Schlüssel-ID und Ändern eines Ordners.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Hinweise (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) <br/> |Gibt ein Array von Informationen für eine oder mehrere Kontakte oder active Directory (AD) Empfänger in der zugeordneten Rolle aggregiert.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

