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
description: Das Permission-Element definiert den Zugriff, den ein Benutzer verfügt in einen Ordner.
ms.openlocfilehash: 600d60f481c4f1d407c3a39ab65d6ddcf46d04e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830735"
---
# <a name="permission"></a>Berechtigung

Das **Permission** -Element definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. 
  
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
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |Gibt an, ob ein Benutzer die Berechtigung zum Erstellen von Unterordnern in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[DeleteItems](deleteitems.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Löschen von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[-Smarttagbereich](edititems.md) <br/> |Gibt an, ob ein Benutzer die Berechtigung zum Bearbeiten von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |Gibt an, ob ein Benutzer einen Kontakt für einen Ordner ist. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |Gibt an, ob ein Benutzer den Besitzer eines Ordners ist. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |Gibt an, ob ein Benutzer einen Ordner anzeigen kann. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[PermissionLevel](permissionlevel.md) <br/> |Stellt die Kombination von Berechtigungen, mit denen ein Benutzer für einen Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ReadItems (PermissionType)](readitems-permissiontype.md) <br/> |Gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Ordner verfügt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[Benutzer-ID](userid.md) <br/> |Identifiziert ein Stellvertreter oder ein Benutzer mit Zugriffsberechtigungen für Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Berechtigungen](permissions.md) <br/> |Enthält die konfigurierten Berechtigungen für einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Dieses Element wurde in Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
  
### <a name="version-differences"></a>Versionsunterschiede

Für Applikationen werden, Exchange Online abzielen, Exchange Online als Teil von Office 365 oder eine lokale Version von Exchange beginnend mit Exchange 2013 Ordnerberechtigungen nicht zurückgegeben, wenn das Element [BaseShape](baseshape.md) **AllProperties** Wert hat in der Anforderung [GetFolder](getfolder-operation.md) -Vorgang. Um Ordnerberechtigungen abzurufen, fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der Anforderung **GetFolder** die [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) -Element hinzu. 
  
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

