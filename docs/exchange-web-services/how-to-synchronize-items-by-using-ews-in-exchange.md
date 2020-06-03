---
title: Synchronisieren von Elementen unter Verwendung von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 886e7d35-9096-480b-8a8c-a7db27da06c2
description: Erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS eine Liste aller Elemente in einem Ordner oder eine Liste der Änderungen abrufen können, die in einem Ordner aufgetreten sind, um den Client zu synchronisieren.
ms.openlocfilehash: e75f90b2d28d782465de89000796deccdd125e25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527712"
---
# <a name="synchronize-items-by-using-ews-in-exchange"></a><span data-ttu-id="e4210-103">Synchronisieren von Elementen unter Verwendung von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e4210-103">Synchronize items by using EWS in Exchange</span></span>

<span data-ttu-id="e4210-104">Erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS eine Liste aller Elemente in einem Ordner oder eine Liste der Änderungen abrufen können, die in einem Ordner aufgetreten sind, um den Client zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="e4210-104">Find out how to use the EWS Managed API or EWS to get a list of all items in a folder, or a list of changes that have occurred in a folder, in order to synchronize your client.</span></span>
  
<span data-ttu-id="e4210-105">EWS in Exchange verwendet die Element Synchronisierung und die Ordnersynchronisierung zum Synchronisieren von Postfachinhalten zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="e4210-105">EWS in Exchange uses item synchronization and folder synchronization to sync mailbox content between the client and server.</span></span> <span data-ttu-id="e4210-106">Die Element Synchronisierung Ruft die anfängliche Liste der Elemente in einem Ordner ab und ruft dann im Laufe der Zeit Änderungen ab, die an diesen Elementen vorgenommen wurden, und ruft auch neue Elemente ab.</span><span class="sxs-lookup"><span data-stu-id="e4210-106">Item synchronization gets the initial list of items in a folder and then, over time, gets changes that have been made to those items and gets new items as well.</span></span>
  
<span data-ttu-id="e4210-107">Beachten Sie, dass Sie zunächst [die Ordnerhierarchie synchronisieren](how-to-synchronize-folders-by-using-ews-in-exchange.md)müssen, bevor Sie Elemente mit einem Client synchronisieren können.</span><span class="sxs-lookup"><span data-stu-id="e4210-107">Note that before you can sync items to a client, you first have to [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="e4210-108">Nachdem die Ordnerhierarchie auf dem Client vorhanden ist, wenn Sie die Element Synchronisierung mithilfe des verwaltete EWS-API durchführen, rufen Sie zunächst die erste [Liste der Elemente im Posteingang](#bk_cesyncongoingewsma) mithilfe der [Datei "ExchangeService. SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="e4210-108">After the folder hierarchy is in place on the client, if you're performing item synchronization by using the EWS Managed API, you first [get the initial list of items in the Inbox](#bk_cesyncongoingewsma) by using the [ExchangeService.SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="e4210-109">Anschließend aktualisieren Sie den Wert des Parameters _cSyncState_ bei nachfolgenden Aufrufen, um die Liste der geänderten Elemente im Posteingang abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e4210-109">You then update the value of the  _cSyncState_ parameter during subsequent calls to get the list of changed items in the Inbox.</span></span> 
  
<span data-ttu-id="e4210-110">Wenn Sie die Element Synchronisierung mithilfe von EWS ausführen möchten, fordern Sie nach dem [Synchronisieren der Ordnerhierarchie](how-to-synchronize-folders-by-using-ews-in-exchange.md)die [anfängliche Liste der Elemente im Posteingang](#bk_ewsexamplea) an, indem Sie den [SyncFolderItems-Vorgang](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)verwenden, die Antwort analysieren und dann zu einem späteren Zeitpunkt [die Änderungen an den Elementen im Postfach abrufen](#bk_ewsexamplec)und die Antwort analysieren.</span><span class="sxs-lookup"><span data-stu-id="e4210-110">To perform item synchronization by using EWS, after you [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md), you request the [initial list of items in the Inbox](#bk_ewsexamplea) by using the [SyncFolderItems operation](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx), parse the response, and then at some point in the future [get the changes to the items in the mailbox](#bk_ewsexamplec), and parse the response.</span></span> <span data-ttu-id="e4210-111">Nachdem der Client die Liste der anfänglichen oder geänderten Elemente empfangen hat, werden [Aktualisierungen lokal vorgenommen](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="e4210-111">After the client receives the list of initial or changed items, it [makes updates locally](#bk_nextsteps).</span></span> <span data-ttu-id="e4210-112">Wie und wann Sie Änderungen in der Zukunft abrufen, hängt vom [Synchronisierungs Entwurfsmuster](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) ab, das Ihre Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4210-112">How and when you retrieve changes in the future depends on the [synchronization design pattern](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) your application is using.</span></span> 
  
## <a name="get-the-list-of-all-items-or-changed-items-by-using-the-ews-managed-api"></a><span data-ttu-id="e4210-113">Abrufen der Liste aller Elemente oder geänderten Elemente mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="e4210-113">Get the list of all items or changed items by using the EWS Managed API</span></span>
<span data-ttu-id="e4210-114"><a name="bk_cesyncongoingewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e4210-114"><a name="bk_cesyncongoingewsma"> </a></span></span>

<span data-ttu-id="e4210-115">Im folgenden Codebeispiel wird gezeigt, wie Sie eine anfängliche Liste aller Elemente im Posteingangsordner erhalten und dann eine Liste der Änderungen an Elementen im Posteingangsordner erhalten, die seit der vorherigen Synchronisierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="e4210-115">The following code example shows how to get an initial list of all items in the Inbox folder and then get a list of changes to items in the Inbox folder that have occurred since the previous synchronization.</span></span> <span data-ttu-id="e4210-116">Legen Sie beim ersten Aufruf der [SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) -Methode den _cSyncState_ -Wert auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="e4210-116">During the initial call to the [SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) method, set the  _cSyncState_ value to null.</span></span> <span data-ttu-id="e4210-117">Wenn die Methode abgeschlossen ist, speichern Sie den _cSyncState_ -Wert lokal, um ihn im nächsten Aufruf der **SyncFolderItems** -Methode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4210-117">When the method completes, save the  _cSyncState_ value locally to use in the next **SyncFolderItems** method call.</span></span> <span data-ttu-id="e4210-118">Sowohl in der ersten als auch in den nachfolgenden Aufrufen werden die Elemente in 10-Batches abgerufen, indem aufeinanderfolgende Aufrufe der **SyncFolderItems** -Methode verwendet werden, bis keine weiteren Änderungen mehr bestehen.</span><span class="sxs-lookup"><span data-stu-id="e4210-118">In both the initial call and the subsequent calls, the items are retrieved in batches of ten, by using successive calls to the **SyncFolderItems** method, until no more changes remain.</span></span> 
  
<span data-ttu-id="e4210-119">In diesem Beispiel wird der _PropertySet-_ Parameter auf IdOnly festgelegt, um Aufrufe an die Exchange-Datenbank zu reduzieren, was eine [bewährte Synchronisierungsmethode](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)ist.</span><span class="sxs-lookup"><span data-stu-id="e4210-119">This example sets the  _propertySet_ parameter to IdOnly to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="e4210-120">In diesem Beispiel wird davon ausgegangen, dass **Dienst** eine gültige **Datei "ExchangeService** -Objektbindung ist und dass _cSyncState_ den Synchronisierungs Zustand darstellt, der von einem vorherigen Aufruf von **SyncFolderItems**zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e4210-120">In this example, we assume that **service** is a valid **ExchangeService** object binding and that  _cSyncState_ represents the sync state that was returned by a prior call to **SyncFolderItems**.</span></span> 
  
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

Die **SyncFolderItems** -Methode ähnelt der [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methode darin, dass Sie keine Eigenschaften wie [Body](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) oder [Attachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx)zurückgeben kann. <span data-ttu-id="e4210-122">Wenn Sie Eigenschaften benötigen, die von der **SyncFolderItems** -Methode nicht zurückgegeben werden können, geben Sie beim Aufrufen **von SyncFolderItems**den [IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset.idonly%28v=exchg.80%29.aspx) -Eigenschaftswert an, und verwenden Sie dann die [Datei "ExchangeService. LoadPropertiesForItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) -Methode, um die Eigenschaften abzurufen, die Sie für die Elemente benötigen, die von der **SyncFolderItems** -Methode zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="e4210-122">If you need properties that cannot be returned by the **SyncFolderItems** method, specify the [IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset.idonly%28v=exchg.80%29.aspx) property set when you call **SyncFolderItems**, and then use the [ExchangeService.LoadPropertiesForItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) method to get the properties you require for the items that were returned by the **SyncFolderItems** method.</span></span> 
  
<span data-ttu-id="e4210-123">Nachdem Sie die Liste der neuen oder geänderten Elemente auf dem Server abgerufen haben, [erstellen oder aktualisieren Sie die Elemente auf dem Client](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="e4210-123">After you retrieve the list of new or changed items on the server, [create or update the items on the client](#bk_nextsteps).</span></span>
  
## <a name="get-the-initial-list-of-items-by-using-ews"></a><span data-ttu-id="e4210-124">Abrufen der anfänglichen Liste von Elementen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="e4210-124">Get the initial list of items by using EWS</span></span>
<span data-ttu-id="e4210-125"><a name="bk_ewsexamplea"> </a></span><span class="sxs-lookup"><span data-stu-id="e4210-125"><a name="bk_ewsexamplea"> </a></span></span>

<span data-ttu-id="e4210-126">Das folgende Beispiel zeigt die XML-Anforderung zum Abrufen der anfänglichen Liste der Elemente im Posteingang mithilfe des [SyncFolderItems-Vorgangs](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e4210-126">The following example shows the XML request to get the initial list of items in the Inbox by using the [SyncFolderItems operation](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx).</span></span> <span data-ttu-id="e4210-127">Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn [die Liste der Elemente mithilfe der SyncFolderItems-Methode abgerufen](#bk_cesyncongoingewsma)wird.</span><span class="sxs-lookup"><span data-stu-id="e4210-127">This is also the XML request that the EWS Managed API sends when [retrieving the list of items by using the SyncFolderItems method](#bk_cesyncongoingewsma).</span></span> <span data-ttu-id="e4210-128">Das [von "SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) -Element des **SyncFolderItems** -Vorgangs ist nicht enthalten, da dies die anfängliche Synchronisierung ist.</span><span class="sxs-lookup"><span data-stu-id="e4210-128">The [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element of the **SyncFolderItems** operation is not included because this is the initial synchronization.</span></span> <span data-ttu-id="e4210-129">In diesem Beispiel wird das [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Element auf **IdOnly** festgelegt, um Aufrufe an die Exchange-Datenbank zu reduzieren, was eine [bewährte Synchronisierungsmethode](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)ist.</span><span class="sxs-lookup"><span data-stu-id="e4210-129">This example sets the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span>
  
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

<span data-ttu-id="e4210-130"><a name="bk_responsesyncfolderitems"> </a></span><span class="sxs-lookup"><span data-stu-id="e4210-130"><a name="bk_responsesyncfolderitems"> </a></span></span>

<span data-ttu-id="e4210-131">Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die **SyncFolderItems** -Vorgangsanforderung vom Client verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="e4210-131">The following example shows the XML response that is returned by the server after it processes the **SyncFolderItems** operation request from the client.</span></span> <span data-ttu-id="e4210-132">Die anfängliche Antwort umfasst [Create](https://msdn.microsoft.com/library/cb5e64a2-66a5-4447-921e-7c13efb8f6bf%28Office.15%29.aspx) -Elemente für fünf Elemente, da alle Elemente während einer anfänglichen Synchronisierung als neu betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="e4210-132">The initial response includes [Create](https://msdn.microsoft.com/library/cb5e64a2-66a5-4447-921e-7c13efb8f6bf%28Office.15%29.aspx) elements for five items because all items are considered new during an initial synchronization.</span></span> <span data-ttu-id="e4210-133">Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="e4210-133">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e4210-134">Nachdem Sie die Liste der neuen Elemente auf dem Server abgerufen haben, [Erstellen Sie die Elemente auf dem Client](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="e4210-134">After you retrieve the list of new items on the server, [create the items on the client](#bk_nextsteps).</span></span>
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a><span data-ttu-id="e4210-135">Abrufen der Änderungen seit der letzten Synchronisierung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="e4210-135">Get the changes since the last sync by using EWS</span></span>
<span data-ttu-id="e4210-136"><a name="bk_ewsexamplec"> </a></span><span class="sxs-lookup"><span data-stu-id="e4210-136"><a name="bk_ewsexamplec"> </a></span></span>

<span data-ttu-id="e4210-137">Das folgende Beispiel zeigt die XML-Anforderung zum Abrufen der Liste der Änderungen an Elementen im Posteingang mithilfe des [SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) -Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e4210-137">The following example shows the XML request to get the list of changes to items in the Inbox by using the [SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="e4210-138">Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn [die Liste der Änderungen im Posteingang abgerufen](#bk_cesyncongoingewsma)wird.</span><span class="sxs-lookup"><span data-stu-id="e4210-138">This is also the XML request that the EWS Managed API sends when [retrieving the list of changes to the Inbox](#bk_cesyncongoingewsma).</span></span> <span data-ttu-id="e4210-139">In diesem Beispiel wird der Wert des [von "SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) -Elements auf den in der [vorherigen Antwort](#bk_responsesyncfolderitems)zurückgegebenen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e4210-139">This example sets the [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element value to the value returned in the [previous response](#bk_responsesyncfolderitems).</span></span> <span data-ttu-id="e4210-140">In diesem Beispiel wird das [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Element zu Demonstrationszwecken auf **allproperties** statt auf **IdOnly** festgelegt, um die zurückgegebenen zusätzlichen Eigenschaften anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e4210-140">And for demonstration purposes, this example sets the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **AllProperties** instead of **IdOnly** to show the additional properties returned.</span></span> <span data-ttu-id="e4210-141">Das Festlegen des [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Elements auf **IdOnly** ist eine [bewährte Methode](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)für die Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="e4210-141">Setting the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="e4210-142">Der Wert von **von "SyncState** wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="e4210-142">The value of **SyncState** has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="e4210-143">Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die **SyncFolderItems** -Vorgangsanforderung vom Client verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="e4210-143">The following example shows the XML response that is returned by the server after it processes the **SyncFolderItems** operation request from the client.</span></span> <span data-ttu-id="e4210-144">Diese Antwort gibt an, dass ein Element aktualisiert wurde, zwei Elemente erstellt wurden, die Lese Markierung eines Elements geändert wurde und ein Element seit der vorherigen Synchronisierung gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="e4210-144">This response indicates that one item was updated, two items were created, the read flag of one item was changed, and one item was deleted since the prior synchronization.</span></span> <span data-ttu-id="e4210-145">Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="e4210-145">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3"
                 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                 xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

Die **SyncFolderItems** -Operation ähnelt der [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methode darin, dass Sie keine Elemente wie die Elemente [Body](https://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) oder [Attachments](https://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) zurückgeben kann. <span data-ttu-id="e4210-147">Wenn Sie Eigenschaften benötigen, die nicht vom **SyncFolderItems** -Vorgang zurückgegeben werden können, legen Sie den Wert des [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Elements auf IdOnly fest, wenn Sie **SyncFolderItems**aufrufen, und verwenden Sie dann den [GetItem-Vorgang](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) , um die Eigenschaften abzurufen, die Sie für die Elemente benötigen, die von der **SyncFolderItems** -Operation zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="e4210-147">If you need properties that cannot be returned by the **SyncFolderItems** operation, set the value of the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to IdOnly when you call **SyncFolderItems**, and then use the [GetItem operation](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) to get the properties you require for the items that were returned by the **SyncFolderItems** operation.</span></span> 
  
<span data-ttu-id="e4210-148">Nachdem Sie die Liste der geänderten Elemente auf dem Server abgerufen haben, [Aktualisieren Sie die Elemente auf dem Client](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="e4210-148">After you retrieve the list of changed items on the server, [update the items on the client](#bk_nextsteps).</span></span>
  
## <a name="update-the-client"></a><span data-ttu-id="e4210-149">Aktualisieren des Clients</span><span class="sxs-lookup"><span data-stu-id="e4210-149">Update the client</span></span>
<span data-ttu-id="e4210-150"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="e4210-150"><a name="bk_nextsteps"> </a></span></span>

<span data-ttu-id="e4210-151">Wenn Sie die verwaltete EWS-API verwenden, nachdem Sie die Liste der neuen oder geänderten Elemente abgerufen haben, verwenden Sie die [LoadPropertiesForItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) -Methode, um Eigenschaften für die neuen oder geänderten Elemente abzurufen, die Eigenschaften mit den lokalen Werten zu vergleichen und die Elemente auf dem Client zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e4210-151">If you're using the EWS Managed API, after you get the list of new or changed items, use the [LoadPropertiesForItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) method to get properties on the new or changed items, compare the properties to the local values, and update the items on the client.</span></span> 
  
<span data-ttu-id="e4210-152">Wenn Sie EWS verwenden, verwenden Sie den [GetItem-Vorgang](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) , um Eigenschaften für die neuen oder geänderten Elemente abzurufen und die Elemente auf dem Client zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e4210-152">If you're using EWS, use the [GetItem operation](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) to get properties on the new or changed items and update the items on the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4210-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4210-153">See also</span></span>


- [<span data-ttu-id="e4210-154">Postfachsynchronisierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e4210-154">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    
- [<span data-ttu-id="e4210-155">Synchronisieren von Ordnern unter Verwendung von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e4210-155">Synchronize folders by using EWS in Exchange</span></span>](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="e4210-156">Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e4210-156">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="e4210-157">Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e4210-157">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    

