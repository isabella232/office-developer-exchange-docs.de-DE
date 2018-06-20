---
title: Serienmuster und EWS
manager: luken
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fd9ef706-1e01-49fa-af6f-2f6d3e173c16
description: Informationen Sie zu Serienmuster und sich wiederholenden Reihe im Exchange ein.
ms.openlocfilehash: ac10e9b9a347abb5907b77f0e0e7315e4e86d97a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757128"
---
# <a name="recurrence-patterns-and-ews"></a><span data-ttu-id="2f641-103">Serienmuster und EWS</span><span class="sxs-lookup"><span data-stu-id="2f641-103">Recurrence patterns and EWS</span></span>

<span data-ttu-id="2f641-104">Informationen Sie zu Serienmuster und sich wiederholenden Reihe im Exchange ein.</span><span class="sxs-lookup"><span data-stu-id="2f641-104">Learn about recurrence patterns and recurring series in Exchange.</span></span>
  
<span data-ttu-id="2f641-105">Eine Terminserie ist ein Termin oder eine Besprechung, die nach einem definierten Muster wiederholt.</span><span class="sxs-lookup"><span data-stu-id="2f641-105">A recurring series is an appointment or meeting that repeats according to a defined pattern.</span></span> <span data-ttu-id="2f641-106">Eine Terminserie kann entweder eine bestimmte Anzahl von Vorkommen oder kann auf unbestimmte Zeit wiederholen.</span><span class="sxs-lookup"><span data-stu-id="2f641-106">A recurring series can either have a specific number of occurrences or can repeat indefinitely.</span></span> <span data-ttu-id="2f641-107">Darüber hinaus kann sich wiederholenden Reihe Ausnahmen verfügen, die folgen nicht das Muster der restlichen vorkommen, und kann vorkommen, die aus dem Muster gelöscht wurden aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2f641-107">Additionally, a recurring series can have exceptions that don't follow the pattern of the rest of the occurrences, and can have occurrences that have been deleted from the pattern.</span></span> <span data-ttu-id="2f641-108">Die EWS Managed API und EWS können sich wiederholenden Reihe und deren zugeordneten Kalenderelemente entwickelt.</span><span class="sxs-lookup"><span data-stu-id="2f641-108">You can use the EWS Managed API and EWS to work with recurring series and their associated calendar items.</span></span>
  
## <a name="recurring-calendar-items"></a><span data-ttu-id="2f641-109">Wiederkehrende Kalenderelemente</span><span class="sxs-lookup"><span data-stu-id="2f641-109">Recurring calendar items</span></span>

<span data-ttu-id="2f641-110">Alle Elemente im Kalender werden in der folgenden vier Kategorien unterteilt:</span><span class="sxs-lookup"><span data-stu-id="2f641-110">All calendar items fall into one of the following four categories:</span></span>
  
- <span data-ttu-id="2f641-111">Nicht wiederkehrende Kalenderelemente</span><span class="sxs-lookup"><span data-stu-id="2f641-111">Non-recurring calendar items</span></span>
    
- <span data-ttu-id="2f641-112">Wiederkehrende Master-Shapes</span><span class="sxs-lookup"><span data-stu-id="2f641-112">Recurring masters</span></span>
    
- <span data-ttu-id="2f641-113">Vorkommen in einer Reihe</span><span class="sxs-lookup"><span data-stu-id="2f641-113">Occurrences in a series</span></span>
    
- <span data-ttu-id="2f641-114">Geänderte Vorkommen in einer Reihe, bezeichnet als Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="2f641-114">Modified occurrences in a series, known as exceptions</span></span>
    
<span data-ttu-id="2f641-115">In diesem Artikel werden die drei Typen von Kalenderelementen betrachten wir, die Teil einer Serie sind.</span><span class="sxs-lookup"><span data-stu-id="2f641-115">In this article, we'll look at the three types of calendar items that are part of a recurring series.</span></span>
  
<span data-ttu-id="2f641-116">Es ist hilfreich, zu verstehen, wie sich wiederholenden Reihe implementiert werden, auf dem Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="2f641-116">It's helpful to understand how recurring series are implemented on the Exchange server.</span></span> <span data-ttu-id="2f641-117">Anstatt für jedes Vorkommen einer separaten separate Element in einer Terminserie zu erstellen, erstellt der Server nur ein Element im Kalender als wiederkehrenden Master bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2f641-117">Instead of creating a separate distinct item for each occurrence in a recurring series, the server creates only one actual item in the calendar, known as the recurring master.</span></span> <span data-ttu-id="2f641-118">Das Format eines sich wiederholenden Master ist ein Termin nicht wiederkehrende durch die hinzugefügte Muster Serieninformationen sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="2f641-118">The format of a recurring master is very similar to a non-recurring appointment, with the addition of recurrence pattern information.</span></span> <span data-ttu-id="2f641-119">Der Server generiert dann basierende auf das Serienmuster als Antwort auf Clientanforderungen für Informationen zum Kalendertermin, unter Verwendung der sogenannten Erweiterung vorkommen.</span><span class="sxs-lookup"><span data-stu-id="2f641-119">The server then generates occurrences based on the recurrence pattern in response to client requests for appointment information, using a process called expansion.</span></span> <span data-ttu-id="2f641-120">Diese generierten Vorkommen werden auf dem Server nicht dauerhaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2f641-120">These generated occurrences are not permanently stored on the server.</span></span> <span data-ttu-id="2f641-121">Dies ist wichtig zu verstehen, da die Möglichkeit, die Sie für Kalenderelemente suchen bestimmt, welche Informationen Sie erhalten und gibt an, ob die Erweiterung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2f641-121">This is important to understand because the way that you search for calendar items determines what information you receive and whether expansion occurs.</span></span>
  
## <a name="recurrence-patterns"></a><span data-ttu-id="2f641-122">Serienmuster</span><span class="sxs-lookup"><span data-stu-id="2f641-122">Recurrence patterns</span></span>

<span data-ttu-id="2f641-123">Die Hauptinformationen in einer Terminserie, die Erweiterung ermöglicht ist das Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="2f641-123">The key piece to a recurring series that makes expansion possible is the recurrence pattern.</span></span> <span data-ttu-id="2f641-124">Das Serienmuster gefunden wird, auf dem sich wiederholenden Master und beschreibt einen Satz von Kriterien für die Berechnung basierend auf Datum und Uhrzeit des wiederkehrenden Master vorkommen.</span><span class="sxs-lookup"><span data-stu-id="2f641-124">The recurrence pattern is found on the recurring master, and describes a set of criteria for calculating occurrences based on the date and time of the recurring master.</span></span>
  
<span data-ttu-id="2f641-125">**In Tabelle 1. Serienmuster verfügbar**</span><span class="sxs-lookup"><span data-stu-id="2f641-125">**Table 1. Available recurrence patterns**</span></span>

|<span data-ttu-id="2f641-126">**Verwaltete EWS-API-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2f641-126">**EWS Managed API class**</span></span>|<span data-ttu-id="2f641-127">**EWS-Element**</span><span class="sxs-lookup"><span data-stu-id="2f641-127">**EWS element**</span></span>|<span data-ttu-id="2f641-128">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="2f641-128">**Examples**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2f641-129">Recurrence.DailyPattern</span><span class="sxs-lookup"><span data-stu-id="2f641-129">Recurrence.DailyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.dailypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2f641-130">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2f641-130">DailyRecurrence</span></span>](http://msdn.microsoft.com/library/0aaf265d-b723-49c6-8e9c-9ba60141e9ab%28Office.15%29.aspx) <br/> |<span data-ttu-id="2f641-131">Wiederholen Sie täglich aus.</span><span class="sxs-lookup"><span data-stu-id="2f641-131">Repeat every day.</span></span>  <br/> <span data-ttu-id="2f641-132">Wiederholen Sie jeden zweiten Tag.</span><span class="sxs-lookup"><span data-stu-id="2f641-132">Repeat every other day.</span></span>  <br/> |
|[<span data-ttu-id="2f641-133">Recurrence.MonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="2f641-133">Recurrence.MonthlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.monthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2f641-134">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2f641-134">AbsoluteMonthlyRecurrence</span></span>](http://msdn.microsoft.com/library/178fa0ae-9dfc-417f-933c-d657d31c2161%28Office.15%29.aspx) <br/> |<span data-ttu-id="2f641-135">Wiederholen Sie jeden Monat am zehnten Tag des Monats.</span><span class="sxs-lookup"><span data-stu-id="2f641-135">Repeat every month on the tenth day of the month.</span></span>  <br/> <span data-ttu-id="2f641-136">Wiederholen Sie alle zwei Monate am zwanzig ersten Tag des Monats.</span><span class="sxs-lookup"><span data-stu-id="2f641-136">Repeat every other month on the twenty-first day of the month.</span></span>  <br/> |
|[<span data-ttu-id="2f641-137">Recurrence.RelativeMonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="2f641-137">Recurrence.RelativeMonthlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.relativemonthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2f641-138">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2f641-138">RelativeMonthlyRecurrence</span></span>](http://msdn.microsoft.com/library/a76595db-7460-44ac-ac2a-53241caa33a7%28Office.15%29.aspx) <br/> |<span data-ttu-id="2f641-139">Wiederholen Sie die am zweiten Dienstag des Monats.</span><span class="sxs-lookup"><span data-stu-id="2f641-139">Repeat on the second Tuesday of every month.</span></span>  <br/> <span data-ttu-id="2f641-140">Wiederholen Sie die dem dritten Donnerstag des Monats alle drei Monate.</span><span class="sxs-lookup"><span data-stu-id="2f641-140">Repeat on the third Thursday of the month every three months.</span></span>  <br/> |
|[<span data-ttu-id="2f641-141">Recurrence.RelativeYearlyPattern</span><span class="sxs-lookup"><span data-stu-id="2f641-141">Recurrence.RelativeYearlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2f641-142">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2f641-142">RelativeYearlyRecurrence</span></span>](http://msdn.microsoft.com/library/25b67876-9979-4a30-a637-357ea10a93b8%28Office.15%29.aspx) <br/> |<span data-ttu-id="2f641-143">Wiederholen Sie am ersten Montag August jedes Jahr.</span><span class="sxs-lookup"><span data-stu-id="2f641-143">Repeat on the first Monday of August every year.</span></span>  <br/> |
|[<span data-ttu-id="2f641-144">Recurrence.WeeklyPattern</span><span class="sxs-lookup"><span data-stu-id="2f641-144">Recurrence.WeeklyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.weeklypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2f641-145">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2f641-145">WeeklyRecurrence</span></span>](http://msdn.microsoft.com/library/69c41dd5-597c-45bc-be3f-e2f2b5615aa3%28Office.15%29.aspx) <br/> |<span data-ttu-id="2f641-146">Wiederholen Sie jeden Montag.</span><span class="sxs-lookup"><span data-stu-id="2f641-146">Repeat every Monday.</span></span>  <br/> <span data-ttu-id="2f641-147">Wiederholen Sie jeden Dienstag und Donnerstag alle zwei Wochen.</span><span class="sxs-lookup"><span data-stu-id="2f641-147">Repeat every Tuesday and Thursday every other week.</span></span>  <br/> |
|[<span data-ttu-id="2f641-148">Recurrence.YearlyPattern</span><span class="sxs-lookup"><span data-stu-id="2f641-148">Recurrence.YearlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2f641-149">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2f641-149">AbsoluteYearlyRecurrence</span></span>](http://msdn.microsoft.com/library/96f53e2c-3893-4f6e-a78a-ac179f45c5db%28Office.15%29.aspx) <br/> |<span data-ttu-id="2f641-150">Wiederholen Sie am 1. September jedes Jahr.</span><span class="sxs-lookup"><span data-stu-id="2f641-150">Repeat on September 1st every year.</span></span>  <br/> |
   
<span data-ttu-id="2f641-151">Der andere wichtige Informationen für ein Serienmuster ist, wenn das Serienmuster endet.</span><span class="sxs-lookup"><span data-stu-id="2f641-151">The other important piece of information for a recurrence pattern is when the recurrence ends.</span></span> <span data-ttu-id="2f641-152">Dies kann als eine festgelegte Anzahl von vorkommen, als ein Enddatum oder dass kein Ende ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="2f641-152">This can be expressed as either a set number of occurrences, as an end date, or as having no end.</span></span>
  
<span data-ttu-id="2f641-153">**In Tabelle 2. Optionen für das Ende einer Terminserie**</span><span class="sxs-lookup"><span data-stu-id="2f641-153">**Table 2. Options for the end of a recurring series**</span></span>

|<span data-ttu-id="2f641-154">**EWS Managed API-Methode /-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="2f641-154">**EWS Managed API method/property**</span></span>|<span data-ttu-id="2f641-155">**EWS-Element**</span><span class="sxs-lookup"><span data-stu-id="2f641-155">**EWS element**</span></span>|<span data-ttu-id="2f641-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f641-156">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2f641-157">Recurrence.NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="2f641-157">Recurrence.NumberOfOccurrences</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.numberofoccurrences%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2f641-158">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="2f641-158">NumberedRecurrence</span></span>](http://msdn.microsoft.com/library/53746909-ef21-4764-8715-a7769b943cca%28Office.15%29.aspx) <br/> |<span data-ttu-id="2f641-159">Der Wert dieser Eigenschaft oder eines Elements gibt die Anzahl von vorkommen.</span><span class="sxs-lookup"><span data-stu-id="2f641-159">The value of this property or element specifies the number of occurrences.</span></span>  <br/> |
|[<span data-ttu-id="2f641-160">Recurrence.EndDate</span><span class="sxs-lookup"><span data-stu-id="2f641-160">Recurrence.EndDate</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2f641-161">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="2f641-161">EndDateRecurrence</span></span>](http://msdn.microsoft.com/library/a5ee2504-db84-49ee-870c-cca9269f2e26%28Office.15%29.aspx) <br/> |<span data-ttu-id="2f641-162">Das letzte Vorkommen in der Datenreihe liegt am oder vor dem angegebenen Datum die durch diese Eigenschaft oder eines Elements.</span><span class="sxs-lookup"><span data-stu-id="2f641-162">The last occurrence in the series falls on or before the date specified by this property or element.</span></span>  <br/> |
|[<span data-ttu-id="2f641-163">Recurrence.HasEnd</span><span class="sxs-lookup"><span data-stu-id="2f641-163">Recurrence.HasEnd</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.hasend%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="2f641-164">Recurrence.NeverEnds</span><span class="sxs-lookup"><span data-stu-id="2f641-164">Recurrence.NeverEnds</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.neverends%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2f641-165">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="2f641-165">NoEndRecurrence</span></span>](http://msdn.microsoft.com/library/ab2ebd9c-388e-45f1-abf9-56e293ef123b%28Office.15%29.aspx) <br/> |<span data-ttu-id="2f641-166">Die Datenreihe, weist kein Ende.</span><span class="sxs-lookup"><span data-stu-id="2f641-166">The series has no end.</span></span>  <br/> |
   
## <a name="expanded-vs-non-expanded-views"></a><span data-ttu-id="2f641-167">Im Vergleich zu Ansichten nicht erweiterten erweitert</span><span class="sxs-lookup"><span data-stu-id="2f641-167">Expanded vs. non-expanded views</span></span>

<span data-ttu-id="2f641-168">Verwendung der **FindAppointments** -Methode in die EWS Managed API (oder mit einem **CalendarView** -Element im EWS-Vorgangs **FindItem** ) Ruft den Erweiterungsprozess.</span><span class="sxs-lookup"><span data-stu-id="2f641-168">Using the **FindAppointments** method in the EWS Managed API (or the **FindItem** operation with a **CalendarView** element in EWS) invokes the expansion process.</span></span> <span data-ttu-id="2f641-169">Dies Blendet master Terminserien aus dem Ergebnissatz und stattdessen stellt eine erweiterte Ansicht dieser Serie.</span><span class="sxs-lookup"><span data-stu-id="2f641-169">This hides recurring master appointments from the result set, and instead presents an expanded view of that recurring series.</span></span> <span data-ttu-id="2f641-170">Vorkommen und Ausnahmen auf der sich wiederholenden Master, die in die Parameter der Kalenderansicht fallen sind im Resultset enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f641-170">Occurrences of and exceptions to the recurring master that fall within the parameters of the calendar view are included in the result set.</span></span> <span data-ttu-id="2f641-171">Dagegen mithilfe der **FindItems** -Methode in die EWS Managed API (oder die Operation **FindItem** mit einem **IndexedPageItemView** oder **FractionalPageItemView** -Element im EWS) wird keine aufgerufen Erweiterung Prozesses und der Vorkommen und Ausnahmen sind nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f641-171">Conversely, using the **FindItems** method in the EWS Managed API (or the **FindItem** operation with a **IndexedPageItemView** or **FractionalPageItemView** element in EWS), does not invoke the expansion process, and occurrences and exceptions are not included.</span></span> <span data-ttu-id="2f641-172">Sehen wir uns ein Beispiel für die beiden Methoden verglichen.</span><span class="sxs-lookup"><span data-stu-id="2f641-172">Let's look at an example comparing the two methods.</span></span> 
  
<span data-ttu-id="2f641-173">**Tabelle 3. Methoden und Vorgänge für die Suche nach Terminen**</span><span class="sxs-lookup"><span data-stu-id="2f641-173">**Table 3. Methods and operations for finding appointments**</span></span>

|<span data-ttu-id="2f641-174">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="2f641-174">**EWS Managed API method**</span></span>|<span data-ttu-id="2f641-175">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="2f641-175">**EWS operation**</span></span>|<span data-ttu-id="2f641-176">**Erweitert die Datenreihe?**</span><span class="sxs-lookup"><span data-stu-id="2f641-176">**Expands series?**</span></span>|<span data-ttu-id="2f641-177">**Elemente, die in Suchergebnissen enthalten**</span><span class="sxs-lookup"><span data-stu-id="2f641-177">**Items included in results**</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="2f641-178">ExchangeService.FindAppointments</span><span class="sxs-lookup"><span data-stu-id="2f641-178">ExchangeService.FindAppointments</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="2f641-179">[FindItem Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit einem [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) -element</span><span class="sxs-lookup"><span data-stu-id="2f641-179">[FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with a [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="2f641-180">Ja</span><span class="sxs-lookup"><span data-stu-id="2f641-180">Yes</span></span>  <br/> |<span data-ttu-id="2f641-181">Nicht wiederkehrende Termine einzelnen Vorkommen von sich wiederholenden Reihe und Ausnahmen von sich wiederholenden Reihe</span><span class="sxs-lookup"><span data-stu-id="2f641-181">Non-recurring appointments, single occurrences of recurring series, and exceptions to recurring series</span></span>  <br/> |
|[<span data-ttu-id="2f641-182">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="2f641-182">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="2f641-183">[FindItem Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit einer [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) Element oder [FractionalPageItemView](http://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) -element</span><span class="sxs-lookup"><span data-stu-id="2f641-183">[FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with an [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or [FractionalPageItemView](http://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="2f641-184">Nein</span><span class="sxs-lookup"><span data-stu-id="2f641-184">No</span></span>  <br/> |<span data-ttu-id="2f641-185">Nicht wiederkehrende Termine und Terminserien Master-Shape</span><span class="sxs-lookup"><span data-stu-id="2f641-185">Non-recurring appointments and recurring master appointments</span></span>  <br/> |
   
<span data-ttu-id="2f641-186">Sadie hat sich ihr Son bei schwimmen Team gerade angemeldet.</span><span class="sxs-lookup"><span data-stu-id="2f641-186">Sadie has just signed her son up for swim team.</span></span> <span data-ttu-id="2f641-187">Das Team weist Practice jeden Mittwoch Morgen um 8:30 Uhr, beginnend mit der letzten Practice wird am 6. August 2. Juli.</span><span class="sxs-lookup"><span data-stu-id="2f641-187">The team has practice every Wednesday morning at 8:30 AM, starting July 2, with the last practice being on August 6.</span></span> <span data-ttu-id="2f641-188">Nicht möchte, praktischen vergessen, fügt Sadie eine Terminserie auf ihren Kalender aus, um ihn zu erinnern.</span><span class="sxs-lookup"><span data-stu-id="2f641-188">Not wanting to forget about practice, Sadie adds a recurring appointment to her calendar to remind her.</span></span>
  
<span data-ttu-id="2f641-189">**In Tabelle 4. Terminserie des Sadie**</span><span class="sxs-lookup"><span data-stu-id="2f641-189">**Table 4. Sadie's recurring appointment**</span></span>

|<span data-ttu-id="2f641-190">**Termin dar**</span><span class="sxs-lookup"><span data-stu-id="2f641-190">**Appointment field**</span></span>|<span data-ttu-id="2f641-191">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2f641-191">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f641-192">Subject</span><span class="sxs-lookup"><span data-stu-id="2f641-192">Subject</span></span>  <br/> |<span data-ttu-id="2f641-193">Schwimmen Team-Methode</span><span class="sxs-lookup"><span data-stu-id="2f641-193">Swim Team Practice</span></span>  <br/> |
|<span data-ttu-id="2f641-194">Beginn</span><span class="sxs-lookup"><span data-stu-id="2f641-194">Start</span></span>  <br/> |<span data-ttu-id="2f641-195">2 Juli 2014 8:30 Uhr ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f641-195">July 2, 2014 8:30 AM</span></span>  <br/> |
|<span data-ttu-id="2f641-196">Ende</span><span class="sxs-lookup"><span data-stu-id="2f641-196">End</span></span>  <br/> |<span data-ttu-id="2f641-197">2 Juli 2014 10:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="2f641-197">July 2, 2014 10:00 AM</span></span>  <br/> |
|<span data-ttu-id="2f641-198">Wiederholt</span><span class="sxs-lookup"><span data-stu-id="2f641-198">Recurs</span></span>  <br/> |<span data-ttu-id="2f641-199">Jeden Mittwoch</span><span class="sxs-lookup"><span data-stu-id="2f641-199">Every Wednesday</span></span>  <br/> |
|<span data-ttu-id="2f641-200">Letzte Vorkommen</span><span class="sxs-lookup"><span data-stu-id="2f641-200">Last occurrence</span></span>  <br/> |<span data-ttu-id="2f641-201">6 August 2014 8:30 Uhr ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f641-201">August 6, 2014 8:30 AM</span></span>  <br/> |
   
<span data-ttu-id="2f641-202">Ein schnellen Blick auf einen Kalender zeigt, dass das Team insgesamt sechs Methoden hat.</span><span class="sxs-lookup"><span data-stu-id="2f641-202">A quick look at a calendar shows that the team will have a total of six practices.</span></span> <span data-ttu-id="2f641-203">Jedoch keine sechs verschiedene Terminelemente vorhanden sind, im Kalender.</span><span class="sxs-lookup"><span data-stu-id="2f641-203">However, there aren't six distinct appointment items in the calendar.</span></span> <span data-ttu-id="2f641-204">Stattdessen wird nur ein Master-Shape Terminserie, der Datenreihe darstellt.</span><span class="sxs-lookup"><span data-stu-id="2f641-204">Instead, there is just one recurring master appointment representing the series.</span></span>
  
<span data-ttu-id="2f641-205">Jetzt sehen wir uns finden von Terminen Sadie Kalender, die innerhalb des Monats Juli auftreten.</span><span class="sxs-lookup"><span data-stu-id="2f641-205">Now let's look at finding appointments on Sadie's calendar that occur within the month of July.</span></span> <span data-ttu-id="2f641-206">Im folgenden Codebeispiel wird verwendet die **FindItems** -Methode in der Exchange-Managed-API zum Erstellen einer nicht erweiterten Ansicht des Sadies Kalenders.</span><span class="sxs-lookup"><span data-stu-id="2f641-206">The following code example uses the **FindItems** method in the Exchange Managed API to produce a non-expanded view of Sadie's calendar.</span></span> 
  
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

<span data-ttu-id="2f641-207">Dieser Code führt die folgenden [FindItem Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Anforderung mit einem [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) -Element.</span><span class="sxs-lookup"><span data-stu-id="2f641-207">That code results in the following [FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with an [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="2f641-208">Die Antwort des Servers enthält nur ein einzelnes Element, das sich wiederholenden Master-Shape, von dem Elementwert [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) des **RecurringMaster**angegeben.</span><span class="sxs-lookup"><span data-stu-id="2f641-208">The server's response includes only a single item, the recurring master, indicated by the [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element value of **RecurringMaster**.</span></span> <span data-ttu-id="2f641-209">Der Wert des Elements [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="2f641-209">The value of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
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

<span data-ttu-id="2f641-210">Jetzt Vergleichen wir mit einer erweiterten Ansicht.</span><span class="sxs-lookup"><span data-stu-id="2f641-210">Now let's compare with an expanded view.</span></span> <span data-ttu-id="2f641-211">Im folgenden Codebeispiel wird die **FindAppointments** -Methode in die EWS Managed API zum Erstellen einer erweiterten Ansicht Sadies Kalenders verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f641-211">The following code example uses the **FindAppointments** method in the EWS Managed API to create an expanded view of Sadie's calendar.</span></span> 
  
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

<span data-ttu-id="2f641-212">Dieser Code führt die folgenden [FindItem Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Anforderung mit einem [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) -Element.</span><span class="sxs-lookup"><span data-stu-id="2f641-212">This code results in the following [FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with a [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="2f641-213">Diesmal enthält die Antwort vom Server fünf vorkommen, einen für jeden Mittwoch im Juli.</span><span class="sxs-lookup"><span data-stu-id="2f641-213">This time, the server response includes five occurrences, one for each Wednesday in July.</span></span> <span data-ttu-id="2f641-214">Auf diese Elemente, die alle Elemente [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) aufweisen Wert **Vorkommen**.</span><span class="sxs-lookup"><span data-stu-id="2f641-214">The [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) elements on these items all have a value of **Occurrence**.</span></span> <span data-ttu-id="2f641-215">Beachten Sie, dass das wiederkehrende Master-Shape nicht in der Antwort vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2f641-215">Note that the recurring master is not present in the response.</span></span> <span data-ttu-id="2f641-216">Die Werte der [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="2f641-216">The values of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
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

<span data-ttu-id="2f641-217">Nachdem Sie ein wiederkehrendes Master-Shape, das Auftreten eines Serientermins oder eine Ausnahme haben, können Sie immer für [die anderen verwandten Elemente abzurufen](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="2f641-217">After you have a recurring master, an occurrence, or an exception, you can always [retrieve the other related items](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="2f641-218">Sie können erhält ein Vorkommen oder eine Ausnahmebedingung, das sich wiederholenden Master-Shape abrufen und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="2f641-218">Given an occurrence or exception, you can retrieve the recurring master, and vice versa.</span></span>
  
## <a name="working-with-recurring-calendar-items"></a><span data-ttu-id="2f641-219">Arbeiten mit sich wiederholenden Kalenderelementen (engl.)</span><span class="sxs-lookup"><span data-stu-id="2f641-219">Working with recurring calendar items</span></span>

<span data-ttu-id="2f641-220">Sie verwenden die gleichen Methoden und Vorgänge sich wiederholenden Reihe entwickelt, wie Sie verwenden, um eine nicht wiederkehrende Kalenderelemente entwickelt.</span><span class="sxs-lookup"><span data-stu-id="2f641-220">You use all the same methods and operations to work with recurring series as you use to work with non-recurring calendar items.</span></span> <span data-ttu-id="2f641-221">Der Unterschied besteht darin, je nach dem Element, das Sie verwenden, um das Aufrufen von Methoden oder Vorgänge, die Aktionen, mit denen Sie auf die gesamte Datenreihe oder nur ein einzelnes Vorkommen anwenden können.</span><span class="sxs-lookup"><span data-stu-id="2f641-221">The difference is that, depending on the item you use to invoke those methods or operations, the actions you take can apply to the entire series, or just a single occurrence.</span></span> <span data-ttu-id="2f641-222">[Aktionen, die für die periodische Master](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) gilt für alle Vorkommen in der Datenreihe während [Aktionen, um ein einzelnes Vorkommen oder eine Ausnahme](how-to-update-a-recurring-series-by-using-ews.md) nur diese Vorkommen oder Ausnahme zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2f641-222">[Actions taken on the recurring master](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) will apply to all occurrences in the series, while [actions taken to a single occurrence or exception](how-to-update-a-recurring-series-by-using-ews.md) will only apply to that occurrence or exception.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="2f641-223">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="2f641-223">In this section</span></span>

- [<span data-ttu-id="2f641-224">Zugriff auf eine Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f641-224">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="2f641-225">Erstellen einer Terminserie mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f641-225">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="2f641-226">Löschen der Termine in einer Terminserie mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f641-226">Delete appointments in a recurring series by using EWS in Exchange</span></span>](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="2f641-227">Aktualisieren einer Terminserie mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="2f641-227">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="2f641-228">Aktualisieren einer Terminserie mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f641-228">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="2f641-229">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f641-229">See also</span></span>


- [<span data-ttu-id="2f641-230">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f641-230">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="2f641-231">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="2f641-231">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="2f641-232">Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f641-232">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

