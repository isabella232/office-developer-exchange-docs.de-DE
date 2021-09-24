---
title: IndexedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IndexedFieldURI
api_type:
- schema
ms.assetid: 5c9cd0b5-7eca-480a-8730-fe98b1779afa
description: Das IndexedFieldURI -Element identifiziert einzelne Elemente eines Wörterbuchs.
ms.openlocfilehash: 851d0d4296e926ab21e5bd1b842d5a215c27308a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539626"
---
# <a name="indexedfielduri"></a>IndexedFieldURI

Das **IndexedFieldURI** -Element identifiziert einzelne Elemente eines Wörterbuchs. 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 **PathToIndexedFieldType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**FieldURI** <br/> |Identifiziert das Wörterbuch, das Element zurückzugebenden enthält. Dieses Attribut ist erforderlich.  <br/> |
|**FieldIndex** <br/> |Bezeichnet den Member des Wörterbuchs zurückgegeben. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="fielduri-attribute"></a>FieldURI Attribute

|**Wert**|**Beschreibung**|
|:-----|:-----|
|item:InternetMessageHeader  <br/> |Der Nachrichtenkopf eines Elements darstellt.  <br/> |
|contacts:ImAddress  <br/> |Stellt die Instant messaging-Adresse eines Kontakts an.  <br/> |
|contacts:PhysicalAddress:Street  <br/> |Stellt die Straße eines Kontakts an.  <br/> |
|contacts:PhysicalAddress:City  <br/> |Stellt den Ort eines Kontakts an.  <br/> |
|contacts:PhysicalAddress:State  <br/> |Stellt den Status eines Kontakts an.  <br/> |
|contacts:PhysicalAddress:Country  <br/> |Stellt das Land/Region eines Kontakts an.  <br/> |
|contacts:PhysicalAddress:PostalCode  <br/> |Stellt die Postleitzahl des Kontakts an.  <br/> |
|contacts:PhoneNumber  <br/> |Stellt die Rufnummer eines Kontakts an.  <br/> |
|contacts:EmailAddress  <br/> |Stellt die e-Mail-Adresse eines Kontakts an.  <br/> |
|DistributionList:Members:Member  <br/> |Stellt ein Element einer Verteilerliste dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdditionalProperties](additionalproperties.md) <br/> |Identifiziert zusätzliche Eigenschaften zum Abrufen, Festlegen oder Erstellen.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Stellt die Eigenschaft dar, die zum Ermitteln der Reihenfolge gruppierter Elemente für einen gruppierten FindItem-Ergebnissatz verwendet werden.  <br/> |
|[GroupBy](groupby.md) <br/> |Gibt eine beliebige Gruppierung für FindItem-Abfragen an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

