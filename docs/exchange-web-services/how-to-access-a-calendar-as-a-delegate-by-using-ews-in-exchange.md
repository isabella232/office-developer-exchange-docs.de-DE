---
title: Zugriff auf einen Kalender als Stellvertretung mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d7db4a1e-9ed6-41da-8529-a73ca285cdf2
description: Hier erfahren Sie, wie Sie einen Kalender als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 609e5f0bb22c78174289a2eb10210999c8391a3d
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353840"
---
#  <a name="access-a-calendar-as-a-delegate-by-using-ews-in-exchange"></a>Zugriff auf einen Kalender als Stellvertretung mithilfe der EWS in Exchange

Hier erfahren Sie, wie Sie einen Kalender als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.
  
Sie können die EWS Managed API verwenden oder EWS so erteilen Sie einen Benutzer delegieren des Zugriffs auf Kalenderordner des Postfachbesitzers. Delegaten kann dann Erstellen von Besprechungsanfragen im Auftrag des Postfachbesitzers, Erstellen von Terminen, Antworten auf Besprechungsanfragen, und abrufen, aktualisieren und Löschen von Besprechungen von der Postfachbesitzer Kalenderordner abhängig von ihren Berechtigungen.
  
Als Stellvertretung verwenden Sie die gleichen Methoden und Vorgänge auf Kalenderordner des Postfachbesitzers zugreifen, mit denen Sie Ihre eigenen Kalenderordner zugreifen. Der Hauptunterschied ist, dass Sie mithilfe von [expliziten Access](delegate-access-and-ews-in-exchange.md#bk_explicit) suchen oder erstellen Sie ein Kalenderelement oder Kalenderunterordner, und klicken Sie dann, nachdem Sie die Element-ID oder Ordner-ID identifiziert haben, können [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) erhalten möchten, aktualisieren und Löschen des Elements. 
  
**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für den Zugriff auf einen Kalender als Stellvertreter**

|**Aktion**|**Verwenden Sie diese Methode EWS Managed API...**|**Verwenden Sie diese Operation EWS...**|
|:-----|:-----|:-----|
|Erstellen einer Besprechung oder eines Termins als Stellvertreter  <br/> |[Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) , in dem der Parameter [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kalenderordner enthält  <br/> |[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers  <br/> |
|Erstellen Sie mehrerer Besprechungen oder Termine als Stellvertreter  <br/> |[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kalenderordner enthält  <br/> |[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers  <br/> |
|Suchen Sie nach oder suchen Sie nach eines Termins oder einer Besprechung als Stellvertreter  <br/> |[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kalenderordner enthält  <br/> |[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers  <br/> |
|Abrufen eines Termins oder einer Besprechung als Stellvertreter  <br/> |[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|Aktualisieren eines Termins oder einer Besprechung als Stellvertreter  <br/> |[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen eines Termins oder einer Besprechung als Stellvertreter  <br/> |[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Appointment.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
> [!NOTE]
> In den Codebeispielen in diesem Artikel ist primary@contoso.com der Postfachbesitzer. 
  
## <a name="prerequisite-tasks"></a>Erforderliche Aufgaben
<a name="bk_prereq"> </a>

Bevor ein Benutzer eine Postfachbesitzer Kalenderordner als Stellvertreter zugreifen kann, muss der Benutzer des Postfachbesitzers Kalenderordner [als Stellvertreter mit Berechtigungen hinzugefügt](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) . 
  
Eine Stellvertretung muss mit einem Postfach verbunden, ihr Konto so aktualisieren Sie den Kalender des Postfachbesitzers haben.
  
Wenn eine Stellvertretung Besprechungsanfragen und-Antworten entwickelt muss nur, können fügen Sie die Stellvertretung in den Ordner Kalender, und Verwenden der Standardwert [MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) EWS Managed API-Enumeration oder die [ DeliverMeetingRequests](http://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) EWS-Elementwert des **DelegatesAndSendInformationToMe** für die Anfragen an die Stellvertreter und informative Nachrichten an den Postfachbesitzer. Die Stellvertretung muss an den Postfachbesitzer Posteingangsordner Zugriff gewährt werden dann nicht. 
  
## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a>Erstellen einer Besprechung oder eines Termins als Stellvertretung mithilfe der EWS Managed API
<a name="bk_createewsma"> </a>

Die EWS Managed API können Sie das Objekt für den Benutzer Delegaten verwenden, um Elemente im Kalender für den Besitzer des Postfachs zu erstellen. In diesem Beispiel wird veranschaulicht, wie mit der [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode erstellen Sie eine Besprechung und Besprechungsanfragen an die Teilnehmer senden. 
  
In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Delegaten und, die die Stellvertretung hat die entsprechenden Berechtigungen für den Postfachbesitzer Kalenderordner gewährt wurde. 
  
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

Beachten Sie, dass beim Speichern des Elements Methodenaufruf [Speichern](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) des Postfachbesitzers Kalenderordner bestimmen muss. Wenn der Postfachbesitzer Kalenderordner nicht angegeben ist, ruft die Besprechungsanfrage der Stellvertretung Kalender und nicht des Postfachbesitzers Kalenderordner gespeichert. Sie können im Methodenaufruf **Speichern** auf zwei Arten der Postfachbesitzer Kalenderordner einschließen. Es wird empfohlen, dass Sie eine neue Instanz des Objekts [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) instanziieren, mithilfe der [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) und die SMTP-Adresse des Postfachbesitzers. 
  
```cs
meeting.Save(new FolderId(WellKnownFolderName.Calendar,
    "primary@contoso.com"), SendInvitationsMode.SendToAllAndSaveCopy);
```

Sie können jedoch auch [gebunden werden](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) in den Ordner Kalender zuerst, und verwenden Sie die ID des Ordners in den Methodenaufruf **zu speichern** . Beachten Sie jedoch, dass dieser einen zusätzlichen EWS-Aufruf erstellt. 
  
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

## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a>Erstellen einer Besprechung oder eines Termins als Stellvertretung mithilfe der Exchange-Webdienste
<a name="bk_createews"> </a>

Exchange-Webdienste können Sie das Objekt für den Benutzer Delegaten verwenden, um Elemente im Kalender für den Besitzer des Postfachs zu erstellen. In diesem Beispiel wird gezeigt, wie mithilfe den [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgang erstellen Sie eine Besprechung und Besprechungsanfragen an die Teilnehmer senden. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Speichern** -Methode zum [Erstellen einer Besprechung oder eines Termins als Stellvertreter](#bk_createewsma)verwenden.
  
SOAP-Header wurde aus dem folgenden Beispiel aus Platzgründen entfernt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
         xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Besprechung erfolgreich erstellt wurde. Die Antwort enthält auch die Element-ID der neu erstellten Besprechung.
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a>Suchen Sie nach einer Besprechung oder eines Termins als Stellvertretung mithilfe der EWS Managed API
<a name="bk_searchewsma"> </a>

Um für eine Besprechung zu suchen, müssen Sie eine der Methoden, die einen [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter enthält [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) verwenden, damit Sie den Postfachbesitzer Kalenderordner angeben können. 
  
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

Nachdem der Anruf **FindItems** eine Antwort mit einer ID zurückgegeben wurde, können erhalten möchten, aktualisiert oder gelöscht werden diese Besprechung mit der ID und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) – und Sie müssen nicht die SMTP-Adresse des Postfachbesitzers angeben. 
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a>Suchen Sie nach einer Besprechung oder eines Termins als Stellvertretung mithilfe der Exchange-Webdienste
<a name="bk_searchews"> </a>

EWS können Sie das Objekt für den Benutzer Delegaten verwenden, für die Suche nach Terminen und Besprechungen, die eine Reihe von Suchkriterien erfüllen. In diesem Beispiel wird veranschaulicht, wie mit den Vorgang [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) finden Besprechungen in der Postfachbesitzer Kalenderordner, die das Wort "building" im Betreff enthalten. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **FindItem** -Methode für die [Suche nach einer Besprechung oder eines Termins als Stellvertreter](#bk_searchewsma)verwenden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die Anforderung **FindItem** mit einer [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) Element **noError zurück**, das anzeigt, dass die Suche erfolgreich abgeschlossen wurde. Die Antwort enthält eine [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) für Termine oder Besprechungen, die die Suchkriterien erfüllen. In diesem Fall wird nur eine Besprechung gefunden. 
  
Der Wert des Elements [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) wurde zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Nun, da Sie die **ItemId** für die Besprechung verfügen, die die Kriterien erfüllt, können Sie abrufen, aktualisieren oder löschen Sie diese Besprechung mithilfe des **ItemId** und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) – und Sie müssen nicht die SMTP-Adresse des Postfachbesitzers angeben. 
  
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-the-ews-managed-api"></a>Erhalten möchten, aktualisieren oder Löschen von Kalenderelementen (engl.) als Stellvertretung mithilfe der EWS Managed API
<a name="bk_geteswma"> </a>

Die EWS Managed API können Sie abrufen, aktualisieren oder Löschen einer Besprechung oder eines Termins in die gleiche Weise, die Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden. Der einzige Unterschied ist, dass das Objekt für den Benutzer Delegat ist. Die Element-ID im Methodenaufruf **binden** enthalten sind, eindeutig identifiziert das Element im Postfachspeicher im Kalenderordner des Postfachbesitzers. 
  
**In Tabelle 2. EWS Managed API-Methoden zum Arbeiten mit Termine und Besprechungen als Stellvertreter**

|**Aufgabe**|**EWS Managed API-Methode**|**Code example**|
|:-----|:-----|:-----|
|Abrufen eines Termins oder einer Besprechung  <br/> |[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[Abrufen eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|Aktualisieren eines Termins oder einer Besprechung  <br/> |[Binden von](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[Aktualisieren einer Besprechung mithilfe der EWS Managed API](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWSMA) <br/> |
|Löschen eines Termins oder einer Besprechung  <br/> |[Binden von](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Löschen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[Löschen einer Besprechung mithilfe der EWS Managed API](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-ews"></a>Erhalten möchten, aktualisieren oder Löschen von Kalenderelementen (engl.) als Stellvertretung mithilfe der Exchange-Webdienste
<a name="bk_getews"> </a>

Exchange-Webdienste können Sie abrufen, aktualisieren oder Löschen einer Besprechung oder eines Termins in die gleiche Weise, die Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden. Der einzige Unterschied ist, dass das Objekt für den Benutzer Delegat ist. Die Element-ID eindeutig enthalten in den Aufruf [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) -Methode identifiziert das Element im Postfachspeicher im Kalenderordner des Postfachbesitzers. 
  
**Tabelle 3. EWS-Vorgänge für die Arbeit mit Termine und Besprechungen als Stellvertreter**

|**Aufgabe**|**EWS-Vorgang**|**Code example**|
|:-----|:-----|:-----|
|Abrufen eines Termins oder einer Besprechung  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[Abrufen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|Aktualisieren eines Termins oder einer Besprechung  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[Aktualisieren einer Besprechung mithilfe der Exchange-Webdienste](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWS) <br/> |
|Löschen eines Termins oder einer Besprechung  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)   
- [Hinzufügen und Entfernen von Stellvertretungen mithilfe von EWS in Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [Legen Sie Berechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) 
- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    

