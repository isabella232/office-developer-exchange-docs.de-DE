---
title: QueryString (querystringtype)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: Das QueryString-Element enthält eine Post Fach Abfragezeichenfolge basierend auf der erweiterten Abfrage Syntax (AQS).
localization_priority: Priority
ms.openlocfilehash: eafbbab6de8d191197fb4b80e2b8e3cea80ab800
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459188"
---
# <a name="querystring-querystringtype"></a>QueryString (querystringtype)

Das **QueryString** -Element enthält eine Post Fach Abfragezeichenfolge basierend auf der erweiterten Abfrage Syntax (AQS). 
  
```XML
<QueryString/>
```

 **Querystringtype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|ResetCache  <br/> |Gibt an, dass der Cache zurückgesetzt werden soll.  <br/> |
|ReturnDeletedItems  <br/> |Gibt an, dass gelöschte Elemente zurückgegeben werden sollen.  <br/> |
|ReturnHighlightTerms  <br/> |Gibt an, dass hervorgehobene Ausdrücke zurückgegeben werden sollen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.  <br/> Im folgenden finden Sie den XPath-Ausdruck für dieses Element:/FindItem.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Text-Wert des **QueryString** -Elements stellt eine Post Fach Abfrage dar, die mithilfe einer Teilmenge der [erweiterten Abfrage Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx)vorgenommen wird. Weitere Informationen zu den unterstützten Syntaxoptionen für Abfragezeichenfolgen finden Sie im Abschnitt "Hinweise".
  
## <a name="remarks"></a>Bemerkungen

In Exchange Server 2010 ist dieses Element ein XML-Schema Zeichenfolgen-Typ. In Exchange-Versionen, die mit Exchange Server 2013 beginnen, einschließlich Exchange Online, ist der Typ für dieses Element **querystringtype**. Durch diese Änderung werden keine vorhandenen Clients unterbrechen, da drei neue optionale Attribute hinzugefügt werden. 
  
Das **QueryString** -Element schließt die Verwendung von EWS-Einschränkungen aus. AQS in EWS unterstützt drei Arten von Einschränkungen: Wort Phasen Einschränkungen, Datumsbereichs Einschränkungen und Einschränkungen für Nachrichtentypen. In den folgenden Tabellen werden die unterstützten Sucheigenschaften für die einzelnen Einschränkungstypen aufgeführt. 
  
**Word-Phasen Einschränkung**

|**Eigenschaft**|**Beispiel**|**Funktion**|
|:-----|:-----|:-----|
|Von  <br/> |Von: Dean  <br/> Von: "Dean hehe"  <br/> |Von Dean gesendete Suchelemente.  <br/> Von Dean hehe gesendete Suchelemente. Der Absender muss genau "Dean hehe" sein.  <br/> |
|in  <br/> |An: Dean  <br/> |An Dean gesendete Suchelemente.  <br/> |
|cc  <br/> |Cc: Dean  <br/> |Suchen Sie nach Elementen mit Dean in der CC-Zeile.  <br/> |
|bcc  <br/> |BCC: Dean  <br/> |Suchen Sie nach Elementen mit Dean in der Zeile Bcc.  <br/> |
|Participants  <br/> |Teilnehmer: Dekan  <br/> |Suchen Sie nach Elementen mit Dean in den Feldern an, CC oder Bcc.  <br/> |
|Betreff  <br/> |Betreff: product  <br/> Betreff: (Produktentwicklung)  <br/> Betreff: "Produktentwicklung"  <br/> |Suchen nach Elementen mit Produkt im Betreff.  <br/> Suchen Sie nach Elementen mit Produkt und Entwicklung im Betreff.  <br/> |
|Body  <br/> Inhalt  <br/> |Body: Fortschritt  <br/> Inhalt: Fortschritt  <br/> |Suchen Sie nach Elementen mit Fortschritt im Textkörper.  <br/> |
|Attachment  <br/> |Anlage: Bericht  <br/> |Suchen Sie nach Elementen mit dem Bericht im Namen der Anlagendatei oder im Datei Text.  <br/> |
|(Eigenschaft ist nicht angegeben)  <br/> |Produktentwicklung  <br/> |Suchen Sie nach Elementen, die sowohl Produkt als auch Entwicklung in allen Word-Phaseneigenschaften enthalten.  <br/> |
   
Die Übereinstimmung bei der Wort Phasen Einschränkung wird immer Groß-/Kleinschreibung beachtet. Die Word-Phasen Einschränkung unterstützt zwei Übereinstimmungstypen: Präfixübereinstimmung oder exakte Übereinstimmung. Präfixübereinstimmung ist das Standard Übereinstimmungsverhalten. Wenn Sie exakte Übereinstimmung wünschen, verwenden Sie doppelte Anführungszeichen. Der Betreff: "Product" entspricht beispielsweise "Product", aber nicht "Production" im Betreff. Mehrere Wörter in doppelten Anführungszeichen schränken sowohl die Wort Phasen als auch ihre Reihenfolge ein. Beispielsweise entspricht "Win Product" nur "Win Product", nicht "Win95-Produkt" oder "Produkt von Win". Sie können ein Sternchen ( \* ) verwenden, um eine Präfixübereinstimmung mit eingeschränkter Reihenfolge zu definieren. Beispielsweise entspricht "Win Product" " \* Win95-Produkt", "Windows-Produktionsreihe", aber nicht "Windows-neues Produkt" oder "Produkt von Win". Sie können alle Nachrichten durchsuchen, die von oder an eine Domäne gesendet werden. Beispielsweise von: "@Hotmail. com" gibt alle von Hotmail.com gesendeten Nachrichten zurück.
  
In der folgenden Tabelle werden die Einschränkungen für den Datumsbereich beschrieben.
  
**Datumsbereichs Einschränkung**

|**Eigenschaft**|**Beispiel**|**Funktion**|
|:-----|:-----|:-----|
|Gesendet  <br/> |Gesendet: Letzte Woche  <br/> Sent: 01/01/2001  <br/> Sent: 01/01/2001.. 01/15/2001  <br/> |Letzte Woche gesendete Suchelemente.  <br/> Suchelemente, die am 1. Januar 2001 gesendet wurden.  <br/> Suchelemente, die zwischen dem 1. Januar 2001 und dem 15. Januar 2001 gesendet wurden.  <br/> |
|Auszahlung  <br/> |Empfangen: heute  <br/> Empfangen: 01/01/2001  <br/> |Suchelemente, die heute empfangen werden.  <br/> Suchelemente, die am 1. Januar 2001 empfangen wurden.  <br/> |
   
Die beiden Punkte (..) sind ein Bereichsoperator. Es kann verwendet werden, um einen Bereich mit einem Start-und einem Enddatum zu definieren. Um ein Datum anzugeben, können Sie relative Datumsangaben verwenden. Die folgenden relativen Datumsangaben werden unterstützt:
  
- Relative Daten: heute, morgen, gestern
    
- Mehr Wort relative Daten: diese Woche, nächster Monat, letzte Woche, letzter Monat oder nächstes Jahr
    
- Tage: Sonntag, Montag, Dienstag, Mittwoch, Donnerstag, Freitag, Samstag
    
- Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember
    
In der folgenden Tabelle werden Einschränkungen für Nachrichtentypen beschrieben. 
  
**Einschränkung des Nachrichtentyps**

|**Eigenschaft**|**Beispiel**|**Funktion**|
|:-----|:-----|:-----|
|Art  <br/> |Kind: Tasks  <br/> |Alle Aufgabenelemente durchsuchen.  <br/> |
   
AQS in EWS verwendet die **Kind** -Eigenschaft, um den Nachrichtentyp anzugeben. Die Kind-Eigenschaft kann mit den folgenden Elementtypen verwendet werden: 
  
- email
    
- meetings
    
- tasks
    
- notes
    
- docs
    
- journals
    
- contacts
    
- im
    
In der folgenden Tabelle wird die Gruppierung logischer Connectors beschrieben.
  
**Gruppieren von logischen Connectors**

|**Connector**|**Beispiel**|**Funktion**|
|:-----|:-----|:-----|
|UND  <br/> |Betreff: Produkt und Betreff: Development  <br/> Betreff: (Produkt und Entwicklung)  <br/> Betreff: (Produktentwicklung)  <br/> |Suchen von Elementen sowohl mit Produkt als auch mit der Entwicklung im Betreff.  <br/> |
|ODER  <br/> |Body: Projekt oder Body: Vorschlag  <br/> Body: (Projekt oder Vorschlag)  <br/> |Suchen von Elementen mit einem Produkt oder einer Entwicklung im Textkörper.  <br/> |
|NICHT  <br/> |Not Body: Vorschlag  <br/> Body: (kein Vorschlag)  <br/> |Suchen nach Nachrichten ohne Vorschlag im Textkörper.  <br/> |
   
Und ist immer der standardmäßige Connector. Beispielsweise Betreff: Project und Body: Vorschlag ist identisch mit Betreff: Project Body: Proposal. Bei logischen Connectors wird die Groß-/Kleinschreibung beachtet. Body: (Project oder Proposal) sucht beispielsweise Nachrichten mit "Project", "or" und "Proposal" im Textkörper anstelle von "Project" oder "Proposal". Das Plus-Symbol (+) entspricht und. Das Bindestrich Symbol (-) entspricht nicht. Body: (Project-proposal) sucht beispielsweise Nachrichten mit "Project", aber ohne "Vorschlag" im Textkörper. 
  
Die Abfragezeichenfolge kann auch nicht indizierte Eigenschaften für die Suche enthalten. Wenn die Abfragezeichenfolge nicht indizierte Eigenschaften enthält, kann die Suche eine Exchange-Suche für die indizierten Eigenschaften und eine Speichersuche in den nicht indizierten Eigenschaften durchführen. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine Anforderung zum Suchen nach Nachrichten im Posteingang mit AutoErmittlung im Betreff.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:Autodiscover</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" 
                        TotalItemsInView="5" 
                        IncludesLastItemInRange="false">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkADEzOTExYjJkLTYx" ChangeKey="CQAAABY" />
                <t:Subject>How to use Autodiscover</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)
  
[FindConversation-Vorgang](findconversation-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

