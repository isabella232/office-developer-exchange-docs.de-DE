---
title: Aktualisieren einer Terminserie mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7e61bee9-4840-4773-a0a7-47b11e1fdf59
description: Erfahren Sie, wie Termine in einer Terminserie ändern, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: ecee78457d2e6f91483cf897cfb4976fbd83400c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757013"
---
# <a name="update-a-recurring-series-by-using-ews"></a><span data-ttu-id="a870e-103">Aktualisieren einer Terminserie mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="a870e-103">Update a recurring series by using EWS</span></span>

<span data-ttu-id="a870e-104">Erfahren Sie, wie Termine in einer Terminserie ändern, indem Sie die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="a870e-104">Learn how to modify appointments in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="a870e-105">Der EWS Managed API oder EWS können Sie eine Terminserie entweder [die gesamte Datenreihe aktualisieren](how-to-update-a-recurring-series-by-using-ews-in-exchange.md), oder durch ein einzelnes Vorkommen aktualisieren aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a870e-105">You can use the EWS Managed API or EWS to update a recurring series by either [updating the entire series](how-to-update-a-recurring-series-by-using-ews-in-exchange.md), or by updating a single occurrence.</span></span> <span data-ttu-id="a870e-106">In diesem Artikel wird wie ein einzelnes Vorkommen aktualisieren erläutert.</span><span class="sxs-lookup"><span data-stu-id="a870e-106">In this article we'll discuss how to update a single occurrence.</span></span>
  
<span data-ttu-id="a870e-107">Ändern eines Termins in einer Reihe ist [eine einzelne Instanz eines Termins ändern](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="a870e-107">Modifying a single appointment in a series is very similar to [modifying a single instance appointment](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="a870e-108">Verwenden Sie die gleichen Methoden und Vorgänge, aber Sie verwenden die Element-ID des Vorkommens, den Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="a870e-108">You use the same methods and operations, but you use the item ID of the occurrence you want to change.</span></span>
  
<span data-ttu-id="a870e-109">Wenn Sie ein einzelnes Element in einer Reihe ändern, wird ein Array von geänderten Termine, der sich wiederholenden Masterseite für die Datenreihe zugeordnet, Vorkommen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a870e-109">When you change a single occurrence in a series, that occurrence is added to an array of modified appointments associated with the recurring master for the series.</span></span> <span data-ttu-id="a870e-110">Sie können die [Appointment.ModifiedOccurrences](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) EWS Managed API-Eigenschaft oder das [ModifiedOccurrences](http://msdn.microsoft.com/library/552932fc-b3b4-486e-8d73-32c0bb10bd68%28Office.15%29.aspx) EWS-Element verwenden, auf alle Termine in einer Serie zugreifen, die geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="a870e-110">You can use the [Appointment.ModifiedOccurrences](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) EWS Managed API property or the [ModifiedOccurrences](http://msdn.microsoft.com/library/552932fc-b3b4-486e-8d73-32c0bb10bd68%28Office.15%29.aspx) EWS element to access all the appointments in a series that have been modified.</span></span> 
  
## <a name="modify-a-single-occurrence-in-a-series-by-using-the-ews-managed-api"></a><span data-ttu-id="a870e-111">Ändern Sie ein einzelnes Element in einer Reihe, indem Sie die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="a870e-111">Modify a single occurrence in a series by using the EWS Managed API</span></span>

<span data-ttu-id="a870e-112">So ändern Sie eine einzelne Instanz in einer Reihe Sie:</span><span class="sxs-lookup"><span data-stu-id="a870e-112">To modify a single instance in a series, you:</span></span>
  
1. <span data-ttu-id="a870e-113">Binden Sie an das Vorkommen zu ändern, indem Sie entweder die [Appointment.BindToOccurrence](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) -Methode mit der Indexwert des Elements oder die [Appointment.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) -Methode mit der Vorkommen-ID.</span><span class="sxs-lookup"><span data-stu-id="a870e-113">Bind to the occurrence you want to modify by using either the [Appointment.BindToOccurrence](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) method with the item's index value, or the [Appointment.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) method with the occurrence's ID.</span></span> <span data-ttu-id="a870e-114">Sie erhalten diese ID aus der [ID-](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) Eigenschaft eines [Termins](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) -Objekts, das das Vorkommen entspricht, oder aus der [ItemId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.occurrenceinfo.itemid%28v=exchg.80%29.aspx) -Eigenschaft des [OccurrenceInfo](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.occurrenceinfo%28v=exchg.80%29.aspx) -Objekts, das das Vorkommen entspricht.</span><span class="sxs-lookup"><span data-stu-id="a870e-114">You obtain this ID from either the [Id](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) property of an [Appointment](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object that corresponds to the occurrence, or from the [ItemId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.occurrenceinfo.itemid%28v=exchg.80%29.aspx) property of the [OccurrenceInfo](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.occurrenceinfo%28v=exchg.80%29.aspx) object that corresponds to the occurrence.</span></span> 
    
2. <span data-ttu-id="a870e-115">Aktualisieren Sie die Eigenschaften für das Vorkommen Appointment-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a870e-115">Update the properties on the occurrence's Appointment object.</span></span>
    
3. <span data-ttu-id="a870e-116">Speichern Sie die Änderungen auf das Vorkommen eines Termins-Objekt mithilfe der [Appointment.Save](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a870e-116">Save the changes to the occurrence's appointment object by using the [Appointment.Save](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="a870e-117">Im folgenden Beispiel einen Termin in einer Terminserie aktualisiert und stellt sicher, dass der geänderte Termin auf dem sich wiederholenden Master aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a870e-117">The following example updates an appointment in a recurring series and verifies that the modified appointment is updated on the recurring master.</span></span> <span data-ttu-id="a870e-118">In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="a870e-118">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="a870e-119">Die `recurrenceMasterId` Parameter ist ein Bezeichner für das Vorkommen so ändern Sie die wiederkehrende Master zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a870e-119">The  `recurrenceMasterId` parameter is an identifier associated with the recurring master for the occurrence to modify.</span></span> 
  
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

## <a name="modify-a-single-occurrence-in-a-series-by-using-ews"></a><span data-ttu-id="a870e-120">Ändern Sie ein einzelnes Element in einer Reihe mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="a870e-120">Modify a single occurrence in a series by using EWS</span></span>

<span data-ttu-id="a870e-121">Ändern eine einzelne Instanz in einer Reihe ist im Wesentlichen das eine einzelne Instanz eines Termins ändern.</span><span class="sxs-lookup"><span data-stu-id="a870e-121">Modifying a single instance in a series is essentially the same as modifying a single instance appointment.</span></span> <span data-ttu-id="a870e-122">Sie können das Vorkommen so ändern Sie mithilfe einer [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) oder ein [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) -Element angeben.</span><span class="sxs-lookup"><span data-stu-id="a870e-122">You can specify the occurrence to change by using either an [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) or an [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="a870e-123">Das folgende Beispiel zeigt die XML-Anforderung, wenn Sie den Vorgang [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) verwenden, um das Auftreten eines Serientermins in einer Serie von Terminen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a870e-123">The following example shows the request XML when you use the [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) operation to update an occurrence in a recurring series of appointments.</span></span> <span data-ttu-id="a870e-124">Die **ItemId** und **ChangeKey** werden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="a870e-124">The **ItemId** and **ChangeKey** are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="a870e-125">Der Server antwortet auf die **UpdateItem** Anforderung durch eine [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) Nachricht mit dem Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass das Vorkommen erfolgreich aktualisiert wurde, und die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) die aktualisierte Termin.</span><span class="sxs-lookup"><span data-stu-id="a870e-125">The server responds to the **UpdateItem** request with an [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the occurrence was updated successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the updated appointment.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a870e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a870e-126">See also</span></span>


- [<span data-ttu-id="a870e-127">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="a870e-127">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="a870e-128">Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="a870e-128">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="a870e-129">Serienmuster und EWS</span><span class="sxs-lookup"><span data-stu-id="a870e-129">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
- [<span data-ttu-id="a870e-130">Zugriff auf eine Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="a870e-130">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="a870e-131">Erstellen einer Terminserie mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="a870e-131">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="a870e-132">Löschen der Termine in einer Terminserie mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="a870e-132">Delete appointments in a recurring series by using EWS in Exchange</span></span>](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="a870e-133">Aktualisieren einer Terminserie mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="a870e-133">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    

