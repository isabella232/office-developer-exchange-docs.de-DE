---
title: AlternateId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AlternateId
api_type:
- schema
ms.assetid: 9c01fdc3-4adf-4e23-bc33-45d2a45ea08b
description: Das AlternateId-Element beschreibt einen Bezeichner, der in einer Anforderung konvertiert werden soll, und die Ergebnisse eines konvertierten Bezeichners in der Antwort.
ms.openlocfilehash: 6346a45b48eb811cac705d8da85dc77e6c18262c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520941"
---
# <a name="alternateid"></a>AlternateId

Das **AlternateId-Element** beschreibt einen Bezeichner, der in einer Anforderung konvertiert werden soll, und die Ergebnisse eines konvertierten Bezeichners in der Antwort. 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 **AlternateIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Beschreibt den Quellbezeichner in einer [ConvertId-Vorgangsanforderung](convertid-operation.md) und den Zielbezeichner in einer [ConvertId-Vorgangsantwort.](convertid-operation.md)  <br/> |
|Format  <br/> |Beschreibt das Quellformat in einer [ConvertId-Vorgangsanforderung](convertid-operation.md) und das Zielformat in einer [ConvertId-Vorgangsantwort.](convertid-operation.md) Das Zielformat wird durch das **DestinationFormat-Attribut** des [ConvertId-Elements](convertid.md) in der Anforderung beschrieben. Dieses Attribut ist vom Typ **IdFormatType**.  <br/> |
|Postfach  <br/> |Beschreibt die primäre SMTP-Adresse (Simple Mail Transfer Protocol) des Postfachs, die die zu übersetzenden Bezeichner enthält.  <br/> |
|IsArchive  <br/> |Gibt an, ob der Bezeichner ein archiviertes Element oder einen archivierten Ordner darstellt. Der Wert **"true"** gibt an, dass der Bezeichner ein archiviertes Element oder einen archivierten Ordner darstellt. Dieses Attribut ist optional.  <br/> |
   
#### <a name="format-attribute-values"></a>Formatattributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|EwsLegacyId  <br/> |Beschreibt Bezeichner, die von Exchange Webdiensten in der ersten Version von Exchange 2007 erstellt werden.  <br/> |
|EwsId  <br/> |Beschreibt Bezeichner, die von Exchange Webdiensten ab Exchange 2007 SP1 erstellt werden.  <br/> |
|EntryId  <br/> |Beschreibt MAPI-Bezeichner  wie in der PR_ENTRYID-Eigenschaft.  <br/> |
|HexEntryId  <br/> |Beschreibt eine hexadezimal codierte  Darstellung der PR_ENTRYID-Eigenschaft. Dies ist das Format von Verfügbarkeitskalender-Ereignisbezeichnern.  <br/> |
|StoreId  <br/> |Beschreibt Exchange Speicherbezeichner.  <br/> |
|OwaId  <br/> |Beschreibt einen Outlook Web App Bezeichner.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [ConvertId-Vorgangsanforderung.](convertid-operation.md)  <br/> |
|[SourceIds](sourceids.md) <br/> |Enthält die zu konvertierenden Quellbezeichner.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **AlternateId-Element** beschreibt zwei Bezeichner, den Quellbezeichner, der in der [ConvertId-Vorgangsanforderung](convertid-operation.md) konvertiert werden soll, und den konvertierten Bezeichner im [ConvertIdResponse-Element.](convertidresponse.md) 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

||||
|:-----|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ConvertId-Vorgang](convertid-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Konvertieren von Bezeichnern](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

