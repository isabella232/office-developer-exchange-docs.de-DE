---
title: Elemente (NonEmptyArrayOfUploadItemsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Items
api_type:
- schema
ms.assetid: 402bfa6d-11d7-4547-b8bd-197e9922ab49
description: Das Items-Element enthält ein Array von Elementen, die in ein Postfach hochgeladen werden sollen.
ms.openlocfilehash: 5c69134c1613b0a4595a6aa876fa09fde63043ea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44441548"
---
# <a name="items-nonemptyarrayofuploaditemstype"></a>Elemente (NonEmptyArrayOfUploadItemsType)

Das **Items** -Element enthält ein Array von Elementen, die in ein Postfach hochgeladen werden sollen. 
  
[UploadItems](uploaditems.md)
  
[Elemente (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md)
  
```XML
<Items>
   <Item/>
</Items>
```

 **NonEmptyArrayOfUploadItemsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Element (UploadItemType)](item-uploaditemtype.md) <br/> |Stellt ein einzelnes Element dar, das in ein Postfach hochgeladen werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UploadItems](uploaditems.md) <br/> |Stellt eine Anforderung zum Hochladen von Elementen in ein Postfach dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ExportItems-Vorgang](exportitems-operation.md)
  
[UploadItems-Vorgang](uploaditems-operation.md)

