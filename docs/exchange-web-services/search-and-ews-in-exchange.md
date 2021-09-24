---
title: Suche und EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9fa5b836-857e-401d-9450-51e7dbc69104
description: Erfahren Sie, wie Sie mithilfe der verwalteten EWS-API oder EWS nach Elementen in Exchange suchen.
ms.openlocfilehash: f78f4625880480e4f0d1ebb683c6e7c2c7fa83e0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524434"
---
# <a name="search-and-ews-in-exchange"></a>Suche und EWS in Exchange

Erfahren Sie, wie Sie mithilfe der verwalteten EWS-API oder EWS nach Elementen in Exchange suchen.

Kommt diese bekannt? Sie beginnen schließlich mit dem Projekt, das Sie wochenlang verschoben haben, und Sie benötigen Informationen über das Projekt, das Ihr Vorgesetzter Ihnen vor Wochen per E-Mail gesendet hat. Ihr Posteingang enthält Hunderte oder vielleicht Tausende von Nachrichten. Was machst du? Führen Sie einen Bildlauf durch Ihre E-Mail-Überprüfung der einzelnen Betreff- und Absenderdaten durch, bis Sie sie finden? Oder verwenden Sie das Suchfeature in Ihrem bevorzugten E-Mail-Client, um schnell auf das zu reagieren, was Sie benötigen?

Die Suche ist wahrscheinlich ein Muss für jeden E-Mail-Client. Die Suche kann jedoch für viel mehr verwendet werden, als nur benutzern das Durchsuchen ihres Postfachs zu ermöglichen. Muss Ihre App Termine verarbeiten, die in bestimmte Zeitfenster fallen? Vielleicht müssen Sie über alle Aufgabenelemente mit einem bestimmten Status berichten oder alle Kontakte mit einem bestimmten Firmennamen in einen anderen Ordner verschieben. Die Suche kann bei all diesen Anforderungen hilfreich sein.

## <a name="search-basics"></a>Grundlagen der Suche
<a name="bk_SearchBasics"> </a>

Die verwaltete EWS-API und EWS bieten zwei grundlegende Methoden zum Angeben einer Suche. Sie können einen [Suchfilter](how-to-use-search-filters-with-ews-in-exchange.md) oder eine [Abfragezeichenfolge](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)verwenden. Welche Methode Sie verwenden, hängt von der Absicht ihrer Suche ab.

**Tabelle 1. Szenarien für Suchfilter und Suchabfragen**

|**Aktion**|**Verwenden Sie a...**|**Hinweise**|
|:-----|:-----|:-----|
|Beschränken Der Suche auf eine bestimmte Eigenschaft oder einen bestimmten Eigenschaftensatz  <br/> |Suchfilter  <br/> |Suchfilter bieten die beste Kontrolle darüber, welche Eigenschaften durchsucht werden. Obwohl Abfragezeichenfolgen mithilfe der erweiterten Abfragesyntax (Advanced Query Syntax, AQS) auf einen begrenzten Satz von Eigenschaften abzielen können, können Suchfilter auf jede Eigenschaft abzielen.  <br/> |
|Erstellen von Suchvorgängen mit mehreren Kriterien  <br/> |Suchfilter  <br/> |Mit Suchfiltern können mehrere Suchkriterien mit logischen ANDs oder ORs verknüpft werden, sodass Suchvorgänge wie "Betreff enthält 'Besprechungsnotizen' UND Absender gleich 'Sadie Daniels'" möglich sind. Obwohl Abfragezeichenfolgen auch mehrere Suchkriterien verknüpfen können, sind sie auf den Satz von Eigenschaften beschränkt, der von Abfragezeichenfolgen unterstützt wird.  <br/> |
|Benutzerdefinierte Eigenschaften durchsuchen  <br/> |Suchfilter  <br/> |Suchfilter können auf benutzerdefinierte Eigenschaften abzielen. Abfragezeichenfolgen durchsuchen keine benutzerdefinierten Eigenschaften.  <br/> |
|Durchführen einer Suche nach Zeichenfolgeneigenschaften unter Beachtung der Groß-/Kleinschreibung  <br/> |Suchfilter  <br/> |Bei Suchvorgängen in Abfragezeichenfolgen wird die Groß-/Kleinschreibung nicht beachtet.  <br/> |
|Steuern des Aufnahmemodus beim Durchsuchen von Zeichenfolgeneigenschaften  <br/> |Suchfilter  <br/> |Abfragezeichenfolgensuchen sind immer Teilzeichenfolgensuchen. Wenn Sie nach bestimmten Präfixen suchen oder genaue Übereinstimmungen benötigen, ist ein Suchfilter die beste Wahl.  <br/> |
|Suchen nach Ordnern  <br/> |Suchfilter  <br/> |Die Suche nach Ordnern mit einer Abfragezeichenfolge wird von EWS nicht unterstützt.  <br/> |
|Erstellen eines Suchordners  <br/> |Suchfilter  <br/> |Das Erstellen von Suchordnern mit einer Abfragezeichenfolge wird von EWS nicht unterstützt.  <br/> |
|Durchsuchen aller häufig verwendeten Eigenschaften  <br/> |Abfragezeichenfolge  <br/> |Abfragezeichenfolgen, die keine AQS enthalten, durchsuchen alle häufig verwendeten Eigenschaften. Beispielsweise gibt ein Abfragezeichenfolgenwert von "Chaves" alle Nachrichten zurück, die von "Chaves" gesendet wurden, sowie alle Nachrichten, deren Textkörper oder Betreff "Chaves" enthält.  <br/> |
|Erstellen einer Suche basierend auf einfachen Benutzereingaben  <br/> |Abfragezeichenfolge  <br/> |Eine Abfragezeichenfolge ist eine gute Wahl, um endbenutzern die Schnelleuchfunktion durch Eingabe einer einfachen Zeichenfolge zu ermöglichen. Da eine Abfragezeichenfolgensuche alle häufig verwendeten Eigenschaften enthält, enthalten die Ergebnisse alle Elemente, die die Suchbegriffe des Benutzers enthalten.  <br/> |

### <a name="using-a-search-filter"></a>Verwenden eines Suchfilters

Mit Suchfiltern erhalten Sie eine Vielzahl von Suchoptionen und die größtmögliche Kontrolle über die Art und Weise, wie die Suche ausgeführt wird. Sie können Suchfilter verwenden, um grundlegende Gleichheits- und Vergleichssuchen durchzuführen, aber Sie können auch innerhalb des Inhalts von Zeichenfolgeneigenschaften suchen oder Bitmaskenvergleiche durchführen.

Sie können z. B. den Inhalt des Betreffs von Elementen mithilfe der [SearchFilter.ContainsSubstring-Klasse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) in der verwalteten EWS-API durchsuchen. In diesem Beispiel wird ein Suchfilter erstellt, um den Betreff nach der Teilzeichenfolge "Besprechungsnotizen" zu durchsuchen, wobei groß- und kleinschreibung ignoriert wird.

```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

Sie können auch nach benutzerdefinierten Eigenschaften suchen. In diesem Beispiel wird die benutzerdefinierte Eigenschaft **ItemIndex** nach Werten gesucht, die größer als 3 sind.

```cs
Guid MyAppGuid = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
ExtendedPropertyDefinition customPropDefinition =
    new ExtendedPropertyDefinition(MyAppGuid, "ItemIndex", MapiPropertyType.Integer);
SearchFilter.IsGreaterThan customPropFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
```

Sie können auch mehrere Suchfilter kombinieren, um komplexere Suchvorgänge zu erstellen. Beispielsweise können Sie die beiden vorherigen Filter mit einer logischen AND kombinieren, indem Sie die [SearchFilter.SearchFilterCollection-Klasse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) verwenden.

```cs
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, customPropFilter);
```

### <a name="using-a-query-string"></a>Verwenden einer Abfragezeichenfolge

Abfragezeichenfolgen bieten einen anderen Suchansatz. Sie haben weniger Kontrolle über die durchsuchten Felder und die Art und Weise, wie die Suche ausgeführt wird, wenn Sie eine Abfragezeichenfolgensuche verwenden. Das ist nicht schlecht! In einigen Fällen möchten Sie vielleicht sozusagen ein breiteres Netz umwandeln.

Sie können z. B. mithilfe der verwalteten EWS-API-Methode von [ExchangeService.FindItems](https://msdn.microsoft.com/library/jj223808%28v=exchg.80%29.aspx) nach "Besprechungsnotizen" suchen.

```cs
FindItemsResults<Item> results = service.FindItems(folder, "meeting notes", view);
```

Wenn Sie die Ergebnisse dieser Suche mit den Ergebnissen des **Suchbeispiels "SearchFilter.ContainsSubstring"** vergleichen, enthält diese Suche weitere Ergebnisse. Die Suchfiltersuche gibt nur Elemente mit "Besprechungsnotizen" im Betreff zurück, während diese Suche Elemente zurückgibt, die "Besprechungsnotizen" im Betreff, Textkörper und anderen Feldern enthalten.

Sehen wir uns an, wie Sie die Abfragezeichenfolge verfeinern können, um näher an die Ergebnisse des Suchfilters zu gelangen. Mithilfe von AQS können Sie Ihre Suche auf den Betreff beschränken.

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:meeting notes", view);
```

Dies ist näher, aber die Ergebnisse sind immer noch nicht ganz identisch. Wenn Sie eine Abfragezeichenfolge mit mehreren Wörtern verwenden, erhalten Sie Übereinstimmungen, auch wenn sich die Wörter nicht in der angegebenen Reihenfolge befinden oder wenn sie nicht nebeneinander liegen. Mit der Abfragezeichenfolge "Betreff:Besprechungsnotizen" erhalten Sie Übereinstimmungen für "Besprechungsnotizen", "Notizen aus der Besprechung" usw. Zur weiteren Verfeinerung können Sie die Suchbegriffe in doppelte Anführungszeichen umschließen, um anzugeben, dass Sie nur diesen Ausdruck verwenden möchten.

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:\"meeting notes\"", view);
```

## <a name="requesting-specific-properties-in-search-results"></a>Anfordern bestimmter Eigenschaften in Suchergebnissen
<a name="bk_RequestSpecific"> </a>

Standardmäßig enthalten die Suchergebnisse alle Eigenschaften der Elemente, die der Suche entsprechen. In einigen Fällen ist dies möglicherweise das Gewünschte, aber in den meisten Fällen erfordert Ihre Anwendung nur einen separaten Satz von Eigenschaften. In diesem Fall sollten Sie den Satz von Eigenschaften, die zurückgegeben werden, auf die Eigenschaften beschränken, die Ihre Anwendung benötigt. Im folgenden Beispiel wird die [ItemView-Klasse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) verwendet, um die zurückgegebenen Eigenschaften auf den Betreff, das Datum/die Uhrzeit des Empfangs und die ID der Elemente zu beschränken.

```cs
ItemView view = new ItemView(10);
// Creating a new PropertySet with this constructor includes
// ItemSchema.Id.
view.PropertySet = new PropertySet(ItemSchema.Subject, ItemSchema.DateTimeReceived);
```

## <a name="controlling-search-depth"></a>Steuern der Suchtiefe
<a name="bk_SearchDepth"> </a>

Durch Festlegen des Traversals in der Ansicht werden die Tiefe und der Umfang der Suche gesteuert.

**Tabelle 2. Durchsuchen von Traversalwerten**

|**Traversalwert**|**Gilt für**|**Beschreibung**|
|:-----|:-----|:-----|
|Flachen  <br/> |Elemente und Ordner  <br/> |Flache Suchvorgänge sind auf direkte untergeordnete Elemente des zu durchsuchenden Ordners beschränkt.  <br/> |
|Tief  <br/> |Elemente (nur mit Suchordnern) und Ordner  <br/> |Bei tiefen Suchvorgängen wird rekursiv nach dem durchsuchten Ordner und den Unterordnern gesucht.  <br/> |
|Zugeordneten  <br/> |Elemente  <br/> |Zugeordnete Suchvorgänge umfassen nur zugeordnete Elemente aus dem zu durchsuchenden Ordner. Zugeordnete Elemente sind ausgeblendete Elemente innerhalb des Ordners.  <br/> |
|Vorläufig gelöscht  <br/> |Elemente und Ordner  <br/> |Dieser Traversaltyp ist veraltet. SoftDeleted-Suchvorgänge umfassen nur Elemente, die sich im Dumpster befinden. Der Dumpster wurde durch den [Ordner "Wiederherstellbare Elemente"](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder) in Exchange Online ersetzt, Exchange Online als Teil von Office 365 und Versionen von Exchange ab Exchange 2010.  <br/> |

## <a name="managing-search-results"></a>Verwalten von Suchergebnissen
<a name="bk_ManageSearchResults"> </a>

Mit der verwalteten EWS-API und EWS können Sie auch ändern, wie Ihre Suchergebnisse zurückgegeben werden. Mithilfe von Ansichten können Sie angeben, welche Eigenschaften in den Ergebnissen enthalten sind, Ergebnisse sortieren und Ihre Ergebnisse auf der Seite anzeigen, um nur eine festgelegte Anzahl von Ergebnissen pro Antwort abzurufen. Sie können Ergebnisse auch nach bestimmten Feldwerten gruppieren und die Tiefe einer Suche steuern, indem Sie einen Traversierungstyp angeben. Schließlich können Sie Suchordner verwenden, um dauerhafte Suchvorgänge zu erstellen, die dynamisch aktualisiert werden, sobald neue Elemente eintreffen.

### <a name="sorting"></a>Die Sortierung

Sie können den Server abrufen, um sortierte Ergebnisse zurückzugeben, wodurch die Anzeige oder Verarbeitung von Elementen in der angegebenen Reihenfolge vereinfacht wird. In diesem Beispiel werden die Ergebnisse nach dem Empfangen von Datum/Uhrzeit sortiert, wobei die neuesten Elemente an erster Stelle stehen.

```cs
view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
```

### <a name="paging"></a>Paging

Wenn Sie eine Suchanforderung mithilfe der verwalteten EWS-API oder EWS senden, geben Sie eine Ansichtsgröße an, die die maximale Anzahl zurückgegebener Elemente steuert. Die Anzahl der Elemente auf dem Server, die Ihrer Suche entsprechen, kann jedoch größer als die Ansichtsgröße sein. In diesem Fall gibt der Server an, dass weitere Elemente verfügbar sind. Sie können [paging verwenden, um Ihre Suche zu wiederholen](how-to-perform-paged-searches-by-using-ews-in-exchange.md) und den nächsten Satz von Ergebnissen abzurufen.

Sie können z. B. eine Suchanfrage mit einer Ansichtsgröße von 10 senden. Möglicherweise befinden sich 15 Elemente auf dem Server, die ihrer Suche entsprechen, aber Sie erhalten nur die ersten 10 zusammen mit einem Indikator [(findItemsResults \<TItem\> . MoreAvailable-Eigenschaft,](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) wenn Sie die verwaltete EWS-API verwenden), dass mehr Ergebnisse auf dem Server vorhanden sind. Sie können dann dieselbe Suche mit einem Offset von 10 senden, um nach den nächsten 10 Elementen zu fragen, die Ihrer Suche entsprechen. Der Server gibt die verbleibenden fünf Elemente zurück.

**Abbildung 1. Beispiel für eine seitenseitige Suche**

![Eine Abbildung einer Seitensuche. Es wird eine erste Anforderung für 10 Elemente gesendet. Eine zweite Anforderung wird für die nächsten 10 Elemente gesendet.](media/Ex15_Search_PagedSearch.png)

### <a name="grouping"></a>Gruppieren

 mit Exchange können Sie Suchergebnisse nach einem bestimmten Feld gruppieren. Dies kann dazu beitragen, Suchergebnisse in besser verwaltbare Sätze aufzubrechen. Sie können z. B. nach "Besprechungsnotizen" suchen und die Ergebnisse nach Absender gruppieren. Wie in der folgenden Abbildung dargestellt, werden die zurückgegebenen Elemente in Gruppen unterteilt, wobei alle Elemente, die den Kriterien desselben Absenders in einer Gruppe entsprechen, alle übereinstimmenden Elemente eines anderen Absenders in einer anderen Gruppe usw.

**Abbildung 2. Suchergebnisse nach Absender gruppiert**

![Eine Abbildung, in der Suchergebnisse nach Absender gruppiert sind](media/Ex15_Search_GroupedResults.png)

## <a name="search-folders"></a>Suchordner
<a name="bk_SearchFolders"> </a>

Bei einer regulären Suche wird die Suche ausgeführt, die Ergebnisse werden zur Verarbeitung an Ihre Anwendung zurückgegeben, und die Suche ist nicht mehr vorhanden. Suchordner bieten eine Möglichkeit, eine Suche dauerhaft zu machen. Dies ist eine hervorragende Option für Suchvorgänge, von denen Sie wissen, dass Sie mehrmals ausgeführt werden sollen. Anstatt die gleiche Suche wiederholt auszuführen, wodurch der Server die Suche jedes Mal von Grund auf neu auswertet, führt ein Suchordner eine Suche immer ein, sodass der Server das vorhandene Resultset aktualisieren kann, wenn Elemente dem Suchbereich hinzugefügt oder daraus entfernt werden. Suchordner verhalten sich wie reguläre Ordner, da sie als Ordner mit Elementen angezeigt werden. Der Unterschied besteht darin, dass im Ordner nur die Elemente enthalten sind, die den Suchkriterien entsprechen, die dem Ordner zugeordnet sind. Nachdem ein Suchordner erstellt wurde, kann Ihre Anwendung aktuelle Ergebnisse der Suche abrufen, indem nur der Inhalt des Ordners überprüft wird.

Das Erstellen eines Suchordners ist einfach, wenn Sie das Erstellen von Suchfiltern gemastert haben. Im folgenden Beispiel wird ein Suchordner erstellt, um alle E-Mails mit einem Betreff anzuzeigen, der "Besprechungsnotizen" enthält.

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

- [Verwenden von Suchfiltern mit EWS in Exchange](how-to-use-search-filters-with-ews-in-exchange.md)

- [Durchführen einer AQS-Suche mithilfe von EWS in Exchange](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)

- [Durchführen seitenweiter Suchen mithilfe von EWS in Exchange](how-to-perform-paged-searches-by-using-ews-in-exchange.md)

- [Durchführen gruppierter Suchen mithilfe von EWS in Exchange](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)

- [Arbeiten mit Suchordnern mithilfe von EWS in Exchange](how-to-work-with-search-folders-by-using-ews-in-exchange.md)

## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)

- [Ordner „Wiederherstellbare Elemente"](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder)

- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)

- [Einschränkungsrichtlinienparameter, die sich auf EWS-Suchvorgänge auswirken](ews-throttling-in-exchange.md#throttling-policy-parameters-that-affect-ews-search-operations)
