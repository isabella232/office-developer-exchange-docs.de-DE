---
title: Führen Sie gruppierte Suchvorgänge in Exchange mithilfe der Exchange-Webdienste aus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 55de92eb-8e8b-4156-8ad9-dd3828024242
description: Erfahren Sie, wie Sie gruppierten Suchvorgänge in die EWS Managed API oder EWS-Anwendung, die beruht auf Exchange ausführen.
ms.openlocfilehash: 63a796e2c724351c15287a5596a9a063954f8b40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756977"
---
# <a name="perform-grouped-searches-by-using-ews-in-exchange"></a>Führen Sie gruppierte Suchvorgänge in Exchange mithilfe der Exchange-Webdienste aus

Erfahren Sie, wie Sie gruppierten Suchvorgänge in die EWS Managed API oder EWS-Anwendung, die beruht auf Exchange ausführen.
  
Gruppierte Suchvorgänge sind hilfreich, da sie können Sie steuern, wie Suchergebnisse geordnet sind. Organisierten Suchergebnisse können erleichtern für die Anwendung zum Verarbeiten von Ergebnissen oder in ein Endbenutzer in einer verwaltbaren Weise angezeigt werden.
  
Gruppieren von Works durch werden die Websitemigration alle Elemente innerhalb des Resultsets, die den gleichen Wert eines bestimmten Felds in einer Gruppe aufweisen. Sie können die Ergebnisse vom Absender, gruppieren und alle Elemente aus der gleichen Person kann in einer separaten Gruppe und der Elemente innerhalb jeder Gruppe gemäß der Reihenfolge aus, die Sie, in der Ansicht angeben sortiert werden sollen. Die Gruppen selbst werden durch einen aggregierten Wert basierend auf einem Feld gewählte sortiert.
  
**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge zum Organisieren von Suchergebnissen**

|**Aktion**|**Verwenden Sie in die EWS Managed API...**|**Verwenden Sie in der Exchange-Webdienste...**|
|:-----|:-----|:-----|
|Organisieren Sie Elemente mit demselben Wert in einer bestimmten Eigenschaft in die Ergebnisse in Gruppen.  <br/> |[Grouping.GroupOn](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.groupon%28v=exchg.80%29.aspx) <br/> |[FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) -Element als untergeordnetes Element des Elements [GroupBy](http://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx)  <br/> |
|Sortieren der Elemente innerhalb jeder Gruppe durch den Wert in eine bestimmte Eigenschaft  <br/> |[ItemView.OrderBy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) <br/> |[SortOrder](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) -element  <br/> |
|Sortieren der Gruppen  <br/> |[Grouping.AggregateOn](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) <br/><br/> [Grouping.AggregateType](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) <br/><br/> [Grouping.SortDirection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) <br/> |**FieldURI** -Element als untergeordnetes Element des Elements [AggregateOn](http://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx)<br/><br/> **Aggregate** -Attribut für das **AggregateOn** -element<br/><br/>**Reihenfolge** -Attribut die **GroupBy** -element  <br/> |
   
Betrachten sie Schritt für Schritt.
  
## <a name="group-results-by-a-specific-property"></a>Gruppieren von Ergebnissen nach einer bestimmten Eigenschaft
<a name="bk_GroupResults"> </a>

Der erste Schritt bei der Verwendung der Gruppierung ist, wählen Sie eine Eigenschaft oder-Attribut für die Elemente im Exchange-Speicher, nach dem gruppiert werden. Die EWS Managed API stellt diese als Klasseneigenschaften auf die entsprechenden Klassen, während EWS als XML-Elemente macht. Sie können eine beliebige Eigenschaft, einschließlich der benutzerdefinierte oder erweiterte Eigenschaften auswählen, aber es ist hilfreich, zu verstehen, wie die Elemente basierend auf dem Wert der Eigenschaft gruppiert sind gewählte. 

Alle Elemente, die den gleichen Wert in der Eigenschaft aufweisen, nach denen gruppiert gewählte werden zusammengefasst werden. Dies möglicherweise offensichtlich, aber es ist eine wichtige Details. Beachten Sie, was geschieht, wenn Sie nach einem Datum/Uhrzeit-Eigenschaft, wie beispielsweise [Item.DateTimeReceived](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx) in die EWS Managed API oder das [DateTimeReceived](http://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx) -Element im EWS gruppieren. Die Absicht möglicherweise die Ergebnisse in Gruppen, mit dem jede Gruppe, die Elemente aus der gleichen Tag zu organisieren. Gruppierung untersucht jedoch den gesamten Wert, der die Zeit enthält. 

Das Ergebnis ist, dass sodass gleichzeitig nach unten zu der zweite empfangenen Elemente in ihren jeweiligen Gruppen sind die Elemente gruppiert werden. Die Ergebnisse werden in den meisten Fällen in eine große Anzahl von Gruppen mit einer kleinen Anzahl von Elementen in den einzelnen Gruppen sortiert. 
  
Wenn Sie eine Resultsets mit einer kleineren Anzahl von Gruppen und eine größere Anzahl von Elementen in den einzelnen Gruppen erhalten möchten, wählen Sie eine Eigenschaft, die wahrscheinlich haben eine kleinere Anzahl von Werten, wie [EmailMessage.From](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx) oder [Item.Categories](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx) in die EWS Managed API oder [aus](http://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx) oder EWS [Kategorien](http://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx) . Die folgende Abbildung zeigt eine Liste der e-Mail-Nachrichten, die angezeigt werden, in einen Ordner Posteingang. 
  
**Abbildung 1. Nachrichten in einen Ordner Posteingang**

![Eine Beispielliste von Nachrichten im Posteingang eines Benutzers.](media/Ex15_GroupedSearch_MsgList.png)
  
Wenn Sie von der **EmailMessage.From** -Eigenschaft der Elemente in Abbildung 1 zu gruppieren, wird das Ergebnis zwei Gruppen, hoffe Brutto gesendeten Nachrichten und Sadie Daniels gesendeten Nachrichten werden. 
  
**Abbildung 2. Nachrichten, die getrennt in Gruppen basierend auf der From-Eigenschaft**

![Abbildung, in der in zwei Listen anhand der Eigenschaft "Von" sortierte Nachrichten gezeigt werden.](media/Ex15_GroupedSearch_SeparateGroups.png)
  
## <a name="sort-the-items-within-groups"></a>Sortieren der Elemente in Gruppen
<a name="bk_SortItems"> </a>

Sie können steuern, wie Elemente in den einzelnen Gruppen mithilfe der [ItemView.OrderBy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) -Eigenschaft in die EWS Managed API oder die [SortOrder](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) -Element im EWS sortiert werden. Die gleichen Reihenfolge gilt für jede Gruppe. Angenommen, wenn Sie die Elemente in Abbildung 1 von der **Item.DateTimeReceived** -Eigenschaft, in absteigender Reihenfolge sortiert das Element zuletzt von hoffe Brutto-empfangen werden in der Gruppe hoffe Brutto erste, und das Element zuletzt von Sadie Daniels empfangen werden der erste in der Gruppe Sadie Daniels. Gruppen in Abbildung 2 sind bequem, bereits auf diese Weise sortiert. 
  
## <a name="sort-the-groups"></a>Sortieren der Gruppen
<a name="bk_SortGroups"> </a>

Nun, da Sie Ihren Gruppen ausgeglichen haben, ist der letzte Schritt die Gruppen selbst sortieren. Da die Gruppen selbst keine bestimmte Werte haben, kann der Gruppierung zuweisen ein Werts sortieren jeder Gruppe. Dies erfolgt durch Aggregation der Werte einer bestimmten Eigenschaft in jeder Gruppe von der [Grouping.AggregateOn](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) -Eigenschaft in die EWS Managed API oder das [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) -Element als untergeordnetes Element des Elements [AggregateOn](http://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) im EWS angegeben. Die [Grouping.AggregateType](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) -Eigenschaft in die EWS Managed API (oder das **aggregieren** der **AggregateOn** -Element im EWS-Attribut) gibt an, welcher Wert aus der Elemente innerhalb jeder Gruppe der Sortierwert für die Gruppe zugewiesen ist, entweder die größten Wert oder den kleinsten Wert. Schließlich wird die Sortierreihenfolge (absteigend oder aufsteigend) von der [Grouping.SortDirection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) -Eigenschaft in die EWS Managed API oder das Attribut **Reihenfolge** der [GroupBy](http://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) -Element im EWS angegeben. 
  
Beispielsweise wenn die Gruppen aus der Abbildung 2 Aggregieren auf die **Item.DateTimeReceived** -Eigenschaft sortiert werden, werden mithilfe des kleinsten Werts und Sortierung in absteigender Reihenfolge die Elemente in Abbildung 3 in der Reihenfolge zurückgegeben. 
  
**Abbildung 3. Gruppierte Suchergebnisse mit den Gruppen sortiert nach der DateTimeReceived-Eigenschaft**

![Abbildung einer sortierten Liste von Nachrichten (gruppiert anhand der Eigenschaft "Von"), in der die Gruppen nach dem jüngsten Empfangsdatum samt Uhrzeit sortiert sind.](media/Ex15_GroupedSearch_Results.png)
  
In den nächsten Abschnitten anzeigen Sie, wie Sie gruppieren und Sortieren zusammen im Code abrufen können.
  
## <a name="example-perform-a-grouped-search-by-using-the-ews-managed-api"></a>Beispiel: Führen Sie eine gruppierte Suche mithilfe der EWS Managed API
<a name="bk_GroupSearchEWSMA"> </a>

Die folgenden EWS Managed API-Methoden können Gruppierung verwenden:
  
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
Das folgende Beispiel verwendet die **ExchangeService.FindItems** -Methode. übernehmen jedoch den gleichen Regeln und Konzepte für die **Folder.FindItems** -Methode. In diesem Beispiel wird eine Methode namens **GroupItemsByFrom** definiert. Es wird ein [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt und ein [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) -Objekt als Parameter. Es fordert die ersten 50 Elemente im Ordner, gruppiert nach der **EmailMessage.From** -Eigenschaft, die von der **Item.DateTimeReceived** -Eigenschaft in absteigender Reihenfolge sortiert. Die Gruppen selbst werden nach der kleinste Wert der **Item.DateTimeReceived** -Eigenschaft auf deren Elemente in absteigender Reihenfolge sortiert. 
  
In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde. 
  
```cs
static void GroupItemsByFrom(ExchangeService service, WellKnownFolderName folder)
{
    // Limit the result set to 50 items.
    ItemView view = new ItemView(50);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.From,
                                       ItemSchema.Categories);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Specify the sorting done within the groups.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    // Configure grouping.
    Grouping groupByFrom = new Grouping();
    groupByFrom.GroupOn = EmailMessageSchema.From;
    groupByFrom.AggregateOn = ItemSchema.DateTimeReceived;
    groupByFrom.AggregateType = AggregateType.Minimum;
    groupByFrom.SortDirection = SortDirection.Descending;
    try
    {
        GroupedFindItemsResults<Item> results = service.FindItems(folder,
            view, groupByFrom);
        foreach (ItemGroup<Item> group in results.ItemGroups)
        {
            Console.WriteLine("Group: {0}", group.GroupIndex);
            foreach (Item item in group.Items)
            {
                if (item is EmailMessage)
                {
                    EmailMessage message = item as EmailMessage;
                    Console.WriteLine("From: {0}", message.From);
                    Console.WriteLine("Subject: {0}", message.Subject);
                    Console.WriteLine("Id: {0}\n", message.Id.ToString());
                }
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="example-perform-a-grouped-search-by-using-ews"></a>Beispiel: Führen Sie eine gruppierte Suche mithilfe der Exchange-Webdienste
<a name="bk_GroupSearchEWS"> </a>

Das folgende anforderungsbeispiel zeigt eine Anforderung [FindItem Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) für die ersten 50 Elemente im Ordner, gruppiert nach dem **aus** -Element, das **DateTimeReceived** -Element in absteigender Reihenfolge sortiert. Die Gruppen selbst werden nach dem kleinsten **DateTimeReceived** Elementwert auf deren Elemente in absteigender Reihenfolge sortiert. 
  
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
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:From" />
          <t:FieldURI FieldURI="item:Categories" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="50" Offset="0" BasePoint="Beginning" />
      <m:GroupBy Order="Descending">
        <t:FieldURI FieldURI="message:From" />
        <t:AggregateOn Aggregate="Minimum">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:AggregateOn>
      </m:GroupBy>
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

Der Server gibt die folgende Antwort zurück.
  
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
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="10" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Groups>
              <t:GroupedItems>
                <t:GroupIndex>0</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Planning resources</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:41:05Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Timeline</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:40:37Z</t:DateTimeReceived>
                    <t:Categories>
                      <t:String>Project</t:String>
                    </t:Categories>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>For your perusal</t:Subject>
                    <t:DateTimeReceived>2013-11-20T21:51:16Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>meeting notes</t:Subject>
                    <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                    <t:Categories>
                      <t:String>Blue category</t:String>
                    </t:Categories>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Meeting notes</t:Subject>
                    <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
              <t:GroupedItems>
                <t:GroupIndex>1</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Query</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:43:15Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Hope Gross</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=9B55E4100C064D9D8C5F72FF36802ED3-HOPE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Update</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:42:33Z</t:DateTimeReceived>
                    <t:Categories>
                      <t:String>Project</t:String>
                      <t:String>Blue category</t:String>
                    </t:Categories>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Hope Gross</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=9B55E4100C064D9D8C5F72FF36802ED3-HOPE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>This cat is hilarious!</t:Subject>
                    <t:DateTimeReceived>2013-10-15T20:22:12Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Hope Gross</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=9B55E4100C064D9D8C5F72FF36802ED3-HOPE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
            </t:Groups>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="version-differences"></a>Versionsunterschiede
<a name="bk_VersionDiffs"> </a>

Versionen von Exchange mit Hauptversion 15 beginnend und endend mit Build 15.0.775.38 return **Gruppe** Elemente (vom Typ **GroupedItemsType**) anstelle von [GroupedItems](http://msdn.microsoft.com/library/53170df4-4272-4b37-b23f-cd8e2d4a7396%28Office.15%29.aspx) Elemente in die SOAP-Antwort. Wenn Sie die EWS Managed API verwenden, bewirkt dies die [GroupedFindItemsResults.ItemGroups](http://msdn.microsoft.com/en-us/library/office/dd633961%28v=exchg.80%29.aspx) -Auflistung, das 0-Objekte enthalten. Wenn Sie Exchange-Webdienste verwenden, sollten **Gruppe** Elemente als **GroupedItems** Elemente behandelt werden. 
  
Versionen von Exchange, beginnend mit Hauptversion 15 werden zusätzliche **Gruppe** oder **GroupedItems** Elemente zurück, mit dem **xsi: nil** -Attribut auf **true fest,** in die SOAP-Antwort festgelegt. Wenn Sie die EWS Managed API verwenden, verursacht diese zusätzlichen Elemente einer [ServiceXmlDeserializationException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.servicexmldeserializationexception%28v=exchg.80%29.aspx) ausgelöst wird. Wenn Sie Exchange-Webdienste verwenden, sollten diese zusätzlichen Elemente ignoriert werden. 
  
## <a name="see-also"></a>Siehe auch

- [Suche und EWS in Exchange](search-and-ews-in-exchange.md)    
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)   
- [Gruppierung-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.grouping%28v=exchg.80%29.aspx)    
- [FindItem-Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

