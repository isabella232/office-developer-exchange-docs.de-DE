---
title: Eintrag (PhysicalAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: 9e5b6515-453e-4f4c-b55e-6ffefe23c31b
description: Das Entry-Element beschreibt eine einzelne physikalische Adresse für ein Kontaktelement.
ms.openlocfilehash: 5e8343e9abebeeff8c2b81327b2e0f4ddcf45364
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459630"
---
# <a name="entry-physicaladdress"></a>Eintrag (PhysicalAddress)

Das **Entry** -Element beschreibt eine einzelne physikalische Adresse für ein Kontaktelement. 
  
```xml
<Entry Key="">
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
</Entry>
```

 **PhysicalAddressDictionaryEntryType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Key** <br/> | Identifiziert eine physikalische Adresse.<br/><br/> Es folgen die möglichen Werte für dieses Attribut.<br/>  <br/>-Business  <br/>-Startseite  <br/>-Sonstiges  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Straße](street.md) <br/> |Stellt eine Straßenadresse für ein Kontaktelement dar.  <br/> |
|[City](city.md) <br/> |Stellt den Namen der Stadt dar, die einem Kontakt zugeordnet ist.  <br/> |
|[State](state-ex15websvcsotherref.md) <br/> |Stellt den Wohnsitzstatus für ein Kontaktelement dar.  <br/> |
|[CountryOrRegion](countryorregion.md) <br/> |Stellt das Land oder die Region für eine bestimmte physikalische Adresse dar.  <br/> |
|[PostalCode](postalcode.md) <br/> |Stellt die Postleitzahl für ein Kontaktelement dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PhysicalAddresses](physicaladdresses.md) <br/> |Enthält eine Auflistung von physikalischen Adressen, die einem Kontakt zugeordnet sind.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [Aktualisieren von Kontakten](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [Deleting Contacts](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

