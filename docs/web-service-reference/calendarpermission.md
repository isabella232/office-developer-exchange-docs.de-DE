---
title: CalendarPermission
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermission
api_type:
- schema
ms.assetid: 3aafb221-a04b-41f6-804e-eda810f1ba28
description: Das CalendarPermission-Element definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 7f6ceb6895add3fdd82cdd595463b3a80db822e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757533"
---
# <a name="calendarpermission"></a>CalendarPermission

Das **CalendarPermission** -Element definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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
|[CalendarPermissionLevel](calendarpermissionlevel.md) <br/> |Stellt die Berechtigungsstufe, die ein Benutzer für einen Kalenderordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[CanCreateItems](cancreateitems.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |Gibt an, ob ein Benutzer die Berechtigung zum Erstellen von Unterordnern in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[DeleteItems](deleteitems.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Löschen von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[-Smarttagbereich](edititems.md) <br/> |Gibt an, ob ein Benutzer die Berechtigung zum Bearbeiten von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |Gibt an, ob ein Benutzer einen Kontakt für einen Ordner ist. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |Gibt an, ob ein Benutzer den Besitzer eines Ordners ist. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |Gibt an, ob ein Benutzer einen Ordner anzeigen kann. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ReadItems (CalendarPermissionType)](readitems-calendarpermissiontype.md) <br/> |Gibt an, ob ein Benutzer über Berechtigungen zum Lesen von Elementen in einem Kalenderordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[Benutzer-ID](userid.md) <br/> |Identifiziert ein Stellvertreter oder ein Benutzer mit Zugriffsberechtigungen für Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarPermissions](calendarpermissions.md) <br/> |Enthält ein Array von Kalenderberechtigungen für einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
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



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

