---
title: JournalFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- JournalFolderPermissionLevel
api_type:
- schema
ms.assetid: 564525fa-cd95-4c1a-9d6c-3806be664579
description: Das JournalFolderPermissionLevel-Element enthält die Berechtigungen für den standardmäßigen Journal Ordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 5c0f30932eb3fbbeef1a8e34611deeb1ffef402c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529049"
---
# <a name="journalfolderpermissionlevel"></a>JournalFolderPermissionLevel

Das **JournalFolderPermissionLevel** -Element enthält die Berechtigungen für den standardmäßigen Journal Ordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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
|[DelegatePermissions](delegatepermissions.md) <br/> |Enthält die Einstellungen für die Stell Vertretungs Berechtigungsstufe für einen Benutzer. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die Textwerte aufgeführt, die die Berechtigungsstufen darstellen.
  
**Text Werte für Berechtigungsstufen**

|**Berechtigungsstufe**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Der Stellvertreter Benutzer verfügt über keine Zugriffsberechtigungen für den Ordner Journal.  <br/> |
|Reviewer  <br/> |Der Stellvertreter-Benutzer kann Elemente im Journal Ordner lesen.  <br/> |
|Ursprung  <br/> |Der Stellvertreter Benutzer kann Elemente im Journal Ordner lesen und erstellen.  <br/> |
|Editor  <br/> |Der Stellvertreter Benutzer kann Elemente im Journal Ordner lesen, erstellen und ändern.  <br/> |
|Benutzerdefiniert  <br/> |Der Stellvertreter Benutzer verfügt über benutzerdefinierte Zugriffsberechtigungen für den Ordner Journal.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

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


[Hinzufügen von Stellvertretungen](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

