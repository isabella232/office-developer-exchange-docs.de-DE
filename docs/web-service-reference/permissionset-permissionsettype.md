---
title: PermissionSet (PermissionSetType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PermissionSet
api_type:
- schema
ms.assetid: 6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d
description: Das PermissionSet-Element enthält alle Berechtigungen, die für einen Ordner konfiguriert sind.
ms.openlocfilehash: b18fef33d3be6cb8c525f731a264860c3a83afdc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543142"
---
# <a name="permissionset-permissionsettype"></a>PermissionSet (PermissionSetType)

Das **PermissionSet-Element** enthält alle Berechtigungen, die für einen Ordner konfiguriert sind. 
  
```XML
<PermissionSet>
   <Permissions/>
   <UnknownEntries/>
</PermissionSet>
```

 **PermissionSetType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Berechtigungen](permissions.md) <br/> |Enthält die Auflistung der Berechtigungen für einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[UnknownEntries](unknownentries.md) <br/> |Enthält ein Array unbekannter Einträge, die nicht für den Active Directory-Verzeichnisdienst aufgelöst werden können. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Definiert einen Ordner zum Erstellen, Abrufen, Suchen, Synchronisieren oder Aktualisieren.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Stellt einen Suchordner dar, der in einem Postfach enthalten ist.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontaktordner dar, der in einem Postfach enthalten ist.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Aufgabenordner dar, der in einem Postfach enthalten ist.  <br/> |
   
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

