---
title: Berechtigung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Permission
api_type:
- schema
ms.assetid: b8d0429a-0e58-4480-9847-4901970c7033
description: Das Permission-Element definiert den Zugriff, den ein Benutzer in einen Ordner hat.
ms.openlocfilehash: 0f7515dbb06f8423f8d4d95e1391496e8ac73653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459258"
---
# <a name="permission"></a>Berechtigung

Das **Permission** -Element definiert den Zugriff, den ein Benutzer in einen Ordner hat. 
  
```XML
<Permission>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <PermissionLevel/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 **PermissionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CanCreateItems](cancreateitems.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Unterordnern in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[DeleteItems](deleteitems.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Löschen von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[EditItems](edititems.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Bearbeiten von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |Gibt an, ob ein Benutzer ein Kontakt für einen Ordner ist. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |Gibt an, ob ein Benutzer der Besitzer eines Ordners ist. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |Gibt an, ob ein Benutzer einen Ordner anzeigen kann. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[PermissionLevel](permissionlevel.md) <br/> |Stellt die Kombination von Berechtigungen dar, die ein Benutzer für einen Ordner hat. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ReadItems (PermissionType)](readitems-permissiontype.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[UserId](userid.md) <br/> |Identifiziert einen Stellvertreter Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Berechtigungen](permissions.md) <br/> |Enthält alle konfigurierten Berechtigungen für einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Dieses Element wurde in Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
  
### <a name="version-differences"></a>Versionsunterschiede

Für Anwendungen, die auf Exchange Online Zielen, Exchange Online im Rahmen von Office 365 oder einer lokalen Exchange-Version, die mit Exchange 2013 beginnt, werden Ordnerberechtigungen nicht zurückgegeben, wenn das [BaseShape](baseshape.md) -Element den Wert **allproperties** in der [GetFolder](getfolder-operation.md) -Vorgangsanforderung aufweist. Zum Abrufen von Ordnerberechtigungen fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der **GetFolder** -Anforderung das [PermissionSet-Element (permissionsettype)](permissionset-permissionsettype.md) hinzu. 
  
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

