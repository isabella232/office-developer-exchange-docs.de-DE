---
title: Aktualisieren einer Serienserie mithilfe von EWS
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7e61bee9-4840-4773-a0a7-47b11e1fdf59
description: Erfahren Sie, wie Sie Termine in einer Terminserie mithilfe der verwalteten EWS-API oder EWS in Exchange ändern.
ms.openlocfilehash: 3b9260bf271581a9a47fcad36d35f48e9845eb91
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521077"
---
# <a name="update-a-recurring-series-by-using-ews"></a>Aktualisieren einer Serienserie mithilfe von EWS

Erfahren Sie, wie Sie Termine in einer Terminserie mithilfe der verwalteten EWS-API oder EWS in Exchange ändern.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um eine Terminserie zu aktualisieren, indem Sie entweder [die gesamte Datenreihe](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)oder ein einzelnes Vorkommen aktualisieren. In diesem Artikel wird erläutert, wie ein einzelnes Vorkommen aktualisiert wird.
  
Das Ändern eines einzelnen Termins in einer Reihe ähnelt dem [Ändern eines Termins einer einzelnen Instanz.](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md) Sie verwenden die gleichen Methoden und Vorgänge, aber Sie verwenden die Element-ID des Vorkommens, das Sie ändern möchten.
  
Wenn Sie ein einzelnes Vorkommen in einer Datenreihe ändern, wird dieses Vorkommen einem Array geänderter Termine hinzugefügt, die dem Serienmaster für die Datenreihe zugeordnet sind. Sie können die verwaltete EWS-API-Eigenschaft [Appointment.ModifiedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) oder das [ModifiedOccurrences](https://msdn.microsoft.com/library/552932fc-b3b4-486e-8d73-32c0bb10bd68%28Office.15%29.aspx) EWS-Element verwenden, um auf alle Termine in einer Geänderten Datenreihe zuzugreifen. 
  
## <a name="modify-a-single-occurrence-in-a-series-by-using-the-ews-managed-api"></a>Ändern eines einzelnen Vorkommens in einer Datenreihe mithilfe der verwalteten EWS-API

Um eine einzelne Instanz in einer Datenreihe zu ändern, gehen Sie wiederherstellungshalber vor:
  
1. Binden Sie eine Bindung an das Vorkommen, das Sie ändern möchten, indem Sie entweder die [Appointment.BindToOccurrence-Methode](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) mit dem Indexwert des Elements oder die [Appointment.Bind-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) mit der ID des Vorkommens verwenden. Sie erhalten diese ID entweder aus der [ID-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) eines [Appointment-Objekts,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) das dem Vorkommen entspricht, oder aus der [ItemId-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.occurrenceinfo.itemid%28v=exchg.80%29.aspx) des [OccurrenceInfo-Objekts,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.occurrenceinfo%28v=exchg.80%29.aspx) das dem Vorkommen entspricht. 
    
2. Dient zum Aktualisieren der Eigenschaften für das Appointment-Objekt des Vorkommens.
    
3. Speichern Sie die Änderungen am Terminobjekt des Vorkommens mithilfe der [Appointment.Save-Methode.](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) 
    
Im folgenden Beispiel wird ein Termin in einer Terminserie aktualisiert und überprüft, ob der geänderte Termin für den Serienmaster aktualisiert wird. In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. Der  `recurrenceMasterId` Parameter ist ein Bezeichner, der dem Serienmaster zugeordnet ist, damit das Vorkommen geändert werden kann. 
  
```cs
public static ItemId ModifyARecurringSeries(ExchangeService service, ItemId recurrenceMasterId)
{
    Appointment calendarItem = Appointment.Bind(service, recurrenceMasterId, new PropertySet(AppointmentSchema.AppointmentType));
    Appointment recurrMaster = new Appointment(service);
    if (calendarItem.AppointmentType == AppointmentType.RecurringMaster)
    {
        // Get the recurring master from an occurrence in a recurring series with the properties you need.
        recurrMaster = Appointment.Bind(service,
                                        recurrenceMasterId,
                                        new PropertySet(AppointmentSchema.AppointmentType,
                                                        AppointmentSchema.Subject,
                                                        AppointmentSchema.FirstOccurrence,
                                                        AppointmentSchema.LastOccurrence,
                                                        AppointmentSchema.ModifiedOccurrences,
                                                        AppointmentSchema.DeletedOccurrences));
    }
    else
    {
        Console.WriteLine("Item id was not for a recurring master.");
        return recurrenceMasterId;
    }
    // Bind to the second occurrence in the series with the properties to modify.
    Appointment occurrenceToModify = Appointment.BindToOccurrence(service,
                                                                    recurrMaster.Id,
                                                                    2,
                                                                    new PropertySet(AppointmentSchema.Location,
                                                                                    AppointmentSchema.Start,
                                                                                    AppointmentSchema.End,
                                                                                    AppointmentSchema.RequiredAttendees,
                                                                                    AppointmentSchema.Subject));
    // Update the properties you want to change.
    occurrenceToModify.Location = "Helipad of Contoso Bldg 1";
    occurrenceToModify.Start = occurrenceToModify.Start.AddDays(1);
    occurrenceToModify.End = occurrenceToModify.End.AddDays(1);
    occurrenceToModify.RequiredAttendees.Add("Contoso CEO", "sadie@contoso");
    occurrenceToModify.RequiredAttendees.Add("Contoso Head of Research", "ronnie@contoso.com");
    occurrenceToModify.RequiredAttendees.Add("Contoso Head of Security", "alfred@contoso.com");
    occurrenceToModify.Subject = occurrenceToModify.Subject.ToString() + ":Mandatory";
    // Update the occurrence in your calendar folder and send meeting update requests to attendees.
    // This method call results in an UpdateItem request to EWS.
    occurrenceToModify.Update(ConflictResolutionMode.AlwaysOverwrite, SendInvitationsOrCancellationsMode.SendToAllAndSaveCopy);
    // View updated and deleted occurrences on the recurring master prior to retrieving updated information.
    Console.WriteLine("Modified Occurrences prior to updating recurring master: {0}",
                    (recurrMaster.ModifiedOccurrences == null ? "None" : recurrMaster.ModifiedOccurrences.Count.ToString()));
    // Update the recurring master to view the modified and deleted occurrences.
    recurrMaster = Appointment.Bind(service, recurrenceMasterId, new PropertySet(AppointmentSchema.ModifiedOccurrences,
                                                                        AppointmentSchema.DeletedOccurrences));
    // View updated and deleted occurrences on the recurring master after retrieving updated information.
    Console.WriteLine("Modified Occurrences after updating recurring master:\t {0}",
                    (recurrMaster.ModifiedOccurrences == null ? "None" : recurrMaster.ModifiedOccurrences.Count.ToString()));
    return recurrMaster.Id;            
}

```

## <a name="modify-a-single-occurrence-in-a-series-by-using-ews"></a>Ändern eines einzelnen Vorkommens in einer Datenreihe mithilfe von EWS

Das Ändern einer einzelnen Instanz in einer Datenreihe entspricht im Wesentlichen dem Ändern eines Einzelnen Instanztermins. Sie können das zu ändernde Vorkommen mithilfe einer [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) oder eines [OccurrenceItemId-Elements](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) angeben. 
  
Das folgende Beispiel zeigt den Anforderungs-XML-Code, wenn Sie den [UpdateItem-Vorgang](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) verwenden, um ein Vorkommen in einer Terminserie zu aktualisieren. Die **ItemId** und **der ChangeKey** werden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToAllAndSaveCopy">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkA" ChangeKey="DwAAAB" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Location" />
              <t:CalendarItem>
                <t:Location>Helipad of Contoso Bldg 1</t:Location>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Start" />
              <t:CalendarItem>
                <t:Start>2014-03-27T19:33:00.000-07:00</t:Start>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:End" />
              <t:CalendarItem>
                <t:End>2014-03-27T20:33:00.000-07:00</t:End>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:RequiredAttendees" />
              <t:CalendarItem>
                <t:RequiredAttendees>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Mack@contoso.com</t:Name>
                      <t:EmailAddress>Mack@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Sadie@contoso.com</t:Name>
                      <t:EmailAddress>Sadie@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Magdalena@contoso.com</t:Name>
                      <t:EmailAddress>Magdalena@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Contoso CEO</t:Name>
                      <t:EmailAddress>sadie@contoso</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Contoso Head of Research</t:Name>
                      <t:EmailAddress>ronnie@contoso.com</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Contoso Head of Security</t:Name>
                      <t:EmailAddress>alfred@contoso.com</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                </t:RequiredAttendees>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:CalendarItem>
                <t:Subject>Weekly Update Meeting:Mandatory</t:Subject>
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **UpdateItem-Anforderung** mit einer [UpdateItemResponse-Nachricht,](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) die den [ResponseCode-Wert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** enthält, der angibt, dass das Vorkommen erfolgreich aktualisiert wurde, und die [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) des aktualisierten Termins. 
  
## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Serienmuster und EWS](recurrence-patterns-and-ews.md)
    
- [Zugreifen auf eine Serienserie mithilfe von EWS in Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Erstellen einer Serienserie mithilfe von EWS in Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Löschen von Terminen in einer Terminserie mithilfe von EWS in Exchange](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Aktualisieren einer Serienserie mithilfe von EWS in Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    

