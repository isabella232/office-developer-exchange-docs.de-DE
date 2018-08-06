---
title: Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fdea70a4-9267-4e5d-9152-b749e2acc3b0
description: Erfahren Sie, wie Sie mit der verwalteten EWS-API und EWS in Exchange Termine und Besprechungen erstellen.
ms.openlocfilehash: 1c840fac2ecca9fb51a28044dfac6299cb4fc038
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756882"
---
# <a name="create-appointments-and-meetings-by-using-ews-in-exchange-2013"></a>Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013

Erfahren Sie, wie Sie mit der verwalteten EWS-API und EWS in Exchange Termine und Besprechungen erstellen.
  
Der wesentliche Unterschied zwischen Besprechungen und Terminen ist, dass Besprechungen Teilnehmer haben und Termine nicht. Termine und Besprechungen können einzelne Instanzen oder Teil einer Reihe sein. Da Termine keine Teilnehmer, Räume oder Ressourcen enthalten, muss keine Nachricht gesendet werden. Intern verwendet Exchange das gleiche Objekt für Besprechungen und Termine. Verwenden Sie die [Appointment-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) in der EWS Managed API oder das Element [CalendarItem](http://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx) in EWS zum Arbeiten mit Besprechungen und Termine. 
  
**Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für das Arbeiten mit Terminen und Besprechungen**

|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|
|[Appointment.Save](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) <br/> |[CreateItem-Vorgang (Kalenderelement)](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) <br/> |
|[Item.Bind](http://msdn.microsoft.com/de-DE/library/dd634410%28v=exchg.80%29.aspx) <br/> |[GetItem-Vorgang (Kalenderelement)](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
   
## <a name="create-an-appointment-by-using-the-ews-managed-api"></a>Erstellen eines Termins mithilfe der EWS Managed API
<a name="bk_CreateApptEWSMA"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie mit dem [Appointment-Objekt](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) ein Termin erstellt werden kann, der mit der [Save](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)-Methode in Ihrem Kalenderordner gespeichert wird. Anschließend wird mit der Methode [Item.Bind](http://msdn.microsoft.com/de-DE/library/dd634410%28v=exchg.80%29.aspx) geprüft, ob der Termin auch wirklich erstellt wurde. 
  
In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. 
  
```cs
Appointment appointment = new Appointment(service);
// Set the properties on the appointment object to create the appointment.
appointment.Subject = "Tennis lesson";
appointment.Body = "Focus on backhand this week.";
appointment.Start = DateTime.Now.AddDays(2);
appointment.End = appointment.Start.AddHours(1);
appointment.Location = "Tennis club";
appointment.ReminderDueBy = DateTime.Now;
// Save the appointment to your calendar.
appointment.Save(SendInvitationsMode.SendToNone);
// Verify that the appointment was created by using the appointment's item ID.
Item item = Item.Bind(service, appointment.Id, new PropertySet(ItemSchema.Subject));
Console.WriteLine("\nAppointment created: " + item.Subject + "\n");

```

Nach dem Festlegen der Eigenschaften für das Appointment-Objekt, können Sie den Termin mit der [Save](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)-Methode des Appointment-Objekts im Kalenderordner speichern. 
  
Bei der Prüfung verwenden Sie die [Id](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des Elements, das mit dem Termin verknüpft ist. Dadurch stellen Sie sicher, dass der Termin im Kalenderordner abgelegt wurde. Wir empfehlen Ihnen, die vom Server zurückgegebenen Eigenschaften auf die Daten einzuschränken, die Sie auch wirklich benötigen - in diesem Fall der Betreff des Termins. 
  
## <a name="create-an-appointment-by-using-ews"></a>Erstellen eines Termins mithilfe von EWS
<a name="bk_CreateApptEWS"> </a>

Der Anforderungs- und Antwort-XML-Code im folgenden Beispiel entspricht den Aufrufen über den Code für die EWS Managed API unter [Erstellen eines Termins mithilfe der EWS Managed API](#bk_CreateApptEWSMA). Außerdem wird der Anforderungs- und Antwort-XML-Code gezeigt, mit dem geprüft werden kann, ob sich Terminelemente im Kalenderordner befinden.
  
Das folgende Beispiel zeigt den Anforderungs-XML-Code, wenn Sie den [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)-Vorgang zum Erstellen eines Termins verwenden. 
  
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
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Tennis lesson</t:Subject>
          <t:Body BodyType="HTML">Focus on backhand this week.</t:Body>
          <t:ReminderDueBy>2013-09-19T14:37:10.732-07:00</t:ReminderDueBy>
          <t:Start>2013-09-21T19:00:00.000Z</t:Start>
          <t:End>2013-09-21T20:00:00.000Z</t:End>
          <t:Location>Tennis club</t:Location>
          <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

 Das folgende Beispiel zeigt den Antwort-XML-Code, der vom **CreateItem**-Vorgang zurückgegeben wird. 
  
> [!NOTE]
> Die Attribute **ItemId** und **ChangeKey** wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>

```

Das folgende Beispiel zeigt den Anforderungs-XML-Code, der generiert wird, wenn Sie die Erstellung des Termins mithilfe des [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)-Vorgangs überprüfen. 
  
> [!NOTE]
> Die Attribute **ItemId** und **ChangeKey** wurden zur besseren Lesbarkeit gekürzt. 
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>

```

 Das folgende Beispiel zeigt den Antwort-XML-Code, der vom **GetItem**-Vorgang zurückgegeben wird. 
  
> [!NOTE]
> Die Attribute **ItemId** und **ChangeKey** wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
              <t:Subject>Tennis lesson</t:Subject>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="create-a-meeting-by-using-the-ews-managed-api"></a>Erstellen Sie eine Besprechung mithilfe der EWS Managed API
<a name="bk_CreateMtgEWSMA"> </a>

Beim Erstellen einer Besprechung ist es neben dem Speichern eines Elements im Kalenderordner üblich, dass Sie Besprechungsanfragen an die Teilnehmer senden möchten. Im folgenden Codebeispiel wird veranschaulicht, wie Sie eine Besprechung erstellen und Besprechungsanfragen senden können.
  
In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. 
  
```cs
Appointment meeting = new Appointment(service);
// Set the properties on the meeting object to create the meeting.
meeting.Subject = "Team building exercise";
meeting.Body = "Let's learn to really work as a team and then have lunch!";
meeting.Start = DateTime.Now.AddDays(2);            
meeting.End = meeting.Start.AddHours(4);
meeting.Location = "Conference Room 12";
meeting.RequiredAttendees.Add("Mack@contoso.com");
meeting.RequiredAttendees.Add("Sadie@contoso.com");
meeting.OptionalAttendees.Add("Magdalena@contoso.com");
meeting.ReminderMinutesBeforeStart = 60;
// Save the meeting to the Calendar folder and send the meeting request.
meeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);
// Verify that the meeting was created.
Item item = Item.Bind(service, meeting.Id, new PropertySet(ItemSchema.Subject));
Console.WriteLine("\nMeeting created: " + item.Subject + "\n");

```

Speichern Sie die Besprechung nach dem Festlegen der Eigenschaften für das [Appointment](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)-Objekt mithilfe der [Save](http://msdn.microsoft.com/de-DE/library/dd635394%28v=exchg.80%29.aspx)-Methode in Ihrem Kalenderordner. Wenn Sie den Aufzählungswert [SendInvitationsMode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.sendinvitationsmode%28v=exchg.80%29.aspx) auf **SendOnlyToAll** oder **SendToAllAndSaveCopy** einstellen, werden Einladungen an Teilnehmer gesendet.
  
Verwenden Sie das Element [Id](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx), das mit der Besprechung verknüpft ist, um zu überprüfen, ob die Besprechung im Kalenderordner gespeichert wurde. Wir empfehlen Ihnen, die vom Server zurückgegebenen Eigenschaften auf die Daten einzuschränken, die Sie auch wirklich benötigen - in diesem Fall der Betreff der Besprechung. 
  
## <a name="create-a-meeting-by-using-ews"></a>Erstellen einer Besprechung mithilfe von EWS
<a name="bk_CreateMtgEWS"> </a>

Der Anforderungs- und Antwort-XML-Code im folgenden Beispiel entspricht den Aufrufen über den Code für die EWS Managed API unter [Erstellen Sie eine Besprechung mithilfe der EWS Managed API](#bk_CreateMtgEWSMA). Außerdem wird der Anforderungs- und Antwort-XML-Code gezeigt, mit dem geprüft werden kann, ob sich Besprechungselemente im Kalenderordner befinden.
  
Das folgende Beispiel zeigt den Anforderungs-XML-Code beim Erstellen einer Besprechung mithilfe des [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)-Vorgangs. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Team building exercise</t:Subject>
          <t:Body BodyType="HTML">Let's learn to really work as a team and then have lunch!</t:Body>
          <t:ReminderMinutesBeforeStart>60</t:ReminderMinutesBeforeStart>
          <t:Start>2013-09-21T16:00:00.000Z</t:Start>
          <t:End>2013-09-21T20:00:00.000Z</t:End>
          <t:Location>Conference Room 12</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Sadie.Daniels@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
          <t:OptionalAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Magdalena.Kemp@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:OptionalAttendees>
          <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt den Antwort-XML-Code, der vom **CreateItem**-Vorgang zurückgegeben wird. 
  
> [!NOTE]
> Die Attribute **ItemId** und **ChangeKey** wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

Das folgende Beispiel zeigt den Anforderungs-XML-Code, der generiert wird, wenn Sie mit dem [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)-Vorgang prüfen, ob eine Besprechung auch wirklich erstellt wurde. 
  
> [!NOTE]
> Die Attribute **ItemId** und **ChangeKey** wurden zur besseren Lesbarkeit gekürzt. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt den Antwort-XML-Code, der vom **GetItem**-Vorgang zurückgegeben wird. 
  
> [!NOTE]
> Die Attribute **ItemId** und **ChangeKey** wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
              <t:Subject>Team building exercise</t:Subject>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Siehe auch

- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)  
- [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md) 
- [Löschen von Terminen und Absagen von Besprechungen mithilfe von EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md) 
- [Vorschlagen einer neuen Besprechungszeit mithilfe von EWS in Exchange](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

