---
title: CreateItem-Vorgang (Kalenderelement)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateItem
api_type:
- schema
ms.assetid: aa4a7c94-f668-4bd2-8079-c855f6ab17e1
description: Der CreateItem-Vorgang erstellt Kalenderelemente im Exchange Speicher.
ms.openlocfilehash: 4b2506dd4d5353c7670cab0ddb029e542d5861ba
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538422"
---
# <a name="createitem-operation-calendar-item"></a>CreateItem-Vorgang (Kalenderelement)

Der CreateItem-Vorgang erstellt Kalenderelemente im Exchange Speicher.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der CreateItem-Vorgang erstellt Termine, Besprechungen und Besprechungsanfragen. Wenn ein Kalenderelement ohne Teilnehmer erstellt wird, wird es als Termin betrachtet. Wenn Teilnehmer angegeben werden, ist das Kalenderelement eine Besprechung. Wenn eine Besprechung mithilfe des CreateItem-Vorgangs erstellt wird, werden Besprechungsanfragen automatisch an die identifizierten Teilnehmer gesendet, wenn das SendMeetingInvitations-Attribut so festgelegt ist, dass die Besprechungsanfragen gesendet werden.
  
## <a name="createitem-calendar-item-request-example"></a>CreateItem (Calendar Item)-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer CreateItem-Anforderung zeigt, wie Sie eine Besprechung mit zwei erforderlichen Teilnehmern erstellen. Diese Anforderung sendet die Besprechungsanfragen an die beiden Teilnehmer.
  
### <a name="code"></a>Code

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                SendMeetingInvitations="SendToAllAndSaveCopy" >
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar"/>
      </SavedItemFolderId>
      <Items>
        <t:CalendarItem xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Planning Meeting</Subject>
          <Body BodyType="Text">Plan the agenda for next week's meeting.</Body>
          <ReminderIsSet>true</ReminderIsSet>
          <ReminderMinutesBeforeStart>60</ReminderMinutesBeforeStart>
          <Start>2006-11-02T14:00:00</Start>
          <End>2006-11-02T15:00:00</End>
          <IsAllDayEvent>false</IsAllDayEvent>
          <LegacyFreeBusyStatus>Busy</LegacyFreeBusyStatus>
          <Location>Conference Room 721</Location>
          <RequiredAttendees>
            <Attendee>
              <Mailbox>
                <EmailAddress>User1@example.com</EmailAddress>
              </Mailbox>
            </Attendee>
            <Attendee>
              <Mailbox>
                <EmailAddress>User2@example.com</EmailAddress>
              </Mailbox>
            </Attendee>
          </RequiredAttendees>
        </t:CalendarItem>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Ein Beispiel für die Reaktion auf eine Besprechungsanfrage finden Sie im Thema zum [CreateItem-Vorgang (Besprechungsanfrage).](createitem-operation-meeting-request.md) 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [CreateItem](createitem.md)
    
- [SavedItemFolderId](saveditemfolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [CalendarItem](calendaritem.md)
    
- [Betreff](subject.md)
    
- [Body](body.md)
    
- [ReminderIsSet](reminderisset.md)
    
- [ReminderMinutesBeforeStart](reminderminutesbeforestart.md)
    
- [Start](start.md)
    
- [Ende ](end-ex15websvcsotherref.md)
    
- [IsAllDayEvent](isalldayevent.md)
    
- [LegacyFreeBusyStatus](legacyfreebusystatus.md)
    
- [Ort](location.md)
    
- [RequiredAttendees](requiredattendees.md)
    
- [Teilnehmer](attendee.md)
    
- [Postfach](mailbox.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
## <a name="successful-createitem-calendar-item-response"></a>Erfolgreiche CreateItem-Antwort (Kalenderelement)

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateItem-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAAlAFV" ChangeKey="DwAAABYA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Die Attribute [ItemId-Element-ID](itemid.md) und  **ChangeKey** wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateItemResponse](createitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateItemResponseMessage](createitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Items](items.md)
    
- [CalendarItem](calendaritem.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>Siehe auch



[CreateItem-Vorgang](createitem-operation.md)

