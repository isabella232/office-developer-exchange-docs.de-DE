---
title: ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 9684c22c-29d4-4f7f-befc-8cd41da56d38
description: Das Convert-ID-Element definiert eine Anforderung zum Konvertieren von Element-und Ordner Bezeichnern zwischen unterstützten Exchange-Formaten. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: d421baf1f29fb59a8c6eb2b09e1fa0e8a38ffaa4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452538"
---
# <a name="convertid"></a>ConvertId

Das **Convert** -ID-Element definiert eine Anforderung zum Konvertieren von Element-und Ordner Bezeichnern zwischen unterstützten Exchange-Formaten. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<ConvertId DestinationFormat="">
   <SourceIds/>
</ConvertId>
```

 **ConvertIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**DestinationFormat** <br/> |Beschreibt das ID-Format, das für alle konvertierten Bezeichner zurückgegeben wird. Das DestinationFormat wird von der IdFormatType beschrieben.  <br/> |
   
#### <a name="destinationformat-attribute"></a>DestinationFormat-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**EwsLegacyId** <br/> |Stellt das ID-Format dar, das für Exchange Webdienste-Bezeichner verwendet wird, die in der ersten Version von Exchange 2007 bereitgestellt werden.  <br/> |
|**EwsId** <br/> |Stellt das ID-Format dar, das für Exchange Webdienste-IDs verwendet wird, die mit Exchange Server 2007 SP1 beginnen.  <br/> |
|**EntryID** <br/> |Stellt den MAPI-Bezeichner dar, wie in der PR_ENTRYID-Eigenschaft.  <br/> |
|**HexEntryId** <br/> |Stellt die Ereignis-ID für den Verfügbarkeitskalender dar. Dies ist eine hexadezimal codierte Darstellung der PR_ENTRYID-Eigenschaft.  <br/> |
|**StoreId** <br/> |Stellt den Exchange-Informationsspeicher Bezeichner dar.  <br/> |
|**OwaId** <br/> |Stellt das Outlook Web Access-ID-Format dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Enthält die Quellbezeichner, die konvertiert werden sollen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ConvertId-Vorgang](convertid-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Konvertieren von Bezeichnern](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

