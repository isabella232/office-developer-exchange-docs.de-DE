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
description: Das UnknownEntries-Element enthält ein Array von unbekannten Berechtigungseinträge, die gegen den Verzeichnisdienst Active Directory nicht aufgelöst werden kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 306e5f226a56694bb1ff32362f77e7dff80865ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839320"
---
# <a name="unknownentries"></a>UnknownEntries

Das **UnknownEntries** -Element enthält ein Array von unbekannten Berechtigungseinträge, die gegen den Verzeichnisdienst Active Directory nicht aufgelöst werden kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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
|[UnknownEntry](unknownentry.md) <br/> |Stellt einen einzelnen unbekannte Berechtigungseintrag, der anhand von Active Directory nicht aufgelöst werden kann. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Enthält alle Berechtigungen, die für einen Ordner konfiguriert sind. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[PermissionSet (CalendarPermissionSetType)](permissionset-calendarpermissionsettype.md) <br/> |Enthält alle Berechtigungen, die für einen Kalenderordner konfiguriert sind. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können unbekannte Einträge aus einem Ordner mit der UpdateFolder-Operation mit dem [SetFolderField](setfolderfield.md) Element löschen. Die unbekannte Einträge werden gelöscht, wenn Sie mithilfe der Option SetFolderField des Vorgangs UpdateFolder PermissionSet zurücksetzen. Exchange-Webdienste unterstützt nicht das Löschen der einzelnen Einträge. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateFolder-Vorgang](updatefolder-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

