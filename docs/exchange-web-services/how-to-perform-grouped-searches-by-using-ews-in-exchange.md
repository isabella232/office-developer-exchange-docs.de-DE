---
title: Durchführen gruppierter Suchen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 55de92eb-8e8b-4156-8ad9-dd3828024242
description: Erfahren Sie, wie Sie gruppierte Suchvorgänge in ihrer verwaltete EWS-API-oder EWS-Anwendung durchführen, die auf Exchange abzielt.
ms.openlocfilehash: 65c6f75ea6b8ab848a263349dcceceead52fa210
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527930"
---
# <a name="perform-grouped-searches-by-using-ews-in-exchange"></a>Durchführen gruppierter Suchen mithilfe von EWS in Exchange

Erfahren Sie, wie Sie gruppierte Suchvorgänge in ihrer verwaltete EWS-API-oder EWS-Anwendung durchführen, die auf Exchange abzielt.
  
Gruppierte Suchvorgänge sind hilfreich, da Sie Ihnen die Kontrolle darüber geben, wie Suchergebnisse organisiert werden. Organisierte Suchergebnisse können es Ihrer Anwendung erleichtern, Ergebnisse zu verarbeiten oder Sie auf eine verwaltbare Weise an einen Endbenutzer anzuzeigen.
  
Die Gruppierung funktioniert, indem alle Elemente innerhalb des Resultsets mit dem gleichen Wert eines bestimmten Felds in einer Gruppe eingefügt werden. Beispielsweise können Sie Ihre Ergebnisse nach dem Absender gruppieren, und alle Elemente derselben Person befinden sich in einer separaten Gruppe, und die Elemente innerhalb jeder Gruppe werden entsprechend der in der Ansicht angegebenen Reihenfolge sortiert. Die Gruppen selbst werden nach einem aggregierten Wert basierend auf einem von Ihnen ausgewählten Feld sortiert.
  
**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge zum Organisieren von Suchergebnissen**

|**Aktion**|**Verwenden Sie im verwaltete EWS-API die...**|**Verwenden Sie in EWS die...**|
|:-----|:-----|:-----|
|Organisieren von Elementen mit dem gleichen Wert in einer bestimmten Eigenschaft in ihren Ergebnissen in Gruppen  <br/> |[GROUPING. GroupOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.groupon%28v=exchg.80%29.aspx) <br/> |[FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) -Element als untergeordnetes Element des [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) -Elements  <br/> |
|Sortieren von Elementen innerhalb jeder Gruppe nach dem Wert in einer bestimmten Eigenschaft  <br/> |[ItemView. OrderBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) <br/> |[Sortierreihenfolge](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) -Element  <br/> |
|Sortieren der Gruppen  <br/> |[GROUPING. AggregateOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) <br/><br/> [GROUPING. aggregattype](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) <br/><br/> [GROUPING. SortDirection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) <br/> |**FieldURI** -Element als untergeordnetes Element des [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) -Elements<br/><br/> **Aggregate** -Attribut für das **AggregateOn** -Element<br/><br/>**Order** -Attribut für das **GroupBy** -Element  <br/> |
   
Lassen Sie uns Schritt für Schritt vorgehen.
  
## <a name="group-results-by-a-specific-property"></a>Gruppieren von Ergebnissen nach einer bestimmten Eigenschaft
<a name="bk_GroupResults"> </a>

Der erste Schritt bei der Verwendung von Gruppierungen besteht darin, eine Eigenschaft oder ein Attribut für die Elemente im Exchange-Informationsspeicher auszuwählen, um nach Group by zu gruppieren. Das verwaltete EWS-API macht diese als Klassen Eigenschaften für die entsprechenden Klassen verfügbar, während EWS Sie als XML-Elemente verfügbar macht. Sie können eine beliebige Eigenschaft, einschließlich benutzerdefinierter oder erweiterter Eigenschaften, auswählen, es ist jedoch hilfreich zu verstehen, wie Elemente basierend auf dem Wert der ausgewählten Eigenschaft gruppiert werden. 

Alle Elemente mit dem gleichen Wert in der Eigenschaft, die Sie für die Gruppierung auswählen, werden zusammen gruppiert. Dies scheint zwar offensichtlich zu sein, es handelt sich jedoch um ein wichtiges Detail. Stellen Sie sich vor, was passiert, wenn Sie nach einer Date/Time-Eigenschaft gruppieren, wie beispielsweise [Item. DateTimeReceived](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx) im verwaltete EWS-API oder das [DateTimeReceived](https://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx) -Element in EWS. Die Absicht besteht darin, die Ergebnisse in Gruppen zu organisieren, wobei jede Gruppe Elemente vom selben Tag enthält. Bei der Gruppierung wird jedoch der gesamte Wert untersucht, der die Uhrzeit enthält. 

Das Endergebnis ist, dass die Elemente so gruppiert werden, dass Elemente, die gleichzeitig empfangen werden, bis zum zweiten, in ihren eigenen Gruppen liegen. Die Ergebnisse werden höchstwahrscheinlich in eine große Anzahl von Gruppen mit einer kleinen Anzahl von Elementen in jeder Gruppe sortiert. 
  
Wenn Sie ein Resultset mit einer kleineren Anzahl von Gruppen und einer größeren Anzahl von Elementen in jeder Gruppe abrufen möchten, wählen Sie eine Eigenschaft aus, bei der es sich wahrscheinlich um eine geringere Anzahl von Werten wie [Email Message. from](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx) oder [Item. categories](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx) im verwaltete EWS-API [From](https://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx) oder aus [Kategorien](https://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx) in EWS handelt. Die folgende Abbildung zeigt eine Liste von e-Mails, die in einem Posteingang angezeigt werden. 
  
**Abbildung 1. Nachrichten in einem Posteingang**

![Eine Beispielliste von Nachrichten im Posteingang eines Benutzers.](media/Ex15_GroupedSearch_MsgList.png)
  
Wenn Sie die Elemente in Abbildung 1 durch die **Email Message. from** -Eigenschaft gruppieren, werden zwei Gruppen angezeigt: eine für Nachrichten, die von Hope Brutto gesendet wurden, und eine für Nachrichten, die von Sadie Daniels gesendet wurden. 
  
**Abbildung 2. Nachrichten, die basierend auf der From-Eigenschaft in Gruppen unterteilt sind**

![Abbildung, in der in zwei Listen anhand der Eigenschaft "Von" sortierte Nachrichten gezeigt werden.](media/Ex15_GroupedSearch_SeparateGroups.png)
  
## <a name="sort-the-items-within-groups"></a>Sortieren der Elemente in Gruppen
<a name="bk_SortItems"> </a>

Sie können steuern, wie Elemente innerhalb jeder Gruppe sortiert werden, indem Sie die [ItemView. OrderBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) -Eigenschaft in der verwaltete EWS-API oder das Element " [Sortierreihenfolge](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) " in EWS verwenden. Die gleiche Reihenfolge gilt für jede Gruppe. Wenn Sie beispielsweise die Elemente aus Abbildung 1 nach der **Item. DateTimeReceived** -Eigenschaft in absteigender Reihenfolge sortieren, wird das Element, das zuletzt von Hope Brutto empfangen wurde, zuerst in der Hope-Brutto Gruppe angezeigt, und das Element, das zuletzt von Sadie Daniels empfangen wurde, wird zuerst in der Sadie Daniels-Gruppe sein. Bequem sind die Gruppen in Abbildung 2 bereits auf diese Weise sortiert. 
  
## <a name="sort-the-groups"></a>Sortieren der Gruppen
<a name="bk_SortGroups"> </a>

Nachdem Sie Ihre Gruppen abgewickelt haben, besteht der letzte Schritt darin, die Gruppen selbst zu sortieren. Da die Gruppen selbst keine spezifischen Werte haben, muss der Gruppierungs Prozess jeder Gruppe einen Sortierwert zuweisen. Dies erfolgt durch Aggregation der Werte einer bestimmten Eigenschaft innerhalb jeder Gruppe, die durch die [Grouping. AggregateOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) -Eigenschaft in der verwaltete EWS-API oder das [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) -Element als untergeordnetes Element des [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) -Elements in EWS angegeben wird. Die [Grouping. aggregattype](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) -Eigenschaft in der verwaltete EWS-API (oder das **Aggregate** -Attribut für das **AggregateOn** -Element in EWS) gibt an, welcher Wert aus den Elementen innerhalb jeder Gruppe dem Sortierwert für die Gruppe zugewiesen ist, entweder den größten oder den kleinsten Wert. Schließlich wird die Sortierreihenfolge (absteigend oder aufsteigend) durch die [Grouping. SortDirection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) -Eigenschaft im verwaltete EWS-API oder das **Order** -Attribut für das [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) -Element in EWS angegeben. 
  
Wenn beispielsweise die Gruppen aus Abbildung 2 durch Aggregieren der **Item. DateTimeReceived** -Eigenschaft sortiert werden, wobei der kleinste Wert verwendet wird und die Sortierung in absteigender Reihenfolge erfolgt, werden die Elemente in der angegebenen Reihenfolge in Abbildung 3 zurückgegeben. 
  
**Abbildung 3. Gruppierte Suchergebnisse mit den Gruppen, sortiert nach der DateTimeReceived-Eigenschaft**

![Abbildung einer sortierten Liste von Nachrichten (gruppiert anhand der Eigenschaft "Von"), in der die Gruppen nach dem jüngsten Empfangsdatum samt Uhrzeit sortiert sind.](media/Ex15_GroupedSearch_Results.png)
  
In den nächsten Abschnitten erfahren Sie, wie Sie die Gruppierung und Sortierung in Code zusammenführen können.
  
## <a name="example-perform-a-grouped-search-by-using-the-ews-managed-api"></a>Beispiel: Durchführen einer gruppierten Suche mithilfe der verwaltete EWS-API
<a name="bk_GroupSearchEWSMA"> </a>

Die folgenden verwaltete EWS-API Methoden können die Gruppierung verwenden:
  
- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
Im folgenden Beispiel wird die **Datei "ExchangeService. FindItems** -Methode verwendet; die gleichen Regeln und Konzepte gelten jedoch für die **Folder. FindItems** -Methode. In diesem Beispiel wird eine Methode namens " **GroupItemsByFrom** " definiert. Es akzeptiert ein [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt und ein [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) -Objekt als Parameter. Die ersten 50-Elemente in dem Ordner werden angefordert, gruppiert nach der **Email Message. from** -Eigenschaft, sortiert nach der **Item. DateTimeReceived** -Eigenschaft in absteigender Reihenfolge. Die Gruppen selbst werden nach dem kleinsten **Item. DateTimeReceived** -Eigenschaftswert für ihre Elemente in absteigender Reihenfolge sortiert. 
  
In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde. 
  
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

## <a name="example-perform-a-grouped-search-by-using-ews"></a>Beispiel: Ausführen einer gruppierten Suche mithilfe von EWS
<a name="bk_GroupSearchEWS"> </a>

Das folgende Anforderungs Beispiel zeigt eine [FindItem-Vorgangs](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) Anforderung für die ersten 50-Elemente im Ordner, gruppiert nach dem **from** -Element, sortiert nach dem **DateTimeReceived** -Element in absteigender Reihenfolge. Die Gruppen selbst werden nach dem kleinsten **DateTimeReceived** -Elementwert für ihre Elemente in absteigender Reihenfolge sortiert. 
  
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

Versionen von Exchange, die mit der Hauptversion 15 beginnen und mit Build 15.0.775.38 zurückgegeben werden, geben **Gruppen** Elemente (vom Typ **GroupedItemsType**) anstelle von [GroupedItems](https://msdn.microsoft.com/library/53170df4-4272-4b37-b23f-cd8e2d4a7396%28Office.15%29.aspx) -Elementen in der SOAP-Antwort zurück. Wenn Sie die verwaltete EWS-API verwenden, führt dies dazu, dass die [GroupedFindItemsResults. ItemGroups](https://msdn.microsoft.com/library/office/dd633961%28v=exchg.80%29.aspx) -Auflistung 0-Objekte enthält. Wenn Sie EWS verwenden, sollten **Group** -Elemente als **GroupedItems** -Elemente behandelt werden. 
  
Versionen von Exchange, die mit der Hauptversion 15 beginnen, geben zusätzliche **Group** -oder **GroupedItems** -Elemente zurück, wobei das **xsi: Nil** -Attribut in der SOAP-Antwort auf **true** festgelegt ist. Wenn Sie die verwaltete EWS-API verwenden, führen diese zusätzlichen Elemente dazu, dass ein [ServiceXmlDeserializationException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.servicexmldeserializationexception%28v=exchg.80%29.aspx) -Objekt ausgelöst wird. Wenn Sie EWS verwenden, sollten diese zusätzlichen Elemente ignoriert werden. 
  
## <a name="see-also"></a>Siehe auch

- [Suche und EWS in Exchange](search-and-ews-in-exchange.md)    
- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)   
- [GROUPING-Klasse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping%28v=exchg.80%29.aspx)    
- [FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

