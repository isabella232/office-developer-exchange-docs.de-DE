---
title: Aktion (SetClientExtensionActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: Das Action-Element enthält die Aktion, die der Exchange-Server für eine app ausgeführt werden soll.
ms.openlocfilehash: a231cedfa6e4759dabfcbecfbe9a9b851f834247
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757215"
---
# <a name="action-setclientextensionactiontype"></a>Aktion (SetClientExtensionActionType)

Das **Action** -Element enthält die Aktion, die der Exchange-Server für eine app ausgeführt werden soll. 
  
```XML
<Action ActionId="" ExtensionId="">
   <ClientExtension/>
</Action>
```

 **SetClientExtensionActionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|ActionId  <br/> |Gibt den Bezeichner der Aktion. Dieses Attribut ist erforderlich.  <br/> |
|ExtensionID geändert  <br/> |Gibt den Bezeichner der Erweiterung. Dieses Attribut ist optional.  <br/> |
   
#### <a name="actionid"></a>ActionId

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Konfigurieren  <br/> |Gibt eine Konfigurationsaktion an.  <br/> |
|Installieren Sie  <br/> |Gibt eine Installation Aktion an.  <br/> |
|Deinstallieren  <br/> |Gibt eine Deinstallation Aktion an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ClientExtension](clientextension.md) <br/> |Benutzer- und Konfigurationsdaten Informationen zu einer app enthält.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Aktionen (ArrayOfSetClientExtensionActionsType)](actions-arrayofsetclientextensionactionstype.md) <br/> |Gibt ein Array von **Action** -Elementen.  <br/> |
   
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

