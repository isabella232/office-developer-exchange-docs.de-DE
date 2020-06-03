---
title: Durchführen einer AQS-Suche mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: c136901a-313e-4adf-a223-1d090d16917a
description: Erfahren Sie, wie Sie mit Abfragezeichenfolgen und AQS in ihrer verwaltete EWS-API-oder EWS-Anwendung suchen.
localization_priority: Priority
ms.openlocfilehash: 9f611a8d90c6baf0f307897735c6366c82bb63c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455716"
---
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a>Durchführen einer AQS-Suche mithilfe von EWS in Exchange

Erfahren Sie, wie Sie mit Abfragezeichenfolgen und AQS in ihrer verwaltete EWS-API-oder EWS-Anwendung suchen.
  
Abfragezeichenfolgen bieten eine Alternative zu [Suchfiltern](how-to-use-search-filters-with-ews-in-exchange.md) zum Ausdrücken von Suchkriterien. Der größte Vorteil bei der Verwendung von Abfragezeichenfolgen besteht darin, dass Sie keine einzelne zu durchsuchende Eigenschaft angeben müssen. Sie können nur einen Wert angeben, und die Suche wird auf alle häufig verwendeten Felder in den Elementen angewendet. Sie können die Suche auch verfeinern, indem Sie die Erweiterte Abfrage Syntax (AQS) anstelle eines einfachen Werts verwenden. Abfragezeichenfolgen weisen jedoch die folgenden Einschränkungen auf, die Sie kennen sollten, bevor Sie sie ihrer Toolbox hinzufügen: 
  
- **Beschränkte Fähigkeit zum Durchsuchen bestimmter Eigenschaften.** Wenn Sie mit einem einfachen Wert in einer Abfragezeichenfolge suchen, wird die Suche für alle indizierten Eigenschaften ausgeführt. Sie können die Suche auf bestimmte Eigenschaften verfeinern, die verfügbaren Eigenschaften in einer AQS-Zeichenfolge sind jedoch limitiert. Wenn die Eigenschaft, die Sie durchsuchen möchten, nicht zu den Eigenschaften gehört, die für AQS verfügbar sind, sollten Sie einen Suchfilter verwenden. 
    
- **Benutzerdefinierte Eigenschaften werden nicht durchsucht.** Abfragezeichen folgen suchen werden für einen Index ausgeführt, und benutzerdefinierte Eigenschaften sind nicht in diesem Index enthalten. Wenn Sie benutzerdefinierte Eigenschaften durchsuchen müssen, verwenden Sie stattdessen einen Suchfilter. 
    
- **Beschränkte Steuerung für Zeichenfolgensuchen.** Bei Abfragezeichen folgen suchen wird Case immer ignoriert, und es werden immer unter Zeichenfolgen Suchvorgänge durchsucht. Wenn Sie die Suche nach Groß-/Kleinschreibung, Präfix oder exakte Übereinstimmung durchführen möchten, verwenden Sie einen Suchfilter. 
    
- **Nicht verfügbar für Ordner oder Suchordner.** Die EWS-Vorgänge für die Suche nach Ordnern unterstützen nicht die Verwendung einer Abfragezeichenfolge. Außerdem unterstützen Suchordner keine Abfragezeichenfolgen. In beiden Fällen ist ein Suchfilter die einzige Option. 
    
## <a name="creating-a-query-string"></a>Erstellen einer Abfragezeichenfolge
<a name="bk_CreateQueryString"> </a>

Abfragezeichenfolgen im verwaltete EWS-API und EWS werden als Teilmenge der AQS-Syntax interpretiert. AQS-Zeichenfolgen bestehen entweder aus Werten oder aus Schlüsselwort/Wert-Paaren, getrennt durch einen Doppelpunkt (:).
  
`keyword:value`

Wenn ein Wert ohne Schlüsselwort angegeben wird, werden alle indizierten Eigenschaften nach dem Wert durchsucht. Wenn ein Schlüsselwort mit einem Wert gekoppelt wird, gibt das Schlüsselwort eine Eigenschaft zum Suchen nach dem entsprechenden Wert an.
  
**Tabelle 1. Unterstützte AQS-Schlüsselwörter**

|**Schlüsselwort**|**Werttyp**|**Beispiel**|
|:-----|:-----|:-----|
|Betreff  <br/> |Zeichenfolge  <br/> |Betreff: Project  <br/> |
|body  <br/> |Zeichenfolge  <br/> |Body: Verkaufszahlen  <br/> |
|attachment  <br/> |Zeichenfolge  <br/> |Anlage: Bericht  <br/> |
|in  <br/> |Zeichenfolge  <br/> |an: "Sadie Daniels"  <br/> |
|Von  <br/> |Zeichenfolge  <br/> |von: Hope  <br/> |
|cc  <br/> |Zeichenfolge  <br/> |cc: "Ronnie Kardinal"  <br/> |
|bcc  <br/> |Zeichenfolge  <br/> |BCC: Mack  <br/> |
|participants  <br/> |Zeichenfolge  <br/> |Teilnehmer: Sadie  <br/> |
|category  <br/> |String  <br/> |Kategorie: Project  <br/> |
|Wichtigkeit  <br/> |String  <br/> |Wichtigkeit:Hoch  <br/> |
|kind  <br/> |Elementtyp  <br/> |Art: Besprechungen  <br/> |
|sent  <br/> |Datum  <br/> |gesendet: 12/10/2013  <br/> |
|received  <br/> |Datum  <br/> |empfangen: Gestern  <br/> |
|hatanlage  <br/> |Boolean  <br/> |Has-Anlage: true  <br/> |
|isflaged  <br/> |Boolean  <br/> |isflaged: true  <br/> |
|isread  <br/> |Boolean  <br/> |isread: false  <br/> |
|size  <br/> |Nummer  <br/> |Größe: \> 5000  <br/> |
   
Werfen wir einen Blick auf die Funktionsweise der unterschiedlichen Wertetypen.
  
### <a name="using-a-string-value-type"></a>Verwenden eines Zeichenfolgen Werttyp

Zeichenfolgenwerte Typen werden standardmäßig als Präfix-Teil Zeichenfolgensuche durchsucht, bei denen die Groß-/Kleinschreibung nicht beachtet wird. Das bedeutet, dass die Suche nach Subject: Project mit einem der folgenden Themen übereinstimmen würde: 
  
- Projekt-Besprechungsnotizen
    
- Haben Sie die Projektpläne?
    
- Verkaufsprognosen im Dezember
    
Sie können die Suche so ändern, dass das ganze Wort statt übereinstimmender Präfixe erforderlich ist, indem Sie die Zeichenfolge in Anführungszeichen einschließen. Durchsuchen des Betreffs: "Project" würde den Wert "Dezember Sales Projektionen" aus der Liste der Übereinstimmungen ausschließen. Beachten Sie, dass bei dem Wert weiterhin die Groß-/Kleinschreibung beachtet wird. 
  
Wenn Sie mehrere Wörter in einer Abfragezeichenfolge verwenden, erfordert eine Übereinstimmung, dass beide Wörter in den durchsuchten Feldern angezeigt werden. Beispielsweise würde die Suche nach Subject: Project Plan mit einem der folgenden Themen übereinstimmen: 
  
- Projektplan
    
- Haben Sie die Projektpläne?
    
- Bitte senden Sie mir den Plan für unser Projekt
    
- Planen von Projektmeilensteinen
    
Wenn Sie mehrere Wörter in Anführungszeichen einschließen, werden Sie als einzelne Phrase behandelt. Die Suche nach Betreff: "Projektplan" würde nur dem Betreff "Projektplan" aus der vorherigen Liste entsprechen. 
  
### <a name="using-an-item-type-value-type"></a>Verwenden eines Werttyp Werts für den Typ "Item"

Sie können die folgenden Elementtyp Werte mit dem Schlüsselwort **Kind** verwenden, um die Suchergebnisse auf einen bestimmten Elementtyp wie e-Mail oder Besprechungsanfragen einzuschränken: 
  
- contacts    
- docs    
- email    
- faxes    
- Chat (entspricht Chatnachrichten)    
- journals    
- Besprechungen (entspricht Terminen und Besprechungsanfragen)    
- notes    
- posts    
- rssfeeds    
- tasks    
- voicemail
    
### <a name="using-a-date-value-type"></a>Verwenden eines Datums Werttyp

Sie können Datumswert Typen auf verschiedene Weise durchsuchen. Am einfachsten ist die Suche nach einem bestimmten Datum. Bei der Suche mit Received: 12/11/2013 werden alle Elemente zurückgegeben, die am 11. Dezember 2013 empfangen wurden. Sie können jedoch auch nicht so spezifisch sein. Bei der Suche mit Received: 12/11 werden alle Elemente zurückgegeben, die am 11. Dezember des aktuellen Jahres empfangen wurden. 
  
Eine weitere Option besteht darin, die Monatsnamen zu verwenden. Sie können mit received suchen: 11. Dezember 2013 oder 11. Dezember, um die gleichen Ergebnisse wie empfangen zu erhalten: 12/11/2013 und Received: 12/11, beziehungsweise. Sie können auch mit Received: Dezember suchen, um alle Elemente abzurufen, die im Monat Dezember im aktuellen Jahr empfangen wurden. 
  
Die Verwendung der Namen der Wochentage ist ebenfalls eine Option. Bei der Suche mit Received: Dienstag werden alle Elemente zurückgegeben, die am Dienstag der aktuellen Woche empfangen wurden. 
  
Datumswert Typen unterstützen auch eine Reihe von Schlüsselwörtern für Suchvorgänge relativ zur aktuellen Uhrzeit. Die folgenden Schlüsselwörter werden unterstützt:
  
- heute  
- morgen
- yesterday
- this week    
- Letzte Woche    
- Nächster Monat    
- vergangener Monat    
- kommendes Jahr
    
Datumswert Typen können auch mit relationalen Operatoren wie größer als oder kleiner als oder als Bereich mit dem Range-Operator angegeben werden **..**. Angenommen: \> 11/30/2013, Sent: \> = Yesterday und Received: 12/1/2013.. heute sind alle gültigen Abfragezeichenfolgen. 
  
### <a name="using-a-boolean-value-type"></a>Verwenden eines Werts vom Typ Boolean

Boolesche Wertetypen können "true" oder "false" lauten. Bei den Werten wird die Groß-/Kleinschreibung nicht beachtet, daher erzeugt isread: false dieselben Ergebnisse wie isread: false.
  
### <a name="using-a-number-value-type"></a>Verwenden eines Zahlen Werttyp

Zahl Wert Typen können als exakte Übereinstimmungen durchsucht werden, Sie können aber auch mithilfe relationaler Operatoren wie größer als oder kleiner als durchsucht werden. Beispielsweise gibt size: 10000 nur Elemente zurück, die eine Größe von genau 10000 Bytes aufweisen, aber size: \> = 10000 gibt Elemente zurück, deren Größe größer als oder gleich 10000 Bytes ist. Sie können auch einen Bereich mithilfe des Bereichsoperators ( **..**) angeben. Beispielsweise gibt size: 7000.. 8000 Elemente zurück, die eine Größe zwischen 7000 und 8000 haben. 
  
### <a name="using-logical-operators"></a>Verwenden von logischen Operatoren

Abfragezeichenfolgen unterstützen die folgenden logischen Operatoren.
  
**Tabelle 2. Unterstützte logische Operatoren**

|**Operator**|**Beispiele**|
|:-----|:-----|
|UND  <br/> |Projekt und von: "Sadie Daniels"  <br/> Subject: (Projekt und Plan)  <br/> |
|ODER  <br/> |Betreff: Meeting oder von: "Hope gross"  <br/> aus:("Sadie Daniels" oder "Hope gross")  <br/> |
|NICHT  <br/> |Nicht von: "Ronnie McCulloch"  <br/> empfangen: nicht heute  <br/> |
   
Beachten Sie, dass Sie diese Operatoren verwenden können, um mehrere Kriterien miteinander zu verknüpfen oder um mehrere Werte in einem einzelnen Schlüsselwort/Wert-Paar miteinander zu verbinden. Wenn Sie jedoch mehrere Werte in einem einzelnen Schlüsselwort/Wert-Paar verknüpfen, sollten Sie Klammern verwenden, um mehrere Werte einzuschließen. Um zu verstehen, warum, sollten Sie die Suche mit von: "Sadie Daniels" oder "Hope gross". Diese Suche wird tatsächlich als die folgenden Kriterien interpretiert:
  
- Das Element stammt aus Sadie Daniels oder
    
- Das Element hat den Ausdruck "Hope gross" in einer seiner indizierten Eigenschaften.
    
Im Gegensatz dazu wird aus:("Sadie Daniels" oder "Hope gross") als Folgendes interpretiert: 
  
- Das Element stammt aus Sadie Daniels oder
    
- Das Element ist von der Hoffnung Brutto
    
Der Standardoperator, wenn mehrere Kriterien angegeben werden, aber kein logischer Operator enthalten ist, ist und. Enthält beispielsweise Attachment: true Subject: Project entspricht has: Attachment: true und Subject: Project.
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a>Beispiel: Suchen von Elementen mithilfe einer Abfragezeichenfolge und der verwaltete EWS-API
<a name="bk_ExampleEWSMA"> </a>

In diesem Beispiel wird eine Methode namens " **SearchWithQueryString** " definiert. Es benötigt ein [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, ein [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) -Objekt und ein **String** -Objekt, das die Abfragezeichenfolge als Parameter darstellt. In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde. 
  
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

Sie können diese Methode verwenden, um nach allen Elementen mit dem Ausdruck "Projektplan" im Betreff zu suchen, wie in diesem Beispiel gezeigt.
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a>Beispiel: Suchen von Elementen mithilfe einer Abfragezeichenfolge und EWS
<a name="bk_ExampleEWS"> </a>

In diesem Beispiel findet eine SOAP- [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Anforderung alle Elemente im Posteingang mit dem Ausdruck "Projektplan" im Betreff. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Im folgenden Beispiel wird die Antwort vom Server mit den Suchergebnissen dargestellt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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
- [Verwenden von Suchfiltern mit EWS in Exchange](how-to-use-search-filters-with-ews-in-exchange.md)    
- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

