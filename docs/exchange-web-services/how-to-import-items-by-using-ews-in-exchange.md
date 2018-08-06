---
title: Importieren von Elementen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd3d3221-c98e-4fa0-81f0-77f733d2f432
description: Informationen zum Importieren von Terminen, E-Mails, Kontakten, Aufgaben und anderen Elemente mithilfe der verwalteten EWS-API oder EWS in Exchange.
ms.openlocfilehash: c09c96eff455b7584b084e71b937853abfde731d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756952"
---
# <a name="import-items-by-using-ews-in-exchange"></a><span data-ttu-id="f3ed6-103">Importieren von Elementen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f3ed6-103">How to: Import items by using EWS in Exchange</span></span>

<span data-ttu-id="f3ed6-104">Informationen zum Importieren von Terminen, E-Mails, Kontakten, Aufgaben und anderen Elemente mithilfe der verwalteten EWS-API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-104">Learn how to import appointments, emails, contacts, tasks, and other items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="f3ed6-p101">Viele Systeme enthalten Termine, E-Mails, Kontakte und Aufgaben, und Sie können diese Elemente auf verschiedene Arten in Exchange importieren. Das Importieren von Elementen in Exchange ist einfach, wenn für diese Elemente keine Postfachbeziehungen verwaltet werden. Sie können die [Item.Save](http://msdn.microsoft.com/de-DE/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx)-Methode der EWS Managed API oder den [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)-Vorgang in EWS verwenden, um die Elemente in einem Exchange-Postfach zu erstellen. Der einfache Ansatz unterstützt jedoch nicht alle Szenarien. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f3ed6-p101">Many systems contain appointments, emails, contacts, and tasks, and you can import those items into Exchange in a number of different ways. Importing items into Exchange is simple when mailbox relationships aren't maintained on those items. You can use the [Item.Save](http://msdn.microsoft.com/de-DE/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) EWS Managed API method or the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation to create the items in an Exchange mailbox. The simple approach does not support all scenarios, however; for example:</span></span> 
  
- <span data-ttu-id="f3ed6-p102">Die Beziehung zwischen Organisatoren und Teilnehmer wird nicht beibehalten, wenn Sie Termine mit Teilnehmern (Besprechungen) importieren. Dies bedeutet, dass der Organisator der Besprechung, den Teilnehmern an der Besprechung erneut eine Einladung senden muss, damit die Beziehung zwischen den Organisator und den Teilnehmer wiederhergestellt wird. Wenn der Termin in den Kalender eines Teilnehmers importiert wurde, wird der Termin nicht mit dem Termin des Organisators verknüpft. Die Teilnehmer müssen die aktuellste Besprechungseinladung des Organisators akzeptieren, um die Beziehung zwischen Organisator und Teilnehmer wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-p102">You cannot maintain the relationship between organizers and attendees when importing appointments with attendees (meetings). This means that the meeting organizer will need to resend meeting invites to attendees in order to reestablish the relationship between the organizer and attendees. If the appointment was imported into an attendee's calendar, the appointment will not be related to the meeting organizer's appointment. The attendees will need to accept the resent meeting invite from the organizer in order to reestablish the organizer-attendee relationship.</span></span>
    
- <span data-ttu-id="f3ed6-113">Informationen zu den Teilnehmern werden nicht beibehalten, wenn zugewiesene Aufgaben importiert werden.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-113">Information about the assignees is not preserved when assigned tasks are imported.</span></span>
    
<span data-ttu-id="f3ed6-114">Alle Importoptionen können für den Stapelimport von Elementen in Exchange verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-114">All the import options can be used to batch import items into Exchange.</span></span>
  
## <a name="use-ews-managed-api-or-ews-item-types-to-import-an-item"></a><span data-ttu-id="f3ed6-115">Verwenden der EWS Managed API oder von EWS-Elementtypen zum Import eines Elements</span><span class="sxs-lookup"><span data-stu-id="f3ed6-115">Use EWS Managed API or EWS item types to import an item</span></span>
<span data-ttu-id="f3ed6-116"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="f3ed6-116"></span></span>

<span data-ttu-id="f3ed6-p103">Sie können die EWS Managed API oder EWS zum Import von E-Mails, Kontakten, Terminen oder Aufgaben von anderen Systemen verwenden. Stellen Sie die [Eigenschaften ](properties-and-extended-properties-in-ews-in-exchange.md) Ihres Quellformat abhängig vom importierten Element auf einen der folgenden Werte ein.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-p103">You can use the EWS Managed API or EWS to import emails, contacts, appointments, or tasks from other systems. Just set the [properties ](properties-and-extended-properties-in-ews-in-exchange.md) from your source format on any of the following objects, depending on what you're importing.</span></span> 
  
<span data-ttu-id="f3ed6-119">**Tabelle 1. EWS Managed API-Objekte und EWS-Elemente**</span><span class="sxs-lookup"><span data-stu-id="f3ed6-119">**Table 1. EWS Managed API objects and EWS elements**</span></span>

|<span data-ttu-id="f3ed6-120">**EWS Managed API-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f3ed6-120">**EWS Managed API object**</span></span>|<span data-ttu-id="f3ed6-121">**EWS-Element**</span><span class="sxs-lookup"><span data-stu-id="f3ed6-121">**EWS element**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3ed6-122">EmailMessage</span><span class="sxs-lookup"><span data-stu-id="f3ed6-122">EmailMessage</span></span>](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="f3ed6-123">Message</span><span class="sxs-lookup"><span data-stu-id="f3ed6-123">Message</span></span>](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="f3ed6-124">Contact</span><span class="sxs-lookup"><span data-stu-id="f3ed6-124">Contact</span></span>](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="f3ed6-125">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="f3ed6-125">Contact</span></span>](http://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="f3ed6-126">Appointment</span><span class="sxs-lookup"><span data-stu-id="f3ed6-126">Appointment</span></span>](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="f3ed6-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="f3ed6-127">CalendarItem</span></span>](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="f3ed6-128">Task</span><span class="sxs-lookup"><span data-stu-id="f3ed6-128">Task</span></span>](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="f3ed6-129">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="f3ed6-129">Task</span></span>](http://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="f3ed6-p104">Verwenden Sie die [Item.Save](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx)-Methode der EWS Managed API oder den [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)-Vorgang in EWS zum Import von Elementen. Wir empfehlen diesen Ansatz für den Import, da Sie dabei die Kontrolle darüber haben, welche Eigenschaften importiert werden. Weitere Informationen zum Festlegen von Eigenschaften für ein Element und das anschließende Speichern des Elements finden Sie unter [Erstellen eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma) bzw. [Erstellen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews).</span><span class="sxs-lookup"><span data-stu-id="f3ed6-p104">Use the [Item.Save](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) EWS Managed API method or the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation to perform the import of items. We recommend this approach when you're importing items from other systems because you have control over which properties get imported. For more information about how to set properties on items and then save the item, see [Create an item by using the EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma) or [Create an item by using EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews).</span></span>
  
## <a name="import-items-with-full-fidelity"></a><span data-ttu-id="f3ed6-133">Importieren von Elementen mit voller Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="f3ed6-133">Import items with full fidelity</span></span>
<span data-ttu-id="f3ed6-134"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="f3ed6-134"></span></span>

<span data-ttu-id="f3ed6-p105">Sie können den EWS-Vorgang [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) zum Hochladen eines Elements als Datenstrom verwenden. Diese Datenstromdarstellung eines Elements muss aus dem Ergebnis eines [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx)-Vorgangsaufrufs kommen. Da der **UploadItems** -Vorgang in der EWS Managed API nicht verfügbar ist, müssen Sie eine Routine zum Versenden der Webanfragen schreiben.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-p105">You can use the [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) EWS operation to upload an item as a data stream. This data stream representation of an item has to come from the results of an [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) operation call. Because the EWS Managed API does not implement the **UploadItems** operation, if you use the EWS Managed API, you'll need to write a routine to send the web requests.</span></span> 
  
<span data-ttu-id="f3ed6-138">Dies ist die einfachste Möglichkeit zum Importieren von Elementen, die von einem anderen Exchange-Server exportiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-138">This is the easiest way to import items that have been exported from another Exchange server.</span></span>
  
<span data-ttu-id="f3ed6-139">Im folgenden Beispiel wurden die IDs und das **Data**-Element zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-139">In the following example, the identifiers and the **Data** element content are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1"/>
  </soap:Header>
  <soap:Body>
    <m:UploadItems>
      <m:Items>
        <t:Item CreateAction="CreateNew">
          <t:ParentFolderId  Id="AAMkADEzOTE7kV0AAA=" ChangeKey="AQAAAA=="/>
          <t:Data>AQAAAAgAAAAAAQAAAAADABZADQASDkANABMO</t:Data>
        </t:Item>
      </m:Items>
    </m:UploadItems>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f3ed6-p106">Der Server antwortet auf die **UploadItems**-Anforderung mit einem [UploadItemsResponse](http://msdn.microsoft.com/library/93044d39-4489-456a-8cce-b6d69873348f%28Office.15%29.aspx)-Element, dass den Wert des Elements [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** enthält. Dadurch wird angezeigt, dass das Element erfolgreich hochgeladen wurde. Die Antwort ist ach in der Element-ID des hochgeladenen Elements enthalten.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-p106">The server responds to the **UploadItems** request with an [UploadItemsResponse](http://msdn.microsoft.com/library/93044d39-4489-456a-8cce-b6d69873348f%28Office.15%29.aspx) element that that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the item was successfully uploaded. The response also includes the item ID of the uploaded item.</span></span> 
  
## <a name="use-the-mime-stream-to-import-from-common-file-formats"></a><span data-ttu-id="f3ed6-142">Verwenden des MIME-Streams zum Import aus gängigen Dateiformaten</span><span class="sxs-lookup"><span data-stu-id="f3ed6-142">Use the MIME stream to import from common file formats</span></span>
<span data-ttu-id="f3ed6-143"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="f3ed6-143"></span></span>

<span data-ttu-id="f3ed6-p107">EWS unterstützt den Import von EML und iCal-Dateien. Sie sollten den MIME-Inhalt sicherheitshalber testen, damit Sie sehen, wie der Exchange-MIME-Parser den Inhalt Ihres MIME-Streams verarbeitet. Obwohl die Verwendung eines MIME-Streams praktisch ist, empfiehlt sich üblicherweise das [Verwenden der EWS Managed API oder von EWS-Elementtypen zum Import eines Elements](#bk_importproperties). Hier finden Sie ein Beispiel für das [Importieren einer vCard](http://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50).</span><span class="sxs-lookup"><span data-stu-id="f3ed6-p107">EWS can import EML (.eml) and iCal (.ics) files. You'll want to test your MIME content to see how the Exchange MIME parser handles the content of your MIME stream. Although using the MIME stream is convenient, it is typically better to [Use EWS Managed API or EWS item types to import an item](#bk_importproperties). Here's an example of how to [import a vCard](http://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50).</span></span>
  
### <a name="use-the-ews-managed-api-to-import-an-email-from-an-eml-file-by-using-the-mime-stream"></a><span data-ttu-id="f3ed6-148">Verwenden der EWS Managed API zum Import einer E-Mail aus einer EML-Datei mithilfe eines MIME-Streams</span><span class="sxs-lookup"><span data-stu-id="f3ed6-148">Use the EWS Managed API to import an email from an EML file by using the MIME stream</span></span>

<span data-ttu-id="f3ed6-p108">Das folgende Beispiel zeigt, wie Sie die [MimeContent](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)-Eigenschaft mit dem Inhalt einer EML-Datei festlegen und die E-Mail anschließend in Ihr Postfach importieren können. Dieses Beispiel zeigt auch, wie Sie die erweiterte Eigenschaft [PidTagMessageFlags (0x0E07)](http://msdn.microsoft.com/de-DE/library/office/cc839733%28v=office.15%29.aspx) einer importierten E-Mail festlegen können, damit sie im Postfach nicht als Entwurf angezeigt wird. Dieses Beispiel setzt voraus, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer sich beim Exchange-Server authentifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-p108">The following example shows how to set the [MimeContent](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property with the contents of an EML file and then import the email into a mailbox. This example also shows how to set the [PidTagMessageFlags (0x0E07)](http://msdn.microsoft.com/de-DE/library/office/cc839733%28v=office.15%29.aspx) extended property on an imported email so that it doesn't appear in the mailbox as a draft item. This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> 
  
```cs
private static void UploadMIMEEmail(ExchangeService service)
{
    EmailMessage email = new EmailMessage(service);
    
    string emlFileName = @"C:\import\email.eml";
    using (FileStream fs = new FileStream(emlFileName, FileMode.Open, FileAccess.Read))
    {
        byte[] bytes = new byte[fs.Length];
        int numBytesToRead = (int)fs.Length;
        int numBytesRead = 0;
        while (numBytesToRead > 0)
        {
            int n = fs.Read(bytes, numBytesRead, numBytesToRead);
            if (n == 0)
                break;
            numBytesRead += n;
            numBytesToRead -= n;
        }
        // Set the contents of the .eml file to the MimeContent property.
        email.MimeContent = new MimeContent("UTF-8", bytes);
    }
    
    // Indicate that this email is not a draft. Otherwise, the email will appear as a 
    // draft to clients.
    ExtendedPropertyDefinition PR_MESSAGE_FLAGS_msgflag_read = new ExtendedPropertyDefinition(3591, MapiPropertyType.Integer);
    email.SetExtendedProperty(PR_MESSAGE_FLAGS_msgflag_read, 1);
    // This results in a CreateItem call to EWS. The email will be saved in the Inbox folder.
    email.Save(WellKnownFolderName.Inbox);
}
```

### <a name="use-the-ews-managed-api-to-import-an-appointment-from-an-ical-file-by-using-the-mime-stream"></a><span data-ttu-id="f3ed6-152">Verwenden der EWS Managed API zum Import eines Termins aus einer iCal-Datei mithilfe eines MIME-Streams</span><span class="sxs-lookup"><span data-stu-id="f3ed6-152">Use the EWS Managed API to import an appointment from an iCal file by using the MIME stream</span></span>

<span data-ttu-id="f3ed6-p109">Sie können einfache Termine aus mithilfe eines MIME-Streams aus iCalendar-Dateien importieren. Sie können allerdings keine Besprechungen importieren. Dabei handelt es sich um Termine mit Teilnehmern. Dem liegt zugrunde, dass die Beziehung zwischen Organisator und Teilnehmern als Teil des Workflows [Exchange-Kalenderfunktion](calendars-and-ews-in-exchange.md) festgelegt werden muss. Teilnehmer können über den MIME-Stream nicht erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-p109">You can import simple appointments in the form of iCalendar files by using the MIME stream. You can't import meetings, which are appointments with attendees, because the relationship between meeting organizers and attendees has to be set as part of the [Exchange calendaring](calendars-and-ews-in-exchange.md) workflow. Attendees cannot be captured in the MIME stream.</span></span> 
  
<span data-ttu-id="f3ed6-156">Im folgenden Codebeispiel wird gezeigt, wie Sie eine einfache ICS-Datei in das Postfach eines Benutzers importieren können.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-156">The following code example shows you how to import a simple .ics file into a user's mailbox.</span></span>
  
```cs
private static void UploadMIMEAppointment(ExchangeService service)
{
    Appointment appointment = new Appointment(service);
    string iCalFileName = @"C:\import\appointment.ics";
    using (FileStream fs = new FileStream(iCalFileName, FileMode.Open, FileAccess.Read))
    {
        byte[] bytes = new byte[fs.Length];
        int numBytesToRead = (int)fs.Length;
        int numBytesRead = 0;
        while (numBytesToRead > 0)
        {
            int n = fs.Read(bytes, numBytesRead, numBytesToRead);
            if (n == 0)
                break;
            numBytesRead += n;
            numBytesToRead -= n;
        }
        // Set the contents of the .ics file to the MimeContent property.
        appointment.MimeContent = new MimeContent("UTF-8", bytes);
    }
    // This results in a CreateItem call to EWS. 
    appointment.Save(WellKnownFolderName.Calendar);
}
```

### <a name="use-ews-to-import-an-item-by-using-the-mime-stream"></a><span data-ttu-id="f3ed6-157">Verwenden von EWS zum Import eines Elements mithilfe eines MIME-Streams</span><span class="sxs-lookup"><span data-stu-id="f3ed6-157">Use EWS to import an item by using the MIME stream</span></span>

<span data-ttu-id="f3ed6-158">Sie können den [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)-Vorgang in EWS zum Import von EML- und iCal-Elementen mithilfe eines MIME-Streams verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3ed6-158">You can use the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation to import EML and iCal items by using their MIME stream.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
    <t:MailboxCulture>en-US</t:MailboxCulture>
  </soap:Header>
  <soap:Body >
    <m:CreateItem>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </m:SavedItemFolderId> 
        <m:Items>
        <t:Message>
          <t:MimeContent CharacterSet="UTF-8">
            <!-- Insert MIME content here-->
          </t:MimeContent>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="next-steps"></a><span data-ttu-id="f3ed6-159">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="f3ed6-159">Next steps</span></span>
<span data-ttu-id="f3ed6-160"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="f3ed6-160"></span></span>

<span data-ttu-id="f3ed6-161">Nachdem Sie Elemente in ein Postfach importieren, möchten Sie möglicherweise eine der folgenden Aufgaben durchführen: [Erstellen eines benutzerdefinierten Ordners zum Speichern der importierten Elemente](how-to-work-with-folders-by-using-ews-in-exchange.md) bzw. [Synchronisieren Ihrer Client- und Postfachserver-Elemente](mailbox-synchronization-and-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="f3ed6-161">After you import items into a mailbox, you might want to [create a custom folder to store your imported items](how-to-work-with-folders-by-using-ews-in-exchange.md), or [synchronize your client and mailbox items](mailbox-synchronization-and-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f3ed6-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3ed6-162">See also</span></span>


- [<span data-ttu-id="f3ed6-163">Exportieren und Importieren von Elementen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f3ed6-163">Exporting and importing items by using EWS in Exchange</span></span>](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="f3ed6-164">Exportieren von Elementen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f3ed6-164">How to: Export items by using EWS in Exchange</span></span>](how-to-export-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="f3ed6-165">Ordner und Elemente in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f3ed6-165">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="f3ed6-166">Postfachsynchronisierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f3ed6-166">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    

