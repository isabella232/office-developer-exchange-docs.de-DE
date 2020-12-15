---
title: Seitensuchen mithilfe von EWS in Exchange durchführen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 64ed70e4-32eb-4c25-bfc4-43d1477296e5
description: Lernen Sie, wie Sie Seitensuchen in Ihrem verwalteten EWS-API oder EWS-Anwendung, die auf Exchange zielen, durchführen können.
localization_priority: Priority
ms.openlocfilehash: fa36a2ce77150f29e5a62876138c9693a3b4ab1f
ms.sourcegitcommit: 37d4ecd4f469690ba1de87baad2f2f58c40c96ba
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "49348822"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a>Seitensuchen mithilfe von EWS in Exchange durchführen

Lernen Sie, wie Sie Seitensuchen in Ihrem verwalteten EWS-API oder EWS-Anwendung, die auf Exchange zielen, durchführen können.
  
Das Paging ist ein Feature in EWS, das es Ihnen ermöglicht, die Größe der Ergebnisse einer Suche zu steuern. Statt das ganze Resultset in einer EWS-Antwort abzurufen, können Sie kleinere Sets in mehreren EWS-Antworten abrufen. Erwägen Sie z.B. einen Benutzer, der 10 000 Emails in seinem Posteingang hat. Hypothetisch könnten Sie alle 10 000 Emails in einer einzigen sehr großen Antwort abrufen, Sie könnten es jedoch in mehrere übersichtlichere Teile trennen wollen, um eine bessere Bandbreite und Leistung zu gewährleisten. Das Paging bietet Ihnen die Tools um genau das machen zu können.
  
> [!NOTE]
> Sie können zwar hypothetisch 10 000 Elemente in einer Anforderung abrufen, tatsächlich ist es jedoch wegen der EWS-Drosselung unwahrscheinlich. Weiter Informationen finden Sie unter [EWS-Drosselung in Exchange](ews-throttling-in-exchange.md). 
  
**Tabelle 1. Das Paging in der verwalteten EWS-API und EWS**

|**Um die...** zu konfigurieren und abzurufen|**Verwalten Sie in der verwalteten EWS-API...**|**Verwalten Sie in EWS...**|
|:-----|:-----|:-----|
|Maximale Anzahl von Elementen oder Ordnern in einer Antwort  <br/> |Die **pageSize**-Parameter zum [ItemView-Konstruktor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) oder dem [FolderView-Konstruktor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx) <br/> Oder  <br/> Die [PagedView.PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx)-Eigenschaft  <br/> |Das **MaxEntriesReturned**-Attribut auf dem [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)-Element oder das [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)-Element  <br/> |
|Ausgangspunkt in der Liste der Elemente oder Ordner  <br/> |Die **offsetBasePoint**-Parameter zum **ItemView**-Konstruktor oder dem **FolderView**-Konstruktor  <br/> Oder  <br/> Die [PagedView.OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx)-Eigenschaft  <br/> |Das **BasePoint**-Attribut auf dem **IndexedPageItemView**-Element oder das **IndexedPageFolderView**-Element  <br/> |
|Offset vom Ausgangspunkt  <br/> |Das **Offset**-Parameter zum **ItemView**-Konstruktor oder dem **FolderView**-Konstruktor  <br/> Oder  <br/> Die [PagedView.Offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx)-Eigenschaft  <br/> |Das **Offset**-Attribut auf dem **IndexedPageItemView**-Element oder das **IndexedPageFolderView**-Element  <br/> |
|Gesamtnummer der Ergebnisse auf dem Server  <br/> |Die [FindItemsResults.TotalCount](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx)-Eigenschaft oder die [FindFoldersResults.TotalCount](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx)-Eigenschaft  <br/> |Das **TotalItemsInView**-Attribut auf dem [RootFolder(FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx)-Element oder dem [RootFolder(FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)-Element  <br/> |
|Offset des ersten Elements oder Ordners ist nicht in der aktuellen Antwort enthalten  <br/> |Die [FindItemsResults.NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx)-Eigenschaft oder die [FindFoldersResults.NextPageOffset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx)-Eigenschaft  <br/> |Das **IndexedPagingOffset**-Attribut auf dem **RootFolder**-Element  <br/> |
|Indikator, dass die Antwort das letzte Element oder den letzten Ordner in der Liste enthält  <br/> |Die [FindItemsResults.MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx)-Eigenschaft oder die [FindFoldersResults.MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx)-Eigenschaft  <br/> |Das **IncludesLastItemInRange**-Attribut auf dem **RootFolder**-Element  <br/> |
   
## <a name="how-paging-works"></a>Funktionsweise des Pagings
<a name="bk_HowPagingWorks"> </a>

Um zu verstehen, wie das Paging funktioniert, ist es hilfreich die Nachrichten in einem Ordner als nebeneinander angeordnete Billboards in einem Feld außerhalb Ihres Hauses zu visualisieren. Sie können einige dieser Billboards durch ein magisches Fenster sehen. Sie können die Größe des Fensters ändern (um eine größere oder kleinere Anzahl der Billboards zu sehen) und Sie können das Fenster verlagern (um zu steuern, welche Billboards Sie sehen und welche nicht). Diese Manipulation des Fensters ist das Paging. 
  
Wenn Sie Ihre Anforderung an den Exchange-Server senden, spezifizieren Sie die Größe Ihres Fensters im Hinblick auf die Zahl der Elemente, die zurückgesendet werden sollen. Sie bestimmen die Position des Fensters, indem Sie einen Ausgangspunkt bestimmen (entweder den Anfang der Zeile oder das Ende der Zeile) und ein Offset von diesem Ausgangspunkt, der in einer Nummer von Elementen angegeben wird. Der Anfang des Fensters ist die Nummer der Elemente, die durch den Offset vom Ausgangspunkt bestimmt wurden.
  
Das Paging fängt an ein bisschen spannender zu sein, wenn es um die Antwort des Servers geht, und darum, wie Ihre Anwendung diese Antwort verwenden kann, um ihre nächste Anforderung zu gestalten. Der Server stellt Ihnen drei Informationen bereit, die Sie dazu verwenden können, um zu bestimmen, wie Ihr „Fenster“ für Ihre nächste Anforderung konfiguriert werden soll: 
  
- Ob die Ergebnisse in der Antwort das letzte Element in der Gesamtergebnismenge auf dem Server enthalten.
    
- Die Gesamtzahl der Elemente im Resultset auf dem Server.
    
- Was der nächste Offsetwert sein sollte, wenn Sie das Fenster zum nächsten Element im Resultset bringen möchten, das in der aktuellen Antwort nicht enthalten ist.
    
Betrachten wir ein einfaches Beispiel. Stellen Sie sich einen Posteingang mit 15 Nachrichten vor. Ihre Anwendung sendet eine anfängliche Anforderung, um maximal 10 Elemente abzurufen, beginnend am Anfang der Liste der Nachrichten (sodass der Offset gleich Null ist). Der Server antwortet mit den ersten 10 Nachrichten und gibt an, dass die Antwort das letzte Element nicht beinhaltet, dass insgesamt 15 Elemente vorhanden sind, und dass der nächste Offset 10 sein sollte.
  
**Abbildung 1. Anfordern von 10 Elementen bei Offset 0 ab dem Anfang einer Liste mit 15 Elementen**

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 0 am dem Anfang einer Liste mit 15 Elementen.](media/Ex15_PagedSearch_FirstPage.png)
  
Ihre Anwendung sendet dann erneut die gleichen Anforderungen an den Server, wobei die einzige Änderung darin besteht, dass der Offset jetzt 10 gleicht. Der Server gibt die letzten fünf Elemente zurück und gibt an, dass die Antwort nicht das letzte Elemente enthält, dass insgesamt 15 Elemente vorhanden sind, und dass der nächste Offset 15 sein sollte (obwohl Sie natürlich das Ende erreich haben und demnach kein weiterer Offset folgen wird.)
  
**Abbildung 2. Anfordern von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 15 Elementen**

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 15 Elementen.](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a>Entwurfsaspekte für das Paging
<a name="bk_DesignConsiderations"> </a>

Um das Paging in Ihrer Anwendung optimal zu nutzen, müssen Sie sich einige Aspekte gründlich überlegen. Beispielsweise, wie groß wollen Sie Ihr „Fenster“ machen? Was machen Sie, wenn sich die Ergebnisse auf dem Server ändern, während Sie das „Fenster“ verschieben? 
  
### <a name="determine-the-size-of-your-window"></a>Die Größe des Fensters bestimmen

Es gibt keine „universale“ maximale Eintragnummer, die alle Anwendungen verwenden sollten. Das Bestimmen der für Ihre Anwendung geeigneten Nummer hängt von mehreren Faktoren ab. Es empfiehlt sich allerdings die folgenden Richtlinien im Kopf zu behalten:
  
- Standardmäßig beschränkt Exchange die maximale Anzahl von Elementen, die in einer einzigen Anforderung zurückgegeben werden können auf 1000.
    
- Wenn Sie die maximale Anzahl von Einträgen auf eine größere Zahl festlegen, müssen Sie weniger Anforderungen senden, um alle Elemente zu erhalten, Sie werden jedoch länger auf Antworten warten müssen.
    
- Wenn Sie die maximale Anzahl von Einträgen auf eine kleinere Zahl festlegen, wird die Antwortzeit beschleunigt, Sie werden mehrere Anforderungen senden müssen, um alle Elemente zu erhalten.
    
### <a name="handling-changes-to-the-result-set"></a>Behandeln von Änderungen zum Resultset

In dem bereits im Artikel erwähnten vereinfachten Beispiel war die Anzahl der Elemente im Posteingang des Benutzers konstant. In Wirklichkeit kann sich die Anzahl der Elemente in einem Posteingang jedoch häufig ändern. Nue Nachrichten können eintreffen und Elemente können jederzeit gelöscht und verschoben werden. Doch wie wirkt sich dies auf das Paging aus? Zur Veranschaulichung werden wir nun das frühere Beispielszenario ein wenig ändern.
  
Wir beginnen wieder mit den 15 Elementen im Posteingang des Benutzers und senden die selbe Anfangsanforderung. Wie bereits zuvor antwortet der Server mit den ersten 10 Nachrichten und gibt an, dass die Antwort das letzte Element nicht beinhaltet, dass insgesamt 15 Elemente vorhanden sind, und dass der nächste Offset 10 sein sollte, wie veranschaulicht auf der Abbildung 1.
  
Während Ihre Anwendung diese 10 Elemente verarbeitet, trifft einer neue Nachricht in Ihrem Posteingang ein und wird zum Resultset auf dem Server hinzugefügt. Ihre Anwendung sendet die gleiche Anforderung an den Server weiter (nur bei dem auf 10 eingestellten Offset). Diesmal bekommt der Server sechs Elemente zurück und gibt an, dass das Resultset insgesamt 16 Elemente enthält.
  
In diesem Moment fragen Sie sich vielleicht, ob dies überhaupt ein Problem darstellt. Schließlich haben sie 16 Elemente zu den zwei Antworten zurückbekommen. Warum dann die ganze Aufregung? Die Antwort darauf häng davon ab, wohin in der Liste das neue Element platziert wurde. Wenn die Liste so sortiert ist, dass die ältesten Elemente (nach Empfangsdatum/Zeit) erst stehen, haben Sie keinen Grund zur Beunruhigung. Das neue Element wird an das Ende der Liste gestellt und wird in die nächsten Antwort einbezogen.
  
**Abbildung 3. Anfordern von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wobei das 16. Element in der Liste neu ist**

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Ende der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
Falls die Liste so sortiert ist, dass die neuesten Elemente erst stehen, ist dies ein Problem. In diesem Fall wäre das erste Element in der zweiten Anforderung das letzte Element der vorherigen Anforderung plus die restlichen fünf Elemente aus der ursprünglichen 15. Um es an unserem magischen Fenster zu veranschaulichen, Sie haben Ihr Fenster um 10 verschoben, aber die Billboards selbst sind ebenfalls um 1 verschoben worden.
  
**Abbildung 4. Anfordern von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wobei das erste Element in der Liste neu ist**

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Anfang der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
Eine Möglichkeit, wie eine Änderung der Ergebnisse auf dem Server erkannt werden kann, ist das Verwenden des Konzeptes eines Ankerelements. Ein Ankerelement ist ein zusätzliches Element in Ihrer Antwort, dass nicht mit den anderen Ergebnisse mitverarbeitet wird, aber zum Vergleichen mit den nächsten Ergebnissen verwendet wird, um festzustellen, ob die Elemente selbst verschoben wurden. Um es wieder mittels unseres Beispiels zu veranschaulichen, wenn Ihre Anwendung eine „Fenster“-Größe von 10 verwendet, stellen Sie in Wirklichkeit die maximale Anzahl von Elementen, die zurückgesetzt werden, auf 11.  Ihre Anwendung verarbeitet die ersten 10 Elemente in der Antwort wie gewohnt. Für das letzte Element speichern Sie den Bezeichner des Elements als Anker und geben Sie die nächste Anforderung mit einem Offset von 10 ein. Wenn sich die Daten nicht geändert haben, sollte das erste Element in der zweiten Antwort einen Bezeichner haben, der mit dem Anker übereinstimmt. Wenn die Elementbezeichner nicht übereinstimmen, wissen Sie, dass die Daten in den Abschnitten der Liste, die Sie bereits „ausgelagert“ haben, entfernt oder eingefügt wurden.
  
Auch wenn Sie wissen, das sich die Daten geändert haben, müssen Sie sich immer noch entscheiden, wie reagiert werden soll. Auch auf diese Frage gibt es keine universale Antwort. Ihre Aktionen werden von der Art Ihrer Anwendung und davon, wie wichtig es ist, alle Elemente zu erfassen, abhängen. Sie könnten sie völlig ignorieren, den Vorgang neu starten, oder zurückverfolgen und versuchen, die Stelle der Änderung zu finden.
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a>Beispiel: Eine ausgelagerte Suche mittels verwalteten EWS-API durchführen
<a name="bk_PagedSearchEWSMA"> </a>

Das Paging wird von den folgenden verwalteten EWS-API-Methoden unterstützt:
  
- [ExchangeService.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
Wenn Sie die verwaltete EWS-API verwenden, konfiguriert Ihre Anwendung das Paging mit der [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) oder [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx)-Klasse und empfängt Informationen von dem Server bezüglich des Pagings von der [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) oder der [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx)-Klasse. 
  
Im folgenden Beispiel werden alle Elemente in einem Ordner mithilfe einer ausgelagerten Suche abgerufen, die fünf Elemente in jeder Antwort zurückgibt. Außerdem ruft es ein zusätzliches Element ab, das als Anker dient, um Änderungen an den Ergebnissen auf dem Server zu erkennen. 
  
In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde. 
  
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
            if (moreItems && anchorId != null)
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
            int displayCount = 0;
            if ((results.MoreAvailable == false && results.Items.Count > pageSize) || (results.Items.Count < pageSize))
            {
                displayCount = results.Items.Count;
            }
            else
            {
                displayCount = pageSize;
            }
            
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

## <a name="example-perform-a-paged-search-by-using-ews"></a>Beispiel: Eine ausgelagerte Suche mittels EWS durchführen
<a name="bk_PagedSearchEWS"> </a>

Das Paging wird von den folgenden EWS-Vorgängen unterstützt:
  
- [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
Wenn Sie EWS verwenden, konfiguriert ihre Anwendung das Paging mit den [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)-Element oder dem [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)-Element und empfängt Informationen vom Server hinsichtlich des Pagings aus dem [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx)-Element oder dem [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)-Element. 
  
In diesem Anforderungsbeispiel wird eine **FindItem**-Anforderung für maximal sechs Elemente gesendet, beginnend bei einem Offset von 0 vom Anfang der Liste der Elemente im Posteingang des Benutzers. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Der Servers gibt die folgende Antwort zurück, die sechs Elemente enthält. Die Antwort gibt außerdem an, dass in den Ergebnissen auf dem Server insgesamt acht Elemente vorhanden sind, und dass das letzte Element in der Ergebnisliste nicht in der Antwort enthalten ist.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

In diesem Beispiel wird die gleiche Anforderung gesendet, aber diesmal wird das **Offset**-Attribut in „fünf“ geändert, wodurch angegeben wird, dass der Server höchstens sechs Elemente zurückgeben sollte, beginnend mit dem Offset von fünf vom Anfang. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Der Servers sendet die folgende Antwort, die drei Elemente enthält. Die Antwort gibt außerdem an, dass in den Ergebnissen auf dem Server immer noch insgesamt acht Elemente vorhanden sind, und dass das letzte Element in der Ergebnisliste nicht in der Antwort einbezogen ist.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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
    
- [ExchangeService.FindFolders-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [FindFolder-Vorgang](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [EWS-Einschränkung in Exchange](ews-throttling-in-exchange.md)
    

