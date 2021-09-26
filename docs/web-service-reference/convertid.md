---
title: ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 9684c22c-29d4-4f7f-befc-8cd41da56d38
description: Das ConvertId-Element definiert eine Anforderung zum Konvertieren von Element- und Ordnerbezeichnern zwischen unterstützten Exchange Formaten. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: fe7d46697ba72ba6458136541488f5cd498169f4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545559"
---
# <a name="convertid"></a>ConvertId

Das **ConvertId-Element** definiert eine Anforderung zum Konvertieren von Element- und Ordnerbezeichnern zwischen unterstützten Exchange Formaten. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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
|**DestinationFormat** <br/> |Beschreibt das Bezeichnerformat, das für alle konvertierten Bezeichner zurückgegeben wird. Das DestinationFormat wird von IdFormatType beschrieben.  <br/> |
   
#### <a name="destinationformat-attribute"></a>DestinationFormat-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**EwsLegacyId** <br/> |Stellt das Bezeichnerformat dar, das für Exchange Webdienstbezeichner verwendet wird, die in der ersten Version von Exchange 2007 bereitgestellt werden.  <br/> |
|**EwsId** <br/> |Stellt das Bezeichnerformat dar, das für Exchange Webdienstbezeichner ab Exchange Server 2007 SP1 verwendet wird.  <br/> |
|**EntryId** <br/> |Stellt den MAPI-Bezeichner wie in der PR_ENTRYID-Eigenschaft dar.  <br/> |
|**HexEntryId** <br/> |Stellt den Ereignisbezeichner des Verfügbarkeitskalenders dar. Dies ist eine hexadezimal codierte Darstellung der PR_ENTRYID-Eigenschaft.  <br/> |
|**Storeid** <br/> |Stellt den Exchange Speicherbezeichner dar.  <br/> |
|**OwaId** <br/> |Stellt das Outlook Web Access-Bezeichnerformat dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Enthält die zu konvertierenden Quellbezeichner.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ConvertId-Vorgang](convertid-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Konvertieren von Bezeichnern](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

