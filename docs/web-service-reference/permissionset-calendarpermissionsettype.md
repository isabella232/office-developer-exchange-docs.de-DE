---
title: PermissionSet (CalendarPermissionSetType)
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
ms.assetid: 75f20033-85eb-4627-b4f8-be85e4889e96
description: Das PermissionSet-Element enthält alle Berechtigungen, die für einen Kalenderordner konfiguriert sind.
ms.openlocfilehash: 26351be8fd9fbe56ea5abb2dd346cb9c9458c463
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539153"
---
# <a name="permissionset-calendarpermissionsettype"></a>PermissionSet (CalendarPermissionSetType)

Das **PermissionSet-Element** enthält alle Berechtigungen, die für einen Kalenderordner konfiguriert sind. 
  
```XML
<PermissionSet>
   <CalendarPermissions/>
   <UnknownEntries/>
</PermissionSet>
```

 **CalendarPermissonSetType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarPermissions](calendarpermissions.md) <br/> |Enthält ein Array von Kalenderberechtigungen für einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[UnknownEntries](unknownentries.md) <br/> |Enthält ein Array unbekannter Einträge, die nicht für den Active Directory-Verzeichnisdienst aufgelöst werden können. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.  <br/> |
   
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

