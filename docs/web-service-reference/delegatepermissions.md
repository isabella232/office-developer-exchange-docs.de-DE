---
title: DelegatePermissions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DelegatePermissions
api_type:
- schema
ms.assetid: 292badc7-bab3-4368-9d7c-9a8b7edb279b
description: Das DelegatePermissions-Element enthält die Stellvertretungseinstellungen auf Berechtigungsebene für einen Benutzer. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: a8c7e06ae0ad4e1d12d06b559ad7d9f9468c4ade
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528992"
---
# <a name="delegatepermissions"></a>DelegatePermissions

Das **DelegatePermissions-Element** enthält die Stellvertretungseinstellungen auf Berechtigungsebene für einen Benutzer. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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
|[CalendarFolderPermissionLevel](calendarfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardordner "Kalender". Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[TasksFolderPermissionLevel](tasksfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardaufgabenordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[InboxFolderPermissionLevel](inboxfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardordner "Posteingang". Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ContactsFolderPermissionLevel](contactsfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardordner "Kontakte". Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[NotesFolderPermissionLevel](notesfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardordner "Notizen". Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[JournalFolderPermissionLevel](journalfolderpermissionlevel.md) <br/> |Enthält die Berechtigungen für den Standardordner "Journal". Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |Identifiziert einen einzelnen Delegaten, der in einem Postfach hinzugefügt oder aktualisiert werden soll. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
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

- [AddDelegate-Vorgang](adddelegate-operation.md) 
- [UpdateDelegate-Vorgang](updatedelegate-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Hinzufügen von Delegaten](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

