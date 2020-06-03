---
title: Action (SetClientExtensionActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: Das Action-Element enthält die Aktion, die der Exchange-Server für eine APP ausführen sollte.
ms.openlocfilehash: 29579e26377edacb5fb0bb8406144eeb116b8d15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529686"
---
# <a name="action-setclientextensionactiontype"></a>Action (SetClientExtensionActionType)

Das **Action** -Element enthält die Aktion, die der Exchange-Server für eine APP ausführen sollte. 
  
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
|ActionId  <br/> |Gibt den Bezeichner der Aktion an. Dieses Attribut ist erforderlich.  <br/> |
|ExtensionID geändert  <br/> |Gibt den Bezeichner der Erweiterung an. Dieses Attribut ist optional.  <br/> |
   
#### <a name="actionid"></a>ActionId

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Konfigurieren  <br/> |Gibt eine Konfigurationsaktion an.  <br/> |
|Installieren  <br/> |Gibt eine Installationsaktion an.  <br/> |
|Uninstall  <br/> |Gibt eine Deinstallations Aktion an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Client Extension](clientextension.md) <br/> |Enthält Benutzer-und Konfigurationsinformationen zu einer App.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Actions (ArrayOfSetClientExtensionActionsType)](actions-arrayofsetclientextensionactionstype.md) <br/> |Gibt ein Array von **Action** -Elementen an.  <br/> |
   
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

