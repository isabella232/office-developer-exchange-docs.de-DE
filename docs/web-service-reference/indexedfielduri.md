---
title: IndexedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedFieldURI
api_type:
- schema
ms.assetid: 5c9cd0b5-7eca-480a-8730-fe98b1779afa
description: Das IndexedFieldURI -Element identifiziert einzelne Elemente eines Wörterbuchs.
ms.openlocfilehash: f794d9970590417d916925f7258b28d4f0920d0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467018"
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
|Element: InternetMessageHeader  <br/> |Der Nachrichtenkopf eines Elements darstellt.  <br/> |
|Kontakte: imaddresse  <br/> |Stellt die Instant messaging-Adresse eines Kontakts an.  <br/> |
|Kontakte: PhysicalAddress: Street  <br/> |Stellt die Straße eines Kontakts an.  <br/> |
|Kontakte: PhysicalAddress: City  <br/> |Stellt den Ort eines Kontakts an.  <br/> |
|Kontakte: PhysicalAddress: State  <br/> |Stellt den Status eines Kontakts an.  <br/> |
|Kontakte: PhysicalAddress: Country  <br/> |Stellt das Land/Region eines Kontakts an.  <br/> |
|Kontakte: PhysicalAddress: PostalCode  <br/> |Stellt die Postleitzahl des Kontakts an.  <br/> |
|Kontakte: Faxnummer  <br/> |Stellt die Rufnummer eines Kontakts an.  <br/> |
|Kontakte: Email Adressbuch  <br/> |Stellt die e-Mail-Adresse eines Kontakts an.  <br/> |
|DistributionList:Members:Member  <br/> |Stellt ein Element einer Verteilerliste dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdditionalProperties](additionalproperties.md) <br/> |Identifiziert zusätzliche Eigenschaften zum Abrufen, Festlegen oder Erstellen.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Stellt die Eigenschaft dar, die zum Ermitteln der Reihenfolge gruppierter Elemente für einen gruppierten FindItem-Ergebnissatz verwendet werden.  <br/> |
|[GroupBy](groupby.md) <br/> |Gibt eine beliebige Gruppierung für FindItem-Abfragen an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

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

