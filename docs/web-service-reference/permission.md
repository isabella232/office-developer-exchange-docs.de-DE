---
title: Berechtigung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Permission
api_type:
- schema
ms.assetid: b8d0429a-0e58-4480-9847-4901970c7033
description: Das Permission-Element definiert den Zugriff, den ein Benutzer auf einen Ordner hat.
ms.openlocfilehash: bc3e140aaf7bd9ea7f1a4993c9bea1dcad8d39fa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512667"
---
# <a name="permission"></a>Berechtigung

Das **Permission-Element** definiert den Zugriff, den ein Benutzer auf einen Ordner hat. 
  
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

 **Permissiontype**
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
|[PermissionLevel](permissionlevel.md) <br/> |Stellt die Kombination von Berechtigungen dar, über die ein Benutzer für einen Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ReadItems (PermissionType)](readitems-permissiontype.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[UserId](userid.md) <br/> |Identifiziert einen Stellvertreterbenutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Berechtigungen](permissions.md) <br/> |Enthält alle konfigurierten Berechtigungen für einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Dieses Element wurde in Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
  
### <a name="version-differences"></a>Versionsunterschiede

Für Anwendungen, die auf Exchange Online abzielen, Exchange Online als Teil Office 365 oder eine lokale Version von Exchange ab Exchange 2013, werden Ordnerberechtigungen nicht zurückgegeben, wenn das [BaseShape-Element](baseshape.md) den Wert **AllProperties** in [GetFolder aufweist.](getfolder-operation.md) Vorgangsanforderung. Um Ordnerberechtigungen abzurufen, fügen Sie das [PermissionSet (PermissionSetType)-Element](permissionset-permissionsettype.md) dem [AdditionalProperties-Element](additionalproperties.md) in der **GetFolder-Anforderung** hinzu. 
  
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

