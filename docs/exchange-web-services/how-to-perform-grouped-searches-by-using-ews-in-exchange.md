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
# <a name="perform-grouped-searches-by-using-ews-in-exchange"></a><span data-ttu-id="4d09f-103">Durchführen gruppierter Suchen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="4d09f-103">Perform grouped searches by using EWS in Exchange</span></span>

<span data-ttu-id="4d09f-104">Erfahren Sie, wie Sie gruppierte Suchvorgänge in ihrer verwaltete EWS-API-oder EWS-Anwendung durchführen, die auf Exchange abzielt.</span><span class="sxs-lookup"><span data-stu-id="4d09f-104">Find out how to perform grouped searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="4d09f-105">Gruppierte Suchvorgänge sind hilfreich, da Sie Ihnen die Kontrolle darüber geben, wie Suchergebnisse organisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4d09f-105">Grouped searches are useful in that they gives you control over how search results are organized.</span></span> <span data-ttu-id="4d09f-106">Organisierte Suchergebnisse können es Ihrer Anwendung erleichtern, Ergebnisse zu verarbeiten oder Sie auf eine verwaltbare Weise an einen Endbenutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4d09f-106">Organized search results can make it easier for your application to process results or display them to an end user in a manageable way.</span></span>
  
<span data-ttu-id="4d09f-107">Die Gruppierung funktioniert, indem alle Elemente innerhalb des Resultsets mit dem gleichen Wert eines bestimmten Felds in einer Gruppe eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4d09f-107">Grouping works by putting all items within the result set that have the same value of a specific field into a group.</span></span> <span data-ttu-id="4d09f-108">Beispielsweise können Sie Ihre Ergebnisse nach dem Absender gruppieren, und alle Elemente derselben Person befinden sich in einer separaten Gruppe, und die Elemente innerhalb jeder Gruppe werden entsprechend der in der Ansicht angegebenen Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="4d09f-108">For example, you can group your results by the sender, and all items from the same person will be in a separate group, and the items within each group will be sorted according to the order you specify on the view.</span></span> <span data-ttu-id="4d09f-109">Die Gruppen selbst werden nach einem aggregierten Wert basierend auf einem von Ihnen ausgewählten Feld sortiert.</span><span class="sxs-lookup"><span data-stu-id="4d09f-109">The groups themselves are sorted by an aggregate value based on a field you choose.</span></span>
  
<span data-ttu-id="4d09f-110">**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge zum Organisieren von Suchergebnissen**</span><span class="sxs-lookup"><span data-stu-id="4d09f-110">**Table 1. EWS Managed API methods and EWS operations for organizing search results**</span></span>

|<span data-ttu-id="4d09f-111">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="4d09f-111">**If you want to…**</span></span>|<span data-ttu-id="4d09f-112">**Verwenden Sie im verwaltete EWS-API die...**</span><span class="sxs-lookup"><span data-stu-id="4d09f-112">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="4d09f-113">**Verwenden Sie in EWS die...**</span><span class="sxs-lookup"><span data-stu-id="4d09f-113">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4d09f-114">Organisieren von Elementen mit dem gleichen Wert in einer bestimmten Eigenschaft in ihren Ergebnissen in Gruppen</span><span class="sxs-lookup"><span data-stu-id="4d09f-114">Organize items with the same value in a specific property in your results into groups</span></span>  <br/> |[<span data-ttu-id="4d09f-115">GROUPING. GroupOn</span><span class="sxs-lookup"><span data-stu-id="4d09f-115">Grouping.GroupOn</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.groupon%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="4d09f-116">[FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) -Element als untergeordnetes Element des [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) -Elements</span><span class="sxs-lookup"><span data-stu-id="4d09f-116">[FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) element as a child of the [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="4d09f-117">Sortieren von Elementen innerhalb jeder Gruppe nach dem Wert in einer bestimmten Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d09f-117">Sort items within each group by the value in a specific property</span></span>  <br/> |[<span data-ttu-id="4d09f-118">ItemView. OrderBy</span><span class="sxs-lookup"><span data-stu-id="4d09f-118">ItemView.OrderBy</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="4d09f-119">[Sortierreihenfolge](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) -Element</span><span class="sxs-lookup"><span data-stu-id="4d09f-119">[SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="4d09f-120">Sortieren der Gruppen</span><span class="sxs-lookup"><span data-stu-id="4d09f-120">Sort the groups</span></span>  <br/> |[<span data-ttu-id="4d09f-121">GROUPING. AggregateOn</span><span class="sxs-lookup"><span data-stu-id="4d09f-121">Grouping.AggregateOn</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) <br/><br/> [<span data-ttu-id="4d09f-122">GROUPING. aggregattype</span><span class="sxs-lookup"><span data-stu-id="4d09f-122">Grouping.AggregateType</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) <br/><br/> [<span data-ttu-id="4d09f-123">GROUPING. SortDirection</span><span class="sxs-lookup"><span data-stu-id="4d09f-123">Grouping.SortDirection</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="4d09f-124">**FieldURI** -Element als untergeordnetes Element des [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) -Elements</span><span class="sxs-lookup"><span data-stu-id="4d09f-124">**FieldURI** element as a child of the [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) element</span></span><br/><br/> <span data-ttu-id="4d09f-125">**Aggregate** -Attribut für das **AggregateOn** -Element</span><span class="sxs-lookup"><span data-stu-id="4d09f-125">**Aggregate** attribute on the **AggregateOn** element</span></span><br/><br/><span data-ttu-id="4d09f-126">**Order** -Attribut für das **GroupBy** -Element</span><span class="sxs-lookup"><span data-stu-id="4d09f-126">**Order** attribute on the **GroupBy** element</span></span>  <br/> |
   
<span data-ttu-id="4d09f-127">Lassen Sie uns Schritt für Schritt vorgehen.</span><span class="sxs-lookup"><span data-stu-id="4d09f-127">Let's take it step by step.</span></span>
  
## <a name="group-results-by-a-specific-property"></a><span data-ttu-id="4d09f-128">Gruppieren von Ergebnissen nach einer bestimmten Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d09f-128">Group results by a specific property</span></span>
<span data-ttu-id="4d09f-129"><a name="bk_GroupResults"> </a></span><span class="sxs-lookup"><span data-stu-id="4d09f-129"><a name="bk_GroupResults"> </a></span></span>

<span data-ttu-id="4d09f-130">Der erste Schritt bei der Verwendung von Gruppierungen besteht darin, eine Eigenschaft oder ein Attribut für die Elemente im Exchange-Informationsspeicher auszuwählen, um nach Group by zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="4d09f-130">The first step to using grouping is to select a property, or attribute on the items in the Exchange store, to group by.</span></span> <span data-ttu-id="4d09f-131">Das verwaltete EWS-API macht diese als Klassen Eigenschaften für die entsprechenden Klassen verfügbar, während EWS Sie als XML-Elemente verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="4d09f-131">The EWS Managed API exposes these as class properties on the corresponding classes, while EWS exposes them as XML elements.</span></span> <span data-ttu-id="4d09f-132">Sie können eine beliebige Eigenschaft, einschließlich benutzerdefinierter oder erweiterter Eigenschaften, auswählen, es ist jedoch hilfreich zu verstehen, wie Elemente basierend auf dem Wert der ausgewählten Eigenschaft gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="4d09f-132">You can choose any property, including custom or extended properties, but it is helpful to understand how items are grouped based on the value of the property you choose.</span></span> 

<span data-ttu-id="4d09f-133">Alle Elemente mit dem gleichen Wert in der Eigenschaft, die Sie für die Gruppierung auswählen, werden zusammen gruppiert.</span><span class="sxs-lookup"><span data-stu-id="4d09f-133">All items that have the same value in the property you choose to group by will be grouped together.</span></span> <span data-ttu-id="4d09f-134">Dies scheint zwar offensichtlich zu sein, es handelt sich jedoch um ein wichtiges Detail.</span><span class="sxs-lookup"><span data-stu-id="4d09f-134">This might seem obvious, but it is an important detail.</span></span> <span data-ttu-id="4d09f-135">Stellen Sie sich vor, was passiert, wenn Sie nach einer Date/Time-Eigenschaft gruppieren, wie beispielsweise [Item. DateTimeReceived](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx) im verwaltete EWS-API oder das [DateTimeReceived](https://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx) -Element in EWS.</span><span class="sxs-lookup"><span data-stu-id="4d09f-135">Consider what happens if you group by a date/time property, such as [Item.DateTimeReceived](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx) in the EWS Managed API, or the [DateTimeReceived](https://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="4d09f-136">Die Absicht besteht darin, die Ergebnisse in Gruppen zu organisieren, wobei jede Gruppe Elemente vom selben Tag enthält.</span><span class="sxs-lookup"><span data-stu-id="4d09f-136">The intent might be to organize the results into groups, with each group containing items from the same day.</span></span> <span data-ttu-id="4d09f-137">Bei der Gruppierung wird jedoch der gesamte Wert untersucht, der die Uhrzeit enthält.</span><span class="sxs-lookup"><span data-stu-id="4d09f-137">However, grouping looks at the entire value, which includes the time.</span></span> 

<span data-ttu-id="4d09f-138">Das Endergebnis ist, dass die Elemente so gruppiert werden, dass Elemente, die gleichzeitig empfangen werden, bis zum zweiten, in ihren eigenen Gruppen liegen.</span><span class="sxs-lookup"><span data-stu-id="4d09f-138">The end result is that the items will be grouped so that items received at the same time, down to the second, are in their own groups.</span></span> <span data-ttu-id="4d09f-139">Die Ergebnisse werden höchstwahrscheinlich in eine große Anzahl von Gruppen mit einer kleinen Anzahl von Elementen in jeder Gruppe sortiert.</span><span class="sxs-lookup"><span data-stu-id="4d09f-139">The results will most likely be sorted into a large number of groups with a small number of items in each group.</span></span> 
  
<span data-ttu-id="4d09f-140">Wenn Sie ein Resultset mit einer kleineren Anzahl von Gruppen und einer größeren Anzahl von Elementen in jeder Gruppe abrufen möchten, wählen Sie eine Eigenschaft aus, bei der es sich wahrscheinlich um eine geringere Anzahl von Werten wie [Email Message. from](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx) oder [Item. categories](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx) im verwaltete EWS-API [From](https://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx) oder aus [Kategorien](https://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx) in EWS handelt.</span><span class="sxs-lookup"><span data-stu-id="4d09f-140">To get a results set with a smaller number of groups and a larger number of items in each group, choose a property that is likely to have a smaller number of values, such as [EmailMessage.From](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx) or [Item.Categories](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx) in the EWS Managed API, or [From](https://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx) or [Categories](https://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx) in EWS.</span></span> <span data-ttu-id="4d09f-141">Die folgende Abbildung zeigt eine Liste von e-Mails, die in einem Posteingang angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4d09f-141">The following figure shows a list of emails that appear in an Inbox.</span></span> 
  
<span data-ttu-id="4d09f-142">**Abbildung 1. Nachrichten in einem Posteingang**</span><span class="sxs-lookup"><span data-stu-id="4d09f-142">**Figure 1. Messages in an Inbox**</span></span>

![Eine Beispielliste von Nachrichten im Posteingang eines Benutzers.](media/Ex15_GroupedSearch_MsgList.png)
  
<span data-ttu-id="4d09f-144">Wenn Sie die Elemente in Abbildung 1 durch die **Email Message. from** -Eigenschaft gruppieren, werden zwei Gruppen angezeigt: eine für Nachrichten, die von Hope Brutto gesendet wurden, und eine für Nachrichten, die von Sadie Daniels gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="4d09f-144">If you group the items in Figure 1 by the **EmailMessage.From** property, the result will be two groups, one for messages sent by Hope Gross, and one for messages sent by Sadie Daniels.</span></span> 
  
<span data-ttu-id="4d09f-145">**Abbildung 2. Nachrichten, die basierend auf der From-Eigenschaft in Gruppen unterteilt sind**</span><span class="sxs-lookup"><span data-stu-id="4d09f-145">**Figure 2. Messages separated into groups based on the From property**</span></span>

![Abbildung, in der in zwei Listen anhand der Eigenschaft "Von" sortierte Nachrichten gezeigt werden.](media/Ex15_GroupedSearch_SeparateGroups.png)
  
## <a name="sort-the-items-within-groups"></a><span data-ttu-id="4d09f-147">Sortieren der Elemente in Gruppen</span><span class="sxs-lookup"><span data-stu-id="4d09f-147">Sort the items within groups</span></span>
<span data-ttu-id="4d09f-148"><a name="bk_SortItems"> </a></span><span class="sxs-lookup"><span data-stu-id="4d09f-148"><a name="bk_SortItems"> </a></span></span>

<span data-ttu-id="4d09f-149">Sie können steuern, wie Elemente innerhalb jeder Gruppe sortiert werden, indem Sie die [ItemView. OrderBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) -Eigenschaft in der verwaltete EWS-API oder das Element " [Sortierreihenfolge](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) " in EWS verwenden.</span><span class="sxs-lookup"><span data-stu-id="4d09f-149">You can control how items are sorted within each group by using the [ItemView.OrderBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) property in the EWS Managed API, or the [SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="4d09f-150">Die gleiche Reihenfolge gilt für jede Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4d09f-150">The same ordering applies to each group.</span></span> <span data-ttu-id="4d09f-151">Wenn Sie beispielsweise die Elemente aus Abbildung 1 nach der **Item. DateTimeReceived** -Eigenschaft in absteigender Reihenfolge sortieren, wird das Element, das zuletzt von Hope Brutto empfangen wurde, zuerst in der Hope-Brutto Gruppe angezeigt, und das Element, das zuletzt von Sadie Daniels empfangen wurde, wird zuerst in der Sadie Daniels-Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="4d09f-151">For example, if you sort the items from Figure 1 by the **Item.DateTimeReceived** property, in descending order, the item most recently received from Hope Gross will be first in the Hope Gross group, and the item most recently received from Sadie Daniels will be first in the Sadie Daniels group.</span></span> <span data-ttu-id="4d09f-152">Bequem sind die Gruppen in Abbildung 2 bereits auf diese Weise sortiert.</span><span class="sxs-lookup"><span data-stu-id="4d09f-152">Conveniently, the groups in Figure 2 are already sorted this way.</span></span> 
  
## <a name="sort-the-groups"></a><span data-ttu-id="4d09f-153">Sortieren der Gruppen</span><span class="sxs-lookup"><span data-stu-id="4d09f-153">Sort the groups</span></span>
<span data-ttu-id="4d09f-154"><a name="bk_SortGroups"> </a></span><span class="sxs-lookup"><span data-stu-id="4d09f-154"><a name="bk_SortGroups"> </a></span></span>

<span data-ttu-id="4d09f-155">Nachdem Sie Ihre Gruppen abgewickelt haben, besteht der letzte Schritt darin, die Gruppen selbst zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="4d09f-155">Now that you have your groups settled, the final step is sorting the groups themselves.</span></span> <span data-ttu-id="4d09f-156">Da die Gruppen selbst keine spezifischen Werte haben, muss der Gruppierungs Prozess jeder Gruppe einen Sortierwert zuweisen.</span><span class="sxs-lookup"><span data-stu-id="4d09f-156">Because the groups themselves have no specific values, the grouping process has to assign a sort value to each group.</span></span> <span data-ttu-id="4d09f-157">Dies erfolgt durch Aggregation der Werte einer bestimmten Eigenschaft innerhalb jeder Gruppe, die durch die [Grouping. AggregateOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) -Eigenschaft in der verwaltete EWS-API oder das [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) -Element als untergeordnetes Element des [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) -Elements in EWS angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4d09f-157">This is done by aggregation of the values of a specific property within each group, specified by the [Grouping.AggregateOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) property in the EWS Managed API, or the [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) element as a child of the [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="4d09f-158">Die [Grouping. aggregattype](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) -Eigenschaft in der verwaltete EWS-API (oder das **Aggregate** -Attribut für das **AggregateOn** -Element in EWS) gibt an, welcher Wert aus den Elementen innerhalb jeder Gruppe dem Sortierwert für die Gruppe zugewiesen ist, entweder den größten oder den kleinsten Wert.</span><span class="sxs-lookup"><span data-stu-id="4d09f-158">The [Grouping.AggregateType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) property in the EWS Managed API (or the **Aggregate** attribute on the **AggregateOn** element in EWS) specifies which value from the items within each group is assigned to the sort value for the group — either the largest value or the smallest value.</span></span> <span data-ttu-id="4d09f-159">Schließlich wird die Sortierreihenfolge (absteigend oder aufsteigend) durch die [Grouping. SortDirection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) -Eigenschaft im verwaltete EWS-API oder das **Order** -Attribut für das [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) -Element in EWS angegeben.</span><span class="sxs-lookup"><span data-stu-id="4d09f-159">Finally, the sort order (descending or ascending) is specified by the [Grouping.SortDirection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) property in the EWS Managed API, or the **Order** attribute on the [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) element in EWS.</span></span> 
  
<span data-ttu-id="4d09f-160">Wenn beispielsweise die Gruppen aus Abbildung 2 durch Aggregieren der **Item. DateTimeReceived** -Eigenschaft sortiert werden, wobei der kleinste Wert verwendet wird und die Sortierung in absteigender Reihenfolge erfolgt, werden die Elemente in der angegebenen Reihenfolge in Abbildung 3 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4d09f-160">For example, if the groups from Figure 2 are sorted by aggregating on the **Item.DateTimeReceived** property, using the smallest value, and sorting in descending order, the items are returned in the order in shown Figure 3.</span></span> 
  
<span data-ttu-id="4d09f-161">**Abbildung 3. Gruppierte Suchergebnisse mit den Gruppen, sortiert nach der DateTimeReceived-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="4d09f-161">**Figure 3. Grouped search results with the groups sorted by the DateTimeReceived property**</span></span>

![Abbildung einer sortierten Liste von Nachrichten (gruppiert anhand der Eigenschaft "Von"), in der die Gruppen nach dem jüngsten Empfangsdatum samt Uhrzeit sortiert sind.](media/Ex15_GroupedSearch_Results.png)
  
<span data-ttu-id="4d09f-163">In den nächsten Abschnitten erfahren Sie, wie Sie die Gruppierung und Sortierung in Code zusammenführen können.</span><span class="sxs-lookup"><span data-stu-id="4d09f-163">The next sections show you how you might pull grouping and sorting together in code.</span></span>
  
## <a name="example-perform-a-grouped-search-by-using-the-ews-managed-api"></a><span data-ttu-id="4d09f-164">Beispiel: Durchführen einer gruppierten Suche mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="4d09f-164">Example: Perform a grouped search by using the EWS Managed API</span></span>
<span data-ttu-id="4d09f-165"><a name="bk_GroupSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="4d09f-165"><a name="bk_GroupSearchEWSMA"> </a></span></span>

<span data-ttu-id="4d09f-166">Die folgenden verwaltete EWS-API Methoden können die Gruppierung verwenden:</span><span class="sxs-lookup"><span data-stu-id="4d09f-166">The following EWS Managed API methods can use grouping:</span></span>
  
- [<span data-ttu-id="4d09f-167">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="4d09f-167">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="4d09f-168">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="4d09f-168">Folder.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="4d09f-169">Im folgenden Beispiel wird die **Datei "ExchangeService. FindItems** -Methode verwendet; die gleichen Regeln und Konzepte gelten jedoch für die **Folder. FindItems** -Methode.</span><span class="sxs-lookup"><span data-stu-id="4d09f-169">The following example uses the **ExchangeService.FindItems** method; however, the same rules and concepts apply to the **Folder.FindItems** method.</span></span> <span data-ttu-id="4d09f-170">In diesem Beispiel wird eine Methode namens " **GroupItemsByFrom** " definiert.</span><span class="sxs-lookup"><span data-stu-id="4d09f-170">In this example, a method called **GroupItemsByFrom** is defined.</span></span> <span data-ttu-id="4d09f-171">Es akzeptiert ein [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt und ein [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) -Objekt als Parameter.</span><span class="sxs-lookup"><span data-stu-id="4d09f-171">It takes an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and a [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object as parameters.</span></span> <span data-ttu-id="4d09f-172">Die ersten 50-Elemente in dem Ordner werden angefordert, gruppiert nach der **Email Message. from** -Eigenschaft, sortiert nach der **Item. DateTimeReceived** -Eigenschaft in absteigender Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4d09f-172">It requests the first 50 items in the folder, grouped by the **EmailMessage.From** property, sorted by the **Item.DateTimeReceived** property in descending order.</span></span> <span data-ttu-id="4d09f-173">Die Gruppen selbst werden nach dem kleinsten **Item. DateTimeReceived** -Eigenschaftswert für ihre Elemente in absteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="4d09f-173">The groups themselves are sorted by the smallest **Item.DateTimeReceived** property value on their items, in descending order.</span></span> 
  
<span data-ttu-id="4d09f-174">In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4d09f-174">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

## <a name="example-perform-a-grouped-search-by-using-ews"></a><span data-ttu-id="4d09f-175">Beispiel: Ausführen einer gruppierten Suche mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="4d09f-175">Example: Perform a grouped search by using EWS</span></span>
<span data-ttu-id="4d09f-176"><a name="bk_GroupSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="4d09f-176"><a name="bk_GroupSearchEWS"> </a></span></span>

<span data-ttu-id="4d09f-177">Das folgende Anforderungs Beispiel zeigt eine [FindItem-Vorgangs](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) Anforderung für die ersten 50-Elemente im Ordner, gruppiert nach dem **from** -Element, sortiert nach dem **DateTimeReceived** -Element in absteigender Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4d09f-177">The following request example shows a [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request for the first 50 items in the folder, grouped by the **From** element, sorted by the **DateTimeReceived** element in descending order.</span></span> <span data-ttu-id="4d09f-178">Die Gruppen selbst werden nach dem kleinsten **DateTimeReceived** -Elementwert für ihre Elemente in absteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="4d09f-178">The groups themselves are sorted by the smallest **DateTimeReceived** element value on their items, in descending order.</span></span> 
  
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

<span data-ttu-id="4d09f-179">Der Server gibt die folgende Antwort zurück.</span><span class="sxs-lookup"><span data-stu-id="4d09f-179">The server returns the following response.</span></span>
  
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

## <a name="version-differences"></a><span data-ttu-id="4d09f-180">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="4d09f-180">Version differences</span></span>
<span data-ttu-id="4d09f-181"><a name="bk_VersionDiffs"> </a></span><span class="sxs-lookup"><span data-stu-id="4d09f-181"><a name="bk_VersionDiffs"> </a></span></span>

<span data-ttu-id="4d09f-182">Versionen von Exchange, die mit der Hauptversion 15 beginnen und mit Build 15.0.775.38 zurückgegeben werden, geben **Gruppen** Elemente (vom Typ **GroupedItemsType**) anstelle von [GroupedItems](https://msdn.microsoft.com/library/53170df4-4272-4b37-b23f-cd8e2d4a7396%28Office.15%29.aspx) -Elementen in der SOAP-Antwort zurück.</span><span class="sxs-lookup"><span data-stu-id="4d09f-182">Versions of Exchange starting with major version 15 and ending with build 15.0.775.38 return **Group** elements (of type **GroupedItemsType**) in place of [GroupedItems](https://msdn.microsoft.com/library/53170df4-4272-4b37-b23f-cd8e2d4a7396%28Office.15%29.aspx) elements in the SOAP response.</span></span> <span data-ttu-id="4d09f-183">Wenn Sie die verwaltete EWS-API verwenden, führt dies dazu, dass die [GroupedFindItemsResults. ItemGroups](https://msdn.microsoft.com/library/office/dd633961%28v=exchg.80%29.aspx) -Auflistung 0-Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="4d09f-183">If you are using the EWS Managed API, this will cause the [GroupedFindItemsResults.ItemGroups](https://msdn.microsoft.com/library/office/dd633961%28v=exchg.80%29.aspx) collection to contain 0 objects.</span></span> <span data-ttu-id="4d09f-184">Wenn Sie EWS verwenden, sollten **Group** -Elemente als **GroupedItems** -Elemente behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="4d09f-184">If you are using EWS, **Group** elements should be handled as **GroupedItems** elements.</span></span> 
  
<span data-ttu-id="4d09f-185">Versionen von Exchange, die mit der Hauptversion 15 beginnen, geben zusätzliche **Group** -oder **GroupedItems** -Elemente zurück, wobei das **xsi: Nil** -Attribut in der SOAP-Antwort auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4d09f-185">Versions of Exchange starting with major version 15 return extra **Group** or **GroupedItems** elements with the **xsi:nil** attribute set to **true** in the SOAP response.</span></span> <span data-ttu-id="4d09f-186">Wenn Sie die verwaltete EWS-API verwenden, führen diese zusätzlichen Elemente dazu, dass ein [ServiceXmlDeserializationException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.servicexmldeserializationexception%28v=exchg.80%29.aspx) -Objekt ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="4d09f-186">If you are using the EWS Managed API, these extra elements will cause a [ServiceXmlDeserializationException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.servicexmldeserializationexception%28v=exchg.80%29.aspx) to be thrown.</span></span> <span data-ttu-id="4d09f-187">Wenn Sie EWS verwenden, sollten diese zusätzlichen Elemente ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="4d09f-187">If you are using EWS, these extra elements should be ignored.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d09f-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d09f-188">See also</span></span>

- [<span data-ttu-id="4d09f-189">Suche und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="4d09f-189">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="4d09f-190">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="4d09f-190">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="4d09f-191">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="4d09f-191">Folder.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)   
- [<span data-ttu-id="4d09f-192">GROUPING-Klasse</span><span class="sxs-lookup"><span data-stu-id="4d09f-192">Grouping class</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="4d09f-193">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4d09f-193">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

