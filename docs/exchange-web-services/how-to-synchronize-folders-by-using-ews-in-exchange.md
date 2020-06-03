---
title: Synchronisieren von Ordnern unter Verwendung von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d3bbacd1-8e4b-4fd0-8d27-4cbbc045ec3f
description: Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um eine Liste der Ordner oder eine Liste von Ordnern abzurufen, die sich geändert haben, um den Client zu synchronisieren.
ms.openlocfilehash: e49fdaf2faf97c2369f2ad7dbb141c5ac3100884
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455863"
---
# <a name="synchronize-folders-by-using-ews-in-exchange"></a><span data-ttu-id="5517f-103">Synchronisieren von Ordnern unter Verwendung von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="5517f-103">Synchronize folders by using EWS in Exchange</span></span>

<span data-ttu-id="5517f-104">Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um eine Liste der Ordner oder eine Liste von Ordnern abzurufen, die sich geändert haben, um den Client zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5517f-104">Find out how to use the EWS Managed API or EWS to get a list of folders, or a list of folders that have changed, in order to synchronize your client.</span></span>
  
<span data-ttu-id="5517f-105">EWS in Exchange verwendet die Element Synchronisierung und die Ordnersynchronisierung zum Synchronisieren von Postfachinhalten zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="5517f-105">EWS in Exchange uses item synchronization and folder synchronization to sync mailbox content between the client and server.</span></span> <span data-ttu-id="5517f-106">Die Ordnersynchronisierung Ruft die anfängliche Liste der Ordner aus einem Stammordner ab und ruft dann im Laufe der Zeit Änderungen ab, die an diesen Ordnern vorgenommen wurden, und ruft auch neue Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="5517f-106">Folder synchronization gets the initial list of folders from a root folder and then, over time, gets changes that were made to those folders and gets new folders as well.</span></span>
  
<span data-ttu-id="5517f-107">Wenn Sie die Ordnersynchronisierung mit dem verwaltete EWS-API durchführen, erhalten Sie zunächst die erste [Liste der Ordner im Stammordner](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) mithilfe der [Datei "ExchangeService. SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5517f-107">If you're performing folder synchronization by using the EWS Managed API, you first [get the initial list of folders in the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) by using the [ExchangeService.SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="5517f-108">Anschließend aktualisieren Sie den Wert des Parameters _cSyncState_ bei nachfolgenden Aufrufen, um die Liste der neuen und geänderten Ordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5517f-108">You then update the value of the  _cSyncState_ parameter during subsequent calls to get the list of new and changed folders.</span></span> 
  
<span data-ttu-id="5517f-109">Um die Ordnersynchronisierung mithilfe von EWS durchzuführen, fordern Sie die [anfängliche Liste der Ordner im Stammordner](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) mithilfe des [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) -Vorgangs an, analysieren die Antwort und dann zu einem späteren Zeitpunkt [die Änderungen an den Ordnern im Stamm](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews)Verzeichnis und analysieren die Antwort.</span><span class="sxs-lookup"><span data-stu-id="5517f-109">To perform folder synchronization by using EWS, you request the [initial list of folders in the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) by using the [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation, parse the response, and then at some point in the future [get the changes to the folders in the root](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews), and parse the response.</span></span> <span data-ttu-id="5517f-110">Nachdem der Client die Liste der anfänglichen oder geänderten Ordner empfangen hat, werden [Aktualisierungen lokal vorgenommen](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="5517f-110">After the client receives the list of initial or changed folders, it [makes updates locally](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span> <span data-ttu-id="5517f-111">Wie und wann Sie Änderungen in der Zukunft abrufen, hängt vom [Synchronisierungs Entwurfsmuster](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) ab, das Ihre Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5517f-111">How and when you retrieve changes in the future depends on the [synchronization design pattern](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) your application is using.</span></span> 
  
## <a name="get-the-list-of-all-folders-or-changed-folders-by-using-the-ews-managed-api"></a><span data-ttu-id="5517f-112">Abrufen der Liste aller Ordner oder geänderten Ordner mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="5517f-112">Get the list of all folders or changed folders by using the EWS Managed API</span></span>
<span data-ttu-id="5517f-113"><a name="bk_cesyncinitialewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="5517f-113"><a name="bk_cesyncinitialewsma"> </a></span></span>

<span data-ttu-id="5517f-114">Im folgenden Codebeispiel wird gezeigt, wie eine anfängliche Liste von Ordnern in einem Stammordner abgerufen und dann eine Liste der Änderungen an Ordnern im Stammordner abgerufen wird, die seit der vorherigen Synchronisierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="5517f-114">The following code example shows how to get an initial list of folders in a root folder and then get a list of changes to folders in the root folder that have occurred since the previous synchronization.</span></span> <span data-ttu-id="5517f-115">Legen Sie beim ersten Aufruf der [Datei "ExchangeService. SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) -Methode den _cSyncState_ -Wert auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="5517f-115">During the initial call to the [ExchangeService.SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) method, set the  _cSyncState_ value to null.</span></span> <span data-ttu-id="5517f-116">Wenn die Methode abgeschlossen ist, speichern Sie den _cSyncState_ -Wert lokal, um ihn im nächsten Aufruf der **SyncFolderHierarchy** -Methode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5517f-116">When the method completes, save the  _cSyncState_ value locally to use in the next **SyncFolderHierarchy** method call.</span></span> <span data-ttu-id="5517f-117">Sowohl in der ersten als auch in den nachfolgenden Aufrufen werden die Ordner mit aufeinanderfolgenden Aufrufen der **SyncFolderHierarchy** -Methode in Batches von zehn abgerufen, bis keine weiteren Änderungen mehr vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="5517f-117">In both the initial call and the subsequent calls, the folders are retrieved in batches of ten, by using successive calls to the **SyncFolderHierarchy** method, until no more changes remain.</span></span> <span data-ttu-id="5517f-118">In diesem Beispiel wird der _PropertySet-_ Parameter auf IdOnly festgelegt, um Aufrufe an die Exchange-Datenbank zu reduzieren, was eine [bewährte Synchronisierungsmethode](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)ist.</span><span class="sxs-lookup"><span data-stu-id="5517f-118">This example sets the  _propertySet_ parameter to IdOnly to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="5517f-119">In diesem Beispiel wird davon ausgegangen, dass **Dienst** eine gültige **Datei "ExchangeService** -Objektbindung ist und dass _cSyncState_ den Synchronisierungs Zustand darstellt, der von einem vorherigen Aufruf von **SyncFolderHierarchy**zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5517f-119">In this example, we assume that **service** is a valid **ExchangeService** object binding and that  _cSyncState_ represents the sync state that was returned by a prior call to **SyncFolderHierarchy**.</span></span> 
  
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

<span data-ttu-id="5517f-120">Nachdem Sie die Liste der neuen oder geänderten Ordner auf dem Server abgerufen haben, [erstellen oder aktualisieren Sie die Ordner auf dem Client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="5517f-120">After you retrieve the list of new or changed folders on the server, [create or update the folders on the client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="get-the-initial-list-of-folders-by-using-ews"></a><span data-ttu-id="5517f-121">Abrufen der anfänglichen Liste der Ordner mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="5517f-121">Get the initial list of folders by using EWS</span></span>
<span data-ttu-id="5517f-122"><a name="bk_cesyncewsrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="5517f-122"><a name="bk_cesyncewsrequest"> </a></span></span>

<span data-ttu-id="5517f-123">Das folgende Beispiel zeigt eine XML-Anforderung zum Abrufen der anfänglichen Ordnerhierarchie mithilfe des [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) -Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5517f-123">The following example shows an XML request to get the initial folder hierarchy by using the [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="5517f-124">Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn die [Liste der anfänglichen Ordner mithilfe der SyncFolderHierarchy-Methode abgerufen](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)wird.</span><span class="sxs-lookup"><span data-stu-id="5517f-124">This is also the XML request that the EWS Managed API sends when [retrieving the list of initial folders by using the SyncFolderHierarchy method](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span></span> <span data-ttu-id="5517f-125">Das [von "SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) -Element des [SyncFolderHierarchy](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) -Vorgangs ist nicht enthalten, da dies die anfängliche Synchronisierung ist.</span><span class="sxs-lookup"><span data-stu-id="5517f-125">The [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element of the [SyncFolderHierarchy](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) operation is not included because this is the initial synchronization.</span></span> <span data-ttu-id="5517f-126">In diesem Beispiel wird das [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Element auf **IdOnly** festgelegt, um Aufrufe an die Exchange-Datenbank zu reduzieren, was eine [bewährte Synchronisierungsmethode](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)ist.</span><span class="sxs-lookup"><span data-stu-id="5517f-126">This example sets the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span>
  
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

<span data-ttu-id="5517f-127">Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) -Vorgangsanforderung verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="5517f-127">The following example shows the XML response that is returned by the server after it processes the [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation request.</span></span> <span data-ttu-id="5517f-128">Die anfängliche Antwort umfasst [Create](https://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) -Elemente für alle Ordner, da alle Ordner bei einer Erstsynchronisierung als neu betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="5517f-128">The initial response includes [Create](https://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) elements for all folders because all folders are considered new during an initial synchronization.</span></span> <span data-ttu-id="5517f-129">Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt, und einige **Create** -Elementblöcke wurden aus Gründen der Kürze entfernt.</span><span class="sxs-lookup"><span data-stu-id="5517f-129">The values of some attributes and elements have been shortened for readability, and some **Create** element blocks were removed for brevity.</span></span> 
  
```xml
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
    <m:SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                   xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="5517f-130">Nachdem Sie die Liste der neuen Ordner auf dem Server abgerufen haben, [Erstellen Sie die Ordner auf dem Client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="5517f-130">After you retrieve the list of new folders on the server, [create the folders on the client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a><span data-ttu-id="5517f-131">Abrufen der Änderungen seit der letzten Synchronisierung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="5517f-131">Get the changes since the last sync by using EWS</span></span>
<span data-ttu-id="5517f-132"><a name="bk_cesyncrespews"> </a></span><span class="sxs-lookup"><span data-stu-id="5517f-132"><a name="bk_cesyncrespews"> </a></span></span>

<span data-ttu-id="5517f-133">Das folgende Beispiel zeigt die XML-Anforderung zum Abrufen der Liste der Änderungen an Ordnern im Stammordner mithilfe des [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) -Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5517f-133">The following example shows the XML request to get the list of changes to folders in the root folder by using the [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="5517f-134">Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn [die Liste der Änderungen am Stammordner abgerufen](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)wird.</span><span class="sxs-lookup"><span data-stu-id="5517f-134">This is also the XML request that the EWS Managed API sends when [retrieving the list of changes to the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span></span> <span data-ttu-id="5517f-135">In diesem Beispiel wird der Wert des [von "SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) -Elements auf den in der vorherigen Antwort zurückgegebenen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5517f-135">This example sets the [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element value to the value returned in the previous response.</span></span> <span data-ttu-id="5517f-136">In diesem Beispiel wird das [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Element zu Demonstrationszwecken auf **allproperties** statt auf **IdOnly** festgelegt, um die zurückgegebenen zusätzlichen Eigenschaften anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5517f-136">And for demonstration purposes, this example sets the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **AllProperties** instead of **IdOnly** to show the additional properties returned.</span></span> <span data-ttu-id="5517f-137">Das Festlegen des [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Elements auf **IdOnly** ist eine [bewährte Methode](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)für die Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="5517f-137">Setting the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="5517f-138">Der Wert von **von "SyncState** wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="5517f-138">The value of **SyncState** has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="5517f-139">Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die [SyncFolderHierarchy-Vorgangs](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) Anforderung vom Client verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="5517f-139">The following example shows the XML response that is returned by the server after it processes the [SyncFolderHierarchy operation](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) request from the client.</span></span> <span data-ttu-id="5517f-140">Diese Antwort gibt an, dass ein Ordner aktualisiert wurde, ein Ordner erstellt wurde und ein Ordner seit der vorherigen Synchronisierung gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="5517f-140">This response indicates that one folder was updated, one folder was created, and one folder was deleted since the prior synchronization.</span></span> <span data-ttu-id="5517f-141">Der Wert für das [von "SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) -Element, das **ID-** Attribut und das **ChangeKey** -Attribut wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="5517f-141">The value of the [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element, **Id** attributes, and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
<span data-ttu-id="5517f-142">Beachten Sie, dass die Anforderung die **allproperties**-[BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)enthalten hat.</span><span class="sxs-lookup"><span data-stu-id="5517f-142">Remember that the request included the **AllProperties**[BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx).</span></span> <span data-ttu-id="5517f-143">Dies dient nur zu Demonstrationszwecken.</span><span class="sxs-lookup"><span data-stu-id="5517f-143">This is just for demonstration purposes.</span></span> <span data-ttu-id="5517f-144">Es wird empfohlen, das **BaseShape** -Element auf **IdOnly** in Production festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5517f-144">We recommend that you set the **BaseShape** element to **IdOnly** in production.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
<h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="745" MinorBuildNumber="21" Version="V2_3" 
           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="update-the-client"></a><span data-ttu-id="5517f-145">Aktualisieren des Clients</span><span class="sxs-lookup"><span data-stu-id="5517f-145">Update the client</span></span>
<span data-ttu-id="5517f-146"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="5517f-146"><a name="bk_nextsteps"> </a></span></span>

<span data-ttu-id="5517f-147">Wenn Sie die verwaltete EWS-API verwenden, nachdem Sie die Liste der neuen oder geänderten Ordner abgerufen haben, verwenden Sie die [Folder. Laden](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) -Methode, um Eigenschaften für die neuen oder geänderten Elemente abzurufen, die Eigenschaften mit den lokalen Werten zu vergleichen und die Ordner auf dem Client zu aktualisieren oder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5517f-147">If you're using the EWS Managed API, after you get the list of new or changed folders, use the [Folder.Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) method to get properties on the new or changed items, compare the properties to the local values, and update or create the folders on the client.</span></span> 
  
<span data-ttu-id="5517f-148">Wenn Sie EWS verwenden, verwenden Sie den [GetFolder-Vorgang](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) , um Eigenschaften für die neuen oder geänderten Ordner abzurufen und die Ordner auf dem Client zu aktualisieren oder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5517f-148">If you're using EWS, use the [GetFolder operation](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) to get properties on the new or changed folders and update or create the folders on the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5517f-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5517f-149">See also</span></span>

- [<span data-ttu-id="5517f-150">Postfachsynchronisierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="5517f-150">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)   
- [<span data-ttu-id="5517f-151">Synchronisieren von Elementen unter Verwendung von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="5517f-151">Synchronize items by using EWS in Exchange</span></span>](how-to-synchronize-items-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="5517f-152">Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="5517f-152">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    

