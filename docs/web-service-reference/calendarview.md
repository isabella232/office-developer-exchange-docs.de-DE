---
title: CalendarView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarView
api_type:
- schema
ms.assetid: a4a953b8-0710-416c-95ef-59e51eba9982
description: Das CalendarView-Element definiert eine FindItem-Operation als zurückgeben von Kalenderelementen in einer Gruppe, wie Sie in einem Kalender angezeigt werden.
ms.openlocfilehash: e547a4b2db5c09ebefd9a072da6cc4733818002e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462262"
---
# <a name="calendarview"></a><span data-ttu-id="c6127-103">CalendarView</span><span class="sxs-lookup"><span data-stu-id="c6127-103">CalendarView</span></span>

<span data-ttu-id="c6127-104">Das **CalendarView** -Element definiert eine [FindItem-Operation](finditem-operation.md) als zurückgeben von Kalenderelementen in einer Gruppe, wie Sie in einem Kalender angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c6127-104">The **CalendarView** element defines a [FindItem operation](finditem-operation.md) as returning calendar items in a set as they appear in a calendar.</span></span> 
  
[<span data-ttu-id="c6127-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="c6127-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="c6127-106">CalendarView</span><span class="sxs-lookup"><span data-stu-id="c6127-106">CalendarView</span></span>](calendarview.md)
  
```XML
<CalendarView MaxEntriesReturned="" StartDate="" EndDate="" />
```

<span data-ttu-id="c6127-107">**CalendarView**</span><span class="sxs-lookup"><span data-stu-id="c6127-107">**CalendarView**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c6127-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c6127-108">Attributes and elements</span></span>

<span data-ttu-id="c6127-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c6127-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6127-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="c6127-110">Attributes</span></span>

|<span data-ttu-id="c6127-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c6127-111">**Attribute**</span></span>|<span data-ttu-id="c6127-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c6127-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6127-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="c6127-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="c6127-114">Beschreibt die maximale Anzahl von Ergebnissen, die in der FindItem-Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c6127-114">Describes the maximum number of results to return in the FindItem response.</span></span>  <br/> |
|<span data-ttu-id="c6127-115">**StartDate**</span><span class="sxs-lookup"><span data-stu-id="c6127-115">**StartDate**</span></span> <br/> |<span data-ttu-id="c6127-116">Gibt den Anfang einer Zeitspanne an, die für Kalenderelemente abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="c6127-116">Identifies the start of a time span queried for calendar items.</span></span> <span data-ttu-id="c6127-117">Alle Kalenderelemente mit einer Endzeit, die vor dem Start **Datum** liegt, werden nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6127-117">All calendar items that have an end time that is before **StartDate** will not be returned.</span></span> <span data-ttu-id="c6127-118">Der Wert von **StartDate** kann in koordinierte Weltzeit (UTC) Format angegeben werden, wie in 2006-01-02T12:00:00Z oder in einem Format, in dem der lokale Zeit-und Zeitzonenoffset angegeben ist, wie in 2006-01-02T04:00:00-08:00.</span><span class="sxs-lookup"><span data-stu-id="c6127-118">The value of **StartDate** can be specified in coordinated universal time (UTC) format, as in 2006-01-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-01-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="c6127-119">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c6127-119">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="c6127-120">**EndDate**</span><span class="sxs-lookup"><span data-stu-id="c6127-120">**EndDate**</span></span> <br/> |<span data-ttu-id="c6127-121">Gibt das Ende einer Zeitspanne an, die für Kalenderelemente abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="c6127-121">Identifies the end of a time span queried for calendar items.</span></span> <span data-ttu-id="c6127-122">Alle Kalenderelemente mit einer Startzeit, die sich auf oder nach **EndDate** befinden, werden nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6127-122">All calendar items that have a start time that is on or after **EndDate** will not be returned.</span></span> <span data-ttu-id="c6127-123">Der Wert von **EndDate** kann im UTC-Format angegeben werden, wie in 2006-02-02T12:00:00Z oder in einem Format, in dem der lokale Zeit-und Zeitzonenoffset angegeben ist, wie in 2006-02-02T04:00:00-08:00.</span><span class="sxs-lookup"><span data-stu-id="c6127-123">The value of **EndDate** can be specified in UTC format, as in 2006-02-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-02-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="c6127-124">**EndDate** muss größer als oder gleich **StartDate**sein; Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6127-124">**EndDate** must be greater than or equal to **StartDate**; otherwise an error is returned.</span></span> <span data-ttu-id="c6127-125">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c6127-125">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c6127-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c6127-126">Child elements</span></span>

<span data-ttu-id="c6127-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="c6127-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c6127-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c6127-128">Parent elements</span></span>

|<span data-ttu-id="c6127-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="c6127-129">**Element**</span></span>|<span data-ttu-id="c6127-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c6127-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6127-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="c6127-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="c6127-132">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="c6127-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="c6127-133">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="c6127-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6127-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6127-134">Remarks</span></span>

<span data-ttu-id="c6127-135">Wenn das **CalendarView** -Element in einer FindItem-Anforderung angegeben ist, gibt der Webdienst eine Liste einzelner Kalenderelemente und Vorkommen von wiederkehrenden Kalenderelementen innerhalb des durch **StartDate** und **EndDate**angegebenen Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="c6127-135">If the **CalendarView** element is specified in a FindItem request, the Web service returns a list of single calendar items and occurrences of recurring calendar items within the range specified by **StartDate** and **EndDate**.</span></span>
  
<span data-ttu-id="c6127-136">Wenn das **CalendarView** -Element in einer FindItem-Anforderung nicht angegeben ist, gibt der Webdienst eine Liste einzelner Kalenderelemente und wiederkehrende Master Kalenderelemente zurück.</span><span class="sxs-lookup"><span data-stu-id="c6127-136">If the **CalendarView** element is not specified in a FindItem request, the Web service returns a list of single calendar items and recurring master calendar items.</span></span> <span data-ttu-id="c6127-137">Kalender Vorkommen eines wiederkehrenden Kalenderelements werden nicht erweitert.</span><span class="sxs-lookup"><span data-stu-id="c6127-137">Calendar occurrences of a recurring calendar item are not expanded.</span></span> 
  
<span data-ttu-id="c6127-138">CalendarView-Abfragen sollten nur die folgenden Eigenschaften verwenden, da Sie schnellere Kalenderabfragen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c6127-138">CalendarView queries should only make use of the following properties since they support faster calendar queries.</span></span>
  
### <a name="recurrence-blob-properties"></a><span data-ttu-id="c6127-139">Serien-BLOB-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6127-139">Recurrence blob properties</span></span>
  
- <span data-ttu-id="c6127-140">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="c6127-140">MapiStartTime</span></span>
    
- <span data-ttu-id="c6127-141">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="c6127-141">MapiEndTime</span></span>
    
- <span data-ttu-id="c6127-142">SubjectPrefixInternal</span><span class="sxs-lookup"><span data-stu-id="c6127-142">SubjectPrefixInternal</span></span>
    
- <span data-ttu-id="c6127-143">NormalizedSubjectInternal</span><span class="sxs-lookup"><span data-stu-id="c6127-143">NormalizedSubjectInternal</span></span>
    
- <span data-ttu-id="c6127-144">MapiSubject</span><span class="sxs-lookup"><span data-stu-id="c6127-144">MapiSubject</span></span>
    
- <span data-ttu-id="c6127-145">Standort</span><span class="sxs-lookup"><span data-stu-id="c6127-145">Location</span></span>
    
- <span data-ttu-id="c6127-146">AppointmentColor</span><span class="sxs-lookup"><span data-stu-id="c6127-146">AppointmentColor</span></span>
    
- <span data-ttu-id="c6127-147">MapiIsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="c6127-147">MapiIsAllDayEvent</span></span>
    
- <span data-ttu-id="c6127-148">MapiHasAttachment</span><span class="sxs-lookup"><span data-stu-id="c6127-148">MapiHasAttachment</span></span>
    
- <span data-ttu-id="c6127-149">FreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="c6127-149">FreeBusyStatus</span></span>
    
- <span data-ttu-id="c6127-150">ReminderIsSetInternal</span><span class="sxs-lookup"><span data-stu-id="c6127-150">ReminderIsSetInternal</span></span>
    
- <span data-ttu-id="c6127-151">ReminderMinutesBeforeStartInternal</span><span class="sxs-lookup"><span data-stu-id="c6127-151">ReminderMinutesBeforeStartInternal</span></span>
    
- <span data-ttu-id="c6127-152">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="c6127-152">AppointmentState</span></span>
    
- <span data-ttu-id="c6127-153">AllAttachmentsHidden</span><span class="sxs-lookup"><span data-stu-id="c6127-153">AllAttachmentsHidden</span></span>
    
- <span data-ttu-id="c6127-154">ChangeHighlight</span><span class="sxs-lookup"><span data-stu-id="c6127-154">ChangeHighlight</span></span>
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a><span data-ttu-id="c6127-155">Berechnet aus dem primären Serien-BLOB oder-Stamm</span><span class="sxs-lookup"><span data-stu-id="c6127-155">Calculated from the primary recurrence blob or master</span></span>
  
- <span data-ttu-id="c6127-156">Itemid</span><span class="sxs-lookup"><span data-stu-id="c6127-156">ItemId</span></span>
    
- <span data-ttu-id="c6127-157">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="c6127-157">IsRecurring</span></span>
    
- <span data-ttu-id="c6127-158">Isexception</span><span class="sxs-lookup"><span data-stu-id="c6127-158">IsException</span></span>
    
- <span data-ttu-id="c6127-159">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="c6127-159">AppointmentRecurring</span></span>
    
- <span data-ttu-id="c6127-160">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="c6127-160">MapiStartTime</span></span>
    
- <span data-ttu-id="c6127-161">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="c6127-161">MapiPRStartDate</span></span>
    
- <span data-ttu-id="c6127-162">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="c6127-162">MapiEndTime</span></span>
    
- <span data-ttu-id="c6127-163">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="c6127-163">MapiPREndDate</span></span>
    
- <span data-ttu-id="c6127-164">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="c6127-164">CalendarItemType</span></span>
    
- <span data-ttu-id="c6127-165">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="c6127-165">GlobalObjectId</span></span>
    
- <span data-ttu-id="c6127-166">TimeZoneDefinitionStart</span><span class="sxs-lookup"><span data-stu-id="c6127-166">TimeZoneDefinitionStart</span></span>
    
- <span data-ttu-id="c6127-167">TimeZoneDefinitionEnd</span><span class="sxs-lookup"><span data-stu-id="c6127-167">TimeZoneDefinitionEnd</span></span>
    
### <a name="master-calendar-item-properties"></a><span data-ttu-id="c6127-168">Eigenschaften des Master Kalenderelements</span><span class="sxs-lookup"><span data-stu-id="c6127-168">Master calendar item properties</span></span>
  
- <span data-ttu-id="c6127-169">EntryId</span><span class="sxs-lookup"><span data-stu-id="c6127-169">EntryId</span></span>
    
- <span data-ttu-id="c6127-170">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="c6127-170">ChangeKey</span></span>
    
- <span data-ttu-id="c6127-171">ItemClass</span><span class="sxs-lookup"><span data-stu-id="c6127-171">ItemClass</span></span>
    
- <span data-ttu-id="c6127-172">SentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c6127-172">SentRepresentingEmailAddress</span></span>
    
- <span data-ttu-id="c6127-173">SentRepresentingDisplayName</span><span class="sxs-lookup"><span data-stu-id="c6127-173">SentRepresentingDisplayName</span></span>
    
- <span data-ttu-id="c6127-174">SentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="c6127-174">SentRepresentingEntryId</span></span>
    
- <span data-ttu-id="c6127-175">AppointmentRecurrenceBlob</span><span class="sxs-lookup"><span data-stu-id="c6127-175">AppointmentRecurrenceBlob</span></span>
    
- <span data-ttu-id="c6127-176">TimeZone</span><span class="sxs-lookup"><span data-stu-id="c6127-176">TimeZone</span></span>
    
- <span data-ttu-id="c6127-177">TimeZoneBlob</span><span class="sxs-lookup"><span data-stu-id="c6127-177">TimeZoneBlob</span></span>
    
- <span data-ttu-id="c6127-178">TimeZoneDefinitionRecurring</span><span class="sxs-lookup"><span data-stu-id="c6127-178">TimeZoneDefinitionRecurring</span></span>
    
- <span data-ttu-id="c6127-179">CleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="c6127-179">CleanGlobalObjectId</span></span>
    
- <span data-ttu-id="c6127-180">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="c6127-180">AppointmentRecurring</span></span>
    
- <span data-ttu-id="c6127-181">Isexception</span><span class="sxs-lookup"><span data-stu-id="c6127-181">IsException</span></span>
    
- <span data-ttu-id="c6127-182">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="c6127-182">IsRecurring</span></span>
    
- <span data-ttu-id="c6127-183">MapiSensitivity</span><span class="sxs-lookup"><span data-stu-id="c6127-183">MapiSensitivity</span></span>
    
- <span data-ttu-id="c6127-184">ContainerClass</span><span class="sxs-lookup"><span data-stu-id="c6127-184">ContainerClass</span></span>
    
- <span data-ttu-id="c6127-185">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="c6127-185">MapiPRStartDate</span></span>
    
- <span data-ttu-id="c6127-186">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="c6127-186">MapiPREndDate</span></span>
    
- <span data-ttu-id="c6127-187">Kategorien</span><span class="sxs-lookup"><span data-stu-id="c6127-187">Categories</span></span>
    
<span data-ttu-id="c6127-188">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c6127-188">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="c6127-189">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c6127-189">Example</span></span>

<span data-ttu-id="c6127-190">Das folgende Beispiel zeigt eine FindItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c6127-190">The following example shows a FindItem request.</span></span> <span data-ttu-id="c6127-191">Bei einer erfolgreichen Anforderung wird eine Antwort zurückgegeben, die Kalenderelemente enthält, die in 2006-05-18T00:00:00-08:00 oder nach gestartet und vor 2006-05-19T00:00:00-08:00-beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c6127-191">A successful request returns a response that includes calendar items that started at 2006-05-18T00:00:00-08:00 or after and ended before 2006-05-19T00:00:00-08:00.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="calendar:Start"/>
          <t:FieldURI FieldURI="calendar:End"/>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <CalendarView MaxEntriesReturned="2" StartDate="2006-05-18T00:00:00-08:00" EndDate="2006-05-19T00:00:00-08:00"/>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="c6127-192">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c6127-192">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6127-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6127-193">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c6127-194">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c6127-194">Schema Name</span></span>  <br/> |<span data-ttu-id="c6127-195">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c6127-195">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c6127-196">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c6127-196">Validation File</span></span>  <br/> |<span data-ttu-id="c6127-197">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c6127-197">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c6127-198">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c6127-198">Can be Empty</span></span>  <br/> |<span data-ttu-id="c6127-199">False</span><span class="sxs-lookup"><span data-stu-id="c6127-199">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6127-200">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6127-200">See also</span></span>

- [<span data-ttu-id="c6127-201">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c6127-201">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="c6127-202">Finding Items</span><span class="sxs-lookup"><span data-stu-id="c6127-202">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

