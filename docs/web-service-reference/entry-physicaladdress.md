---
title: Eintrag (physikalische Adresse)
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
description: Entry-Element wird eine einzelne physische Adresse für ein Kontaktelement beschrieben.
ms.openlocfilehash: 4551e6117e5f91d901fe160f37e8f67cb1bc5ac7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758253"
---
# <a name="entry-physicaladdress"></a>Eintrag (physikalische Adresse)

**Entry** -Element wird eine einzelne physische Adresse für ein Kontaktelement beschrieben. 
  
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
|**Key** <br/> | Eine physische Adresse identifiziert.<br/><br/> Es folgen die möglichen Werte für dieses Attribut.<br/>  <br/>-Business  <br/>-Startseite  <br/>-Andere  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Straße](street.md) <br/> |Stellt eine Adresse für ein Kontaktelement.  <br/> |
|[City](city.md) <br/> |Stellt den Namen der Stadt, der einem Kontakt zugeordnet ist.  <br/> |
|[State](state-ex15websvcsotherref.md) <br/> |Stellt den Zustand des US-Bundesstaates, ein Kontaktelement.  <br/> |
|[CountryOrRegion](countryorregion.md) <br/> |Stellt das Land oder die Region für eine bestimmte physische Adresse.  <br/> |
|[PostalCode](postalcode.md) <br/> |Stellt die Postleitzahl für ein Kontaktelement.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PhysicalAddresses](physicaladdresses.md) <br/> |Enthält eine Auflistung von physischen Adressen, die mit einem Kontakt verknüpft sind.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [Aktualisierung von Kontakten](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [Deleting Contacts](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

