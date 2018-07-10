---
title: Synchronisieren von Elementen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 886e7d35-9096-480b-8a8c-a7db27da06c2
description: Erfahren Sie, wie Sie verwenden die EWS Managed API oder EWS zum Abrufen einer Liste aller Elemente in einem Ordner oder eine Liste der Änderungen, die aufgetreten sind in einem Ordner, um den Client synchronisieren.
ms.openlocfilehash: ce29a77cee595c2358441e4a22d32d45e78c6e60
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757002"
---
# <a name="synchronize-items-by-using-ews-in-exchange"></a><span data-ttu-id="25444-103">Synchronisieren von Elementen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="25444-103">Synchronize items by using EWS in Exchange</span></span>

<span data-ttu-id="25444-104">Erfahren Sie, wie Sie verwenden die EWS Managed API oder EWS zum Abrufen einer Liste aller Elemente in einem Ordner oder eine Liste der Änderungen, die aufgetreten sind in einem Ordner, um den Client synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="25444-104">Find out how to use the EWS Managed API or EWS to get a list of all items in a folder, or a list of changes that have occurred in a folder, in order to synchronize your client.</span></span>
  
<span data-ttu-id="25444-105">EWS in Exchange verwendet Element Synchronisierung und Ordner der Synchronisierung der Inhalt von Postfächern Synchronisierung zwischen dem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="25444-105">EWS in Exchange uses item synchronization and folder synchronization to sync mailbox content between the client and server.</span></span> <span data-ttu-id="25444-106">Element-Synchronisierung Ruft die ursprüngliche Liste der Elemente in einem Ordner und ruft dann im Laufe der Zeit Änderungen, die mit diesen Elementen erfolgt ist und neue Elemente ebenfalls Ruft ab.</span><span class="sxs-lookup"><span data-stu-id="25444-106">Item synchronization gets the initial list of items in a folder and then, over time, gets changes that have been made to those items and gets new items as well.</span></span>
  
<span data-ttu-id="25444-107">Beachten Sie, bevor Sie die Elemente an einen Client synchronisieren können, Sie zuerst auf [Synchronisieren der Ordnerhierarchie](how-to-synchronize-folders-by-using-ews-in-exchange.md)verfügen.</span><span class="sxs-lookup"><span data-stu-id="25444-107">Note that before you can sync items to a client, you first have to [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="25444-108">Nach dem Ordner ist Hierarchie direkt auf dem Client, wenn Sie mithilfe der EWS Managed API, Sie zuerst [die ursprüngliche Liste der Elemente im Posteingang erhalten möchten](#bk_cesyncongoingewsma) , mithilfe der Methode [ExchangeService.SyncFolderItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) Element Synchronisierung durchführen.</span><span class="sxs-lookup"><span data-stu-id="25444-108">After the folder hierarchy is in place on the client, if you're performing item synchronization by using the EWS Managed API, you first [get the initial list of items in the Inbox](#bk_cesyncongoingewsma) by using the [ExchangeService.SyncFolderItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="25444-109">Dann aktualisieren Sie den Wert des Parameters _cSyncState_ bei nachfolgenden Aufrufen, um die Liste der geänderten Elemente im Posteingang abzurufen.</span><span class="sxs-lookup"><span data-stu-id="25444-109">You then update the value of the  _cSyncState_ parameter during subsequent calls to get the list of changed items in the Inbox.</span></span> 
  
<span data-ttu-id="25444-110">Zum Element Synchronisierung ausführen nach [Synchronisieren der Ordnerhierarchie](how-to-synchronize-folders-by-using-ews-in-exchange.md)mithilfe eines EWS, fordern Sie die [ursprüngliche Liste der Elemente im Posteingang](#bk_ewsexamplea) mit der [SyncFolderItems-Vorgang](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx), analysieren die Antwort, und zeigen Sie einige in der Zukunft [ Abrufen die Änderungen auf die Elemente im Postfach](#bk_ewsexamplec), und die Antwort zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="25444-110">To perform item synchronization by using EWS, after you [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md), you request the [initial list of items in the Inbox](#bk_ewsexamplea) by using the [SyncFolderItems operation](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx), parse the response, and then at some point in the future [get the changes to the items in the mailbox](#bk_ewsexamplec), and parse the response.</span></span> <span data-ttu-id="25444-111">Nachdem der Client die Liste der anfänglichen oder geänderte Elemente empfangen sie [Updates lokal macht](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="25444-111">After the client receives the list of initial or changed items, it [makes updates locally](#bk_nextsteps).</span></span> <span data-ttu-id="25444-112">Wie und wann Sie Änderungen in der Zukunft abrufen, hängt von der [Synchronisierung Entwurfsmuster](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) , Ihre Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="25444-112">How and when you retrieve changes in the future depends on the [synchronization design pattern](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) your application is using.</span></span> 
  
## <a name="get-the-list-of-all-items-or-changed-items-by-using-the-ews-managed-api"></a><span data-ttu-id="25444-113">Abrufen Sie die Liste aller Elemente oder geänderte Elemente, indem Sie die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="25444-113">Get the list of all items or changed items by using the EWS Managed API</span></span>
<span data-ttu-id="25444-114"><a name="bk_cesyncongoingewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="25444-114"></span></span>

<span data-ttu-id="25444-115">Im folgenden Codebeispiel wird veranschaulicht, wie auf eine anfängliche Liste aller Elemente im Ordner Posteingang rufen und anschließend eine Liste der Änderungen auf Elemente im Ordner Posteingang, die seit der vorherigen Synchronisierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="25444-115">The following code example shows how to get an initial list of all items in the Inbox folder and then get a list of changes to items in the Inbox folder that have occurred since the previous synchronization.</span></span> <span data-ttu-id="25444-116">Während der anfänglichen Aufruf der [SyncFolderItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) -Methode den _cSyncState_ -Wert auf null festgelegt.</span><span class="sxs-lookup"><span data-stu-id="25444-116">During the initial call to the [SyncFolderItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) method, set the  _cSyncState_ value to null.</span></span> <span data-ttu-id="25444-117">Wenn die Methode abgeschlossen ist, speichern Sie den _cSyncState_ Wert lokal für den nächsten Aufruf der **SyncFolderItems** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="25444-117">When the method completes, save the  _cSyncState_ value locally to use in the next **SyncFolderItems** method call.</span></span> <span data-ttu-id="25444-118">In der ersten Aufruf und die nachfolgenden Aufrufen werden die Elemente in Batches von zehn mithilfe von aufeinander folgenden Aufrufen der Methode **SyncFolderItems** bis keine weitere Änderungen bleiben abgerufen.</span><span class="sxs-lookup"><span data-stu-id="25444-118">In both the initial call and the subsequent calls, the items are retrieved in batches of ten, by using successive calls to the **SyncFolderItems** method, until no more changes remain.</span></span> 
  
<span data-ttu-id="25444-119">In diesem Beispiel wird den Parameter _PropertySet_ IdOnly um Anrufe an die Exchange-Datenbank eine [bewährte Methode Synchronisierung ist](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)reduzieren.</span><span class="sxs-lookup"><span data-stu-id="25444-119">This example sets the  _propertySet_ parameter to IdOnly to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="25444-120">In diesem Beispiel wird davon ausgegangen, dass **-Dienst** eine gültige **ExchangeService** Objekt Bindung ist und diese _cSyncState_ stellt den Synchronisierungsstatus an, der von einem vorherigen Aufruf von **SyncFolderItems**zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="25444-120">In this example, we assume that **service** is a valid **ExchangeService** object binding and that  _cSyncState_ represents the sync state that was returned by a prior call to **SyncFolderItems**.</span></span> 
  
```cs
// Track whether there are more items available for download on the server.
bool moreChangesAvailable = false;
do
{
    // Get a list of all items in the Inbox by calling SyncFolderHierarchy repeatedly until no more changes are available.
    // The folderId parameter must be set to the root folder to synchronize,
    // and must be same folder ID as used in previous synchronization calls. 
    // The propertySet parameter is set to IdOnly to reduce calls to the Exchange database,
    // because any additional properties result in additional calls to the Exchange database. 
    // The ignoredItemIds parameter is set to null, so that no items are ignored.
    // The maxChangesReturned parameter is set to return a maximum of 10 items (512 is the maximum).
    // The syncScope parameter is set to Normal items, so that associated items will not be returned.
    // The syncState parameter is set to cSyncState, which should be null in the initial call, 
    // and should be set to the sync state returned by the 
    // previous SyncFolderItems call in subsequent calls.
    ChangeCollection<ItemChange> icc = service.SyncFolderItems(new FolderId(WellKnownFolderName.Inbox), PropertySet.IdOnly, null, 10, SyncFolderItemsScope.NormalItems, cSyncState);
    // If the count of changes is zero, there are no changes to synchronize.
    if (icc.Count == 0)
    {
        Console.WriteLine("There are no item changes to synchronize.");
    }
    // Otherwise, write all the changes included in the response 
    // to the console. 
    else
    {
        foreach (ItemChange ic in icc)
        {
            Console.WriteLine("ChangeType: " + ic.ChangeType.ToString());
            Console.WriteLine("ItemId: " + ic.ItemId);
            Console.WriteLine("===========");
        }
    }
    // Save the sync state for use in future SyncFolderContent requests.
    // The sync state is used by the server to determine what changes to report
    // to the client.
    string sSyncState = icc.SyncState;
   // Determine whether more changes are available on the server.
   moreChangesAvailable = icc.MoreChangesAvailable;
}
while (moreChangesAvailable);

```

Die **SyncFolderItems** -Methode ähnelt der [FindItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methode, dass es Eigenschaften wie [Nachrichtentext](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) oder [Anlagen](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx)zurückgeben kann. <span data-ttu-id="25444-122">Wenn Sie Eigenschaften, die von der **SyncFolderItems** -Methode zurückgegeben werden kann benötigen, geben Sie die [IdOnly](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.propertyset.idonly%28v=exchg.80%29.aspx) -Eigenschaft festlegen, wenn Sie **SyncFolderItems**aufrufen, und klicken Sie dann die [ExchangeService.LoadPropertiesForItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) -Methode zum Abrufen der Eigenschaften müssen Sie für die Elemente, die von der **SyncFolderItems** -Methode zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="25444-122">If you need properties that cannot be returned by the **SyncFolderItems** method, specify the [IdOnly](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.propertyset.idonly%28v=exchg.80%29.aspx) property set when you call **SyncFolderItems**, and then use the [ExchangeService.LoadPropertiesForItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) method to get the properties you require for the items that were returned by the **SyncFolderItems** method.</span></span> 
  
<span data-ttu-id="25444-123">Rufen Sie nachdem die Liste der neue oder geänderte Elemente auf dem Server, [Erstellen oder aktualisieren die Elemente auf dem Client ab](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="25444-123">After you retrieve the list of new or changed items on the server, [create or update the items on the client](#bk_nextsteps).</span></span>
  
## <a name="get-the-initial-list-of-items-by-using-ews"></a><span data-ttu-id="25444-124">Möchten Sie die ursprüngliche Liste der Elemente mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="25444-124">Get the initial list of items by using EWS</span></span>
<span data-ttu-id="25444-125"><a name="bk_ewsexamplea"> </a></span><span class="sxs-lookup"><span data-stu-id="25444-125"></span></span>

<span data-ttu-id="25444-126">Das folgende Beispiel zeigt die XML-Anforderung an die ursprüngliche Liste der Elemente im Posteingang abgerufen, mit der [SyncFolderItems-Vorgang](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="25444-126">The following example shows the XML request to get the initial list of items in the Inbox by using the [SyncFolderItems operation](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx).</span></span> <span data-ttu-id="25444-127">Dies ist auch, dass die EWS Managed API, wenn gesendet die XML-Anfrage [beim Abrufen der Liste von Elementen mithilfe der SyncFolderItems-Methode](#bk_cesyncongoingewsma).</span><span class="sxs-lookup"><span data-stu-id="25444-127">This is also the XML request that the EWS Managed API sends when [retrieving the list of items by using the SyncFolderItems method](#bk_cesyncongoingewsma).</span></span> <span data-ttu-id="25444-128">Das Element [Synchronisierungsstatus](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) des Vorgangs **SyncFolderItems** ist nicht mit inbegriffen, da dies die anfängliche Synchronisierung ist.</span><span class="sxs-lookup"><span data-stu-id="25444-128">The [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element of the **SyncFolderItems** operation is not included because this is the initial synchronization.</span></span> <span data-ttu-id="25444-129">In diesem Beispiel wird das Element [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) **IdOnly** um Anrufe an die Exchange-Datenbank eine [bewährte Methode Synchronisierung ist](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)reduzieren.</span><span class="sxs-lookup"><span data-stu-id="25444-129">This example sets the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span>
  
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
    <m:SyncFolderItems>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:ItemShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:SyncFolderId>
      <m:MaxChangesReturned>10</m:MaxChangesReturned>
      <m:SyncScope>NormalItems</m:SyncScope>
    </m:SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="25444-130">Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die **SyncFolderItems** Vorgang Anforderung vom Client verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="25444-130">The following example shows the XML response that is returned by the server after it processes the **SyncFolderItems** operation request from the client.</span></span> <span data-ttu-id="25444-131">Die erste Antwort enthält [Erstellen](http://msdn.microsoft.com/library/cb5e64a2-66a5-4447-921e-7c13efb8f6bf%28Office.15%29.aspx) von Elementen für fünf Elemente, da alle Elemente neu während einer anfänglichen Synchronisierung gelten.</span><span class="sxs-lookup"><span data-stu-id="25444-131">The initial response includes [Create](http://msdn.microsoft.com/library/cb5e64a2-66a5-4447-921e-7c13efb8f6bf%28Office.15%29.aspx) elements for five items because all items are considered new during an initial synchronization.</span></span> <span data-ttu-id="25444-132">Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt, und einige Ordner wurden aus Platzgründen nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="25444-132">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA==</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q04QAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdC"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q07AAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdB"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q1AwAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdA"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AAMkADBh=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVc5"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AAMkADBh=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVc4"/>
              </t:Message>
            </t:Create>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderItemsResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="25444-133">Rufen Sie nach der die Liste der neuen Elemente auf dem Server, [die Elemente auf dem Client erstellen](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="25444-133">After you retrieve the list of new items on the server, [create the items on the client](#bk_nextsteps).</span></span>
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a><span data-ttu-id="25444-134">Abrufen von Änderungen seit der letzten Synchronisierung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="25444-134">Get the changes since the last sync by using EWS</span></span>
<span data-ttu-id="25444-135"><a name="bk_ewsexamplec"> </a></span><span class="sxs-lookup"><span data-stu-id="25444-135"></span></span>

<span data-ttu-id="25444-136">Das folgende Beispiel zeigt die XML-Anforderung an die Liste der Änderungen auf Elemente im Posteingang abrufen, indem Sie den Vorgang [SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="25444-136">The following example shows the XML request to get the list of changes to items in the Inbox by using the [SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="25444-137">Dies ist auch, dass die EWS Managed API, wenn gesendet die XML-Anfrage [Abrufen der Liste der Änderungen an den Posteingang](#bk_cesyncongoingewsma).</span><span class="sxs-lookup"><span data-stu-id="25444-137">This is also the XML request that the EWS Managed API sends when [retrieving the list of changes to the Inbox](#bk_cesyncongoingewsma).</span></span> <span data-ttu-id="25444-138">In diesem Beispiel wird den [Synchronisierungsstatus](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) Elementwert auf den Wert in der [vorherigen Antwort](http://msdn.microsoft.com/library/886e7d35-9096-480b-8a8c-a7db27da06c2bk_ewsexamplea%28Office.15%29.aspx)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="25444-138">This example sets the [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element value to the value returned in the [previous response](http://msdn.microsoft.com/library/886e7d35-9096-480b-8a8c-a7db27da06c2bk_ewsexamplea%28Office.15%29.aspx).</span></span> <span data-ttu-id="25444-139">Und zur Veranschaulichung in diesem Beispiel wird das Element [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) **AllProperties** anstelle von **IdOnly** zum Anzeigen der zusätzlichen Eigenschaften zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="25444-139">And for demonstration purposes, this example sets the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **AllProperties** instead of **IdOnly** to show the additional properties returned.</span></span> <span data-ttu-id="25444-140">Festlegen der [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Elements auf **IdOnly** ist eine [bewährte Methode Synchronisierung](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span><span class="sxs-lookup"><span data-stu-id="25444-140">Setting the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="25444-141">Der Wert der **Synchronisierungsstatus** wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="25444-141">The value of **SyncState** has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
      <t:RequestServerVersion Version="Exchange2010_SP2" />
  </soap:Header>
  <soap:Body>
    <m:SyncFolderItems>
      <m:ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:ItemShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:SyncFolderId>
      <m:SyncState>H4sIAAA==</m:SyncState>
      <m:MaxChangesReturned>10</m:MaxChangesReturned>
      <m:SyncScope>NormalItems</m:SyncScope>
    </m:SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="25444-142">Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die **SyncFolderItems** Vorgang Anforderung vom Client verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="25444-142">The following example shows the XML response that is returned by the server after it processes the **SyncFolderItems** operation request from the client.</span></span> <span data-ttu-id="25444-143">Diese Antwort gibt an, dass ein Element aktualisiert wurde, wurden zwei Elemente erstellt, das Lese-Flag eines Elements geändert wurde und ein Element wurde seit der vorherigen Synchronisierung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="25444-143">This response indicates that one item was updated, two items were created, the read flag of one item was changed, and one item was deleted since the prior synchronization.</span></span> <span data-ttu-id="25444-144">Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt, und einige Ordner wurden aus Platzgründen nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="25444-144">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3"
                 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                 xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAAAAAAEAO29B2AcSZY==</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Update>
                <t:Message>
                  <t:ItemId Id="q04QAAAA==" ChangeKey="CQAAABYAAADZGACZQpSgSpyNkexYe2b7AAAAird/" />
                  <t:ParentFolderId Id=" AgENAAAA" ChangeKey="AQAAAA==" />
                  <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Company Soccer Team</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T15:22:10Z</t:DateTimeReceived>
                  <t:Size>23110</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;8e084ea1a5b64f97b95fa8a863a5869d@CH1SR01MB001.namsdf01.sdf.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T15:22:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:38Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>All Employees</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara  Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T16:53:35Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQACAi+NTh0F5Eg5YDwpJsXPE=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Alfred  Welker </t:Name>
                      <t:EmailAddress>Alfred.Welker@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5V/ZICL41OHQXkSDlgPCkmxc8ZYxA3I4gAAP5UeAANHpbIAAEE+0gAABYhSAACGYTIAAA2+vgAAE81qAkhv0Eg==</t:ConversationIndex>
                  <t:ConversationTopic>Company Soccer Team</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Alfred  Welker </t:Name>
                      <t:EmailAddress>Alfred.Welker@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;e5919a09c8fc4d64b6ffd3542e194fc3@BY2SR01MB609.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>namsdf01.sdf.contoso.com&amp;gt;</t:References>
                </t:Message>
            </t:Update>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AQMkAD+" />
                <t:ParentFolderId Id="AQMkA==" ChangeKey="AQAAAA==" />
                <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Review Proposal for Contoso</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T16:20:10Z</t:DateTimeReceived>
                  <t:Size>32515</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;e52a4de6b98d484887e141da094a2ce6@SN2SR01MB006.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T16:20:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:33Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>Legal Team; Executives</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara  Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T04:07:35Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQAIsBEZp25UpElByLLUQFH6Q=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Hope Gross</t:Name>
                      <t:EmailAddress>Hope.Gross@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5WBRiwERmnblSkSUHIstRAUfpJYw9fbSgAAAdm2AAAB6koAAAHTDgAADl6+AAAbxCYAABm5PgAACSA+AANx034AAEKGQgAAAfsiAAB7m3IAABG+ngAABPZyAAASUzoAAA2DNgAAAfKE=</t:ConversationIndex>
                  <t:ConversationTopic>Review Proposal for Contoso</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Hope Gross</t:Name>
                      <t:EmailAddress>Hope.Gross@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;bcdb185495834370a874a1e7ebedbb96@SN2SR01MB005.namsdf01.sdf.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>&amp;lt;2d4d7d…</t:References>
                </t:Message>
              </t:Create>
              <t:Create>
                <t:Message>
                  <t:ItemId Id="Q04AAAAA==" ChangeKey="AAAirbnd" />
                  <t:ParentFolderId Id="AgENAAAA" ChangeKey="AQAAAA==" />
                  <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Review Proposal for Contoso</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T15:30:10Z</t:DateTimeReceived>
                  <t:Size>29518</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;f0db3ead01db4fe087d98022149aa16f@SN2SR01MB001.namsdf01.sdf.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T15:30:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:36Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>Legal Team; Executives</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T04:07:38Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQAIsBEZp25UpElByLLUQFH6Q=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Mack Chaves</t:Name>
                      <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5WBRiwERmnblSkSUHIstRAUfpJYw9fbSgAAAdm2AAAB6koAAAHTDgAADl6+AAAbxCYAABm5PgAACSA+AANx034AAEKGQgAAAfsiAAB7m3IAABG+ngAABPZyAAASUzoAAA2DN</t:ConversationIndex>
                  <t:ConversationTopic>Review Proposal for Contoso</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Mack Chaves</t:Name>
                      <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;e52a4de6b98d484887e141da094a2ce6@SN2SR01MB006.namsdf01.sdf.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>namsdf01.sdf.contoso.com&amp;gt;</t:References>
                </t:Message>
              </t:Create>
              <t:ReadFlagChange>
                <t:ItemId Id=" q07AAAAA==" ChangeKey="CQAAAA==" />
                <t:IsRead>true</t:IsRead>
              </t:ReadFlagChange>
              <t:Delete>
                <t:ItemId Id=" q1AwAAAA==" ChangeKey="CQAAAA==" />
              </t:Delete>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderItemsResponse>
  </s:Body>
</s:Envelope>
```

Der Vorgang **SyncFolderItems** ähnelt der [FindItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methode, dass sie Elemente wie die [Nachrichtentext](http://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) oder [Anlagen](http://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) Elemente zurückgeben kann. <span data-ttu-id="25444-146">Wenn Sie Eigenschaften, die von der Operation **SyncFolderItems** zurückgegeben werden kann benötigen, legen Sie den Wert des [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Elements auf IdOnly beim Aufrufen von **SyncFolderItems**, und klicken Sie dann den [GetItem Operation](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) verwenden, um die Eigenschaften abzurufen Sie erforderlich für die Elemente, die von der Operation **SyncFolderItems** zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="25444-146">If you need properties that cannot be returned by the **SyncFolderItems** operation, set the value of the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to IdOnly when you call **SyncFolderItems**, and then use the [GetItem operation](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) to get the properties you require for the items that were returned by the **SyncFolderItems** operation.</span></span> 
  
<span data-ttu-id="25444-147">Abgerufen Sie nachdem die Liste der geänderte Elemente auf dem Server, [die Elemente auf dem Client aktualisieren](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="25444-147">After you retrieve the list of changed items on the server, [update the items on the client](#bk_nextsteps).</span></span>
  
## <a name="update-the-client"></a><span data-ttu-id="25444-148">Aktualisieren des Clients</span><span class="sxs-lookup"><span data-stu-id="25444-148">Update the client</span></span>
<span data-ttu-id="25444-149"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="25444-149"></span></span>

<span data-ttu-id="25444-150">Wenn Sie die EWS Managed API verwenden, nachdem Sie die Liste der neuen oder geänderten Elemente erhalten möchten, verwenden Sie die [LoadPropertiesForItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) -Methode zum Abrufen von Eigenschaften für die neue oder geänderte Elemente, die Eigenschaften auf die lokalen Werte vergleichen und aktualisieren die Elemente auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="25444-150">If you're using the EWS Managed API, after you get the list of new or changed items, use the [LoadPropertiesForItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) method to get properties on the new or changed items, compare the properties to the local values, and update the items on the client.</span></span> 
  
<span data-ttu-id="25444-151">Wenn Sie Exchange-Webdienste verwenden, verwenden Sie die [GetItem Operation](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) zum Abrufen von Eigenschaften für die neue oder geänderte Elemente und aktualisieren die Elemente auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="25444-151">If you're using EWS, use the [GetItem operation](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) to get properties on the new or changed items and update the items on the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25444-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25444-152">See also</span></span>


- [<span data-ttu-id="25444-153">Postfachsynchronisierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="25444-153">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    
- [<span data-ttu-id="25444-154">Synchronisieren von Ordnern in Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="25444-154">Synchronize folders by using EWS in Exchange</span></span>](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="25444-155">Fehlerbehandlung Synchronisierung-bezogene in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="25444-155">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="25444-156">Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="25444-156">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    

