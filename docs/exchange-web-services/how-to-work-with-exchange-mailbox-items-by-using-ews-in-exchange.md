---
title: Arbeiten Sie mit Exchange-Postfach-Elementen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 721deb84-f85d-45d0-84c1-0ed55f359969
description: Erfahren Sie, wie Elemente mithilfe der verwalteten EWS-API oder EWS in Exchange erstellt, abgerufen, aktualisiert und gelöscht werden können.
ms.openlocfilehash: e70ac499da57faa60b4bcb6082648b23d1a7e791
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757024"
---
# <a name="work-with-exchange-mailbox-items-by-using-ews-in-exchange"></a>Arbeiten Sie mit Exchange-Postfach-Elementen mithilfe von EWS in Exchange

Erfahren Sie, wie Elemente mithilfe der verwalteten EWS-API oder EWS in Exchange erstellt, abgerufen, aktualisiert und gelöscht werden können.
  
Zum Arbeiten mit Elementen in einem Postfach können Sie mit der verwalteten EWS-API oder EWS arbeiten. Sie können generische Elemente - verwaltete EWS-API-[Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)-Objekte oder EWS [Item](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx)-Typen verwenden, um einige Operationen (Abrufen eines Elements oder Löschen eines Elements mithilfe des Bezeichners des Elements) auszuführen; den Großteil der Zeit müssen Sie jedoch ein [stark typisiertes Element](folders-and-items-in-ews-in-exchange.md#bk_item) verwenden, um eine Abruf- oder Aktualisierungsoperation auszuführen, da Sie Zugriff auf die Eigenschaften benötigen, die spezifisch für das stark typisierte Element sind. 

Sie können beispielsweise kein generisches Element zum Abrufen eines Elements verwenden, das ein Start- und Enddatum aufweist - dazu benötigen Sie ein verwaltetes EWS-API- [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)-Objekt oder einen EWS-[CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)-Typen. Und wenn Sie die verwaltete EWS-API verwenden, müssen Sie immer stark typisierte Elemente erstellen, da die generische **Item** -Klasse keinen Konstruktor aufweist. Wenn Sie mit einem nicht stark typisierten Element arbeiten, können Sie immer die einfache **Item** -Klasse zum Arbeiten mit dem Element verwenden. 
  
**Tabelle 1. Verwaltete EWS-API-Methoden und EWS-Operationen für das Arbeiten mit Elementen**

|**Gewünschte Aktion**|**EWS Managed API-Methode**|**EWS-Operation**|
|:-----|:-----|:-----|
|Erstellen eines generischen Elements  <br/> |Keine. Sie können nur mit der verwalteten EWS-API bestimmte Elementtypen erstellen; Sie können keine generischen Elemente erstellen.  <br/> |[CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
|Abrufen eines Elements  <br/> |[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|Aktualisieren eines Elements  <br/> |[Item.Update](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx) <br/> |[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen eines Elements  <br/> |[Item.Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) <br/> |[DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |
   
In diesem Artikel erfahren Sie, wann Sie die generische Basisklasse verwenden können und wann Sie zum Abschließen der Aufgabe ein stark typisiertes Element benötigen. In den Codebeispielen wird die Verwendung der Basisklasse veranschaulicht, und was Sie tun müssen, wenn Sie die Basisklasse nicht verwenden können oder Sie nicht Ihren Anforderungen entspricht.
  
## <a name="create-an-item-by-using-the-ews-managed-api"></a>Erstellen eines Elements mithilfe der verwalteten EWS-API
<a name="bk_createewsma"> </a>

Die verwaltete EWS-API weist keinen öffentlich verfügbaren Konstruktur für die [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)-Klasse auf, Sie müssen den Konstruktor für den spezifischen Elementtypen verwenden, den Sie erstellen möchten, um ein Element zu erstellen. Verwenden Sie beispielsweise den [EmailMessage-Klassenkonstruktor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) zum Erstellen einer neuen E-Mail-Nachricht, und den [Contact-Klassenkonstruktor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx), um einen neuen Kontakt zu erstellen. Gleichermaßen gibt der Server niemals generische **Item** -Objekte in Antworten zurück; alle generischen Elemente werden als **EmailMessage** -Objekte zurückgegeben. 
  
Wenn Sie den zu erstellenden Elementtypen kennen, können Sie die Aufgabe in wenigen Schritten abschließen. Diese Schritte ähneln sich für alle Elementtypen:
  
1. Initialisieren Sie eine neue Instanz einer der [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)-Klassen mit dem [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt als Parameter. 
    
2. Legen Sie die Eigenschaften des Elements fest. Die Schemas für jeden Elementtyp unterscheiden sich, es sind also unterschiedliche Eigenschaften für die verschiedenen Elemente verfügbar.
    
3. Speichern Sie das Element oder speichern und senden Sie das Element.
    
Sie können beispielsweise ein [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)-Objekt erstellen, die [Subject](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx)-, [Body](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx)- und [ToRecipients](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx)-Eigenschaften festlegen und es dann mithilfe der [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)-Methode senden. 
  
```cs
// Create an email message and provide it with connection 
// configuration information by using an ExchangeService object named service.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.Subject = "Company Soccer Team";
message.Body = "Are you interested in joining?";
message.ToRecipients.Add("sadie@contoso.com");
// Send the email message and save a copy.
// This method call results in a CreateItem call to EWS.
message.SendAndSaveCopy();
```

Gewusst wie: Erstellen Sie eine Besprechung oder einen Termin mithilfe der EWS Managed API finden Sie unter [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).
  
## <a name="create-an-item-by-using-ews"></a>Erstellen eines Elements mithilfe von EWS
<a name="bk_createews"> </a>

Sie können ein generische Element oder ein stark typisierte Element mithilfe von EWS erstellen. Die Schritte sind für alle Elementtypen ähnlich:
  
1. Verwenden Sie die [CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx)-Operation, um ein Element im Exchange-Speicher zu erstellen. 
    
2. Verwenden Sie das [Items](http://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx)-Element, um ein oder mehrere zu erstellende Elemente aufzunehmen. 
    
3. Legen Sie die Eigenschaften des Elements fest.
    
Sie können beispielsweise eine E-Mail-Nachricht erstellen und senden, indem Sie den Code aus dem folgenden Beispiel verwenden. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)-Methode aufrufen. 
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com </t:EmailAddress>
              </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **CreateItem**-Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)-Wert **NoError** umfasst, der angibt, dass die E-Mail erfolgreich erstellt wurde, und die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht enthält. 
  
Wie Sie eine Besprechung oder einen Termin erstellen mithilfe der Exchange-Webdienste finden Sie unter [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).
  
## <a name="get-an-item-by-using-the-ews-managed-api"></a>Abrufen eines Elements mithilfe der verwalteten EWS-API
<a name="bk_getewsma"> </a>

Um ein Element mithilfe der verwalteten EWS-API abzurufen, wenn Sie die [Item.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des abzurufenden Elements kennen, können Sie bei dem Element einfach eine der [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)-Methoden aufrufen, sodass das Element abgerufen wird. Als bewährte Vorgehensweise empfehlen wir die zurückgegebenen Eigenschaften nur auf erforderlichen zu begrenzen. In diesem Beispiel wird die **Id** -Eigenschaft des Elements und die **Subject** -Eigenschaft zurückgegeben. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer an einem Exchange-Server authentifiziert wurde. Die lokale Variable  *itemId*  ist die [ID](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des zu aktualisieren Elements. 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.Subject);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId, propSet);

```

Wenn Sie ein Element suchen, das bestimmte Kriterien erfüllt, gehen Sie folgendermaßen vor:
  
1. Erstellen Sie eine Bindung für den Ordner, der die abzurufenden Elemente enthält.
    
2. Instanziieren Sie ein [SearchFilter.SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) oder ein [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx), um die zurückzugebenden Elemente zu filtern. 
    
3. Instanziieren Sie ein [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx)- oder [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx)-Objekt, um die Anzahl der zurückzugebenden Elemente anzugeben. 
    
4. Rufen Sie die [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)- oder [ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx)-Methode auf. 
    
Wenn Sie beispielsweise ungelesene E-Mail-Nachrichten im Postfach abrufen möchten, verwenden Sie den Code aus dem folgenden Beispiel. In diesem Beispiel wird eine **SearchFilterCollection** zum Begrenzen der Ergebnisse der **FindItems** -Methode für ungelesene Nachrichten verwendet, außerdem wird die **ItemView** eingeschränkt, damit die Ergebnisse auf ein Element begrenzt. Dieser bestimmte Code funktioniert nur mit [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)-Objekten, da der [EmailMessageSchema.IsRead](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx)-Wert Teil des **SearchFilter** ist. 
  
```cs
// Bind the Inbox folder to the service object.
Folder inbox = Folder.Bind(service, WellKnownFolderName.Inbox);
// The search filter to get unread email.
SearchFilter sf = new SearchFilter.SearchFilterCollection(LogicalOperator.And, new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false));
ItemView view = new ItemView(1);
// Fire the query for the unread items.
// This method call results in a FindItem call to EWS.
FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Inbox, sf, view);
```

Alternativ können Sie ein [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) verwenden, um die Ergebnisse der Suche einzuschränken, siehe folgendes Codebeispiel. In diesem Beispiel wird die [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx)-Methode verwendet, um bis zu fünf Termine abzurufen, die in den nächsten 30 Tagen anstehen. Dieser Code funktioniert natürlich nur bei Kalenderelementen. 
  
```cs
// Initialize values for the start and end times, and the number of appointments to retrieve.
DateTime startDate = DateTime.Now;
DateTime endDate = startDate.AddDays(30);
const int NUM_APPTS = 5;
// Bind the Calendar folder to the service object.
// This method call results in a GetFolder call to EWS.
CalendarFolder calendar = CalendarFolder.Bind(service, WellKnownFolderName.Calendar, new PropertySet());
// Set the start and end time and number of appointments to retrieve.
CalendarView cView = new CalendarView(startDate, endDate, NUM_APPTS);
// Limit the properties returned to the appointment's subject, start time, and end time.
cView.PropertySet = new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End);
// Retrieve a collection of appointments by using the calendar view.
// This method call results in a FindAppointments call to EWS.
FindItemsResults<Appointment> appointments = calendar.FindAppointments(cView);
```

Beachten Sie, dass sich die vom Server in der **Bind** -Methodenantwort zurückgegebenen Informationen von denen unterscheiden, die der Server für eine **FindItem** - oder **FindAppointment** -Methodenantwort zurückgibt. Die **Bind** -Methode kann alle schematisierten Eigenschaften zurückgeben, wohingegen die **FindItem** - und **FindAppointment** -Methoden nicht alle schematisierten Eigenschaften zurückgibt. Wenn Sie also vollständigen Zugriff auf das Element benötigen, müssen Sie die **Bind** -Methode verwenden. Wenn Sie das Element **Id** des abzurufenden Elements nicht haben, verwenden Sie die **FindItem** - oder **FindAppointment** -Methoden zum Abrufen der ID, und verwenden Sie dann die **Bind** -Methode, um die erforderlichen Eigenschaften abzurufen. 
  
Wie Sie eine Besprechung oder einen Termin abrufen, indem Sie die EWS Managed API finden Sie unter [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="get-an-item-by-using-ews"></a>Abrufen eines Elements mithilfe von EWS
<a name="bk_getews"> </a>

Wenn Sie die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) des abzurufenden Elements kennen, können Sie das Element mithilfe der [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)-Operation abrufen. 
  
Im folgenden Beispiel wird die XML-Anforderung zum Abrufen des [Betreffs](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) eines Elements mit einer bestimmten **ItemId** veranschaulicht. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API beim Aufrufen der [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)-Methode zu einer **ItemId** sendet. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="GJc/NAAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

Im folgenden Beispiel wird die XML-Antwort veranschaulicht, die der Server zurückgibt, nachdem er die **GetItem**-Operation verarbeitet. Die Antwort gibt an, dass das Element erfolgreich abgerufen wurde. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="GJc/NAAA=" ChangeKey="CQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAGJd9Z"/>
              <t:Subject>Company Soccer Team</t:Subject>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

Wenn Sie die **ItemId** des abzurufenden Elements nicht kennen, können Sie die [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)-Operation verwenden, um das Element zu suchen. Um die **FindItem**-Operation verwenden zu können, müssen Sie zunächst den Ordner identifizieren, den Sie suchen. Sie können den Ordner identifizieren, indem Sie den **DistinguinguishedFolderName** oder die [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) verwenden. Zum Abrufen der erforderlichen [FolderId](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) können Sie die [FindFolder](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)- oder **SyncFolderHierarchy**-Operationen verwenden. Verwenden Sie anschließend die **FindItem**-Operation, um den Ordner nach Ergebnissen zu durchsuchen, die mit dem Suchfilter übereinstimmen. Im Gegensatz zur verwalteten EWS-API bietet EWS keine separate Suchoperation für Termine. Die **FindItem**-Operation ruft Elemente aller Typen ab. 
  
Im folgenden Beispiel wird die XML- **FindItem**-Operationsanforderung veranschaulicht, die an den Server gesendet wird, um Termine im Kalenderordner zu suchen, die in den nächsten 30 Tagen anstehen. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt. 
  
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
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView MaxEntriesReturned="5" StartDate="2013-10-16T17:04:28.722Z" EndDate="2013-11-15T18:04:28.722Z" />
      <m:ParentFolderIds>
        <t:FolderId Id="AAAEOAAA=" ChangeKey="AgAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAAAA3" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **FindItem**-Anforderung mit einer [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx)-Nachricht, die den [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert von **NoError** umfasst, der angibt, dass die Operation erfolgreich abgeschlossen wurde. Falls Kalenderelemente die Filterkriterien erfüllen, sind sie in der Antwort enthalten.
  
Beachten Sie, dass sich die vom Server in der **GetItem**-Operationsantwort zurückgegebenen Informationen von denen unterscheiden, die der Server in einer **FindItem**- oder **FindAppointment**-Operationsantwort zurückgibt. Die **GetItem**-Operation kann alle schematisierten Eigenschaften zurückgeben, wohingegen die **FindItem**- und **FindAppointment**-Operationen nicht alle schematisierten Eigenschaften zurückgeben. Wenn Sie also vollständigen Zugriff auf das Element benötigen, müssen Sie die **GetItem**-Operation verwenden. Wenn Sie die **ItemId** des abzurufenden Elements nicht haben, verwenden Sie die **FindItem**- oder **FindAppointment**-Operationen, um die **ItemId** abzurufen und verwenden Sie anschließend die **GetItem**-Operation zum Abrufen der erforderlichen Elemente. 
  
Eine Besprechung oder einen Termin mithilfe von EWS Abrufen von Informationen finden Sie unter [erhalten Sie Termine und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="update-an-item-by-using-the-ews-managed-api"></a>Aktualisieren eines Elements mithilfe der verwalteten EWS-API
<a name="bk_updateewsma"> </a>

Die Schritte zum Aktualisieren eines Elements mithilfe der verwalteten EWS-API ähneln sich für alle Elementtypen; die Elementeigenschaften für die einzelnen Elementtypen unterscheiden sich jedoch und bei der [Update](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx)-Methode stehen viele überladene Methoden zur Auswahl. So aktualisieren Sie ein Element: 
  
1. Verwenden Sie die [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)-Methode zum Abrufen der aktuellsten Version des Elements, sofern Sie sie nicht bereits haben. Um die Eigenschaften eines bestimmten stark typisierten Elements zu aktualisieren, müssen Sie eine Bindung zu diesem Elementtyp erstellen. Zum Aktualisieren der für einen generischen Elementtyp verfügbaren Eigenschaften können Sie eine Bindung zum [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)-Objekt erstellen. 
    
2. Aktualisieren Sie die Eigenschaften des Elements.
    
3. Rufen Sie die **Update** -Methode auf. 
    
Sie können beispielsweise den Betreff einer E-Mail mithilfe des generischen Elementtyps aktualisieren, wie im Code des folgenden Beispiels dargestellt.
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer an einem Exchange-Server authentifiziert wurde. Die lokale Variable  *itemId*  ist die [ID](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des zu aktualisierenden Elements. 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Update the Subject of the email.
item.Subject = "New subject";
// Save the updated email.
// This method call results in an UpdateItem call to EWS.
item.Update(ConflictResolutionMode.AlwaysOverwrite);
```

Weitere Informationen zu einer Besprechung oder Terminelement aktualisieren, indem Sie die EWS Managed API finden Sie unter [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="update-an-item-by-using-ews"></a>Aktualisieren eines Elements mithilfe von EWS
<a name="bk_updateews"> </a>

Gehen Sie zum Aktualisieren eines Elements mithilfe von EWS folgendermaßen vor:
  
1. Verwenden Sie die [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)-Operation zum Abrufen der aktuellsten Version des Elements, sofern Sie sie nicht bereits haben. 
    
2. Verwenden Sie die [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)-Operation, um die zu aktualisierenden Felder anzugeben und weisen Sie diesen Feldern neue Werte zu. 
    
Im folgenden Beispiel wird die XML- **UpdateItem**-Operationsanforderung veranschaulicht, die an den Server gesendet wird, um den [Betreff](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx)-Wert der E-Mail-Nachricht zu aktualisieren. Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AlwaysOverwrite">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAPdgr" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>New subject</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **UpdateItem**-Anforderung mit einer [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)-Wert von **NoError** umfasst, der angibt, dass die Elementaktualisierung erfolgreich war.
  
Um weitere Informationen zum Aktualisieren von einer Besprechung oder Terminelement mithilfe von EWS finden Sie unter [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="delete-an-item-by-using-the-ews-managed-api"></a>Löschen eines Elements mithilfe der verwalteten EWS-API
<a name="bk_deleteewsma"> </a>

Sie können Elemente löschen, indem Sie sie in den Ordner „Gelöschte Elemente" oder den Papierkorb verschieben. Wenn Sie die [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des zu löschenden Elements kennen, rufen Sie bei dem Element einfach die [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx)-Methode auf. 
  
Gehen Sie folgendermaßen vor, wenn Sie das Element suchen müssen, bevor Sie es löschen:
  
1. Rufen Sie die [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)- oder [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx)-Methode, um nach dem zu löschenden Element zu suchen. 
    
1. Instanziieren Sie ein [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) und begrenzen Sie es auf die zurückzugebenden Eigenschaften oder verwenden Sie eine [SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx), um nach bestimmten Elementen zu suchen. 
    
2. Instanziieren Sie eine [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) oder [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx), um die Anzahl der zurückzugebenden Elemente anzugeben. 
    
2. Rufen Sie die [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx)-Methode auf. 
    
Im folgenden Code wird beispielsweise veranschaulicht, wie eine E-Mail-Nachricht in den Ordner „Gelöschte Elemente" verschoben werden kann.
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer an einem Exchange-Server authentifiziert wurde. Die lokale Variable  *itemId*  ist die [ID](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des zu aktualisierenden Elements. 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Delete the item by moving it to the Deleted Items folder.
// This method call results in a DeleteItem call to EWS.
item.Delete(DeleteMode.MoveToDeletedItems);
```

Weitere Details zum Löschen von Elementen finden Sie unter [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md). Wie Sie eine Besprechung oder einen Termin zu löschen, indem Sie die EWS Managed API finden Sie unter [Löschen Termine und Besprechungen mithilfe von EWS in Exchange Abbrechen](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).
  
## <a name="delete-an-item-by-using-ews"></a>Löschen eines Elements mithilfe von EWS
<a name="bk_deleteews"> </a>

Sie können ein Element mithilfe der [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)-Operation löschen. 
  
Im folgenden Beispiel wird die XML-Anforderung veranschaulicht, die an den Server gesendet wird, um die E-Mail-Nachricht in den Ordner „Gelöschte Elemente" zu verschieben. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteItem DeleteType="MoveToDeletedItems">
      <m:ItemIds>
        <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAANIFzC" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **DeleteItem**-Anforderung mit einer [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)-Wert von **NoError** umfasst, der angibt, dass der Löschvorgang des Elements erfolgreich war.
  
Weitere Details zum Löschen von Elementen finden Sie unter [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md). Wie Sie eine Besprechung oder einen Termin löschen mithilfe der Exchange-Webdienste finden Sie unter [Löschen Termine und Besprechungen mithilfe von EWS in Exchange Abbrechen](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).
  
## <a name="move-or-copy-items-to-another-mailbox"></a>Verschieben oder Kopieren von Elementen in ein anderes Postfach
<a name="bk_movecopybtnmailboxes"> </a>

Sie können Elemente mithilfe der [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx)- und [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx)-Operationen zwischen Postfächern verschieben oder kopieren. Weitere Informationen dazu finden Sie unter [Exportieren und Importieren von Elementen mit EWS in Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md).
  
## <a name="see-also"></a>Siehe auch

- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)    
- [Arbeiten Sie mit Ordnern in Exchange mithilfe der Exchange-Webdienste](how-to-work-with-folders-by-using-ews-in-exchange.md)    
- [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)
    

