---
title: DelegatePermissions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegatePermissions
api_type:
- schema
ms.assetid: 292badc7-bab3-4368-9d7c-9a8b7edb279b
description: Das DelegatePermissions-Element enthält die Stellvertretung Berechtigungsstufe Einstellungen für einen Benutzer. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 319592b6c3386a07b3094115c335c7fb8ffe1130
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757892"
---
# <a name="delegatepermissions"></a>DelegatePermissions

Das **DelegatePermissions** -Element enthält die Stellvertretung Berechtigungsstufe Einstellungen für einen Benutzer. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<DelegatePermissions>
   <CalendarFolderPermissionLevel/>
   <TasksFolderPermissionLevel/>
   <InboxFolderPermissionLevel/>
   <ContactsFolderPermissionLevel/>
   <NotesFolderPermissionLevel/>
   <JournalFolderPermissionLevel/>
</DelegatePermissions>
```

**DelegatePermissionsType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarFolderPermissionLevel](calendarfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardordner Kalender. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[TasksFolderPermissionLevel](tasksfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardordner für den Vorgang. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[InboxFolderPermissionLevel](inboxfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardordner Posteingang. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ContactsFolderPermissionLevel](contactsfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardordner Kontakte. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[NotesFolderPermissionLevel](notesfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardordner Notizen. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[JournalFolderPermissionLevel](journalfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardordner Journal. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Beauftragte Benutzer](delegateuser.md) <br/> |Identifiziert einen einzelnen Delegaten hinzufügen oder aktualisieren in einem Postfach. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [AddDelegate-Vorgang](adddelegate-operation.md) 
- [UpdateDelegate-Vorgang](updatedelegate-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Hinzufügen von Stellvertretungen](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

