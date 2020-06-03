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
description: Das Alternate-ID-Element beschreibt einen Bezeichner, der in einer Anforderung konvertiert werden soll, sowie die Ergebnisse eines konvertierten Bezeichners in der Antwort.
ms.openlocfilehash: 26df68bd814c2d323630c6bb40b4c31745017c71
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527453"
---
# <a name="alternateid"></a>AlternateId

Das **Alternate** -ID-Element beschreibt einen Bezeichner, der in einer Anforderung konvertiert werden soll, sowie die Ergebnisse eines konvertierten Bezeichners in der Antwort. 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 **AlternateIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Beschreibt den Quellbezeichner in einer [Konvertierungs](convertid-operation.md) -ID-Vorgangsanforderung und beschreibt den Zielbezeichner in einer [converto-Vorgangs](convertid-operation.md) Antwort.  <br/> |
|Format  <br/> |Beschreibt das Quellformat in einer Anforderung für den [Konvertierungsvorgang](convertid-operation.md) und beschreibt das Zielformat in einer [Convert-Vorgangs](convertid-operation.md) Antwort. Das Zielformat wird durch das **DestinationFormat** -Attribut des [Convert](convertid.md) -Elements in der Anforderung beschrieben. Dieses Attribut ist vom Typ **IdFormatType**.  <br/> |
|Postfach  <br/> |Beschreibt die primäre Simple Mail Transfer Protocol (SMTP) Adresse des Postfachs, die die zu übersetzenden Bezeichner enthält.  <br/> |
|IsArchive  <br/> |Gibt an, ob der Bezeichner ein archiviertes Element oder einen Ordner darstellt. Der Wert **true** gibt an, dass der Bezeichner ein archiviertes Element oder einen archivierten Ordner darstellt. Dieses Attribut ist optional.  <br/> |
   
#### <a name="format-attribute-values"></a>Formatieren von Attributwerten

|**Wert**|**Beschreibung**|
|:-----|:-----|
|EwsLegacyId  <br/> |Beschreibt Bezeichner, die von Exchange Webdienste in der ersten Version von Exchange 2007 erstellt werden.  <br/> |
|EwsId  <br/> |Beschreibt Bezeichner, die von Exchange Webdienste ab Exchange 2007 SP1 erstellt werden.  <br/> |
|EntryId  <br/> |Beschreibt MAPI-IDs wie in der **PR_ENTRYID** -Eigenschaft.  <br/> |
|HexEntryId  <br/> |Beschreibt eine hexadezimal codierte Darstellung der **PR_ENTRYID** -Eigenschaft. Dies ist das Format der Ereignisbezeichner für den Verfügbarkeitskalender.  <br/> |
|StoreId  <br/> |Beschreibt Exchange-Informationsspeicher Bezeichner.  <br/> |
|OwaId  <br/> |Beschreibt einen Outlook Web App Bezeichner.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [Konvertierungsvorgangs](convertid-operation.md) Anforderung.  <br/> |
|[SourceIds](sourceids.md) <br/> |Enthält die Quellbezeichner, die konvertiert werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das **Alternate** -ID-Element beschreibt zwei Bezeichner, den Quellbezeichner, der in der Anforderung für den [Konvertierungsvorgang](convertid-operation.md) konvertiert werden soll, und den konvertierten Bezeichner im [ConvertIdResponse](convertidresponse.md) -Element. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

||||
|:-----|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ConvertId-Vorgang](convertid-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Konvertieren von Bezeichnern](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

