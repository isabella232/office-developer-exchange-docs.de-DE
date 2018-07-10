---
title: Synchronisieren von Ordnern in Exchange mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d3bbacd1-8e4b-4fd0-8d27-4cbbc045ec3f
description: Erfahren Sie, wie die EWS Managed API oder EWS zum Abrufen einer Liste von Ordnern oder eine Liste von Ordnern, die zum Synchronisieren von Ihrem Clients geändert haben, verwenden.
ms.openlocfilehash: 4b0686134d642da34b2890a0e692e3d03e4a9fb1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757008"
---
# <a name="synchronize-folders-by-using-ews-in-exchange"></a><span data-ttu-id="7c1ac-103">Synchronisieren von Ordnern in Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="7c1ac-103">Synchronize folders by using EWS in Exchange</span></span>

<span data-ttu-id="7c1ac-104">Erfahren Sie, wie die EWS Managed API oder EWS zum Abrufen einer Liste von Ordnern oder eine Liste von Ordnern, die zum Synchronisieren von Ihrem Clients geändert haben, verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-104">Find out how to use the EWS Managed API or EWS to get a list of folders, or a list of folders that have changed, in order to synchronize your client.</span></span>
  
<span data-ttu-id="7c1ac-105">EWS in Exchange verwendet Element Synchronisierung und Ordner der Synchronisierung der Inhalt von Postfächern Synchronisierung zwischen dem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-105">EWS in Exchange uses item synchronization and folder synchronization to sync mailbox content between the client and server.</span></span> <span data-ttu-id="7c1ac-106">Ordnersynchronisation Ruft die ursprüngliche Liste der Ordner aus einer Stammordner ab und ruft dann im Laufe der Zeit Änderungen, die für diese Ordner vorgenommen wurden und ruft sowie neue Ordner.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-106">Folder synchronization gets the initial list of folders from a root folder and then, over time, gets changes that were made to those folders and gets new folders as well.</span></span>
  
<span data-ttu-id="7c1ac-107">Wenn Sie mithilfe der EWS Managed API, Sie zuerst [die ursprüngliche Liste der Ordner im Stammordner erhalten möchten](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) , mithilfe der Methode [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) Ordnersynchronisation durchführen.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-107">If you're performing folder synchronization by using the EWS Managed API, you first [get the initial list of folders in the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) by using the [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="7c1ac-108">Dann aktualisieren Sie den Wert des Parameters _cSyncState_ bei nachfolgenden Aufrufen, um die Liste der neuen und geänderten Ordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-108">You then update the value of the  _cSyncState_ parameter during subsequent calls to get the list of new and changed folders.</span></span> 
  
<span data-ttu-id="7c1ac-109">Mithilfe der Exchange-Webdienste führen Ordnersynchronisation Sie die [ursprüngliche Liste der Ordner im Stammordner](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) mit der [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) -Operation anfordern, Verarbeiten der Antwort und anschließend zu einem bestimmten Zeitpunkt in der Zukunft [die Änderungen in den Ordnern in das Stammverzeichnis](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews), und die Antwort zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-109">To perform folder synchronization by using EWS, you request the [initial list of folders in the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) by using the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation, parse the response, and then at some point in the future [get the changes to the folders in the root](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews), and parse the response.</span></span> <span data-ttu-id="7c1ac-110">Nachdem der Client die Liste der ursprünglichen oder geänderten Ordner empfangen sie [Updates lokal macht](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="7c1ac-110">After the client receives the list of initial or changed folders, it [makes updates locally](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span> <span data-ttu-id="7c1ac-111">Wie und wann Sie Änderungen in der Zukunft abrufen, hängt von der [Synchronisierung Entwurfsmuster](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) , Ihre Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-111">How and when you retrieve changes in the future depends on the [synchronization design pattern](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) your application is using.</span></span> 
  
## <a name="get-the-list-of-all-folders-or-changed-folders-by-using-the-ews-managed-api"></a><span data-ttu-id="7c1ac-112">Abrufen der Liste aller Ordner oder geänderten Ordner mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="7c1ac-112">Get the list of all folders or changed folders by using the EWS Managed API</span></span>
<span data-ttu-id="7c1ac-113"><a name="bk_cesyncinitialewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="7c1ac-113"></span></span>

<span data-ttu-id="7c1ac-114">Im folgenden Codebeispiel wird veranschaulicht, wie die ursprüngliche Liste von Ordnern in einem Stammordner rufen und anschließend eine Liste der Änderungen auf Ordner im Stammordner gespeichert, die seit der vorherigen Synchronisierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-114">The following code example shows how to get an initial list of folders in a root folder and then get a list of changes to folders in the root folder that have occurred since the previous synchronization.</span></span> <span data-ttu-id="7c1ac-115">Während der anfänglichen Aufruf der [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) -Methode den _cSyncState_ -Wert auf null festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-115">During the initial call to the [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) method, set the  _cSyncState_ value to null.</span></span> <span data-ttu-id="7c1ac-116">Wenn die Methode abgeschlossen ist, speichern Sie den _cSyncState_ Wert lokal für den nächsten Aufruf der **SyncFolderHierarchy** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-116">When the method completes, save the  _cSyncState_ value locally to use in the next **SyncFolderHierarchy** method call.</span></span> <span data-ttu-id="7c1ac-117">In der ersten Aufruf und die nachfolgenden Aufrufen werden die Ordner in Batches von zehn mithilfe von aufeinander folgenden Aufrufen der Methode **SyncFolderHierarchy** bis keine weitere Änderungen bleiben abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-117">In both the initial call and the subsequent calls, the folders are retrieved in batches of ten, by using successive calls to the **SyncFolderHierarchy** method, until no more changes remain.</span></span> <span data-ttu-id="7c1ac-118">In diesem Beispiel wird den Parameter _PropertySet_ IdOnly um Anrufe an die Exchange-Datenbank eine [bewährte Methode Synchronisierung ist](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)reduzieren.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-118">This example sets the  _propertySet_ parameter to IdOnly to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="7c1ac-119">In diesem Beispiel wird davon ausgegangen, dass **-Dienst** eine gültige **ExchangeService** Objekt Bindung ist und diese _cSyncState_ stellt den Synchronisierungsstatus an, der von einem vorherigen Aufruf von **SyncFolderHierarchy**zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-119">In this example, we assume that **service** is a valid **ExchangeService** object binding and that  _cSyncState_ represents the sync state that was returned by a prior call to **SyncFolderHierarchy**.</span></span> 
  
```cs
// Get a list of all folders in the mailbox by calling SyncFolderHierarchy.
// The folderId parameter must be set to the root folder to synchronize. 
// The propertySet parameter is set to IdOnly to reduce calls to the Exchange database
// because any additional properties result in additional calls to the Exchange database. 
// The syncState parameter is set to cSyncState, which should be null in the initial call, 
// and should be set to the sync state returned by the previous SyncFolderHierarchy call 
// in subsequent calls.
ChangeCollection<FolderChange> fcc = service.SyncFolderHierarchy(new FolderId(WellKnownFolderName.Root), PropertySet.IdOnly, cSyncState);
// If the count of changes is zero, there are no changes to synchronize.
if (fcc.Count == 0)
{
    Console.WriteLine("There are no folders to synchronize.");
}
// Otherwise, write all the changes included in the response 
// to the console. 
// For the initial synchronization, all the changes will be of type
// ChangeType.Create.
else
{
    foreach (FolderChange fc in fcc)
    {
        Console.WriteLine("ChangeType: " + fc.ChangeType.ToString());
        Console.WriteLine("FolderId: " + fc.FolderId);
        Console.WriteLine("===========");
    }
}
// Save the sync state for use in future SyncFolderItems requests.
// The sync state is used by the server to determine what changes to report
// to the client.
string fSyncState = fcc.SyncState;

```

<span data-ttu-id="7c1ac-120">Rufen Sie nach dem Sie die Liste der neuen oder geänderten Ordner auf dem Server, [Erstellen oder aktualisieren den Ordner auf dem Client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)ab.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-120">After you retrieve the list of new or changed folders on the server, [create or update the folders on the client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="get-the-initial-list-of-folders-by-using-ews"></a><span data-ttu-id="7c1ac-121">Möchten Sie die ursprüngliche Liste der Ordner mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="7c1ac-121">Get the initial list of folders by using EWS</span></span>
<span data-ttu-id="7c1ac-122"><a name="bk_cesyncewsrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="7c1ac-122"></span></span>

<span data-ttu-id="7c1ac-123">Das folgende Beispiel zeigt eine XML-Anforderung die anfänglichen Ordnerhierarchie mithilfe des Vorgangs [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) abrufen.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-123">The following example shows an XML request to get the initial folder hierarchy by using the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="7c1ac-124">Dies ist auch die XML-Anfrage, dass die EWS Managed API, wenn gesendet [die Liste der ursprünglichen Ordner mithilfe der SyncFolderHierarchy-Methode abrufen](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span><span class="sxs-lookup"><span data-stu-id="7c1ac-124">This is also the XML request that the EWS Managed API sends when [retrieving the list of initial folders by using the SyncFolderHierarchy method](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span></span> <span data-ttu-id="7c1ac-125">Das Element [Synchronisierungsstatus](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) des Vorgangs [SyncFolderHierarchy](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) ist nicht mit inbegriffen, da dies die anfängliche Synchronisierung ist.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-125">The [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element of the [SyncFolderHierarchy](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) operation is not included because this is the initial synchronization.</span></span> <span data-ttu-id="7c1ac-126">In diesem Beispiel wird das Element [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) **IdOnly** um Anrufe an die Exchange-Datenbank eine [bewährte Methode Synchronisierung ist](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)reduzieren.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-126">This example sets the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span>
  
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
    <m:SyncFolderHierarchy>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="root" />
      </m:SyncFolderId>
    </m:SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7c1ac-127">Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) Vorgang Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-127">The following example shows the XML response that is returned by the server after it processes the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation request.</span></span> <span data-ttu-id="7c1ac-128">Die erste Antwort enthält Elemente für alle Ordner [Erstellen](http://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) , da alle Ordner neu beim eine anfängliche Synchronisierung berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-128">The initial response includes [Create](http://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) elements for all folders because all folders are considered new during an initial synchronization.</span></span> <span data-ttu-id="7c1ac-129">Die Werte der einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt wurde, und einige **Erstellen** Element Blöcke der Kürze halber entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-129">The values of some attributes and elements have been shortened for readability, and some **Create** element blocks were removed for brevity.</span></span> 
  
```xml
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
    <m:SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                   xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAA==</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADM="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADMzM="
                            ChangeKey="AQAAABY"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkAD/AAA="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADBh="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            ...
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderHierarchyResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="7c1ac-130">Abgerufen Sie nachdem die Liste der neue Ordner auf dem Server, [Erstellen Sie die Ordner auf dem Client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="7c1ac-130">After you retrieve the list of new folders on the server, [create the folders on the client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a><span data-ttu-id="7c1ac-131">Abrufen von Änderungen seit der letzten Synchronisierung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="7c1ac-131">Get the changes since the last sync by using EWS</span></span>
<span data-ttu-id="7c1ac-132"><a name="bk_cesyncrespews"> </a></span><span class="sxs-lookup"><span data-stu-id="7c1ac-132"></span></span>

<span data-ttu-id="7c1ac-133">Das folgende Beispiel zeigt die XML-Anforderung an die Liste der Änderungen auf Ordner im Stammordner abrufen, indem Sie den Vorgang [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7c1ac-133">The following example shows the XML request to get the list of changes to folders in the root folder by using the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="7c1ac-134">Dies ist auch, dass die EWS Managed API, wenn gesendet die XML-Anfrage [Abrufen der Liste der Änderungen in den Stammordner](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span><span class="sxs-lookup"><span data-stu-id="7c1ac-134">This is also the XML request that the EWS Managed API sends when [retrieving the list of changes to the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span></span> <span data-ttu-id="7c1ac-135">In diesem Beispiel wird den [Synchronisierungsstatus](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) Elementwert auf den Wert in der vorherigen Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-135">This example sets the [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element value to the value returned in the previous response.</span></span> <span data-ttu-id="7c1ac-136">Und zur Veranschaulichung in diesem Beispiel wird das Element [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) **AllProperties** anstelle von **IdOnly** zum Anzeigen der zusätzlichen Eigenschaften zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-136">And for demonstration purposes, this example sets the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **AllProperties** instead of **IdOnly** to show the additional properties returned.</span></span> <span data-ttu-id="7c1ac-137">Festlegen der [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Elements auf **IdOnly** ist eine [bewährte Methode Synchronisierung](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span><span class="sxs-lookup"><span data-stu-id="7c1ac-137">Setting the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="7c1ac-138">Der Wert der **Synchronisierungsstatus** wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-138">The value of **SyncState** has been shortened for readability.</span></span> 
  
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
    <m:SyncFolderHierarchy>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="root" />
      </m:SyncFolderId>
      <m:SyncState>H4sIAA==</m:SyncState>
    </m:SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7c1ac-139">Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem der [Vorgang SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) Anforderung vom Client verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-139">The following example shows the XML response that is returned by the server after it processes the [SyncFolderHierarchy operation](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) request from the client.</span></span> <span data-ttu-id="7c1ac-140">Diese Antwort gibt an, dass ein Ordner aktualisiert wurde, einen Ordner erstellt wurde, und ein Ordner, seit der vorherigen Synchronisierung gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-140">This response indicates that one folder was updated, one folder was created, and one folder was deleted since the prior synchronization.</span></span> <span data-ttu-id="7c1ac-141">Der Wert der [Synchronisierungsstatus](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) -Element, Attribute **Id** und **ChangeKey** Attribute wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-141">The value of the [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element, **Id** attributes, and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
<span data-ttu-id="7c1ac-142">Denken Sie daran, dass die Anforderung der **AllProperties**[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)enthalten.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-142">Remember that the request included the **AllProperties**[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx).</span></span> <span data-ttu-id="7c1ac-143">Dies ist nur zu Demonstrationszwecken.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-143">This is just for demonstration purposes.</span></span> <span data-ttu-id="7c1ac-144">Es wird empfohlen, dass Sie das **BaseShape** -Element in der Produktion auf **IdOnly** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-144">We recommend that you set the **BaseShape** element to **IdOnly** in production.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
<h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="745" MinorBuildNumber="21" Version="V2_3" 
           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Update>
              <t:Folder>
                <t:FolderId Id="AAMkADM=" ChangeKey="AQAAABY" />
                <t:ParentFolderId Id="AQMkADMzADI1==" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>Meeting Notes</t:DisplayName>
                <t:TotalCount>3</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:EffectiveRights>
                  <t:CreateAssociated>true</t:CreateAssociated>
                  <t:CreateContents>true</t:CreateContents>
                  <t:CreateHierarchy>true</t:CreateHierarchy>
                  <t:Delete>true</t:Delete>
                  <t:Modify>true</t:Modify>
                  <t:Read>true</t:Read>
                  <t:ViewPrivateItems>true</t:ViewPrivateItems>
                </t:EffectiveRights>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Update>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADMzM=" ChangeKey="AQAAABYAA" />
                <t:ParentFolderId Id="AQMkO67A==" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>Schedules</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:EffectiveRights>
                  <t:CreateAssociated>true</t:CreateAssociated>
                  <t:CreateContents>true</t:CreateContents>
                  <t:CreateHierarchy>true</t:CreateHierarchy>
                  <t:Delete>true</t:Delete>
                  <t:Modify>true</t:Modify>
                  <t:Read>true</t:Read>
                  <t:ViewPrivateItems>true</t:ViewPrivateItems>
                </t:EffectiveRights>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Create>
            <t:Delete>
              <t:FolderId Id="AAMkAD/AAA=" ChangeKey="AQAAAA==" />
            </t:Delete>
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderHierarchyResponse>
  </s:Body>
</s:Envelope>

```

## <a name="update-the-client"></a><span data-ttu-id="7c1ac-145">Aktualisieren des Clients</span><span class="sxs-lookup"><span data-stu-id="7c1ac-145">Update the client</span></span>
<span data-ttu-id="7c1ac-146"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="7c1ac-146"></span></span>

<span data-ttu-id="7c1ac-147">Wenn Sie die EWS Managed API, nachdem Sie die Liste der neuen oder geänderten Ordner abrufen, verwenden Sie die [Folder.Load](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) -Methode zum Abrufen von Eigenschaften für die neue oder geänderte Elemente, die Eigenschaften in die lokale Werte vergleichen und aktualisieren oder erstellen Sie die Ordner auf dem Client verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-147">If you're using the EWS Managed API, after you get the list of new or changed folders, use the [Folder.Load](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) method to get properties on the new or changed items, compare the properties to the local values, and update or create the folders on the client.</span></span> 
  
<span data-ttu-id="7c1ac-148">Wenn Sie Exchange-Webdienste verwenden, verwenden Sie die [GetFolder-Vorgang](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) zum Abrufen von Eigenschaften für die neue oder geänderte Ordner und aktualisieren oder erstellen Sie die Ordner auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="7c1ac-148">If you're using EWS, use the [GetFolder operation](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) to get properties on the new or changed folders and update or create the folders on the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c1ac-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c1ac-149">See also</span></span>

- [<span data-ttu-id="7c1ac-150">Postfachsynchronisierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7c1ac-150">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)   
- [<span data-ttu-id="7c1ac-151">Synchronisieren von Elementen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7c1ac-151">Synchronize items by using EWS in Exchange</span></span>](how-to-synchronize-items-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="7c1ac-152">Fehlerbehandlung Synchronisierung-bezogene in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7c1ac-152">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    

