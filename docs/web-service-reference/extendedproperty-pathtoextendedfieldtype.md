---
title: Extended (pathtoextendedfieldtype Schematyp)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa620b48-2ce3-437d-b51e-541247eea1d9
description: Das Extended-Element gibt eine erweiterte Eigenschaft für den einheitlichen Kontaktspeicher an.
ms.openlocfilehash: f6c283d5cce3bc927662ad0d9c796c0589e7054c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460141"
---
# <a name="extendedproperty-pathtoextendedfieldtype"></a>Extended (pathtoextendedfieldtype Schematyp)

Das **Extended** -Element gibt eine erweiterte Eigenschaft für den einheitlichen Kontaktspeicher an. 
  
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
|DistinguishedPropertySetId  <br/> |Gibt die Distinguished Property Sets-ID an. Dieses Attribut ist optional.  <br/> |
|PropertySetId  <br/> |Gibt die GUID-Eigenschaftengruppe-ID an. Dieses Attribut ist optional.  <br/> |
|PropertyTag  <br/> | Stellt das Eigenschaften-Tag minus dem Typ Part dar.<br/><br/>Es gibt zwei Optionen für die Darstellung:  <br/><br/>-Hexadezimal: 0x3fa4  <br/>-Dezimalzahl: 0-65535<br/><br/>  Dieses Attribut ist optional.  <br/> |
|PropertyName  <br/> |Zeichenfolge, die den Namen der Eigenschaft angibt. Dieses Attribut ist optional.  <br/> |
|PropertyId  <br/> |Ganze Zahl, die den Eigenschaftenbezeichner angibt. Dieses Attribut ist optional.  <br/> |
|PropertyType  <br/> |Gibt den Typ der Eigenschaft an. Dieses Attribut ist erforderlich.  <br/> |
|FieldURI  <br/> |Gibt den URI (Uniform Resource Identifier) des Felds an. Dieses Attribut ist erforderlich. Informationen zu möglichen Werten finden Sie unter dem [FieldURI](fielduri.md) -Element.  <br/> |
   
#### <a name="distinguishedpropertysetid"></a>DistinguishedPropertySetId

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Besprechung  <br/> |Gibt eine Besprechung an.  <br/> |
|Termin  <br/> |Gibt einen Termin an.  <br/> |
|Standard  <br/> |Gibt die allgemeine Eigenschaftengruppe an.  <br/> |
|PublicStrings  <br/> |Gibt öffentliche Zeichenfolgen an.  <br/> |
|Adresse  <br/> |Gibt eine Adresse an.  <br/> |
|InternetHeaders  <br/> |Gibt Internet Kopfzeilen an.  <br/> |
|CalendarAssistant  <br/> |Gibt den Kalender-Assistenten an.  <br/> |
|UnifiedMessaging  <br/> |Gibt Unified Messaging an.  <br/> |
|Vorgang  <br/> |Gibt eine Aufgabe an.  <br/> |
   
#### <a name="propertytype"></a>PropertyType

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Anwendungs Zeitprogramme  <br/> |Gibt die Anwendungszeit an.  <br/> |
|ApplicationTimeArray  <br/> |Gibt ein Array von Anwendungszeiten an.  <br/> |
|Binär  <br/> |Gibt einen binären Wert an.  <br/> |
|BinaryArray  <br/> |Gibt ein Array von binären Werten an.  <br/> |
|Boolean  <br/> |Gibt einen booleschen Wert an.  <br/> |
|CLSID  <br/> |Gibt eine CLSID an.  <br/> |
|CLSIDArray  <br/> |Gibt ein Array von CLSIDs an.  <br/> |
|Währung  <br/> |Gibt einen Währungswert an.  <br/> |
|CurrencyArray  <br/> |Gibt ein Array von Währungswerten an.  <br/> |
|Gleitkommawert mit doppelter Genauigkeit  <br/> |Gibt einen **Double**-Wert an.  <br/> |
|Double Array  <br/> |Gibt ein Array von **Double** -Werten an.  <br/> |
|Fehler (ungefährer Wortlaut)  <br/> |Gibt einen Fehler an. Dies ist für Fehler Berichterstattungs Zwecke gedacht. Sie kann nicht in Einschränkungen oder zum Aufrufen oder Festlegen von Werten verwendet werden.  <br/> |
|Gleitkommazahl  <br/> |Gibt einen **float**an.  <br/> |
|FloatArray  <br/> |Gibt ein Array von **float** -Werten an.  <br/> |
|Ganze Zahl  <br/> |Gibt eine ganze Zahl an.  <br/> |
|IntegerArray  <br/> |Gibt ein Array von ganzen Zahlen an.  <br/> |
|Long  <br/> |Gibt einen **Long**-Wert an.  <br/> |
|LongArray  <br/> |Gibt ein Array von **Long** -Werten an.  <br/> |
|Null  <br/> |Gibt einen NULL-Wert an. Dies ist für Fehler Berichterstattungs Zwecke gedacht. Sie kann nicht in Einschränkungen oder zum Aufrufen oder Festlegen von Werten verwendet werden.  <br/> |
|Objekt  <br/> |Gibt ein Objekt an. Dies ist für Fehler Berichterstattungs Zwecke gedacht. Sie kann nicht in Einschränkungen oder zum Aufrufen oder Festlegen von Werten verwendet werden.  <br/> |
|ObjectArray  <br/> |Gibt ein Array von Objekten an. Dies ist für Fehler Berichterstattungs Zwecke gedacht. Sie kann nicht in Einschränkungen oder zum Aufrufen oder Festlegen von Werten verwendet werden.  <br/> |
|Kurz  <br/> |Gibt einen **Short**-Wert an.  <br/> |
|ShortArray  <br/> |Gibt ein Array von **Short** -Werten an.  <br/> |
|System Time  <br/> |Gibt einen System Zeitwert an.  <br/> |
|SystemTimeArray  <br/> |Gibt ein Array von Systemzeit Werten an.  <br/> |
|Zeichenfolge  <br/> |Gibt eine Zeichenfolge an.  <br/> |
|StringArray  <br/> |Gibt ein Array von Zeichenfolgen an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifiziert eine erweiterte MAPI-Eigenschaft.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

