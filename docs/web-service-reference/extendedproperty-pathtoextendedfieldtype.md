---
title: ExtendedProperty (PathToExtendedFieldType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa620b48-2ce3-437d-b51e-541247eea1d9
description: Das ExtendedProperty-Element gibt eine erweiterte Eigenschaft für den einheitlichen Kontaktspeicher.
ms.openlocfilehash: 7541fa6330ee96f7791febfabc672dbcf0e95b54
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758361"
---
# <a name="extendedproperty-pathtoextendedfieldtype"></a>ExtendedProperty (PathToExtendedFieldType)

Das **ExtendedProperty** -Element gibt eine erweiterte Eigenschaft für den einheitlichen Kontaktspeicher. 
  
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
|DistinguishedPropertySetId  <br/> |Gibt die distinguished Eigenschaftensatz-Bezeichner an. Dieses Attribut ist optional.  <br/> |
|PropertySetId  <br/> |Gibt die GUID-Eigenschaft Set Identifier an. Dieses Attribut ist optional.  <br/> |
|' PropertyTag '  <br/> | Stellt das Eigenschafts-Tag abzüglich der Teil des Typs.<br/><br/>Es gibt zwei Optionen für die Darstellung:  <br/><br/>-Hexadezimale: 0x3fa4  <br/>-Decimal: zwischen 0 und 65535<br/><br/>  Dieses Attribut ist optional.  <br/> |
|PropertyName  <br/> |String-Wert, der der Name der Eigenschaft angibt. Dieses Attribut ist optional.  <br/> |
|PropertyId  <br/> |Integer-Wert, der den Eigenschaftenbezeichner angibt. Dieses Attribut ist optional.  <br/> |
|PropertyType  <br/> |Gibt den Eigenschaftstyp an. Dieses Attribut ist erforderlich.  <br/> |
|FieldURI  <br/> |Gibt das Feld Uniform Resource Identifier (URI). Dieses Attribut ist erforderlich. Mögliche Werte finden Sie unter [FieldURI](fielduri.md) -Element.  <br/> |
   
#### <a name="distinguishedpropertysetid"></a>DistinguishedPropertySetId

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Besprechung  <br/> |Gibt eine Besprechung an.  <br/> |
|Appointment  <br/> |Gibt einen Termin an.  <br/> |
|Common  <br/> |Gibt den allgemeinen Eigenschaftensatz an.  <br/> |
|PublicStrings  <br/> |Gibt an, öffentliche Zeichenfolgen.  <br/> |
|Adresse  <br/> |Gibt eine Adresse an.  <br/> |
|InternetHeaders  <br/> |Gibt die Internetkopfzeilen an.  <br/> |
|CalendarAssistant  <br/> |Gibt den Kalender-Assistenten an.  <br/> |
|Unified Messaging  <br/> |Gibt an, Unified Messaging.  <br/> |
|Aufgabe  <br/> |Gibt eine Aufgabe.  <br/> |
   
#### <a name="propertytype"></a>PropertyType

|**Wert**|**Beschreibung**|
|:-----|:-----|
|ApplicationTime  <br/> |Gibt den Zeitpunkt der Anwendung.  <br/> |
|ApplicationTimeArray  <br/> |Gibt ein Array wie oft die Anwendung an.  <br/> |
|Binary  <br/> |Gibt einen Binärwert an.  <br/> |
|BinaryArray  <br/> |Gibt ein Array von binären Werten an.  <br/> |
|Boolean  <br/> |Gibt einen booleschen Wert an.  <br/> |
|CLSID  <br/> |Gibt eine CLSID an.  <br/> |
|CLSIDArray  <br/> |Gibt ein Array von CLSIDs an.  <br/> |
|Währung  <br/> |Gibt einen Währungswert an.  <br/> |
|CurrencyArray  <br/> |Gibt ein Array von Währungswerten an.  <br/> |
|Double  <br/> |Gibt einen **double**an.  <br/> |
|DoubleArray  <br/> |Gibt ein Array von **double** -Werte an.  <br/> |
|Fehler  <br/> |Gibt einen Fehler an. Dies ist für die Fehlerberichterstattung Zwecke. Es kann nicht in Einschränkungen oder zum Abrufen oder Festlegen von Werten verwendet werden.  <br/> |
|Gleitkomma  <br/> |Gibt ein **Float**an.  <br/> |
|FloatArray  <br/> |Gibt ein Array von **Float** -Werte an.  <br/> |
|Ganzzahl  <br/> |Gibt eine ganze Zahl an.  <br/> |
|IntegerArray  <br/> |Gibt ein Array mit ganzen Zahlen.  <br/> |
|Long  <br/> |Gibt einen **long**an.  <br/> |
|LongArray  <br/> |Gibt ein Array von **long** -Werte an.  <br/> |
|Null  <br/> |Gibt einen null-Wert an. Dies ist für die Fehlerberichterstattung Zwecke. Es kann nicht in Einschränkungen oder zum Abrufen oder Festlegen von Werten verwendet werden.  <br/> |
|Objekt  <br/> |Gibt ein Objekt an. Dies ist für die Fehlerberichterstattung Zwecke. Es kann nicht in Einschränkungen oder zum Abrufen oder Festlegen von Werten verwendet werden.  <br/> |
|ObjectArray  <br/> |Gibt ein Array von Objekten an. Dies ist für die Fehlerberichterstattung Zwecke. Es kann nicht in Einschränkungen oder zum Abrufen oder Festlegen von Werten verwendet werden.  <br/> |
|Kurz  <br/> |Gibt einen **kurzen**an.  <br/> |
|ShortArray  <br/> |Gibt ein Array von **kurzen** Werte an.  <br/> |
|SystemTime  <br/> |Gibt einen Zeitwert System an.  <br/> |
|SystemTimeArray  <br/> |Gibt ein Array von Zeitwerte System an.  <br/> |
|String  <br/> |Gibt eine Zeichenfolge an.  <br/> |
|StringArray  <br/> |Gibt ein Array von Zeichenfolgen an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifiziert eine erweiterte MAPI-Eigenschaft.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

