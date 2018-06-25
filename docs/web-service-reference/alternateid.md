---
title: AlternateId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternateId
api_type:
- schema
ms.assetid: 9c01fdc3-4adf-4e23-bc33-45d2a45ea08b
description: AlternateId-Element beschreibt einen Bezeichner für die Konvertierung in einer Anforderung und die Ergebnisse einer konvertierten-ID in der Antwort.
ms.openlocfilehash: e4d29087b63b52638dd93e4e3b643cdee39a5b97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757254"
---
# <a name="alternateid"></a>AlternateId

**AlternateId** -Element beschreibt einen Bezeichner für die Konvertierung in einer Anforderung und die Ergebnisse einer konvertierten-ID in der Antwort. 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 **AlternateIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Beschreibt den Quellbezeichner in einer Anforderung [ConvertId Vorgang](convertid-operation.md) und die Ziel-ID in eine Antwort [ConvertId Vorgang](convertid-operation.md) .  <br/> |
|Format  <br/> |Beschreibt das Format der Quelle in einer Anforderung [ConvertId Vorgang](convertid-operation.md) und das Zielformat in einer Antwort [ConvertId Vorgang](convertid-operation.md) . Das Zielformat wird vom **DestinationFormat** -Attribut des [ConvertId](convertid.md) -Elements in der Anforderung beschrieben. Dieses Attribut ist vom Typ **IdFormatType**.  <br/> |
|Postfach  <br/> |Beschreibt die Postfach der primäre Simple Mail Transfer Protocol (SMTP)-Adresse, die die Bezeichner übersetzen enthält.  <br/> |
|IsArchive  <br/> |Gibt an, ob der Bezeichner eines archivierten Elements oder Ordners darstellt. Der Wert **true** gibt an, dass der Bezeichner eines archivierten Elements oder Ordners darstellt. Dieses Attribut ist optional.  <br/> |
   
#### <a name="format-attribute-values"></a>Format-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|EwsLegacyId  <br/> |Beschreibt Bezeichner, die in der ursprünglich freigegebenen Version von Exchange 2007 von Exchange-Webdienste erstellt werden.  <br/> |
|EwsId  <br/> |Beschreibt Bezeichner, die von der Exchange-Webdienste beginnend mit Exchange 2007 SP1 erstellt werden.  <br/> |
|EntryId  <br/> |MAPI-IDs, wie in der **PR_ENTRYID** -Eigenschaft beschreibt.  <br/> |
|HexEntryId  <br/> |Beschreibt eine hexadezimal-codierte Darstellung der **PR_ENTRYID** -Eigenschaft. Dies ist das Format der Verfügbarkeit Kalender-Ereignis-IDs.  <br/> |
|StoreId  <br/> |Beschreibt die Exchange-Speicher-IDs.  <br/> |
|OwaId  <br/> |Beschreibt einen Outlook Web App-Bezeichner.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung [ConvertId Vorgang](convertid-operation.md) .  <br/> |
|[SourceIds](sourceids.md) <br/> |Enthält die Bezeichner der Quelle zu konvertieren.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

**AlternateId** -Element werden zwei Bezeichner, der Source-Bezeichner, der in der Anforderung [ConvertId Vorgang](convertid-operation.md) konvertiert werden soll und der konvertierten Bezeichner im [ConvertIdResponse](convertidresponse.md) -Element beschrieben. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

||||
|:-----|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ConvertId-Vorgang](convertid-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Konvertieren von Bezeichnern](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

