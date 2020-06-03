---
title: Durchführen seitenweiter Suchen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 64ed70e4-32eb-4c25-bfc4-43d1477296e5
description: Erfahren Sie, wie Sie Auslagerungs Suchvorgänge in ihrer verwaltete EWS-API-oder EWS-Anwendung durchführen, die auf Exchange abzielt.
localization_priority: Priority
ms.openlocfilehash: 2b608584918c936f62883b8b444d59c05c5952ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456834"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a><span data-ttu-id="16d39-103">Durchführen seitenweiter Suchen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="16d39-103">Perform paged searches by using EWS in Exchange</span></span>

<span data-ttu-id="16d39-104">Erfahren Sie, wie Sie Auslagerungs Suchvorgänge in ihrer verwaltete EWS-API-oder EWS-Anwendung durchführen, die auf Exchange abzielt.</span><span class="sxs-lookup"><span data-stu-id="16d39-104">Find out how to perform paged searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="16d39-105">Paging ist ein Feature in EWS, mit dem Sie die Größe der Ergebnisse einer Suche steuern können.</span><span class="sxs-lookup"><span data-stu-id="16d39-105">Paging is a feature in EWS that enables you to control the size of the results of a search.</span></span> <span data-ttu-id="16d39-106">Anstatt das gesamte Resultset in einer EWS-Antwort abzurufen, können Sie kleinere Sätze in mehreren EWS-Antworten abrufen.</span><span class="sxs-lookup"><span data-stu-id="16d39-106">Rather than retrieve the entire result set in one EWS response, you can retrieve smaller sets in multiple EWS responses.</span></span> <span data-ttu-id="16d39-107">Halten Sie sich beispielsweise an einen Benutzer mit 10.000 e-Mail-Nachrichten in Ihrem Posteingang.</span><span class="sxs-lookup"><span data-stu-id="16d39-107">For example, consider a user with 10,000 email messages in their Inbox.</span></span> <span data-ttu-id="16d39-108">Theoretisch könnten Sie alle 10.000-e-Mails in einer sehr großen Antwort abrufen, aber Sie können dies aus Bandbreiten-oder Leistungsgründen in mehr verwaltbare Abschnitte unterteilen.</span><span class="sxs-lookup"><span data-stu-id="16d39-108">Hypothetically, you could retrieve all 10,000 emails in one very large response, but you might want to break that up into more manageable chunks for bandwidth or performance reasons.</span></span> <span data-ttu-id="16d39-109">Paging bietet Ihnen die Tools, die genau dies tun.</span><span class="sxs-lookup"><span data-stu-id="16d39-109">Paging gives you the tools to do just that.</span></span>
  
> [!NOTE]
> <span data-ttu-id="16d39-110">Sie können zwar hypothetisch 10.000-Elemente in einer Anforderung abrufen, in Wirklichkeit ist dies jedoch aufgrund der EWS-Drosselung unwahrscheinlich.</span><span class="sxs-lookup"><span data-stu-id="16d39-110">While you can hypothetically retrieve 10,000 items in one request, in reality, this is unlikely due to EWS throttling.</span></span> <span data-ttu-id="16d39-111">Weitere Informationen finden Sie unter [EWS-Drosselung in Exchange](ews-throttling-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="16d39-111">To find out more, see [EWS throttling in Exchange](ews-throttling-in-exchange.md).</span></span> 
  
<span data-ttu-id="16d39-112">**Tabelle 1. Paging-Parameter im verwaltete EWS-API und EWS**</span><span class="sxs-lookup"><span data-stu-id="16d39-112">**Table 1. Paging parameters in the EWS Managed API and EWS**</span></span>

|<span data-ttu-id="16d39-113">**So konfigurieren oder rufen Sie den...**</span><span class="sxs-lookup"><span data-stu-id="16d39-113">**To configure or retrieve the…**</span></span>|<span data-ttu-id="16d39-114">**Verwenden Sie im verwaltete EWS-API die...**</span><span class="sxs-lookup"><span data-stu-id="16d39-114">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="16d39-115">**Verwenden Sie in EWS die...**</span><span class="sxs-lookup"><span data-stu-id="16d39-115">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16d39-116">Maximale Anzahl von Elementen oder Ordnern in einer Antwort</span><span class="sxs-lookup"><span data-stu-id="16d39-116">Maximum number of items or folders in a response</span></span>  <br/> |<span data-ttu-id="16d39-117">Der **PageSize** -Parameter für den [ItemView-Konstruktor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) oder den [folderview-Konstruktor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d39-117">The **pageSize** parameter to the [ItemView constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) or the [FolderView constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span></span> <br/> <span data-ttu-id="16d39-118">Oder:</span><span class="sxs-lookup"><span data-stu-id="16d39-118">Or</span></span>  <br/> <span data-ttu-id="16d39-119">Die [PagedView. PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="16d39-119">The [PagedView.PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="16d39-120">Das **MaxEntriesReturned** -Attribut für das [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) -Element oder das [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) -Element</span><span class="sxs-lookup"><span data-stu-id="16d39-120">The **MaxEntriesReturned** attribute on the [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="16d39-121">Ausgangspunkt in der Liste der Elemente oder Ordner</span><span class="sxs-lookup"><span data-stu-id="16d39-121">Starting point in the list of items or folders</span></span>  <br/> |<span data-ttu-id="16d39-122">Der **offsetBasePoint** -Parameter für den **ItemView** -Konstruktor oder den **folderview** -Konstruktor</span><span class="sxs-lookup"><span data-stu-id="16d39-122">The **offsetBasePoint** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="16d39-123">Oder:</span><span class="sxs-lookup"><span data-stu-id="16d39-123">Or</span></span>  <br/> <span data-ttu-id="16d39-124">Die [PagedView. OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="16d39-124">The [PagedView.OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="16d39-125">Das **Basepoint** -Attribut für das **IndexedPageItemView** -Element oder das **IndexedPageFolderView** -Element</span><span class="sxs-lookup"><span data-stu-id="16d39-125">The **BasePoint** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="16d39-126">Offset vom Ausgangspunkt</span><span class="sxs-lookup"><span data-stu-id="16d39-126">Offset from the starting point</span></span>  <br/> |<span data-ttu-id="16d39-127">Der **Offset** -Parameter für den **ItemView** -Konstruktor oder den **folderview** -Konstruktor</span><span class="sxs-lookup"><span data-stu-id="16d39-127">The **offset** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="16d39-128">Oder:</span><span class="sxs-lookup"><span data-stu-id="16d39-128">Or</span></span>  <br/> <span data-ttu-id="16d39-129">Die [PagedView. Offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="16d39-129">The [PagedView.Offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="16d39-130">Das **Offset** -Attribut für das **IndexedPageItemView** -Element oder das **IndexedPageFolderView** -Element</span><span class="sxs-lookup"><span data-stu-id="16d39-130">The **Offset** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="16d39-131">Gesamtzahl der Ergebnisse auf dem Server</span><span class="sxs-lookup"><span data-stu-id="16d39-131">Total number of results on the server</span></span>  <br/> |<span data-ttu-id="16d39-132">Die [FindItemsResults. Total count](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx) -Eigenschaft oder die [FindFoldersResults. Total count](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="16d39-132">The [FindItemsResults.TotalCount](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx) property or the [FindFoldersResults.TotalCount](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="16d39-133">Das **TotalItemsInView** -Attribut für das [RootFolder (FindItemResponseMessage)-](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) Element oder das [RootFolder (FindFolderResponseMessage)-](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) Element</span><span class="sxs-lookup"><span data-stu-id="16d39-133">The **TotalItemsInView** attribute on the [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="16d39-134">Offset des ersten Elements oder Ordners, der nicht in der aktuellen Antwort enthalten ist</span><span class="sxs-lookup"><span data-stu-id="16d39-134">Offset of first item or folder not included in current response</span></span>  <br/> |<span data-ttu-id="16d39-135">Die [FindItemsResults. NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx) -Eigenschaft oder die [FindFoldersResults. NextPageOffset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="16d39-135">The [FindItemsResults.NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx) property or the [FindFoldersResults.NextPageOffset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="16d39-136">Das **IndexedPagingOffset** -Attribut für das **RootFolder** -Element</span><span class="sxs-lookup"><span data-stu-id="16d39-136">The **IndexedPagingOffset** attribute on the **RootFolder** element</span></span>  <br/> |
|<span data-ttu-id="16d39-137">Indikator, dass die Antwort das letzte Element oder den letzten Ordner in der Liste enthält.</span><span class="sxs-lookup"><span data-stu-id="16d39-137">Indicator that response includes the last item or folder in the list</span></span>  <br/> |<span data-ttu-id="16d39-138">Die [FindItemsResults. MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) -Eigenschaft oder die [FindFoldersResults. MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="16d39-138">The [FindItemsResults.MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) property or the [FindFoldersResults.MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="16d39-139">Das **IncludesLastItemInRange** -Attribut für das **RootFolder** -Element</span><span class="sxs-lookup"><span data-stu-id="16d39-139">The **IncludesLastItemInRange** attribute on the **RootFolder** element</span></span>  <br/> |
   
## <a name="how-paging-works"></a><span data-ttu-id="16d39-140">Funktionsweise von Paging</span><span class="sxs-lookup"><span data-stu-id="16d39-140">How paging works</span></span>
<span data-ttu-id="16d39-141"><a name="bk_HowPagingWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="16d39-141"><a name="bk_HowPagingWorks"> </a></span></span>

<span data-ttu-id="16d39-142">Um zu verstehen, wie das Paging funktioniert, ist es hilfreich, die Nachrichten in einem Ordner als nebeneinander in einem Feld außerhalb Ihres Hauses nebeneinander liegenden Plakaten zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="16d39-142">To understand how paging works, it's helpful to visualize the messages in a folder as billboards lined up side by side in a field outside your house.</span></span> <span data-ttu-id="16d39-143">Einige dieser Plakate können Sie in einem magischen Fenster sehen.</span><span class="sxs-lookup"><span data-stu-id="16d39-143">You can see some of these billboards through a magical window.</span></span> <span data-ttu-id="16d39-144">Sie haben die Möglichkeit, die Größe des Fensters zu ändern (um mehr oder weniger Billboards gleichzeitig anzuzeigen) und das Fenster zu wechseln (um zu steuern, welche Billboards angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="16d39-144">You have the ability to change the size of the window (to see more or fewer billboards at once) and to move the window (to control which billboards you can see).</span></span> <span data-ttu-id="16d39-145">Bei dieser Manipulation des Fensters handelt es sich um Paging.</span><span class="sxs-lookup"><span data-stu-id="16d39-145">This manipulation of the window is paging.</span></span> 
  
<span data-ttu-id="16d39-146">Wenn Sie Ihre Anforderung an den Exchange-Server senden, geben Sie die Größe des Fensters im Hinblick auf die Anzahl der zurückzugebenden Elemente an.</span><span class="sxs-lookup"><span data-stu-id="16d39-146">When you send your request to the Exchange server, you specify the size of your window in terms of how many items to return.</span></span> <span data-ttu-id="16d39-147">Sie legen die Position des Fensters fest, indem Sie einen Anfangspunkt (entweder den Anfang der Linien oder das Ende der Position) und einen Offset von diesem Anfangspunkt angeben, der in einer Anzahl von Elementen ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="16d39-147">You set the position of the window by specifying a starting point (either the beginning of the line or the end of the line) and an offset from that starting point, expressed in a number of items.</span></span> <span data-ttu-id="16d39-148">Der Anfang des Fensters ist die Anzahl der Elemente, die vom Offset vom Ausgangspunkt angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="16d39-148">The beginning of the window is the number of items specified by the offset from the starting point.</span></span>
  
<span data-ttu-id="16d39-149">Wo Paging wird ein bisschen interessanter ist in der Antwort des Servers, und wie Ihre Anwendung diese Antwort verwenden können, um die nächste Anforderung zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="16d39-149">Where paging gets a bit more interesting is in the server's response, and how your application can use that response to shape its next request.</span></span> <span data-ttu-id="16d39-150">Der Server enthält drei Informationen, die Sie verwenden können, um zu bestimmen, wie Sie Ihr "Fenster" für Ihre nächste Anforderung konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="16d39-150">The server gives you three pieces of information that you can use to determine how to configure your "window" for your next request:</span></span> 
  
- <span data-ttu-id="16d39-151">Gibt an, ob die Ergebnisse in der Antwort das letzte Element in der Gesamtergebnismenge auf dem Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="16d39-151">Whether the results in the response include the last item in the overall result set on the server.</span></span>
    
- <span data-ttu-id="16d39-152">Die Gesamtzahl der Elemente in der Ergebnisgruppe auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="16d39-152">The total number of items in the result set on the server.</span></span>
    
- <span data-ttu-id="16d39-153">Was der nächste Offsetwert sein soll, wenn Sie das Fenster auf das nächste Element im Resultset heraufsetzen möchten, das in der aktuellen Antwort nicht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="16d39-153">What the next offset value should be, if you want to advance your window to the next item in the result set that isn't included in the current response.</span></span>
    
<span data-ttu-id="16d39-154">Lassen Sie uns ein einfaches Beispiel betrachten.</span><span class="sxs-lookup"><span data-stu-id="16d39-154">Let's look at a simple example.</span></span> <span data-ttu-id="16d39-155">Stellen Sie sich einen Posteingang mit 15 Nachrichten vor.</span><span class="sxs-lookup"><span data-stu-id="16d39-155">Imagine an Inbox with 15 messages in it.</span></span> <span data-ttu-id="16d39-156">Ihre Anwendung sendet eine anfängliche Anforderung zum Abrufen von maximal 10 Elementen, beginnend am Anfang der Liste der Nachrichten (sodass der Offset NULL ist).</span><span class="sxs-lookup"><span data-stu-id="16d39-156">Your application sends an initial request to retrieve a maximum of 10 items, starting at the beginning of the list of messages (so the offset is zero).</span></span> <span data-ttu-id="16d39-157">Der Server antwortet mit den ersten 10 Nachrichten und gibt an, dass die Antwort nicht das letzte Element enthält, dass es insgesamt 15 Elemente gibt und dass der nächste Offset 10 sein sollte.</span><span class="sxs-lookup"><span data-stu-id="16d39-157">The server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10.</span></span>
  
<span data-ttu-id="16d39-158">**Abbildung 1. Anfordern von 10 Elementen bei Offset 0 vom Anfang einer Liste mit 15 Elementen**</span><span class="sxs-lookup"><span data-stu-id="16d39-158">**Figure 1. Requesting 10 items at offset 0 from the beginning of a list of 15 items**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 0 am dem Anfang einer Liste mit 15 Elementen.](media/Ex15_PagedSearch_FirstPage.png)
  
<span data-ttu-id="16d39-160">Die Anwendung sendet dann die gleiche Anforderung erneut an den Server, wobei die einzige Änderung darin besteht, dass der Offset jetzt 10 ist.</span><span class="sxs-lookup"><span data-stu-id="16d39-160">Your application then resends the same request to the server, with the only change being that the offset is now 10.</span></span> <span data-ttu-id="16d39-161">Der Server gibt die letzten fünf Elemente zurück und gibt an, dass die Antwort das letzte Element enthält, dass es insgesamt 15 Elemente gibt und dass der nächste Offset 15 sein sollte (obwohl Sie natürlich das Ende erreicht haben, gibt es keinen nächsten Offset.)</span><span class="sxs-lookup"><span data-stu-id="16d39-161">The server returns the last five items, and indicates that the response does include the last item, that there are a total of 15 items, and that the next offset should be 15 (though of course, you've reached the end, so there won't be a next offset.)</span></span>
  
<span data-ttu-id="16d39-162">**Abbildung 2. Anfordern von 10 Elementen bei Offset 10 vom Anfang einer Liste mit 15 Elementen**</span><span class="sxs-lookup"><span data-stu-id="16d39-162">**Figure 2. Requesting 10 items at offset 10 from the beginning of a list of 15 items**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 0 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Anfang der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a><span data-ttu-id="16d39-164">Entwurfsüberlegungen für das Paging</span><span class="sxs-lookup"><span data-stu-id="16d39-164">Design considerations for paging</span></span>
<span data-ttu-id="16d39-165"><a name="bk_DesignConsiderations"> </a></span><span class="sxs-lookup"><span data-stu-id="16d39-165"><a name="bk_DesignConsiderations"> </a></span></span>

<span data-ttu-id="16d39-166">Das Beste aus dem Paging in Ihrer Anwendung herauszunehmen, erfordert einige Überlegungen.</span><span class="sxs-lookup"><span data-stu-id="16d39-166">Making the most out of paging in your application does require some consideration.</span></span> <span data-ttu-id="16d39-167">Wie groß ist beispielsweise die Größe des Fensters?</span><span class="sxs-lookup"><span data-stu-id="16d39-167">For example, how large do you make your "window"?</span></span> <span data-ttu-id="16d39-168">Was tun Sie, wenn sich die Ergebnisse auf dem Server ändern, während Sie Ihr "Fenster" verschieben?</span><span class="sxs-lookup"><span data-stu-id="16d39-168">What do you do if the results on the server change while you're moving your "window"?</span></span>
  
### <a name="determine-the-size-of-your-window"></a><span data-ttu-id="16d39-169">Bestimmen der Größe des Fensters</span><span class="sxs-lookup"><span data-stu-id="16d39-169">Determine the size of your window</span></span>

<span data-ttu-id="16d39-170">Es gibt keine maximale Anzahl von Einträgen in einer Größe, die alle Anwendungen verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="16d39-170">There is no "one-size-fits-all" maximum number of entries that all applications should use.</span></span> <span data-ttu-id="16d39-171">Die Bestimmung der Nummer, die für Ihre Anwendung richtig ist, hängt von verschiedenen Faktoren ab.</span><span class="sxs-lookup"><span data-stu-id="16d39-171">Determining the number that's right for your application depends on several different factors.</span></span> <span data-ttu-id="16d39-172">Es ist jedoch hilfreich, die folgenden Richtlinien im Hinterkopf zu behalten:</span><span class="sxs-lookup"><span data-stu-id="16d39-172">However, it's helpful to keep the following guidelines in mind:</span></span>
  
- <span data-ttu-id="16d39-173">Standardmäßig schränkt Exchange die maximale Anzahl von Elementen ein, die in einer einzigen Anforderung an 1000 zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="16d39-173">By default, Exchange limits the maximum number of items that can be returned in a single request to 1000.</span></span>
    
- <span data-ttu-id="16d39-174">Wenn Sie die maximale Anzahl von Einträgen auf eine größere Zahl festlegen, müssen weniger Anforderungen zum Abrufen aller Elemente gesendet werden, sodass die Antworten nicht länger gewartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="16d39-174">Setting the maximum number of entries to a larger number results in having to send fewer requests to get all items, at the cost of having to wait longer for responses.</span></span>
    
- <span data-ttu-id="16d39-175">Wenn Sie die maximale Anzahl von Einträgen auf eine kleinere Zahl festlegen, erhalten Sie schnellere Antwortzeiten, wobei mehr Anforderungen zum Abrufen aller Elemente gesendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="16d39-175">Setting the maximum number of entries to a smaller number results in quicker response times, at the cost of having to send more requests to get all items.</span></span>
    
### <a name="handling-changes-to-the-result-set"></a><span data-ttu-id="16d39-176">Behandeln von Änderungen an der Ergebnismenge</span><span class="sxs-lookup"><span data-stu-id="16d39-176">Handling changes to the result set</span></span>

<span data-ttu-id="16d39-177">Im einfachen Beispiel weiter oben in diesem Artikel ist die Anzahl der Elemente im Posteingang des Benutzers konstant geblieben.</span><span class="sxs-lookup"><span data-stu-id="16d39-177">In the simple example earlier in this article, the number of items in the user's Inbox remained constant.</span></span> <span data-ttu-id="16d39-178">In Wirklichkeit kann sich die Anzahl der Elemente in einem Posteingang jedoch häufig ändern.</span><span class="sxs-lookup"><span data-stu-id="16d39-178">However, in reality, the number of items in an Inbox can change frequently.</span></span> <span data-ttu-id="16d39-179">Neue Nachrichten können eintreffen, und Elemente können jederzeit gelöscht oder verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="16d39-179">New messages can arrive and items can be deleted or moved at any time.</span></span> <span data-ttu-id="16d39-180">Wie wirkt sich dies jedoch auf die Auslagerungsdatei aus?</span><span class="sxs-lookup"><span data-stu-id="16d39-180">But how does this impact paging?</span></span> <span data-ttu-id="16d39-181">Lassen Sie uns das frühere Beispielszenario ändern, um es herauszufinden.</span><span class="sxs-lookup"><span data-stu-id="16d39-181">Let's modify the earlier example scenario to find out.</span></span>
  
<span data-ttu-id="16d39-182">Wir beginnen erneut mit den 15 Elementen im Posteingang des Benutzers und senden die gleiche anfängliche Anforderung.</span><span class="sxs-lookup"><span data-stu-id="16d39-182">We'll start again with the 15 items in the user's Inbox, and send the same initial request.</span></span> <span data-ttu-id="16d39-183">Wie zuvor antwortet der Server mit den ersten 10 Nachrichten und gibt an, dass die Antwort nicht das letzte Element enthält, dass insgesamt 15 Elemente vorhanden sind und dass der nächste Offset 10 sein sollte, wie in Abbildung 1 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="16d39-183">As before, the server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10, as shown in Figure 1.</span></span>
  
<span data-ttu-id="16d39-184">Während Ihre Anwendung diese 10 Elemente verarbeitet, kommt eine neue Nachricht im Posteingang an und wird dem Resultset auf dem Server hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="16d39-184">Now, while your application is processing those 10 items, a new message arrives in the Inbox and is added to the result set on the server.</span></span> <span data-ttu-id="16d39-185">Die Anwendung sendet die gleiche Anforderung erneut an den Server (nur mit dem Offset auf 10).</span><span class="sxs-lookup"><span data-stu-id="16d39-185">Your application resends the same request to the server (only with the offset set to 10).</span></span> <span data-ttu-id="16d39-186">Dieses Mal erhält der Server sechs Elemente zurück und gibt an, dass insgesamt 16 Elemente in der Ergebnisgruppe vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="16d39-186">This time the server gets back six items, and indicates that there are a total of 16 items in the result set.</span></span>
  
<span data-ttu-id="16d39-187">An diesem Punkt Fragen Sie sich möglicherweise, ob dies sogar ein Problem ist.</span><span class="sxs-lookup"><span data-stu-id="16d39-187">At this point you might be wondering if this is even a problem.</span></span> <span data-ttu-id="16d39-188">Immerhin haben Sie 16 Elemente zurück über die beiden Antworten, also warum all die Aufregung?</span><span class="sxs-lookup"><span data-stu-id="16d39-188">After all, you got 16 items back over the two responses, so why all the fuss?</span></span> <span data-ttu-id="16d39-189">Die Antwort hängt davon ab, an welcher Stelle in der Liste das neue Element eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="16d39-189">The answer depends on where in the list the new item is placed.</span></span> <span data-ttu-id="16d39-190">Wenn die Liste so sortiert ist, dass die ältesten Elemente (nach Empfangsdatum/-Uhrzeit) zuerst vorhanden sind, gibt es in diesem Szenario keinen Anlass zur Besorgnis.</span><span class="sxs-lookup"><span data-stu-id="16d39-190">If the list is sorted so that the oldest items (by received date/time) are first, there's no cause for concern in this scenario.</span></span> <span data-ttu-id="16d39-191">Das neue Element wird am Ende der Liste eingefügt und in die zweite Antwort aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="16d39-191">The new item will be placed at the end of the list, and will be included in the second response.</span></span>
  
<span data-ttu-id="16d39-192">**Abbildung 3. Anfordern von 10 Elementen bei Offset 10 vom Anfang einer Liste mit 16 Elementen, wobei das 16. Element in der Liste neu ist**</span><span class="sxs-lookup"><span data-stu-id="16d39-192">**Figure 3. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the 16th item in the list being new**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Ende der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
<span data-ttu-id="16d39-194">Wenn die Liste so sortiert ist, dass die neuesten Elemente zuerst sind, handelt es sich um eine andere Geschichte.</span><span class="sxs-lookup"><span data-stu-id="16d39-194">If the list is sorted so that the newest items are first, it's a different story.</span></span> <span data-ttu-id="16d39-195">In diesem Fall wäre das erste Element in der zweiten Anforderung das letzte Element aus der vorherigen Anforderung und die restlichen fünf Elemente aus dem ursprünglichen 15.</span><span class="sxs-lookup"><span data-stu-id="16d39-195">In this case, the first item in the second request would be the last item from the previous request plus the remaining five items from the original 15.</span></span> <span data-ttu-id="16d39-196">Um es in Bezug auf unser imaginäres magisches Fenster zu setzen, haben Sie die Position Ihres Fensters um 10 verschoben, aber auch die Plakate wurden um 1 verschoben.</span><span class="sxs-lookup"><span data-stu-id="16d39-196">To put it in terms of our imaginary magical window, you shifted your window's position by 10, but the billboards themselves also shifted by 1.</span></span>
  
<span data-ttu-id="16d39-197">**Abbildung 4. Anfordern von 10 Elementen bei Offset 10 vom Anfang einer Liste mit 16 Elementen, wobei das erste Element in der Liste neu ist**</span><span class="sxs-lookup"><span data-stu-id="16d39-197">**Figure 4. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the first item in the list being new**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Anfang der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
<span data-ttu-id="16d39-199">Eine Möglichkeit zum Erkennen einer Änderung an den Ergebnissen auf dem Server besteht darin, das Konzept eines Ankerelements zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="16d39-199">One way to detect a change to the results on the server is to use the concept of an anchor item.</span></span> <span data-ttu-id="16d39-200">Ein Ankerelement ist ein zusätzliches Element in der Antwort, das nicht zusammen mit den restlichen Ergebnissen verarbeitet wird, sondern zum Vergleichen mit den nächsten Ergebnissen verwendet wird, um zu ermitteln, ob die Elemente selbst verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="16d39-200">An anchor item is an additional item in your response that is not processed along with the rest of the results, but is used to compare with the next results to see if the items themselves have shifted.</span></span> <span data-ttu-id="16d39-201">Wenn die Anwendung eine Fenstergröße von 10 verwendet, legen Sie die maximale Anzahl von Elementen, die auf 11 zurückgegeben werden sollen, in unserem einfachen Beispiel fest.</span><span class="sxs-lookup"><span data-stu-id="16d39-201">Building again on our simple example, if your application is using a "window" size of 10, you actually set the maximum number of items to return to 11.</span></span> <span data-ttu-id="16d39-202">Ihre Anwendung verarbeitet die ersten 10 Elemente in der Antwort wie gewohnt.</span><span class="sxs-lookup"><span data-stu-id="16d39-202">Your application processes the first 10 items in the response as usual.</span></span> <span data-ttu-id="16d39-203">Für das letzte Element speichern Sie den Bezeichner des Elements als Anker und geben dann die nächste Anforderung mit einem Offset von 10 aus.</span><span class="sxs-lookup"><span data-stu-id="16d39-203">For the last item, you save the item's identifier as an anchor, then issue the next request with an offset of 10.</span></span> <span data-ttu-id="16d39-204">Wenn sich die Daten nicht geändert haben, sollte das erste Element in der zweiten Antwort eine Element-ID aufweisen, die mit dem Anker übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="16d39-204">If the data has not changed, the first item in the second response should have an item identifier that matches the anchor.</span></span> <span data-ttu-id="16d39-205">Wenn die Element-IDs nicht übereinstimmen, wissen Sie, dass die Daten entfernt oder in die Teile der Liste eingefügt wurden, die Sie bereits "ausgelagert" haben.</span><span class="sxs-lookup"><span data-stu-id="16d39-205">If the item identifiers don't match, you know that the data has been removed or inserted in the parts of the list you have already "paged" over.</span></span>
  
<span data-ttu-id="16d39-206">Selbst wenn Sie wissen, dass die Daten geändert wurden, müssen Sie dennoch entscheiden, wie Sie reagieren sollen.</span><span class="sxs-lookup"><span data-stu-id="16d39-206">Even when you know that the data has changed, you still need to decide how to react.</span></span> <span data-ttu-id="16d39-207">Für diese Frage gibt es auch keine One-size-fits-all-Antwort.</span><span class="sxs-lookup"><span data-stu-id="16d39-207">There isn't a one-size-fits-all answer for this question either.</span></span> <span data-ttu-id="16d39-208">Ihre Aktionen hängen von der Art der Anwendung und der Wichtigkeit der Erfassung aller Elemente ab.</span><span class="sxs-lookup"><span data-stu-id="16d39-208">Your actions will depend on the nature of your application and how critical it is to capture all items.</span></span> <span data-ttu-id="16d39-209">Sie können ihn möglicherweise ganz ignorieren, den Prozess von Anfang oder zurückverfolgen und versuchen zu ermitteln, wo die Änderung vorging.</span><span class="sxs-lookup"><span data-stu-id="16d39-209">You might ignore it altogether, restart the process from the beginning, or back track and try to detect where the change happened.</span></span>
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a><span data-ttu-id="16d39-210">Beispiel: Durchführen einer ausgelagerten Suche mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="16d39-210">Example: Perform a paged search by using the EWS Managed API</span></span>
<span data-ttu-id="16d39-211"><a name="bk_PagedSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="16d39-211"><a name="bk_PagedSearchEWSMA"> </a></span></span>

<span data-ttu-id="16d39-212">Das Paging wird von den folgenden verwaltete EWS-API-Methoden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="16d39-212">Paging is supported by the following EWS Managed API methods:</span></span>
  
- [<span data-ttu-id="16d39-213">ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="16d39-213">ExchangeService.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="16d39-214">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="16d39-214">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="16d39-215">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="16d39-215">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="16d39-216">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="16d39-216">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="16d39-217">Wenn Sie die verwaltete EWS-API verwenden, konfiguriert ihre Anwendung das Paging mit der [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) -oder der [folderview](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) -Klasse und empfängt Informationen vom Server zum Paging von der [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) -oder der [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="16d39-217">If you are using the EWS Managed API, your application configures paging with the [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) or [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) class and receives information from the server regarding paging from the [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) or [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) class.</span></span> 
  
<span data-ttu-id="16d39-218">Im folgenden Beispiel werden alle Elemente in einem Ordner mithilfe einer ausgelagerten Suche abgerufen, die fünf Elemente in jeder Antwort zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="16d39-218">The following example retrieves all the items in a folder using a paged search that returns five items in each response.</span></span> <span data-ttu-id="16d39-219">Außerdem ruft es ein zusätzliches Element ab, das als Anker dient, um Änderungen an den Ergebnissen auf dem Server zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="16d39-219">It also retrieves an additional item to serve as an anchor to detect changes to the results on the server.</span></span> 
  
<span data-ttu-id="16d39-220">In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="16d39-220">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void PageSearchItems(ExchangeService service, WellKnownFolderName folder)
{
    int pageSize = 5;
    int offset = 0;
    // Request one more item than your actual pageSize.
    // This will be used to detect a change to the result
    // set while paging.
    ItemView view = new ItemView(pageSize + 1, offset);
    view.PropertySet = new PropertySet(ItemSchema.Subject);
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    view.Traversal = ItemTraversal.Shallow;
    bool moreItems = true;
    ItemId anchorId = null;
    while (moreItems)
    {
        try
        {
            FindItemsResults<Item> results = service.FindItems(folder, view);
            moreItems = results.MoreAvailable;
            if (moreItems &amp;&amp; anchorId != null)
            {
                // Check the first result to make sure it matches
                // the last result (anchor) from the previous page.
                // If it doesn't, that means that something was added
                // or deleted since you started the search.
                if (results.Items.First<Item>().Id != anchorId)
                {
                    Console.WriteLine("The collection has changed while paging. Some results may be missed.");
                }
            }
            if (moreItems)
                view.Offset += pageSize;
            anchorId = results.Items.Last<Item>().Id;
            // Because you're including an additional item on the end of your results
            // as an anchor, you don't want to display it.
            // Set the number to loop as the smaller value between
            // the number of items in the collection and the page size.
            int displayCount = results.Items.Count > pageSize ? pageSize : results.Items.Count;
            for (int i = 0; i < displayCount; i++)
            {
                Item item = results.Items[i];
                Console.WriteLine("Subject: {0}", item.Subject);
                Console.WriteLine("Id: {0}\n", item.Id.ToString());
            }
        }
        catch (Exception ex)
        {
            Console.WriteLine("Exception while paging results: {0}", ex.Message);
        }
    }
}
```

## <a name="example-perform-a-paged-search-by-using-ews"></a><span data-ttu-id="16d39-221">Beispiel: Durchführen einer Seiten weisen Suche mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="16d39-221">Example: Perform a paged search by using EWS</span></span>
<span data-ttu-id="16d39-222"><a name="bk_PagedSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="16d39-222"><a name="bk_PagedSearchEWS"> </a></span></span>

<span data-ttu-id="16d39-223">Paging wird von den folgenden EWS-Vorgängen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="16d39-223">Paging is supported by the following EWS operations:</span></span>
  
- [<span data-ttu-id="16d39-224">FindFolder</span><span class="sxs-lookup"><span data-stu-id="16d39-224">FindFolder</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="16d39-225">FindItem</span><span class="sxs-lookup"><span data-stu-id="16d39-225">FindItem</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
<span data-ttu-id="16d39-226">Wenn Sie EWS verwenden, konfiguriert ihre Anwendung das Paging mit dem [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) -Element oder dem [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) -Element und empfängt Informationen vom Server hinsichtlich der Paginierung vom [RootFolder (FindItemResponseMessage)-](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) Element oder dem [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) -Element.</span><span class="sxs-lookup"><span data-stu-id="16d39-226">If you're using EWS, your application configures paging with the [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element and receives information from the server regarding paging from the [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="16d39-227">In diesem Anforderungs Beispiel wird eine **FindItem** -Anforderung für maximal sechs Elemente gesendet, beginnend bei einem Offset von NULL vom Anfang der Liste der Elemente im Posteingang des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="16d39-227">In this request example, a **FindItem** request is sent for a maximum of six items, starting at an offset of zero from the beginning of the list of items in the user's Inbox.</span></span> 
  
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
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="6" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="16d39-228">Der Server gibt die folgende Antwort zurück, die sechs Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="16d39-228">The server returns the following response, which contains six items.</span></span> <span data-ttu-id="16d39-229">Die Antwort weist außerdem darauf hin, dass es insgesamt acht Elemente in den Ergebnissen auf dem Server gibt und dass das letzte Element in der Ergebnisliste in dieser Antwort nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="16d39-229">The response also indicates that there are a total of eight items in the results on the server, and that the last item in the results list is not present in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
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
          <m:RootFolder IndexedPagingOffset="6" TotalItemsInView="8" IncludesLastItemInRange="false">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Query</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Update</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Planning resources</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Timeline</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>For your perusal</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="16d39-230">In diesem Beispiel wird dieselbe Anforderung gesendet, dieses Mal wird jedoch das **Offset** -Attribut in fünf geändert, was darauf hinweist, dass der Server höchstens sechs Elemente zurückgeben soll, beginnend mit Offset 5 vom Anfang an.</span><span class="sxs-lookup"><span data-stu-id="16d39-230">In this example, the same request is sent, but this time, the **Offset** attribute is changed to five, which indicates that the server should return at most six items starting at offset five from the beginning.</span></span> 
  
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
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="6" Offset="5" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="16d39-231">Der Server sendet die folgende Antwort, die drei Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="16d39-231">The server sends the following response, which contains three items.</span></span> <span data-ttu-id="16d39-232">Die Antwort weist außerdem darauf hin, dass die Gesamtzahl der Elemente in den Ergebnissen auf dem Server immer noch acht ist und dass das letzte Element in der Ergebnisliste in dieser Antwort enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="16d39-232">The response also indicates that the total number of items in the results on the server is still eight, and that the last item in the results list is included in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
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
          <m:RootFolder IndexedPagingOffset="8" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting notes</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>This cat is hilarious!</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="16d39-233">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16d39-233">See also</span></span>


- [<span data-ttu-id="16d39-234">Suche und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="16d39-234">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="16d39-235">ExchangeService.FindFolders-Methode</span><span class="sxs-lookup"><span data-stu-id="16d39-235">ExchangeService.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="16d39-236">ExchangeService.FindItems-Methode</span><span class="sxs-lookup"><span data-stu-id="16d39-236">ExchangeService.FindItems method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="16d39-237">Folder.FindFolders-Methode</span><span class="sxs-lookup"><span data-stu-id="16d39-237">Folder.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="16d39-238">Folder.FindFolders-Methode</span><span class="sxs-lookup"><span data-stu-id="16d39-238">Folder.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="16d39-239">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16d39-239">FindFolder operation</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="16d39-240">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16d39-240">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [<span data-ttu-id="16d39-241">EWS-Einschränkung in Exchange</span><span class="sxs-lookup"><span data-stu-id="16d39-241">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    

