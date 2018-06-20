---
title: Führen Sie eine AQS-Suche mithilfe der EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c136901a-313e-4adf-a223-1d090d16917a
description: Erfahren Sie, wie Sie mit Abfragezeichenfolgen und AQS in die EWS Managed API oder EWS-Anwendung zu suchen.
ms.openlocfilehash: dc859e24fa80cd5627477182979c9cc9527818d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756997"
---
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a>Führen Sie eine AQS-Suche mithilfe der EWS in Exchange

Erfahren Sie, wie Sie mit Abfragezeichenfolgen und AQS in die EWS Managed API oder EWS-Anwendung zu suchen.
  
Abfragezeichenfolgen bieten eine Alternative zur [Suchfilter](how-to-use-search-filters-with-ews-in-exchange.md) Suchkriterien ausgedrückt. Der größte Vorteil von Abfragezeichenfolgen ist, dass Sie nicht erforderlich sind, um eine einzelne Eigenschaft zum Suchen anzugeben. Sie können nur einen Wert angeben, und die Suche gilt für alle häufig verwendeten Felder auf die Elemente. Sie können auch die Suche mithilfe von (Erweiterte Query Syntax, AQS) anstelle eines einfachen Werts verfeinern. Abfragezeichenfolgen haben jedoch die folgenden Nachteile, denen Ihnen bekannt sein sollten, bevor Sie die Toolbox hinzufügen: 
  
- **Möglichkeit zur Suche nach bestimmten Eigenschaften.** Wenn Sie mit einem einfachen Wert in einer Abfragezeichenfolge suchen, wird die Suche für alle indizierten Eigenschaften ausgeführt. Sie können die Suche auf bestimmte Eigenschaften verfeinern, aber die Eigenschaften für die Verwendung in einer Zeichenfolge AQS verfügbar sind beschränkt. Wenn die Eigenschaft, die Sie suchen möchten eine der Eigenschaften nicht zur Verfügung, die für AQS verfügbar sind, sollten Sie einen Suchfilter. 
    
- **Benutzerdefinierte Eigenschaften werden nicht durchsucht.** Zeichenfolgensuchen Abfrage für einen Index ausgeführt werden, und benutzerdefinierte Eigenschaften sind nicht in der betreffenden Index enthalten. Wenn Sie die Suche nach benutzerdefinierten Eigenschaften müssen, verwenden Sie stattdessen einen Suchfilter. 
    
- **Eingeschränkte Steuerung für Zeichenfolge durchsucht.** Abfrage Zeichenfolgensuchen immer groß-und Kleinschreibung ignorieren, und sind immer Suchvorgänge nach Teilzeichenfolgen dar. Wenn Sie möchten Groß-/Kleinschreibung beachtet, Präfix oder genauen Übereinstimmung gesucht, verwenden Sie einen Filter für die Suche. 
    
- **Nicht verfügbar für Ordner oder Suchordner.** Der EWS-Vorgänge für die Suche nach Ordner unterstützen nicht mit einer Abfragezeichenfolge. Darüber hinaus unterstützen keine Suchordner Abfragezeichenfolgen. In beiden Fällen ist ein Suchfilter nur die Option. 
    
## <a name="creating-a-query-string"></a>Erstellen einer Abfragezeichenfolge
<a name="bk_CreateQueryString"> </a>

Abfragezeichenfolgen in die EWS Managed API und EWS werden als eine Teilmenge der Syntax AQS interpretiert. AQS Zeichenfolgen bestehen aus Werten oder Schlüsselwort/Wert-Paaren, getrennt durch einen Doppelpunkt (:)).
  
`keyword:value`

Wenn Sie ein Wert ohne ein Schlüsselwort angegeben wird, werden alle indizierte Eigenschaften für den Wert durchsucht. Wenn ein Schlüsselwort mit einem Wert kombiniert ist, gibt das Schlüsselwort Suche nach den entsprechenden Wert einer Eigenschaft an.
  
**In Tabelle 1. Unterstützte AQS Schlüsselwörter**

|**Schlüsselwort**|**Werttyp**|**Beispiel**|
|:-----|:-----|:-----|
|subject  <br/> |String  <br/> |Betreff: Projekt  <br/> |
|body  <br/> |String  <br/> |Body: Verkaufszahlen  <br/> |
|Anlage  <br/> |String  <br/> |Anhang: Bericht  <br/> |
|in  <br/> |String  <br/> |an: "Sadie Daniels"  <br/> |
|Von  <br/> |String  <br/> |von: hoffe  <br/> |
|cc  <br/> |String  <br/> |cc: "Ronnie Sturgis"  <br/> |
|bcc  <br/> |String  <br/> |Bcc:mack  <br/> |
|participants  <br/> |String  <br/> |Teilnehmer: sadie  <br/> |
|category  <br/> |String  <br/> |Kategorie: Projekt  <br/> |
|Wichtigkeit  <br/> |String  <br/> |Wichtigkeit: hoch  <br/> |
|Art  <br/> |Elementtyp  <br/> |Art-Besprechungen:  <br/> |
|gesendet  <br/> |Date  <br/> |gesendet: 12/10/2013  <br/> |
|empfangen  <br/> |Date  <br/> |empfangen: gestern  <br/> |
|HasAttachment  <br/> |Boolean  <br/> |Hat Anlage: true  <br/> |
|isflagged  <br/> |Boolean  <br/> |isflagged:true  <br/> |
|isread  <br/> |Boolean  <br/> |isread:false  <br/> |
|size  <br/> |Zahl  <br/> |Größe:\>5000  <br/> |
   
Sehen wir uns an, wie die verschiedenen Werttypen funktionieren.
  
### <a name="using-a-string-value-type"></a>Verwenden einen String-Wert-Typ

Zeichenfolge Werttypen sind standardmäßig als Präfix Suchmethode, die Groß-/ nicht Kleinschreibung durchsucht. Dies bedeutet, dass die Suche nach Betreff: Project eine der folgenden Betreffzeilen würde sich eine Übereinstimmung: 
  
- Projekt Besprechungsnotizen
    
- Haben Sie die Projektpläne?
    
- Den Umsatzprognosen Dezember
    
Sie können die ganzes Wort anstelle von übereinstimmenden Präfixe erforderlich, durch die Zeichenfolge in Anführungszeichen einschließen, um die Suche ändern. Suchen nach Betreff: würde ein "Projekt" den Wert "Dezember den Umsatzprognosen" aus der Liste der Übereinstimmungen. Beachten Sie, dass der Wert immer noch nicht Groß-/Kleinschreibung beachtet wird. 
  
Wenn Sie mehrere Wörter in einer Abfragezeichenfolge verwenden, erfordert eine Übereinstimmung, dass beide Wörter in den durchsuchten Feldern angezeigt werden. Beispielsweise würde Suchen nach Betreff: Projektplan eine der folgenden Betreffzeilen entsprechen: 
  
- Projektplan
    
- Haben Sie die Projektpläne?
    
- Senden Sie mir bitte des Plans für unsere Projekt
    
- Planen von Projektmeilensteine
    
Wenn Sie mehrere Wörter in Anführungszeichen einschließen, werden sie als eine einzelne Phrase behandelt. Suchen nach Betreff: "Projektplan" würde nur den Betreff "Projektplan" aus der vorherigen Liste übereinstimmen. 
  
### <a name="using-an-item-type-value-type"></a>Verwenden einen Element Typ Werttyp

Die folgenden Artikelwerte können mit dem Schlüsselwort **Art** Sie die Suchergebnisse auf nur einen bestimmten Typ des Elements, wie e-Mail oder Besprechungsanfragen einschränken: 
  
- contacts    
- Dokumente    
- E-Mail    
- Faxnachrichten    
- Instant Messaging (Sofortnachrichten entspricht)    
- Journale    
- Besprechungen (entspricht Termine und Besprechungsanfragen)    
- notes    
- posts    
- rssfeeds    
- tasks    
- Voicemail
    
### <a name="using-a-date-value-type"></a>Verwenden einen Datum Werttyp

Sie können auf unterschiedliche Arten Datumstypen Wert suchen. Am einfachsten ist, um nach einem bestimmten Datum zu suchen. Suchen mit empfangen: 12/11/2013 werden alle 11 Dezember 2013 empfangenen Elemente zurückgegeben. Jedoch können Sie auch weniger spezifischen sein. Suchen mit empfangen: 12/11 werden alle am 11. Dezember des aktuellen Jahres empfangenen Elemente zurückgegeben. 
  
Eine weitere Option ist die Verwendung die Monatsnamen an. Für die Suche können mit empfangen: 11 Dezember 2013 oder Dezember 11 die gleichen Ergebnisse zu erhalten, empfangen: 12/11/2013 und empfangene: 12/11, jeweils. Sie können auch mit suchen empfangen: Dezember zum Abrufen aller Elemente im Dezember, im aktuellen Jahr eingegangen. 
  
Verwenden die Namen der Wochentage ist auch eine Option aus. Suchen mit empfangen: Dienstag wird Dienstag der aktuellen Woche empfangene alle Elemente zurückgegeben. 
  
Datum Werttypen unterstützen auch einen Satz von Schlüsselwörtern für Suchvorgänge relativ zu der aktuellen Zeit. Die folgenden Schlüsselwörter werden unterstützt:
  
- heute  
- tomorrow
- yesterday
- this week    
- Letzte Woche    
- nächsten Monat    
- letzten Monat    
- Jahr
    
Datumstypen Wert können auch mit relationalen Operatoren wie größer oder kleiner verglichen werden als, oder als Bereich Bereich Operator **.** angegeben. Beispielsweise erhalten:\>11/30/2013 gesendet:\>= gestern und received:12/1/2013..today sind alle gültigen Abfragezeichenfolgen. 
  
### <a name="using-a-boolean-value-type"></a>Verwenden einen Wert vom Typ Boolean-Typ

Boolescher Werttypen können "true" oder "false" sein. Die Werte sind nicht Groß-/Kleinschreibung beachtet, damit Isread:false die gleichen Ergebnisse wie Isread:FALSE erzielt wird.
  
### <a name="using-a-number-value-type"></a>Verwenden einen Nummer Werttyp

Zahl Werttypen als nach genauen Übereinstimmungen durchsucht werden können, aber sie können auch durchsucht werden mit relationalen Operatoren wie größer oder kleiner als. Größe: 10000 werden beispielsweise nur auf Elemente mit einer Größe von genau 10000 Byte, aber Größe zurückgegeben:\>= 10000 werden Elemente mit einer Größe größer als oder gleich 10000 Byte zurückgegeben. Sie können auch einen Bereich mithilfe des Range-Operators ( **.**) angeben. Größe: 7000..8000 gibt beispielsweise Elemente zurück, die eine Größe zwischen 7000 und 8000 aufweisen. 
  
### <a name="using-logical-operators"></a>Verwenden von logischen Operatoren

Abfragezeichenfolgen unterstützt die folgenden logischen Operatoren.
  
**In Tabelle 2. Unterstützte logische Operatoren**

|**Operator**|**Beispiele**|
|:-----|:-----|
|AND  <br/> |Project und aus: "Sadie Daniels"  <br/> Betreff:(project AND plan)  <br/> |
|ODER  <br/> |Betreff: Besprechung oder aus: "Hoffe Brutto"  <br/> von: ("Sadie Daniels" oder "Hoffe Brutto")  <br/> |
|NOT  <br/> |NICHT aus: "Ronnie Sturgis"  <br/> empfangen: heute nicht mehr  <br/> |
   
Beachten Sie, dass Sie diese Operatoren zusammengefügt mehrerer Kriterien oder mehrere Werte in einem einzelnen Wert-Paar zusammengefügt verwenden können. Allerdings sollten bei der Teilnahme an mehrere Werte in einem einzelnen Schlüsselwort/Wert-Paar Sie Klammern verwenden mehrere Werte eingeschlossen wird. Um dies zu verstehen, sollten Sie mit Suche: "Sadie Daniels" oder "Hoffe Bruttogewicht". Diese Suche ist als die folgenden Kriterien tatsächlich interpretiert werden:
  
- Das Element hat ihren Ursprung Sadie Daniels, OR
    
- Das Element wurde dem Begriff "Hoffe Brutto" in seine indizierten Eigenschaften.
    
Im Gegensatz dazu aus: ("Sadie Daniels" oder "Hoffe Brutto") als interpretiert wird: 
  
- Das Element hat ihren Ursprung Sadie Daniels, OR
    
- Das Element hat ihren Ursprung hoffe Brutto
    
Ist der Standardoperator, wenn mehrere Kriterien angegeben werden, jedoch kein logischer Operator enthalten ist und. Beispielsweise hat Anlage: True Betreff: Projekt entspricht hat: Anlage: True und Betreff: Projekt.
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a>Beispiel: Suchen von Elementen mithilfe von einer Abfragezeichenfolge und die EWS Managed API
<a name="bk_ExampleEWSMA"> </a>

In diesem Beispiel wird eine Methode namens **SearchWithQueryString** definiert. Es wird ein [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, ein [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) -Objekt und ein **String** -Objekt, das als Parameter die Abfragezeichenfolge darstellt. In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde. 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void SearchWithQueryString(ExchangeService service, WellKnownFolderName folder, string queryString)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       ItemSchema.Size,
                                       ItemSchema.Importance,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Execute the search based on the query string.
        // Example: "subject:project plan"
        FindItemsResults<Item> results = service.FindItems(folder, queryString, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Received: {0}", item.DateTimeReceived.ToString());
            Console.WriteLine("Size: {0}", item.Size.ToString());
            Console.WriteLine("Importance: {0}", item.Importance.ToString());
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

Mit dieser Methode können Sie für alle Elemente mit dem Ausdruck "Projektplan" in der Betreffzeile suchen, wie im folgenden Beispiel dargestellt.
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a>Beispiel: Suchen von Elementen mithilfe eines Abfragezeichenfolge und Exchange-Webdienste
<a name="bk_ExampleEWS"> </a>

In diesem Beispiel sucht eine Anforderung SOAP- [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) alle Elemente im Posteingang mit dem Begriff "Projektplan" im Betreff. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="item:Size" />
          <t:FieldURI FieldURI="item:Importance" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:"project plan"</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt die Antwort vom Server mit den Suchergebnissen.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>project plan</t:Subject>
                <t:DateTimeReceived>2013-12-11T15:42:02Z</t:DateTimeReceived>
                <t:Size>7406</t:Size>
                <t:Importance>Normal</t:Importance>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Siehe auch

- [Suche und EWS in Exchange](search-and-ews-in-exchange.md)    
- [Verwenden Sie Suchfilter mit EWS in Exchange](how-to-use-search-filters-with-ews-in-exchange.md)    
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [FindItem-Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

