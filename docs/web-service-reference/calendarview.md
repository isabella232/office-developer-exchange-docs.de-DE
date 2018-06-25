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
description: Das CalendarView-Element definiert einen Vorgang FindItem als Kalenderelemente in einem Satz zurückgeben, wenn sie in einem Kalender angezeigt werden.
ms.openlocfilehash: 79b5ad268a8013092c1122c99bdcd10d876abf2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757543"
---
# <a name="calendarview"></a><span data-ttu-id="0b6ef-103">CalendarView</span><span class="sxs-lookup"><span data-stu-id="0b6ef-103">CalendarView</span></span>

<span data-ttu-id="0b6ef-104">Das **CalendarView** -Element definiert einen [Vorgang FindItem](finditem-operation.md) als Kalenderelemente in einem Satz zurückgeben, wenn sie in einem Kalender angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-104">The **CalendarView** element defines a [FindItem operation](finditem-operation.md) as returning calendar items in a set as they appear in a calendar.</span></span> 
  
[<span data-ttu-id="0b6ef-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="0b6ef-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="0b6ef-106">CalendarView</span><span class="sxs-lookup"><span data-stu-id="0b6ef-106">CalendarView</span></span>](calendarview.md)
  
```XML
<CalendarView MaxEntriesReturned="" StartDate="" EndDate="" />
```

<span data-ttu-id="0b6ef-107">**CalendarView**</span><span class="sxs-lookup"><span data-stu-id="0b6ef-107">**CalendarView**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0b6ef-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0b6ef-108">Attributes and elements</span></span>

<span data-ttu-id="0b6ef-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b6ef-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0b6ef-110">Attributes</span></span>

|<span data-ttu-id="0b6ef-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0b6ef-111">**Attribute**</span></span>|<span data-ttu-id="0b6ef-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b6ef-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b6ef-113">**"MaxEntriesReturned"**</span><span class="sxs-lookup"><span data-stu-id="0b6ef-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="0b6ef-114">Beschreibt die maximale Anzahl der in der Antwort FindItem zurückzugebender Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-114">Describes the maximum number of results to return in the FindItem response.</span></span>  <br/> |
|<span data-ttu-id="0b6ef-115">**StartDate**</span><span class="sxs-lookup"><span data-stu-id="0b6ef-115">**StartDate**</span></span> <br/> |<span data-ttu-id="0b6ef-116">Identifiziert den Anfang einer bestimmten Zeitspanne für Kalenderelemente abgefragt.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-116">Identifies the start of a time span queried for calendar items.</span></span> <span data-ttu-id="0b6ef-117">Alle Kalenderelemente, die eine Endzeit verfügen, bevor **StartDate** nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-117">All calendar items that have an end time that is before **StartDate** will not be returned.</span></span> <span data-ttu-id="0b6ef-118">Der Wert der **StartDate** angegeben werden kann, in koordinierter Weltzeit (UTC) Format, z. B. 2006-01-02T12:00:00Z, oder in einem Format, in dem Ortszeit sowie zur Zeitzone Offset, wie in 2006 angegeben ist-01-02T04:00:00-08:00.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-118">The value of **StartDate** can be specified in coordinated universal time (UTC) format, as in 2006-01-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-01-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="0b6ef-119">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-119">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="0b6ef-120">**EndDate**</span><span class="sxs-lookup"><span data-stu-id="0b6ef-120">**EndDate**</span></span> <br/> |<span data-ttu-id="0b6ef-121">Bezeichnet das Ende einer bestimmten Zeitspanne für Kalenderelemente abgefragt.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-121">Identifies the end of a time span queried for calendar items.</span></span> <span data-ttu-id="0b6ef-122">Alle Elemente im Kalender, die eine Startzeit aufweisen, die am oder nach dem **EndDate** ist werden nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-122">All calendar items that have a start time that is on or after **EndDate** will not be returned.</span></span> <span data-ttu-id="0b6ef-123">Der Wert der **EndDate** angegeben werden kann, im UTC-Format, wie in 2006-02-02T12:00:00Z, oder in einem Format, in dem Ortszeit sowie zur Zeitzone Offset, wie in 2006 angegeben ist-02-02T04:00:00-08:00.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-123">The value of **EndDate** can be specified in UTC format, as in 2006-02-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-02-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="0b6ef-124">**EndDate** muss größer als oder gleich **"StartDate"** sein. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-124">**EndDate** must be greater than or equal to **StartDate**; otherwise an error is returned.</span></span> <span data-ttu-id="0b6ef-125">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-125">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0b6ef-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b6ef-126">Child elements</span></span>

<span data-ttu-id="0b6ef-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0b6ef-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b6ef-128">Parent elements</span></span>

|<span data-ttu-id="0b6ef-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="0b6ef-129">**Element**</span></span>|<span data-ttu-id="0b6ef-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b6ef-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b6ef-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="0b6ef-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="0b6ef-132">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="0b6ef-133">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="0b6ef-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b6ef-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b6ef-134">Remarks</span></span>

<span data-ttu-id="0b6ef-135">Wenn das **CalendarView** -Element in einer Anforderung FindItem angegeben ist, wird eine Liste der einzelnen Kalenderelemente und Vorkommen des wiederkehrende Kalenderelemente innerhalb des Bereichs **StartDate** und **EndDate**angegeben wird von der Webdienst zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-135">If the **CalendarView** element is specified in a FindItem request, the Web service returns a list of single calendar items and occurrences of recurring calendar items within the range specified by **StartDate** and **EndDate**.</span></span>
  
<span data-ttu-id="0b6ef-136">Wenn das **CalendarView** -Element in einer Anforderung FindItem nicht angegeben ist, gibt der Webdienst eine Liste der einzelnen Kalenderelemente und wiederkehrende Kalenderelemente Master-Shape zurück.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-136">If the **CalendarView** element is not specified in a FindItem request, the Web service returns a list of single calendar items and recurring master calendar items.</span></span> <span data-ttu-id="0b6ef-137">Kalender Vorkommen eines sich wiederholenden Kalenderelements werden nicht erweitert.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-137">Calendar occurrences of a recurring calendar item are not expanded.</span></span> 
  
<span data-ttu-id="0b6ef-138">CalendarView Abfragen sollten nur vornehmen der folgenden Eigenschaften verwendet werden, da sie schnellere Kalenderabfragen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-138">CalendarView queries should only make use of the following properties since they support faster calendar queries.</span></span>
  
### <a name="recurrence-blob-properties"></a><span data-ttu-id="0b6ef-139">Serie BLOB-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b6ef-139">Recurrence blob properties</span></span>
  
- <span data-ttu-id="0b6ef-140">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="0b6ef-140">MapiStartTime</span></span>
    
- <span data-ttu-id="0b6ef-141">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="0b6ef-141">MapiEndTime</span></span>
    
- <span data-ttu-id="0b6ef-142">SubjectPrefixInternal</span><span class="sxs-lookup"><span data-stu-id="0b6ef-142">SubjectPrefixInternal</span></span>
    
- <span data-ttu-id="0b6ef-143">NormalizedSubjectInternal</span><span class="sxs-lookup"><span data-stu-id="0b6ef-143">NormalizedSubjectInternal</span></span>
    
- <span data-ttu-id="0b6ef-144">MapiSubject</span><span class="sxs-lookup"><span data-stu-id="0b6ef-144">MapiSubject</span></span>
    
- <span data-ttu-id="0b6ef-145">Speicherort</span><span class="sxs-lookup"><span data-stu-id="0b6ef-145">Location</span></span>
    
- <span data-ttu-id="0b6ef-146">AppointmentColor</span><span class="sxs-lookup"><span data-stu-id="0b6ef-146">AppointmentColor</span></span>
    
- <span data-ttu-id="0b6ef-147">MapiIsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="0b6ef-147">MapiIsAllDayEvent</span></span>
    
- <span data-ttu-id="0b6ef-148">MapiHasAttachment</span><span class="sxs-lookup"><span data-stu-id="0b6ef-148">MapiHasAttachment</span></span>
    
- <span data-ttu-id="0b6ef-149">FreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="0b6ef-149">FreeBusyStatus</span></span>
    
- <span data-ttu-id="0b6ef-150">ReminderIsSetInternal</span><span class="sxs-lookup"><span data-stu-id="0b6ef-150">ReminderIsSetInternal</span></span>
    
- <span data-ttu-id="0b6ef-151">ReminderMinutesBeforeStartInternal</span><span class="sxs-lookup"><span data-stu-id="0b6ef-151">ReminderMinutesBeforeStartInternal</span></span>
    
- <span data-ttu-id="0b6ef-152">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="0b6ef-152">AppointmentState</span></span>
    
- <span data-ttu-id="0b6ef-153">AllAttachmentsHidden</span><span class="sxs-lookup"><span data-stu-id="0b6ef-153">AllAttachmentsHidden</span></span>
    
- <span data-ttu-id="0b6ef-154">ChangeHighlight</span><span class="sxs-lookup"><span data-stu-id="0b6ef-154">ChangeHighlight</span></span>
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a><span data-ttu-id="0b6ef-155">Aus dem primären Serienblob oder Master-Shape berechnet</span><span class="sxs-lookup"><span data-stu-id="0b6ef-155">Calculated from the primary recurrence blob or master</span></span>
  
- <span data-ttu-id="0b6ef-156">ItemId</span><span class="sxs-lookup"><span data-stu-id="0b6ef-156">ItemId</span></span>
    
- <span data-ttu-id="0b6ef-157">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="0b6ef-157">IsRecurring</span></span>
    
- <span data-ttu-id="0b6ef-158">IsException</span><span class="sxs-lookup"><span data-stu-id="0b6ef-158">IsException</span></span>
    
- <span data-ttu-id="0b6ef-159">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="0b6ef-159">AppointmentRecurring</span></span>
    
- <span data-ttu-id="0b6ef-160">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="0b6ef-160">MapiStartTime</span></span>
    
- <span data-ttu-id="0b6ef-161">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="0b6ef-161">MapiPRStartDate</span></span>
    
- <span data-ttu-id="0b6ef-162">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="0b6ef-162">MapiEndTime</span></span>
    
- <span data-ttu-id="0b6ef-163">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="0b6ef-163">MapiPREndDate</span></span>
    
- <span data-ttu-id="0b6ef-164">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="0b6ef-164">CalendarItemType</span></span>
    
- <span data-ttu-id="0b6ef-165">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="0b6ef-165">GlobalObjectId</span></span>
    
- <span data-ttu-id="0b6ef-166">TimeZoneDefinitionStart</span><span class="sxs-lookup"><span data-stu-id="0b6ef-166">TimeZoneDefinitionStart</span></span>
    
- <span data-ttu-id="0b6ef-167">TimeZoneDefinitionEnd</span><span class="sxs-lookup"><span data-stu-id="0b6ef-167">TimeZoneDefinitionEnd</span></span>
    
### <a name="master-calendar-item-properties"></a><span data-ttu-id="0b6ef-168">Elementeigenschaften Master Kalender</span><span class="sxs-lookup"><span data-stu-id="0b6ef-168">Master calendar item properties</span></span>
  
- <span data-ttu-id="0b6ef-169">EntryId</span><span class="sxs-lookup"><span data-stu-id="0b6ef-169">EntryId</span></span>
    
- <span data-ttu-id="0b6ef-170">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="0b6ef-170">ChangeKey</span></span>
    
- <span data-ttu-id="0b6ef-171">ItemClass</span><span class="sxs-lookup"><span data-stu-id="0b6ef-171">ItemClass</span></span>
    
- <span data-ttu-id="0b6ef-172">SentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0b6ef-172">SentRepresentingEmailAddress</span></span>
    
- <span data-ttu-id="0b6ef-173">SentRepresentingDisplayName</span><span class="sxs-lookup"><span data-stu-id="0b6ef-173">SentRepresentingDisplayName</span></span>
    
- <span data-ttu-id="0b6ef-174">SentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="0b6ef-174">SentRepresentingEntryId</span></span>
    
- <span data-ttu-id="0b6ef-175">AppointmentRecurrenceBlob</span><span class="sxs-lookup"><span data-stu-id="0b6ef-175">AppointmentRecurrenceBlob</span></span>
    
- <span data-ttu-id="0b6ef-176">TimeZone</span><span class="sxs-lookup"><span data-stu-id="0b6ef-176">TimeZone</span></span>
    
- <span data-ttu-id="0b6ef-177">TimeZoneBlob</span><span class="sxs-lookup"><span data-stu-id="0b6ef-177">TimeZoneBlob</span></span>
    
- <span data-ttu-id="0b6ef-178">TimeZoneDefinitionRecurring</span><span class="sxs-lookup"><span data-stu-id="0b6ef-178">TimeZoneDefinitionRecurring</span></span>
    
- <span data-ttu-id="0b6ef-179">CleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="0b6ef-179">CleanGlobalObjectId</span></span>
    
- <span data-ttu-id="0b6ef-180">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="0b6ef-180">AppointmentRecurring</span></span>
    
- <span data-ttu-id="0b6ef-181">IsException</span><span class="sxs-lookup"><span data-stu-id="0b6ef-181">IsException</span></span>
    
- <span data-ttu-id="0b6ef-182">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="0b6ef-182">IsRecurring</span></span>
    
- <span data-ttu-id="0b6ef-183">MapiSensitivity</span><span class="sxs-lookup"><span data-stu-id="0b6ef-183">MapiSensitivity</span></span>
    
- <span data-ttu-id="0b6ef-184">ContainerClass</span><span class="sxs-lookup"><span data-stu-id="0b6ef-184">ContainerClass</span></span>
    
- <span data-ttu-id="0b6ef-185">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="0b6ef-185">MapiPRStartDate</span></span>
    
- <span data-ttu-id="0b6ef-186">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="0b6ef-186">MapiPREndDate</span></span>
    
- <span data-ttu-id="0b6ef-187">Kategorien</span><span class="sxs-lookup"><span data-stu-id="0b6ef-187">Categories</span></span>
    
<span data-ttu-id="0b6ef-188">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-188">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="0b6ef-189">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0b6ef-189">Example</span></span>

<span data-ttu-id="0b6ef-190">Das folgende Beispiel zeigt eine FindItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-190">The following example shows a FindItem request.</span></span> <span data-ttu-id="0b6ef-191">Eine erfolgreiche Anforderung gibt eine Antwort mit Kalenderelementen (engl.), die Schritte unter 2006-05-18T00:00:00-08:00 oder nach und beendeten vor dem 2006-05-19T00:00:00-08:00.</span><span class="sxs-lookup"><span data-stu-id="0b6ef-191">A successful request returns a response that includes calendar items that started at 2006-05-18T00:00:00-08:00 or after and ended before 2006-05-19T00:00:00-08:00.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="0b6ef-192">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0b6ef-192">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b6ef-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b6ef-193">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0b6ef-194">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0b6ef-194">Schema Name</span></span>  <br/> |<span data-ttu-id="0b6ef-195">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0b6ef-195">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0b6ef-196">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0b6ef-196">Validation File</span></span>  <br/> |<span data-ttu-id="0b6ef-197">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0b6ef-197">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0b6ef-198">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0b6ef-198">Can be Empty</span></span>  <br/> |<span data-ttu-id="0b6ef-199">False</span><span class="sxs-lookup"><span data-stu-id="0b6ef-199">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0b6ef-200">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b6ef-200">See also</span></span>

- [<span data-ttu-id="0b6ef-201">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0b6ef-201">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="0b6ef-202">Finding Items</span><span class="sxs-lookup"><span data-stu-id="0b6ef-202">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

