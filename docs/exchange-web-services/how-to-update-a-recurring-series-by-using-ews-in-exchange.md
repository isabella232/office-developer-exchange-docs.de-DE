---
title: Aktualisieren einer Terminserie mithilfe der EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c922072f-ce33-4bff-97b0-1c1d0f9b880d
description: Hier erfahren Sie, wie eine gesamte Serie gleichzeitig zu aktualisieren, und verwenden die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 03f414845674bfcacca62ef96fdb84f8b8823920
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756998"
---
# <a name="update-a-recurring-series-by-using-ews-in-exchange"></a>Aktualisieren einer Terminserie mithilfe der EWS in Exchange

Hier erfahren Sie, wie eine gesamte Serie gleichzeitig zu aktualisieren, und verwenden die EWS Managed API oder EWS in Exchange.
  
Der EWS Managed API oder EWS können Sie eine Terminserie entweder aktualisieren Sie die gesamte Datenreihe oder durch [ein einzelnes Vorkommen aktualisieren](how-to-update-a-recurring-series-by-using-ews.md)aktualisieren. In diesem Artikel wird die gesamte Datenreihe gleichzeitig aktualisieren erläutert.
  
Im Allgemeinen ist das Aktualisieren einer Terminserie [Ändern eines Termins](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)sehr ähnlich. Sie verwenden die gleichen Methoden und Vorgänge, aber Sie verwenden die Element-ID der Datenreihe wiederkehrenden Master-Shape. In einigen Fällen können Sie nicht mit dem sich wiederholenden Master starten, und möglicherweise müssen Sie [finden die Element-ID für das wiederkehrende Master-Shape](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).
  
Es ist jedoch eine wesentliche Unterschiede beim Aktualisieren einer Terminserie berücksichtigt werden sollten: das Serienmuster aktualisieren. Aktualisieren das Serienmuster ist nur möglich, mit dem sich wiederholenden Master, und Änderungen an dem Muster hinzufügen oder Entfernen von vorkommen. Wenn Sie die [Recurrence.EndDate](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) -Eigenschaft zu einem Datum zu einem späteren Zeitpunkt als den aktuellen Wert ändern, beispielsweise das Serienmuster erneut ausgewertet wird, und möglicherweise zusätzliche Vorkommen hinzugefügt werden. 
  
## <a name="modify-all-occurrences-in-a-series-by-using-the-ews-managed-api"></a>Ändern Sie alle Vorkommen in einer Reihe, indem Sie die EWS Managed API

So ändern Sie alle Vorkommen in einer Reihe Sie:
  
1. Binden Sie an den sich wiederholenden Master für die Datenreihe mithilfe der [Appointment.BindToRecurringMaster](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) oder [Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) -Methode auf einen sich wiederholenden Master-Shape. 
    
2. Aktualisieren Sie die Eigenschaften für wiederkehrende master [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) -Objekts. 
    
3. Speichern Sie die Änderungen an den sich wiederholenden Master mithilfe der [Appointment.Save](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode. 
    
Im folgenden Beispiel wird eine Terminserie zum Ändern des Speicherorts aktualisiert Hinzufügen eines Teilnehmers, und ändern Sie das Serienmuster. In diesem Beispiel wird davon ausgegangen, dass das im _Dienst_ -Parameter übergebene [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt durch gültige Werte in die [Anmeldeinformationen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) und [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) -Eigenschaften initialisiert wurde. Der Parameter _Terminserie_ ist ein **Termin** -Objekt an das Auftreten eines Serientermins oder wiederkehrenden Master für die Datenreihe zu aktualisierenden gebunden. 
  
```cs
using Microsoft.Exchange.WebServices.Data;
public static bool UpdateRecurringSeries(ExchangeService service, Appointment recurringAppointment)
{
    Appointment recurringMaster = null;
    // If the item is a single appointment, fail.
    if (recurringAppointment.AppointmentType == AppointmentType.Single)
    {
        Console.WriteLine("ERROR: The item to delete is not part of a recurring series.");
        return false;
    }
    // Check the Appointment that was passed. Is it
    // an occurrence or the recurring master?
    if (recurringAppointment.AppointmentType != AppointmentType.RecurringMaster)
    {
        // If an occurrence was passed in, bind to the master.
        try
        {
            // This method results in a call to EWS.
            recurringMaster = Appointment.BindToRecurringMaster(service, recurringAppointment.Id);
        }
        catch (Exception ex)
        {
            Console.WriteLine("Couldn't bind to master: {0}", ex.Message);
            return false;
        }
    }
    else
    {
        // Bind to the appointment to load all properties.
        // This method results in a call to EWS.
        recurringMaster = Appointment.Bind(service, recurringAppointment.Id);
    }
    // Basic updates. These kinds of updates are the same
    // as if you were updating a single appointment.
    // Update the location. All occurrences will update to this new location.
    recurringMaster.Location = "Conference Room 2";
    // Add an attendee.
    Attendee newAttendee = new Attendee("sadie@contoso.com");
    recurringMaster.RequiredAttendees.Add(newAttendee);
    // Changes to the recurrence. This is only applicable to a recurring
    // master.
    // If the series has an end date, extend the series to add two more occurrences.
    if (recurringMaster.Recurrence.HasEnd)
    {
        // NumberOfOccurrences is only set if the user created the
        // appointment with a set number of occurrences.
        // Otherwise, there's a start and end date.
        if (recurringMaster.Recurrence.NumberOfOccurrences != null)
        {
            recurringMaster.Recurrence.NumberOfOccurrences += 2;
        }
        else
        {
            // This is a bit more complicated if you want to add two more
            // occurrences. You need to calculate a new end date.
            Type recurrenceType = recurringMaster.Recurrence.GetType();
            switch (recurrenceType.Name)
            {
                case "DailyPattern":
                    recurringMaster.Recurrence.EndDate =
                        recurringMaster.Recurrence.EndDate.Value.AddDays(2);
                    break;
                case "WeeklyPattern":
                    recurringMaster.Recurrence.EndDate =
                        recurringMaster.Recurrence.EndDate.Value.AddDays(14);
                    break;
                case "YearlyPattern":
                    recurringMaster.Recurrence.EndDate =
                        recurringMaster.Recurrence.EndDate.Value.AddYears(2);
                    break;
                default:
                    // Do nothing here. There are other recurrence
                    // types but for simplicity, these aren't covered.
                    break;
            }
        }
    }
    else
    {
        // If it has no end, set an end date to 2 weeks from today.
        recurringMaster.Recurrence.EndDate = DateTime.Now.AddDays(14);
    }
    // Update the series.
    try
    {
        // This method results in a call to EWS.
        recurringMaster.Update(ConflictResolutionMode.AutoResolve);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error updating series: {0}", ex.Message);
        return false;
    }
    return true;
}
```

## <a name="modify-all-occurrences-in-a-series-by-using-ews"></a>Ändern Sie alle Vorkommen in einer Reihe mithilfe der Exchange-Webdienste

Um alle Vorkommen in einer Reihe zu ändern, müssen Sie den [Vorgang UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) verwenden, mit der Element-ID des wiederkehrenden Master im [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Element in der Anforderung. Die Struktur der Anforderung ist identisch mit einer Anforderung an einen einzelnen Termin zu aktualisieren. 
  
Im folgenden Beispiel aktualisiert die Serie auf folgende Weise:
  
- Aktualisiert den Speicherort der Datenreihe durch Festlegen des [Speicherorts](http://msdn.microsoft.com/library/3fcf7133-ae1c-47b4-a187-660045f71df0%28Office.15%29.aspx) -Elements an. 
    
- Aktualisiert die Teilnehmer durch Festlegen des [RequiredAttendees](http://msdn.microsoft.com/library/422f8d44-b0eb-49ca-af0f-0e22b54c78d2%28Office.15%29.aspx) -Elements an. 
    
- Aktualisiert die Serie durch Festlegen des Elements [Serie (RecurrenceType)](http://msdn.microsoft.com/library/3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12%28Office.15%29.aspx) . 
    
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
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" SendMeetingInvitationsOrCancellations="SendToAllAndSaveCopy">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Location" />
              <t:CalendarItem>
                <t:Location>Conference Room 2</t:Location>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:RequiredAttendees" />
              <t:CalendarItem>
                <t:RequiredAttendees>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Mack Chaves</t:Name>
                      <t:EmailAddress>mack@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Sadie Daniels</t:Name>
                      <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                </t:RequiredAttendees>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Recurrence" />
              <t:CalendarItem>
                <t:Recurrence>
                  <t:WeeklyRecurrence>
                    <t:Interval>1</t:Interval>
                    <t:DaysOfWeek>Tuesday</t:DaysOfWeek>
                  </t:WeeklyRecurrence>
                  <t:EndDateRecurrence>
                    <t:StartDate>2014-05-06</t:StartDate>
                    <t:EndDate>2014-06-22-04:00</t:EndDate>
                  </t:EndDateRecurrence>
                </t:Recurrence>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:MeetingTimeZone" />
              <t:CalendarItem>
                <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet mit einem [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) -Element, das ein [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element mit dem Wert **NoError**, gibt an, dass die Aktualisierung erfolgreich war.
  
## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Serienmuster und EWS](recurrence-patterns-and-ews.md)
    
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Aktualisieren einer Terminserie mithilfe der Exchange-Webdienste](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Zugriff auf eine Terminserie mithilfe von EWS in Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    

