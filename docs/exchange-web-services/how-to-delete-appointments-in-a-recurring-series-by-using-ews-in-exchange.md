---
title: Löschen der Termine in einer Terminserie mithilfe der EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a9d5244a-bc4a-4e9c-9c6c-ff361e04cbf8
description: Erfahren Sie, wie Termine in einer Terminserie löschen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 5e4d95058808adf8db159000bdf90c1f92945338
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756902"
---
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a>Löschen der Termine in einer Terminserie mithilfe der EWS in Exchange

Erfahren Sie, wie Termine in einer Terminserie löschen, indem Sie die EWS Managed API oder EWS in Exchange.
  
Der EWS Managed API oder EWS können Sie eine Reihe von Terminen oder Besprechungen oder nur eine Instanz in der Datenreihe löschen. Der Prozess, mit denen Sie eine gesamte Datenreihe gelöscht ist im Wesentlichen identisch mit den Prozess, mit denen Sie nur ein einzelnes Element löschen. Sie verwenden die gleichen EWS Managed API-Methoden oder EWS-Vorgänge, die Sie, um [eine einzelne Instanz Termin oder eine Besprechung zu löschen verwenden](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md). Der Unterschied liegt in der Element-ID, die in der Methode oder der Vorgang enthalten ist. Zunächst betrachten, wie beide Szenarien identisch sind. 
  
Um eine Terminserie oder ein einzelnes Element in einer Terminserie löschen möchten, müssen Sie hier finden das Vorkommen oder die Serie, die Sie löschen möchten, und rufen Sie dann die entsprechende Methode oder der Vorgang zu entfernen. Während Sie einfach eine Art von Termin löschen können, wird empfohlen, alle Teilnehmer oder der Organisator auf dem aktuellen Stand halten und Besprechungen, die der Benutzer organisiert hat abzubrechen und Ablehnen von Besprechungen, die der Benutzer nicht organisiert.
  
So unterscheiden sich wie die Szenarien? Es ist alles über [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) -Objekts verwendet, um die-Methode (für die EWS Managed API) oder die Element-ID aufzurufen in die Operation Anforderung (EWS) enthalten. Um eine gesamte Datenreihe zu löschen, benötigen Sie die **Appointment** -Objekt oder Element-ID für das wiederkehrende Master-Shape. Um ein einzelnes Vorkommen löschen möchten, benötigen Sie die **Appointment** -Objekt oder Element-ID für das Vorkommen. 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a>Löschen einer Terminserie mithilfe der EWS Managed API

In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. Der Parameter _RecurringItem_ ist ein **Termin** -Objekt für das wiederkehrende Master-Shape oder ein einzelnes Vorkommen. Der Parameter _DeleteEntireSeries_ gibt an, ob die gesamte Datenreihe gelöscht, denen die _RecurringItem_ gehört. 
  
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

Um dieses Beispiel zu verwenden, um eine [Bindung an das Auftreten eines Serientermins oder wiederkehrenden Master](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)müssen und resultierenden **Appointment** -Objekts an die-Methode übergeben. Beachten Sie, dass wenn Sie Termine mithilfe einer [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) -Klasse zugreifen, die resultierenden Elemente alle einzelnen Vorkommen werden beibehalten. Wenn Sie die [aufrufenArtikel aufrufen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) -Klasse verwenden, sind die resultierenden Elemente dagegen alle wiederkehrenden Master-Shapes. 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a>Löschen einer Terminserie mithilfe der Exchange-Webdienste

Löschen einer Terminserie mit dem Exchange-Webdienste ist gleichbedeutend mit dem [Löschen einer Besprechung Einzel-Instanz](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md). Die SOAP-Anforderungen können Sie sogar das gleiche Format in Anspruch nehmen. In diesem Fall ist der Schlüssel die Element-ID in der Anforderung verwendet. Wenn das wiederkehrende Master-Shape die Element-ID entspricht, wird die gesamte Datenreihe gelöscht. Wenn ein einzelnes Vorkommen die Element-ID entspricht, wird nur dieses auftreten gelöscht werden.
  
> [!NOTE]
> In den folgenden Codebeispielen, werden die Attribute **ItemId**, **ChangeKey**und **RecurringMasterId** zur besseren Lesbarkeit gekürzt. 
  
In diesem Beispiel wird die [CreateItem-Vorgang](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) mit einem [CancelCalendarItem](http://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) -Element eine Besprechung absagen, bei der der Benutzer der Organisator ist. Der Wert des [ReferenceItemId](http://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) -Elements gibt an, das Element um abzubrechen, und die Element-ID ein wiederkehrendes Master-Shape oder ein einzelnes Vorkommen werden kann. 
  
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

In diesem Beispiel wird die **CreateItem-Vorgang** mit einem Element [DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) ablehnen eine Besprechung, für die der Benutzer nicht der Organisator ist. Wie im vorherigen Beispiel wird der Wert des **ReferenceItemId** -Elements gibt das Element an ablehnen möchten, und die Element-ID ein wiederkehrendes Master-Shape oder ein einzelnes Vorkommen werden kann. 
  
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

In diesem Beispiel wird mit der [DeleteItem Vorgang](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) ein einzelnes Vorkommen eines Termins ohne Teilnehmer gelöscht. Das Vorkommen löschen wird durch das [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) -Element angegeben, der aus der Element-ID des wiederkehrenden Master-Shapes und der Index des Vorkommens erstellt wird. 
  
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
    <m:DeleteItem DeleteType="MoveToDeletedItems" SendMeetingCancellations="SendToAllAndSaveCopy">
      <m:ItemIds>
        <t:OccurrenceItemId RecurringMasterId="AAMkADA8..." InstanceIndex="3" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

Beachten Sie, dass Sie dasselbe Ergebnis abrufen können, indem das **OccurrenceItemId** -Element durch ein [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Element, das die Element-ID das Vorkommen enthält (siehe) ersetzt. 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a>Siehe auch


- [Serienmuster und EWS](recurrence-patterns-and-ews.md)
    
- [Zugriff auf eine Terminserie mithilfe von EWS in Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Erstellen einer Terminserie mithilfe der EWS in Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Aktualisieren einer Terminserie mithilfe der Exchange-Webdienste](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Aktualisieren einer Terminserie mithilfe der EWS in Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Löschen von Terminen und Abbrechen an Besprechungen mithilfe von EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

