---
title: UnknownEntries
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UnknownEntries
api_type:
- schema
ms.assetid: 107ec73e-083a-4956-9d37-33d4734cc157
description: Das UnknownEntries-Element enthält ein Array unbekannter Berechtigungseinträge, die nicht für den Active Directory-Verzeichnisdienst aufgelöst werden können. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 9ada724abbecddf192b5f345c1800ac38a8b41aa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514081"
---
# <a name="unknownentries"></a>UnknownEntries

Das **UnknownEntries-Element** enthält ein Array unbekannter Berechtigungseinträge, die nicht für den Active Directory-Verzeichnisdienst aufgelöst werden können. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<UnknownEntries>
   <UnknownEntry/>
</UnknownEntries>
```

 **ArrayOfUnknownEntriesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UnknownEntry](unknownentry.md) <br/> |Stellt einen einzelnen unbekannten Berechtigungseintrag dar, der nicht für Active Directory aufgelöst werden kann. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Enthält alle Berechtigungen, die für einen Ordner konfiguriert sind. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[PermissionSet (CalendarPermissionSetType)](permissionset-calendarpermissionsettype.md) <br/> |Enthält alle Berechtigungen, die für einen Kalenderordner konfiguriert sind. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können unbekannte Einträge aus einem Ordner löschen, indem Sie den UpdateFolder-Vorgang mit dem [SetFolderField-Element](setfolderfield.md) verwenden. Die unbekannten Einträge werden gelöscht, wenn Sie permissionSet mithilfe der Option "SetFolderField" des UpdateFolder-Vorgangs zurücksetzen. Exchange Webdienste unterstützen das Löschen einzelner Einträge nicht. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateFolder-Vorgang](updatefolder-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

