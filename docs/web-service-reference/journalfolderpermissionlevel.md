---
title: JournalFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- JournalFolderPermissionLevel
api_type:
- schema
ms.assetid: 564525fa-cd95-4c1a-9d6c-3806be664579
description: Das JournalFolderPermissionLevel-Element enthält die Berechtigungen für den Standardordner Journal. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 0237048e61fbae12a1341cef33e5ca30ebc0c838
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524966"
---
# <a name="journalfolderpermissionlevel"></a>JournalFolderPermissionLevel

Das **JournalFolderPermissionLevel-Element** enthält die Berechtigungen für den Standardordner Journal. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<JournalFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</JournalFolderPermissionLevel>
```

 **DelegateFolderPermissionLevelType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DelegatePermissions](delegatepermissions.md) <br/> |Enthält die Einstellungen für die Stellvertretungsberechtigungsstufe für einen Benutzer. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die Textwerte aufgeführt, die die Berechtigungsstufen darstellen.
  
**Textwerte auf Berechtigungsebene**

|**Berechtigungsstufe**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Der Stellvertretungsbenutzer hat keine Zugriffsberechtigungen für den Journalordner.  <br/> |
|Reviewer  <br/> |Der Stellvertretungsbenutzer kann Elemente im Journalordner lesen.  <br/> |
|Ursprung  <br/> |Der Stellvertretungsbenutzer kann Elemente im Journalordner lesen und erstellen.  <br/> |
|Editor  <br/> |Der Stellvertretungsbenutzer kann Elemente im Journalordner lesen, erstellen und ändern.  <br/> |
|Benutzerdefiniert  <br/> |Der Stellvertretungsbenutzer verfügt über benutzerdefinierte Zugriffsberechtigungen für den Journalordner.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AddDelegate-Vorgang](adddelegate-operation.md)
  
[UpdateDelegate-Vorgang](updatedelegate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Hinzufügen von Delegaten](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

