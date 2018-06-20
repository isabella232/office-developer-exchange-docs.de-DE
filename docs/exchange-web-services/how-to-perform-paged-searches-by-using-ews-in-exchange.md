---
title: Führen Sie seitenweise durch Verwenden von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64ed70e4-32eb-4c25-bfc4-43d1477296e5
description: Erfahren Sie, wie Sie seitenweise in die EWS Managed API oder EWS-Anwendung, die beruht auf Exchange ausführen.
ms.openlocfilehash: 3f82f46d0582b0b7ff8be63de8a7054b5f3cacab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756980"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a>Führen Sie seitenweise durch Verwenden von EWS in Exchange

Erfahren Sie, wie Sie seitenweise in die EWS Managed API oder EWS-Anwendung, die beruht auf Exchange ausführen.
  
Auslagerungsdatei ist ein Feature in der Exchange-Webdienste, mit dem Sie die Größe der Ergebnisse einer Suche steuern können. Anstatt das gesamte Resultset in eine EWS-Antwort abzurufen, können Sie kleinere Inhaltssätze in mehreren EWS-Antworten abrufen. Angenommen Sie, einen Benutzer mit 10.000 e-Mail-Nachrichten in ihren Posteingang. Wenn, Sie konnte alle 10.000-e-Mails in eine sehr große Antwort abrufen, jedoch möglicherweise möchten Sie, die mehrere Blöcken aus Gründen der Bandbreite oder Leistung aufteilen. Paging können Sie die Tools, die genau das, was.
  
> [!NOTE]
> Während Sie 10.000 Elemente in einer Anforderung, wenn in der Praxis abrufen können, ist dies unwahrscheinlich EWS-Einschränkung. Wenn Sie mehr erfahren möchten, finden Sie unter [EWS-Einschränkung im Exchange](ews-throttling-in-exchange.md). 
  
**In Tabelle 1. Pagingparameter in die EWS Managed API und die Exchange-Webdienste**

|**So konfigurieren oder Abrufen der...**|**Verwenden Sie in die EWS Managed API...**|**Verwenden Sie in der Exchange-Webdienste...**|
|:-----|:-----|:-----|
|Maximale Anzahl von Elementen oder Ordner in einer Antwort  <br/> |Die **PageSize** -Parameter für den [Konstruktor aufrufenArtikel aufrufen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) oder den [FolderView-Konstruktor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx) <br/> Oder  <br/> Die [PagedView.PageSize](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |Das Attribut **"MaxEntriesReturned"** auf dem [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) -Element oder das [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) -element  <br/> |
|Startpunkt in der Liste der Elemente oder Ordner  <br/> |Der Parameter **OffsetBasePoint** an den Konstruktor **aufrufenArtikel aufrufen** oder die **FolderView** -Konstruktor  <br/> Oder  <br/> Die [PagedView.OffsetBasePoint](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |Das Attribut **Basispunkt** auf dem **IndexedPageItemView** -Element oder das **IndexedPageFolderView** -element  <br/> |
|Abstand vom Ausgangspunkt  <br/> |Der Parameter **Offset** an den Konstruktor **aufrufenArtikel aufrufen** oder die **FolderView** -Konstruktor  <br/> Oder  <br/> Die [PagedView.Offset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |Das Attribut **Offset** für das Element **IndexedPageItemView** oder das **IndexedPageFolderView** -element  <br/> |
|Gesamtanzahl der Ergebnisse auf dem server  <br/> |Die [FindItemsResults.TotalCount](http://msdn.microsoft.com/en-us/library/dd635348%28v=exchg.80%29.aspx) -Eigenschaft oder die [FindFoldersResults.TotalCount](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |Das **TotalItemsInView** -Attribut für das Element [RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) oder das Element [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)  <br/> |
|Offset des ersten Elements oder Ordners in der aktuellen Antwort nicht enthalten  <br/> |Die [FindItemsResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/ee693014%28v=exchg.80%29.aspx) -Eigenschaft oder die [FindFoldersResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |Das Attribut **IndexedPagingOffset** die **RootFolder** -element  <br/> |
|Symbol, dass die Antwort des letzten Elements oder Ordners in der Liste enthält  <br/> |Die [FindItemsResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/dd635477%28v=exchg.80%29.aspx) -Eigenschaft oder die [FindFoldersResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |Das Attribut **IncludesLastItemInRange** die **RootFolder** -element  <br/> |
   
## <a name="how-paging-works"></a>Funktionsweise von paging
<a name="bk_HowPagingWorks"> </a>

Zum Verständnis der Funktionsweise der Auslagerungsdatei ist es hilfreich, die Nachrichten in einem Ordner als horizontal/vertikal ausgerichtet nebeneinander in einem Feld außerhalb Haus an visualisieren. Sie können einige dieser an über das magische Fenster sehen. Sie haben die Möglichkeit zum Ändern der Größe des Fensters (mehr oder weniger an gleichzeitig finden Sie unter) und das Fenster (zu steuern, welche an, die Sie sehen) zu verschieben. Diese Manipulation des Fensters paging ist. 
  
Wenn Sie Ihre Anforderung an den Exchange-Server senden, geben Sie die Größe des Fensters hinsichtlich der Anzahl der Elemente zurückgegeben. Die Position des Fensters festlegen durch Angabe Ausgangspunkt (am Anfang der Zeile) oder das Ende der Zeile und einem Offset aus den Ausgangspunkt, ausgedrückt als eine Anzahl von Elementen. Der Anfang des Fensters ist die Anzahl der Elemente, die durch den Offset vom Anfangspunkt angegeben.
  
Wobei Paging etwas interessant ist in der Antwort des Servers, und wie Ihre Anwendung Antwort an die nächste Anforderung shape verwenden kann. Der Server gibt Ihnen drei Angaben, die Sie verwenden können, zu bestimmen, wie das "Fenster" für die nächste Anforderung zu konfigurieren: 
  
- Gibt an, ob die Ergebnisse in der Antwort das letzte Element in der gesamten Ergebnismenge auf dem Server enthalten.
    
- Die Gesamtzahl der Elemente in der Ergebnismenge auf dem Server.
    
- Was sollte der nächste Offsetwert sein sollten Sie das Fenster auf das nächste Element im Resultset zur nächsten Folie gewechselt, die nicht in der aktuellen Antwort steht.
    
Sehen wir uns ein einfaches Beispiel. Stellen Sie sich vor einem Posteingang mit 15 Beiträge. Die Anwendung sendet eine anfängliche Anforderung zum Abrufen von maximal 10 Elemente, beginnend am Anfang der Liste der Nachrichten (damit der Offset gleich 0 (null) ist). Der Server antwortet mit der ersten 10 Nachrichten und gibt an, dass die Antwort nicht enthalten, ist das letzte Element, das, dass es werden insgesamt 15 Elementen und der nächste Offset 10 werden soll.
  
**Abbildung 1. Anforderns von 10 Elementen bei Offset 0 am Anfang einer Liste mit 15 Elementen**

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 0 am dem Anfang einer Liste mit 15 Elementen.](media/Ex15_PagedSearch_FirstPage.png)
  
Klicken Sie dann die Anwendung sendet derselben Anforderung an den Server, mit der nur ändern, dass der Offset jetzt 10 ist. Der Server gibt den letzten fünf Elemente zurück, und gibt an, dass die Antwort enthält das letzte Element, das, dass es werden insgesamt 15 Elementen und der nächste Offset 15 werden soll (obwohl natürlich Sie am Ende erreicht haben und kein nächsten Offset.)
  
**Abbildung 2. Anfordern von 10 Elementen bei Offset 10 vom Anfang einer Liste mit 15 Elementen**

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 0 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Anfang der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a>Entwurfsaspekte für die Auslagerung
<a name="bk_DesignConsiderations"> </a>

Optimale Nutzung Paging in Ihrer Anwendung erfordert einige berücksichtigt. Beispielsweise wie groß gemacht Sie Ihr "Fenster"? Was tun Sie, wenn die Ergebnisse auf dem Server ändern, während Sie Ihr "Fenster" verschieben?
  
### <a name="determine-the-size-of-your-window"></a>Bestimmen Sie die Größe des Fensters

Es ist keine "Stange" maximale Anzahl von Einträgen, die alle Anwendungen verwendet werden soll. Bestimmen der Anzahl, die für Ihre Anwendung geeignet ist, hängt von verschiedenen Faktoren ab. Jedoch ist es hilfreich, die folgenden Richtlinien im Hinterkopf behalten:
  
- Standardmäßig begrenzt Exchange die maximale Anzahl der Elemente, die in einer einzelnen Anforderung bis 1000 zurückgegeben werden kann.
    
- Durch Festlegen der maximalen Anzahl der Einträge auf eine größere Zahl zu müssen weniger Anfragen zum Abrufen aller Elemente, aber mehr Antworten warten müssen.
    
- Die maximale Anzahl von Einträgen aus der festlegen auf einer kleineren Anzahl Ergebnisse schnellere Antwortzeiten Kosten für weitere Anfragen zum Abrufen aller Elemente müssen.
    
### <a name="handling-changes-to-the-result-set"></a>Behandlung von Änderungen an dem Resultset

In der einfachen Beispiel weiter oben in diesem Artikel blieb die Anzahl der Elemente im Posteingang des Benutzers Konstante. Die Anzahl der Elemente im Posteingang kann jedoch in der Praxis häufig ändern. Neue Nachrichten eingehen können und Elemente gelöscht oder zu einem beliebigen Zeitpunkt verschoben werden können. Aber wie führt diese Auswirkungen Paging? Lassen Sie uns ändern das frühere Beispielszenario Sie herausfinden können.
  
Wir beginnen Sie erneut mit der 15 Elementen im Posteingang des Benutzers und die gleiche anfängliche Anforderung senden. Als vor, der Server antwortet mit der ersten 10 Nachrichten und gibt an, dass die Antwort das letzte Element, das, dass es werden insgesamt 15 Elementen und der nächste Offset 10, sollten nicht einschließen, wie in Abbildung 1 dargestellt.
  
Nun, während die Anwendung die 10 Elemente verarbeitet wird, eine neue Nachricht im Posteingang eingeht und das Resultset auf dem Server hinzugefügt wird. Die Anwendung sendet die gleiche Anforderung an den Server (nur mit der Offset auf 10). Diesmal der Server ruft zurück sechs Elemente ab und gibt an, dass insgesamt 16 Elemente im Resultset.
  
An dieser Stelle Sie vielleicht, wenn dies auch ein Problem darstellt. Schließlich haben Sie 16 Elemente wieder über die zwei Antworten, warum also ganze? Die Antwort hängt davon ab, wo in der Liste das neue Element platziert wird. Wenn die Liste sortiert wird, damit die ältesten Elemente (nach Empfangsdatum samt Uhrzeit) erste sind, ist keine Ursache für Herausforderung in diesem Szenario. Das neue Element wird am Ende der Liste eingefügt werden, und wird in der zweiten Antwort enthalten sein.
  
**Abbildung 3. Anfordern von 10 Elementen bei Offset 10 vom Anfang einer Liste von 16 Elemente mit dem 16. Element in der Liste neue wird**

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Ende der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
Wenn die Liste sortiert wird, damit die neuesten Elemente ersten sind, ist es anders. In diesem Fall würde das erste Element in der zweiten Anforderung das letzte Element aus der vorherigen Anforderung plus die verbleibenden fünf Elemente aus der ursprünglichen 15 sein. Im Hinblick auf unser imaginäre magische Fenster ausgedrückt, verschoben Sie Position des Fensters um 10, aber die an sich selbst auch um verschoben, 1.
  
**Abbildung 4. Anfordern von 10 Elementen bei Offset 10 vom Anfang einer Liste von 16 Elemente mit dem ersten Element in der Liste neue wird**

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Anfang der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
Eine Möglichkeit, eine Änderung auf die Ergebnisse auf dem Server zu erkennen ist das Konzept eines Anker-Elements verwenden. Ein Anker-Element ist ein zusätzliches Element in Ihre Antwort, die nicht zusammen mit dem Rest der Ergebnisse verarbeitet wird, aber wird verwendet, um mit der nächsten Ergebnisse zu sehen, ob die Elemente selbst verschoben wurden vergleichen. Erstellen in unserem einfachen Beispiel erneut, wenn der Anwendung eine "" Fenstergröße von 10 verwendet wird, legen Sie tatsächlich die maximale Anzahl von Elementen, die zur 11 zurückzukehren. Die Anwendung verarbeitet die ersten 10 Elemente in der Antwort auf wie gewohnt. Für das letzte Element der Element-ID als Anker speichern und dann die nächste Anforderung mit einem Offset von 10 ausstellen. Wenn die Daten nicht geändert wurde, sollte das erste Element in der zweiten Antwort eine Element-ID, die mit den Anker übereinstimmt. Wenn die Element-IDs nicht übereinstimmen, wissen Sie, dass die Daten wurden entfernt oder in den Teilen der Liste, die Sie bereits "ausgelagert haben" eingefügt über.
  
Auch wenn Sie wissen, dass die Daten geändert haben, müssen Sie dennoch entscheiden, wie Sie reagieren. Es ist nicht entweder eine Stange Antwort für diese Frage ein. Ihre Aktionen hängt die Art der Anwendung und wie wichtig die Erfassen aller Elemente ist. Möglicherweise vollständig zu ignorieren, starten den Prozess von der Anfang oder Sichern nachverfolgen und versuchen, zu ermitteln, in dem die Änderung erfolgt.
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a>Beispiel: Führen Sie eine ausgelagerte Suche mithilfe der EWS Managed API
<a name="bk_PagedSearchEWSMA"> </a>

Paging wird von den folgenden EWS Managed API-Methoden unterstützt:
  
- [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
Wenn Sie die EWS Managed API verwenden, wird die Anwendung Paging mit der Klasse [aufrufenArtikel aufrufen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) oder [FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) konfiguriert und empfängt Informationen von dem Server im Hinblick auf Paging von [FindItemsResults](http://msdn.microsoft.com/en-us/library/dd635381%28v=exchg.80%29.aspx) oder [FindFoldersResults](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) -Klasse. 
  
Das folgende Beispiel ruft alle Elemente in einem Ordner mithilfe einer ausgelagerten Suche, die fünf Elemente in jeder Antwort zurückgegeben. Es ruft auch ein weiteres Element dienen als Anker zum Erkennen von Änderungen an die Ergebnisse auf dem Server ab. 
  
In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde. 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void PageSearchItems(ExchangeService service, WellKnownFolderName folder)
{
    int pageSize = 5;
    int offset = 0;
    // Request one more item than your actual pageSize.
    // This will be used to detect a change to the result
    // set while paging.
    ItemView view = new ItemView(pageSize + 1, offset);
    view.PropertySet = new PropertySet(ItemSchema.Subject);
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    view.Traversal = ItemTraversal.Shallow;
    bool moreItems = true;
    ItemId anchorId = null;
    while (moreItems)
    {
        try
        {
            FindItemsResults<Item> results = service.FindItems(folder, view);
            moreItems = results.MoreAvailable;
            if (moreItems &amp;&amp; anchorId != null)
            {
                // Check the first result to make sure it matches
                // the last result (anchor) from the previous page.
                // If it doesn't, that means that something was added
                // or deleted since you started the search.
                if (results.Items.First<Item>().Id != anchorId)
                {
                    Console.WriteLine("The collection has changed while paging. Some results may be missed.");
                }
            }
            if (moreItems)
                view.Offset += pageSize;
            anchorId = results.Items.Last<Item>().Id;
            // Because you're including an additional item on the end of your results
            // as an anchor, you don't want to display it.
            // Set the number to loop as the smaller value between
            // the number of items in the collection and the page size.
            int displayCount = results.Items.Count > pageSize ? pageSize : results.Items.Count;
            for (int i = 0; i < displayCount; i++)
            {
                Item item = results.Items[i];
                Console.WriteLine("Subject: {0}", item.Subject);
                Console.WriteLine("Id: {0}\n", item.Id.ToString());
            }
        }
        catch (Exception ex)
        {
            Console.WriteLine("Exception while paging results: {0}", ex.Message);
        }
    }
}
```

## <a name="example-perform-a-paged-search-by-using-ews"></a>Beispiel: Führen Sie eine ausgelagerte Suche mithilfe der Exchange-Webdienste
<a name="bk_PagedSearchEWS"> </a>

Paging wird durch folgende EWS-Vorgänge unterstützt:
  
- [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
Wenn Sie Exchange-Webdienste verwenden, wird die Anwendung Paging mit der [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) -Element oder das Element [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) konfiguriert und empfängt Informationen von dem Server im Hinblick auf Paging aus der [RootFolder () FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) Element oder das Element [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) . 
  
In diesem anforderungsbeispiel wird eine **FindItem** -Anforderung für ein Maximum von sechs Elementen, beginnend bei einem Offset 0 (null) am Anfang der Liste der Elemente im Posteingang des Benutzers gesendet. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="6" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Der Server gibt die folgende Antwort, die sechs Elemente enthält. Die Antwort gibt auch an, dass insgesamt acht Elemente in den Ergebnissen auf dem Server vorhanden sind und dass das letzte Element in der Liste "Suchergebnisse" nicht in der Antwort vorhanden ist.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="6" TotalItemsInView="8" IncludesLastItemInRange="false">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Query</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Update</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Planning resources</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Timeline</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>For your perusal</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

In diesem Beispiel wird die gleiche Anforderung wird gesendet, aber diesmal das **Offset** -Attribut auf fünf, die angibt, dass der Server maximal sechs Artikel beginnend am Offset fünf vom Anfang zurückgegeben werden soll, geändert wird. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="6" Offset="5" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Der Server sendet die folgende Antwort, die drei Elemente enthält. Die Antwort gibt auch an, dass die Gesamtanzahl der Elemente in den Ergebnissen auf dem Server ist weiterhin acht festgelegt, und das letzte Element in den Ergebnissen Liste in der Antwort enthalten ist.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="8" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting notes</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>This cat is hilarious!</t:Subject>
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
    
- [ExchangeService.FindFolders-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [FindFolder Operation](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [FindItem-Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [EWS-Einschränkung in Exchange](ews-throttling-in-exchange.md)
    

