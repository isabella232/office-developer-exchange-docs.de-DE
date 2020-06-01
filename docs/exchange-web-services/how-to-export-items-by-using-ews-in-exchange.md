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
# <a name="export-items-by-using-ews-in-exchange"></a><span data-ttu-id="7e70c-103">Exportieren von Elementen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e70c-103">Export items by using EWS in Exchange</span></span>

<span data-ttu-id="7e70c-104">Informationen zum Exportieren von Terminen, E-Mails, Kontakten, Aufgaben und anderen Elementen mithilfe der verwalteten EWS-API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="7e70c-104">Learn how to export appointments, emails, contacts, tasks, and other items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="7e70c-p101">Sie können Elemente aus Exchange mithilfe der verwalteten EWS-API oder EWS auf unterschiedliche Weise exportieren. Die zu verwendende Option hängt von folgenden Faktoren ab:</span><span class="sxs-lookup"><span data-stu-id="7e70c-p101">You can export items from Exchange by using the EWS Managed API or EWS in a number of different ways. The option you use depends on:</span></span>
  
- <span data-ttu-id="7e70c-107">Vom exportierten Elementtyp</span><span class="sxs-lookup"><span data-stu-id="7e70c-107">The item type that is exported.</span></span>
    
- <span data-ttu-id="7e70c-108">Vom Genauigkeitsgrad, der zwischen dem Elementzustand in Exchange und dem exportierten Element beibehalten werden soll</span><span class="sxs-lookup"><span data-stu-id="7e70c-108">The degree of fidelity that you want maintained between the item state in Exchange and the exported item.</span></span>
    
- <span data-ttu-id="7e70c-109">Vom Format des exportierten Elements</span><span class="sxs-lookup"><span data-stu-id="7e70c-109">The format of the exported item.</span></span>
    
- <span data-ttu-id="7e70c-110">Von Anforderungen an die Nachbearbeitung</span><span class="sxs-lookup"><span data-stu-id="7e70c-110">Any post-processing requirements.</span></span>
    
- <span data-ttu-id="7e70c-111">Davon, ob das Element wieder zurück in Exchange importiert werden soll</span><span class="sxs-lookup"><span data-stu-id="7e70c-111">Whether you want to import the item back into Exchange.</span></span>
    
<span data-ttu-id="7e70c-p102">In diesem Artikel wird gezeigt, wie die verschiedenen Optionen zum Exportieren von Elementen verwendet werden. Sie können eine beliebige Option für den Batch-Export von Elementen aus Exchange verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e70c-p102">This article shows you how to use each of the different options to export items. You can use any option to batch export items out of Exchange.</span></span>
  
## <a name="export-an-item-into-a-custom-format"></a><span data-ttu-id="7e70c-114">Exportieren eines Elements in ein benutzerdefiniertes Format</span><span class="sxs-lookup"><span data-stu-id="7e70c-114">Export an item into a custom format</span></span>
<span data-ttu-id="7e70c-115"><a name="bk_exportcustom"> </a></span><span class="sxs-lookup"><span data-stu-id="7e70c-115"><a name="bk_exportcustom"> </a></span></span>

<span data-ttu-id="7e70c-p103">Sie können die Ergebnisse eines verwalteten [Item.Bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma)-EWS-API-Methodenaufrufs verwenden oder die Ergebnisse eines [GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews)-EWS-Vorgangs in einem Format analysieren, das mit den Anforderungen Ihrer Anwendung funktioniert. Verwenden Sie diese Option, wenn Sie Elemente exportieren, um Sie in eine Datenbank, CSV-Datei, ein anderes Format oder ein anderes System zu importieren. Sie können das Element sogar in Form der Element-EWS-XML speichern. Das kann nützlich sein, da viele Systeme über eine XML-Analysefunktion verfügen. Wir empfehlen Ihnen, die **Item.Bind**-Methode oder den **GetItem**-Vorgang (ohne die [Item.MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)-Eigenschaft) zu verwenden, da Sie anhand dieser Option die Kontrolle darüber haben, welche Eigenschaften exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="7e70c-p103">You can use the results of an [Item.Bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) EWS Managed API method call or parse the results of a [GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) EWS operation into a format that works with your application requirements. Use this option when you are exporting items in order to import them into a database, .csv file, or another format or system. You can even save the item in the form of the item EWS XML, which can be useful because many systems have XML parsing capability. We recommend that you use the **Item.Bind** method or the **GetItem** operation (without the [Item.MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property) because this option gives you control over which properties are exported.</span></span> 
  
## <a name="export-items-with-full-fidelity"></a><span data-ttu-id="7e70c-120">Exportieren von Elementen mit vollständiger Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="7e70c-120">Export items with full fidelity</span></span>
<span data-ttu-id="7e70c-121"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="7e70c-121"><a name="bk_exportfullfidelity"> </a></span></span>

<span data-ttu-id="7e70c-p104">Wenn Sie Elemente mit vollständiger Genauigkeit exportieren möchten, können Sie den [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx)-EWS-Vorgang verwenden. Durch den **ExportItems**-Vorgang werden die Elemente als Datenstrom exportiert. Dieser Datenstrom dient nicht zur Analyse, kann jedoch als Sicherung auf Elementebene verwendet werden, die dann zurück in ein Exchange-Postfach importiert werden kann. Sie können viele Elemente in eine **ExportItems**-Anforderung aufnehmen, wir empfehlen jedoch, nicht mehr als 100 Elemente in die einzelnen Aufrufe einzufügen. Da die verwaltete EWS-API den **ExportItems**-Vorgang nicht implementiert, müssen Sie zum Senden der Webanforderungen eine Routine schreiben, wenn sie die verwaltete EWS-API verwenden. Optional können Sie die [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)-Methode verwenden, um Metadaten zu dem Element abzurufen, sodass Sie Informationen zu dem Datenstrom indizieren und speichern können.</span><span class="sxs-lookup"><span data-stu-id="7e70c-p104">If you want to export items with full fidelity, you can use the [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) EWS operation. The **ExportItems** operation exports each item as a data stream. This data stream is not for parsing, but can be used as an item-level backup that can be imported back into an Exchange mailbox. You can include many items in each **ExportItems** request, although we recommend that you include no more than 100 items in each call. Because the EWS Managed API does not implement the **ExportItems** operation, if you use the EWS Managed API, you'll need to write a routine to send the web requests. You can optionally use the [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method to get metadata about the item so that you can index and store information about the data stream.</span></span> 
  
<span data-ttu-id="7e70c-128">Wir empfehlen Ihnen, zum Exportieren von Elementen den **ExportItems**-Vorgang zu verwenden, die Sie anschließend in ein Exchange-Postfach importieren möchten.</span><span class="sxs-lookup"><span data-stu-id="7e70c-128">We recommend that you use the **ExportItems** operation to export items that you plan to import into an Exchange mailbox.</span></span> 
  
<span data-ttu-id="7e70c-p105">Im folgenden Beispiel wird aufgezeigt, wie Sie den **ExportItems**-Vorgang verwenden. In diesem Beispiel wird der Elementbezeichner zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="7e70c-p105">The following example shows how to use the **ExportItems** operation. In this example, the item identifier is shortened for readability.</span></span> 
  
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

<span data-ttu-id="7e70c-p106">Der Server antwortet auf die **ExportItems**-Anforderung mit einem [ExportItemsResponse](https://msdn.microsoft.com/library/ef44354b-fbdb-4f7c-b6bd-b27f56a1d018%28Office.15%29.aspx)-Element, das einen [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Elementwert von **NoError** enthält, der angibt, dass das Element erfolgreich exportiert wurde. Die Antwort enthält außerdem die Element-ID des exportierten Elements und den Datenstrom, der die exportierten Inhalte enthält. Im folgenden Beispiel wird der SOAP-Text veranschaulicht, der das exportierte Element enthält.</span><span class="sxs-lookup"><span data-stu-id="7e70c-p106">The server responds to the **ExportItems** request with an [ExportItemsResponse](https://msdn.microsoft.com/library/ef44354b-fbdb-4f7c-b6bd-b27f56a1d018%28Office.15%29.aspx) element that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the item was successfully exported. The response also includes the item ID of the exported item and the data stream that contains the exported content. The following example shows the SOAP body that contains the exported item.</span></span>
  
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

## <a name="use-the-mime-stream-to-export-into-common-file-formats"></a><span data-ttu-id="7e70c-134">Verwenden des MIME-Stroms zum Exportieren in gängige Dateiformate</span><span class="sxs-lookup"><span data-stu-id="7e70c-134">Use the MIME stream to export into common file formats</span></span>
<span data-ttu-id="7e70c-135"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="7e70c-135"><a name="bk_exportfullfidelity"> </a></span></span>

<span data-ttu-id="7e70c-p107">Sie können die verwaltete [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)-EWS-API-Methode oder den [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)-EWS-Vorgang verwenden, um eine MIME-Darstellung eines Elements abzurufen. Da Exchange die MIME-Inhalte der einzelnen Elemente nicht speichert, muss es die Datenbank-Darstellung der einzelnen Elemente in den MIME-Strom konvertieren. Da diese Konvertierung sehr ressourcenintensiv ist, wird nicht empfohlen, den MIME-Strom für viele Elemente anzufordern. Beachten Sie außerdem, dass der MIME-Strom eine begrenzte Anzahl von Eigenschaften enthält; Sie müssen möglicherweise andere Optionen in Betracht ziehen, wenn die Eigenschaftengruppe nicht die erforderlichen Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="7e70c-p107">You can use the [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) EWS Managed API method or the [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS operation to get a MIME representation of an item. Because Exchange doesn't store the MIME content of each item, it has to convert the database representation of each item into the MIME stream. Because this conversion is costly, we do not recommend that you request the MIME stream for items on a large scale. Also note that the MIME stream contains a limited set of properties; you might have to consider other options if the property set doesn't contain the properties you need.</span></span> 
  
### <a name="use-the-ews-managed-api-to-export-an-email-into-an-eml-and-mht-file-by-using-the-mime-stream"></a><span data-ttu-id="7e70c-140">Verwenden Sie zum Exportieren einer E-Mail in eine EML- und MHT-Datei die verwaltete EWS-API, indem Sie den MIME-Strom verwenden</span><span class="sxs-lookup"><span data-stu-id="7e70c-140">Use the EWS Managed API to export an email into an .eml and .mht file by using the MIME stream</span></span>
<span data-ttu-id="7e70c-141"><a name="bk_exportemailmime"> </a></span><span class="sxs-lookup"><span data-stu-id="7e70c-141"><a name="bk_exportemailmime"> </a></span></span>

<span data-ttu-id="7e70c-p108">Outlook und andere gängige E-Mail-Anwendungen können das EML-Dateiformat öffnen. Im folgenden Beispiel wird veranschaulicht, wie Sie eine E-Mail mithilfe des MIME-Stroms exportieren können, und den MIME-Strom zum Erstellen einer EML- und MIME-HTML-Datei (MHT) verwenden können. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist, und der Benutzer sich an einem Exchange-Server authentifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="7e70c-p108">Outlook and other common email applications can open the EML (.eml) file format. The following example shows you how you can export an email by using the MIME stream, and use the MIME stream to create an EML and a MIME HTML (.mht) file. Many web browsers support the MIME HTML file format. This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> 
  
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

### <a name="use-the-ews-managed-api-to-export-an-appointment-into-an-ical-file-by-using-the-mime-stream"></a><span data-ttu-id="7e70c-146">Verwenden der verwalteten EWS-API zum Exportieren eines Termins in eine iCal-Datei mithilfe des MIME-Stroms</span><span class="sxs-lookup"><span data-stu-id="7e70c-146">Use the EWS Managed API to export an appointment into an iCal file by using the MIME stream</span></span>
<span data-ttu-id="7e70c-147"><a name="bk_exporticalmime"> </a></span><span class="sxs-lookup"><span data-stu-id="7e70c-147"><a name="bk_exporticalmime"> </a></span></span>

<span data-ttu-id="7e70c-p109">Outlook und andere gängige Kalenderanwendungen können das iCal-Dateiformat (ICS) öffnen. Im folgenden Beispiel wird veranschaulicht, wie ein Termin mithilfe des MIME-Stroms exportiert, und der MIME-Strom zum Erstellen einer iCal-Datei verwendet werden kann. Beachten Sie, dass viele Eigenschaften nicht mit dem MIME-Strom exportiert werden, dazu gehören auch Teilnehmer und anhangsbezogene Eigenschaften. Sie können andere Eigenschaften aus EWS aufnehmen, indem Sie sie anfordern und in der iCal-Datei als private Erweiterungen speichern. Diese privaten Erweiterungen erhalten das Präfix „x-".</span><span class="sxs-lookup"><span data-stu-id="7e70c-p109">Outlook and other common calendar applications can open the iCal (.ics) file format. The following example shows you how to export an appointment by using the MIME stream, and use the MIME stream to create an iCal file. Note that many properties are not exported with the MIME stream, including attendees and attachment-related properties. You can capture other properties from EWS by requesting them and saving them in the iCal file as private extensions. These private extensions are prefixed with "x-".</span></span> 
  
<span data-ttu-id="7e70c-p110">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist, und der Benutzer sich an einem Exchange-Server authentifizieren kann. In diesem Beispiel wird außerdem davon ausgegangen, dass Sie einen Termin mit dem Betreff „Finanzplanung 2015" im Kalender-Ordner besitzen.</span><span class="sxs-lookup"><span data-stu-id="7e70c-p110">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server. This example also assumes that you have an appointment with the subject "2015 Financial Projections" in the calendar folder.</span></span> 
  
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

### <a name="use-the-ews-managed-api-to-export-a-contact-into-a-vcard-file-by-using-the-mime-stream"></a><span data-ttu-id="7e70c-155">Verwenden der verwalteten EWS-API zum Exportieren eines Kontakts in eine vCard-Datei mithilfe des MIME-Stroms</span><span class="sxs-lookup"><span data-stu-id="7e70c-155">Use the EWS Managed API to export a contact into a vCard file by using the MIME stream</span></span>
<span data-ttu-id="7e70c-156"><a name="bk_exportvcardmime"> </a></span><span class="sxs-lookup"><span data-stu-id="7e70c-156"><a name="bk_exportvcardmime"> </a></span></span>

<span data-ttu-id="7e70c-p111">Outlook und andere gängige Kontaktverwaltungsanwendungen können das vCard-Dateiformat (VCF) öffnen. Im folgenden Beispiel wird veranschaulicht, wie Sie einen Kontakt mit dem MIME-Strom exportieren, und den MIME-Strom zum Erstellen einer vCard verwenden können. Sie können andere Eigenschaften aus EWS aufnehmen, indem Sie sie anfordern und in der vCard als private Erweiterungen speichern. Diese Erweiterungen erhalten das Präfix „x-".</span><span class="sxs-lookup"><span data-stu-id="7e70c-p111">Outlook and other common contact management applications can open the vCard (.vcf) file format. The following example shows you how to export a contact by using the MIME stream, and use the MIME stream to create a vCard. You can capture other properties from EWS by requesting them and saving them in the . vCard as private extensions. These extensions are prefixed with "x-".</span></span> 
  
<span data-ttu-id="7e70c-162">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist, und der Benutzer sich mit einem Exchange-Server authentifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="7e70c-162">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> 
  
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
> <span data-ttu-id="7e70c-p112">Sie können vCard-Dateien nicht mithilfe der **MimeContent** -Eigenschaft importieren. Sie können Kontakte mithilfe der verwalteten [Contact.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx)-EWS-API-Methode oder dem [CreateItem](https://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx)-EWS-Vorgang importieren.</span><span class="sxs-lookup"><span data-stu-id="7e70c-p112">You cannot import vCard files by using the **MimeContent** property. You can import contacts by using the [Contact.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) EWS Managed API method or the [CreateItem](https://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) EWS operation.</span></span> 
  
### <a name="use-ews-to-export-any-item-by-using-the-mime-stream"></a><span data-ttu-id="7e70c-165">Verwenden Sie EWS zum Exportieren eines beliebigen Elements mithilfe des MIME-Stroms</span><span class="sxs-lookup"><span data-stu-id="7e70c-165">Use EWS to export any item by using the MIME stream</span></span>
<span data-ttu-id="7e70c-166"><a name="bk_exportewsmime"> </a></span><span class="sxs-lookup"><span data-stu-id="7e70c-166"><a name="bk_exportewsmime"> </a></span></span>

<span data-ttu-id="7e70c-p113">Verwenden Sie den **GetItem**-Vorgang zum Abrufen des MIME-Stroms eines Elements. In der folgenden **GetItem**-Anforderung wird veranschaulicht, wie der MIME-Inhalt eines Elements angefordert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e70c-p113">Use the **GetItem** operation to get the MIME stream of an item. The following **GetItem** request shows how to request the MIME content of an item.</span></span> 
  
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

<span data-ttu-id="7e70c-p114">Im folgenden Beispiel wird die Antwort auf eine Anforderung zum Abrufen des MIME-Stroms veranschaulicht. Der MIME-Strom wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="7e70c-p114">The following example shows the response to a request to get the MIME stream. The MIME stream has been shortened for readability.</span></span>
  
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
<span data-ttu-id="7e70c-171"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="7e70c-171"><a name="bk_exportfullfidelity"> </a></span></span>

<span data-ttu-id="7e70c-172">Nach dem Exportieren von Elementen möchten Sie vielleicht [Elemente in Exchange importieren](how-to-import-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="7e70c-172">After exporting items, you might want to [import items into Exchange](how-to-import-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e70c-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e70c-173">See also</span></span>


- [<span data-ttu-id="7e70c-174">Exportieren und Importieren von Elementen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e70c-174">Exporting and importing items by using EWS in Exchange</span></span>](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7e70c-175">Importieren von Elementen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e70c-175">Import items by using EWS in Exchange</span></span>](how-to-import-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7e70c-176">Ordner und Elemente in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e70c-176">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="7e70c-177">Postfachsynchronisierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e70c-177">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    

