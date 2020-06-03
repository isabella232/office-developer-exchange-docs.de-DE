---
title: Löschen von Terminen in einer Terminserie mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a9d5244a-bc4a-4e9c-9c6c-ff361e04cbf8
description: In diesem Artikel erfahren Sie, wie Sie Termine in einer Terminserie mithilfe der verwaltete EWS-API oder EWS in Exchange löschen.
ms.openlocfilehash: 5646a30d218ed4d795044aefe5efea1399d19a79
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528125"
---
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a>Löschen von Terminen in einer Terminserie mithilfe von EWS in Exchange

In diesem Artikel erfahren Sie, wie Sie Termine in einer Terminserie mithilfe der verwaltete EWS-API oder EWS in Exchange löschen.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um eine Reihe von Terminen oder Besprechungen oder nur eine Instanz in der Datenreihe zu löschen. Der Vorgang, den Sie zum Löschen einer ganzen Datenreihe verwenden, ist im Wesentlichen identisch mit dem Vorgang, den Sie zum Löschen eines einzelnen Exemplars verwenden. Sie verwenden dieselben verwaltete EWS-API Methoden oder EWS-Vorgänge, die Sie zum [Löschen eines Termins oder einer Besprechung einer einzelnen Instanz](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)verwenden. Der Unterschied besteht in der Element-ID, die in der Methode oder dem Vorgang enthalten ist. Zunächst sehen wir uns an, wie beide Szenarien identisch sind. 
  
Wenn Sie eine wiederkehrende Datenreihe oder ein einzelnes Vorkommen in einer Terminserie löschen möchten, müssen Sie das zu löschende vorkommen oder die zu löschende Datenreihe suchen und dann die entsprechende Methode oder den entsprechenden Vorgang aufrufen, um Sie zu entfernen. Sie können zwar einfach jede Art von Termin löschen, es wird jedoch empfohlen, dass Sie alle Teilnehmer oder Organisatoren auf dem neuesten Stand halten und Besprechungen kündigen, die der Benutzer organisiert hat, und Besprechungen ablehnen, die der Benutzer nicht organisiert hat.
  
Wie unterscheiden sich die Szenarien? Es geht um das [Termin](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) Objekt, mit dem die Methode (für das verwaltete EWS-API) oder die in der Vorgangsanforderung enthaltene Element-ID (für EWS) aufgerufen wird. Zum Löschen einer ganzen Datenreihe benötigen Sie das **Termin** Objekt oder die Element-ID für den wiederkehrenden Master. Zum Löschen eines einzelnen Exemplars benötigen Sie das **Termin** Objekt oder die Element-ID für das vorkommen. 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a>Löschen einer Terminserie mithilfe der verwaltete EWS-API

In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. Der _recurringItem_ -Parameter ist ein **Termin** Objekt für den wiederkehrenden Master oder ein einzelnes vorkommen. Der Parameter _deleteEntireSeries_ gibt an, ob die gesamte Datenreihe gelöscht werden soll, in der das _recurringItem_ -Element enthalten ist. 
  
```cs
public static bool DeleteRecurringItem(ExchangeService service, Appointment recurringItem, bool deleteEntireSeries)
{
    Appointment appointmentToDelete = null;
    // If the item is a single appointment, fail.
    if (recurringItem.AppointmentType == AppointmentType.Single)
    {
        Console.WriteLine("ERROR: The item to delete is not part of a recurring series.");
        return false;
    }
    // Check the Appointment that was passed. Is it
    // an occurrence or the recurring master?
    if (recurringItem.AppointmentType == AppointmentType.RecurringMaster)
    {
        if (!deleteEntireSeries)
        {
            // The item is the recurring master, so deleting it will delete
            // the entire series. The caller indicated that the entire series
            // should not be deleted, so fail.
            Console.WriteLine("ERROR: The item to delete is the recurring master of the series. Deleting it will delete the entire series.");
            return false;
        }
        else
        {
            appointmentToDelete = recurringItem;
        }
    }
    else
    {
        if (deleteEntireSeries)
        {
            // The item passed is not the recurring master, but the caller
            // wants to delete the entire series. Bind to the recurring
            // master to delete it.
            try
            {
                appointmentToDelete = Appointment.BindToRecurringMaster(service, recurringItem.Id);
            }
            catch (Exception ex)
            {
                Console.WriteLine("ERROR: {0}", ex.Message);
                return false;
            }
        }
        else
        {
            // The item passed is not the recurring master, but the caller
            // only wants to delete the occurrence, so just
            // delete the passed item.
            appointmentToDelete = recurringItem;
        }
    }
    if (appointmentToDelete != null)
    {
        // Remove the item, depending on the scenario. 
        if (appointmentToDelete.IsMeeting)
        {
            CalendarActionResults results;
            // If it's a meeting and the user is the organizer, cancel it.
            // Determine this by testing the AppointmentState bitmask for 
            // the presence of the second bit. This bit indicates that the appointment
            // was received, which means that someone sent it to the user. Therefore,
            // they're not the organizer.
            int isReceived = 2;
            if ((appointmentToDelete.AppointmentState &amp; isReceived) == 0)
            {
                results = appointmentToDelete.CancelMeeting("Cancelling this meeting.");
                return true;
            }
            // If it's a meeting and the user is not the organizer, decline it.
            else
            {
                results = appointmentToDelete.Decline(true);
                return true;
            }
        }
        else
        {
            // The item isn't a meeting, so just delete it.
            appointmentToDelete.Delete(DeleteMode.MoveToDeletedItems);
            return true;
        }
    }
    return false;
}
```

Um dieses Beispiel verwenden zu können, müssen Sie an [ein vorkommen oder den wiederkehrenden Master binden](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)und das resultierende **Termin** Objekt an die Methode übergeben. Beachten Sie, dass beim Zugriff auf Termine mithilfe einer [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) -Klasse die resultierenden Elemente alle einzelnen Vorkommen sind. Wenn Sie die [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) -Klasse verwenden, sind die resultierenden Elemente umgekehrt alle wiederkehrenden Master. 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a>Löschen einer Terminserie mithilfe von EWS

Das Löschen einer Terminserie mithilfe von EWS entspricht dem [Löschen einer Besprechung mit einer Einzelinstanz](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md). Tatsächlich nehmen die SOAP-Anforderungen dasselbe Format an. Der Schlüssel ist wiederum die Element-ID, die in der Anforderung verwendet wird. Wenn die Element-ID dem wiederkehrenden Master entspricht, wird die gesamte Datenreihe gelöscht. Wenn die Element-ID einem einzelnen Vorkommen entspricht, wird nur dieses vorkommen gelöscht.
  
> [!NOTE]
> In den folgenden Codebeispielen werden die Attribute **ItemID**, **ChangeKey**und **RecurringMasterId** zur Lesbarkeit gekürzt. 
  
In diesem Beispiel wird der [CreateItem-Vorgang](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) mit einem [CancelCalendarItem](https://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) -Element verwendet, um eine Besprechung abzubrechen, für die der Benutzer der Organisator ist. Der Wert des [ReferenceItemId](https://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) -Elements gibt das Element an, das abgebrochen werden soll, und kann die Element-ID eines wiederkehrenden Masters oder eines einzelnen Exemplars sein. 
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:CancelCalendarItem>
          <t:ReferenceItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:NewBodyContent BodyType="HTML">Cancelling this meeting.</t:NewBodyContent>
        </t:CancelCalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

In diesem Beispiel wird der **CreateItem-Vorgang** mit einem [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) -Element verwendet, um eine Besprechung abzulehnen, für die der Benutzer nicht der Organisator ist. Wie im vorherigen Beispiel gibt der Wert des **ReferenceItemId** -Elements das Element an, das abgelehnt werden soll, und kann die Element-ID eines wiederkehrenden Masters oder eines einzelnen Exemplars sein. 
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:DeclineItem>
          <t:ReferenceItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
        </t:DeclineItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

In diesem Beispiel wird der [DeleteItem-Vorgang](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) verwendet, um ein einzelnes Vorkommen eines Termins ohne Teilnehmer zu löschen. Das zu löschende vorkommen wird durch das [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) -Element angegeben, das aus der Element-ID des wiederkehrenden Master-Objekts und dem Index des Vorkommens erstellt wird. 
  
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
    <m:DeleteItem DeleteType="MoveToDeletedItems" SendMeetingCancellations="SendToAllAndSaveCopy">
      <m:ItemIds>
        <t:OccurrenceItemId RecurringMasterId="AAMkADA8..." InstanceIndex="3" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

Beachten Sie, dass Sie dasselbe Ergebnis erhalten können, indem Sie das **OccurrenceItemId** -Element durch ein [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Element ersetzen, das die Element-ID des Vorkommens enthält (siehe Abbildung). 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a>Siehe auch


- [Serienmuster und EWS](recurrence-patterns-and-ews.md)
    
- [Zugreifen auf eine Terminserie mithilfe von EWS in Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Erstellen einer Terminserie mithilfe von EWS in Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Aktualisieren einer Terminserie mithilfe von EWS](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Aktualisieren einer Terminserie mithilfe von EWS in Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Löschen von Terminen und Absagen von Besprechungen mithilfe von EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

