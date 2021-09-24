---
title: ExtendedProperty (PathToExtendedFieldType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fa620b48-2ce3-437d-b51e-541247eea1d9
description: Das ExtendedProperty-Element gibt eine erweiterte Eigenschaft für die Unified Contact-Store an.
ms.openlocfilehash: 5cb320e15d3a01c542907048357d1ef0cc78f96a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530759"
---
# <a name="extendedproperty-pathtoextendedfieldtype"></a>ExtendedProperty (PathToExtendedFieldType)

Das **ExtendedProperty-Element** gibt eine erweiterte Eigenschaft für die Unified Contact-Store an. 
  
```xml
<ExtendedProperty DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" FieldURI="">
</ExtendedProperty>
```

**PathToExtendedFieldType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|DistinguishedPropertySetId  <br/> |Gibt den Bezeichner des definierten Eigenschaftensatzes an. Dieses Attribut ist optional.  <br/> |
|PropertySetId  <br/> |Gibt den GUID-Eigenschaftensatzbezeichner an. Dieses Attribut ist optional.  <br/> |
|PropertyTag  <br/> | Stellt das Eigenschaftstag ohne den Typteil dar.<br/><br/>Es gibt zwei Optionen für die Darstellung:  <br/><br/>- Hexadezimal: 0x3fa4  <br/>- Dezimal: 0-65535<br/><br/>  Dieses Attribut ist optional.  <br/> |
|PropertyName  <br/> |Zeichenfolge, die den Eigenschaftennamen angibt. Dieses Attribut ist optional.  <br/> |
|PropertyId  <br/> |Ganze Zahl, die den Eigenschaftsbezeichner angibt. Dieses Attribut ist optional.  <br/> |
|Propertytype  <br/> |Gibt den Eigenschaftstyp an. Dieses Attribut ist erforderlich.  <br/> |
|FieldURI  <br/> |Gibt das Feld Uniform Resource Identifier (URI) an. Dieses Attribut ist erforderlich. Mögliche Werte finden Sie im [FieldURI-Element.](fielduri.md)  <br/> |
   
#### <a name="distinguishedpropertysetid"></a>DistinguishedPropertySetId

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Besprechung  <br/> |Gibt eine Besprechung an.  <br/> |
|Termin  <br/> |Gibt einen Termin an.  <br/> |
|Standard  <br/> |Gibt den allgemeinen Eigenschaftensatz an.  <br/> |
|PublicStrings  <br/> |Gibt öffentliche Zeichenfolgen an.  <br/> |
|Adresse  <br/> |Gibt eine Adresse an.  <br/> |
|InternetHeaders  <br/> |Gibt Internetheader an.  <br/> |
|CalendarAssistant  <br/> |Gibt den Kalender-Assistenten an.  <br/> |
|UnifiedMessaging  <br/> |Gibt Unified Messaging an.  <br/> |
|Aufgabe  <br/> |Gibt einen Vorgang an.  <br/> |
   
#### <a name="propertytype"></a>Propertytype

|**Wert**|**Beschreibung**|
|:-----|:-----|
|ApplicationTime  <br/> |Gibt die Anwendungszeit an.  <br/> |
|ApplicationTimeArray  <br/> |Gibt ein Array von Anwendungszeiten an.  <br/> |
|Binär  <br/> |Gibt einen binären Wert an.  <br/> |
|BinaryArray  <br/> |Gibt ein Array von binären Werten an.  <br/> |
|Boolesch  <br/> |Gibt einen booleschen Wert an.  <br/> |
|CLSID  <br/> |Gibt eine CLSID an.  <br/> |
|CLSIDArray  <br/> |Gibt ein Array von CLSIDs an.  <br/> |
|Währung  <br/> |Gibt einen Währungswert an.  <br/> |
|CurrencyArray  <br/> |Gibt ein Array von Währungswerten an.  <br/> |
|Gleitkommawert mit doppelter Genauigkeit  <br/> |Gibt einen **doppelten** Wert an.  <br/> |
|DoubleArray  <br/> |Gibt ein Array mit **doppelten** Werten an.  <br/> |
|Fehler  <br/> |Gibt einen Fehler an. Dies dient der Fehlerberichterstattung. Sie kann nicht in Einschränkungen oder zum Abrufen oder Festlegen von Werten verwendet werden.  <br/> |
|Gleitkommazahl  <br/> |Gibt einen **Float -Wert an.**  <br/> |
|FloatArray  <br/> |Gibt ein Array von **Float-Werten** an.  <br/> |
|Ganze Zahl  <br/> |Gibt eine ganze Zahl an.  <br/> |
|IntegerArray  <br/> |Gibt ein Array von ganzen Zahlen an.  <br/> |
|Long  <br/> |Gibt eine **lange** an.  <br/> |
|LongArray  <br/> |Gibt ein Array **mit langen** Werten an.  <br/> |
|Null  <br/> |Gibt einen NULL-Wert an. Dies dient der Fehlerberichterstattung. Sie kann nicht in Einschränkungen oder zum Abrufen oder Festlegen von Werten verwendet werden.  <br/> |
|Objekt  <br/> |Gibt ein Objekt an. Dies dient der Fehlerberichterstattung. Sie kann nicht in Einschränkungen oder zum Abrufen oder Festlegen von Werten verwendet werden.  <br/> |
|ObjectArray  <br/> |Gibt ein Array von Objekten an. Dies dient der Fehlerberichterstattung. Sie kann nicht in Einschränkungen oder zum Abrufen oder Festlegen von Werten verwendet werden.  <br/> |
|Kurz  <br/> |Gibt eine **kurze** an.  <br/> |
|ShortArray  <br/> |Gibt ein Array von **Kurzwerten** an.  <br/> |
|Systemtime  <br/> |Gibt einen Systemzeitwert an.  <br/> |
|SystemTimeArray  <br/> |Gibt ein Array von Systemzeitwerten an.  <br/> |
|String  <br/> |Gibt eine Zeichenfolge an.  <br/> |
|StringArray  <br/> |Gibt ein Array von Zeichenfolgen an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies an extended MAPI property.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

