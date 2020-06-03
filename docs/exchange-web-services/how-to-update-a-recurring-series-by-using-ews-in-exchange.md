---
title: Aktualisieren einer Terminserie mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c922072f-ce33-4bff-97b0-1c1d0f9b880d
description: Hier erfahren Sie, wie Sie eine ganze Serie von Serien auf einmal mithilfe der verwaltete EWS-API oder EWS in Exchange aktualisieren.
ms.openlocfilehash: 253bc7da176a954480db97e303393fecdda54892
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527614"
---
# <a name="update-a-recurring-series-by-using-ews-in-exchange"></a>Aktualisieren einer Terminserie mithilfe von EWS in Exchange

Hier erfahren Sie, wie Sie eine ganze Serie von Serien auf einmal mithilfe der verwaltete EWS-API oder EWS in Exchange aktualisieren.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um eine wiederkehrende Datenreihe zu aktualisieren, indem Sie entweder die gesamte Datenreihe aktualisieren oder [ein einzelnes Vorkommen aktualisieren](how-to-update-a-recurring-series-by-using-ews.md). In diesem Artikel wird erläutert, wie Sie die gesamte Datenreihe gleichzeitig aktualisieren.
  
Im Allgemeinen ähnelt das Aktualisieren einer Terminserie sehr dem [Ändern eines einzelnen Termins](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md). Sie verwenden dieselben Methoden und Vorgänge, verwenden jedoch die Element-ID des wiederkehrenden Masters der Serie. In einigen Fällen beginnen Sie möglicherweise nicht mit dem wiederkehrenden Master, und Sie müssen möglicherweise [die Element-ID für den wiederkehrenden Master suchen](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).
  
Es gibt jedoch einen wichtigen Unterschied, der beim Aktualisieren einer Terminserie beachtet werden muss: Aktualisieren des Serienmusters. Das Aktualisieren des Serienmusters ist nur mit dem wiederkehrenden Master möglich, und durch Änderungen am Muster können Vorkommnisse hinzugefügt oder entfernt werden. Wenn Sie beispielsweise die [Serie. EndDate](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) -Eigenschaft auf ein Datum später als den aktuellen Wert ändern, wird das Serienmuster neu ausgewertet, und es können zusätzliche Vorkommen hinzugefügt werden. 
  
## <a name="modify-all-occurrences-in-a-series-by-using-the-ews-managed-api"></a>Ändern aller Vorkommen in einer Datenreihe mithilfe der verwaltete EWS-API

So ändern Sie alle Vorkommen in einer Reihe:
  
1. Binden Sie mit der [Termin-BindToRecurringMaster](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) -oder der [Termin Bindungs](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) Methode für einen wiederkehrenden Master an den wiederkehrenden Master für die Datenreihe. 
    
2. Aktualisieren der Eigenschaften für das Terminserien-Master [Termin](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) Objekt. 
    
3. Speichern Sie die Änderungen am wiederkehrenden Master mithilfe der [Termin. Save](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode. 
    
Im folgenden Beispiel wird eine Terminserie aktualisiert, um den Speicherort zu ändern, einen Teilnehmer hinzuzufügen und das Serienmuster zu ändern. In diesem Beispiel wird davon ausgegangen, dass das [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, das im Parameter _Service_ übergeben wurde, mit gültigen Werten in den Eigenschaften [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) und [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) initialisiert wurde. Der _Terminserie_ -Parameter ist ein **Termin** Objekt, das entweder an ein vorkommen oder an den wiederkehrenden Master gebunden ist, damit die Datenreihe aktualisiert wird. 
  
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

## <a name="modify-all-occurrences-in-a-series-by-using-ews"></a>Ändern aller Vorkommen in einer Datenreihe mithilfe von EWS

Um alle Vorkommen in einer Datenreihe zu ändern, müssen Sie den [UpdateItem-Vorgang](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) mit der Element-ID des wiederkehrenden Masters im [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Element in der Anforderung verwenden. Die Struktur der Anforderung ist identisch mit einer Anforderung zum Aktualisieren eines einzelnen Termins. 
  
Im folgenden Beispiel wird die wiederkehrende Datenreihe folgendermaßen aktualisiert:
  
- Aktualisiert die Position der Datenreihe durch Festlegen des [Location](https://msdn.microsoft.com/library/3fcf7133-ae1c-47b4-a187-660045f71df0%28Office.15%29.aspx) -Elements. 
    
- Aktualisiert die Teilnehmer durch Festlegen des [RequiredAttendees](https://msdn.microsoft.com/library/422f8d44-b0eb-49ca-af0f-0e22b54c78d2%28Office.15%29.aspx) -Elements. 
    
- Aktualisiert die Serie durch Festlegen des Serienelements [(Serienelement)](https://msdn.microsoft.com/library/3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12%28Office.15%29.aspx) . 
    
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

Der Server antwortet mit einem [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) -Element, das ein [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element mit dem Wert **noError**enthält, das angibt, dass das Update erfolgreich war.
  
## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Serienmuster und EWS](recurrence-patterns-and-ews.md)
    
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Aktualisieren einer Terminserie mithilfe von EWS](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Zugreifen auf eine Terminserie mithilfe von EWS in Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    

