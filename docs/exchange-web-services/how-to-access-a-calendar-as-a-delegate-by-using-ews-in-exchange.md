---
title: Zugriff auf einen Kalender als Delegat mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: d7db4a1e-9ed6-41da-8529-a73ca285cdf2
description: Erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS in Exchange auf einen Kalender als Stellvertreter zugreifen.
localization_priority: Priority
ms.openlocfilehash: 20ec294ddc4ccf014f0b2148c786c8c3ef8a6069
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528293"
---
#  <a name="access-a-calendar-as-a-delegate-by-using-ews-in-exchange"></a>Zugriff auf einen Kalender als Delegat mithilfe der EWS in Exchange

Erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS in Exchange auf einen Kalender als Stellvertreter zugreifen.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um einem Benutzer Stellvertretungszugriff auf den Kalenderordner eines Postfachbesitzers zu gewähren. Der Stellvertreter kann dann Besprechungsanfragen im Auftrag des Postfachbesitzers erstellen, Termine erstellen, Besprechungsanfragen beantworten sowie Besprechungen aus dem Kalenderordner des Postfachbesitzers abhängig von ihren Berechtigungen abrufen, aktualisieren und löschen.
  
Als Stellvertretung verwenden Sie dieselben Methoden und Vorgänge für den Zugriff auf den Kalenderordner eines Postfachbesitzers, den Sie für den Zugriff auf Ihren eigenen Kalenderordner verwenden. Der Hauptunterschied besteht darin, dass Sie [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicit) zum Suchen oder Erstellen eines Kalenderelements oder eines Kalender Unterordners verwenden müssen, und nachdem Sie die Element-ID oder Ordner-ID identifiziert haben, können Sie den [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) zum Abrufen, aktualisieren oder Löschen des Elements verwenden. 
  
**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge für den Zugriff auf einen Kalender als Stellvertretung**

|**Aktion**|**Verwenden Sie diese verwaltete EWS-API-Methode...**|**Verwenden Sie diesen EWS-Vorgang...**|
|:-----|:-----|:-----|
|Erstellen einer Besprechung oder eines Termins als Stellvertreter  <br/> |[Termin. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) , wobei der [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Kalenderordner des Postfachbesitzers ermöglicht  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt  <br/> |
|Erstellen mehrerer Besprechungen oder Termine als Stellvertreter  <br/> |[Datei "ExchangeService. CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , wobei der **Folder** -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Kalenderordner des Postfachbesitzers ermöglicht  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt  <br/> |
|Suchen nach oder suchen nach einem Termin oder einer Besprechung als Stellvertreter  <br/> |[Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , wobei der **Folder** -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Kalenderordner des Postfachbesitzers ermöglicht.  <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt  <br/> |
|Abrufen eines Termins oder einer Besprechung als Stellvertreter  <br/> |[Appointment.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|Aktualisieren eines Termins oder einer Besprechung als Stellvertreter  <br/> |[Termin. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Termin. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen eines Termins oder einer Besprechung als Stellvertreter  <br/> |[Termin. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Termin. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
> [!NOTE]
> In den Codebeispielen in diesem Artikel ist Primary@contoso.com der Postfachbesitzer. 
  
## <a name="prerequisite-tasks"></a>Erforderliche Aufgaben
<a name="bk_prereq"> </a>

Bevor ein Benutzer als Stellvertreter auf den Kalenderordner eines Postfachbesitzers zugreifen kann, muss der Benutzer [als Stellvertreter mit Berechtigungen](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) für den Kalenderordner des Postfachbesitzers hinzugefügt werden. 
  
Eine Stellvertretung muss über ein Postfach verfügen, das Ihrem Konto zugeordnet ist, um den Kalender eines Postfachbesitzers zu aktualisieren.
  
Wenn eine Stellvertretung nur mit Besprechungsanfragen und-Antworten arbeiten muss, können Sie die Stellvertretung dem Kalenderordner hinzufügen und den Standardwert [MeetingRequestsDeliveryScope. DelegatesAndSendInformationToMe](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) verwaltete EWS-API Aufzählungswert oder den [DeliverMeetingRequests](https://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) EWS-Elementwert von **DelegatesAndSendInformationToMe** verwenden, um die Anforderungen an die Stellvertretung und die Informationsmeldungen an den Postfachbesitzer zu senden. Die Stellvertretung muss dann keinen Zugriff auf den Posteingang-Ordner des Postfachbesitzers erhalten. 
  
## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a>Erstellen einer Besprechung oder eines Termins als Stellvertretung mithilfe der verwaltete EWS-API
<a name="bk_createewsma"> </a>

Mit dem verwaltete EWS-API können Sie das Dienstobjekt für den Stellvertreter Benutzer verwenden, um Kalenderelemente für den Postfachbesitzer zu erstellen. In diesem Beispiel wird gezeigt, wie Sie mit der [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode eine Besprechung erstellen und Besprechungsanfragen an die Teilnehmer senden. 
  
In diesem Beispiel wird davon ausgegangen, dass **Service** ein gültiges [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für die Stellvertretung ist und dass der Stellvertretung die entsprechenden Berechtigungen für den Kalenderordner des Postfachbesitzers erteilt wurden. 
  
```cs
private static void DelegateAccessCreateMeeting(ExchangeService service)
{
    Appointment meeting = new Appointment(service);
    // Set the properties on the meeting object to create the meeting.
    meeting.Subject = "Team building exercise";
    meeting.Body = "Let's learn to really work as a team and then have lunch!";
    meeting.Start = DateTime.Now.AddDays(2);
    meeting.End = meeting.Start.AddHours(4);
    meeting.Location = "Conference Room 12";
    meeting.RequiredAttendees.Add("sadie@contoso.com");
    meeting.ReminderMinutesBeforeStart = 60;
    // Save the meeting to the Calendar folder for 
    // the mailbox owner and send the meeting request.
    // This method call results in a CreateItem call to EWS.
    meeting.Save(new FolderId(WellKnownFolderName.Calendar, 
        "primary@contoso.com"), 
        SendInvitationsMode.SendToAllAndSaveCopy);
    // Verify that the meeting was created.
    Item item = Item.Bind(service, meeting.Id, new PropertySet(ItemSchema.Subject));
    Console.WriteLine("\nMeeting created: " + item.Subject + "\n");
}
```

Beachten Sie, dass beim Speichern des Elements der Aufruf der [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode den Kalenderordner des Postfachbesitzers identifizieren muss. Wenn der Kalenderordner des Postfachbesitzers nicht angegeben ist, wird die Besprechungsanfrage im Kalender der Stellvertretung und nicht im Kalenderordner des Postfachbesitzers gespeichert. Sie können den Kalenderordner des Postfachbesitzers in den **Save** -Methodenaufruf auf zwei Arten einschließen. Es wird empfohlen, dass Sie eine neue Instanz des [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Objekts mit dem [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) und der SMTP-Adresse des Postfachbesitzers instanziieren. 
  
```cs
meeting.Save(new FolderId(WellKnownFolderName.Calendar,
    "primary@contoso.com"), SendInvitationsMode.SendToAllAndSaveCopy);
```

Sie können jedoch auch zuerst eine [Bindung](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) an den Ordner Kalender durchführen und dann die ID des Ordners im Aufruf der **Save** -Methode verwenden. Beachten Sie jedoch, dass dadurch ein zusätzlicher EWS-Aufruf erstellt wird. 
  
```cs
    // Identify the mailbox owner's SMTP address
    // and bind to their Calendar folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryCalendar = Folder.Bind(service, 
        new FolderId(WellKnownFolderName.Calendar, primary)); 
…
    // Save the meeting to the Calendar folder for the mailbox owner and send the meeting request.
    meeting.Save(primaryCalendar.Id, 
        SendInvitationsMode.SendToAllAndSaveCopy);
```

## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a>Erstellen einer Besprechung oder eines Termins als Stellvertretung mithilfe von EWS
<a name="bk_createews"> </a>

Mit EWS können Sie das Dienstobjekt für den Delegate-Benutzer verwenden, um Kalenderelemente für den Postfachbesitzer zu erstellen. In diesem Beispiel wird gezeigt, wie Sie mithilfe des [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgangs eine Besprechung erstellen und Besprechungsanfragen an die Teilnehmer senden. 
  
Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die **Save** -Methode verwenden, um [eine Besprechung oder einen Termin als Stellvertreter zu erstellen](#bk_createewsma).
  
Der SOAP-Header wurde aus dem folgenden Beispiel aus Gründen der Kürze entfernt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
         xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
…
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Team building exercise</t:Subject>
          <t:Body BodyType="HTML">Let's learn to really work as a 
              team and then have lunch!</t:Body>
          <t:ReminderMinutesBeforeStart>60</t:ReminderMinutesBeforeStart>
          <t:Start>2014-03-09T23:26:33.756-05:00</t:Start>
          <t:End>2014-03-10T03:26:33.756-05:00</t:End>
          <t:Location>Conference Room 12</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die Besprechung erfolgreich erstellt wurde. Die Antwort enthält auch die Element-ID der neu erstellten Besprechung.
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a>Suchen nach einer Besprechung oder einem Termin als Stellvertretung mithilfe der verwaltete EWS-API
<a name="bk_searchewsma"> </a>

Um nach einer Besprechung zu suchen, müssen Sie eine der [Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methoden verwenden, die einen [foldercode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter enthält, sodass Sie den Kalenderordner des Postfachbesitzers angeben können. 
  
```cs
static void DelegateAccessSearchWithFilter
    (ExchangeService service, SearchFilter filter)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Define the sort order.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching calendar items. 
        // The FindItems parameters must denote the mailbox owner,
        // mailbox, and Calendar folder.
        // This method call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(
        new FolderId(WellKnownFolderName.Calendar, 
            "primary@contoso.com"), 
            filter, 
            view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while 
            enumerating results: {0}", ex.Message);
    }
}
```

Nachdem der **FindItems** -Aufruf eine Antwort mit einer ID zurückgibt, können Sie diese Besprechung abrufen, aktualisieren oder löschen, indem Sie die ID und den [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) verwenden – und Sie müssen die SMTP-Adresse des Postfachbesitzers nicht angeben. 
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a>Suchen nach einer Besprechung oder einem Termin als Stellvertretung mithilfe von EWS
<a name="bk_searchews"> </a>

Mit EWS können Sie das Dienstobjekt für den Stellvertreter-Benutzer verwenden, um nach Terminen und Besprechungen zu suchen, die eine Reihe von Suchkriterien erfüllen. In diesem Beispiel wird gezeigt, wie Sie mithilfe des [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Vorgangs Besprechungen im Kalenderordner des Postfachbesitzers finden, der das Wort "Building" im Betreff enthält. 
  
Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die **FindItem** -Methode verwenden, um [eine Besprechung oder einen Termin als Stellvertreter zu suchen](#bk_searchewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:Restriction>
        <t:Contains ContainmentMode="Substring"
                    ContainmentComparison="IgnoreCase">
          <t:FieldURI FieldURI="item:Subject" />
          <t:Constant Value="building" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **FindItem** -Anforderung mit einer [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die Suche erfolgreich abgeschlossen wurde. Die Antwort enthält ein [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) für alle Termine oder Besprechungen, die die Suchkriterien erfüllen. In diesem Fall wird nur eine Besprechung gefunden. 
  
Der Wert des [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Elements wurde zur Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1"
                        TotalItemsInView="1"
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="IJpUAAA="
                          ChangeKey="DwAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAAAIKhS" />
                <t:Subject>Team building exercise</t:Subject>
                <t:DateTimeReceived>2014-03-04T21:27:22Z</t:DateTimeReceived>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

Nachdem Sie nun die **ItemID** für die Besprechung haben, die Ihre Kriterien erfüllt, können Sie diese Besprechung mit dem **ItemID** -und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) abrufen, aktualisieren oder löschen, und Sie müssen die SMTP-Adresse des Postfachbesitzers nicht angeben. 
  
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-the-ews-managed-api"></a>Abrufen, aktualisieren oder Löschen von Kalenderelementen als Stellvertretung mithilfe der verwaltete EWS-API
<a name="bk_geteswma"> </a>

Sie können die verwaltete EWS-API verwenden, um eine Besprechung oder einen Termin auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie Sie diese Aktionen ausführen, wenn Sie keinen Stellvertretungszugriff verwenden. Der einzige Unterschied besteht darin, dass das Dienstobjekt für den Stellvertreter Benutzer ist. Die im **Bindungs** Methodenaufruf enthaltene Element-ID identifiziert das Element im Postfachspeicher im Kalenderordner des Postfachbesitzers eindeutig. 
  
**Tabelle 2. Verwaltete EWS-API Methoden zum Arbeiten mit Terminen und Besprechungen als Stellvertretung**

|**Aufgabe**|**EWS Managed API-Methode**|**Codebeispiel**|
|:-----|:-----|:-----|
|Abrufen eines Termins oder einer Besprechung  <br/> |[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[Abrufen eines Elements mithilfe der verwaltete EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|Aktualisieren eines Termins oder einer Besprechung  <br/> |[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[Aktualisieren einer Besprechung mithilfe der verwaltete EWS-API](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWSMA) <br/> |
|Löschen eines Termins oder einer Besprechung  <br/> |[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[Löschen einer Besprechung mithilfe der verwaltete EWS-API](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-ews"></a>Abrufen, aktualisieren oder Löschen von Kalenderelementen als Stellvertretung mithilfe von EWS
<a name="bk_getews"> </a>

Sie können EWS verwenden, um eine Besprechung oder einen Termin auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie Sie diese Aktionen ausführen, wenn Sie keinen Stellvertretungszugriff verwenden. Der einzige Unterschied besteht darin, dass das Dienstobjekt für den Stellvertreter Benutzer ist. Die Element-ID, die im [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) -Methodenaufruf enthalten ist, identifiziert das Element im Postfachspeicher im Kalenderordner des Postfachbesitzers eindeutig. 
  
**Tabelle 3. EWS-Vorgänge für das Arbeiten mit Terminen und Besprechungen als Stellvertretung**

|**Aufgabe**|**EWS-Funktion**|**Codebeispiel**|
|:-----|:-----|:-----|
|Abrufen eines Termins oder einer Besprechung  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[Abrufen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|Aktualisieren eines Termins oder einer Besprechung  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[Aktualisieren einer Besprechung mithilfe von EWS](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWS) <br/> |
|Löschen eines Termins oder einer Besprechung  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)   
- [Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) 
- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    

