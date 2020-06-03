---
title: AlternatePublicFolderItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternatePublicFolderItemId
api_type:
- schema
ms.assetid: a67df9b9-8fdb-42de-b9c5-8377b71fa3d9
description: Das AlternatePublicFolderItemId-Element beschreibt einen Elementbezeichner für Öffentliche Ordner, der in ein anderes ID-Format konvertiert werden soll. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 11a9fafec78a9bd14e4d98982fd38954d45e4d1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464770"
---
# <a name="alternatepublicfolderitemid"></a>AlternatePublicFolderItemId

Das **AlternatePublicFolderItemId** -Element beschreibt einen Elementbezeichner für Öffentliche Ordner, der in ein anderes ID-Format konvertiert werden soll. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
- [ConvertId](convertid.md)
  
- [SourceIds](sourceids.md)
  
- [AlternatePublicFolderItemId](alternatepublicfolderitemid.md)
  
```xml
<AlternatePublicFolderItemId FolderId="" Format="" ItemId=""/>
```

 **AlternatePublicFolderItemIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|FolderId  <br/> |Gibt den öffentlichen Ordner an, der das Element für Öffentliche Ordner enthält. Dieses Attribut ist erforderlich.  <br/> |
|Format  <br/> |Gibt das Format an, das den zu konvertierenden Elementbezeichner für Öffentliche Ordner beschreibt. Dieses Attribut ist erforderlich.  <br/> |
|ItemId  <br/> |Bezeichner das Element des öffentlichen Ordners, das konvertiert werden soll. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="format-attribute-values"></a>Formatieren von Attributwerten

|**Wert**|**Beschreibung**|
|:-----|:-----|
|EwsLegacyId  <br/> |Beschreibt Bezeichner, die von Exchange Webdienste in der ersten Version von Exchange 2007 erstellt werden.  <br/> |
|EwsId  <br/> |Beschreibt Bezeichner, die von Exchange Webdienste ab Exchange 2007 SP1 erstellt werden.  <br/> |
|EntryId  <br/> |Beschreibt MAPI-IDs wie in der PR_ENTRYID-Eigenschaft.  <br/> |
|HexEntryId  <br/> |Beschreibt eine hexadezimal codierte Darstellung der PR_ENTRYID-Eigenschaft. Dies ist das Format der Ereignisbezeichner für den Verfügbarkeitskalender.  <br/> |
|StoreId  <br/> |Beschreibt Exchange-Informationsspeicher Bezeichner.  <br/> |
|OwaId  <br/> |Beschreibt einen Outlook Web Access Bezeichner.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Enthält die Quellbezeichner, die konvertiert werden sollen. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
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

