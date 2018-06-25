---
title: QueryString (QueryStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: Das QueryString-Element enthält eine Postfach-Abfragezeichenfolge basierend auf Erweiterte Query Syntax (AQS).
ms.openlocfilehash: 410405638b3f8628dc589049873cfea1f153310c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830943"
---
# <a name="querystring-querystringtype"></a>QueryString (QueryStringType)

Das **QueryString** -Element enthält eine Postfach-Abfragezeichenfolge basierend auf Erweiterte Query Syntax (AQS). 
  
```XML
<QueryString/>
```

 **QueryStringType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|ResetCache  <br/> |Gibt an, dass der Cache zurückgesetzt werden sollen.  <br/> |
|ReturnDeletedItems  <br/> |Gibt an, dass gelöschte Elemente zurückgegeben werden sollen.  <br/> |
|ReturnHighlightTerms  <br/> |Gibt an, dass hervorgehobene Begriffe zurückgegeben werden sollen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.  <br/> Im folgenden werden der XPath-Ausdruck, der dieses Element: /FindItem.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert der **QueryString** -Element stellt eine Postfach-Abfrage, die mithilfe einer Teilmenge der [(Erweiterte Query Syntax, AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx)erfolgt ist. Finden Sie im Abschnitt "Hinweise" Informationen zu den unterstützten Syntaxoptionen für Abfragezeichenfolgen.
  
## <a name="remarks"></a>Hinweise

Exchange Server 2010 ist dieses Element vom Typ String XML-Schema. In Versionen von Exchange, beginnend mit Exchange Server 2013 ist einschließlich Exchange Online, den Typ für dieses Element **QueryStringType**. Diese Änderung wird alle vorhandenen Clients werden nicht umbrochen, da drei neue optionale Attribute hinzugefügt. 
  
Das Element **QueryString** schließt die Verwendung der EWS-Einschränkungen aus. AQS im EWS unterstützt drei Arten von Beschränkungen: word-Phase Einschränkung, Datum Bereich Einschränkung und Nachricht Typ Einschränkung. Den folgenden Tabellen sind die unterstützten Sucheigenschaften für jeden Einschränkungstyp. 
  
**Word Phase Einschränkung**

|**Eigenschaft**|**Beispiel**|**Funktion**|
|:-----|:-----|:-----|
|Von  <br/> |Von: Dominik  <br/> Aus: "Dominik Halstead"  <br/> |Suchen von Dominik gesendete Elemente.  <br/> Suchen von Dean Halstead gesendete Elemente. Der Absender muss genau "Dominik Halstead".  <br/> |
|in  <br/> |An: Dominik  <br/> |Suchen Sie Elemente, die an Dominik gesendet.  <br/> |
|cc  <br/> |Cc:Dean  <br/> |Suchen Sie nach Elementen mit Dominik in der Zeile Cc.  <br/> |
|bcc  <br/> |Bcc:Dean  <br/> |Suchen Sie nach Elementen mit Dominik in der Bcc-Zeile.  <br/> |
|Teilnehmer  <br/> |Teilnehmer: Dominik  <br/> |Suchen Sie nach Elementen mit Dominik in an, Cc oder Bcc Felder.  <br/> |
|Subject  <br/> |Betreff: Produkt  <br/> Betreff:(product development)  <br/> Betreff: "Produktentwicklung"  <br/> |Suchen Sie nach Elementen mit Produkt im Betreff.  <br/> Suchen Sie nach Elementen mit Produkt- und Entwicklung im Betreff.  <br/> |
|Textkörper  <br/> Inhalt  <br/> |Body: Status  <br/> Inhalt: Status  <br/> |Suchen Sie nach Elementen mit dem Fortschritt im Textkörper.  <br/> |
|Anlage  <br/> |Anhang: Bericht  <br/> |Suchen Sie nach Elementen mit Bericht der Name oder die Datei Textkörper Anlage-Datei.  <br/> |
|(die Eigenschaft ist nicht angegeben)  <br/> |Produktentwicklung  <br/> |Suchen Sie nach Elementen, die Produkt- und Entwicklung Word Phase Eigenschaften enthalten.  <br/> |
   
Word Phase Einschränkung Übereinstimmung ist immer zwischen Groß-und Kleinschreibung. Word Phase Beschränkung unterstützt zwei Übereinstimmungstypen: Präfix oder genaue Entsprechung. Präfixübereinstimmung ist das Standardverhalten für die Übereinstimmung. Wenn Sie eine genaue Übereinstimmung möchten, verwenden Sie doppelte Anführungszeichen. Z. B. Betreff: "Produkt" stimmt mit 'Product' aber nicht 'Backup' im Betreff. Mehrere Wörter in doppelte Anführungszeichen einschränken Word Phasen und deren Reihenfolge. Produkt beispielsweise "win" ermittelt nur "Win Produkt", nicht "Windows 95 Produkt" oder "Produkt des Win". Sie können ein Sternchen (\*) so definieren Sie eine präfixübereinstimmung mit Reihenfolge eingeschränkt. Beispielsweise "win Produkt"\* 'Windows 95 Produkt', 'Windows Produktion Line', aber nicht "Windows neue Produkt" oder "Produkt des Win" entspricht. Sie können alle Nachrichten aus oder einer Domäne suchen. Beispielsweise from:"@hotmail.com" gibt alle Nachrichten von hotmail.com zurück.
  
Die folgende Tabelle beschreibt Datum Bereich Einschränkungen.
  
**Datum Bereich Einschränkung**

|**Eigenschaft**|**Beispiel**|**Funktion**|
|:-----|:-----|:-----|
|Gesendet  <br/> |Gesendet: letzte Woche  <br/> Gesendet: 01/01/2001  <br/> Sent:01/01/2001..01/15/2001  <br/> |Search-Elemente, die letzte Woche gesendet.  <br/> Suchen Sie am 1. Januar 2001 gesendete Elemente.  <br/> Suchen Sie Elemente, die zwischen dem 1. Januar 2001 und dem 15. Januar 2001 gesendet.  <br/> |
|Auszahlung  <br/> |Empfangen: heute  <br/> Empfangen: 01/01/2001  <br/> |Suchen Sie noch heute empfangenen Elemente.  <br/> Suchen Sie am 1. Januar 2001 empfangenen Elemente.  <br/> |
   
Die zwei Punkte (.) ist ein Range-Operator. Hiermit können Sie einen Bereich mit einer Start- und Enddatum zu definieren. Um ein Datum angeben, können Sie die relative Daten verwenden. Die folgenden relativen Datumsangaben werden unterstützt:
  
- Relative Datumsangaben: heute, morgen, gestern
    
- Relative Datumsangaben aus: Diese Woche, nächsten Monat, letzte Woche, letzten Monat oder Jahr
    
- Tage: Sonntag, Montag, Dienstag, Mittwoch, Donnerstag, Freitag, Samstag
    
- Januar, Februar, März, Mai April, Juni, Juli, August, September, Oktober, November, Dezember
    
Die folgende Tabelle beschreibt die Nachricht Typ Einschränkungen. 
  
**Beschränkung der Nachricht-Typ**

|**Eigenschaft**|**Beispiel**|**Funktion**|
|:-----|:-----|:-----|
|Art  <br/> |Art-Aufgaben:  <br/> |Durchsuchen Sie alle Aufgabenelemente.  <br/> |
   
AQS im EWS verwendet die **Art** -Eigenschaft den Nachrichtentyp an. Die Kind-Eigenschaft kann mit den folgenden Elementtypen verwendet werden: 
  
- E-Mail
    
- Besprechungen
    
- tasks
    
- notes
    
- Dokumente
    
- Journale
    
- contacts
    
- Instant Messaging
    
Die folgende Tabelle beschreibt die logische Connectors gruppieren.
  
**Logische Gruppierung-connectors**

|**Connector**|**Beispiel**|**Funktion**|
|:-----|:-----|:-----|
|AND  <br/> |Betreff: Produkt-und Thema: Entwicklung  <br/> Betreff:(product AND development)  <br/> Betreff:(product development)  <br/> |Durchsuchen Sie Elemente mit Produkt- und Entwicklung im Betreff.  <br/> |
|ODER  <br/> |Body: Project oder Text Vorschlag:  <br/> Body:(project OR proposal)  <br/> |Suchen Sie Elemente mit dem Produkt oder Entwicklung im Textkörper.  <br/> |
|NOT  <br/> |NICHT Body: Vorschlag  <br/> Body:(NOT proposal)  <br/> |Suchen Sie im Textkörper Nachrichten ohne Vorschlag.  <br/> |
   
UND ist immer der Standard-Connector. Beispielsweise Betreff: Projekt und Textkörper: Vorschlag entspricht dem Betreff: Body: Projektvorschlag. Logische Verbinder sind Groß-/Kleinschreibung beachtet. Beispielsweise body:(project Or proposal) sucht Nachrichten mit "Projekt", "oder" und "Vorschlag" im Nachrichtentext anstelle von "Project" oder "Vorschlag". Das Pluszeichen (+) entspricht und. Das Symbol Bindestrich (-) entspricht nicht. Beispielsweise body:(project-proposal) Nachrichten mit "Projekt", jedoch ohne 'Vorschlag' im Text durchsucht. 
  
Die Abfragezeichenfolge kann auch nicht indizierte Eigenschaften für die Suche enthalten. Wenn die Abfragezeichenfolge nicht indizierte Eigenschaften enthält, kann die Suche eine Exchange-Suche auf indizierten Eigenschaften sowie eine Store-Suche in nicht indizierten Eigenschaften ausführen. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine Anforderung an die Nachrichten im Posteingang mit der AutoErmittlung in den Betreff gesucht.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)
  
[FindConversation Operation](findconversation-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

