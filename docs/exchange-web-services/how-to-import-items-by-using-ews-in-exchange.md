---
title: Importieren von Elementen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dd3d3221-c98e-4fa0-81f0-77f733d2f432
description: Informationen zum Importieren von Terminen, E-Mails, Kontakten, Aufgaben und anderen Elemente mithilfe der verwalteten EWS-API oder EWS in Exchange.
ms.openlocfilehash: 1e111a03f43c7c6ea30ab0dedf5cc0bb5c6a41f8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513164"
---
# <a name="import-items-by-using-ews-in-exchange"></a>Importieren von Elementen mithilfe von EWS in Exchange

Informationen zum Importieren von Terminen, E-Mails, Kontakten, Aufgaben und anderen Elemente mithilfe der verwalteten EWS-API oder EWS in Exchange.
  
Viele Systeme enthalten Termine, E-Mails, Kontakte und Aufgaben, und Sie können diese Elemente auf verschiedene Arten in Exchange importieren. Das Importieren von Elementen in Exchange ist einfach, wenn für diese Elemente keine Postfachbeziehungen verwaltet werden. Sie können die [Item.Save](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx)-Methode der EWS Managed API oder den [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)-Vorgang in EWS verwenden, um die Elemente in einem Exchange-Postfach zu erstellen. Der einfache Ansatz unterstützt jedoch nicht alle Szenarien. Beispiel: 
  
- Die Beziehung zwischen Organisatoren und Teilnehmer wird nicht beibehalten, wenn Sie Termine mit Teilnehmern (Besprechungen) importieren. Dies bedeutet, dass der Organisator der Besprechung, den Teilnehmern an der Besprechung erneut eine Einladung senden muss, damit die Beziehung zwischen den Organisator und den Teilnehmer wiederhergestellt wird. Wenn der Termin in den Kalender eines Teilnehmers importiert wurde, wird der Termin nicht mit dem Termin des Organisators verknüpft. Die Teilnehmer müssen die aktuellste Besprechungseinladung des Organisators akzeptieren, um die Beziehung zwischen Organisator und Teilnehmer wiederherzustellen.
    
- Informationen zu den Teilnehmern werden nicht beibehalten, wenn zugewiesene Aufgaben importiert werden.
    
Alle Importoptionen können für den Stapelimport von Elementen in Exchange verwendet werden.
  
## <a name="use-ews-managed-api-or-ews-item-types-to-import-an-item"></a>Verwenden der EWS Managed API oder von EWS-Elementtypen zum Import eines Elements
<a name="bk_importproperties"> </a>

Sie können die EWS Managed API oder EWS zum Import von E-Mails, Kontakten, Terminen oder Aufgaben von anderen Systemen verwenden. Stellen Sie die [Eigenschaften ](properties-and-extended-properties-in-ews-in-exchange.md) Ihres Quellformat abhängig vom importierten Element auf einen der folgenden Werte ein. 
  
**Tabelle 1. EWS Managed API-Objekte und EWS-Elemente**

|**EWS Managed API-Objekt**|**EWS-Element**|
|:-----|:-----|
|[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[Contact](https://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[Task](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[Task](https://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
Verwenden Sie die [Item.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx)-Methode der EWS Managed API oder den [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)-Vorgang in EWS zum Import von Elementen. Wir empfehlen diesen Ansatz für den Import, da Sie dabei die Kontrolle darüber haben, welche Eigenschaften importiert werden. Weitere Informationen zum Festlegen von Eigenschaften für ein Element und das anschließende Speichern des Elements finden Sie unter [Erstellen eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma) bzw. [Erstellen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews).
  
## <a name="import-items-with-full-fidelity"></a>Importieren von Elementen mit voller Genauigkeit
<a name="bk_importproperties"> </a>

Sie können den EWS-Vorgang [UploadItems](https://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) zum Hochladen eines Elements als Datenstrom verwenden. Diese Datenstromdarstellung eines Elements muss aus dem Ergebnis eines [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx)-Vorgangsaufrufs kommen. Da der **UploadItems** -Vorgang in der EWS Managed API nicht verfügbar ist, müssen Sie eine Routine zum Versenden der Webanfragen schreiben. 
  
Dies ist die einfachste Möglichkeit zum Importieren von Elementen, die von einem anderen Exchange-Server exportiert wurden.
  
Im folgenden Beispiel wurden die IDs und das **Data**-Element zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Der Server antwortet auf die **UploadItems**-Anforderung mit einem [UploadItemsResponse](https://msdn.microsoft.com/library/93044d39-4489-456a-8cce-b6d69873348f%28Office.15%29.aspx)-Element, dass den Wert des Elements [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** enthält. Dadurch wird angezeigt, dass das Element erfolgreich hochgeladen wurde. Die Antwort ist ach in der Element-ID des hochgeladenen Elements enthalten. 
  
## <a name="use-the-mime-stream-to-import-from-common-file-formats"></a>Verwenden des MIME-Streams zum Import aus gängigen Dateiformaten
<a name="bk_importproperties"> </a>

EWS unterstützt den Import von EML und iCal-Dateien. Sie sollten den MIME-Inhalt sicherheitshalber testen, damit Sie sehen, wie der Exchange-MIME-Parser den Inhalt Ihres MIME-Streams verarbeitet. Obwohl die Verwendung eines MIME-Streams praktisch ist, empfiehlt sich üblicherweise das [Verwenden der EWS Managed API oder von EWS-Elementtypen zum Import eines Elements](#bk_importproperties). Hier finden Sie ein Beispiel für das [Importieren einer vCard](https://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50).
  
### <a name="use-the-ews-managed-api-to-import-an-email-from-an-eml-file-by-using-the-mime-stream"></a>Verwenden der EWS Managed API zum Import einer E-Mail aus einer EML-Datei mithilfe eines MIME-Streams

Das folgende Beispiel zeigt, wie Sie die [MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)-Eigenschaft mit dem Inhalt einer EML-Datei festlegen und die E-Mail anschließend in Ihr Postfach importieren können. Dieses Beispiel zeigt auch, wie Sie die erweiterte Eigenschaft [PidTagMessageFlags (0x0E07)](https://msdn.microsoft.com/library/office/cc839733%28v=office.15%29.aspx) einer importierten E-Mail festlegen können, damit sie im Postfach nicht als Entwurf angezeigt wird. Dieses Beispiel setzt voraus, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer sich beim Exchange-Server authentifizieren kann. 
  
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

### <a name="use-the-ews-managed-api-to-import-an-appointment-from-an-ical-file-by-using-the-mime-stream"></a>Verwenden der EWS Managed API zum Import eines Termins aus einer iCal-Datei mithilfe eines MIME-Streams

Sie können einfache Termine aus mithilfe eines MIME-Streams aus iCalendar-Dateien importieren. Sie können allerdings keine Besprechungen importieren. Dabei handelt es sich um Termine mit Teilnehmern. Dem liegt zugrunde, dass die Beziehung zwischen Organisator und Teilnehmern als Teil des Workflows [Exchange-Kalenderfunktion](calendars-and-ews-in-exchange.md) festgelegt werden muss. Teilnehmer können über den MIME-Stream nicht erfasst werden. 
  
Im folgenden Codebeispiel wird gezeigt, wie Sie eine einfache ICS-Datei in das Postfach eines Benutzers importieren können.
  
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

### <a name="use-ews-to-import-an-item-by-using-the-mime-stream"></a>Verwenden von EWS zum Import eines Elements mithilfe eines MIME-Streams

Sie können den [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)-Vorgang in EWS zum Import von EML- und iCal-Elementen mithilfe eines MIME-Streams verwenden. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="next-steps"></a>Nächste Schritte
<a name="bk_importproperties"> </a>

Nachdem Sie Elemente in ein Postfach importieren, möchten Sie möglicherweise eine der folgenden Aufgaben durchführen: [Erstellen eines benutzerdefinierten Ordners zum Speichern der importierten Elemente](how-to-work-with-folders-by-using-ews-in-exchange.md) bzw. [Synchronisieren Ihrer Client- und Postfachserver-Elemente](mailbox-synchronization-and-ews-in-exchange.md).
  
## <a name="see-also"></a>Siehe auch


- [Exportieren und Importieren von Elementen mithilfe von EWS in Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [Exportieren von Elementen mithilfe von EWS in Exchange](how-to-export-items-by-using-ews-in-exchange.md)
    
- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Postfachsynchronisierung und EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    

