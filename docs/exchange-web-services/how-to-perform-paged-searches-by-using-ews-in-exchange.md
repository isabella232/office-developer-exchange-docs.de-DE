---
title: Seitensuchen mithilfe von EWS in Exchange durchführen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 64ed70e4-32eb-4c25-bfc4-43d1477296e5
description: Lernen Sie, wie Sie Seitensuchen in Ihrem verwalteten EWS-API oder EWS-Anwendung, die auf Exchange zielen, durchführen können.
localization_priority: Priority
ms.openlocfilehash: fa36a2ce77150f29e5a62876138c9693a3b4ab1f
ms.sourcegitcommit: 37d4ecd4f469690ba1de87baad2f2f58c40c96ba
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "49348822"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a><span data-ttu-id="55ee2-103">Seitensuchen mithilfe von EWS in Exchange durchführen</span><span class="sxs-lookup"><span data-stu-id="55ee2-103">Perform paged searches by using EWS in Exchange</span></span>

<span data-ttu-id="55ee2-104">Lernen Sie, wie Sie Seitensuchen in Ihrem verwalteten EWS-API oder EWS-Anwendung, die auf Exchange zielen, durchführen können.</span><span class="sxs-lookup"><span data-stu-id="55ee2-104">Find out how to perform paged searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="55ee2-105">Das Paging ist ein Feature in EWS, das es Ihnen ermöglicht, die Größe der Ergebnisse einer Suche zu steuern.</span><span class="sxs-lookup"><span data-stu-id="55ee2-105">Paging is a feature in EWS that enables you to control the size of the results of a search.</span></span> <span data-ttu-id="55ee2-106">Statt das ganze Resultset in einer EWS-Antwort abzurufen, können Sie kleinere Sets in mehreren EWS-Antworten abrufen.</span><span class="sxs-lookup"><span data-stu-id="55ee2-106">Rather than retrieve the entire result set in one EWS response, you can retrieve smaller sets in multiple EWS responses.</span></span> <span data-ttu-id="55ee2-107">Erwägen Sie z.B. einen Benutzer, der 10 000 Emails in seinem Posteingang hat.</span><span class="sxs-lookup"><span data-stu-id="55ee2-107">For example, consider a user with 10,000 email messages in their Inbox.</span></span> <span data-ttu-id="55ee2-108">Hypothetisch könnten Sie alle 10 000 Emails in einer einzigen sehr großen Antwort abrufen, Sie könnten es jedoch in mehrere übersichtlichere Teile trennen wollen, um eine bessere Bandbreite und Leistung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="55ee2-108">Hypothetically, you could retrieve all 10,000 emails in one very large response, but you might want to break that up into more manageable chunks for bandwidth or performance reasons.</span></span> <span data-ttu-id="55ee2-109">Das Paging bietet Ihnen die Tools um genau das machen zu können.</span><span class="sxs-lookup"><span data-stu-id="55ee2-109">Paging gives you the tools to do just that.</span></span>
  
> [!NOTE]
> <span data-ttu-id="55ee2-110">Sie können zwar hypothetisch 10 000 Elemente in einer Anforderung abrufen, tatsächlich ist es jedoch wegen der EWS-Drosselung unwahrscheinlich.</span><span class="sxs-lookup"><span data-stu-id="55ee2-110">While you can hypothetically retrieve 10,000 items in one request, in reality, this is unlikely due to EWS throttling.</span></span> <span data-ttu-id="55ee2-111">Weiter Informationen finden Sie unter [EWS-Drosselung in Exchange](ews-throttling-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="55ee2-111">To find out more, see [EWS throttling in Exchange](ews-throttling-in-exchange.md).</span></span> 
  
<span data-ttu-id="55ee2-112">**Tabelle 1. Das Paging in der verwalteten EWS-API und EWS**</span><span class="sxs-lookup"><span data-stu-id="55ee2-112">**Table 1. Paging parameters in the EWS Managed API and EWS**</span></span>

|<span data-ttu-id="55ee2-113">**Um die...** zu konfigurieren und abzurufen</span><span class="sxs-lookup"><span data-stu-id="55ee2-113">**To configure or retrieve the…**</span></span>|<span data-ttu-id="55ee2-114">**Verwalten Sie in der verwalteten EWS-API...**</span><span class="sxs-lookup"><span data-stu-id="55ee2-114">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="55ee2-115">**Verwalten Sie in EWS...**</span><span class="sxs-lookup"><span data-stu-id="55ee2-115">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="55ee2-116">Maximale Anzahl von Elementen oder Ordnern in einer Antwort</span><span class="sxs-lookup"><span data-stu-id="55ee2-116">Maximum number of items or folders in a response</span></span>  <br/> |<span data-ttu-id="55ee2-117">Die **pageSize**-Parameter zum [ItemView-Konstruktor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) oder dem [FolderView-Konstruktor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55ee2-117">The **pageSize** parameter to the [ItemView constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) or the [FolderView constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span></span> <br/> <span data-ttu-id="55ee2-118">Oder</span><span class="sxs-lookup"><span data-stu-id="55ee2-118">Or</span></span>  <br/> <span data-ttu-id="55ee2-119">Die [PagedView.PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx)-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55ee2-119">The [PagedView.PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="55ee2-120">Das **MaxEntriesReturned**-Attribut auf dem [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)-Element oder das [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)-Element</span><span class="sxs-lookup"><span data-stu-id="55ee2-120">The **MaxEntriesReturned** attribute on the [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="55ee2-121">Ausgangspunkt in der Liste der Elemente oder Ordner</span><span class="sxs-lookup"><span data-stu-id="55ee2-121">Starting point in the list of items or folders</span></span>  <br/> |<span data-ttu-id="55ee2-122">Die **offsetBasePoint**-Parameter zum **ItemView**-Konstruktor oder dem **FolderView**-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="55ee2-122">The **offsetBasePoint** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="55ee2-123">Oder</span><span class="sxs-lookup"><span data-stu-id="55ee2-123">Or</span></span>  <br/> <span data-ttu-id="55ee2-124">Die [PagedView.OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx)-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55ee2-124">The [PagedView.OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="55ee2-125">Das **BasePoint**-Attribut auf dem **IndexedPageItemView**-Element oder das **IndexedPageFolderView**-Element</span><span class="sxs-lookup"><span data-stu-id="55ee2-125">The **BasePoint** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="55ee2-126">Offset vom Ausgangspunkt</span><span class="sxs-lookup"><span data-stu-id="55ee2-126">Offset from the starting point</span></span>  <br/> |<span data-ttu-id="55ee2-127">Das **Offset**-Parameter zum **ItemView**-Konstruktor oder dem **FolderView**-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="55ee2-127">The **offset** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="55ee2-128">Oder</span><span class="sxs-lookup"><span data-stu-id="55ee2-128">Or</span></span>  <br/> <span data-ttu-id="55ee2-129">Die [PagedView.Offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx)-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55ee2-129">The [PagedView.Offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="55ee2-130">Das **Offset**-Attribut auf dem **IndexedPageItemView**-Element oder das **IndexedPageFolderView**-Element</span><span class="sxs-lookup"><span data-stu-id="55ee2-130">The **Offset** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="55ee2-131">Gesamtnummer der Ergebnisse auf dem Server</span><span class="sxs-lookup"><span data-stu-id="55ee2-131">Total number of results on the server</span></span>  <br/> |<span data-ttu-id="55ee2-132">Die [FindItemsResults.TotalCount](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx)-Eigenschaft oder die [FindFoldersResults.TotalCount](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx)-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55ee2-132">The [FindItemsResults.TotalCount](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx) property or the [FindFoldersResults.TotalCount](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="55ee2-133">Das **TotalItemsInView**-Attribut auf dem [RootFolder(FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx)-Element oder dem [RootFolder(FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)-Element</span><span class="sxs-lookup"><span data-stu-id="55ee2-133">The **TotalItemsInView** attribute on the [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="55ee2-134">Offset des ersten Elements oder Ordners ist nicht in der aktuellen Antwort enthalten</span><span class="sxs-lookup"><span data-stu-id="55ee2-134">Offset of first item or folder not included in current response</span></span>  <br/> |<span data-ttu-id="55ee2-135">Die [FindItemsResults.NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx)-Eigenschaft oder die [FindFoldersResults.NextPageOffset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx)-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55ee2-135">The [FindItemsResults.NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx) property or the [FindFoldersResults.NextPageOffset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="55ee2-136">Das **IndexedPagingOffset**-Attribut auf dem **RootFolder**-Element</span><span class="sxs-lookup"><span data-stu-id="55ee2-136">The **IndexedPagingOffset** attribute on the **RootFolder** element</span></span>  <br/> |
|<span data-ttu-id="55ee2-137">Indikator, dass die Antwort das letzte Element oder den letzten Ordner in der Liste enthält</span><span class="sxs-lookup"><span data-stu-id="55ee2-137">Indicator that response includes the last item or folder in the list</span></span>  <br/> |<span data-ttu-id="55ee2-138">Die [FindItemsResults.MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx)-Eigenschaft oder die [FindFoldersResults.MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx)-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55ee2-138">The [FindItemsResults.MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) property or the [FindFoldersResults.MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="55ee2-139">Das **IncludesLastItemInRange**-Attribut auf dem **RootFolder**-Element</span><span class="sxs-lookup"><span data-stu-id="55ee2-139">The **IncludesLastItemInRange** attribute on the **RootFolder** element</span></span>  <br/> |
   
## <a name="how-paging-works"></a><span data-ttu-id="55ee2-140">Funktionsweise des Pagings</span><span class="sxs-lookup"><span data-stu-id="55ee2-140">How paging works</span></span>
<span data-ttu-id="55ee2-141"><a name="bk_HowPagingWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="55ee2-141"><a name="bk_HowPagingWorks"> </a></span></span>

<span data-ttu-id="55ee2-142">Um zu verstehen, wie das Paging funktioniert, ist es hilfreich die Nachrichten in einem Ordner als nebeneinander angeordnete Billboards in einem Feld außerhalb Ihres Hauses zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="55ee2-142">To understand how paging works, it's helpful to visualize the messages in a folder as billboards lined up side by side in a field outside your house.</span></span> <span data-ttu-id="55ee2-143">Sie können einige dieser Billboards durch ein magisches Fenster sehen.</span><span class="sxs-lookup"><span data-stu-id="55ee2-143">You can see some of these billboards through a magical window.</span></span> <span data-ttu-id="55ee2-144">Sie können die Größe des Fensters ändern (um eine größere oder kleinere Anzahl der Billboards zu sehen) und Sie können das Fenster verlagern (um zu steuern, welche Billboards Sie sehen und welche nicht).</span><span class="sxs-lookup"><span data-stu-id="55ee2-144">You have the ability to change the size of the window (to see more or fewer billboards at once) and to move the window (to control which billboards you can see).</span></span> <span data-ttu-id="55ee2-145">Diese Manipulation des Fensters ist das Paging.</span><span class="sxs-lookup"><span data-stu-id="55ee2-145">This manipulation of the window is paging.</span></span> 
  
<span data-ttu-id="55ee2-146">Wenn Sie Ihre Anforderung an den Exchange-Server senden, spezifizieren Sie die Größe Ihres Fensters im Hinblick auf die Zahl der Elemente, die zurückgesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55ee2-146">When you send your request to the Exchange server, you specify the size of your window in terms of how many items to return.</span></span> <span data-ttu-id="55ee2-147">Sie bestimmen die Position des Fensters, indem Sie einen Ausgangspunkt bestimmen (entweder den Anfang der Zeile oder das Ende der Zeile) und ein Offset von diesem Ausgangspunkt, der in einer Nummer von Elementen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="55ee2-147">You set the position of the window by specifying a starting point (either the beginning of the line or the end of the line) and an offset from that starting point, expressed in a number of items.</span></span> <span data-ttu-id="55ee2-148">Der Anfang des Fensters ist die Nummer der Elemente, die durch den Offset vom Ausgangspunkt bestimmt wurden.</span><span class="sxs-lookup"><span data-stu-id="55ee2-148">The beginning of the window is the number of items specified by the offset from the starting point.</span></span>
  
<span data-ttu-id="55ee2-149">Das Paging fängt an ein bisschen spannender zu sein, wenn es um die Antwort des Servers geht, und darum, wie Ihre Anwendung diese Antwort verwenden kann, um ihre nächste Anforderung zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="55ee2-149">Where paging gets a bit more interesting is in the server's response, and how your application can use that response to shape its next request.</span></span> <span data-ttu-id="55ee2-150">Der Server stellt Ihnen drei Informationen bereit, die Sie dazu verwenden können, um zu bestimmen, wie Ihr „Fenster“ für Ihre nächste Anforderung konfiguriert werden soll:</span><span class="sxs-lookup"><span data-stu-id="55ee2-150">The server gives you three pieces of information that you can use to determine how to configure your "window" for your next request:</span></span> 
  
- <span data-ttu-id="55ee2-151">Ob die Ergebnisse in der Antwort das letzte Element in der Gesamtergebnismenge auf dem Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="55ee2-151">Whether the results in the response include the last item in the overall result set on the server.</span></span>
    
- <span data-ttu-id="55ee2-152">Die Gesamtzahl der Elemente im Resultset auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="55ee2-152">The total number of items in the result set on the server.</span></span>
    
- <span data-ttu-id="55ee2-153">Was der nächste Offsetwert sein sollte, wenn Sie das Fenster zum nächsten Element im Resultset bringen möchten, das in der aktuellen Antwort nicht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="55ee2-153">What the next offset value should be, if you want to advance your window to the next item in the result set that isn't included in the current response.</span></span>
    
<span data-ttu-id="55ee2-154">Betrachten wir ein einfaches Beispiel.</span><span class="sxs-lookup"><span data-stu-id="55ee2-154">Let's look at a simple example.</span></span> <span data-ttu-id="55ee2-155">Stellen Sie sich einen Posteingang mit 15 Nachrichten vor.</span><span class="sxs-lookup"><span data-stu-id="55ee2-155">Imagine an Inbox with 15 messages in it.</span></span> <span data-ttu-id="55ee2-156">Ihre Anwendung sendet eine anfängliche Anforderung, um maximal 10 Elemente abzurufen, beginnend am Anfang der Liste der Nachrichten (sodass der Offset gleich Null ist).</span><span class="sxs-lookup"><span data-stu-id="55ee2-156">Your application sends an initial request to retrieve a maximum of 10 items, starting at the beginning of the list of messages (so the offset is zero).</span></span> <span data-ttu-id="55ee2-157">Der Server antwortet mit den ersten 10 Nachrichten und gibt an, dass die Antwort das letzte Element nicht beinhaltet, dass insgesamt 15 Elemente vorhanden sind, und dass der nächste Offset 10 sein sollte.</span><span class="sxs-lookup"><span data-stu-id="55ee2-157">The server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10.</span></span>
  
<span data-ttu-id="55ee2-158">**Abbildung 1. Anfordern von 10 Elementen bei Offset 0 ab dem Anfang einer Liste mit 15 Elementen**</span><span class="sxs-lookup"><span data-stu-id="55ee2-158">**Figure 1. Requesting 10 items at offset 0 from the beginning of a list of 15 items**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 0 am dem Anfang einer Liste mit 15 Elementen.](media/Ex15_PagedSearch_FirstPage.png)
  
<span data-ttu-id="55ee2-160">Ihre Anwendung sendet dann erneut die gleichen Anforderungen an den Server, wobei die einzige Änderung darin besteht, dass der Offset jetzt 10 gleicht.</span><span class="sxs-lookup"><span data-stu-id="55ee2-160">Your application then resends the same request to the server, with the only change being that the offset is now 10.</span></span> <span data-ttu-id="55ee2-161">Der Server gibt die letzten fünf Elemente zurück und gibt an, dass die Antwort nicht das letzte Elemente enthält, dass insgesamt 15 Elemente vorhanden sind, und dass der nächste Offset 15 sein sollte (obwohl Sie natürlich das Ende erreich haben und demnach kein weiterer Offset folgen wird.)</span><span class="sxs-lookup"><span data-stu-id="55ee2-161">The server returns the last five items, and indicates that the response does include the last item, that there are a total of 15 items, and that the next offset should be 15 (though of course, you've reached the end, so there won't be a next offset.)</span></span>
  
<span data-ttu-id="55ee2-162">**Abbildung 2. Anfordern von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 15 Elementen**</span><span class="sxs-lookup"><span data-stu-id="55ee2-162">**Figure 2. Requesting 10 items at offset 10 from the beginning of a list of 15 items**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 15 Elementen.](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a><span data-ttu-id="55ee2-164">Entwurfsaspekte für das Paging</span><span class="sxs-lookup"><span data-stu-id="55ee2-164">Design considerations for paging</span></span>
<span data-ttu-id="55ee2-165"><a name="bk_DesignConsiderations"> </a></span><span class="sxs-lookup"><span data-stu-id="55ee2-165"><a name="bk_DesignConsiderations"> </a></span></span>

<span data-ttu-id="55ee2-166">Um das Paging in Ihrer Anwendung optimal zu nutzen, müssen Sie sich einige Aspekte gründlich überlegen.</span><span class="sxs-lookup"><span data-stu-id="55ee2-166">Making the most out of paging in your application does require some consideration.</span></span> <span data-ttu-id="55ee2-167">Beispielsweise, wie groß wollen Sie Ihr „Fenster“ machen?</span><span class="sxs-lookup"><span data-stu-id="55ee2-167">For example, how large do you make your "window"?</span></span> <span data-ttu-id="55ee2-168">Was machen Sie, wenn sich die Ergebnisse auf dem Server ändern, während Sie das „Fenster“ verschieben? </span><span class="sxs-lookup"><span data-stu-id="55ee2-168">What do you do if the results on the server change while you're moving your "window"?</span></span>
  
### <a name="determine-the-size-of-your-window"></a><span data-ttu-id="55ee2-169">Die Größe des Fensters bestimmen</span><span class="sxs-lookup"><span data-stu-id="55ee2-169">Determine the size of your window</span></span>

<span data-ttu-id="55ee2-170">Es gibt keine „universale“ maximale Eintragnummer, die alle Anwendungen verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="55ee2-170">There is no "one-size-fits-all" maximum number of entries that all applications should use.</span></span> <span data-ttu-id="55ee2-171">Das Bestimmen der für Ihre Anwendung geeigneten Nummer hängt von mehreren Faktoren ab.</span><span class="sxs-lookup"><span data-stu-id="55ee2-171">Determining the number that's right for your application depends on several different factors.</span></span> <span data-ttu-id="55ee2-172">Es empfiehlt sich allerdings die folgenden Richtlinien im Kopf zu behalten:</span><span class="sxs-lookup"><span data-stu-id="55ee2-172">However, it's helpful to keep the following guidelines in mind:</span></span>
  
- <span data-ttu-id="55ee2-173">Standardmäßig beschränkt Exchange die maximale Anzahl von Elementen, die in einer einzigen Anforderung zurückgegeben werden können auf 1000.</span><span class="sxs-lookup"><span data-stu-id="55ee2-173">By default, Exchange limits the maximum number of items that can be returned in a single request to 1000.</span></span>
    
- <span data-ttu-id="55ee2-174">Wenn Sie die maximale Anzahl von Einträgen auf eine größere Zahl festlegen, müssen Sie weniger Anforderungen senden, um alle Elemente zu erhalten, Sie werden jedoch länger auf Antworten warten müssen.</span><span class="sxs-lookup"><span data-stu-id="55ee2-174">Setting the maximum number of entries to a larger number results in having to send fewer requests to get all items, at the cost of having to wait longer for responses.</span></span>
    
- <span data-ttu-id="55ee2-175">Wenn Sie die maximale Anzahl von Einträgen auf eine kleinere Zahl festlegen, wird die Antwortzeit beschleunigt, Sie werden mehrere Anforderungen senden müssen, um alle Elemente zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="55ee2-175">Setting the maximum number of entries to a smaller number results in quicker response times, at the cost of having to send more requests to get all items.</span></span>
    
### <a name="handling-changes-to-the-result-set"></a><span data-ttu-id="55ee2-176">Behandeln von Änderungen zum Resultset</span><span class="sxs-lookup"><span data-stu-id="55ee2-176">Handling changes to the result set</span></span>

<span data-ttu-id="55ee2-177">In dem bereits im Artikel erwähnten vereinfachten Beispiel war die Anzahl der Elemente im Posteingang des Benutzers konstant.</span><span class="sxs-lookup"><span data-stu-id="55ee2-177">In the simple example earlier in this article, the number of items in the user's Inbox remained constant.</span></span> <span data-ttu-id="55ee2-178">In Wirklichkeit kann sich die Anzahl der Elemente in einem Posteingang jedoch häufig ändern.</span><span class="sxs-lookup"><span data-stu-id="55ee2-178">However, in reality, the number of items in an Inbox can change frequently.</span></span> <span data-ttu-id="55ee2-179">Nue Nachrichten können eintreffen und Elemente können jederzeit gelöscht und verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="55ee2-179">New messages can arrive and items can be deleted or moved at any time.</span></span> <span data-ttu-id="55ee2-180">Doch wie wirkt sich dies auf das Paging aus?</span><span class="sxs-lookup"><span data-stu-id="55ee2-180">But how does this impact paging?</span></span> <span data-ttu-id="55ee2-181">Zur Veranschaulichung werden wir nun das frühere Beispielszenario ein wenig ändern.</span><span class="sxs-lookup"><span data-stu-id="55ee2-181">Let's modify the earlier example scenario to find out.</span></span>
  
<span data-ttu-id="55ee2-182">Wir beginnen wieder mit den 15 Elementen im Posteingang des Benutzers und senden die selbe Anfangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="55ee2-182">We'll start again with the 15 items in the user's Inbox, and send the same initial request.</span></span> <span data-ttu-id="55ee2-183">Wie bereits zuvor antwortet der Server mit den ersten 10 Nachrichten und gibt an, dass die Antwort das letzte Element nicht beinhaltet, dass insgesamt 15 Elemente vorhanden sind, und dass der nächste Offset 10 sein sollte, wie veranschaulicht auf der Abbildung 1.</span><span class="sxs-lookup"><span data-stu-id="55ee2-183">As before, the server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10, as shown in Figure 1.</span></span>
  
<span data-ttu-id="55ee2-184">Während Ihre Anwendung diese 10 Elemente verarbeitet, trifft einer neue Nachricht in Ihrem Posteingang ein und wird zum Resultset auf dem Server hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="55ee2-184">Now, while your application is processing those 10 items, a new message arrives in the Inbox and is added to the result set on the server.</span></span> <span data-ttu-id="55ee2-185">Ihre Anwendung sendet die gleiche Anforderung an den Server weiter (nur bei dem auf 10 eingestellten Offset).</span><span class="sxs-lookup"><span data-stu-id="55ee2-185">Your application resends the same request to the server (only with the offset set to 10).</span></span> <span data-ttu-id="55ee2-186">Diesmal bekommt der Server sechs Elemente zurück und gibt an, dass das Resultset insgesamt 16 Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="55ee2-186">This time the server gets back six items, and indicates that there are a total of 16 items in the result set.</span></span>
  
<span data-ttu-id="55ee2-187">In diesem Moment fragen Sie sich vielleicht, ob dies überhaupt ein Problem darstellt.</span><span class="sxs-lookup"><span data-stu-id="55ee2-187">At this point you might be wondering if this is even a problem.</span></span> <span data-ttu-id="55ee2-188">Schließlich haben sie 16 Elemente zu den zwei Antworten zurückbekommen. Warum dann die ganze Aufregung?</span><span class="sxs-lookup"><span data-stu-id="55ee2-188">After all, you got 16 items back over the two responses, so why all the fuss?</span></span> <span data-ttu-id="55ee2-189">Die Antwort darauf häng davon ab, wohin in der Liste das neue Element platziert wurde.</span><span class="sxs-lookup"><span data-stu-id="55ee2-189">The answer depends on where in the list the new item is placed.</span></span> <span data-ttu-id="55ee2-190">Wenn die Liste so sortiert ist, dass die ältesten Elemente (nach Empfangsdatum/Zeit) erst stehen, haben Sie keinen Grund zur Beunruhigung.</span><span class="sxs-lookup"><span data-stu-id="55ee2-190">If the list is sorted so that the oldest items (by received date/time) are first, there's no cause for concern in this scenario.</span></span> <span data-ttu-id="55ee2-191">Das neue Element wird an das Ende der Liste gestellt und wird in die nächsten Antwort einbezogen.</span><span class="sxs-lookup"><span data-stu-id="55ee2-191">The new item will be placed at the end of the list, and will be included in the second response.</span></span>
  
<span data-ttu-id="55ee2-192">**Abbildung 3. Anfordern von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wobei das 16. Element in der Liste neu ist**</span><span class="sxs-lookup"><span data-stu-id="55ee2-192">**Figure 3. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the 16th item in the list being new**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Ende der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
<span data-ttu-id="55ee2-194">Falls die Liste so sortiert ist, dass die neuesten Elemente erst stehen, ist dies ein Problem.</span><span class="sxs-lookup"><span data-stu-id="55ee2-194">If the list is sorted so that the newest items are first, it's a different story.</span></span> <span data-ttu-id="55ee2-195">In diesem Fall wäre das erste Element in der zweiten Anforderung das letzte Element der vorherigen Anforderung plus die restlichen fünf Elemente aus der ursprünglichen 15.</span><span class="sxs-lookup"><span data-stu-id="55ee2-195">In this case, the first item in the second request would be the last item from the previous request plus the remaining five items from the original 15.</span></span> <span data-ttu-id="55ee2-196">Um es an unserem magischen Fenster zu veranschaulichen, Sie haben Ihr Fenster um 10 verschoben, aber die Billboards selbst sind ebenfalls um 1 verschoben worden.</span><span class="sxs-lookup"><span data-stu-id="55ee2-196">To put it in terms of our imaginary magical window, you shifted your window's position by 10, but the billboards themselves also shifted by 1.</span></span>
  
<span data-ttu-id="55ee2-197">**Abbildung 4. Anfordern von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wobei das erste Element in der Liste neu ist**</span><span class="sxs-lookup"><span data-stu-id="55ee2-197">**Figure 4. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the first item in the list being new**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Anfang der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
<span data-ttu-id="55ee2-199">Eine Möglichkeit, wie eine Änderung der Ergebnisse auf dem Server erkannt werden kann, ist das Verwenden des Konzeptes eines Ankerelements.</span><span class="sxs-lookup"><span data-stu-id="55ee2-199">One way to detect a change to the results on the server is to use the concept of an anchor item.</span></span> <span data-ttu-id="55ee2-200">Ein Ankerelement ist ein zusätzliches Element in Ihrer Antwort, dass nicht mit den anderen Ergebnisse mitverarbeitet wird, aber zum Vergleichen mit den nächsten Ergebnissen verwendet wird, um festzustellen, ob die Elemente selbst verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="55ee2-200">An anchor item is an additional item in your response that is not processed along with the rest of the results, but is used to compare with the next results to see if the items themselves have shifted.</span></span> <span data-ttu-id="55ee2-201">Um es wieder mittels unseres Beispiels zu veranschaulichen, wenn Ihre Anwendung eine „Fenster“-Größe von 10 verwendet, stellen Sie in Wirklichkeit die maximale Anzahl von Elementen, die zurückgesetzt werden, auf 11. </span><span class="sxs-lookup"><span data-stu-id="55ee2-201">Building again on our simple example, if your application is using a "window" size of 10, you actually set the maximum number of items to return to 11.</span></span> <span data-ttu-id="55ee2-202">Ihre Anwendung verarbeitet die ersten 10 Elemente in der Antwort wie gewohnt.</span><span class="sxs-lookup"><span data-stu-id="55ee2-202">Your application processes the first 10 items in the response as usual.</span></span> <span data-ttu-id="55ee2-203">Für das letzte Element speichern Sie den Bezeichner des Elements als Anker und geben Sie die nächste Anforderung mit einem Offset von 10 ein.</span><span class="sxs-lookup"><span data-stu-id="55ee2-203">For the last item, you save the item's identifier as an anchor, then issue the next request with an offset of 10.</span></span> <span data-ttu-id="55ee2-204">Wenn sich die Daten nicht geändert haben, sollte das erste Element in der zweiten Antwort einen Bezeichner haben, der mit dem Anker übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="55ee2-204">If the data has not changed, the first item in the second response should have an item identifier that matches the anchor.</span></span> <span data-ttu-id="55ee2-205">Wenn die Elementbezeichner nicht übereinstimmen, wissen Sie, dass die Daten in den Abschnitten der Liste, die Sie bereits „ausgelagert“ haben, entfernt oder eingefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="55ee2-205">If the item identifiers don't match, you know that the data has been removed or inserted in the parts of the list you have already "paged" over.</span></span>
  
<span data-ttu-id="55ee2-206">Auch wenn Sie wissen, das sich die Daten geändert haben, müssen Sie sich immer noch entscheiden, wie reagiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="55ee2-206">Even when you know that the data has changed, you still need to decide how to react.</span></span> <span data-ttu-id="55ee2-207">Auch auf diese Frage gibt es keine universale Antwort.</span><span class="sxs-lookup"><span data-stu-id="55ee2-207">There isn't a one-size-fits-all answer for this question either.</span></span> <span data-ttu-id="55ee2-208">Ihre Aktionen werden von der Art Ihrer Anwendung und davon, wie wichtig es ist, alle Elemente zu erfassen, abhängen.</span><span class="sxs-lookup"><span data-stu-id="55ee2-208">Your actions will depend on the nature of your application and how critical it is to capture all items.</span></span> <span data-ttu-id="55ee2-209">Sie könnten sie völlig ignorieren, den Vorgang neu starten, oder zurückverfolgen und versuchen, die Stelle der Änderung zu finden.</span><span class="sxs-lookup"><span data-stu-id="55ee2-209">You might ignore it altogether, restart the process from the beginning, or back track and try to detect where the change happened.</span></span>
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a><span data-ttu-id="55ee2-210">Beispiel: Eine ausgelagerte Suche mittels verwalteten EWS-API durchführen</span><span class="sxs-lookup"><span data-stu-id="55ee2-210">Example: Perform a paged search by using the EWS Managed API</span></span>
<span data-ttu-id="55ee2-211"><a name="bk_PagedSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="55ee2-211"><a name="bk_PagedSearchEWSMA"> </a></span></span>

<span data-ttu-id="55ee2-212">Das Paging wird von den folgenden verwalteten EWS-API-Methoden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="55ee2-212">Paging is supported by the following EWS Managed API methods:</span></span>
  
- [<span data-ttu-id="55ee2-213">ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="55ee2-213">ExchangeService.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="55ee2-214">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="55ee2-214">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="55ee2-215">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="55ee2-215">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="55ee2-216">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="55ee2-216">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="55ee2-217">Wenn Sie die verwaltete EWS-API verwenden, konfiguriert Ihre Anwendung das Paging mit der [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) oder [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx)-Klasse und empfängt Informationen von dem Server bezüglich des Pagings von der [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) oder der [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx)-Klasse.</span><span class="sxs-lookup"><span data-stu-id="55ee2-217">If you are using the EWS Managed API, your application configures paging with the [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) or [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) class and receives information from the server regarding paging from the [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) or [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) class.</span></span> 
  
<span data-ttu-id="55ee2-218">Im folgenden Beispiel werden alle Elemente in einem Ordner mithilfe einer ausgelagerten Suche abgerufen, die fünf Elemente in jeder Antwort zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="55ee2-218">The following example retrieves all the items in a folder using a paged search that returns five items in each response.</span></span> <span data-ttu-id="55ee2-219">Außerdem ruft es ein zusätzliches Element ab, das als Anker dient, um Änderungen an den Ergebnissen auf dem Server zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="55ee2-219">It also retrieves an additional item to serve as an anchor to detect changes to the results on the server.</span></span> 
  
<span data-ttu-id="55ee2-220">In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="55ee2-220">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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
            if (moreItems && anchorId != null)
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
            int displayCount = 0;
            if ((results.MoreAvailable == false && results.Items.Count > pageSize) || (results.Items.Count < pageSize))
            {
                displayCount = results.Items.Count;
            }
            else
            {
                displayCount = pageSize;
            }
            
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

## <a name="example-perform-a-paged-search-by-using-ews"></a><span data-ttu-id="55ee2-221">Beispiel: Eine ausgelagerte Suche mittels EWS durchführen</span><span class="sxs-lookup"><span data-stu-id="55ee2-221">Example: Perform a paged search by using EWS</span></span>
<span data-ttu-id="55ee2-222"><a name="bk_PagedSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="55ee2-222"><a name="bk_PagedSearchEWS"> </a></span></span>

<span data-ttu-id="55ee2-223">Das Paging wird von den folgenden EWS-Vorgängen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="55ee2-223">Paging is supported by the following EWS operations:</span></span>
  
- [<span data-ttu-id="55ee2-224">FindFolder</span><span class="sxs-lookup"><span data-stu-id="55ee2-224">FindFolder</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="55ee2-225">FindItem</span><span class="sxs-lookup"><span data-stu-id="55ee2-225">FindItem</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
<span data-ttu-id="55ee2-226">Wenn Sie EWS verwenden, konfiguriert ihre Anwendung das Paging mit den [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)-Element oder dem [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)-Element und empfängt Informationen vom Server hinsichtlich des Pagings aus dem [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx)-Element oder dem [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)-Element.</span><span class="sxs-lookup"><span data-stu-id="55ee2-226">If you're using EWS, your application configures paging with the [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element and receives information from the server regarding paging from the [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="55ee2-227">In diesem Anforderungsbeispiel wird eine **FindItem**-Anforderung für maximal sechs Elemente gesendet, beginnend bei einem Offset von 0 vom Anfang der Liste der Elemente im Posteingang des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="55ee2-227">In this request example, a **FindItem** request is sent for a maximum of six items, starting at an offset of zero from the beginning of the list of items in the user's Inbox.</span></span> 
  
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

<span data-ttu-id="55ee2-228">Der Servers gibt die folgende Antwort zurück, die sechs Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="55ee2-228">The server returns the following response, which contains six items.</span></span> <span data-ttu-id="55ee2-229">Die Antwort gibt außerdem an, dass in den Ergebnissen auf dem Server insgesamt acht Elemente vorhanden sind, und dass das letzte Element in der Ergebnisliste nicht in der Antwort enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="55ee2-229">The response also indicates that there are a total of eight items in the results on the server, and that the last item in the results list is not present in this response.</span></span>
  
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

<span data-ttu-id="55ee2-230">In diesem Beispiel wird die gleiche Anforderung gesendet, aber diesmal wird das **Offset**-Attribut in „fünf“ geändert, wodurch angegeben wird, dass der Server höchstens sechs Elemente zurückgeben sollte, beginnend mit dem Offset von fünf vom Anfang.</span><span class="sxs-lookup"><span data-stu-id="55ee2-230">In this example, the same request is sent, but this time, the **Offset** attribute is changed to five, which indicates that the server should return at most six items starting at offset five from the beginning.</span></span> 
  
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

<span data-ttu-id="55ee2-231">Der Servers sendet die folgende Antwort, die drei Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="55ee2-231">The server sends the following response, which contains three items.</span></span> <span data-ttu-id="55ee2-232">Die Antwort gibt außerdem an, dass in den Ergebnissen auf dem Server immer noch insgesamt acht Elemente vorhanden sind, und dass das letzte Element in der Ergebnisliste nicht in der Antwort einbezogen ist.</span><span class="sxs-lookup"><span data-stu-id="55ee2-232">The response also indicates that the total number of items in the results on the server is still eight, and that the last item in the results list is included in this response.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="55ee2-233">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55ee2-233">See also</span></span>


- [<span data-ttu-id="55ee2-234">Suche und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="55ee2-234">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="55ee2-235">ExchangeService.FindFolders-Methode</span><span class="sxs-lookup"><span data-stu-id="55ee2-235">ExchangeService.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="55ee2-236">ExchangeService.FindItems-Methode</span><span class="sxs-lookup"><span data-stu-id="55ee2-236">ExchangeService.FindItems method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="55ee2-237">Folder.FindFolders-Methode</span><span class="sxs-lookup"><span data-stu-id="55ee2-237">Folder.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="55ee2-238">Folder.FindFolders-Methode</span><span class="sxs-lookup"><span data-stu-id="55ee2-238">Folder.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="55ee2-239">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="55ee2-239">FindFolder operation</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="55ee2-240">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="55ee2-240">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [<span data-ttu-id="55ee2-241">EWS-Einschränkung in Exchange</span><span class="sxs-lookup"><span data-stu-id="55ee2-241">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    

