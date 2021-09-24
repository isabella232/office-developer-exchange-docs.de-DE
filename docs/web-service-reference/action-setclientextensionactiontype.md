---
title: Aktion (SetClientExtensionActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: Das Action-Element enthält die Aktion, die der Exchange-Server für eine App ausführen soll.
ms.openlocfilehash: a0f5c2743ef976db2faddbb7509a8a015ef4dd8f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510379"
---
# <a name="action-setclientextensionactiontype"></a>Aktion (SetClientExtensionActionType)

Das  Action-Element enthält die Aktion, die der Exchange-Server für eine App ausführen soll. 
  
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
|ExtensionId  <br/> |Gibt den Bezeichner der Erweiterung an. Dieses Attribut ist optional.  <br/> |
   
#### <a name="actionid"></a>ActionId

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Konfigurieren  <br/> |Gibt eine Konfigurationsaktion an.  <br/> |
|Installieren  <br/> |Gibt eine Installationsaktion an.  <br/> |
|Deinstallieren  <br/> |Gibt eine Deinstallationsaktion an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ClientExtension](clientextension.md) <br/> |Enthält Benutzer- und Konfigurationsinformationen zu einer App.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Aktionen (ArrayOfSetClientExtensionActionsType)](actions-arrayofsetclientextensionactionstype.md) <br/> |Gibt ein Array von **Aktionselementen** an.  <br/> |
   
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

