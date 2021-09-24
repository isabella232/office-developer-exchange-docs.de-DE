---
title: AlternatePublicFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AlternatePublicFolderId
api_type:
- schema
ms.assetid: 0a4dc1cc-959e-4b93-aa3a-3020ca8b8a02
description: Das AlternatePublicFolderId-Element beschreibt einen Bezeichner für öffentliche Ordner, der in ein anderes Bezeichnerformat konvertiert werden soll. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 7c4471c0c1e3e1eee3b47eba42f924340891c777
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525358"
---
# <a name="alternatepublicfolderid"></a>AlternatePublicFolderId

Das **AlternatePublicFolderId-Element** beschreibt einen Bezeichner für öffentliche Ordner, der in ein anderes Bezeichnerformat konvertiert werden soll. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
- [ConvertId](convertid.md)
  
- [SourceIds](sourceids.md)
  
- [AlternatePublicFolderId](alternatepublicfolderid.md)
  
```xml
<AlternatePublicFolderId FolderId="" Format="" />
```

 **AlternatePublicFolderIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|FolderId  <br/> |Enthält den zu konvertierenden Bezeichner für öffentliche Ordner. Dieses Attribut ist erforderlich.  <br/> |
|Format  <br/> |Gibt das Format an, das den zu konvertierenden Bezeichner für öffentliche Ordner beschreibt. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="format-attribute"></a>Format-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|EwsLegacyId  <br/> |Beschreibt Bezeichner, die von Exchange Webdiensten in der ersten Version von Exchange 2007 erstellt werden.  <br/> |
|EwsId  <br/> |Beschreibt Bezeichner, die von Exchange Webdiensten ab Exchange 2007 SP1 erstellt werden.  <br/> |
|EntryId  <br/> |Beschreibt MAPI-Bezeichner wie in der PR_ENTRYID-Eigenschaft.  <br/> |
|HexEntryId  <br/> |Beschreibt eine hexadezimal codierte Darstellung der PR_ENTRYID-Eigenschaft. Dies ist das Format von Verfügbarkeitskalender-Ereignisbezeichnern.  <br/> |
|StoreId  <br/> |Beschreibt Exchange Speicherbezeichner.  <br/> |
|OwaId  <br/> |Beschreibt einen Outlook Web Access-Bezeichner.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Enthält die zu konvertierenden Quellbezeichner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ConvertId-Vorgang](convertid-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Konvertieren von Bezeichnern](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

