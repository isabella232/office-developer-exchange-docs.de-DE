---
title: Führen Sie seitenweise durch Verwenden von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64ed70e4-32eb-4c25-bfc4-43d1477296e5
description: Erfahren Sie, wie Sie seitenweise in die EWS Managed API oder EWS-Anwendung, die beruht auf Exchange ausführen.
ms.openlocfilehash: 3f82f46d0582b0b7ff8be63de8a7054b5f3cacab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756980"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a><span data-ttu-id="2db1d-103">Führen Sie seitenweise durch Verwenden von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2db1d-103">Perform paged searches by using EWS in Exchange</span></span>

<span data-ttu-id="2db1d-104">Erfahren Sie, wie Sie seitenweise in die EWS Managed API oder EWS-Anwendung, die beruht auf Exchange ausführen.</span><span class="sxs-lookup"><span data-stu-id="2db1d-104">Find out how to perform paged searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="2db1d-105">Auslagerungsdatei ist ein Feature in der Exchange-Webdienste, mit dem Sie die Größe der Ergebnisse einer Suche steuern können.</span><span class="sxs-lookup"><span data-stu-id="2db1d-105">Paging is a feature in EWS that enables you to control the size of the results of a search.</span></span> <span data-ttu-id="2db1d-106">Anstatt das gesamte Resultset in eine EWS-Antwort abzurufen, können Sie kleinere Inhaltssätze in mehreren EWS-Antworten abrufen.</span><span class="sxs-lookup"><span data-stu-id="2db1d-106">Rather than retrieve the entire result set in one EWS response, you can retrieve smaller sets in multiple EWS responses.</span></span> <span data-ttu-id="2db1d-107">Angenommen Sie, einen Benutzer mit 10.000 e-Mail-Nachrichten in ihren Posteingang.</span><span class="sxs-lookup"><span data-stu-id="2db1d-107">For example, consider a user with 10,000 email messages in their Inbox.</span></span> <span data-ttu-id="2db1d-108">Wenn, Sie konnte alle 10.000-e-Mails in eine sehr große Antwort abrufen, jedoch möglicherweise möchten Sie, die mehrere Blöcken aus Gründen der Bandbreite oder Leistung aufteilen.</span><span class="sxs-lookup"><span data-stu-id="2db1d-108">Hypothetically, you could retrieve all 10,000 emails in one very large response, but you might want to break that up into more manageable chunks for bandwidth or performance reasons.</span></span> <span data-ttu-id="2db1d-109">Paging können Sie die Tools, die genau das, was.</span><span class="sxs-lookup"><span data-stu-id="2db1d-109">Paging gives you the tools to do just that.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2db1d-110">Während Sie 10.000 Elemente in einer Anforderung, wenn in der Praxis abrufen können, ist dies unwahrscheinlich EWS-Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="2db1d-110">While you can hypothetically retrieve 10,000 items in one request, in reality, this is unlikely due to EWS throttling.</span></span> <span data-ttu-id="2db1d-111">Wenn Sie mehr erfahren möchten, finden Sie unter [EWS-Einschränkung im Exchange](ews-throttling-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="2db1d-111">To find out more, see [EWS throttling in Exchange](ews-throttling-in-exchange.md).</span></span> 
  
<span data-ttu-id="2db1d-112">**In Tabelle 1. Pagingparameter in die EWS Managed API und die Exchange-Webdienste**</span><span class="sxs-lookup"><span data-stu-id="2db1d-112">**Table 1. Paging parameters in the EWS Managed API and EWS**</span></span>

|<span data-ttu-id="2db1d-113">**So konfigurieren oder Abrufen der...**</span><span class="sxs-lookup"><span data-stu-id="2db1d-113">**To configure or retrieve the…**</span></span>|<span data-ttu-id="2db1d-114">**Verwenden Sie in die EWS Managed API...**</span><span class="sxs-lookup"><span data-stu-id="2db1d-114">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="2db1d-115">**Verwenden Sie in der Exchange-Webdienste...**</span><span class="sxs-lookup"><span data-stu-id="2db1d-115">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2db1d-116">Maximale Anzahl von Elementen oder Ordner in einer Antwort</span><span class="sxs-lookup"><span data-stu-id="2db1d-116">Maximum number of items or folders in a response</span></span>  <br/> |<span data-ttu-id="2db1d-117">Die **PageSize** -Parameter für den [Konstruktor aufrufenArtikel aufrufen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) oder den [FolderView-Konstruktor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2db1d-117">The **pageSize** parameter to the [ItemView constructor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) or the [FolderView constructor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span></span> <br/> <span data-ttu-id="2db1d-118">Oder</span><span class="sxs-lookup"><span data-stu-id="2db1d-118">Or</span></span>  <br/> <span data-ttu-id="2db1d-119">Die [PagedView.PageSize](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2db1d-119">The [PagedView.PageSize](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="2db1d-120">Das Attribut **"MaxEntriesReturned"** auf dem [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) -Element oder das [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) -element</span><span class="sxs-lookup"><span data-stu-id="2db1d-120">The **MaxEntriesReturned** attribute on the [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="2db1d-121">Startpunkt in der Liste der Elemente oder Ordner</span><span class="sxs-lookup"><span data-stu-id="2db1d-121">Starting point in the list of items or folders</span></span>  <br/> |<span data-ttu-id="2db1d-122">Der Parameter **OffsetBasePoint** an den Konstruktor **aufrufenArtikel aufrufen** oder die **FolderView** -Konstruktor</span><span class="sxs-lookup"><span data-stu-id="2db1d-122">The **offsetBasePoint** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="2db1d-123">Oder</span><span class="sxs-lookup"><span data-stu-id="2db1d-123">Or</span></span>  <br/> <span data-ttu-id="2db1d-124">Die [PagedView.OffsetBasePoint](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2db1d-124">The [PagedView.OffsetBasePoint](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="2db1d-125">Das Attribut **Basispunkt** auf dem **IndexedPageItemView** -Element oder das **IndexedPageFolderView** -element</span><span class="sxs-lookup"><span data-stu-id="2db1d-125">The **BasePoint** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="2db1d-126">Abstand vom Ausgangspunkt</span><span class="sxs-lookup"><span data-stu-id="2db1d-126">Offset from the starting point</span></span>  <br/> |<span data-ttu-id="2db1d-127">Der Parameter **Offset** an den Konstruktor **aufrufenArtikel aufrufen** oder die **FolderView** -Konstruktor</span><span class="sxs-lookup"><span data-stu-id="2db1d-127">The **offset** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="2db1d-128">Oder</span><span class="sxs-lookup"><span data-stu-id="2db1d-128">Or</span></span>  <br/> <span data-ttu-id="2db1d-129">Die [PagedView.Offset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2db1d-129">The [PagedView.Offset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="2db1d-130">Das Attribut **Offset** für das Element **IndexedPageItemView** oder das **IndexedPageFolderView** -element</span><span class="sxs-lookup"><span data-stu-id="2db1d-130">The **Offset** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="2db1d-131">Gesamtanzahl der Ergebnisse auf dem server</span><span class="sxs-lookup"><span data-stu-id="2db1d-131">Total number of results on the server</span></span>  <br/> |<span data-ttu-id="2db1d-132">Die [FindItemsResults.TotalCount](http://msdn.microsoft.com/en-us/library/dd635348%28v=exchg.80%29.aspx) -Eigenschaft oder die [FindFoldersResults.TotalCount](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2db1d-132">The [FindItemsResults.TotalCount](http://msdn.microsoft.com/en-us/library/dd635348%28v=exchg.80%29.aspx) property or the [FindFoldersResults.TotalCount](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="2db1d-133">Das **TotalItemsInView** -Attribut für das Element [RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) oder das Element [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2db1d-133">The **TotalItemsInView** attribute on the [RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="2db1d-134">Offset des ersten Elements oder Ordners in der aktuellen Antwort nicht enthalten</span><span class="sxs-lookup"><span data-stu-id="2db1d-134">Offset of first item or folder not included in current response</span></span>  <br/> |<span data-ttu-id="2db1d-135">Die [FindItemsResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/ee693014%28v=exchg.80%29.aspx) -Eigenschaft oder die [FindFoldersResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2db1d-135">The [FindItemsResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/ee693014%28v=exchg.80%29.aspx) property or the [FindFoldersResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="2db1d-136">Das Attribut **IndexedPagingOffset** die **RootFolder** -element</span><span class="sxs-lookup"><span data-stu-id="2db1d-136">The **IndexedPagingOffset** attribute on the **RootFolder** element</span></span>  <br/> |
|<span data-ttu-id="2db1d-137">Symbol, dass die Antwort des letzten Elements oder Ordners in der Liste enthält</span><span class="sxs-lookup"><span data-stu-id="2db1d-137">Indicator that response includes the last item or folder in the list</span></span>  <br/> |<span data-ttu-id="2db1d-138">Die [FindItemsResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/dd635477%28v=exchg.80%29.aspx) -Eigenschaft oder die [FindFoldersResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2db1d-138">The [FindItemsResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/dd635477%28v=exchg.80%29.aspx) property or the [FindFoldersResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="2db1d-139">Das Attribut **IncludesLastItemInRange** die **RootFolder** -element</span><span class="sxs-lookup"><span data-stu-id="2db1d-139">The **IncludesLastItemInRange** attribute on the **RootFolder** element</span></span>  <br/> |
   
## <a name="how-paging-works"></a><span data-ttu-id="2db1d-140">Funktionsweise von paging</span><span class="sxs-lookup"><span data-stu-id="2db1d-140">How paging works</span></span>
<span data-ttu-id="2db1d-141"><a name="bk_HowPagingWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="2db1d-141"></span></span>

<span data-ttu-id="2db1d-142">Zum Verständnis der Funktionsweise der Auslagerungsdatei ist es hilfreich, die Nachrichten in einem Ordner als horizontal/vertikal ausgerichtet nebeneinander in einem Feld außerhalb Haus an visualisieren.</span><span class="sxs-lookup"><span data-stu-id="2db1d-142">To understand how paging works, it's helpful to visualize the messages in a folder as billboards lined up side by side in a field outside your house.</span></span> <span data-ttu-id="2db1d-143">Sie können einige dieser an über das magische Fenster sehen.</span><span class="sxs-lookup"><span data-stu-id="2db1d-143">You can see some of these billboards through a magical window.</span></span> <span data-ttu-id="2db1d-144">Sie haben die Möglichkeit zum Ändern der Größe des Fensters (mehr oder weniger an gleichzeitig finden Sie unter) und das Fenster (zu steuern, welche an, die Sie sehen) zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="2db1d-144">You have the ability to change the size of the window (to see more or fewer billboards at once) and to move the window (to control which billboards you can see).</span></span> <span data-ttu-id="2db1d-145">Diese Manipulation des Fensters paging ist.</span><span class="sxs-lookup"><span data-stu-id="2db1d-145">This manipulation of the window is paging.</span></span> 
  
<span data-ttu-id="2db1d-146">Wenn Sie Ihre Anforderung an den Exchange-Server senden, geben Sie die Größe des Fensters hinsichtlich der Anzahl der Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2db1d-146">When you send your request to the Exchange server, you specify the size of your window in terms of how many items to return.</span></span> <span data-ttu-id="2db1d-147">Die Position des Fensters festlegen durch Angabe Ausgangspunkt (am Anfang der Zeile) oder das Ende der Zeile und einem Offset aus den Ausgangspunkt, ausgedrückt als eine Anzahl von Elementen.</span><span class="sxs-lookup"><span data-stu-id="2db1d-147">You set the position of the window by specifying a starting point (either the beginning of the line or the end of the line) and an offset from that starting point, expressed in a number of items.</span></span> <span data-ttu-id="2db1d-148">Der Anfang des Fensters ist die Anzahl der Elemente, die durch den Offset vom Anfangspunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="2db1d-148">The beginning of the window is the number of items specified by the offset from the starting point.</span></span>
  
<span data-ttu-id="2db1d-149">Wobei Paging etwas interessant ist in der Antwort des Servers, und wie Ihre Anwendung Antwort an die nächste Anforderung shape verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="2db1d-149">Where paging gets a bit more interesting is in the server's response, and how your application can use that response to shape its next request.</span></span> <span data-ttu-id="2db1d-150">Der Server gibt Ihnen drei Angaben, die Sie verwenden können, zu bestimmen, wie das "Fenster" für die nächste Anforderung zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="2db1d-150">The server gives you three pieces of information that you can use to determine how to configure your "window" for your next request:</span></span> 
  
- <span data-ttu-id="2db1d-151">Gibt an, ob die Ergebnisse in der Antwort das letzte Element in der gesamten Ergebnismenge auf dem Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="2db1d-151">Whether the results in the response include the last item in the overall result set on the server.</span></span>
    
- <span data-ttu-id="2db1d-152">Die Gesamtzahl der Elemente in der Ergebnismenge auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="2db1d-152">The total number of items in the result set on the server.</span></span>
    
- <span data-ttu-id="2db1d-153">Was sollte der nächste Offsetwert sein sollten Sie das Fenster auf das nächste Element im Resultset zur nächsten Folie gewechselt, die nicht in der aktuellen Antwort steht.</span><span class="sxs-lookup"><span data-stu-id="2db1d-153">What the next offset value should be, if you want to advance your window to the next item in the result set that isn't included in the current response.</span></span>
    
<span data-ttu-id="2db1d-154">Sehen wir uns ein einfaches Beispiel.</span><span class="sxs-lookup"><span data-stu-id="2db1d-154">Let's look at a simple example.</span></span> <span data-ttu-id="2db1d-155">Stellen Sie sich vor einem Posteingang mit 15 Beiträge.</span><span class="sxs-lookup"><span data-stu-id="2db1d-155">Imagine an Inbox with 15 messages in it.</span></span> <span data-ttu-id="2db1d-156">Die Anwendung sendet eine anfängliche Anforderung zum Abrufen von maximal 10 Elemente, beginnend am Anfang der Liste der Nachrichten (damit der Offset gleich 0 (null) ist).</span><span class="sxs-lookup"><span data-stu-id="2db1d-156">Your application sends an initial request to retrieve a maximum of 10 items, starting at the beginning of the list of messages (so the offset is zero).</span></span> <span data-ttu-id="2db1d-157">Der Server antwortet mit der ersten 10 Nachrichten und gibt an, dass die Antwort nicht enthalten, ist das letzte Element, das, dass es werden insgesamt 15 Elementen und der nächste Offset 10 werden soll.</span><span class="sxs-lookup"><span data-stu-id="2db1d-157">The server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10.</span></span>
  
<span data-ttu-id="2db1d-158">**Abbildung 1. Anforderns von 10 Elementen bei Offset 0 am Anfang einer Liste mit 15 Elementen**</span><span class="sxs-lookup"><span data-stu-id="2db1d-158">**Figure 1. Requesting 10 items at offset 0 from the beginning of a list of 15 items**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 0 am dem Anfang einer Liste mit 15 Elementen.](media/Ex15_PagedSearch_FirstPage.png)
  
<span data-ttu-id="2db1d-160">Klicken Sie dann die Anwendung sendet derselben Anforderung an den Server, mit der nur ändern, dass der Offset jetzt 10 ist.</span><span class="sxs-lookup"><span data-stu-id="2db1d-160">Your application then resends the same request to the server, with the only change being that the offset is now 10.</span></span> <span data-ttu-id="2db1d-161">Der Server gibt den letzten fünf Elemente zurück, und gibt an, dass die Antwort enthält das letzte Element, das, dass es werden insgesamt 15 Elementen und der nächste Offset 15 werden soll (obwohl natürlich Sie am Ende erreicht haben und kein nächsten Offset.)</span><span class="sxs-lookup"><span data-stu-id="2db1d-161">The server returns the last five items, and indicates that the response does include the last item, that there are a total of 15 items, and that the next offset should be 15 (though of course, you've reached the end, so there won't be a next offset.)</span></span>
  
<span data-ttu-id="2db1d-162">**Abbildung 2. Anfordern von 10 Elementen bei Offset 10 vom Anfang einer Liste mit 15 Elementen**</span><span class="sxs-lookup"><span data-stu-id="2db1d-162">**Figure 2. Requesting 10 items at offset 10 from the beginning of a list of 15 items**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 0 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Anfang der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a><span data-ttu-id="2db1d-164">Entwurfsaspekte für die Auslagerung</span><span class="sxs-lookup"><span data-stu-id="2db1d-164">Design considerations for paging</span></span>
<span data-ttu-id="2db1d-165"><a name="bk_DesignConsiderations"> </a></span><span class="sxs-lookup"><span data-stu-id="2db1d-165"></span></span>

<span data-ttu-id="2db1d-166">Optimale Nutzung Paging in Ihrer Anwendung erfordert einige berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="2db1d-166">Making the most out of paging in your application does require some consideration.</span></span> <span data-ttu-id="2db1d-167">Beispielsweise wie groß gemacht Sie Ihr "Fenster"?</span><span class="sxs-lookup"><span data-stu-id="2db1d-167">For example, how large do you make your "window"?</span></span> <span data-ttu-id="2db1d-168">Was tun Sie, wenn die Ergebnisse auf dem Server ändern, während Sie Ihr "Fenster" verschieben?</span><span class="sxs-lookup"><span data-stu-id="2db1d-168">What do you do if the results on the server change while you're moving your "window"?</span></span>
  
### <a name="determine-the-size-of-your-window"></a><span data-ttu-id="2db1d-169">Bestimmen Sie die Größe des Fensters</span><span class="sxs-lookup"><span data-stu-id="2db1d-169">Determine the size of your window</span></span>

<span data-ttu-id="2db1d-170">Es ist keine "Stange" maximale Anzahl von Einträgen, die alle Anwendungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2db1d-170">There is no "one-size-fits-all" maximum number of entries that all applications should use.</span></span> <span data-ttu-id="2db1d-171">Bestimmen der Anzahl, die für Ihre Anwendung geeignet ist, hängt von verschiedenen Faktoren ab.</span><span class="sxs-lookup"><span data-stu-id="2db1d-171">Determining the number that's right for your application depends on several different factors.</span></span> <span data-ttu-id="2db1d-172">Jedoch ist es hilfreich, die folgenden Richtlinien im Hinterkopf behalten:</span><span class="sxs-lookup"><span data-stu-id="2db1d-172">However, it's helpful to keep the following guidelines in mind:</span></span>
  
- <span data-ttu-id="2db1d-173">Standardmäßig begrenzt Exchange die maximale Anzahl der Elemente, die in einer einzelnen Anforderung bis 1000 zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="2db1d-173">By default, Exchange limits the maximum number of items that can be returned in a single request to 1000.</span></span>
    
- <span data-ttu-id="2db1d-174">Durch Festlegen der maximalen Anzahl der Einträge auf eine größere Zahl zu müssen weniger Anfragen zum Abrufen aller Elemente, aber mehr Antworten warten müssen.</span><span class="sxs-lookup"><span data-stu-id="2db1d-174">Setting the maximum number of entries to a larger number results in having to send fewer requests to get all items, at the cost of having to wait longer for responses.</span></span>
    
- <span data-ttu-id="2db1d-175">Die maximale Anzahl von Einträgen aus der festlegen auf einer kleineren Anzahl Ergebnisse schnellere Antwortzeiten Kosten für weitere Anfragen zum Abrufen aller Elemente müssen.</span><span class="sxs-lookup"><span data-stu-id="2db1d-175">Setting the maximum number of entries to a smaller number results in quicker response times, at the cost of having to send more requests to get all items.</span></span>
    
### <a name="handling-changes-to-the-result-set"></a><span data-ttu-id="2db1d-176">Behandlung von Änderungen an dem Resultset</span><span class="sxs-lookup"><span data-stu-id="2db1d-176">Handling changes to the result set</span></span>

<span data-ttu-id="2db1d-177">In der einfachen Beispiel weiter oben in diesem Artikel blieb die Anzahl der Elemente im Posteingang des Benutzers Konstante.</span><span class="sxs-lookup"><span data-stu-id="2db1d-177">In the simple example earlier in this article, the number of items in the user's Inbox remained constant.</span></span> <span data-ttu-id="2db1d-178">Die Anzahl der Elemente im Posteingang kann jedoch in der Praxis häufig ändern.</span><span class="sxs-lookup"><span data-stu-id="2db1d-178">However, in reality, the number of items in an Inbox can change frequently.</span></span> <span data-ttu-id="2db1d-179">Neue Nachrichten eingehen können und Elemente gelöscht oder zu einem beliebigen Zeitpunkt verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="2db1d-179">New messages can arrive and items can be deleted or moved at any time.</span></span> <span data-ttu-id="2db1d-180">Aber wie führt diese Auswirkungen Paging?</span><span class="sxs-lookup"><span data-stu-id="2db1d-180">But how does this impact paging?</span></span> <span data-ttu-id="2db1d-181">Lassen Sie uns ändern das frühere Beispielszenario Sie herausfinden können.</span><span class="sxs-lookup"><span data-stu-id="2db1d-181">Let's modify the earlier example scenario to find out.</span></span>
  
<span data-ttu-id="2db1d-182">Wir beginnen Sie erneut mit der 15 Elementen im Posteingang des Benutzers und die gleiche anfängliche Anforderung senden.</span><span class="sxs-lookup"><span data-stu-id="2db1d-182">We'll start again with the 15 items in the user's Inbox, and send the same initial request.</span></span> <span data-ttu-id="2db1d-183">Als vor, der Server antwortet mit der ersten 10 Nachrichten und gibt an, dass die Antwort das letzte Element, das, dass es werden insgesamt 15 Elementen und der nächste Offset 10, sollten nicht einschließen, wie in Abbildung 1 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2db1d-183">As before, the server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10, as shown in Figure 1.</span></span>
  
<span data-ttu-id="2db1d-184">Nun, während die Anwendung die 10 Elemente verarbeitet wird, eine neue Nachricht im Posteingang eingeht und das Resultset auf dem Server hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2db1d-184">Now, while your application is processing those 10 items, a new message arrives in the Inbox and is added to the result set on the server.</span></span> <span data-ttu-id="2db1d-185">Die Anwendung sendet die gleiche Anforderung an den Server (nur mit der Offset auf 10).</span><span class="sxs-lookup"><span data-stu-id="2db1d-185">Your application resends the same request to the server (only with the offset set to 10).</span></span> <span data-ttu-id="2db1d-186">Diesmal der Server ruft zurück sechs Elemente ab und gibt an, dass insgesamt 16 Elemente im Resultset.</span><span class="sxs-lookup"><span data-stu-id="2db1d-186">This time the server gets back six items, and indicates that there are a total of 16 items in the result set.</span></span>
  
<span data-ttu-id="2db1d-187">An dieser Stelle Sie vielleicht, wenn dies auch ein Problem darstellt.</span><span class="sxs-lookup"><span data-stu-id="2db1d-187">At this point you might be wondering if this is even a problem.</span></span> <span data-ttu-id="2db1d-188">Schließlich haben Sie 16 Elemente wieder über die zwei Antworten, warum also ganze?</span><span class="sxs-lookup"><span data-stu-id="2db1d-188">After all, you got 16 items back over the two responses, so why all the fuss?</span></span> <span data-ttu-id="2db1d-189">Die Antwort hängt davon ab, wo in der Liste das neue Element platziert wird.</span><span class="sxs-lookup"><span data-stu-id="2db1d-189">The answer depends on where in the list the new item is placed.</span></span> <span data-ttu-id="2db1d-190">Wenn die Liste sortiert wird, damit die ältesten Elemente (nach Empfangsdatum samt Uhrzeit) erste sind, ist keine Ursache für Herausforderung in diesem Szenario.</span><span class="sxs-lookup"><span data-stu-id="2db1d-190">If the list is sorted so that the oldest items (by received date/time) are first, there's no cause for concern in this scenario.</span></span> <span data-ttu-id="2db1d-191">Das neue Element wird am Ende der Liste eingefügt werden, und wird in der zweiten Antwort enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="2db1d-191">The new item will be placed at the end of the list, and will be included in the second response.</span></span>
  
<span data-ttu-id="2db1d-192">**Abbildung 3. Anfordern von 10 Elementen bei Offset 10 vom Anfang einer Liste von 16 Elemente mit dem 16. Element in der Liste neue wird**</span><span class="sxs-lookup"><span data-stu-id="2db1d-192">**Figure 3. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the 16th item in the list being new**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Ende der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
<span data-ttu-id="2db1d-194">Wenn die Liste sortiert wird, damit die neuesten Elemente ersten sind, ist es anders.</span><span class="sxs-lookup"><span data-stu-id="2db1d-194">If the list is sorted so that the newest items are first, it's a different story.</span></span> <span data-ttu-id="2db1d-195">In diesem Fall würde das erste Element in der zweiten Anforderung das letzte Element aus der vorherigen Anforderung plus die verbleibenden fünf Elemente aus der ursprünglichen 15 sein.</span><span class="sxs-lookup"><span data-stu-id="2db1d-195">In this case, the first item in the second request would be the last item from the previous request plus the remaining five items from the original 15.</span></span> <span data-ttu-id="2db1d-196">Im Hinblick auf unser imaginäre magische Fenster ausgedrückt, verschoben Sie Position des Fensters um 10, aber die an sich selbst auch um verschoben, 1.</span><span class="sxs-lookup"><span data-stu-id="2db1d-196">To put it in terms of our imaginary magical window, you shifted your window's position by 10, but the billboards themselves also shifted by 1.</span></span>
  
<span data-ttu-id="2db1d-197">**Abbildung 4. Anfordern von 10 Elementen bei Offset 10 vom Anfang einer Liste von 16 Elemente mit dem ersten Element in der Liste neue wird**</span><span class="sxs-lookup"><span data-stu-id="2db1d-197">**Figure 4. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the first item in the list being new**</span></span>

![Diagramm mit den Ergebnissen des Anforderns von 10 Elementen bei Offset 10 ab dem Anfang einer Liste mit 16 Elementen, wenn das 16. Element dem Anfang der Liste hinzugefügt wurde.](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
<span data-ttu-id="2db1d-199">Eine Möglichkeit, eine Änderung auf die Ergebnisse auf dem Server zu erkennen ist das Konzept eines Anker-Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="2db1d-199">One way to detect a change to the results on the server is to use the concept of an anchor item.</span></span> <span data-ttu-id="2db1d-200">Ein Anker-Element ist ein zusätzliches Element in Ihre Antwort, die nicht zusammen mit dem Rest der Ergebnisse verarbeitet wird, aber wird verwendet, um mit der nächsten Ergebnisse zu sehen, ob die Elemente selbst verschoben wurden vergleichen.</span><span class="sxs-lookup"><span data-stu-id="2db1d-200">An anchor item is an additional item in your response that is not processed along with the rest of the results, but is used to compare with the next results to see if the items themselves have shifted.</span></span> <span data-ttu-id="2db1d-201">Erstellen in unserem einfachen Beispiel erneut, wenn der Anwendung eine "" Fenstergröße von 10 verwendet wird, legen Sie tatsächlich die maximale Anzahl von Elementen, die zur 11 zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="2db1d-201">Building again on our simple example, if your application is using a "window" size of 10, you actually set the maximum number of items to return to 11.</span></span> <span data-ttu-id="2db1d-202">Die Anwendung verarbeitet die ersten 10 Elemente in der Antwort auf wie gewohnt.</span><span class="sxs-lookup"><span data-stu-id="2db1d-202">Your application processes the first 10 items in the response as usual.</span></span> <span data-ttu-id="2db1d-203">Für das letzte Element der Element-ID als Anker speichern und dann die nächste Anforderung mit einem Offset von 10 ausstellen.</span><span class="sxs-lookup"><span data-stu-id="2db1d-203">For the last item, you save the item's identifier as an anchor, then issue the next request with an offset of 10.</span></span> <span data-ttu-id="2db1d-204">Wenn die Daten nicht geändert wurde, sollte das erste Element in der zweiten Antwort eine Element-ID, die mit den Anker übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="2db1d-204">If the data has not changed, the first item in the second response should have an item identifier that matches the anchor.</span></span> <span data-ttu-id="2db1d-205">Wenn die Element-IDs nicht übereinstimmen, wissen Sie, dass die Daten wurden entfernt oder in den Teilen der Liste, die Sie bereits "ausgelagert haben" eingefügt über.</span><span class="sxs-lookup"><span data-stu-id="2db1d-205">If the item identifiers don't match, you know that the data has been removed or inserted in the parts of the list you have already "paged" over.</span></span>
  
<span data-ttu-id="2db1d-206">Auch wenn Sie wissen, dass die Daten geändert haben, müssen Sie dennoch entscheiden, wie Sie reagieren.</span><span class="sxs-lookup"><span data-stu-id="2db1d-206">Even when you know that the data has changed, you still need to decide how to react.</span></span> <span data-ttu-id="2db1d-207">Es ist nicht entweder eine Stange Antwort für diese Frage ein.</span><span class="sxs-lookup"><span data-stu-id="2db1d-207">There isn't a one-size-fits-all answer for this question either.</span></span> <span data-ttu-id="2db1d-208">Ihre Aktionen hängt die Art der Anwendung und wie wichtig die Erfassen aller Elemente ist.</span><span class="sxs-lookup"><span data-stu-id="2db1d-208">Your actions will depend on the nature of your application and how critical it is to capture all items.</span></span> <span data-ttu-id="2db1d-209">Möglicherweise vollständig zu ignorieren, starten den Prozess von der Anfang oder Sichern nachverfolgen und versuchen, zu ermitteln, in dem die Änderung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2db1d-209">You might ignore it altogether, restart the process from the beginning, or back track and try to detect where the change happened.</span></span>
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a><span data-ttu-id="2db1d-210">Beispiel: Führen Sie eine ausgelagerte Suche mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="2db1d-210">Example: Perform a paged search by using the EWS Managed API</span></span>
<span data-ttu-id="2db1d-211"><a name="bk_PagedSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="2db1d-211"></span></span>

<span data-ttu-id="2db1d-212">Paging wird von den folgenden EWS Managed API-Methoden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2db1d-212">Paging is supported by the following EWS Managed API methods:</span></span>
  
- [<span data-ttu-id="2db1d-213">ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="2db1d-213">ExchangeService.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="2db1d-214">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="2db1d-214">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="2db1d-215">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="2db1d-215">Folder.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="2db1d-216">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="2db1d-216">Folder.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="2db1d-217">Wenn Sie die EWS Managed API verwenden, wird die Anwendung Paging mit der Klasse [aufrufenArtikel aufrufen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) oder [FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) konfiguriert und empfängt Informationen von dem Server im Hinblick auf Paging von [FindItemsResults](http://msdn.microsoft.com/en-us/library/dd635381%28v=exchg.80%29.aspx) oder [FindFoldersResults](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="2db1d-217">If you are using the EWS Managed API, your application configures paging with the [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) or [FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) class and receives information from the server regarding paging from the [FindItemsResults](http://msdn.microsoft.com/en-us/library/dd635381%28v=exchg.80%29.aspx) or [FindFoldersResults](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) class.</span></span> 
  
<span data-ttu-id="2db1d-218">Das folgende Beispiel ruft alle Elemente in einem Ordner mithilfe einer ausgelagerten Suche, die fünf Elemente in jeder Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2db1d-218">The following example retrieves all the items in a folder using a paged search that returns five items in each response.</span></span> <span data-ttu-id="2db1d-219">Es ruft auch ein weiteres Element dienen als Anker zum Erkennen von Änderungen an die Ergebnisse auf dem Server ab.</span><span class="sxs-lookup"><span data-stu-id="2db1d-219">It also retrieves an additional item to serve as an anchor to detect changes to the results on the server.</span></span> 
  
<span data-ttu-id="2db1d-220">In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2db1d-220">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

## <a name="example-perform-a-paged-search-by-using-ews"></a><span data-ttu-id="2db1d-221">Beispiel: Führen Sie eine ausgelagerte Suche mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="2db1d-221">Example: Perform a paged search by using EWS</span></span>
<span data-ttu-id="2db1d-222"><a name="bk_PagedSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="2db1d-222"></span></span>

<span data-ttu-id="2db1d-223">Paging wird durch folgende EWS-Vorgänge unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2db1d-223">Paging is supported by the following EWS operations:</span></span>
  
- [<span data-ttu-id="2db1d-224">FindFolder</span><span class="sxs-lookup"><span data-stu-id="2db1d-224">FindFolder</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="2db1d-225">FindItem</span><span class="sxs-lookup"><span data-stu-id="2db1d-225">FindItem</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
<span data-ttu-id="2db1d-226">Wenn Sie Exchange-Webdienste verwenden, wird die Anwendung Paging mit der [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) -Element oder das Element [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) konfiguriert und empfängt Informationen von dem Server im Hinblick auf Paging aus der [RootFolder () FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) Element oder das Element [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2db1d-226">If you're using EWS, your application configures paging with the [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element and receives information from the server regarding paging from the [RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="2db1d-227">In diesem anforderungsbeispiel wird eine **FindItem** -Anforderung für ein Maximum von sechs Elementen, beginnend bei einem Offset 0 (null) am Anfang der Liste der Elemente im Posteingang des Benutzers gesendet.</span><span class="sxs-lookup"><span data-stu-id="2db1d-227">In this request example, a **FindItem** request is sent for a maximum of six items, starting at an offset of zero from the beginning of the list of items in the user's Inbox.</span></span> 
  
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

<span data-ttu-id="2db1d-228">Der Server gibt die folgende Antwort, die sechs Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="2db1d-228">The server returns the following response, which contains six items.</span></span> <span data-ttu-id="2db1d-229">Die Antwort gibt auch an, dass insgesamt acht Elemente in den Ergebnissen auf dem Server vorhanden sind und dass das letzte Element in der Liste "Suchergebnisse" nicht in der Antwort vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2db1d-229">The response also indicates that there are a total of eight items in the results on the server, and that the last item in the results list is not present in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
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

<span data-ttu-id="2db1d-230">In diesem Beispiel wird die gleiche Anforderung wird gesendet, aber diesmal das **Offset** -Attribut auf fünf, die angibt, dass der Server maximal sechs Artikel beginnend am Offset fünf vom Anfang zurückgegeben werden soll, geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2db1d-230">In this example, the same request is sent, but this time, the **Offset** attribute is changed to five, which indicates that the server should return at most six items starting at offset five from the beginning.</span></span> 
  
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

<span data-ttu-id="2db1d-231">Der Server sendet die folgende Antwort, die drei Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="2db1d-231">The server sends the following response, which contains three items.</span></span> <span data-ttu-id="2db1d-232">Die Antwort gibt auch an, dass die Gesamtanzahl der Elemente in den Ergebnissen auf dem Server ist weiterhin acht festgelegt, und das letzte Element in den Ergebnissen Liste in der Antwort enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2db1d-232">The response also indicates that the total number of items in the results on the server is still eight, and that the last item in the results list is included in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
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

## <a name="see-also"></a><span data-ttu-id="2db1d-233">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2db1d-233">See also</span></span>


- [<span data-ttu-id="2db1d-234">Suche und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2db1d-234">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="2db1d-235">ExchangeService.FindFolders-Methode</span><span class="sxs-lookup"><span data-stu-id="2db1d-235">ExchangeService.FindFolders method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="2db1d-236">ExchangeService.FindItems-Methode</span><span class="sxs-lookup"><span data-stu-id="2db1d-236">ExchangeService.FindItems method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="2db1d-237">Folder.FindFolders-Methode</span><span class="sxs-lookup"><span data-stu-id="2db1d-237">Folder.FindFolders method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="2db1d-238">Folder.FindFolders-Methode</span><span class="sxs-lookup"><span data-stu-id="2db1d-238">Folder.FindFolders method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="2db1d-239">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="2db1d-239">FindFolder operation</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="2db1d-240">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2db1d-240">FindItem operation</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [<span data-ttu-id="2db1d-241">EWS-Einschränkung in Exchange</span><span class="sxs-lookup"><span data-stu-id="2db1d-241">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    

