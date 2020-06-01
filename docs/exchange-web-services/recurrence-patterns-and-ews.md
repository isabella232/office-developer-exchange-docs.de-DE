---
title: Serienmuster und EWS
manager: luken
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fd9ef706-1e01-49fa-af6f-2f6d3e173c16
description: Erfahren Sie mehr über Serienmuster und wiederkehrende Datenreihen in Exchange.
ms.openlocfilehash: 681dfee7e0a66a483b8638810da5e4e0ac0f05ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459328"
---
# <a name="recurrence-patterns-and-ews"></a><span data-ttu-id="413c6-103">Serienmuster und EWS</span><span class="sxs-lookup"><span data-stu-id="413c6-103">Recurrence patterns and EWS</span></span>

<span data-ttu-id="413c6-104">Erfahren Sie mehr über Serienmuster und wiederkehrende Datenreihen in Exchange.</span><span class="sxs-lookup"><span data-stu-id="413c6-104">Learn about recurrence patterns and recurring series in Exchange.</span></span>
  
<span data-ttu-id="413c6-105">Eine wiederkehrende Reihe ist ein Termin oder eine Besprechung, die nach einem definierten Muster wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="413c6-105">A recurring series is an appointment or meeting that repeats according to a defined pattern.</span></span> <span data-ttu-id="413c6-106">Eine wiederkehrende Datenreihe kann entweder eine bestimmte Anzahl von Vorkommen aufweisen oder unbegrenzt wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="413c6-106">A recurring series can either have a specific number of occurrences or can repeat indefinitely.</span></span> <span data-ttu-id="413c6-107">Darüber hinaus kann eine wiederkehrende Reihe Ausnahmen aufweisen, die nicht dem Muster der restlichen Vorkommen entsprechen und möglicherweise vorkommen aufweisen, die aus dem Muster gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="413c6-107">Additionally, a recurring series can have exceptions that don't follow the pattern of the rest of the occurrences, and can have occurrences that have been deleted from the pattern.</span></span> <span data-ttu-id="413c6-108">Sie können die verwaltete EWS-API und EWS verwenden, um mit wiederkehrenden Datenreihen und deren zugeordneten Kalenderelementen zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="413c6-108">You can use the EWS Managed API and EWS to work with recurring series and their associated calendar items.</span></span>
  
## <a name="recurring-calendar-items"></a><span data-ttu-id="413c6-109">Wiederkehrende Kalenderelemente</span><span class="sxs-lookup"><span data-stu-id="413c6-109">Recurring calendar items</span></span>

<span data-ttu-id="413c6-110">Alle Kalenderelemente fallen in eine der folgenden vier Kategorien:</span><span class="sxs-lookup"><span data-stu-id="413c6-110">All calendar items fall into one of the following four categories:</span></span>
  
- <span data-ttu-id="413c6-111">Nicht wiederkehrende Kalenderelemente</span><span class="sxs-lookup"><span data-stu-id="413c6-111">Non-recurring calendar items</span></span>
    
- <span data-ttu-id="413c6-112">Wiederkehrende Master</span><span class="sxs-lookup"><span data-stu-id="413c6-112">Recurring masters</span></span>
    
- <span data-ttu-id="413c6-113">Vorkommen in einer Datenreihe</span><span class="sxs-lookup"><span data-stu-id="413c6-113">Occurrences in a series</span></span>
    
- <span data-ttu-id="413c6-114">Geänderte Vorkommen in einer Datenreihe, die als Ausnahmen bezeichnet werden</span><span class="sxs-lookup"><span data-stu-id="413c6-114">Modified occurrences in a series, known as exceptions</span></span>
    
<span data-ttu-id="413c6-115">In diesem Artikel sehen wir uns die drei Arten von Kalenderelementen an, die Teil einer wiederkehrenden Reihe sind.</span><span class="sxs-lookup"><span data-stu-id="413c6-115">In this article, we'll look at the three types of calendar items that are part of a recurring series.</span></span>
  
<span data-ttu-id="413c6-116">Es ist hilfreich zu verstehen, wie wiederkehrende Datenreihen auf dem Exchange-Server implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="413c6-116">It's helpful to understand how recurring series are implemented on the Exchange server.</span></span> <span data-ttu-id="413c6-117">Anstatt ein separates unterschiedliches Element für jedes Vorkommen in einer Terminserie zu erstellen, erstellt der Server nur ein tatsächliches Element im Kalender, das als wiederkehrendes Master-Objekt bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="413c6-117">Instead of creating a separate distinct item for each occurrence in a recurring series, the server creates only one actual item in the calendar, known as the recurring master.</span></span> <span data-ttu-id="413c6-118">Das Format eines wiederkehrenden Masters ähnelt einem Termin mit Wiederholungsmuster Informationen sehr ähnlich wie eine Terminserie.</span><span class="sxs-lookup"><span data-stu-id="413c6-118">The format of a recurring master is very similar to a non-recurring appointment, with the addition of recurrence pattern information.</span></span> <span data-ttu-id="413c6-119">Der Server generiert dann basierend auf dem Serienmuster als Reaktion auf Clientanforderungen für Termininformationen unter Verwendung eines Prozesses namens Expansion Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="413c6-119">The server then generates occurrences based on the recurrence pattern in response to client requests for appointment information, using a process called expansion.</span></span> <span data-ttu-id="413c6-120">Diese generierten vorkommen werden nicht dauerhaft auf dem Server gespeichert.</span><span class="sxs-lookup"><span data-stu-id="413c6-120">These generated occurrences are not permanently stored on the server.</span></span> <span data-ttu-id="413c6-121">Dies ist wichtig zu verstehen, da die Art und Weise, wie Sie nach Kalenderelementen suchen, bestimmt, welche Informationen Sie erhalten und ob eine Erweiterung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="413c6-121">This is important to understand because the way that you search for calendar items determines what information you receive and whether expansion occurs.</span></span>
  
## <a name="recurrence-patterns"></a><span data-ttu-id="413c6-122">Serienmuster</span><span class="sxs-lookup"><span data-stu-id="413c6-122">Recurrence patterns</span></span>

<span data-ttu-id="413c6-123">Das Schlüsselelement für eine wiederkehrende Reihe, die eine Erweiterung ermöglicht, ist das Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="413c6-123">The key piece to a recurring series that makes expansion possible is the recurrence pattern.</span></span> <span data-ttu-id="413c6-124">Das Serienmuster wird im wiederkehrenden Master gefunden und beschreibt einen Satz von Kriterien für die Berechnung von Vorkommen basierend auf dem Datum und der Uhrzeit des wiederkehrenden Masters.</span><span class="sxs-lookup"><span data-stu-id="413c6-124">The recurrence pattern is found on the recurring master, and describes a set of criteria for calculating occurrences based on the date and time of the recurring master.</span></span>
  
<span data-ttu-id="413c6-125">**Tabelle 1. Verfügbare Serienmuster**</span><span class="sxs-lookup"><span data-stu-id="413c6-125">**Table 1. Available recurrence patterns**</span></span>

|<span data-ttu-id="413c6-126">**Verwaltete EWS-API-Klasse**</span><span class="sxs-lookup"><span data-stu-id="413c6-126">**EWS Managed API class**</span></span>|<span data-ttu-id="413c6-127">**EWS-Element**</span><span class="sxs-lookup"><span data-stu-id="413c6-127">**EWS element**</span></span>|<span data-ttu-id="413c6-128">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="413c6-128">**Examples**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="413c6-129">Serie. DailyPattern</span><span class="sxs-lookup"><span data-stu-id="413c6-129">Recurrence.DailyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.dailypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="413c6-130">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="413c6-130">DailyRecurrence</span></span>](https://msdn.microsoft.com/library/0aaf265d-b723-49c6-8e9c-9ba60141e9ab%28Office.15%29.aspx) <br/> |<span data-ttu-id="413c6-131">Jeden Tag wiederholen.</span><span class="sxs-lookup"><span data-stu-id="413c6-131">Repeat every day.</span></span>  <br/> <span data-ttu-id="413c6-132">Jeden zweiten Tag wiederholen.</span><span class="sxs-lookup"><span data-stu-id="413c6-132">Repeat every other day.</span></span>  <br/> |
|[<span data-ttu-id="413c6-133">Serie. MonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="413c6-133">Recurrence.MonthlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.monthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="413c6-134">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="413c6-134">AbsoluteMonthlyRecurrence</span></span>](https://msdn.microsoft.com/library/178fa0ae-9dfc-417f-933c-d657d31c2161%28Office.15%29.aspx) <br/> |<span data-ttu-id="413c6-135">Wiederholen Sie jeden Monat am zehnten Tag des Monats.</span><span class="sxs-lookup"><span data-stu-id="413c6-135">Repeat every month on the tenth day of the month.</span></span>  <br/> <span data-ttu-id="413c6-136">Wiederholen Sie jeden zweiten Monat am 21. Tag des Monats.</span><span class="sxs-lookup"><span data-stu-id="413c6-136">Repeat every other month on the twenty-first day of the month.</span></span>  <br/> |
|[<span data-ttu-id="413c6-137">Serie. RelativeMonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="413c6-137">Recurrence.RelativeMonthlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativemonthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="413c6-138">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="413c6-138">RelativeMonthlyRecurrence</span></span>](https://msdn.microsoft.com/library/a76595db-7460-44ac-ac2a-53241caa33a7%28Office.15%29.aspx) <br/> |<span data-ttu-id="413c6-139">Am zweiten Dienstag jedes Monats wiederholen.</span><span class="sxs-lookup"><span data-stu-id="413c6-139">Repeat on the second Tuesday of every month.</span></span>  <br/> <span data-ttu-id="413c6-140">Wiederholen Sie diese Schritte am dritten Donnerstag des Monats alle drei Monate.</span><span class="sxs-lookup"><span data-stu-id="413c6-140">Repeat on the third Thursday of the month every three months.</span></span>  <br/> |
|[<span data-ttu-id="413c6-141">Serie. RelativeYearlyPattern</span><span class="sxs-lookup"><span data-stu-id="413c6-141">Recurrence.RelativeYearlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="413c6-142">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="413c6-142">RelativeYearlyRecurrence</span></span>](https://msdn.microsoft.com/library/25b67876-9979-4a30-a637-357ea10a93b8%28Office.15%29.aspx) <br/> |<span data-ttu-id="413c6-143">Wiederholen Sie diesen Vorgang am ersten Montag im August jedes Jahres.</span><span class="sxs-lookup"><span data-stu-id="413c6-143">Repeat on the first Monday of August every year.</span></span>  <br/> |
|[<span data-ttu-id="413c6-144">Serie. WeeklyPattern</span><span class="sxs-lookup"><span data-stu-id="413c6-144">Recurrence.WeeklyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.weeklypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="413c6-145">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="413c6-145">WeeklyRecurrence</span></span>](https://msdn.microsoft.com/library/69c41dd5-597c-45bc-be3f-e2f2b5615aa3%28Office.15%29.aspx) <br/> |<span data-ttu-id="413c6-146">Jeden Montag wiederholen.</span><span class="sxs-lookup"><span data-stu-id="413c6-146">Repeat every Monday.</span></span>  <br/> <span data-ttu-id="413c6-147">Wiederholen Sie jeden Dienstag und Donnerstag jede zweite Woche.</span><span class="sxs-lookup"><span data-stu-id="413c6-147">Repeat every Tuesday and Thursday every other week.</span></span>  <br/> |
|[<span data-ttu-id="413c6-148">Serie. YearlyPattern</span><span class="sxs-lookup"><span data-stu-id="413c6-148">Recurrence.YearlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="413c6-149">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="413c6-149">AbsoluteYearlyRecurrence</span></span>](https://msdn.microsoft.com/library/96f53e2c-3893-4f6e-a78a-ac179f45c5db%28Office.15%29.aspx) <br/> |<span data-ttu-id="413c6-150">Wiederholen Sie diesen Vorgang am 1. September jedes Jahr.</span><span class="sxs-lookup"><span data-stu-id="413c6-150">Repeat on September 1st every year.</span></span>  <br/> |
   
<span data-ttu-id="413c6-151">Die andere wichtige Information für ein Serienmuster ist, wenn die Serie endet.</span><span class="sxs-lookup"><span data-stu-id="413c6-151">The other important piece of information for a recurrence pattern is when the recurrence ends.</span></span> <span data-ttu-id="413c6-152">Dies kann entweder als festgelegte Anzahl von vorkommen als Enddatum oder als kein Ende angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="413c6-152">This can be expressed as either a set number of occurrences, as an end date, or as having no end.</span></span>
  
<span data-ttu-id="413c6-153">**Tabelle 2. Optionen für das Ende einer Terminserie**</span><span class="sxs-lookup"><span data-stu-id="413c6-153">**Table 2. Options for the end of a recurring series**</span></span>

|<span data-ttu-id="413c6-154">**Verwaltete EWS-API-Methode/-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="413c6-154">**EWS Managed API method/property**</span></span>|<span data-ttu-id="413c6-155">**EWS-Element**</span><span class="sxs-lookup"><span data-stu-id="413c6-155">**EWS element**</span></span>|<span data-ttu-id="413c6-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="413c6-156">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="413c6-157">Serie. NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="413c6-157">Recurrence.NumberOfOccurrences</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.numberofoccurrences%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="413c6-158">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="413c6-158">NumberedRecurrence</span></span>](https://msdn.microsoft.com/library/53746909-ef21-4764-8715-a7769b943cca%28Office.15%29.aspx) <br/> |<span data-ttu-id="413c6-159">Der Wert dieser Eigenschaft oder dieses Elements gibt die Anzahl der Vorkommen an.</span><span class="sxs-lookup"><span data-stu-id="413c6-159">The value of this property or element specifies the number of occurrences.</span></span>  <br/> |
|[<span data-ttu-id="413c6-160">Serie. EndDate</span><span class="sxs-lookup"><span data-stu-id="413c6-160">Recurrence.EndDate</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="413c6-161">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="413c6-161">EndDateRecurrence</span></span>](https://msdn.microsoft.com/library/a5ee2504-db84-49ee-870c-cca9269f2e26%28Office.15%29.aspx) <br/> |<span data-ttu-id="413c6-162">Das letzte Vorkommen in der Datenreihe fällt auf oder vor dem durch diese Eigenschaft oder dieses Element angegebenen Datum.</span><span class="sxs-lookup"><span data-stu-id="413c6-162">The last occurrence in the series falls on or before the date specified by this property or element.</span></span>  <br/> |
|[<span data-ttu-id="413c6-163">Serie. HasEnd</span><span class="sxs-lookup"><span data-stu-id="413c6-163">Recurrence.HasEnd</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.hasend%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="413c6-164">Serie. NeverEnds</span><span class="sxs-lookup"><span data-stu-id="413c6-164">Recurrence.NeverEnds</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.neverends%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="413c6-165">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="413c6-165">NoEndRecurrence</span></span>](https://msdn.microsoft.com/library/ab2ebd9c-388e-45f1-abf9-56e293ef123b%28Office.15%29.aspx) <br/> |<span data-ttu-id="413c6-166">Die Reihe hat kein Ende.</span><span class="sxs-lookup"><span data-stu-id="413c6-166">The series has no end.</span></span>  <br/> |
   
## <a name="expanded-vs-non-expanded-views"></a><span data-ttu-id="413c6-167">Erweiterte vs. nicht erweiterte Ansichten</span><span class="sxs-lookup"><span data-stu-id="413c6-167">Expanded vs. non-expanded views</span></span>

<span data-ttu-id="413c6-168">Durch die Verwendung der **FindAppointments** -Methode im verwaltete EWS-API (oder des **FindItem** -Vorgangs mit einem **CalendarView** -Element in EWS) wird der Erweiterungsprozess aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="413c6-168">Using the **FindAppointments** method in the EWS Managed API (or the **FindItem** operation with a **CalendarView** element in EWS) invokes the expansion process.</span></span> <span data-ttu-id="413c6-169">Dadurch werden wiederkehrende Mastertermine aus dem Resultset ausgeblendet und stattdessen eine erweiterte Ansicht dieser wiederkehrenden Datenreihe dargestellt.</span><span class="sxs-lookup"><span data-stu-id="413c6-169">This hides recurring master appointments from the result set, and instead presents an expanded view of that recurring series.</span></span> <span data-ttu-id="413c6-170">Das Vorkommen von und Ausnahmen für den wiederkehrenden Master, die innerhalb der Parameter der Kalenderansicht liegen, sind im Resultset enthalten.</span><span class="sxs-lookup"><span data-stu-id="413c6-170">Occurrences of and exceptions to the recurring master that fall within the parameters of the calendar view are included in the result set.</span></span> <span data-ttu-id="413c6-171">Umgekehrt wird mithilfe der **FindItems** -Methode im verwaltete EWS-API (oder dem **FindItem** -Vorgang mit einem **IndexedPageItemView** -oder **FractionalPageItemView** -Element in EWS) der Erweiterungsprozess nicht aufgerufen, und es werden keine vorkommen und Ausnahmen angegeben.</span><span class="sxs-lookup"><span data-stu-id="413c6-171">Conversely, using the **FindItems** method in the EWS Managed API (or the **FindItem** operation with a **IndexedPageItemView** or **FractionalPageItemView** element in EWS), does not invoke the expansion process, and occurrences and exceptions are not included.</span></span> <span data-ttu-id="413c6-172">Sehen wir uns ein Beispiel an, in dem die beiden Methoden verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="413c6-172">Let's look at an example comparing the two methods.</span></span> 
  
<span data-ttu-id="413c6-173">**Tabelle 3. Methoden und Vorgänge zum Suchen von Terminen**</span><span class="sxs-lookup"><span data-stu-id="413c6-173">**Table 3. Methods and operations for finding appointments**</span></span>

|<span data-ttu-id="413c6-174">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="413c6-174">**EWS Managed API method**</span></span>|<span data-ttu-id="413c6-175">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="413c6-175">**EWS operation**</span></span>|<span data-ttu-id="413c6-176">**Erweitert die Datenreihe?**</span><span class="sxs-lookup"><span data-stu-id="413c6-176">**Expands series?**</span></span>|<span data-ttu-id="413c6-177">**In Ergebnissen enthaltene Elemente**</span><span class="sxs-lookup"><span data-stu-id="413c6-177">**Items included in results**</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="413c6-178">ExchangeService.FindAppointments</span><span class="sxs-lookup"><span data-stu-id="413c6-178">ExchangeService.FindAppointments</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="413c6-179">[FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit einem [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) -Element</span><span class="sxs-lookup"><span data-stu-id="413c6-179">[FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with a [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="413c6-180">Ja</span><span class="sxs-lookup"><span data-stu-id="413c6-180">Yes</span></span>  <br/> |<span data-ttu-id="413c6-181">Nicht wiederkehrende Termine, einzelne Vorkommen von Terminserien und Ausnahmen für wiederkehrende Datenreihen</span><span class="sxs-lookup"><span data-stu-id="413c6-181">Non-recurring appointments, single occurrences of recurring series, and exceptions to recurring series</span></span>  <br/> |
|[<span data-ttu-id="413c6-182">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="413c6-182">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="413c6-183">[FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit einem [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) -Element oder einem [FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) -Element</span><span class="sxs-lookup"><span data-stu-id="413c6-183">[FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with an [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or [FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="413c6-184">Nein</span><span class="sxs-lookup"><span data-stu-id="413c6-184">No</span></span>  <br/> |<span data-ttu-id="413c6-185">Nicht wiederkehrende Termine und wiederkehrende Mastertermine</span><span class="sxs-lookup"><span data-stu-id="413c6-185">Non-recurring appointments and recurring master appointments</span></span>  <br/> |
   
<span data-ttu-id="413c6-186">Sadie hat ihren Sohn soeben für das Swim-Team unterschrieben.</span><span class="sxs-lookup"><span data-stu-id="413c6-186">Sadie has just signed her son up for swim team.</span></span> <span data-ttu-id="413c6-187">Das Team übt jeden Mittwoch Vormittag um 8:30 Uhr aus, beginnend am 2. Juli, wobei die letzte Übung am 6. August stattfindet.</span><span class="sxs-lookup"><span data-stu-id="413c6-187">The team has practice every Wednesday morning at 8:30 AM, starting July 2, with the last practice being on August 6.</span></span> <span data-ttu-id="413c6-188">Wenn Sie nicht die Praxis vergessen möchten, fügt Sadie eine Terminserie zu Ihrem Kalender hinzu, um Sie zu erinnern.</span><span class="sxs-lookup"><span data-stu-id="413c6-188">Not wanting to forget about practice, Sadie adds a recurring appointment to her calendar to remind her.</span></span>
  
<span data-ttu-id="413c6-189">**Tabelle 4. Sadies Terminserie**</span><span class="sxs-lookup"><span data-stu-id="413c6-189">**Table 4. Sadie's recurring appointment**</span></span>

|<span data-ttu-id="413c6-190">**Terminfeld**</span><span class="sxs-lookup"><span data-stu-id="413c6-190">**Appointment field**</span></span>|<span data-ttu-id="413c6-191">**Wert**</span><span class="sxs-lookup"><span data-stu-id="413c6-191">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="413c6-192">Betreff</span><span class="sxs-lookup"><span data-stu-id="413c6-192">Subject</span></span>  <br/> |<span data-ttu-id="413c6-193">Swim-Team Praxis</span><span class="sxs-lookup"><span data-stu-id="413c6-193">Swim Team Practice</span></span>  <br/> |
|<span data-ttu-id="413c6-194">Start</span><span class="sxs-lookup"><span data-stu-id="413c6-194">Start</span></span>  <br/> |<span data-ttu-id="413c6-195">2. Juli 2014 8:30 Uhr</span><span class="sxs-lookup"><span data-stu-id="413c6-195">July 2, 2014 8:30 AM</span></span>  <br/> |
|<span data-ttu-id="413c6-196">Ende</span><span class="sxs-lookup"><span data-stu-id="413c6-196">End</span></span>  <br/> |<span data-ttu-id="413c6-197">2. Juli 2014 10:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="413c6-197">July 2, 2014 10:00 AM</span></span>  <br/> |
|<span data-ttu-id="413c6-198">Auftritt</span><span class="sxs-lookup"><span data-stu-id="413c6-198">Recurs</span></span>  <br/> |<span data-ttu-id="413c6-199">Jeden Mittwoch</span><span class="sxs-lookup"><span data-stu-id="413c6-199">Every Wednesday</span></span>  <br/> |
|<span data-ttu-id="413c6-200">Letztes vorkommen</span><span class="sxs-lookup"><span data-stu-id="413c6-200">Last occurrence</span></span>  <br/> |<span data-ttu-id="413c6-201">6. August 2014 8:30 Uhr</span><span class="sxs-lookup"><span data-stu-id="413c6-201">August 6, 2014 8:30 AM</span></span>  <br/> |
   
<span data-ttu-id="413c6-202">Ein kurzer Blick in einen Kalender zeigt, dass das Team insgesamt sechs Methoden hat.</span><span class="sxs-lookup"><span data-stu-id="413c6-202">A quick look at a calendar shows that the team will have a total of six practices.</span></span> <span data-ttu-id="413c6-203">Es gibt jedoch nicht sechs unterschiedliche Termin Elemente im Kalender.</span><span class="sxs-lookup"><span data-stu-id="413c6-203">However, there aren't six distinct appointment items in the calendar.</span></span> <span data-ttu-id="413c6-204">Stattdessen gibt es nur einen wiederkehrenden Mastertermin, der die Datenreihe darstellt.</span><span class="sxs-lookup"><span data-stu-id="413c6-204">Instead, there is just one recurring master appointment representing the series.</span></span>
  
<span data-ttu-id="413c6-205">Schauen wir uns nun die Suche nach Terminen für Sadies Kalender an, die innerhalb des Monats Juli stattfinden.</span><span class="sxs-lookup"><span data-stu-id="413c6-205">Now let's look at finding appointments on Sadie's calendar that occur within the month of July.</span></span> <span data-ttu-id="413c6-206">Im folgenden Codebeispiel wird die **FindItems** -Methode in der Exchange Managed API verwendet, um eine nicht erweiterte Ansicht von Sadies Kalender zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="413c6-206">The following code example uses the **FindItems** method in the Exchange Managed API to produce a non-expanded view of Sadie's calendar.</span></span> 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
#region FindItems + ItemView method
ItemView itemView = new ItemView(100);
itemView.PropertySet = propSet;
List<SearchFilter> filterList = new List<SearchFilter>();
// Find appointments that start after midnight on July 1, 2014.
SearchFilter.IsGreaterThan startFilter = new SearchFilter.IsGreaterThan(AppointmentSchema.Start,
    new DateTime(2014, 7, 1));
// Find appointments that end before midnight on July 31, 2014
SearchFilter.IsLessThan endFilter = new SearchFilter.IsLessThan(AppointmentSchema.End,
    new DateTime(2014, 7, 31));
filterList.Add(startFilter);
filterList.Add(endFilter);
SearchFilter.SearchFilterCollection calendarFilter = new SearchFilter.SearchFilterCollection(LogicalOperator.And, filterList);
// This results in a call to EWS.
FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Calendar, calendarFilter, itemView);
foreach(Item appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

<span data-ttu-id="413c6-207">Dieser Code ergibt die folgende [FindItem-Vorgangs](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) Anforderung mit einem [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) -Element.</span><span class="sxs-lookup"><span data-stu-id="413c6-207">That code results in the following [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with an [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="100" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:And>
          <t:IsGreaterThan>
            <t:FieldURI FieldURI="calendar:Start" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-01T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsGreaterThan>
          <t:IsLessThan>
            <t:FieldURI FieldURI="calendar:End" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-31T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsLessThan>
        </t:And>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="413c6-208">Die Antwort des Servers enthält nur ein einzelnes Element, den wiederkehrenden Master, der durch den [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) -Elementwert von **RecurringMaster**angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="413c6-208">The server's response includes only a single item, the recurring master, indicated by the [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element value of **RecurringMaster**.</span></span> <span data-ttu-id="413c6-209">Der Wert des [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Elements wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="413c6-209">The value of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
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
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>RecurringMaster</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="413c6-210">Lassen Sie uns nun mit einer erweiterten Ansicht vergleichen.</span><span class="sxs-lookup"><span data-stu-id="413c6-210">Now let's compare with an expanded view.</span></span> <span data-ttu-id="413c6-211">Im folgenden Codebeispiel wird die **FindAppointments** -Methode im verwaltete EWS-API verwendet, um eine erweiterte Ansicht von Sadies Kalender zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="413c6-211">The following code example uses the **FindAppointments** method in the EWS Managed API to create an expanded view of Sadie's calendar.</span></span> 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
CalendarView calView = new CalendarView(new DateTime(2014, 7, 1),
    new DateTime(2014, 7, 31));
calView.PropertySet = propSet;
FindItemsResults<Appointment> results = service.FindAppointments(WellKnownFolderName.Calendar, calView);
foreach(Appointment appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

<span data-ttu-id="413c6-212">Dieser Code ergibt die folgende [FindItem-Vorgangs](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) Anforderung mit einem [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) -Element.</span><span class="sxs-lookup"><span data-stu-id="413c6-212">This code results in the following [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with a [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView StartDate="2014-07-01T07:00:00.000Z" EndDate="2014-07-31T07:00:00.000Z" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="413c6-213">Dieses Mal umfasst die Serverantwort fünf vorkommen, eine für jeden Mittwoch im Juli.</span><span class="sxs-lookup"><span data-stu-id="413c6-213">This time, the server response includes five occurrences, one for each Wednesday in July.</span></span> <span data-ttu-id="413c6-214">Die [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) -Elemente für diese Elemente weisen alle den Wert " **vorkommen**" auf.</span><span class="sxs-lookup"><span data-stu-id="413c6-214">The [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) elements on these items all have a value of **Occurrence**.</span></span> <span data-ttu-id="413c6-215">Beachten Sie, dass die wiederkehrende Master in der Antwort nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="413c6-215">Note that the recurring master is not present in the response.</span></span> <span data-ttu-id="413c6-216">Die Werte der [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Elemente wurden zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="413c6-216">The values of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
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
          <m:RootFolder TotalItemsInView="5" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-09T15:30:00Z</t:Start>
                <t:End>2014-07-09T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA8..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-16T15:30:00Z</t:Start>
                <t:End>2014-07-16T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA9..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-23T15:30:00Z</t:Start>
                <t:End>2014-07-23T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADAA..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-30T15:30:00Z</t:Start>
                <t:End>2014-07-30T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="413c6-217">Nachdem Sie eine wiederkehrende Master, ein vorkommen oder eine Ausnahme haben, können Sie immer [die anderen verwandten Elemente abrufen](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="413c6-217">After you have a recurring master, an occurrence, or an exception, you can always [retrieve the other related items](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="413c6-218">Wenn ein vorkommen oder eine Ausnahme vorliegt, können Sie den wiederkehrenden Master abrufen und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="413c6-218">Given an occurrence or exception, you can retrieve the recurring master, and vice versa.</span></span>
  
## <a name="working-with-recurring-calendar-items"></a><span data-ttu-id="413c6-219">Arbeiten mit wiederkehrenden Kalenderelementen</span><span class="sxs-lookup"><span data-stu-id="413c6-219">Working with recurring calendar items</span></span>

<span data-ttu-id="413c6-220">Sie verwenden alle gleichen Methoden und Vorgänge, um mit wiederkehrenden Datenreihen zu arbeiten, während Sie mit nicht wiederkehrenden Kalenderelementen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="413c6-220">You use all the same methods and operations to work with recurring series as you use to work with non-recurring calendar items.</span></span> <span data-ttu-id="413c6-221">Der Unterschied besteht darin, dass abhängig vom Element, das Sie zum Aufrufen dieser Methoden oder Vorgänge verwenden, die von Ihnen ausgeführten Aktionen auf die gesamte Datenreihe oder nur auf ein einzelnes Vorkommen angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="413c6-221">The difference is that, depending on the item you use to invoke those methods or operations, the actions you take can apply to the entire series, or just a single occurrence.</span></span> <span data-ttu-id="413c6-222">[Aktionen, die im wiederkehrenden Master ausgeführt](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) werden, gelten für alle Vorkommen in der Datenreihe, während Aktionen, die [zu einem einzelnen vorkommen oder einer Ausnahme ausgeführt](how-to-update-a-recurring-series-by-using-ews.md) werden, nur auf dieses vorkommen oder jede Ausnahme zutreffen.</span><span class="sxs-lookup"><span data-stu-id="413c6-222">[Actions taken on the recurring master](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) will apply to all occurrences in the series, while [actions taken to a single occurrence or exception](how-to-update-a-recurring-series-by-using-ews.md) will only apply to that occurrence or exception.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="413c6-223">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="413c6-223">In this section</span></span>

- [<span data-ttu-id="413c6-224">Zugreifen auf eine Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="413c6-224">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="413c6-225">Erstellen einer Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="413c6-225">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="413c6-226">Löschen von Terminen in einer Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="413c6-226">Delete appointments in a recurring series by using EWS in Exchange</span></span>](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="413c6-227">Aktualisieren einer Terminserie mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="413c6-227">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="413c6-228">Aktualisieren einer Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="413c6-228">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="413c6-229">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="413c6-229">See also</span></span>


- [<span data-ttu-id="413c6-230">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="413c6-230">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="413c6-231">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="413c6-231">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="413c6-232">Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="413c6-232">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

