---
title: Löschen von Terminen und Abbrechen an Besprechungen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 42412265-3968-468a-a8c2-7e8af3c6deb9
description: Erfahren Sie, wie Termine und Besprechungen zu löschen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: bd7eac803fedffc51133324259f68fd25652fcff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756886"
---
# <a name="delete-appointments-and-cancel-meetings-by-using-ews-in-exchange"></a><span data-ttu-id="56e3d-103">Löschen von Terminen und Abbrechen an Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="56e3d-103">Delete appointments and cancel meetings by using EWS in Exchange</span></span>

<span data-ttu-id="56e3d-104">Erfahren Sie, wie Termine und Besprechungen zu löschen, indem Sie die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="56e3d-104">Learn how to delete appointments and meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="56e3d-p101">Der wesentliche Unterschied zwischen Besprechungen und Terminen ist, dass Besprechungen Teilnehmer haben und Termine nicht. Termine und Besprechungen können einzelne Instanzen oder Teil einer Reihe sein. Da Termine keine Teilnehmer, Räume oder Ressourcen enthalten, muss keine Nachricht gesendet werden. Intern verwendet Exchange das gleiche Objekt für Besprechungen und Termine. Verwenden Sie die [Appointment-Klasse](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) in der EWS Managed API oder das Element [CalendarItem](http://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx) in EWS zum Arbeiten mit Besprechungen und Termine.</span><span class="sxs-lookup"><span data-stu-id="56e3d-p101">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't. Both appointments and meetings can be single instances or part of a recurring series, but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent. Internally, Exchange uses the same object for both meetings and appointments. You use the EWS Managed API [Appointment class](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](http://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="56e3d-109">**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge zum Löschen von Terminen und Besprechungen**</span><span class="sxs-lookup"><span data-stu-id="56e3d-109">**Table 1. EWS Managed API methods and EWS operations for deleting appointments and meetings**</span></span>

|<span data-ttu-id="56e3d-110">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="56e3d-110">**EWS Managed API method**</span></span>|<span data-ttu-id="56e3d-111">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="56e3d-111">**EWS Operation**</span></span>|<span data-ttu-id="56e3d-112">**Funktionsweise**</span><span class="sxs-lookup"><span data-stu-id="56e3d-112">**What it does**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="56e3d-113">Appointment.Delete</span><span class="sxs-lookup"><span data-stu-id="56e3d-113">Appointment.Delete</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="56e3d-114">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="56e3d-114">DeleteItem</span></span>](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |<span data-ttu-id="56e3d-115">Löscht einen Termin an.</span><span class="sxs-lookup"><span data-stu-id="56e3d-115">Deletes an appointment.</span></span>  <br/> |
|[<span data-ttu-id="56e3d-116">Appointment.Delete</span><span class="sxs-lookup"><span data-stu-id="56e3d-116">Appointment.Delete</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="56e3d-117">CreateItem (Kalenderelement)</span><span class="sxs-lookup"><span data-stu-id="56e3d-117">CreateItem (calendar item)</span></span>](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) <br/> |<span data-ttu-id="56e3d-118">Löscht eine Besprechung.</span><span class="sxs-lookup"><span data-stu-id="56e3d-118">Deletes a meeting.</span></span>  <br/> |
   
<span data-ttu-id="56e3d-119">Beachten Sie, dass beim Löschen eines Termins mithilfe der Exchange-Webdienste den Vorgang [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) verwenden, aber wenn Sie eine Besprechung zu löschen, verwenden Sie die [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) Operation.</span><span class="sxs-lookup"><span data-stu-id="56e3d-119">Note that when you delete an appointment by using EWS, you use the [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) operation, but when you delete a meeting, you use the [CreateItem ](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="56e3d-120">Dies mag nicht besonders intuitiv, aber es ist, müssen Sie eine Besprechung erstellen Response-Objekt zum Senden von Besprechungsabsagen Nachrichten an die Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="56e3d-120">This might seem counterintuitive, but it is because you have to create a meeting response object to send meeting cancellation messages to attendees.</span></span> 
  
## <a name="delete-an-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="56e3d-121">Löschen eines Termins mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="56e3d-121">Delete an appointment by using the EWS Managed API</span></span>
<span data-ttu-id="56e3d-122"><a name="bk_DeleteApptEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="56e3d-122"></span></span>

<span data-ttu-id="56e3d-123">Im folgenden Codebeispiel wird veranschaulicht, wie Sie die [Delete](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) -Methode, um einen Termin aus den Kalenderordner zu löschen und die [ExchangeService.FindItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methode, um sicherzustellen, dass der Termin gelöscht wurde, indem Sie im Ordner "Gelöschte Elemente" gesucht.</span><span class="sxs-lookup"><span data-stu-id="56e3d-123">The following code example shows how to use the [Delete](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) method to delete an appointment from your calendar folder, and the [ExchangeService.FindItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) method to verify that the appointment was deleted by looking for it in the Deleted Items folder.</span></span> 
  
<span data-ttu-id="56e3d-124">In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="56e3d-124">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="56e3d-125">Die lokale Variable `appointmentId` ein Bezeichner vorhandenen Termin zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="56e3d-125">The local variable  `appointmentId` is an identifier associated with an existing appointment.</span></span> 
  
```cs
// Instantiate an appointment object by binding to it by using the ItemId.
// As a best practice, limit the properties returned to only the ones you need.
Appointment appointment = Appointment.Bind(service, appointmentId, new PropertySet());
// Delete the appointment. Note that the item ID will change when the item is moved to the Deleted Items folder.
appointment.Delete(DeleteMode.MoveToDeletedItems);
// Verify that the appointment has been deleted by looking for a matching subject in the Deleted Items folder's first entry.
ItemView itemView = new ItemView(1);
itemView.Traversal = ItemTraversal.Shallow;
// Just retrieve the properties you need.
itemView.PropertySet = new PropertySet(ItemSchema.Id, ItemSchema.ParentFolderId, ItemSchema.Subject);
// Note that the FindItems method results in a call to EWS.
FindItemsResults<Item> deletedItems = service.FindItems(WellKnownFolderName.DeletedItems, itemView);
Item deletedItem = deletedItems.First();
Folder parentFolder = Folder.Bind(service, deletedItem.ParentFolderId, new PropertySet(FolderSchema.DisplayName));
Console.WriteLine("The appointment " + "\"" + deletedItem.Subject + "\"" + " is now in the " + parentFolder.DisplayName + " folder.");

```

<span data-ttu-id="56e3d-126">Dieses Beispiel zeigt eine einfache Möglichkeit, stellen Sie sicher, dass der Termin gelöscht wurde, überprüfen Sie, dass der Betreff des ersten Elements in den Ordner Gelöschte Objekte, die von der gelöschten Termin entspricht, an.</span><span class="sxs-lookup"><span data-stu-id="56e3d-126">This example shows a simple way to verify that the appointment was deleted, by verifying that the subject of the first item in the Deleted Items folder matches that of the deleted appointment.</span></span> <span data-ttu-id="56e3d-127">Wie Sie auswählen, um sicherzustellen, dass Ihr Termin gelöscht wurde variiert je nach den Anforderungen der Anwendung basiert.</span><span class="sxs-lookup"><span data-stu-id="56e3d-127">How you choose to verify that your appointment was deleted will vary based the needs of your application.</span></span>
  
<span data-ttu-id="56e3d-128">Wie Sie sehen können, Löschen einen Termin ist einfach und ziemlich erwartet.</span><span class="sxs-lookup"><span data-stu-id="56e3d-128">As you can see, deleting an appointment is straightforward and pretty much what you might expect.</span></span> <span data-ttu-id="56e3d-129">Hinweis: Wenn Sie Ihre Überprüfungsschritt aufgesetzt werden muss, Terminelement in den Ordner Gelöschte Objekte einer anderen ItemId als Terminelement in den Kalenderordner hat.</span><span class="sxs-lookup"><span data-stu-id="56e3d-129">Note when you create your verification step that the appointment item in the Deleted Items folder has a different ItemId than the appointment item in the calendar folder.</span></span> <span data-ttu-id="56e3d-130">Das Element wird kopiert und gelöscht, anstatt einfach in den Ordner Gelöschte Objekte verschoben.</span><span class="sxs-lookup"><span data-stu-id="56e3d-130">The item is copied and deleted rather than simply moved to the Deleted Items folder.</span></span> 
  
## <a name="delete-an-appointment-by-using-ews"></a><span data-ttu-id="56e3d-131">Löschen eines Termins mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="56e3d-131">Delete an appointment by using EWS</span></span>
<span data-ttu-id="56e3d-132"><a name="bk_DeleteApptEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="56e3d-132"></span></span>

<span data-ttu-id="56e3d-133">Die Anforderung und Antwort-XML in den folgenden Beispielen werden von der EWS Managed API-Code in das [Löschen eines Termins mithilfe der EWS Managed API](#bk_DeleteApptEWSMA)-Aufrufe entsprechen.</span><span class="sxs-lookup"><span data-stu-id="56e3d-133">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Delete an appointment by using the EWS Managed API](#bk_DeleteApptEWSMA).</span></span> <span data-ttu-id="56e3d-134">Die Anforderung und Antwort wird XML, das überprüft, ob das Terminelement im Ordner "Gelöschte Elemente" ist ebenfalls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="56e3d-134">The request and response XML that verifies that the appointment item is in the Deleted Items folder is shown as well.</span></span>
  
<span data-ttu-id="56e3d-135">Das folgende Beispiel zeigt die XML-Anforderung für den Vorgang [DeleteItem](http://msdn.microsoft.com/library/e2152410-41ce-1fe7-8169-f206d5081ebc%28Office.15%29.aspx) , um einen Termin zu löschen.</span><span class="sxs-lookup"><span data-stu-id="56e3d-135">The following example shows the request XML for the [DeleteItem](http://msdn.microsoft.com/library/e2152410-41ce-1fe7-8169-f206d5081ebc%28Office.15%29.aspx) operation to delete an appointment.</span></span> 
  
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
    <m:DeleteItem DeleteType="MoveToDeletedItems" SendMeetingCancellations="SendToAllAndSaveCopy">
      <m:ItemIds>
        <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="56e3d-136">Das folgende Beispiel zeigt die Antwort-XML, das von der [DeleteItem Vorgang](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="56e3d-136">The following example shows the response XML that is returned by the [DeleteItem operation](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx).</span></span> <span data-ttu-id="56e3d-137">Die Attribute **ItemId** und **ChangeKey** werden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="56e3d-137">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </m:DeleteItemResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="56e3d-138">Das folgende Beispiel zeigt die XML-Anforderung für den [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Vorgang, der das erste Element in den Ordner Gelöschte Elemente abruft, um das Element Betreff mit der gelöschten Appointment-Objekts verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="56e3d-138">The following example shows the request XML for the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation that retrieves the first item in the Deleted Items folder in order to compare the item's subject with that of the deleted appointment object.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages
" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ItemId" />
          <t:FieldURI FieldURI="item:ParentFolderId" />
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="56e3d-139">Das folgende Beispiel zeigt die Antwort-XML, das von der Operation [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) während der Überprüfung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="56e3d-139">The following example shows the response XML that is returned by the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation during the verification step.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="56e3d-140">Die Attribute **ItemId** und **ChangeKey** werden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="56e3d-140">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="10748" IncludesLastItemInRange="false">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkA=" ChangeKey="DwAAA" />
                <t:ParentFolderId Id="AAMkA" ChangeKey="AQAAA" />
                <t:Subject>Tennis lesson</t:Subject>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="56e3d-141"><a name="bk_DeleteMtgEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="56e3d-141"></span></span>

## <a name="delete-a-meeting-by-using-the-ews-managed-api"></a><span data-ttu-id="56e3d-142">Löschen einer Besprechung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="56e3d-142">Delete a meeting by using the EWS Managed API</span></span>

<span data-ttu-id="56e3d-143">Wenn Sie eine Besprechung, zusätzlich zum Entfernen des Terminelements aus dem Kalenderordner löschen möchten Sie möglicherweise auch Besprechungsabsagen an die Teilnehmer senden.</span><span class="sxs-lookup"><span data-stu-id="56e3d-143">When you delete a meeting, in addition to removing the appointment item from the calendar folder, you might also want to send meeting cancellations to attendees.</span></span> <span data-ttu-id="56e3d-144">Die folgenden drei Methoden können Sie eine Besprechung absagen:</span><span class="sxs-lookup"><span data-stu-id="56e3d-144">You can use the following three methods to cancel a meeting:</span></span>
  
- [<span data-ttu-id="56e3d-145">Appointment.Delete</span><span class="sxs-lookup"><span data-stu-id="56e3d-145">Appointment.Delete</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="56e3d-146">Appointment.CancelMeeting</span><span class="sxs-lookup"><span data-stu-id="56e3d-146">Appointment.CancelMeeting</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="56e3d-147">CancelMeetingMessage</span><span class="sxs-lookup"><span data-stu-id="56e3d-147">CancelMeetingMessage</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.cancelmeetingmessage%28v=exchg.80%29.aspx)
    
<span data-ttu-id="56e3d-148">Die Methode, die Sie auswählen, hängt von der Detailebene, die Sie in Ihre Absage bereitstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="56e3d-148">The method that you choose depends on the level of detail you need to provide in your cancellation message.</span></span> <span data-ttu-id="56e3d-149">[Appointment.CancelMeeting](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx) erleichtert die Absage aktualisieren, indem Sie eine aktualisierte Meldung als Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="56e3d-149">[Appointment.CancelMeeting](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx) makes it easy to update the cancellation message by passing an updated message as a parameter.</span></span> <span data-ttu-id="56e3d-150">[CancelMeetingMessage](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.cancelmeetingmessage%28v=exchg.80%29.aspx) können Sie die Eigenschaften für die Nachricht vor dem Senden eines Abbruchs, damit Sie Aktionen wie Anforderung eine Bestätigung wie ändern.</span><span class="sxs-lookup"><span data-stu-id="56e3d-150">[CancelMeetingMessage](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.cancelmeetingmessage%28v=exchg.80%29.aspx) allows you to modify properties on your message before sending a cancellation, so you can do things like request a receipt.</span></span> 
  
<span data-ttu-id="56e3d-151">Die Codebeispiele in diesem Abschnitt veranschaulichen unterschiedlichen Möglichkeiten zum Löschen einer Besprechung und Senden von Besprechungsabsagen.</span><span class="sxs-lookup"><span data-stu-id="56e3d-151">The code examples in this section show the different ways to delete a meeting and send meeting cancellations.</span></span> <span data-ttu-id="56e3d-152">In den Beispielen wird davon ausgegangen, dass Sie auf einem Exchange-Server authentifiziert wurden und ein [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt mit dem Namen **Service**erworben haben.</span><span class="sxs-lookup"><span data-stu-id="56e3d-152">The examples assume that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="56e3d-153">Die lokale Variable `meetingId` ist ein Bezeichner, die mit einer vorhandenen Besprechung verknüpft ist, in dem die Zielbenutzer der Organisator der Besprechung ist.</span><span class="sxs-lookup"><span data-stu-id="56e3d-153">The local variable  `meetingId` is an identifier associated with an existing meeting where the target user is the meeting organizer.</span></span> 
  
<span data-ttu-id="56e3d-154">Im folgenden Codebeispiel wird veranschaulicht, wie an eine Besprechung mit der [Appointment.Delete](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) -Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="56e3d-154">The following code example shows how to delete a meeting by using the [Appointment.Delete](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) method.</span></span> 
  
```cs
// Instantiate an appointment object for the meeting by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
            
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet());
// Delete the meeting by using the Delete method.
meeting.Delete(DeleteMode.MoveToDeletedItems, SendCancellationsMode.SendToAllAndSaveCopy);
// Verify that the meeting has been deleted by looking for a matching subject in the Deleted Items folder's first entry.
ItemView itemView = new ItemView(1);
itemView.Traversal = ItemTraversal.Shallow;
// Just retrieve the properties you need.
itemView.PropertySet = new PropertySet(ItemSchema.Id, ItemSchema.ParentFolderId, ItemSchema.Subject);
// Note that the FindItems method results in a call to EWS.
FindItemsResults<Item> deletedItems = service.FindItems(WellKnownFolderName.DeletedItems, itemView);
Item deletedItem = deletedItems.First();
Folder parentFolder = Folder.Bind(service, deletedItem.ParentFolderId, new PropertySet(FolderSchema.DisplayName));
Console.WriteLine("The meeting " + "\"" + deletedItem.Subject + "\"" + " is now in the " + parentFolder.DisplayName + " folder.");

```

<span data-ttu-id="56e3d-155">Im folgenden Codebeispiel wird veranschaulicht, wie an eine Besprechung mit der [CancelMeeting](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx) -Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="56e3d-155">The following code example shows how to delete a meeting by using the [CancelMeeting](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx) method.</span></span> 
  
```cs
// Instantiate an appointment object by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet());
// Delete the meeting by using the CancelMeeting method.
meeting.CancelMeeting("The outdoor meeting has been cancelled due to hailstorms.");

```

<span data-ttu-id="56e3d-156">Im folgenden Codebeispiel wird veranschaulicht, wie an eine Besprechung mit der [Appointment.CreateCancelMeetingMessage](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.createcancelmeetingmessage%28v=exchg.80%29.aspx) -Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="56e3d-156">The following code example shows how to delete a meeting by using the [Appointment.CreateCancelMeetingMessage](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.createcancelmeetingmessage%28v=exchg.80%29.aspx) method.</span></span> 
  
```cs
// Instantiate an appointment object by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet());
// Delete the meeting by using the CreateCancelMeetingMessage method.
CancelMeetingMessage cancelMessage = meeting.CreateCancelMeetingMessage();
cancelMessage.Body = new MessageBody("The outdoor meeting has been canceled due to hailstorms.");
cancelMessage.IsReadReceiptRequested = true;
cancelMessage.SendAndSaveCopy();

```

## <a name="delete-a-meeting-by-using-ews"></a><span data-ttu-id="56e3d-157">Löschen einer Besprechung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="56e3d-157">Delete a meeting by using EWS</span></span>
<span data-ttu-id="56e3d-158"><a name="bk_EWSDeleteApptAndMeeting"> </a></span><span class="sxs-lookup"><span data-stu-id="56e3d-158"></span></span>

<span data-ttu-id="56e3d-159">Die Anforderung und Antwort-XML in den folgenden Beispielen entsprechen Aufrufe durch die EWS Managed API-Code in [einer Besprechung mithilfe der EWS Managed API löschen](#bk_DeleteMtgEWSMA) mithilfe der [Appointment.Delete](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="56e3d-159">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Delete a meeting by using the EWS Managed API](#bk_DeleteMtgEWSMA) by using the [Appointment.Delete](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="56e3d-160">Das folgende Beispiel zeigt die XML-Anforderung, wenn Sie den [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgang zum Abbruch Nachrichten an Teilnehmer senden und Löschen einer Besprechung verwenden.</span><span class="sxs-lookup"><span data-stu-id="56e3d-160">The following example shows the request XML when you use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to send cancellation messages to attendees and delete a meeting.</span></span> 
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:CancelCalendarItem>
          <t:ReferenceItemId Id="AAMkA" ChangeKey="DwAAA" />
          <t:NewBodyContent BodyType="HTML">The outdoor meeting has been canceled due to hailstorms.</t:NewBodyContent>
        </t:CancelCalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="56e3d-161">Das folgende Beispiel zeigt den XML-Code, der als Antwort auf eine [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) Operation-Anforderung verwendet, um eine Besprechung löschen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="56e3d-161">The following example shows the XML that is returned in response to a [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation request used to delete a meeting.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="56e3d-162">Die Attribute **ItemId** und **ChangeKey** werden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="56e3d-162">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
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

<span data-ttu-id="56e3d-163">Das folgende Beispiel zeigt die XML-Anforderung für den [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Vorgang, der das erste Element in den Ordner Gelöschte Elemente abruft, um das Element Betreff mit der gelöschten Appointment-Objekts verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="56e3d-163">The following example shows the request XML for the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation that retrieves the first item in the Deleted Items folder in order to compare the item's subject with that of the deleted appointment object.</span></span> 
  
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
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ItemId" />
          <t:FieldURI FieldURI="item:ParentFolderId" />
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="56e3d-164">Das folgende Beispiel zeigt den XML-Code, der von der Operation [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) während der Überprüfung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="56e3d-164">The following example shows the XML that is returned by the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation during the verification step.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="56e3d-165">Die Attribute **Id** und **ChangeKey** werden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="56e3d-165">The **Id** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="10750" IncludesLastItemInRange="false">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
                <t:ParentFolderId Id="AAMkA" ChangeKey="AQAAA" />
                <t:Subject>Team building exercise</t:Subject>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="56e3d-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56e3d-166">See also</span></span>

- [<span data-ttu-id="56e3d-167">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="56e3d-167">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)    
- [<span data-ttu-id="56e3d-168">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="56e3d-168">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)  
- [<span data-ttu-id="56e3d-169">Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="56e3d-169">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="56e3d-170">Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="56e3d-170">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [<span data-ttu-id="56e3d-171">Vorschlagen einer neuen Besprechungszeit mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="56e3d-171">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="56e3d-172">Vorschlagen einer neuen Besprechungszeit mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="56e3d-172">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

