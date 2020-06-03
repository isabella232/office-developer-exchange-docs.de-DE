---
title: Suche und EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9fa5b836-857e-401d-9450-51e7dbc69104
description: Erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS nach Elementen in Exchange suchen.
ms.openlocfilehash: d35cc74ab2fa79530ac09256e315a780023d833b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463837"
---
# <a name="search-and-ews-in-exchange"></a>Suche und EWS in Exchange

Erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS nach Elementen in Exchange suchen.

Kommt diese bekannt? Sie beginnen endlich mit dem Projekt, das Sie Wochen lang abgesetzt haben, und Sie benötigen Informationen zu dem Projekt, das Ihr Vorgesetzter Ihnen in e-Mail-Wochen zurückgeschickt hat. In Ihrem Posteingang befinden sich Hunderte oder vielleicht Tausende von Nachrichten darin. Was machst du? Scrollen Sie durch Ihre e-Mail-Überprüfung für jeden Betreff und Absender, bis Sie ihn finden? Oder verwenden Sie die Suchfunktion in Ihrem bevorzugten e-Mail-Client, um schnell, was Sie benötigen, zu Nullen?

Die Suche ist wohl ein must-have-Feature für jeden e-Mail-Client. Die Suche kann jedoch für vieles mehr verwendet werden, als nur Benutzern das Durchsuchen Ihres Postfachs zu ermöglichen. Muss Ihre APP Termine verarbeiten, die in bestimmte Zeitfenster fallen? Möglicherweise müssen Sie über alle Aufgabenelemente mit einem bestimmten Statusberichten oder alle Kontakte mit einem bestimmten Firmennamen in einen anderen Ordner verlagern. Die Suche kann bei all diesen Anforderungen helfen.

## <a name="search-basics"></a>Grundlagen der Suche
<a name="bk_SearchBasics"> </a>

Die verwaltete EWS-API und EWS bieten zwei grundlegende Methoden zum Angeben einer Suche. Sie können einen [Suchfilter](how-to-use-search-filters-with-ews-in-exchange.md) oder eine [Abfragezeichenfolge](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)verwenden. Die Methode, die Sie verwenden, hängt von der Absicht hinter Ihrer Suche ab.

**Tabelle 1. Szenarien für Suchfilter und Suchabfragen**

|**Aktion**|**Verwenden Sie eine...**|**Hinweise**|
|:-----|:-----|:-----|
|Einschränken der Suche auf eine bestimmte Eigenschaft oder eine bestimmte Gruppe von Eigenschaften  <br/> |Suchfilter  <br/> |Suchfilter bieten das beste Maß an Kontrolle darüber, welche Eigenschaften durchsucht werden. Obwohl Abfragezeichenfolgen mithilfe der erweiterten Abfrage Syntax (AQS) auf eine beschränkte Menge von Eigenschaften Zielen können, können Suchfilter auf jede Eigenschaft abzielen.  <br/> |
|Erstellen von Suchvorgängen mit mehreren Kriterien  <br/> |Suchfilter  <br/> |Mit Suchfiltern können mehrere Suchkriterien mit logischem oder ORS verbunden werden, sodass Suchvorgänge wie "Betreff enthält" Besprechungsnotizen und Absender gleich "Sadie Daniels" sind. Obwohl Abfragezeichenfolgen auch mehreren Suchkriterien beitreten können, sind Sie auf die von Abfragezeichenfolgen unterstützte Gruppe von Eigenschaften limitiert.  <br/> |
|Benutzerdefinierte Sucheigenschaften  <br/> |Suchfilter  <br/> |Suchfilter können auf benutzerdefinierte Eigenschaften abzielen. Abfragezeichenfolgen suchen keine benutzerdefinierten Eigenschaften.  <br/> |
|Durchführen einer Groß-/Kleinschreibung Suche nach Zeichenfolgeneigenschaften  <br/> |Suchfilter  <br/> |Bei Abfragezeichen folgen suchen wird die Groß-/Kleinschreibung nicht beachtet.  <br/> |
|Steuern des Kapselungs Modus beim Durchsuchen von Zeichenfolgeneigenschaften  <br/> |Suchfilter  <br/> |Abfragezeichen folgen suchen sind immer Teil Zeichenfolgensuchen. Wenn Sie nach bestimmten Präfixen suchen oder exakte Übereinstimmungen benötigen, ist ein Suchfilter die beste Wahl.  <br/> |
|Suchen nach Ordnern  <br/> |Suchfilter  <br/> |Die Suche nach Ordnern mit einer Abfragezeichenfolge wird von EWS nicht unterstützt.  <br/> |
|Erstellen eines Suchordners  <br/> |Suchfilter  <br/> |Das Erstellen von Suchordnern mit einer Abfragezeichenfolge wird von EWS nicht unterstützt.  <br/> |
|Durchsuchen aller häufig verwendeten Eigenschaften  <br/> |Abfragezeichenfolge  <br/> |Abfragezeichenfolgen, die keine AQS enthalten, werden in allen häufig verwendeten Eigenschaften durchsucht. Beispielsweise gibt der Wert der Abfragezeichenfolge "Mack chavs" alle von Mack Chaves gesendeten Nachrichten sowie alle Nachrichten zurück, die im Text oder Betreff "Mack Chaves" enthalten.  <br/> |
|Erstellen einer Suche basierend auf einer einfachen Benutzereingabe  <br/> |Abfragezeichenfolge  <br/> |Eine Abfragezeichenfolge eignet sich hervorragend, um einem Endbenutzer die Möglichkeit zu geben, eine Schnellsuche durch Eingabe in eine einfache Zeichenfolge durchführen zu können. Da eine Abfragezeichen folgen Suche alle häufig verwendeten Eigenschaften enthält, enthalten die Ergebnisse alle Elemente, die die Suchbegriffe des Benutzers enthalten.  <br/> |

### <a name="using-a-search-filter"></a>Verwenden eines Suchfilters

Suchfilter bieten eine breite Palette von Suchoptionen und das größte Maß an Kontrolle darüber, wie die Suche durchgeführt wird. Sie können Suchfilter verwenden, um grundlegende Gleichheits-und Vergleichs Suchen durchzuführen, Sie können aber auch innerhalb des Inhalts von Zeichenfolgeneigenschaften suchen oder Bitmasken Vergleiche durchführen.

Beispielsweise können Sie den Inhalt des Betreffs von Elementen mithilfe der [SearchFilter. ContainsSubstring](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) -Klasse im verwaltete EWS-API durchsuchen. In diesem Beispiel wird ein Suchfilter erstellt, um den Betreff nach der Teilzeichenfolge "Besprechungsnotizen" zu durchsuchen, wobei Case ignoriert wird.

```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

Sie können auch nach benutzerdefinierten Eigenschaften suchen. In diesem Beispiel wird die benutzerdefinierte Eigenschaft **itemIndex** nach Werten größer als 3 durchsucht.

```cs
Guid MyAppGuid = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
ExtendedPropertyDefinition customPropDefinition =
    new ExtendedPropertyDefinition(MyAppGuid, "ItemIndex", MapiPropertyType.Integer);
SearchFilter.IsGreaterThan customPropFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
```

Sie können auch mehrere Suchfilter kombinieren, um komplexere Suchvorgänge zu erstellen. Sie können beispielsweise die beiden vorherigen Filter mit einer logischen und mithilfe der [SearchFilter. SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) -Klasse kombinieren.

```cs
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, customPropFilter);
```

### <a name="using-a-query-string"></a>Verwenden einer Abfragezeichenfolge

Abfragezeichenfolgen bieten einen anderen Ansatz für die Suche. Sie haben geringere Kontrolle über die Felder, die durchsucht werden, und wie die Suche durchgeführt wird, wenn Sie eine Abfragezeichen folgen Suche verwenden. Nicht, dass das eine schlechte Sache ist! In einigen Fällen sollten Sie sozusagen ein größeres Netz umwandeln.

Sie können beispielsweise mithilfe der [Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/jj223808%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode nach" Besprechungsnotizen "suchen.

```cs
FindItemsResults<Item> results = service.FindItems(folder, "meeting notes", view);
```

Wenn Sie die Ergebnisse dieser Suche mit den Ergebnissen des **SearchFilter. ContainsSubstring** -Such Beispiels zuvor vergleichen, enthält diese Suche weitere Ergebnisse. Die Suchfilter Suche gibt nur Elemente mit dem Betreff "Besprechungsnotizen" zurück, während diese Suche Elemente mit "Besprechungsnotizen" im Betreff, im Textkörper und in anderen Feldern zurückgibt.

Sehen wir uns an, wie Sie die Abfragezeichenfolge verfeinern können, um die Ergebnisse näher an den Suchfilter zu erhalten. Mit AQS können Sie die Suche auf den Betreff beschränken.

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:meeting notes", view);
```

Dies ist näher, aber die Ergebnisse sind immer noch nicht ganz identisch. Wenn Sie eine Abfragezeichenfolge mit mehreren Wörtern verwenden, erhalten Sie Übereinstimmungen auch dann, wenn die Wörter nicht in der angegebenen Reihenfolge angegeben sind oder wenn Sie nicht nebeneinander liegen. Mit der Abfragezeichenfolge "Betreff: Besprechungsnotizen" werden Übereinstimmungen für "Besprechungsnotizen", "Notizen aus der Besprechung" usw. abgerufen. Zur weiteren Verfeinerung können Sie die Suchbegriffe in doppelte Anführungszeichen einschließen, um anzugeben, dass Sie diesen Ausdruck nur wünschen.

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:\"meeting notes\"", view);
```

## <a name="requesting-specific-properties-in-search-results"></a>Anfordern bestimmter Eigenschaften in Suchergebnissen
<a name="bk_RequestSpecific"> </a>

Standardmäßig enthalten die Suchergebnisse alle Eigenschaften für die Elemente, die mit der Suche übereinstimmen. In einigen Fällen ist dies möglicherweise das, was Sie wünschen, in den meisten Fällen erfordert Ihre Anwendung jedoch nur einen diskreten Eigenschaftensatz. In diesem Fall sollten Sie die Eigenschaften einschränken, die nur auf die Eigenschaften zurückgegeben werden, die Ihre Anwendung benötigt. Im folgenden Beispiel wird die [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) -Klasse verwendet, um die zurückgegebenen Eigenschaften auf den Betreff, das empfangene Datum/die Uhrzeit und die ID der Elemente zu beschränken.

```cs
ItemView view = new ItemView(10);
// Creating a new PropertySet with this constructor includes
// ItemSchema.Id.
view.PropertySet = new PropertySet(ItemSchema.Subject, ItemSchema.DateTimeReceived);
```

## <a name="controlling-search-depth"></a>Steuern der Such Tiefe
<a name="bk_SearchDepth"> </a>

Durch das Festlegen des Durchlaufs in der Ansicht werden die Tiefe und der Umfang der Suche gesteuert.

**Tabelle 2. Such Durchlaufwerte**

|**Durchlauf Wert**|**Gilt für**|**Beschreibung**|
|:-----|:-----|:-----|
|Flachen  <br/> |Elemente und Ordner  <br/> |Flache Suchvorgänge sind auf direkte untergeordnete Elemente des durchsuchten Ordners limitiert.  <br/> |
|Tiefe  <br/> |Elemente (nur mit Suchordnern) und Ordnern  <br/> |Bei Tiefensuchen wird der zu suchende Ordner und Unterordner rekursiv durchsucht.  <br/> |
|Zugeordnet  <br/> |Elemente  <br/> |Zugeordnete Suchvorgänge enthalten nur zugeordnete Elemente aus dem Ordner, der durchsucht wird. Zugeordnete Elemente sind ausgeblendete Elemente innerhalb des Ordners.  <br/> |
|SoftDeleted  <br/> |Elemente und Ordner  <br/> |Dieser Traversale Typ ist veraltet. SoftDeleted-Suchvorgänge enthalten nur Elemente, die sich im Papierkorb befinden. Der Papierkorb wurde durch den [Ordner "Wiederherstellbare Elemente"](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder) in Exchange Online ersetzt, Exchange Online im Rahmen von Office 365 und Exchange-Versionen, die mit Exchange 2010 beginnen.  <br/> |

## <a name="managing-search-results"></a>Verwalten von Suchergebnissen
<a name="bk_ManageSearchResults"> </a>

Mit den verwaltete EWS-API und EWS können Sie auch ändern, wie Ihre Suchergebnisse zurückgegeben werden. Sie können Ansichten verwenden, um anzugeben, welche Eigenschaften in den Ergebnissen enthalten sind, Ergebnisse zu sortieren und die Ergebnisse auf der Seite zu erhalten, um nur eine festgelegte Anzahl von Ergebnissen pro Antwort zurückzukehren. Sie können auch Ergebnisse nach bestimmten Feldwerten gruppieren und die Tiefe einer Suche steuern, indem Sie einen Traversalen Typ angeben. Schließlich können Sie Suchordner verwenden, um dauerhafte Suchvorgänge zu erstellen, die dynamisch aktualisiert werden, wenn neue Elemente eintreffen.

### <a name="sorting"></a>Die Sortierung

Sie können den Server zum Zurückgeben sortierter Ergebnisse abrufen, wodurch es einfacher ist, Elemente in der richtigen Reihenfolge anzuzeigen oder zu verarbeiten. In diesem Beispiel werden die Ergebnisse nach dem empfangenen Datum/der Uhrzeit sortiert, wobei die neuesten Elemente als erstes verwendet werden.

```cs
view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
```

### <a name="paging"></a>Paging

Wenn Sie eine Suchanforderung mithilfe der verwaltete EWS-API oder EWS senden, geben Sie eine Ansichtsgröße an, die die maximale Anzahl zurückgegebener Elemente steuert. Die Anzahl der Elemente auf dem Server, die mit Ihrer Suche übereinstimmen, kann jedoch größer sein als die Größe der Ansicht. In diesem Fall gibt der Server an, dass weitere Elemente verfügbar sind. Sie können [Paging verwenden, um die Suche zu wiederholen](how-to-perform-paged-searches-by-using-ews-in-exchange.md) und die nächsten Ergebnisse zu erhalten.

Sie können beispielsweise eine Suchanfrage mit einer Ansichtsgröße von 10 senden. Es können 15 Elemente auf dem Server vorhanden sein, die mit Ihrer Suche übereinstimmen, aber Sie erhalten nur die ersten 10 zurück, zusammen mit einem Indikator ( [FindItemsResults \<TItem\> . MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) -Eigenschaft wenn Sie die verwaltete EWS-API) verwenden, werden auf dem Server weitere Ergebnisse angezeigt. Sie können die gleiche Suche dann mit einem Offset von 10 senden, um nach den nächsten 10 Elementen zu Fragen, die Ihrer Suche entsprechen. Der Server gibt die restlichen fünf Elemente zurück.

**Abbildung 1. Beispiel für eine Auslagerungs Suche**

![Eine Abbildung einer Seitensuche. Es wird eine erste Anforderung für 10 Elemente gesendet. Eine zweite Anforderung wird für die nächsten 10 Elemente gesendet.](media/Ex15_Search_PagedSearch.png)

### <a name="grouping"></a>Gruppieren

 Exchange ermöglicht Ihnen das Gruppieren von Suchergebnissen nach einem bestimmten Feld. Dies kann dazu beitragen, Suchergebnisse in besser verwaltbare Sätze zu unterteilen. Sie können beispielsweise nach "Besprechungsnotizen" suchen und die Ergebnisse nach Absender gruppieren. Wie in der folgenden Abbildung dargestellt, werden die zurückgegebenen Elemente in Gruppen unterteilt, wobei alle Elemente, die mit den Kriterien des gleichen Absenders in einer Gruppe übereinstimmen, alle übereinstimmenden Elemente eines anderen Absenders in einer anderen Gruppe usw.

**Abbildung 2. Nach Absender gruppierte Suchergebnisse**

![Eine Abbildung, in der Suchergebnisse nach Absender gruppiert sind](media/Ex15_Search_GroupedResults.png)

## <a name="search-folders"></a>Suchordner
<a name="bk_SearchFolders"> </a>

Bei einer regulären Suche wird die Suche ausgeführt, die Ergebnisse werden zur Verarbeitung an Ihre Anwendung zurückgegeben, und die Suche ist nicht mehr vorhanden. Suchordner bieten eine Möglichkeit, eine Suche persistent zu machen. Dies ist eine hervorragende Option für Suchvorgänge, die Sie mehrmals ausführen möchten. Anstatt dieselbe Suche wiederholt auszuführen, wodurch der Server jedes Mal die Suche von Grund auf neu auswertet, führt ein Suchordner immer eine Suche aus, sodass der Server das vorhandene Resultset aktualisieren kann, wenn dem Suchbereich Elemente hinzugefügt oder daraus entfernt werden. Suchordner fungieren wie reguläre Ordner, indem Sie als Ordner mit Elementen angezeigt werden. Der Unterschied besteht darin, dass die einzigen im Ordner enthaltenen Elemente diejenigen sind, die den Suchkriterien entsprechen, die dem Ordner zugeordnet sind. Nachdem ein Suchordner erstellt wurde, kann Ihre Anwendung aktuelle Ergebnisse der Suche abrufen, indem Sie den Inhalt des Ordners überprüft.

Das Erstellen eines Suchordners ist einfach, wenn Sie die Erstellung von Suchfiltern beherrscht haben. Im folgenden Beispiel wird ein Suchordner erstellt, um alle e-Mails mit einem Betreff anzuzeigen, der "Besprechungsnotizen" enthält.

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

- [Einschränkungsrichtlinien Parameter, die sich auf EWS-Suchvorgänge auswirken](ews-throttling-in-exchange.md#throttling-policy-parameters-that-affect-ews-search-operations)
