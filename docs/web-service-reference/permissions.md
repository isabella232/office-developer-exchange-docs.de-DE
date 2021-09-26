---
title: Berechtigungen
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Permissions
api_type:
- schema
ms.assetid: 2ba50bd9-819f-4e5f-a3bb-85a0a87d8a86
description: Das Permissions-Element enthält die Auflistung der Berechtigungen für einen Ordner.
ms.openlocfilehash: 079bd74def1d768b3c8406d8949dcaa3ac0a0baf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544829"
---
# <a name="permissions"></a>Berechtigungen

Das **Permissions-Element** enthält die Auflistung der Berechtigungen für einen Ordner. 
  
```XML
<Permissions>
   <Permission/>
</Permissions>
```

 **Permissiontype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Berechtigung](permission.md) <br/> |Definiert den Zugriff, den ein Delegat auf einen Ordner hat. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Enthält alle Berechtigungen, die für einen Ordner konfiguriert sind. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
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

