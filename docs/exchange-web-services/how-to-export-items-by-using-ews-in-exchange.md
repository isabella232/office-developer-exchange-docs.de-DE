---
title: Exportieren von Elementen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: e93ee68c-e134-4469-9070-fba404d46cb4
description: Informationen zum Exportieren von Terminen, E-Mails, Kontakten, Aufgaben und anderen Elementen mithilfe der verwalteten EWS-API oder EWS in Exchange.
localization_priority: Priority
ms.openlocfilehash: a01c9487821958b06ec162f2aee27e2d2804eaaf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455884"
---
# <a name="export-items-by-using-ews-in-exchange"></a>Exportieren von Elementen mithilfe von EWS in Exchange

Informationen zum Exportieren von Terminen, E-Mails, Kontakten, Aufgaben und anderen Elementen mithilfe der verwalteten EWS-API oder EWS in Exchange.
  
Sie können Elemente aus Exchange mithilfe der verwalteten EWS-API oder EWS auf unterschiedliche Weise exportieren. Die zu verwendende Option hängt von folgenden Faktoren ab:
  
- Vom exportierten Elementtyp
    
- Vom Genauigkeitsgrad, der zwischen dem Elementzustand in Exchange und dem exportierten Element beibehalten werden soll
    
- Vom Format des exportierten Elements
    
- Von Anforderungen an die Nachbearbeitung
    
- Davon, ob das Element wieder zurück in Exchange importiert werden soll
    
In diesem Artikel wird gezeigt, wie die verschiedenen Optionen zum Exportieren von Elementen verwendet werden. Sie können eine beliebige Option für den Batch-Export von Elementen aus Exchange verwenden.
  
## <a name="export-an-item-into-a-custom-format"></a>Exportieren eines Elements in ein benutzerdefiniertes Format
<a name="bk_exportcustom"> </a>

Sie können die Ergebnisse eines verwalteten [Item.Bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma)-EWS-API-Methodenaufrufs verwenden oder die Ergebnisse eines [GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews)-EWS-Vorgangs in einem Format analysieren, das mit den Anforderungen Ihrer Anwendung funktioniert. Verwenden Sie diese Option, wenn Sie Elemente exportieren, um Sie in eine Datenbank, CSV-Datei, ein anderes Format oder ein anderes System zu importieren. Sie können das Element sogar in Form der Element-EWS-XML speichern. Das kann nützlich sein, da viele Systeme über eine XML-Analysefunktion verfügen. Wir empfehlen Ihnen, die **Item.Bind**-Methode oder den **GetItem**-Vorgang (ohne die [Item.MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)-Eigenschaft) zu verwenden, da Sie anhand dieser Option die Kontrolle darüber haben, welche Eigenschaften exportiert werden. 
  
## <a name="export-items-with-full-fidelity"></a>Exportieren von Elementen mit vollständiger Genauigkeit
<a name="bk_exportfullfidelity"> </a>

Wenn Sie Elemente mit vollständiger Genauigkeit exportieren möchten, können Sie den [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx)-EWS-Vorgang verwenden. Durch den **ExportItems**-Vorgang werden die Elemente als Datenstrom exportiert. Dieser Datenstrom dient nicht zur Analyse, kann jedoch als Sicherung auf Elementebene verwendet werden, die dann zurück in ein Exchange-Postfach importiert werden kann. Sie können viele Elemente in eine **ExportItems**-Anforderung aufnehmen, wir empfehlen jedoch, nicht mehr als 100 Elemente in die einzelnen Aufrufe einzufügen. Da die verwaltete EWS-API den **ExportItems**-Vorgang nicht implementiert, müssen Sie zum Senden der Webanforderungen eine Routine schreiben, wenn sie die verwaltete EWS-API verwenden. Optional können Sie die [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)-Methode verwenden, um Metadaten zu dem Element abzurufen, sodass Sie Informationen zu dem Datenstrom indizieren und speichern können. 
  
Wir empfehlen Ihnen, zum Exportieren von Elementen den **ExportItems**-Vorgang zu verwenden, die Sie anschließend in ein Exchange-Postfach importieren möchten. 
  
Im folgenden Beispiel wird aufgezeigt, wie Sie den **ExportItems**-Vorgang verwenden. In diesem Beispiel wird der Elementbezeichner zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013"/>
  </soap:Header>
  <soap:Body>
    <m:ExportItems>
      <m:ItemIds>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA="/>
      </m:ItemIds>
    </m:ExportItems>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **ExportItems**-Anforderung mit einem [ExportItemsResponse](https://msdn.microsoft.com/library/ef44354b-fbdb-4f7c-b6bd-b27f56a1d018%28Office.15%29.aspx)-Element, das einen [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Elementwert von **NoError** enthält, der angibt, dass das Element erfolgreich exportiert wurde. Die Antwort enthält außerdem die Element-ID des exportierten Elements und den Datenstrom, der die exportierten Inhalte enthält. Im folgenden Beispiel wird der SOAP-Text veranschaulicht, der das exportierte Element enthält.
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:ExportItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
    <m:ResponseMessages>
      <m:ExportItemsResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA=" ChangeKey="FwAAAA=="/>
        <m:Data>
          AQAAAAgAAAAAAAAALgBlAHgAdABlAHMAdAAuAG0AaQBjAHIAbwBzAG8AZgB0AC4A
          cgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUAeAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMA
          bwBmAHQALgBjAG8AbQAAAAMAADkAAAAAAwD+DwYAAAADAARAAwACQAMADkA=
        </m:Data>
      </m:ExportItemsResponseMessage>
     </m:ResponseMessages>
  </m:ExportItemsResponse>
</s:Body>
```

## <a name="use-the-mime-stream-to-export-into-common-file-formats"></a>Verwenden des MIME-Stroms zum Exportieren in gängige Dateiformate
<a name="bk_exportfullfidelity"> </a>

Sie können die verwaltete [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)-EWS-API-Methode oder den [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)-EWS-Vorgang verwenden, um eine MIME-Darstellung eines Elements abzurufen. Da Exchange die MIME-Inhalte der einzelnen Elemente nicht speichert, muss es die Datenbank-Darstellung der einzelnen Elemente in den MIME-Strom konvertieren. Da diese Konvertierung sehr ressourcenintensiv ist, wird nicht empfohlen, den MIME-Strom für viele Elemente anzufordern. Beachten Sie außerdem, dass der MIME-Strom eine begrenzte Anzahl von Eigenschaften enthält; Sie müssen möglicherweise andere Optionen in Betracht ziehen, wenn die Eigenschaftengruppe nicht die erforderlichen Eigenschaften enthält. 
  
### <a name="use-the-ews-managed-api-to-export-an-email-into-an-eml-and-mht-file-by-using-the-mime-stream"></a>Verwenden Sie zum Exportieren einer E-Mail in eine EML- und MHT-Datei die verwaltete EWS-API, indem Sie den MIME-Strom verwenden
<a name="bk_exportemailmime"> </a>

Outlook und andere gängige E-Mail-Anwendungen können das EML-Dateiformat öffnen. Im folgenden Beispiel wird veranschaulicht, wie Sie eine E-Mail mithilfe des MIME-Stroms exportieren können, und den MIME-Strom zum Erstellen einer EML- und MIME-HTML-Datei (MHT) verwenden können. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist, und der Benutzer sich an einem Exchange-Server authentifizieren kann. 
  
```cs
private static void ExportMIMEEmail(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Inbox);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly);
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems(view);
    foreach (var item in results)
    { 
        PropertySet props = new PropertySet(EmailMessageSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = EmailMessage.Bind(service, item.Id, props);
                
        string emlFileName = @"C:\export\email.eml";
        string mhtFileName = @"C:\export\email.mht";
        // Save as .eml.
        using (FileStream fs = new FileStream(emlFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
        // Save as .mht.
        using (FileStream fs = new FileStream(mhtFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

### <a name="use-the-ews-managed-api-to-export-an-appointment-into-an-ical-file-by-using-the-mime-stream"></a>Verwenden der verwalteten EWS-API zum Exportieren eines Termins in eine iCal-Datei mithilfe des MIME-Stroms
<a name="bk_exporticalmime"> </a>

Outlook und andere gängige Kalenderanwendungen können das iCal-Dateiformat (ICS) öffnen. Im folgenden Beispiel wird veranschaulicht, wie ein Termin mithilfe des MIME-Stroms exportiert, und der MIME-Strom zum Erstellen einer iCal-Datei verwendet werden kann. Beachten Sie, dass viele Eigenschaften nicht mit dem MIME-Strom exportiert werden, dazu gehören auch Teilnehmer und anhangsbezogene Eigenschaften. Sie können andere Eigenschaften aus EWS aufnehmen, indem Sie sie anfordern und in der iCal-Datei als private Erweiterungen speichern. Diese privaten Erweiterungen erhalten das Präfix „x-". 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist, und der Benutzer sich an einem Exchange-Server authentifizieren kann. In diesem Beispiel wird außerdem davon ausgegangen, dass Sie einen Termin mit dem Betreff „Finanzplanung 2015" im Kalender-Ordner besitzen. 
  
```cs
private static void ExportMIMEAppointment(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Calendar);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly); 
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems("subject:'2015 Financial Projections'", view);
    foreach (var item in results)
    {
        PropertySet props = new PropertySet(AppointmentSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = Appointment.Bind(service, item.Id, props);
        string iCalFileName = @"C:\export\appointment.ics";
        // Save as .ics.
        using (FileStream fs = new FileStream(iCalFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

### <a name="use-the-ews-managed-api-to-export-a-contact-into-a-vcard-file-by-using-the-mime-stream"></a>Verwenden der verwalteten EWS-API zum Exportieren eines Kontakts in eine vCard-Datei mithilfe des MIME-Stroms
<a name="bk_exportvcardmime"> </a>

Outlook und andere gängige Kontaktverwaltungsanwendungen können das vCard-Dateiformat (VCF) öffnen. Im folgenden Beispiel wird veranschaulicht, wie Sie einen Kontakt mit dem MIME-Strom exportieren, und den MIME-Strom zum Erstellen einer vCard verwenden können. Sie können andere Eigenschaften aus EWS aufnehmen, indem Sie sie anfordern und in der vCard als private Erweiterungen speichern. Diese Erweiterungen erhalten das Präfix „x-". 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist, und der Benutzer sich mit einem Exchange-Server authentifizieren kann. 
  
```cs
private static void ExportMIMEContact(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Contacts);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly);
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems(view);
    foreach (var item in results)
    {
        PropertySet props = new PropertySet(ContactSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = Contact.Bind(service, item.Id, props);
        string vcfFileName = @"C:\export\contact.vcf";
        // Save as .vcf.
        using (FileStream fs = new FileStream(vcfFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

> [!NOTE]
> Sie können vCard-Dateien nicht mithilfe der **MimeContent** -Eigenschaft importieren. Sie können Kontakte mithilfe der verwalteten [Contact.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx)-EWS-API-Methode oder dem [CreateItem](https://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx)-EWS-Vorgang importieren. 
  
### <a name="use-ews-to-export-any-item-by-using-the-mime-stream"></a>Verwenden Sie EWS zum Exportieren eines beliebigen Elements mithilfe des MIME-Stroms
<a name="bk_exportewsmime"> </a>

Verwenden Sie den **GetItem**-Vorgang zum Abrufen des MIME-Stroms eines Elements. In der folgenden **GetItem**-Anforderung wird veranschaulicht, wie der MIME-Inhalt eines Elements angefordert werden kann. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADEzYjJkLTYxMwB8GqYicWAAA=" ChangeKey="CQAAABzXv"/>
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

Im folgenden Beispiel wird die Antwort auf eine Anforderung zum Abrufen des MIME-Stroms veranschaulicht. Der MIME-Strom wurde zur besseren Lesbarkeit gekürzt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="893" 
                         MinorBuildNumber="17" 
                         Version="V2_10" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:MimeContent CharacterSet="UTF-8">UmVjZ6IGZyb2b2suY29y5hMzgwZTA1YtDQo=</t:MimeContent>
              <t:ItemId Id="AAMkADEzYjJkLTYxMwB8GqYicWAAA=" ChangeKey="CQAAABzXv"/>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## 
<a name="bk_exportfullfidelity"> </a>

Nach dem Exportieren von Elementen möchten Sie vielleicht [Elemente in Exchange importieren](how-to-import-items-by-using-ews-in-exchange.md).
  
## <a name="see-also"></a>Siehe auch


- [Exportieren und Importieren von Elementen mithilfe von EWS in Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [Importieren von Elementen mithilfe von EWS in Exchange](how-to-import-items-by-using-ews-in-exchange.md)
    
- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Postfachsynchronisierung und EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    

