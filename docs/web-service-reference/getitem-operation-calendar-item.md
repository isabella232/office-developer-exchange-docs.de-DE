---
title: GetItem-Vorgang (Kalenderelement)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8
description: Die GetItem Operation ruft Kalenderelemente aus den Exchange-Speicher ab.
ms.openlocfilehash: 69bce0f0cc7b5c986f9bf4767c3cd429a309e50d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758704"
---
# <a name="getitem-operation-calendar-item"></a><span data-ttu-id="553b9-103">GetItem-Vorgang (Kalenderelement)</span><span class="sxs-lookup"><span data-stu-id="553b9-103">GetItem operation (calendar item)</span></span>

<span data-ttu-id="553b9-104">Die GetItem Operation ruft Kalenderelemente aus den Exchange-Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="553b9-104">The GetItem operation gets calendar items from the Exchange store.</span></span>
  
## <a name="getitem-request-example"></a><span data-ttu-id="553b9-105">GetItem-anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="553b9-105">GetItem request example</span></span>

### <a name="description"></a><span data-ttu-id="553b9-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="553b9-106">Description</span></span>

<span data-ttu-id="553b9-107">Im folgenden Beispiel wird eine Anforderung GetItem bilden eine Anforderung zum Abrufen der Identität und den Betreff eines Elements veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="553b9-107">The following example of a GetItem request shows how to form a request to get the identity and subject of an item.</span></span>
  
### <a name="code"></a><span data-ttu-id="553b9-108">Code</span><span class="sxs-lookup"><span data-stu-id="553b9-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AsdD89=" ChangeKey="Jajs3=="/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="553b9-109">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="553b9-109">Request elements</span></span>

<span data-ttu-id="553b9-110">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="553b9-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="553b9-111">GetItem</span><span class="sxs-lookup"><span data-stu-id="553b9-111">GetItem</span></span>](getitem.md)
    
- [<span data-ttu-id="553b9-112">ItemShape</span><span class="sxs-lookup"><span data-stu-id="553b9-112">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="553b9-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="553b9-113">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="553b9-114">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="553b9-114">AdditionalProperties</span></span>](additionalproperties.md)
    
- [<span data-ttu-id="553b9-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="553b9-115">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="553b9-116">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="553b9-116">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="553b9-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="553b9-117">ItemId</span></span>](itemid.md)
    
> [!NOTE]
> <span data-ttu-id="553b9-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="553b9-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="553b9-119">Um weitere Optionen für die Anforderung an den GetItem Operation zu suchen, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="553b9-119">To find other options for the request message of the GetItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="553b9-120">Starten Sie das [GetItem](getitem.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="553b9-120">Start at the [GetItem](getitem.md) element.</span></span> 
  
## <a name="successful-getitem-response"></a><span data-ttu-id="553b9-121">Erfolgreiche GetItem-Antwort</span><span class="sxs-lookup"><span data-stu-id="553b9-121">Successful GetItem Response</span></span>

### <a name="description"></a><span data-ttu-id="553b9-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="553b9-122">Description</span></span>

<span data-ttu-id="553b9-123">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung GetItem.</span><span class="sxs-lookup"><span data-stu-id="553b9-123">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="553b9-124">Die Anforderung, die dieser Antwort erstellt verwendet die IdOnly Baseshape.</span><span class="sxs-lookup"><span data-stu-id="553b9-124">The request that created this response used the IdOnly baseshape.</span></span> <span data-ttu-id="553b9-125">In diesem Beispiel wird nur die ID des Elements die Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="553b9-125">In this example, the response returns only the ID of the item.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="553b9-126">Die Element-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="553b9-126">The item ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="553b9-127">Code</span><span class="sxs-lookup"><span data-stu-id="553b9-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                   xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="ASUAd" ChangeKey="otlIqB=="/>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="description"></a><span data-ttu-id="553b9-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="553b9-128">Description</span></span>

<span data-ttu-id="553b9-129">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung GetItem.</span><span class="sxs-lookup"><span data-stu-id="553b9-129">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="553b9-130">Die Anforderung, die dieser Antwort erstellt verwendet die standardmäßige Baseshape.</span><span class="sxs-lookup"><span data-stu-id="553b9-130">The request that created this response used the Default baseshape.</span></span> <span data-ttu-id="553b9-131">In diesem Beispiel gibt die Antwort die Standardform für ein Kalenderelement zurück.</span><span class="sxs-lookup"><span data-stu-id="553b9-131">In this example, the response returns the Default shape for a calendar item.</span></span>
  
> [!NOTE]
> <span data-ttu-id="553b9-132">Die Element-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="553b9-132">The item ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="553b9-133">Code</span><span class="sxs-lookup"><span data-stu-id="553b9-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="ASUAdTB" ChangeKey="otlIqBwrt=="/>
              <t:ResponseObjects>
                <t:ForwardItem/>
              </t:ResponseObjects>
              <t:Start>2006-06-16T00:30:00Z</t:Start>
              <t:End>2006-06-16T01:00:00Z</t:End>
              <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
              <t:CalendarItemType>Single</t:CalendarItemType>
              <t:Organizer>
                <t:Mailbox>
                  <t:Name>Bob</t:Name>
                  <t:EmailAddress>someone@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:Organizer>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="description"></a><span data-ttu-id="553b9-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="553b9-134">Description</span></span>

<span data-ttu-id="553b9-135">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung GetItem.</span><span class="sxs-lookup"><span data-stu-id="553b9-135">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="553b9-136">Die Anforderung, die dieser Antwort erstellt verwendet die AllProperties Baseshape.</span><span class="sxs-lookup"><span data-stu-id="553b9-136">The request that created this response used the AllProperties baseshape.</span></span> <span data-ttu-id="553b9-137">In diesem Beispiel gibt die Antwort das AllProperties-Shape für ein Kalenderelement zurück.</span><span class="sxs-lookup"><span data-stu-id="553b9-137">In this example, the response returns the AllProperties shape for a calendar item.</span></span>
  
### <a name="code"></a><span data-ttu-id="553b9-138">Code</span><span class="sxs-lookup"><span data-stu-id="553b9-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="ASUAdT" ChangeKey="otlIqB=="/>
              <t:ParentFolderId Id="ASUAdT=="/>
              <t:ItemClass>IPM.Appointment</t:ItemClass>
              <t:Sensitivity>Normal</t:Sensitivity>
              <t:Body BodyType="Text"/>
              <t:DateTimeReceived>2006-06-16T00:12:41Z</t:DateTimeReceived>
              <t:Size>374</t:Size>
              <t:Importance>Normal</t:Importance>
              <t:IsSubmitted>false</t:IsSubmitted>
              <t:IsDraft>false</t:IsDraft>
              <t:IsFromMe>false</t:IsFromMe>
              <t:IsResend>false</t:IsResend>
              <t:IsUnmodified>false</t:IsUnmodified>
              <t:DateTimeSent>2006-06-16T00:12:41Z</t:DateTimeSent>
              <t:DateTimeCreated>2006-06-16T00:12:41Z</t:DateTimeCreated>
              <t:ResponseObjects>
                <t:ForwardItem/>
              </t:ResponseObjects>
              <t:ReminderDueBy>2006-06-16T00:30:00Z</t:ReminderDueBy>
              <t:ReminderIsSet>true</t:ReminderIsSet>
              <t:ReminderMinutesBeforeStart>15</t:ReminderMinutesBeforeStart>
              <t:DisplayCc/>
              <t:DisplayTo/>
              <t:HasAttachments>false</t:HasAttachments>
              <t:Culture>en-US</t:Culture>
              <t:Start>2006-06-16T00:30:00Z</t:Start>
              <t:End>2006-06-16T01:00:00Z</t:End>
              <t:IsAllDayEvent>false</t:IsAllDayEvent>
              <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
              <t:IsMeeting>false</t:IsMeeting>
              <t:IsCancelled>false</t:IsCancelled>
              <t:IsRecurring>false</t:IsRecurring>
              <t:MeetingRequestWasSent>false</t:MeetingRequestWasSent>
              <t:CalendarItemType>Single</t:CalendarItemType>
              <t:MyResponseType>Organizer</t:MyResponseType>
              <t:Organizer>
                <t:Mailbox>
                  <t:Name>Bob</t:Name>
                  <t:EmailAddress>someone@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:Organizer>
              <t:ConflictingMeetingCount>2</t:ConflictingMeetingCount>
              <t:AdjacentMeetingCount>0</t:AdjacentMeetingCount>
              <t:ConflictingMeetings>
                <t:CalendarItem>
                  <t:ItemId Id="ASUAdTB" ChangeKey="otlIqBwr=="/>
                  <t:Subject/>
                  <t:Start>2006-06-16T00:30:00Z</t:Start>
                  <t:End>2006-06-16T01:00:00Z</t:End>
                  <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
                  <t:Location/>
                </t:CalendarItem>
                <t:CalendarItem>
                  <t:ItemId Id="ASUAd" ChangeKey="otlIqBw=="/>
                  <t:Subject/>
                  <t:Start>2006-06-16T00:30:00Z</t:Start>
                  <t:End>2006-06-16T01:00:00Z</t:End>
                  <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
                  <t:Location/>
                </t:CalendarItem>
              </t:ConflictingMeetings>
              <t:Duration>PT30M</t:Duration>
              <t:TimeZone>Pacific Standard Time</t:TimeZone>
              <t:AppointmentSequenceNumber>0</t:AppointmentSequenceNumber>
              <t:AppointmentState>0</t:AppointmentState>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="553b9-139">Kommentare</span><span class="sxs-lookup"><span data-stu-id="553b9-139">Comments</span></span>

<span data-ttu-id="553b9-140">Wenn andere Optionen für die Antwortnachricht des Vorgangs GetItem suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="553b9-140">To find other options for the response message of the GetItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="553b9-141">Starten Sie das [GetItemResponse](getitemresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="553b9-141">Start at the [GetItemResponse](getitemresponse.md) element.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="553b9-142">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="553b9-142">Successful response elements</span></span>

<span data-ttu-id="553b9-143">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="553b9-143">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="553b9-144">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="553b9-144">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="553b9-145">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="553b9-145">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="553b9-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="553b9-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="553b9-147">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="553b9-147">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="553b9-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="553b9-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="553b9-149">Elemente</span><span class="sxs-lookup"><span data-stu-id="553b9-149">Items</span></span>](items.md)
    
- [<span data-ttu-id="553b9-150">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="553b9-150">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="553b9-151">ItemId</span><span class="sxs-lookup"><span data-stu-id="553b9-151">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="553b9-152">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="553b9-152">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="553b9-153">ItemClass</span><span class="sxs-lookup"><span data-stu-id="553b9-153">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="553b9-154">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="553b9-154">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="553b9-155">Body</span><span class="sxs-lookup"><span data-stu-id="553b9-155">Body</span></span>](body.md)
    
- [<span data-ttu-id="553b9-156">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="553b9-156">DateTimeReceived</span></span>](datetimereceived.md)
    
- [<span data-ttu-id="553b9-157">Size</span><span class="sxs-lookup"><span data-stu-id="553b9-157">Size</span></span>](size.md)
    
- [<span data-ttu-id="553b9-158">Importance</span><span class="sxs-lookup"><span data-stu-id="553b9-158">Importance</span></span>](importance.md)
    
- [<span data-ttu-id="553b9-159">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="553b9-159">IsSubmitted</span></span>](issubmitted.md)
    
- [<span data-ttu-id="553b9-160">IsDraft</span><span class="sxs-lookup"><span data-stu-id="553b9-160">IsDraft</span></span>](isdraft.md)
    
- [<span data-ttu-id="553b9-161">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="553b9-161">IsFromMe</span></span>](isfromme.md)
    
- [<span data-ttu-id="553b9-162">IsResend</span><span class="sxs-lookup"><span data-stu-id="553b9-162">IsResend</span></span>](isresend.md)
    
- [<span data-ttu-id="553b9-163">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="553b9-163">IsUnmodified</span></span>](isunmodified.md)
    
- [<span data-ttu-id="553b9-164">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="553b9-164">DateTimeSent</span></span>](datetimesent.md)
    
- [<span data-ttu-id="553b9-165">"Datetimecreated"</span><span class="sxs-lookup"><span data-stu-id="553b9-165">DateTimeCreated</span></span>](datetimecreated.md)
    
- [<span data-ttu-id="553b9-166">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="553b9-166">ResponseObjects</span></span>](responseobjects.md)
    
- [<span data-ttu-id="553b9-167">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="553b9-167">ForwardItem</span></span>](forwarditem.md)
    
- [<span data-ttu-id="553b9-168">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="553b9-168">ReminderDueBy</span></span>](reminderdueby.md)
    
- [<span data-ttu-id="553b9-169">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="553b9-169">ReminderIsSet</span></span>](reminderisset.md)
    
- [<span data-ttu-id="553b9-170">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="553b9-170">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md)
    
- [<span data-ttu-id="553b9-171">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="553b9-171">DisplayCc</span></span>](displaycc.md)
    
- [<span data-ttu-id="553b9-172">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="553b9-172">DisplayTo</span></span>](displayto.md)
    
- [<span data-ttu-id="553b9-173">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="553b9-173">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="553b9-174">Kultur</span><span class="sxs-lookup"><span data-stu-id="553b9-174">Culture</span></span>](culture.md)
    
- [<span data-ttu-id="553b9-175">Start</span><span class="sxs-lookup"><span data-stu-id="553b9-175">Start</span></span>](start.md)
    
- [<span data-ttu-id="553b9-176">Ende</span><span class="sxs-lookup"><span data-stu-id="553b9-176">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="553b9-177">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="553b9-177">IsAllDayEvent</span></span>](isalldayevent.md)
    
- [<span data-ttu-id="553b9-178">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="553b9-178">LegacyFreeBusyStatus</span></span>](legacyfreebusystatus.md)
    
- [<span data-ttu-id="553b9-179">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="553b9-179">IsMeeting</span></span>](ismeeting.md)
    
- [<span data-ttu-id="553b9-180">IsCancelled</span><span class="sxs-lookup"><span data-stu-id="553b9-180">IsCancelled</span></span>](iscancelled.md)
    
- [<span data-ttu-id="553b9-181">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="553b9-181">IsRecurring</span></span>](isrecurring.md)
    
- [<span data-ttu-id="553b9-182">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="553b9-182">MeetingRequestWasSent</span></span>](meetingrequestwassent.md)
    
- [<span data-ttu-id="553b9-183">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="553b9-183">CalendarItemType</span></span>](calendaritemtype.md)
    
- [<span data-ttu-id="553b9-184">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="553b9-184">MyResponseType</span></span>](myresponsetype.md)
    
- [<span data-ttu-id="553b9-185">Organisator</span><span class="sxs-lookup"><span data-stu-id="553b9-185">Organizer</span></span>](organizer.md)
    
- [<span data-ttu-id="553b9-186">Postfach</span><span class="sxs-lookup"><span data-stu-id="553b9-186">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="553b9-187">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="553b9-187">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="553b9-188">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="553b9-188">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="553b9-189">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="553b9-189">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="553b9-190">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="553b9-190">ConflictingMeetingCount</span></span>](conflictingmeetingcount.md)
    
- [<span data-ttu-id="553b9-191">AdjacentMeetingCount</span><span class="sxs-lookup"><span data-stu-id="553b9-191">AdjacentMeetingCount</span></span>](adjacentmeetingcount.md)
    
- [<span data-ttu-id="553b9-192">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="553b9-192">ConflictingMeetings</span></span>](conflictingmeetings.md)
    
- [<span data-ttu-id="553b9-193">Ort</span><span class="sxs-lookup"><span data-stu-id="553b9-193">Location</span></span>](location.md)
    
- [<span data-ttu-id="553b9-194">Dauer (Elemente)</span><span class="sxs-lookup"><span data-stu-id="553b9-194">Duration (Items)</span></span>](duration-items.md)
    
- [<span data-ttu-id="553b9-195">TimeZone (Element)</span><span class="sxs-lookup"><span data-stu-id="553b9-195">TimeZone (Item)</span></span>](timezone-item.md)
    
- [<span data-ttu-id="553b9-196">AppointmentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="553b9-196">AppointmentSequenceNumber</span></span>](appointmentsequencenumber.md)
    
- [<span data-ttu-id="553b9-197">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="553b9-197">AppointmentState</span></span>](appointmentstate.md)
    
## <a name="see-also"></a><span data-ttu-id="553b9-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="553b9-198">See also</span></span>



[<span data-ttu-id="553b9-199">GetItem Operation</span><span class="sxs-lookup"><span data-stu-id="553b9-199">GetItem operation</span></span>](getitem-operation.md)

