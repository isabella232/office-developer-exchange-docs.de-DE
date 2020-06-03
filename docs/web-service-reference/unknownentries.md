---
title: UnknownEntries
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownEntries
api_type:
- schema
ms.assetid: 107ec73e-083a-4956-9d37-33d4734cc157
description: Das UnknownEntries-Element enthält ein Array von unbekannten Berechtigungseinträgen, die nicht für den Active Directory Verzeichnisdienst aufgelöst werden können. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 68cb2518b895ca0a74e6b9ed649ee92b7502ab05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459419"
---
# <a name="unknownentries"></a>UnknownEntries

Das **UnknownEntries** -Element enthält ein Array von unbekannten Berechtigungseinträgen, die nicht für den Active Directory Verzeichnisdienst aufgelöst werden können. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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
|[PermissionSet (permissionsettype)](permissionset-permissionsettype.md) <br/> |Enthält alle Berechtigungen, die für einen Ordner konfiguriert sind. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[PermissionSet (CalendarPermissionSetType)](permissionset-calendarpermissionsettype.md) <br/> |Enthält alle Berechtigungen, die für einen Kalenderordner konfiguriert sind. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können unbekannte Einträge aus einem Ordner löschen, indem Sie den UpdateFolder-Vorgang mit dem [setfolderfield](setfolderfield.md) -Element verwenden. Die unbekannten Einträge werden gelöscht, wenn Sie das PermissionSet mithilfe der Option setfolderfield des UpdateFolder-Vorgangs zurücksetzen. Das Löschen einzelner Einträge wird von Exchange Webdienste nicht unterstützt. 
  
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

