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
description: Das ConvertId-Element definiert eine Anforderung zum Element und Ordner Bezeichner zwischen Exchange-Formate konvertieren. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 956f6464fd9013f9e72d2915f21c3b011d0add5b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757709"
---
# <a name="convertid"></a>ConvertId

Das **ConvertId** -Element definiert eine Anforderung zum Element und Ordner Bezeichner zwischen Exchange-Formate konvertieren. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
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
|**DestinationFormat** <br/> |Beschreibt das ID-Format, das für alle konvertierten Bezeichner zurückgegeben wird. Die DestinationFormat wird durch die IdFormatType beschrieben.  <br/> |
   
#### <a name="destinationformat-attribute"></a>DestinationFormat-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**EwsLegacyId** <br/> |Stellt das ID-Format, das für Exchange-Webdienste-Bezeichner verwendet wird, die in der ursprünglich freigegebenen Version von Exchange 2007 bereitgestellt werden.  <br/> |
|**EwsId** <br/> |Stellt das ID-Format, das für Exchange-Webdienste-Bezeichner beginnend mit Exchange Server 2007 SP1 verwendet wird.  <br/> |
|**EntryId** <br/> |Stellt die MAPI-ID wie die PR_ENTRYID-Eigenschaft.  <br/> |
|**HexEntryId** <br/> |Stellt die Verfügbarkeit Kalender-Ereignis-ID an. Dies ist eine Hexadezimalzahl-codierte Darstellung der PR_ENTRYID-Eigenschaft.  <br/> |
|**StoreId** <br/> |Stellt den Exchange-Speicher-Bezeichner.  <br/> |
|**OwaId** <br/> |Stellt das Format von Outlook Web Access.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Enthält die Bezeichner der Quelle zu konvertieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ConvertId-Vorgang](convertid-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Konvertieren von Bezeichnern](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

