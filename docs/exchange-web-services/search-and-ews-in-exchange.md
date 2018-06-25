---
title: Suche und EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9fa5b836-857e-401d-9450-51e7dbc69104
description: Erfahren Sie, wie Sie Elemente im Exchange mithilfe der EWS Managed API oder EWS zu suchen.
ms.openlocfilehash: da24258ba94b842fa97fff92148620344c939f05
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757130"
---
# <a name="search-and-ews-in-exchange"></a>Suche und EWS in Exchange

Erfahren Sie, wie Sie Elemente im Exchange mithilfe der EWS Managed API oder EWS zu suchen.
  
Kommt diese bekannt? Starten Sie schließlich das Projekt, den, das Sie für Wochen haben, nicht jetzt noch, ein, und Sie benötigen Informationen über das Projekt, das Sie als Manager in Woche e-Mail gesendet. Posteingang weist Hunderte oder vielleicht Tausende von Nachrichten auf. Was machst du? Blättern Sie durch Ihre e-Mails Scannen jeder Betreff und der Absender, bis Sie ihn finden? Oder verwenden Sie die Suchfunktion in Ihrem bevorzugten e-Mail-Client schnell auf NULL auf, was Sie benötigen?
  
Suche ist wohl ein Feature muss für alle e-Mail-Clients. Aber Suche deutlich mehr als nur die Benutzer sich ihr Postfach Suchen verwendet werden kann. Muss Ihre app Termine verarbeitet, die in bestimmten Zeitfenster fallen verwendet? Möglicherweise müssen Sie alle Aufgabenelemente mit einem bestimmten Status melden, oder verschieben Sie alle Kontakte mit einem bestimmten Unternehmen Namen in einen anderen Ordner. Hilfe können mit all diesen Anforderungen.
  
## <a name="search-basics"></a>Grundlagen der Suche
<a name="bk_SearchBasics"> </a>

Die EWS Managed API und EWS bieten zwei grundlegende Methoden zur Angabe einer Suche. Sie können einen [Suchfilter](how-to-use-search-filters-with-ews-in-exchange.md) oder eine [Abfragezeichenfolge](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)verwenden. Die verwendete Methode hängt von der Absicht hinter der Suche.
  
**In Tabelle 1. Szenarien für die Suchfilter und Suchabfragen**

|**Aktion**|**Verwenden einer...**|**Anmerkungen**|
|:-----|:-----|:-----|
|Beschränken Sie die Suche auf eine bestimmte Eigenschaft oder eine Gruppe von Eigenschaften  <br/> |Suchfilter  <br/> |Suchfilter bieten die beste des Steuerelements über die Eigenschaften durchsucht werden. Obwohl Abfragezeichenfolgen eine begrenzte Auswahl von Eigenschaften mithilfe von (Erweiterte Query Syntax, AQS) ausgerichtet werden, können eine beliebige Eigenschaft Suchfilter Ziel ein.  <br/> |
|Suchvorgänge mit mehreren Kriterien erstellen  <br/> |Suchfilter  <br/> |Suchfilter können mehrere Suchkriterien zusammen mit logisches AND oder or gleichzeitig, für die Suche wie "Betreff enthält 'Besprechungsnotizen' und Absender"Sadie Daniels"gleich" zulassen verknüpft werden. Obwohl Abfragezeichenfolgen auch mehrere Suchkriterien beitreten können, sind sie auf die Gruppe von Eigenschaften von Abfragezeichenfolgen unterstützt beschränkt.  <br/> |
|Benutzerdefinierte Eigenschaften der Suche  <br/> |Suchfilter  <br/> |Suchfilter können benutzerdefinierte Eigenschaften adressieren. Benutzerdefinierte Eigenschaften suchen Abfragezeichenfolgen nicht.  <br/> |
|Führen Sie eine Suche Groß-/Kleinschreibung von Zeichenfolgeneigenschaften  <br/> |Suchfilter  <br/> |Abfrage Zeichenfolgensuchen sind nicht zwischen Groß-und Kleinschreibung.  <br/> |
|Steuern des Beschränkung Modus bei der Suche Zeichenfolgeneigenschaften  <br/> |Suchfilter  <br/> |Abfrage Zeichenfolgensuchen sind immer Suchvorgänge nach Teilzeichenfolgen dar. Wenn Sie müssen zum Suchen nach bestimmten Präfixen oder nach genauen Übereinstimmungen erfordern, ist ein Suchfilter die beste Wahl.  <br/> |
|Suchen nach Ordnern  <br/> |Suchfilter  <br/> |Suchen nach Ordnern mit einer Abfragezeichenfolge unterstützt EWS nicht.  <br/> |
|Erstellen eines Suchordners  <br/> |Suchfilter  <br/> |Erstellen von Suchordnern mit einer Abfragezeichenfolge unterstützt EWS nicht.  <br/> |
|Suchfunktion im Webstil für alle verwendete häufig Eigenschaften  <br/> |Abfragezeichenfolge  <br/> |Abfragezeichenfolgen, die nicht AQS enthalten werden über alle am häufigsten verwendeten Eigenschaften gesucht. Abfrage String-Wert "Mack Chaves" gibt beispielsweise alle Nachrichten von Mack Chaves als auch für alle Nachrichten mit "Mack Chaves" im Nachrichtentext oder der Betreff zurück.  <br/> |
|Erstellen Sie eine Suche basierend auf einfache Benutzereingabe  <br/> |Abfragezeichenfolge  <br/> |Eine Abfragezeichenfolge ist eine hervorragende Wahl für die Endbenutzer quick Suche durchgeführt werden soll, indem Sie in eine einfache Zeichenfolge eingeben. Da eine Abfrage Zeichenfolgensuche alle am häufigsten verwendete Eigenschaften enthält, werden die Ergebnisse Elemente enthalten, die der Benutzer die Suchbegriffe enthalten.  <br/> |
   
### <a name="using-a-search-filter"></a>Verwenden einen Filter für die Suche

Suchfilter können Sie eine Vielzahl von Suchoptionen und den höchsten Grad steuern, wie die Suche ausgeführt wird. Sie können zum Ausführen von grundlegenden Gleichheit und Vergleich sucht Suchfilter verwenden, aber Sie können auch den Inhalt der Zeichenfolgeneigenschaften suchen oder Bitmaske Vergleiche.
  
Beispielsweise können Sie den Inhalt des Betreffs von Elementen mithilfe der [SearchFilter.ContainsSubstring](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) -Klasse in die EWS Managed API suchen. In diesem Beispiel wird ein Suchfilter erstellt, um den Betreff für die Teilzeichenfolge "Besprechungsnotizen" wird zu suchen. 
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

Sie können auch mit benutzerdefinierten Eigenschaften suchen. In diesem Beispiel wird die benutzerdefinierte Eigenschaft **ItemIndex** für Werte, die größer als 3 durchsucht. 
  
```cs
Guid MyAppGuid = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
ExtendedPropertyDefinition customPropDefinition =
    new ExtendedPropertyDefinition(MyAppGuid, "ItemIndex", MapiPropertyType.Integer); 
SearchFilter.IsGreaterThan customPropFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
```

Sie können auch mehrere Suchfilter zum komplexere Suchvorgänge kombinieren. Beispielsweise können Sie die vorherigen beiden Filter mit ein logisches AND kombinieren, mithilfe der [SearchFilter.SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) -Klasse. 
  
```cs
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, customPropFilter);
```

### <a name="using-a-query-string"></a>Verwenden einer Abfragezeichenfolge

Abfragezeichenfolgen bieten einen anderen Ansatz zum Suchen. Sie haben weniger Kontrolle über die Felder, die durchsucht werden und wie die Suche ausgeführt wird, wenn Sie eine Abfrage Zeichenfolgensuche verwenden. Nicht ab, die eine schlechte Sache ist! In einigen Fällen möchten Sie möglicherweise ein breiter Netz, sodass Basisdaten umgewandelt.
  
Beispielsweise können Sie nach "Besprechungsnotizen" suchen, mit der [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/jj223808%28v=exchg.80%29.aspx) EWS Managed API-Methode. 
  
```cs
FindItemsResults<Item> results = service.FindItems(folder, "meeting notes", view);
```

Wenn Sie die Ergebnisse dieser Suche an die Ergebnisse zuvor im **SearchFilter.ContainsSubstring** Search Beispiel vergleichen, wird diese Suche weitere Ergebnisse enthalten. Die Filter-Suche gibt nur Elemente zurück, die "Besprechungsnotizen" in der Betreffzeile haben, während diese Suche Elemente zurückgibt, die "Besprechungsnotizen" in den Betreff, Textkörper und andere Felder aufweisen. 
  
Sehen wir uns an, wie Sie die Abfragezeichenfolge näher auf die Ergebnisse abgerufen, die Sie aus dem Suchfilter finden Sie unter optimieren können. AQS verwenden, können Sie die Suche auf den Betreff beschränken.
  
```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:meeting notes", view);
```

Hierbei handelt es sich um näher, aber die Ergebnisse sind noch nicht ganz identisch. Wenn Sie eine Abfragezeichenfolge mit mehreren Wörtern verwenden, erhalten Sie Übereinstimmungen, selbst wenn die Wörter nicht in der Reihenfolge sind die von die Ihnen angegebenen oder selbst wenn sie nicht nebeneinander sind. Mit der Abfragezeichenfolge "Betreff: Besprechungsnotizen" werden Sie Übereinstimmungen für "Besprechungsnotizen", "Notizen aus der Besprechung" erhalten möchten, und so weiter. Zum verfeinern, können Sie die Suchbegriffe in doppelte Anführungszeichen, um anzugeben, dass Sie diesen Ausdruck nur möchten umbrechen.
  
```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:\"meeting notes\"", view);
```

## <a name="requesting-specific-properties-in-search-results"></a>Anfordern von bestimmten Eigenschaften in Suchergebnissen
<a name="bk_RequestSpecific"> </a>

Standardmäßig werden Suchergebnisse alle Eigenschaften für die Elemente enthalten, die den Suchkriterien entsprechen. In einigen Fällen möglicherweise verfügbare, aber in den meisten Fällen die Anwendung erfordert nur einen einzelnen Satz von Eigenschaften. In diesem Fall sollten Sie begrenzen, die Gruppe von Eigenschaften, die auf die Eigenschaften die Anwendung zurückgegeben werden muss. Im folgenden Beispiel wird die [aufrufenArtikel aufrufen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) -Klasse verwendet, um begrenzen die zurückgegebenen Eigenschaften auf den Betreff Datum/Uhrzeit empfangen und die ID der Elemente. 
  
```cs
ItemView view = new ItemView(10);
// Creating a new PropertySet with this constructor includes 
// ItemSchema.Id.
view.PropertySet = new PropertySet(ItemSchema.Subject, ItemSchema.DateTimeReceived);
```

## <a name="controlling-search-depth"></a>Steuern des Search-Tiefe
<a name="bk_SearchDepth"> </a>

Festlegen der Durchlauf für die Ansicht steuert die projekttiefe und den Umfang der Suche. 
  
**In Tabelle 2. Durchqueren Suchwerten**

|**Traversal Wert**|**Betrifft**|**Beschreibung**|
|:-----|:-----|:-----|
|Flach  <br/> |Elemente und Ordner  <br/> |Flache Suchvorgänge können nur direkte untergeordnete Elemente des Ordners, der durchsucht wird.  <br/> |
|Tief  <br/> |Elemente (nur bei Suchordnern) und Ordner  <br/> |Tiefe Suchvorgänge rekursiv Suchen der durchsuchte Ordner und Unterordner.  <br/> |
|Verknüpft ist  <br/> |Items  <br/> |Zugehörige suchen umfassen nur zugeordnete Elemente aus dem Ordner, der durchsucht wird. Zugeordnete Elemente sind ausgeblendete Elemente im Ordner.  <br/> |
|SoftDeleted  <br/> |Elemente und Ordner  <br/> |Dieses Typs durchqueren ist veraltet. SoftDeleted suchen umfassen nur Elemente in der muss. Die Dumpster wurde durch den [Ordner "wiederherstellbare Elemente"](http://technet.microsoft.com/en-us/library/ee364755%28v=exchg.150%29.aspx(Office.15).aspx) in Exchange Online, Exchange Online als Teil von Office 365 und Exchange beginnend mit Exchange 2010-Versionen ersetzt.  <br/> |
   
## <a name="managing-search-results"></a>Verwalten von Suchergebnissen
<a name="bk_ManageSearchResults"> </a>

Die EWS Managed API und EWS können Sie auch ändern, wie die Suchergebnisse zurückgegeben werden. Sie können mithilfe von Ansichten können Sie angeben, welche Eigenschaften in den Ergebnissen enthalten sind, Ergebnisse sortieren und page Ihre Ergebnisse, um ähnliche nur eine festgelegte Anzahl von Ergebnissen pro Antwort erhalten. Sie können auch Ergebnisse nach bestimmten Feldwerte und Steuerelement die Tiefe der Suche durch Angabe eines bestimmten durchqueren gruppieren. Suchordner können Sie schließlich permanente Suchläufe erstellen, die dynamisch Eintreffen neuer Elemente aktualisiert werden.
  
### <a name="sorting"></a>Sortieren

Sie können den Server um sortierte Ergebnisse zurückzugeben, die angezeigt werden soll oder Verarbeiten von Elementen in der Reihenfolge erleichtern abrufen. In diesem Beispiel werden die Ergebnisse nach Datum/Uhrzeit-erhalten haben, mit den neuesten Elemente der ersten sortiert werden.
  
```cs
view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
```

### <a name="paging"></a>Paging

Wenn Sie eine Suchanfrage mithilfe des EWS Managed API oder EWS senden, geben Sie eine Ansichtsgröße, die steuert die maximale Anzahl der zurückgegebenen Elemente an. Die Anzahl der Elemente auf dem Server, die den Suchkriterien entsprechen größer als die Ansichtsgröße möglicherweise. In diesem Fall gibt den Server an, dass weitere Artikel zur Verfügung stehen. Sie können [verwenden, um die Suche wiederholen die Paging](how-to-perform-paged-searches-by-using-ews-in-exchange.md) und Abrufen der nächsten Gruppe von Ergebnissen. 
  
Beispielsweise können Sie eine Suchanfrage mit einer Ansichtsgröße von 10 senden. Es könnten 15 Elemente auf dem Server, die den Suchkriterien entsprechen, aber Sie erhalten nur dann wieder die ersten 10, Indikator (die [FindItemsResults\<TItem\>. MoreAvailable](http://msdn.microsoft.com/en-us/library/dd635477%28v=exchg.80%29.aspx) Eigenschaft, wenn Sie die EWS Managed API verwenden), dass weitere Ergebnisse auf dem Server vorhanden sind. Sie können dann senden die gleiche Suche mit einem Offset von 10 Fragen für die nächsten 10 Elemente, die den Suchkriterien entsprechen. Der Server gibt die verbleibenden fünf Elemente zurück. 
  
**Abbildung 1. Ausgelagerte Suche-Beispiel**

![Eine Abbildung einer Seitensuche. Es wird eine erste Anforderung für 10 Elemente gesendet. Eine zweite Anforderung wird für die nächsten 10 Elemente gesendet.](media/Ex15_Search_PagedSearch.png)
  
### <a name="grouping"></a>Gruppieren

 Exchange können Sie zur Gruppe der Suchergebnisse nach einem bestimmten Feld. Damit können Sie die Suchergebnisse in leichter Gruppen unterteilen. Beispielsweise können Sie "Besprechungsnotizen" gesucht und die Ergebnisse nach Absender gruppiert. Wie in der folgenden Abbildung gezeigt, werden der zurückgegebenen Elemente in Gruppen, die mit allen aufgeteilt werden die Elemente, die den Suchkriterien vom selben Absender in einer Gruppe: alle übereinstimmenden Elemente aus einer anderen Absender in einer anderen Gruppe usw.. 
  
**Abbildung 2. Die Suchergebnisse nach Absender gruppiert**

![Eine Abbildung, in der Suchergebnisse nach Absender gruppiert sind](media/Ex15_Search_GroupedResults.png)
  
## <a name="search-folders"></a>Suchordner
<a name="bk_SearchFolders"> </a>

Mit einem regulären-Suche für die Suche wird ausgeführt, die Ergebnisse werden an die Anwendung zur Verarbeitung zurückgegeben und für die Suche nicht mehr vorhanden. Suchordner bieten eine Möglichkeit, eine Suche dauerhaft zu machen. Dies ist eine hervorragende Option für Suchvorgänge, die Sie wissen, dass mehrmals ausgeführt werden soll. Statt die gleiche Suche wiederholt ausführen, macht und den Server für die Suche von Grund auf jedes Mal bewerten ein Suchordner eine Suche immer auf, so dass der Server aktualisieren das vorhandene Ergebnis festzulegen, wie Elemente hinzugefügt werden oder aus den Suchbereich entfernt. Ordner Act wie normale Ordner zu suchen, dass sie als Ordner angezeigt werden, die Elemente enthalten. Der Unterschied besteht darin, dass nur Elemente im Ordner enthalten sind, die den Suchkriterien entsprechen, die mit dem Ordner verknüpft sind. Nach dem Erstellen eines Suchordners kann Ihre Anwendung auf dem neuesten Stand Ergebnisse der Suche nur Mobilgeräts auf den Inhalt des Ordners abrufen.
  
Erstellen eines Suchordners ist einfacher, wenn Sie erstellen Suchfilter beherrschen. Im folgenden Beispiel wird ein Suchordner erstellt, um alle e-Mail-Nachrichten mit dem Betreff anzuzeigen, die "Besprechungsnotizen" enthält.
  
```cs
static void CreateSearchFolder(ExchangeService service)
{
    SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
        "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
    SearchFolder searchFolder = new SearchFolder(service);
    searchFolder.DisplayName = "Meeting Notes";
    searchFolder.SearchParameters.RootFolderIds.Add(WellKnownFolderName.Inbox);
    searchFolder.SearchParameters.Traversal = SearchFolderTraversal.Deep;
    searchFolder.SearchParameters.SearchFilter = subjectFilter;
    searchFolder.Save(WellKnownFolderName.SearchFolders);
}
```

## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_InThisSection"> </a>

- [Verwenden Sie Suchfilter mit EWS in Exchange](how-to-use-search-filters-with-ews-in-exchange.md)
    
- [Führen Sie eine AQS-Suche mithilfe der EWS in Exchange](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)
    
- [Führen Sie seitenweise durch Verwenden von EWS in Exchange](how-to-perform-paged-searches-by-using-ews-in-exchange.md)
    
- [Führen Sie gruppierte Suchvorgänge in Exchange mithilfe der Exchange-Webdienste aus](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)
    
- [Arbeiten Sie mit Suchordner in Exchange mithilfe der Exchange-Webdienste](how-to-work-with-search-folders-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Ordner "wiederherstellbare Elemente"](http://technet.microsoft.com/en-us/library/ee364755%28v=exchg.150%29.aspx(Office.15).aspx)
    
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Drosselung Richtlinienparameter, die Einfluss auf EWS-Suchvorgänge](ews-throttling-in-exchange.md#bk_ThrottlingSearch)
    

