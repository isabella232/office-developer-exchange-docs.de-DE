---
title: ExtendedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExtendedFieldURI
api_type:
- schema
ms.assetid: b3c6ea3a-9ead-44b9-9d99-64ecf12bde23
description: Das ExtendedFieldURI -Element identifiziert eine erweiterte MAPI-Eigenschaft.
ms.openlocfilehash: 0cf3926c900e1b1f35018c6706cfe99ebefbe76f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542316"
---
# <a name="extendedfielduri"></a>ExtendedFieldURI

Das **ExtendedFieldURI** -Element identifiziert eine erweiterte MAPI-Eigenschaft. 
  
```xml
<ExtendedFieldURI DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" />
```

**PathToExtendedFieldType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**DistinguishedPropertySetId** <br/> |Definiert die bekannten Eigenschaftensatz-IDs für extended MAPI-Eigenschaften.<br/><br/>Wenn dieses Attribut verwendet wird, können nicht die Attribute **PropertySetId** und **PropertyTag** verwendet werden. Dieses Attribut muss entweder die **PropertyId** oder **PropertyName** -Attribut und das **PropertyType** -Attribut verwendet werden.  <br/><br/>Die **DistinguishedPropertySetId** Attributtabelle weiter unten in diesem Thema werden die möglichen Werte für dieses Attribut aufgelistet.<br/><br/>Dieses Attribut ist optional.  <br/> |
|**PropertySetId** <br/> |MAPI-Eigenschaft oder Namespace erweitert, durch die identifizierende GUID identifiziert.<br/><br/>Wenn dieses Attribut verwendet wird, kann nicht das Attribut **DistinguishedPropertySetId** und **PropertyTag** verwendet werden. Dieses Attribut muss entweder die **PropertyId** oder **PropertyName** -Attribut und das **PropertyType** -Attribut verwendet werden.  <br/><br/>Dieses Attribut ist optional.  <br/> |
|**PropertyTag** <br/> |Identifiziert das Eigenschafts-Tag ohne die Typ-Teil des Tags an. Die **PropertyTag** kann als eine Hexadezimalzahl oder eine kurze ganze Zahl dargestellt werden.  <br/><br/>Der Bereich zwischen 0 x 8000 und 0xFFFE stellt das benutzerdefinierte Eigenschaften der Zellbereich. Wenn eine Postfachdatenbank eine benutzerdefinierte Eigenschaft zum ersten Mal findet, wird diese benutzerdefinierte Eigenschaft ein Eigenschaftentag innerhalb der benutzerdefinierten Eigenschaft 0 x 8000 0xFFFE. Ein Tag für die angegebene benutzerdefinierte Eigenschaft unterscheiden sich höchstwahrscheinlich in Datenbanken. Daher kann eine benutzerdefinierte Eigenschaft Anforderung von Eigenschaftentag verschiedene Eigenschaften in verschiedenen Datenbanken zurück. Die Verwendung des Attributs **PropertyTag** ist unzulässig für benutzerdefinierte Eigenschaften. Verwenden Sie stattdessen die **PropertySetId** -Attribut und das Attribut **PropertyName** oder **PropertyId**.  <br/><br/>**WICHTIG:** Greifen Sie mithilfe der GUID + Name/ID auf eine benutzerdefinierte Eigenschaft zwischen 0x8000 und 0xFFFE zu. If the **PropertyTag** attribute is used, the **DistinguishedPropertySetId**, **PropertySetId**, **PropertyName**, and **PropertyId** attributes cannot be used.<br/><br/>Dieses Attribut ist optional.<br/><br/>**HINWEIS:** Sie können kein Eigenschaftstagattribut für Eigenschaften innerhalb des benutzerdefinierten Bereichs 0x8000-0xFFFE verwenden. You must use a named property in this case.           |
|**PropertyName** <br/> |Identifiziert eine erweiterte Eigenschaft anhand des Namens. Diese Eigenschaft muss mit **DistinguishedPropertySetId** oder **PropertySetId** kombiniert werden. <br/><br/>Wenn dieses Attribut verwendet wird, können nicht die Attribute **PropertyId** und **PropertyTag** verwendet werden.<br/><br/>Dieses Attribut ist optional.  <br/> |
|**PropertyId** <br/> |Identifiziert eine erweiterte Eigenschaft anhand seiner Versendung-ID In den decimal oder hexadezimale kann die Verteiler-ID identifiziert werden. Diese Eigenschaft muss mit **DistinguishedPropertySetId** oder **PropertySetId** kombiniert werden. <br/><br/>Wenn dieses Attribut verwendet wird, können nicht die Attribute **PropertyName** und **PropertyTag** verwendet werden.<br/><br/>Dieses Attribut ist optional.  <br/> |
|**Propertytype** <br/> |Den Eigenschaftentyp eines Tags Eigenschaft darstellt. Dies entspricht dem Unwichtigstes Wort in einem Eigenschaftentag.<br/><br/>Die Tabelle PropertyType-Attribut weiter unten in diesem Thema enthält die möglichen Werte für dieses Attribut.<br/><br/>Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="distinguishedpropertysetid-attribute"></a>DistinguishedPropertySetId-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Adresse  <br/> |Gibt die Adresse-Eigenschaft Satz-ID den Namen.  <br/> |
|Appointment  <br/> |Identifiziert die Satz-ID von Termin-Eigenschaft nach Namen.  <br/> |
|CalendarAssistant  <br/> |Gibt die ID der Kalender-Assistent-Eigenschaft nach Namen.  <br/> |
|Common  <br/> |Gibt den Namen die allgemeine Satz-ID für die Eigenschaft.  <br/> |
|InternetHeaders  <br/> |Bezeichnet die Satz-ID von Internet Kopfzeilen-Eigenschaft nach Namen.  <br/> |
|Besprechung  <br/> |Identifiziert die Besprechung Eigenschaftensatz-ID nach Namen.  <br/> |
|Freigabe  <br/> | <br/> |
|PublicStrings  <br/> |Identifiziert die Satz-ID von öffentlichen Zeichenfolgen-Eigenschaft nach Namen.  <br/> |
|Aufgabe  <br/> |Identifies the task property set ID by name.  <br/> |
|UnifiedMessaging  <br/> |Gibt die unified messaging Eigenschaft Satz-ID den Namen.  <br/> |
   
#### <a name="propertytype-attribute"></a>PropertyType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|ApplicationTime  <br/> |Ein double-Wert, der als Datum und Uhrzeit interpretiert wird. Der ganzzahligen Teil ist das Datum und das zu rundende Teil ist die Zeit.  <br/> |
|ApplicationTimeArray  <br/> |Ein Array von double-Werte, die als Datum und Uhrzeit interpretiert werden.  <br/> |
|Binary  <br/> |Eine Base64-codierte Binärwert.  <br/> |
|BinaryArray  <br/> |Ein Array von Base64-codierten Binärwerte.  <br/> |
|Boolescher Wert  <br/> |Ein Boolean **true** oder **false**.  <br/> |
|CLSID  <br/> |Eine GUID-Zeichenfolge.  <br/> |
|CLSIDArray  <br/> |Ein Array von GUID-Zeichenfolgen.  <br/> |
|Currency  <br/> |Eine 64-Bit-Ganzzahl, die als die Anzahl der Cent interpretiert wird.  <br/> |
|CurrencyArray  <br/> |Ein Array von 64-Bit-Ganzzahlen, die als die Anzahl der Cent interpretiert werden.  <br/> |
|Double  <br/> |Ein 64-Bit-Gleitkomma-Wert.  <br/> |
|DoubleArray  <br/> |Ein Array von 64-Bit-Gleitkomma-Werte.  <br/> |
|Fehler  <br/> |SCODE-Wert; 32-Bit, ganze Zahl ohne Vorzeichen  <br/> Für Einschränkungen oder für erste/Einstellungswerte verwendet nicht. Diese Eigenschaft ist nur für die berichterstellung vorhanden.  <br/> |
|Gleitkomma  <br/> |Ein 32-Bit-Gleitkomma-Wert.  <br/> |
|FloatArray  <br/> |Ein Array von 32-Bit-Gleitkomma-Werte.  <br/> |
|Ganzzahl  <br/> |Eine 32-Bit (Int32) ganze Zahl mit Vorzeichen.  <br/> |
|IntegerArray  <br/> |Ein Array von 32-Bit (Int32) ganze Zahlen mit Vorzeichen.  <br/> |
|Long  <br/> |Eine mit oder ohne Vorzeichen 64-Bit (Int64) ganze Zahl.  <br/> |
|LongArray  <br/> |Ein Array von mit oder ohne Vorzeichen 64-Bit (Int64) ganzen Zahlen.  <br/> |
|Null  <br/> |Gibt keinen Eigenschaftswert an.  <br/> Für Einschränkungen oder für erste/Einstellungswerte verwendet nicht. Diese Eigenschaft ist nur für die berichterstellung vorhanden.  <br/> |
|Objekt  <br/> |Ein Zeiger auf ein Objekt, das die IUnknown-Schnittstelle implementiert wird.  <br/> Für Einschränkungen oder für erste/Einstellungswerte verwendet nicht. Diese Eigenschaft ist nur für die berichterstellung vorhanden.  <br/> |
|ObjectArray  <br/> |Ein Array von Zeigern für Objekte, die die IUnknown-Schnittstelle implementieren.  <br/> Für Einschränkungen oder für erste/Einstellungswerte verwendet nicht. Diese Eigenschaft ist nur für die berichterstellung vorhanden.  <br/> |
|Kurz  <br/> |Eine 16-Bit-Ganzzahl.  <br/> |
|ShortArray  <br/> |Ein Array von 16-Bit-Ganzzahlen mit Vorzeichen.  <br/> |
|Systemtime  <br/> |Eine 64-Bit-Daten und die Uhrzeit Ganzzahlwert in Form von eine FILETIME-Struktur.  <br/> |
|SystemTimeArray  <br/> |Ein Array von 64-Bit-Ganzzahl Datum und Uhrzeit Werte in Form von eine FILETIME-Struktur.  <br/> |
|Zeichenfolge  <br/> |Unicode-Zeichenfolge.  <br/> |
|StringArray  <br/> |Ein Array von Unicode-Zeichenfolgen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für Ordner und Elemente identifiziert.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> | Zusätzliche Eigenschaften identifiziert.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/FindFolder/FolderShape/AdditionalProperties` <br/>  `/GetFolder/FolderShape/AdditionalProperties` <br/>  `/SyncFolderHierarchy/FolderShape/AdditionalProperties` <br/>  `/GetItem/ItemShape/AdditionalProperties` <br/>  `/FindItem/ItemShape/AdditionalProperties` <br/>  `/SyncFolderItems/ItemShape/AdditionalProperties` <br/>  `/GetAttachment/AttachmentShape/AdditionalProperties` <br/> |
|[SetItemField](setitemfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |Stellt einen Löschvorgang für eine bestimmte Eigenschaft aus einem Element löschen, während ein [UpdateItem Operation](updateitem-operation.md)dar.  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |Stellt einen Löschvorgang einer angegebenen Eigenschaft aus einem Ordner während eines UpdateFolder-Aufrufs dar.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten, die während einer [UpdateItem Operation](updateitem-operation.md) an eine einzelne Eigenschaft eines Elements angefügt werden sollen.  <br/> |
|[AppendToFolderField](appendtofolderfield.md) <br/> |Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.  <br/> |
|[Exists](exists.md) <br/> |Stellt einen Suchausdruck dar, der **true** zurückgibt, wenn die angegebene Eigenschaft zu einem Element vorhanden ist.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.  <br/> |
|[IsEqualTo](isequalto.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** ausgibt, wenn sie gleich sind.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft größer ist.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft größer oder gleich der zweiten ist.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft kleiner als die zweite ist.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft kleiner als die zweite ist.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Stellt einen Suchausdruck dar, der einer Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die Wert nicht identisch sind.  <br/> |
|[Schließt](excludes.md) <br/> |Führt eine bitweise Maske der Eigenschaften aus.  <br/> |
|[Enthält](contains.md) <br/> |Stellt einen Suchausdruck dar, der bestimmt, ob eine angegebene Eigenschaft den angegebenen konstanten Zeichenfolgewert enthält.  <br/> |
|[FieldOrder](fieldorder.md) <br/> |Stellt ein einzelnes Feld dar, nach dem die Ergebnisse durchsucht werden und gibt die Richtung für die Sortierung an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Einige Attribute können nicht in Kombination mit anderen Attribute verwendet werden. Jede Anforderung, die sich über eine ungültige Kombination der Attribute der erweiterten Eigenschaft stammen, wird eine Fehlermeldung generiert.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
> [!NOTE]
> [!HINWEIS] In Microsoft .NET ist ein Long-Wert eine 64-Bit-Ganzzahl mit Vorzeichen, während in MAPI und COM, einen Long-Wert ist eine 32-Bit-Ganzzahl. Die meisten Entwickler werden Microsoft.NET Framework verwenden, um die Exchange-Webdienste-Clientanwendungen zu entwickeln. Daher die .NET Benennung wird anstelle der MAPI benennen.
> 
> Die PR_MESSAGE_FLAGS MAPI-Eigenschaft 0x0E07 ist beispielsweise ein PT \_ LONG-Typ. In .NET gilt dies eine ganze Zahl. Eine erweiterte Eigenschaft für PR_MESSAGE_FLAGS wird als `<t:ExtendedFieldURI PropertyTag="0x0E07" PropertyType="Integer"/>` definiert. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird eine Anforderung erstellt ein Element, das zwei benutzerdefinierte Eigenschaften verfügt. Die erste benutzerdefinierte Eigenschaft heißt **IsMyHouse** mit einem booleschen Wert auf **true** festgelegt. Die zweite benutzerdefinierte erweiterte Eigenschaft heißt **HousePrices**. Sie enthält ein Array von Währungsangaben. 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
    MessageDisposition="SaveOnly">
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </SavedItemFolderId>
      <Items>
        <t:Item>
          <t:ItemClass>IPM.Note</t:ItemClass>
          <t:Subject>Create an extended property</t:Subject>
          <t:Body BodyType="Text">Added info to extended props</t:Body>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="PublicStrings" 
                                PropertyName="IsMyHouse" 
                                PropertyType="Boolean"/>
            <t:Value>true</t:Value>
          </t:ExtendedProperty>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="PublicStrings" 
                                PropertyName="HousePrices" 
                                PropertyType="CurrencyArray"/>
            <t:Values>
              <t:Value>30000000</t:Value>
              <t:Value>40000000</t:Value>
              <t:Value>50000000</t:Value>
            </t:Values>
          </t:ExtendedProperty>
        </t:Item>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FieldURI](fielduri.md)
- [IndexedFieldURI](indexedfielduri.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

