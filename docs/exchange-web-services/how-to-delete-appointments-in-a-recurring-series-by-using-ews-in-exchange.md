---
title: Löschen von Terminen in einer Terminserie mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a9d5244a-bc4a-4e9c-9c6c-ff361e04cbf8
description: Erfahren Sie, wie Sie Termine in einer Terminserie mithilfe der verwalteten EWS-API oder EWS in Exchange löschen.
ms.openlocfilehash: 8a68b6655c98f290d569a14dc0ac518c5d875cbe
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513192"
---
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a>Löschen von Terminen in einer Terminserie mithilfe von EWS in Exchange

Erfahren Sie, wie Sie Termine in einer Terminserie mithilfe der verwalteten EWS-API oder EWS in Exchange löschen.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um eine Reihe von Terminen oder Besprechungen oder nur eine Instanz der Reihe zu löschen. Der Prozess, den Sie zum Löschen einer ganzen Datenreihe verwenden, ist im Wesentlichen identisch mit dem Prozess, mit dem Sie nur ein einzelnes Vorkommen löschen. Sie verwenden die gleichen verwalteten EWS-API-Methoden oder EWS-Vorgänge, mit denen Sie [einen einzelnen Instanztermin oder eine Besprechung löschen.](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md) Der Unterschied liegt in der Element-ID, die in der Methode oder dem Vorgang enthalten ist. Betrachten wir zunächst, wie beide Szenarien identisch sind. 
  
Um eine Terminserie oder ein einzelnes Vorkommen in einer Terminserie zu löschen, müssen Sie das Oder die Datenreihe suchen, die Sie löschen möchten, und dann die entsprechende Methode oder den entsprechenden Vorgang aufrufen, um sie zu entfernen. Sie können zwar einfach jede Art von Termin löschen, es wird jedoch empfohlen, alle Teilnehmer oder den Organisator auf dem neuesten Stand zu halten und Besprechungen abzubrechen, die der Benutzer organisiert hat, und Besprechungen abzulehnen, die der Benutzer nicht organisiert hat.
  
Wie unterscheiden sich die Szenarien? Es geht um das [Appointment-Objekt,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) das zum Aufrufen der Methode (für die verwaltete EWS-API) oder der Element-ID verwendet wird, die in der Vorgangsanforderung (für EWS) enthalten ist. Um eine gesamte Datenreihe zu löschen, benötigen Sie das **Appointment-Objekt** oder die Element-ID für den Serienmaster. Um ein einzelnes Vorkommen zu löschen, benötigen Sie das **Appointment-Objekt** oder die Element-ID für das Vorkommen. 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a>Löschen einer Terminserie mithilfe der verwalteten EWS-API

In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. Der  _recurringItem-Parameter_ ist ein **Appointment-Objekt** für den Serienmaster oder ein einzelnes Vorkommen. Der  _parameter deleteEntireSeries_ gibt an, ob die gesamte Datenreihe gelöscht werden soll, zu der das  _recurringItem-Objekt_ gehört. 
  
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

Um dieses Beispiel verwenden zu können, müssen Sie [entweder eine Bindung an ein Vorkommen oder den Serienmaster](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)erstellen und das resultierende **Appointment-Objekt** an die Methode übergeben. Beachten Sie, dass beim Zugriff auf Termine mithilfe einer [CalendarView-Klasse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) die resultierenden Elemente alle einzelnen Vorkommen sind. Wenn Sie dagegen die [ItemView-Klasse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) verwenden, sind die resultierenden Elemente alle wiederkehrende Master. 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a>Löschen einer Terminserie mithilfe von EWS

Das Löschen einer Terminserie mithilfe von EWS entspricht dem Löschen einer Besprechung mit [einer einzelnen Instanz.](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md) Tatsächlich haben die SOAP-Anforderungen das gleiche Format. Auch hier ist der Schlüssel die Element-ID, die in der Anforderung verwendet wird. Wenn die Element-ID dem Serienmaster entspricht, wird die gesamte Datenreihe gelöscht. Wenn die Element-ID einem einzelnen Vorkommen entspricht, wird nur dieses Vorkommen gelöscht.
  
> [!NOTE]
> In den folgenden Codebeispielen werden die Attribute **ItemId,** **ChangeKey** und **RecurringMasterId** zur besseren Lesbarkeit gekürzt. 
  
In diesem Beispiel wird der [CreateItem-Vorgang](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) mit einem [CancelCalendarItem-Element](https://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) verwendet, um eine Besprechung abzubrechen, für die der Benutzer der Organisator ist. Der Wert des [ReferenceItemId-Elements](https://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) gibt das abzubrechende Element an und kann die Element-ID eines wiederkehrenden Master-Shapes oder eines einzelnen Vorkommens sein. 
  
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

In diesem Beispiel wird der **CreateItem-Vorgang** mit einem [DeclineItem-Element](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) verwendet, um eine Besprechung abzulehnen, für die der Benutzer nicht der Organisator ist. Wie im vorherigen Beispiel gibt der Wert des **ReferenceItemId-Elements** das zu ablehnende Element an und kann die Element-ID eines wiederkehrenden Master-Shapes oder eines einzelnen Vorkommens sein. 
  
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

In diesem Beispiel wird der [DeleteItem-Vorgang](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) verwendet, um ein einzelnes Vorkommen eines Termins ohne Teilnehmer zu löschen. Das zu löschende Vorkommen wird durch das [OccurrenceItemId-Element](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) angegeben, das aus der Element-ID des Serienmasters und dem Index des Vorkommens erstellt wird. 
  
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

Beachten Sie, dass Sie dasselbe Ergebnis erzielen können, indem Sie das **OccurrenceItemId-Element** durch ein [ItemId-Element](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) ersetzen, das die Element-ID des Vorkommens enthält( siehe Abbildung). 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a>Siehe auch


- [Serienmuster und EWS](recurrence-patterns-and-ews.md)
    
- [Zugreifen auf eine Terminserie mithilfe von EWS in Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Erstellen einer Serienserie mithilfe von EWS in Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Aktualisieren einer Serienserie mithilfe von EWS](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Aktualisieren einer Serienserie mithilfe von EWS in Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Mithilfe von EWS in Exchange Termine löschen und Besprechungen absagen](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

