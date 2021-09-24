---
title: CalendarPermission
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarPermission
api_type:
- schema
ms.assetid: 3aafb221-a04b-41f6-804e-eda810f1ba28
description: Das CalendarPermission-Element definiert den Zugriff, den ein Benutzer auf einen Kalenderordner hat. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 7794cab261653f8cb6421d4e0633d496ba347a5f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514802"
---
# <a name="calendarpermission"></a>CalendarPermission

Das **CalendarPermission-Element** definiert den Zugriff, den ein Benutzer auf einen Kalenderordner hat. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<Permission>
   <CalendarPermissionLevel/>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 **CalendarPermissionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarPermissionLevel](calendarpermissionlevel.md) <br/> |Stellt die Berechtigungsstufe dar, über die ein Benutzer in einem Kalenderordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[CanCreateItems](cancreateitems.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Unterordnern in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[DeleteItems](deleteitems.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Löschen von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[EditItems](edititems.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Bearbeiten von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |Gibt an, ob ein Benutzer ein Kontakt für einen Ordner ist. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |Gibt an, ob ein Benutzer der Besitzer eines Ordners ist. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |Gibt an, ob ein Benutzer einen Ordner anzeigen kann. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ReadItems (CalendarPermissionType)](readitems-calendarpermissiontype.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Kalenderordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[UserId](userid.md) <br/> |Identifiziert einen Stellvertreterbenutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarPermissions](calendarpermissions.md) <br/> |Enthält ein Array von Kalenderberechtigungen für einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
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



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

