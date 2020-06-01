---
title: Verwenden von Suchfiltern mit EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 20fc6d2d-41c2-4490-98b8-c52513977fef
description: Erfahren Sie, wie Sie mit der verwalteten EWS-API oder mit EWS in Exchange Suchfilter verwenden.
localization_priority: Priority
ms.openlocfilehash: 04a74ec92d4bced8abd58d164a1c186d6405e679
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455835"
---
# <a name="use-search-filters-with-ews-in-exchange"></a>Verwenden von Suchfiltern mit EWS in Exchange

Erfahren Sie, wie Sie mit der verwalteten EWS-API oder mit EWS in Exchange Suchfilter verwenden.
  
Suchfilter sind das primäre Tool zum Ausdrücken von Suchkriterien in Ihrer verwalteten EWS-API oder EWS-Anwendung. Für folgende Vorgänge empfehlen wir Suchfilter statt [Abfragezeichenfolgen](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md) zu verwenden:
  
- Suchen nach einer bestimmten Eigenschaft oder mehreren Eigenschaften  
- Suchen mithilfe von mehreren Suchkriterien
    
Suchfilter sind Ihre einzige Option, wenn Sie einen der folgenden Vorgänge ausführen möchten:
  
- Suchen nach benutzerdefinierten Eigenschaften  
- Suchen nach Zeichenfolgen unter Beachtung der Groß-/Kleinschreibung  
- Durchführen von Suchen in Zeichenfolgen nach Präfix- oder genauen Übereinstimmungen 
- Durchführen von Bitmaskensuchen
- Suchen nach Elementen mit einem bestimmten Eigenschaftensatz, unabhängig des Werts
- Suchen nach Ordnern
- Erstellen von Suchordnern
    
## <a name="determine-what-type-of-search-filter-you-need"></a>Bestimmen der benötigten Suchfiltertypen
<a name="bk_SelectFilter"> </a>

Bevor Sie einen Suchfilter erstellen, müssen Sie zunächst die benötigten Suchfiltertypen bestimmen. Die Filtertypen sind als nachfolgende Klassen der [SearchFilter](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx)-Klasse in der verwalteten EWS-API, und als untergeordnete Elemente des [Restriction](https://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx)-Elements in EWS implementiert. 
  
**Tabelle 1. Suchfiltertypen**

|**Filtertyp**|**Verwaltete EWS-API-Klasse**|**EWS-Element**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|"Enthält"-Filter  <br/> |[ContainsSubstring](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) <br/> |[Enthält](https://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) <br/> |Der beste Filtertyp für Zeichenfolgevergleiche. Damit können Sie die Groß-/Kleinschreibung überwachen, angeben, ob Leerzeichen ignoriert werden, und den Aufnahmemodus festlegen.  <br/> |
|Bitmaskenfilter  <br/> |[ExcludesBitmask](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.excludesbitmask%28v=exchg.80%29.aspx) <br/> |[Schließt](https://msdn.microsoft.com/library/bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1%28Office.15%29.aspx) <br/> |Damit können Sie nach ganzzahlige Eigenschaften als Bitmasken suchen und nur Ergebnisse zurückgeben, bei denen Bits entsprechend der angegebenen Bitmaske nicht festgelegt sind.  <br/> |
|"Vorhanden"-Filter  <br/> |[Exists](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.exists%28v=exchg.80%29.aspx) <br/> |[Exists](https://msdn.microsoft.com/library/55d568bd-8dbc-4d50-b9d7-54b74a54d4b5%28Office.15%29.aspx) <br/> |Gibt alle Elemente zurück, bei denen die angegebene Eigenschaft vorhanden ist, unabhängig des Werts.  <br/> |
|Gleichheitsfilter  <br/> |[IsEqualTo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isequalto%28v=exchg.80%29.aspx) <br/> [IsNotEqualTo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isnotequalto%28v=exchg.80%29.aspx) <br/> |[IsEqualTo](https://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx) <br/> [IsNotEqualTo](https://msdn.microsoft.com/library/e2eff26c-3403-45cd-bb74-1eb98c7dbfcd%28Office.15%29.aspx) <br/> |Vergleicht den Wert der angegebenen Eigenschaft mit einem angegebenen Konstantenwert oder dem Wert einer anderen Eigenschaft und gibt alle Elemente mit einem gleichen Wert (im Falle eines **IsEqualTo**-Filters) oder einen nicht gleichen Wert (im Falle eines **IsNotEqualTo**-Filters) zurück.  <br/> |
|Relationaler Testfilter  <br/> |[IsGreaterThan](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthan%28v=exchg.80%29.aspx) <br/> [IsGreaterThanOrEqualTo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthanorequalto%28v=exchg.80%29.aspx) <br/> [IsLessThan](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.islessthan%28v=exchg.80%29.aspx) <br/> [IsLessThanOrEqualTo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.islessthanorequalto%28v=exchg.80%29.aspx) <br/> |[IsGreaterThan](https://msdn.microsoft.com/library/a6e9d462-cfa7-40ec-903e-128c95050352%28Office.15%29.aspx) <br/> [IsGreaterThanOrEqualTo](https://msdn.microsoft.com/library/373cc954-314d-40e2-be03-cc08aefc0d5b%28Office.15%29.aspx) <br/> [IsLessThan](https://msdn.microsoft.com/library/2550469b-6e5d-45a5-9ecc-090d1b409296%28Office.15%29.aspx) <br/> [IsLessThanOrEqualTo](https://msdn.microsoft.com/library/b5d85eb2-5e15-4d01-ad49-6289e735ad8a%28Office.15%29.aspx) <br/> |Gibt alle Elemente zurück, die für die angegebene Eigenschaft in der entsprechenden Beziehung einen Wert für einen angegebenen Konstantenwert oder eine andere Eigenschaft besitzen. Ein **IsGreaterThan**-Filter gibt alle Elemente zurück, die einen höheren Wert besitzen als der angegebene Wert in der angegebenen Eigenschaft.  <br/> |
|Aufhebungsfilter  <br/> |[Not](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.not%28v=exchg.80%29.aspx) <br/> |[not](https://msdn.microsoft.com/library/1aa16318-7e90-4b19-bce8-dd1a20a66223%28Office.15%29.aspx) <br/> |Hebt das Ergebnis der anderen Filter auf.  <br/> |
|Zusammengesetzter Filter  <br/> |[SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) <br/> |[Und](https://msdn.microsoft.com/library/790246c2-37ad-49a8-91b9-6186d743b011%28Office.15%29.aspx) <br/> [- oder -](https://msdn.microsoft.com/library/4876d83a-73a3-4953-9d95-3048e6b76ccb%28Office.15%29.aspx) <br/> |Kombiniert mehrere Filter, damit komplexere Suchkriterien möglich sind.  <br/> |
   
### <a name="contains-filter"></a>"Enthält"-Filter

Ein "Enthält"-Filter ist die beste Wahl zum Durchsuchen von Zeichenfolgeneigenschaften. Mit einem "Enthält"-Filter können Sie Aspekte des Zeichenfolgeabgleichs steuern, wie z. B. die Groß-/Kleinschreibung und die Behandlung von Leerzeichen, indem Sie den Aufnahme- und Vergleichsmodus festlegen.
  
#### <a name="contains-filter-in-the-ews-managed-api"></a>Der "Enthält"-Filter in der verwalteten EWS-API
<a name="bk_ContainsEWSMA"> </a>

Wenn Sie die verwaltete EWS-API verwenden, legen Sie den Aufnahmemodus fest, indem Sie die [ContainmentMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.containmentmode%28v=exchg.80%29.aspx)-Eigenschaft der [ContainsSubstring](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx)-Klasse verwenden, und Sie legen den Vergleichsmodus fest, indem Sie die [ComparisonMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.comparisonmode%28v=exchg.80%29.aspx)-Eigenschaft der **ContainsSubstring**-Klasse verwenden. In den folgenden Beispielen wird veranschaulicht, wie Sie einen Suchfilter erstellen, der das Betrefffeld der Elemente nach der Teilzeichenfolge „Besprechungsnotizen" durchsucht. In diesem Beispiel wird die Groß-/Kleinschreibung ignoriert, Leerzeichen jedoch nicht. 
  
```cs
// Find all items with a subject that contain the substring
// "meeting notes", regardless of case.
// Matches include:
//   - meeting notes
//   - Meeting Notes
//   - Here are my meeting notes
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

#### <a name="contains-filter-in-ews"></a>Der "Enthält"-Filter in EWS
<a name="bk_ContainsEWSMA"> </a>

In EWS legen Sie den Aufnahmemodus fest, indem Sie das **ContainmentMode**-Attribut für das [Enthält](https://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx)-Element verwenden, und den Vergleichsmodus festlegen, indem Sie das **ContainmentComparison**-Attribut für das **Contains**-Element verwenden. Im folgenden Beispiel wird veranschaulicht, wie einen Suchfilter zum Durchsuchen des Suchfelds von Elementen nach der Teilzeichenfolge „Besprechungsnotizen" erstellen. In diesem Beispiel wird die Groß-/Kleinschreibung ignoriert, Leerzeichen jedoch nicht. 
  
```XML
<t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
  <t:FieldURI FieldURI="item:Subject" />
  <t:Constant Value="meeting notes" />
</t:Contains>
```

### <a name="bitmask-filter"></a>Bitmaskenfilter

Mit einem Bitmaskenfilter können Sie ganzzahlige Eigenschaften als Bitmasken durchsuchen, und Ergebnisse zurückgeben, in denen bestimmte Bits nicht im Wert der angegebenen Eigenschaft festgelegt sind.
  
#### <a name="bitmask-filter-in-the-ews-managed-api"></a>Bitmaskenfilter in der verwalteten EWS-API

Im folgenden Beispiel wird veranschaulicht, wie Sie die verwaltete EWS-API zum Erstellen eines Suchfilters verwendet wird, um alle Elemente zurückzugeben, bei denen sich in der benutzerdefinierten **ItemIndex**-Eigenschaft ein Wert befindet (definiert im Abschnitt [Beispiel: Suchen von Elementen mithilfe eines Suchfilters und der verwalteten EWS-API](#bk_ExampleEWSMA) dieses Artikels), die den sekundären Bitsatz (10 in der Binärdatei) nicht aufweisen. 
  
```cs
// Find all items with a value of the custom property that does not
// have the second bit (0010) set.
// Matches include:
//   - Property not set
//   - 1 (0001)
//   - 4 (0100)
//   - 5 (0101)
//   - 8 (1000)
SearchFilter.ExcludesBitmask bit2NotSetFilter = 
    new SearchFilter.ExcludesBitmask(customPropDefinition, 2);
```

#### <a name="bitmask-filter-in-ews"></a>Bitmaskenfilter in EWS

Im folgenden Beispiel wird veranschaulicht, wie Sie mithilfe von EWS einen Suchfilter erstellen können, um alle Elemente zurückzugeben, die in der benutzerdefinierten **ItemIndex**-Eigenschaft (definiert im Abschnitt [Beispiel: Suchen von Elementen mithilfe eines Suchfilters und der verwalteten EWS-API](#bk_ExampleEWSMA) dieses Artikels), die den sekundären Bitsatz (10 in der Binärdatei) nicht aufweisen. 
  
```XML
<t:Excludes>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:Bitmask Value="2" />
</t:Excludes>
```

### <a name="exists-filter"></a>"Vorhanden"-Filter

Mit einem "Vorhanden"-Filter können Sie nach Elementen suchen, die unabhängig des Werts einen bestimmten Eigenschaftensatz besitzen.
  
#### <a name="exists-filter-in-the-ews-managed-api"></a>"Vorhanden"-Filter in der verwalteten EWS-API

Im folgenden Beispiel wird veranschaulicht, wie ein Suchfilter erstellt wird, mit dem alle Elemente zurückgegeben werden, die einen benutzerdefinierten **ItemIndex**-Eigenschaftensatz besitzen. 
  
```cs
// Find all items that have the custom property set.
SearchFilter.Exists customPropSetFilter =
    new SearchFilter.Exists(customPropDefinition);
```

#### <a name="exists-filter-in-ews"></a>"Vorhanden"-Filter in EWS

Im folgenden Beispiel wird veranschaulicht, wie ein Suchfilter erstellt wird, um alle Elemente zurückzugeben, die den benutzerdefinierten **ItemIndex**-Eigenschaftensatz aufweisen. 
  
```XML
<t:Exists>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
</t:Exists>
```

### <a name="equality-filter"></a>Gleichheitsfilter

Mit Gleichheitsfiltern können Sie nach allen Elementen suchen, die einen Wert für die bestimmte Eigenschaft aufweisen, die mit einem bestimmten Wert übereinstimmt oder mit einem bestimmten Wert nicht übereinstimmt. Der zu vergleichende Wert kann ein Konstantenwert oder der Wert zu einer anderen Eigenschaft jedes Elements sein.
  
#### <a name="equality-filter-in-the-ews-managed-api"></a>Der Gleichheitsfilter in der verwalteten EWS-API

Im folgenden Beispiel wird veranschaulicht, wie Sie die verwaltete EWS-API zum Erstellen eines Suchfilters verwenden können, damit alle Elemente zurückgegeben werden, die noch nicht gelesen wurden.
  
```cs
// Find all items that are not marked as read.
SearchFilter.IsEqualTo unreadFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false);
```

Im folgenden Beispiel wird veranschaulicht, wie ein Suchfilter erstellt wird, um alle Elemente zurückzugeben, die einen Wert in der **ItemIndex**-Eigenschaft besitzen, der nicht mit der Größe des Elements übereinstimmt. 
  
```cs
// Find all items that are marked as read.
SearchFilter.IsNotEqualTo indexNotEqualToSizeFilter =
    new SearchFilter.IsNotEqualTo(customPropDefinition, ItemSchema.Size);
```

#### <a name="equality-filter-in-ews"></a>Gleichheitsfilter in EWS

Im folgenden Beispiel wird veranschaulicht, wie EWS zum Erstellen eines Suchfilters verwendet wird, damit alle Elemente zurückgegeben werden, die noch nicht gelesen wurden.
  
```XML
<t:IsEqualTo>
  <t:FieldURI FieldURI="message:IsRead" />
  <t:FieldURIOrConstant>
    <t:Constant Value="false" />
  </t:FieldURIOrConstant>
</t:IsEqualTo>
```

Im folgenden Beispiel wird veranschaulicht, wie ein Suchfilter erstellt wird, sodass alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben wird, der nicht mit der Größe des Elements übereinstimmt. 
  
```XML
<t:IsNotEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:FieldURI FieldURI="item:Size" />
  </t:FieldURIOrConstant>
</t:IsNotEqualTo>
```

### <a name="relational-testing-filter"></a>Relationaler Testfilter

Mit relationalen Testfiltern können Sie nach allen Elementen suchen, die in der angegebenen Eigenschaft einen Wert aufweisen, der entweder größer als (\>), größer als oder gleich (\>=), kleiner als (\<), oder kleiner als oder gleich (\<=) einem angegebenen Wert ist. Der zu vergleichende Wert kann ein Konstantenwert oder der Wert einer anderen Eigenschaft der einzelnen Elemente sein.
  
#### <a name="relational-testing-filter-in-the-ews-managed-api"></a>Der relational Testfilter in der verwalteten EWS-API

Im folgenden Beispiel wird veranschaulicht, wie die verwaltete EWS-API zum Erstellen von Suchfiltern verwendet werden kann, damit alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben werden, die die angegebene Beziehung zum Konstantenwert 3 aufweisen. 
  
```cs
// Find all items where the custom property value is > 3.
SearchFilter.IsGreaterThan greaterThanFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
// Find all items where the custom property value is >= 3.
SearchFilter.IsGreaterThanOrEqualTo greaterThanOrEqualFilter =
    new SearchFilter.IsGreaterThanOrEqualTo(customPropDefinition, ItemSchema.Size);
// Find all items where the custom property value is < 3.
SearchFilter.IsLessThan lessThanFilter =
    new SearchFilter.IsLessThan(customPropDefinition, 3);
// Find all items where the custom property value is <= 3.
SearchFilter.IsLessThanOrEqualTo lessThanOrEqualFilter =
    new SearchFilter.IsLessThanOrEqualTo(customPropDefinition, 3);
```

#### <a name="relational-testing-filter-in-ews"></a>Der relationale Testfilter in EWS

Im folgenden Beispiel wird veranschaulicht, wie Sie EWS zum Erstellen eines Suchfilters verwenden können, damit alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben werden, der höher ist als Konstantenwert 3. 
  
```XML
<t:IsGreaterThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThan>
```

Im folgenden Beispiel wird veranschaulicht, wie Sie einen Suchfilter erstellen können, damit alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben werden, der größer oder gleich Konstantenwert 3 ist. 
  
```XML
<t:IsGreaterThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThanOrEqualTo>
```

Im folgenden Beispiel wird veranschaulicht, wie Sie einen Suchfilter erstellen können, damit alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben werden, der kleiner ist als Konstantenwert 3. 
  
```XML
<t:IsLessThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThan>
```

Im folgenden Beispiel wird veranschaulicht, wie Sie einen Suchfilter erstellen, damit alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben werden, der kleiner oder gleich Konstantenwert 3 ist. 
  
```XML
<t:IsLessThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThanOrEqualTo>
```

### <a name="negating-filter"></a>Aufhebungsfilter

Mit einem Aufhebungsfilter können Sie einen anderen Filter aufheben und gegenteilige Suchergebnisse erhalten. Während andere Filter Ergebnisse zurückgeben, die mit einem bestimmten Suchkriterium übereinstimmen, gibt ein Aufhebungsfilter Ergebnisse zurück, die nicht mit dem angegebenen Filterkriterium übereinstimmen.
  
#### <a name="negating-filter-in-the-ews-managed-api"></a>Der Aufhebungsfilter in der verwalteten EWS-API

Im folgenden Beispiel wird veranschaulicht, Sie sie die verwaltete EWS-API zum Erstellen eines Suchfilters verwenden können, damit alle Elemente zurückgegeben werden, in denen die Teilzeichenfolge „Besprechungsnotizen" nicht im Betreff enthalten ist.
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
SearchFilter.Not subjectNotFilter =
    new SearchFilter.Not(subjectFilter);
```

#### <a name="negating-filter-in-ews"></a>Der Aufhebungsfilter in EWS

Im folgenden Beispiel wird veranschaulicht, wie Sie einen Suchfilter erstellen können, damit alle Elemente zurückgegeben werden, in denen die Teilzeichenfolge„Besprechungsnotizen" nicht im Betreff enthalten ist.
  
```XML
<t:Not>
  <t:Contains ContainmentMode="ExactPhrase" ContainmentComparison="IgnoreCase">
    <t:FieldURI FieldURI="item:Subject" />
    <t:Constant Value="meeting notes" />
  </t:Contains>
</t:Not>
```

### <a name="compound-filter"></a>Zusammengesetzter Filter

Mit einem zusammengesetzten Filter können Sie mehrere Filter kombinieren, um komplexere Suchkriterien erstellen zu können. Sie können Kriterien mithilfe des logischen Operators AND oder OR kombinieren. So können Sie Suchen wie z. B. „alle Nachrichten Sadie Daniels, bei denen 'Besprechungsnotizen' im Betreff enthalten ist".
  
#### <a name="compound-filter-in-the-ews-managed-api"></a>Der zusammengesetzte Filter in der verwalteten EWS-API

Im folgenden Beispiel wird veranschaulicht, wie Sie die verwaltete EWS-API zum Erstellen eines Suchfilters verwenden können, damit alle Elemente zurückgegeben werden, die von Sadie Daniels gesendet wurden und „Besprechungsnotizen" im Betreff enthalten.
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
EmailAddress manager = new EmailAddress("sadie@contoso.com");
SearchFilter.IsEqualTo fromManagerFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, fromManagerFilter);
```

#### <a name="compound-filter-in-ews"></a>Der zusammengesetzte Filter in EWS

Im folgenden Beispiel wird veranschaulicht, wie EWS zum Erstellen eines Suchfilters verwendet werden kann, damit alle Elemente zurückgegeben werden, die von Sadie Daniels gesendet wurden und „Besprechungsnotizen" im Betreff enthalten.
  
```XML
<t:And>
  <t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
    <t:FieldURI FieldURI="item:Subject" />
    <t:Constant Value="meeting notes" />
  </t:Contains>
  <t:IsEqualTo>
    <t:FieldURI FieldURI="message:Sender" />
    <t:FieldURIOrConstant>
      <t:Constant Value="sadie@fourthcoffee.com" />
    </t:FieldURIOrConstant>
  </t:IsEqualTo>
</t:And>
```

## <a name="example-find-items-by-using-a-search-filter-and-the-ews-managed-api"></a>Beispiel: Suchen von Elementen mithilfe eines Suchfilters und der verwalteten EWS-API
<a name="bk_ExampleEWSMA"> </a>

Folgende verwaltete EWS-API-Methoden verwenden Suchfilter:
  
- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
- [ExchangeService.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
- [Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
- [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
Im folgenden Beispiel wird die **ExchangeService.FindItems**-Methode verwendet; die gleichen Regeln und Konzepte gelten jedoch für alle Methoden. In diesem Beispiel wird eine Methode mit der Bezeichnung **SearchWithFilter** definiert. Als Parameter ist ein [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt, ein [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)-Objekt und ein [SearchFilter](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx)-Objekt erforderlich. In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde. Die **SearchFilter**-Klasse ist die Basisklasse für alle verschiedenen Suchfilter. 
  
```cs
using Microsoft.Exchange.WebServices.Data
private static Guid SearchTestGUID = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
private static ExtendedPropertyDefinition customPropDefinition =
        new ExtendedPropertyDefinition(SearchTestGUID, "ItemIndex", MapiPropertyType.Integer);
static void SearchWithFilter(ExchangeService service, WellKnownFolderName folder, SearchFilter filter)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject, 
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead,
                                       customPropDefinition);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        FindItemsResults<Item> results = service.FindItems(folder, filter, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
            if (item.ExtendedProperties.Count > 0 &&
                 item.ExtendedProperties[0].PropertyDefinition == customPropDefinition)
            {
                Console.WriteLine("Search Index: {0}", item.ExtendedProperties[0].Value);
            }
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

Sie können diese Funktion mit jedem in den Beispielen dieses Artikels veranschaulichten Suchfilter verwenden. In diesem Beispiel wird ein zusammengesetzter Filter verwendet, damit alle Elemente aus dem Posteingang von Sadie Daniels mit „Besprechungsnotizen" im Betreff zurückgegeben werden.
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
EmailAddress manager = new EmailAddress("sadie@contoso.com");
SearchFilter.IsEqualTo fromManagerFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, greaterThanFilter);
SearchWithFilter(service, WellKnownFolderName.Inbox, compoundFilter);
```

## <a name="example-find-an-item-by-using-a-search-filter-and-ews"></a>Beispiel: Suchen eines Elements mithilfe eines Suchfilters und EWS
<a name="bk_ExampleEWS"> </a>

Folgende EWS-Operationen verwenden Suchfilter:
  
- [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
- [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
Im folgenden Beispiel wird die **FindItem**-Operation verwendet; die gleichen Regeln und Konzepte gelten jedoch für beide Operationen. Suchfilter sind im [Restriction](https://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx)-Element in SOAP-Anforderungen enthalten. In diesem Beispiel wird eine SOAP-Anforderung gesendet, die der Suche entspricht, die im vorangegangenen Beispiel der verwalteten EWS-API veranschaulicht wird. 
  
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
          <t:FieldURI FieldURI="message:IsRead" />
          <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:And>
          <t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
            <t:FieldURI FieldURI="item:Subject" />
            <t:Constant Value="meeting notes" />
          </t:Contains>
          <t:IsEqualTo>
            <t:FieldURI FieldURI="message:Sender" />
            <t:FieldURIOrConstant>
              <t:Constant Value="sadie@contoso.com" />
            </t:FieldURIOrConstant>
          </t:IsEqualTo>
        </t:And>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Im folgenden Beispiel wird die Antwort vom Server einschließlich der Suchergebnisse veranschaulicht.
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
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
          <m:RootFolder IndexedPagingOffset="3" TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>5</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting Notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>6</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>7</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="next-steps"></a>Nächste Schritte
<a name="bk_ExampleEWS"> </a>

Da Sie nun mit der Verwendung von Suchfiltern in einfachen Suchen vertraut sind, können Sie mit fortschrittlicheren Suchtechniken fortfahren.
  
- [Durchführen gruppierter Suchen mithilfe von EWS in Exchange](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)
    
- [Durchführen seitenweiter Suchen mithilfe von EWS in Exchange](how-to-perform-paged-searches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [Suche und EWS in Exchange](search-and-ews-in-exchange.md)    
- [Durchführen einer AQS-Suche mithilfe von EWS in Exchange](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)   
- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [ExchangeService.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)    
- [Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)    
- [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)    
- [FindFolder-Vorgang](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)   
- [FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

