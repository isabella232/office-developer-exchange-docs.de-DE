---
title: Hinzufügen von Anlagen im Exchange mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0cbce436-2ae6-4fcc-bd8b-f517a0724e55
description: Informationen Sie zum Erstellen neuer Elemente mit Anlagen oder hinzufügen, indem Sie die EWS Managed API oder EWS in Exchange Anlagen in vorhandenen Elementen.
ms.openlocfilehash: dbfff879c92dafeec588d79cddd92e294b763c06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756889"
---
# <a name="add-attachments-by-using-ews-in-exchange"></a><span data-ttu-id="48bcd-103">Hinzufügen von Anlagen im Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="48bcd-103">Add attachments by using EWS in Exchange</span></span>

<span data-ttu-id="48bcd-104">Informationen Sie zum Erstellen neuer Elemente mit Anlagen oder hinzufügen, indem Sie die EWS Managed API oder EWS in Exchange Anlagen in vorhandenen Elementen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-104">Learn how to create new items with attachments, or add attachments to existing items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="48bcd-105">Sie können mithilfe der EWS Managed API oder EWS Dateianlagen oder elementanlagen auf neue oder vorhandene Elemente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-105">You can add file attachments or item attachments to new or existing items by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="48bcd-106">Wenn Sie die EWS Managed API verwenden, verwenden Sie die gleiche Methode Anlagen neue oder vorhandene Elemente hinzu. die Methode ändert sich allerdings, wenn Sie eine Datei oder ein Element eine Anlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="48bcd-106">If you are using the EWS Managed API, you use the same method to add attachments to new or existing items; however, the method changes if you're using a file or item attachment.</span></span> <span data-ttu-id="48bcd-107">Bei Verwendung von EWS umgekehrt, Sie verwenden den gleichen Vorgang aus, um auf eine Datei oder ein Element eine Anlage zu einem Element hinzufügen, aber die Operation geändert wird, wenn Sie die Anlage in ein neues oder vorhandenes Element hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-107">Conversely, if you are using EWS, you use the same operation to add either a file or item attachment to an item, but the operation changes if you're adding the attachment to a new or existing item.</span></span>
  
<span data-ttu-id="48bcd-108">**Tabelle 1. Verwaltete EWS-API-Methoden und EWS-Operationen für das Hinzufügen von Anlagen**</span><span class="sxs-lookup"><span data-stu-id="48bcd-108">**Table 1. EWS Managed API methods and EWS operations for adding attachments**</span></span>

|<span data-ttu-id="48bcd-109">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="48bcd-109">**Task**</span></span>|<span data-ttu-id="48bcd-110">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="48bcd-110">**EWS Managed API method**</span></span>|<span data-ttu-id="48bcd-111">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="48bcd-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="48bcd-112">Fügen Sie eine Dateianlage für eine neue oder vorhandene e-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="48bcd-112">Add a file attachment to a new or existing email</span></span>  <br/> |[<span data-ttu-id="48bcd-113">AttachmentCollection.AddFileAttachment</span><span class="sxs-lookup"><span data-stu-id="48bcd-113">AttachmentCollection.AddFileAttachment</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="48bcd-114">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) für eine neue e-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="48bcd-114">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) for a new email</span></span>  <br/> <span data-ttu-id="48bcd-115">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) hinzufügen zu einer vorhandenen e-Mail</span><span class="sxs-lookup"><span data-stu-id="48bcd-115">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) to add to an existing email</span></span>  <br/> |
|<span data-ttu-id="48bcd-116">Hinzufügen einer Elementanlage auf einer neuen oder vorhandenen e-Mails</span><span class="sxs-lookup"><span data-stu-id="48bcd-116">Add an item attachment to a new or existing email</span></span>  <br/> |[<span data-ttu-id="48bcd-117">AttachmentCollection.AddItemAttachment</span><span class="sxs-lookup"><span data-stu-id="48bcd-117">AttachmentCollection.AddItemAttachment</span></span>](http://msdn.microsoft.com/en-us/library/dd634986%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="48bcd-118">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) für eine neue e-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="48bcd-118">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) for a new email</span></span>  <br/> <span data-ttu-id="48bcd-119">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) hinzufügen zu einer vorhandenen e-Mail</span><span class="sxs-lookup"><span data-stu-id="48bcd-119">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) to add to an existing email</span></span>  <br/> |
   
## <a name="create-an-email-with-file-and-item-attachments-by-using-the-ews-managed-api"></a><span data-ttu-id="48bcd-120">Erstellen Sie eine e-Mail mit Datei und Element Anlagen mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="48bcd-120">Create an email with file and item attachments by using the EWS Managed API</span></span>
<span data-ttu-id="48bcd-121"><a name="bk_createattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="48bcd-121"></span></span>

<span data-ttu-id="48bcd-122">Im folgenden Codebeispiel wird veranschaulicht, wie eine e-Mail mit mehreren Dateianlagen und Elementanlage durch erstellen:</span><span class="sxs-lookup"><span data-stu-id="48bcd-122">The following code example shows how to create an email with multiple file attachments and an item attachment by:</span></span> 
  
1. <span data-ttu-id="48bcd-123">Verwenden die ["EmailMessage"](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objekts, um eine e-Mail-Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-123">Using the [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message.</span></span> 
    
2. <span data-ttu-id="48bcd-124">Mithilfe der [AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) und [AttachmentCollection.AddItemAttachment](http://msdn.microsoft.com/en-us/library/dd634986%28v=exchg.80%29.aspx) Anlagen der Nachricht hinzu.</span><span class="sxs-lookup"><span data-stu-id="48bcd-124">Using the [AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) and [AttachmentCollection.AddItemAttachment](http://msdn.microsoft.com/en-us/library/dd634986%28v=exchg.80%29.aspx) methods to add attachments to the message.</span></span> 
    
3. <span data-ttu-id="48bcd-125">Verwenden die [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) -Methode zum Senden die Nachricht an die Empfänger, und speichern Sie die Nachricht im Ordner "Gesendete Elemente".</span><span class="sxs-lookup"><span data-stu-id="48bcd-125">Using the [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send the message to the recipients and save the message in the Sent Items folder.</span></span> 
    
<span data-ttu-id="48bcd-126">In diesem Codebeispiel wird veranschaulicht, die in dem eine Dateianlage für ein Element hinzugefügt werden kann mithilfe der EWS Managed API vier Arten:</span><span class="sxs-lookup"><span data-stu-id="48bcd-126">This code example shows the four ways in which a file attachment can be added to an item by using the EWS Managed API:</span></span>
  
- <span data-ttu-id="48bcd-127">Durch die Verwendung eines vollqualifizierten Dateispeicherorts an.</span><span class="sxs-lookup"><span data-stu-id="48bcd-127">By using a fully qualified file location.</span></span>
    
- <span data-ttu-id="48bcd-128">Mit einem vollqualifizierten Speicherort und einen neuen Anlagenamen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-128">By using a fully qualified file location and a new attachment name.</span></span>
    
- <span data-ttu-id="48bcd-129">Mithilfe von Bytearray zurück.</span><span class="sxs-lookup"><span data-stu-id="48bcd-129">By using a byte array.</span></span>
    
- <span data-ttu-id="48bcd-130">Mithilfe eines Streams.</span><span class="sxs-lookup"><span data-stu-id="48bcd-130">By using a stream.</span></span>
    
<span data-ttu-id="48bcd-131">Beachten Sie, dass die Anlage Artikel in diesem Beispiel wird zur selben Zeit als e-Mail-Nachricht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="48bcd-131">Note that the item attachment in this example is created at the same time as the email message.</span></span> <span data-ttu-id="48bcd-132">Um eine vorhandene e-Mail-Nachricht als Elementanlage hinzuzufügen, finden Sie unter [Hinzufügen eines vorhandenen Elements zu einer neuen e-Mail mithilfe der ' MimeContent ' und die EWS Managed API](#bk_addexistingemailewsma).</span><span class="sxs-lookup"><span data-stu-id="48bcd-132">To add an existing email message as an item attachment, see [Add an existing item to a new email by using the MimeContent and the EWS Managed API](#bk_addexistingemailewsma).</span></span>
  
<span data-ttu-id="48bcd-133">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="48bcd-133">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void CreateEmailWithAttachments(ExchangeService service)
{
    // Create an email message and set properties on the message.
    EmailMessage message = new EmailMessage(service);
    // Set properties on the email message.
    message.Subject = "Message with Attachments";
    message.Body = "This message contains four file attachments 
        and one message item attachment.";
    message.ToRecipients.Add("sadie@contoso.com");
    message.ToRecipients.Add("ronnie@contoso.com");
    // Add a file attachment by using the fully qualified location of the file. 
    message.Attachments.AddFileAttachment("C:\\temp\\FileAttachment.txt");
    // Add a file attachment by using the fully qualified string name, 
    // and specify the name of the attachment as it will appear in the email.
    // The new name of the file attachment is SecondAttachment.txt.
    message.Attachments.AddFileAttachment("SecondAttachment.txt", "C:\\temp\\FileAttachment2.txt");
    // Add a file attachment by using a byte array.
    // In this example, theBytes is the byte array that represents the content of the image file to attach.
    byte[] theBytes = File.ReadAllBytes("C:\\Temp\\Tulips.jpg");
    // The byte array file attachment is named ThirdAttachment.jpg.
    message.Attachments.AddFileAttachment("ThirdAttachment.jpg", theBytes);
    // Add a file attachment by using a stream.
    FileStream theStream = new FileStream("C:\\temp\\FileAttachment4.txt", FileMode.OpenOrCreate);
    // The streamed file attachment is named FourthAttachment.txt.
    message.Attachments.AddFileAttachment("FourthAttachment.txt", theStream);
    // Add an email message as an item attachment and set properties on the item.
    ItemAttachment<EmailMessage> itemAttachment = message.Attachments.AddItemAttachment<EmailMessage>();
    itemAttachment.Name = "Attached Message Item";
    itemAttachment.Item.Subject = "Message Item Subject";
    itemAttachment.Item.Body = "Message Item Body";
    itemAttachment.Item.ToRecipients.Add("sadie@contoso.com");
    itemAttachment.Item.ToRecipients.Add("ronnie@contoso.com");
    // Send the mail and save a copy in the Sent Items folder.
    // This method results in a CreateItem and SendItem call to EWS.
    message.SendAndSaveCopy();
}
```

## <a name="create-an-email-with-file-and-item-attachments-by-using-ews"></a><span data-ttu-id="48bcd-134">Erstellen Sie eine e-Mail mit Datei und Element Anlagen mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="48bcd-134">Create an email with file and item attachments by using EWS</span></span>
<span data-ttu-id="48bcd-135"><a name="bk_createattachews"> </a></span><span class="sxs-lookup"><span data-stu-id="48bcd-135"></span></span>

<span data-ttu-id="48bcd-136">Im folgenden Codebeispiel wird veranschaulicht, wie mithilfe den [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -Vorgang um mit vier Dateianlagen und ein Element Anlage eine e-Mail-Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-136">The following code example shows how to use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation to create an email message with four file attachments and one item attachment.</span></span> <span data-ttu-id="48bcd-137">Dies ist eine XML-Anforderung, die die EWS Managed API, wenn sendet Sie [eine e-Mail mit der Datei und Element Anlagen erstellen](#bk_createattachewsma).</span><span class="sxs-lookup"><span data-stu-id="48bcd-137">This is also one of the XML requests that the EWS Managed API sends when you [create an email with file and item attachments](#bk_createattachewsma).</span></span>
  
<span data-ttu-id="48bcd-138">Beachten Sie, dass die Anlage Artikel in diesem Beispiel wird zur selben Zeit als e-Mail-Nachricht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="48bcd-138">Note that the item attachment in this example is created at the same time as the email message.</span></span> <span data-ttu-id="48bcd-139">Um eine vorhandene e-Mail-Nachricht als Elementanlage hinzuzufügen, finden Sie unter [Hinzufügen eines vorhandenen Elements zu einer neuen e-Mail mithilfe der ' MimeContent ' und die EWS Managed API](#bk_addexistingemailewsma).</span><span class="sxs-lookup"><span data-stu-id="48bcd-139">To add an existing email message as an item attachment, see [Add an existing item to a new email by using the MimeContent and the EWS Managed API](#bk_addexistingemailewsma).</span></span>
  
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
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:Items>
        <t:Message>
          <t:Subject>Message with Attachments</t:Subject>
          <t:Body BodyType="HTML">This message contains four file attachments 
              and one message item attachment.</t:Body>
          <t:Attachments>
            <t:FileAttachment>
              <t:Name>FileAttachment.txt</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>VGhpcyBpcyBhIGZpbGUgYXR0YWNobWVudC4=</t:Content>
            </t:FileAttachment>
            <t:FileAttachment>
              <t:Name>SecondAttachment.txt</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>VGhpcyBpcyB0aGUgc2Vjb25kIGZpbGUgYXR0YWNobWVudC4=</t:Content>
            </t:FileAttachment>
            <t:FileAttachment>
              <t:Name>ThirdAttachment.jpg</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>nAoAXNIZMVEZs5GKhdzRcLH/9k=</t:Content>
            </t:FileAttachment>
            <t:FileAttachment>
              <t:Name>FourthAttachment.txt</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>obWVudC4=…</t:Content>
            </t:FileAttachment>
            <t:ItemAttachment>
              <t:Name>Attached Message Item</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:Message>
                <t:Subject>Message Item Subject</t:Subject>
                <t:Body BodyType="HTML">Message Item Body</t:Body>
                <t:ToRecipients>
                  <t:Mailbox>
                    <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                  </t:Mailbox>
                  <t:Mailbox>
                    <t:EmailAddress>mack@contoso.com</t:EmailAddress>
                  </t:Mailbox>
                </t:ToRecipients>
              </t:Message>
            </t:ItemAttachment>
          </t:Attachments>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
            <t:Mailbox>
              <t:EmailAddress>ronnie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="48bcd-140">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **noError zurück**, der angibt, dass die e-Mails und Anlagen erfolgreich erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="48bcd-140">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email and the attachments were created successfully.</span></span> <span data-ttu-id="48bcd-141">Die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht und die [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) Werte für die einzelnen Anlagen ist auch in der Antwort enthalten.</span><span class="sxs-lookup"><span data-stu-id="48bcd-141">The [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) values for each of the attachments is also included in the response.</span></span> <span data-ttu-id="48bcd-142">Die Werte der einige Attribute wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="48bcd-142">The values of some attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="upV4AAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXuktU" />
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="6ts3NuI=" />
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="gOIZx1I=" />
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="esRan5I=" />
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="t7sU6s=" />
                </t:FileAttachment>
                <t:ItemAttachment>
                  <t:AttachmentId Id="XgDCggM=" />
                </t:ItemAttachment>
              </t:Attachments>
            </t:Message>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="48bcd-143">[Diese neu erstellte Nachricht senden](how-to-send-email-messages-by-using-ews-in-exchange.md)rufen Sie [den SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="48bcd-143">To [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md), call the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-the-ews-managed-api"></a><span data-ttu-id="48bcd-144">Hinzufügen eines vorhandenen Elements zu einer neuen e-Mail mithilfe der ' MimeContent ' und die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="48bcd-144">Add an existing item to a new email by using the MimeContent and the EWS Managed API</span></span>
<span data-ttu-id="48bcd-145"><a name="bk_addexistingemailewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="48bcd-145"></span></span>

<span data-ttu-id="48bcd-146">Um ein vorhandenes Element als Elementanlage mit einem anderen Element hinzuzufügen, müssen Sie eine neue Anlage Element erstellen, und kopieren Sie den Inhalt des vorhandenen Elements in das neue Element.</span><span class="sxs-lookup"><span data-stu-id="48bcd-146">To add an existing item as an item attachment to another item, you need to create a new item attachment and copy the content of the existing item to the new item.</span></span> <span data-ttu-id="48bcd-147">Es gibt zwei Methoden, um diese Schritte durchführen:</span><span class="sxs-lookup"><span data-stu-id="48bcd-147">There are two ways to do this:</span></span> 
  
1. <span data-ttu-id="48bcd-148">Wenn Sie insbesondere mit e-Mail-Nachrichten arbeiten, können Sie den Wert der Eigenschaft [' MimeContent '](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) aus der e-Mail in die neu erstellte Element Anlage kopieren.</span><span class="sxs-lookup"><span data-stu-id="48bcd-148">If you're working with email messages specifically, you can copy the value of the [MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property from the email into the newly created item attachment.</span></span> <span data-ttu-id="48bcd-149">Verlieren Sie einige Eigenschaften während dieses Vorgangs wie Nachfassen Kennzeichen und Kategorien, aber es eignet sich bestens für standard-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="48bcd-149">You will lose some properties during this process, such as follow up flags and categories, but it works great for standard email messages.</span></span> 
    
2. <span data-ttu-id="48bcd-150">Wenn Sie für alle Elementtypen originalgetreue benötigen, können Sie mit einem vorhandenen Element binden und kopieren Sie alle Eigenschaften und erweiterten Eigenschaften in die neue Anlage.</span><span class="sxs-lookup"><span data-stu-id="48bcd-150">If you need full fidelity for all item types, you can bind to an existing item and copy all the properties and extended properties into the new attachment.</span></span>
    
<span data-ttu-id="48bcd-151">Im folgenden Codebeispiel wird veranschaulicht, den ersten Ansatz, kopieren die **' MimeContent '** in die neue Anlage des Elements.</span><span class="sxs-lookup"><span data-stu-id="48bcd-151">The following code example shows the first approach, copying the **MimeContent** into the new item attachment.</span></span> <span data-ttu-id="48bcd-152">Folgende in diesem Beispiel wird eine Prozedur, die zeigt, wie Sie den Code, um den zweiten Ansatz verwenden ändern können.</span><span class="sxs-lookup"><span data-stu-id="48bcd-152">Following this example is a procedure that shows how you can modify the code to use the second approach.</span></span> 
  
<span data-ttu-id="48bcd-153">In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, das der Benutzer wurde an einen Exchange-Server authentifiziert wurde und, die die **ItemId** [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) des Elements angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="48bcd-153">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server, and that the **itemId** is the [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the item to attach.</span></span> 
  
```cs
public static void CreateEmailExistingItem(ExchangeService service, ItemId itemId)
{        
    // This method results in a GetItem call to EWS.
    EmailMessage msgToAttach = EmailMessage.Bind(service,itemId, 
        new PropertySet(ItemSchema.MimeContent, ItemSchema.Subject));
    // Create an email message and set properties on the message.
    EmailMessage message = new EmailMessage(service);
    message.Subject = "Message with Item Attachment (MimeContent)";
    message.Body = "The attachment to this message was created by copying
        the MimeContent from the original message and adding it to a new item attachment.";
    message.ToRecipients.Add("sadie@contoso.com");
    // Add an email message item attachment and set properties on the item.
    ItemAttachment<EmailMessage> itemAttachment = message.Attachments.AddItemAttachment<EmailMessage>();
    itemAttachment.Item.MimeContent = msgToAttach.MimeContent;
    itemAttachment.Name = msgToAttach.Subject;
    // Send the mail and save a copy in the Sent Items folder.
    // This method results in a CreateItem and SendItem call to EWS.
    message.SendAndSaveCopy();
}
```

<span data-ttu-id="48bcd-154">Führen Sie folgende Schritte aus, um in diesem Beispiel wird um jede der Eigenschaften für das vorhandene Element in das neue Element Anlage kopieren zu ändern:</span><span class="sxs-lookup"><span data-stu-id="48bcd-154">To modify this example to copy each of the properties on the existing item into the new item attachment, do the following:</span></span> 
  
1. <span data-ttu-id="48bcd-155">Ändern Sie den Eigenschaftensatz zu zählen **PropertySet.FirstClassProperties** und zusätzliche Eigenschaften oder erweiterte Eigenschaften, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-155">Change the property set to include **PropertySet.FirstClassProperties** and any additional properties or extended properties you need.</span></span> 
    
  ```cs
  // Add additional properties to the PropertySet.
  EmailMessage msgToAttach = EmailMessage.Bind(service, itemId, new PropertySet(PropertySet.FirstClassProperties));
  ```

2. <span data-ttu-id="48bcd-156">Entfernen Sie die folgende Zeile, da Sie nicht die Eigenschaft **' MimeContent '** benötigen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-156">Remove the following line, because you do not need the **MimeContent** property.</span></span> 
    
  ```cs
  itemAttachment.Item.MimeContent = msgToAttach.MimeContent;
  ```

3. <span data-ttu-id="48bcd-157">Wiederholen Sie diese Zeile für jede Eigenschaft aus das vorhandene Element in die neue Anlage kopiert.</span><span class="sxs-lookup"><span data-stu-id="48bcd-157">Repeat this line for each property to copy from the existing item to the new attachment.</span></span> <span data-ttu-id="48bcd-158">Kopieren Sie die **ItemId** nicht in das neue Element Anlage, da, die eine schreibgeschützte Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="48bcd-158">Do not copy the **ItemId** into the new item attachment because that's a read-only property.</span></span> 
    
  ```cs
  itemAttachment.Item.Subject = msgToAttach.Subject;
  ```

4. <span data-ttu-id="48bcd-159">Legen Sie die [PidTagMessageFlags](http://msdn.microsoft.com/en-us/library/cc839733.aspx) (0x0E070003)-Eigenschaft, auf die Anlage **gesendet**.</span><span class="sxs-lookup"><span data-stu-id="48bcd-159">Set the [PidTagMessageFlags](http://msdn.microsoft.com/en-us/library/cc839733.aspx) (0x0E070003) property on the attachment to **Sent**.</span></span>
    
  ```cs
  ExtendedPropertyDefinition sent = new ExtendedPropertyDefinition(3591, MapiPropertyType.Integer);
  msgToAttach.Item.SetExtendedProperty(sent, "1");
  ```

## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-ews"></a><span data-ttu-id="48bcd-160">Hinzufügen eines vorhandenen Elements zu einer neuen e-Mail mithilfe der ' MimeContent ' und EWS</span><span class="sxs-lookup"><span data-stu-id="48bcd-160">Add an existing item to a new email by using the MimeContent and EWS</span></span>
<span data-ttu-id="48bcd-161"><a name="bk_addexistingemailews"> </a></span><span class="sxs-lookup"><span data-stu-id="48bcd-161"></span></span>

<span data-ttu-id="48bcd-162">Es gibt zwei Methoden, um ein neues Element in ein neues Element hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="48bcd-162">There are two ways to add an existing item to a new item:</span></span> 
  
1. <span data-ttu-id="48bcd-163">Wenn Sie insbesondere mit e-Mail-Nachrichten arbeiten, können Sie den Wert des Elements [' MimeContent '](http://msdn.microsoft.com/library/4f472a08-5653-4c54-ba65-831dfe32f20f%28Office.15%29.aspx) aus der e-Mail in die neu erstellte Element Anlage kopieren.</span><span class="sxs-lookup"><span data-stu-id="48bcd-163">If you're working with email messages specifically, you can copy the value of the [MimeContent](http://msdn.microsoft.com/library/4f472a08-5653-4c54-ba65-831dfe32f20f%28Office.15%29.aspx) element from the email into the newly created item attachment.</span></span> <span data-ttu-id="48bcd-164">Verlieren Sie einige Eigenschaften während dieses Vorgangs wie Nachfassen Kennzeichen und Kategorien, aber es eignet sich bestens für standard-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="48bcd-164">You will lose some properties during this process, such as follow up flags and categories, but it works great for standard email messages.</span></span> 
    
2. <span data-ttu-id="48bcd-165">Wenn Sie für alle Elementtypen originalgetreue benötigen, können Sie mit einem vorhandenen Element binden und kopieren Sie alle Eigenschaften und erweiterten Eigenschaften in die neue Anlage.</span><span class="sxs-lookup"><span data-stu-id="48bcd-165">If you need full fidelity for all item types, you can bind to an existing item and copy all the properties and extended properties into the new attachment.</span></span>
    
<span data-ttu-id="48bcd-166">Im folgenden Codebeispiel wird veranschaulicht, wie das Element **' MimeContent '** verwenden, um den Inhalt des ursprünglichen Elements in der **' MimeContent '** -Wert, der das neue Element Anlage kopieren.</span><span class="sxs-lookup"><span data-stu-id="48bcd-166">The following code example shows how to use the **MimeContent** element to copy the content of the original item into the **MimeContent** value of the new item attachment.</span></span> <span data-ttu-id="48bcd-167">Das Beispiel verwendet die folgenden Vorgänge:</span><span class="sxs-lookup"><span data-stu-id="48bcd-167">The example uses the following operations:</span></span> 
  
1. <span data-ttu-id="48bcd-168">[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) – abrufen, die **' MimeContent '** und den [Betreff](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) der Nachricht, die die Anlage Element auf die neue Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="48bcd-168">[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) — To get the **MimeContent** and [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) of the message that will become the item attachment on the new message.</span></span> 
    
2. <span data-ttu-id="48bcd-169">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) – die neue e-Mail-Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-169">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) — To create the new email message.</span></span> 
    
3. <span data-ttu-id="48bcd-170">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx), um die neue Anlage zu erstellen, mit dem **' MimeContent '** und den **Betreff** mit den **GetItem** Operation abgerufen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-170">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)— To create the new attachment, using the **MimeContent** and **Subject** retrieved by the **GetItem** operation.</span></span> 
    
4. <span data-ttu-id="48bcd-171">[Den SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) – senden, und speichern Sie die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="48bcd-171">[SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) — To send and save the message.</span></span> 
    
<span data-ttu-id="48bcd-172">Das Beispiel startet durch die **' MimeContent '** und den **Betreff** des vorhandenen Elements abrufen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-172">The example starts by retrieving the **MimeContent** and the **Subject** of the existing item.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:MimeContent" />
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="jCrTAAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="48bcd-173">Der Server antwortet mit einer [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) -Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) Wert der **noError zurück**, der angibt, dass die e-Mail-Nachricht erfolgreich abgerufen wurde, und **' MimeContent '** und **enthält die **GetItem** -Anforderung Betreff** der e-Mail.</span><span class="sxs-lookup"><span data-stu-id="48bcd-173">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was retrieved successfully, and the **MimeContent** and **Subject** of the email.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="944"
                         MinorBuildNumber="11"
                         Version="V2_12"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
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
              <t:MimeContent CharacterSet="UTF-8">tDQe/Eo=…</t:MimeContent>
              <t:ItemId Id="jCrTAAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAZi+7u" />
              <t:Subject>Play tennis?</t:Subject>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="48bcd-174">Im nächsten Schritt rufen Sie den **CreateItem** -Vorgang, um die neue e-Mail zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-174">Next, call the **CreateItem** operation to create the new email.</span></span> 
  
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
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:Items>
        <t:Message>
          <t:Subject>Message with Item Attachment (MimeContent)</t:Subject>
          <t:Body BodyType="HTML">The attachment to this message was created by copying the MimeContent from the original message and adding it to a new item attachment.</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>primary@contoso1000.onmicrosoft.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="48bcd-175">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **noError zurück**, der angibt, dass die e-Mail-Nachricht erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="48bcd-175">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully.</span></span>
  
<span data-ttu-id="48bcd-176">Im nächsten Schritt erstellen Sie die neue Element Anlage mithilfe der **' MimeContent '** und **Betreff** mit den **GetItem** Operation abgerufen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-176">Next, create the new item attachment by using the **MimeContent** and **Subject** retrieved by the **GetItem** operation.</span></span> <span data-ttu-id="48bcd-177">Der Wert des [ParentItemId](http://msdn.microsoft.com/library/72dc4391-72db-44d2-85d9-4718d59886a7%28Office.15%29.aspx) -Elements wird mithilfe des in der Antwort **CreateItem** zurückgegebenen **ItemId** -Werts aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="48bcd-177">The value of the [ParentItemId](http://msdn.microsoft.com/library/72dc4391-72db-44d2-85d9-4718d59886a7%28Office.15%29.aspx) element is populated by using the **ItemId** value returned in the **CreateItem** response.</span></span> 
  
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
    <m:CreateAttachment>
      <m:ParentItemId Id="jDKsAAA=" />
      <m:Attachments>
        <t:ItemAttachment>
          <t:Name>Play tennis?</t:Name>
          <t:IsInline>false</t:IsInline>
          <t:Message>
            <t:MimeContent CharacterSet="UTF-8">tDQe/Eo=…</t:MimeContent>
          </t:Message>
        </t:ItemAttachment>
      </m:Attachments>
    </m:CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="48bcd-178">Der Server antwortet mit einer [CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) -Meldung, die den Wert [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **noError zurück**, der angibt, dass die Anlage erfolgreich erstellt wurde, und die [enthält die **CreateAttachment** -Anforderung AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) der neu erstellten Anlage.</span><span class="sxs-lookup"><span data-stu-id="48bcd-178">The server responds to the **CreateAttachment** request with a [CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was created successfully, and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) of the newly created attachment.</span></span> 
  
<span data-ttu-id="48bcd-179">Nun, dass die neue Nachricht erstellt wurde, und das Element zugeordnet wurde, können Sie für [diese neu erstellte Nachricht senden](how-to-send-email-messages-by-using-ews-in-exchange.md) durch Aufrufen von [den SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="48bcd-179">Now that the new message has been created, and the item was attached, you can [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md) by calling the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
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
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="jDKsAAA="
                  ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAZi/q/" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="48bcd-180">Der Server antwortet auf die Anforderung **den SendItem** mit einer [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die e-Mail erfolgreich gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="48bcd-180">The server responds to the **SendItem** request with a [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email was sent successfully.</span></span>
  
## <a name="create-an-email-with-an-inline-attachment-by-using-the-ews-managed-api"></a><span data-ttu-id="48bcd-181">Erstellen Sie eine e-Mail mit Inlineanlage mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="48bcd-181">Create an email with an inline attachment by using the EWS Managed API</span></span>
<span data-ttu-id="48bcd-182"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="48bcd-182"></span></span>

<span data-ttu-id="48bcd-183">Im folgenden Codebeispiel wird veranschaulicht, wie eine e-Mail mit Inlineanlage durch erstellen:</span><span class="sxs-lookup"><span data-stu-id="48bcd-183">The following code example shows how to create an email with an inline attachment by:</span></span>
  
1. <span data-ttu-id="48bcd-184">Verwenden die ["EmailMessage"](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objekts, um eine e-Mail-Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-184">Using the [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message.</span></span> 
    
2. <span data-ttu-id="48bcd-185">Durch Festlegen der [EmailMessage.Body](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) -Eigenschaft auf ein HTML-Textkörper, die eine Inlineanlage enthält.</span><span class="sxs-lookup"><span data-stu-id="48bcd-185">Setting the [EmailMessage.Body](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) property to an HTML body that includes an inline attachment.</span></span> 
    
3. <span data-ttu-id="48bcd-186">Mithilfe der [AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) -Methode die Anlage der Nachricht hinzu.</span><span class="sxs-lookup"><span data-stu-id="48bcd-186">Using the [AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) method to add the attachment to the message.</span></span> 
    
4. <span data-ttu-id="48bcd-187">Verwenden die [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) -Methode zum Senden die Nachricht an den Empfänger aus, und speichern Sie die Nachricht im Ordner "Gesendete Elemente".</span><span class="sxs-lookup"><span data-stu-id="48bcd-187">Using the [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send the message to the recipient and save the message in the Sent Items folder.</span></span> 
    
<span data-ttu-id="48bcd-188">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="48bcd-188">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void CreateEmailWithInlineAttachment(ExchangeService service)
{
    // Create the HTML body with the content identifier of the attachment.
    string html = @"<html>
                        <head>
                        </head>
                        <body>
                        <img width=100 height=100 id=""1"" src=""cid:Party.jpg"">
                        </body>
                        </html>";
         
    // Create the email message.
    EmailMessage message = new EmailMessage(service);
    message.Subject = "Inline Attachment";
    message.Body = new MessageBody(BodyType.HTML, html);
    message.ToRecipients.Add("sadie@contoso.com");
    // Add the attachment to the local copy of the email message.
    string file = @"C:\Temp\Party.jpg";
    message.Attachments.AddFileAttachment("Party.jpg", file);
    message.Attachments[0].IsInline = true;
    message.Attachments[0].ContentId = "Party.jpg";
         
    // Send the mail and save a copy in the Sent Items folder.
    // This method results in a CreateItem and SendItem call to EWS.
    message.SendAndSaveCopy();
}
```

## <a name="create-an-email-with-an-inline-attachment-by-using-ews"></a><span data-ttu-id="48bcd-189">Erstellen Sie eine e-Mail mit Inlineanlage mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="48bcd-189">Create an email with an inline attachment by using EWS</span></span>
<span data-ttu-id="48bcd-190"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="48bcd-190"></span></span>

<span data-ttu-id="48bcd-191">Im folgenden Codebeispiel wird veranschaulicht, wie mithilfe den [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -Vorgang eine e-Mail-Nachricht mit Anlage Datei Inline erstellen.</span><span class="sxs-lookup"><span data-stu-id="48bcd-191">The following code example shows how to use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation to create an email message with an inline file attachment.</span></span> <span data-ttu-id="48bcd-192">Das **BodyType** -Attribut des [Body](http://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) -Elements gibt an, dass der Inhalt in HTML-Format und die Bildquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="48bcd-192">The **BodyType** attribute of the [Body](http://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) element indicates that the content is in HTML format and includes the image source.</span></span> <span data-ttu-id="48bcd-193">Dies ist eine XML-Anforderung, die die EWS Managed API sendet, wenn Sie die EWS Managed API, [Erstellen Sie eine e-Mail mit Inlineanlage](#bk_createinlineattachewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="48bcd-193">This is also one of the XML requests that the EWS Managed API sends when you use the EWS Managed API to [create an email with an inline attachment](#bk_createinlineattachewsma).</span></span>
  
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
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:Items>
        <t:Message>
          <t:Subject>Inline Attachment</t:Subject>
          <t:Body BodyType="HTML">
            &amp;lt;html&amp;gt;
            &amp;lt;head&amp;gt;
            &amp;lt;/head&amp;gt;
            &amp;lt;body&amp;gt;
            &amp;lt;img width=100 height=100 id="1" src="cid:Party.jpg"&amp;gt;
            &amp;lt;/body&amp;gt;
            &amp;lt;/html&amp;gt;
          </t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="48bcd-194">Der Server antwortet auf die **CreateItem**-Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)-Wert **NoError** umfasst, der angibt, dass die E-Mail erfolgreich erstellt wurde, und die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="48bcd-194">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
<span data-ttu-id="48bcd-195">[Diese neu erstellte Nachricht senden](how-to-send-email-messages-by-using-ews-in-exchange.md)rufen Sie [den SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="48bcd-195">To [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md), call the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="add-an-attachment-to-an-existing-email-by-using-the-ews-managed-api"></a><span data-ttu-id="48bcd-196">Hinzufügen einer Anlage zu einer vorhandenen e-Mail mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="48bcd-196">Add an attachment to an existing email by using the EWS Managed API</span></span>
<span data-ttu-id="48bcd-197"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="48bcd-197"></span></span>

<span data-ttu-id="48bcd-198">Im folgenden Codebeispiel wird veranschaulicht, wie eine Anlage zu einer vorhandenen e-Mails durch Hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="48bcd-198">The following code example shows how to add an attachment to an existing email by:</span></span> 
  
1. <span data-ttu-id="48bcd-199">Mithilfe der [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) -Methode um auf eine vorhandene e-Mail-Nachricht zu binden.</span><span class="sxs-lookup"><span data-stu-id="48bcd-199">Using the [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message.</span></span> 
    
2. <span data-ttu-id="48bcd-200">Hinzufügen von eine Dateianlage für die Nachricht mit der **AddFileAttachment** -Methode.</span><span class="sxs-lookup"><span data-stu-id="48bcd-200">Adding a file attachment to the message by using the **AddFileAttachment** method.</span></span> 
    
3. <span data-ttu-id="48bcd-201">Speichern die Updates durch Aufrufen der [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="48bcd-201">Saving the updates by calling the [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="48bcd-202">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="48bcd-202">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```XML
public static void AddAttachmentToExisting(ExchangeService service, ItemId itemId)
{
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId);
    message.Attachments.AddFileAttachment("C:\\temp\\FileAttachment.txt");
    // This method results in a CreateAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="add-an-attachment-to-an-existing-email-by-using-ews"></a><span data-ttu-id="48bcd-203">Hinzufügen einer Anlage zu einer vorhandenen e-Mail mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="48bcd-203">Add an attachment to an existing email by using EWS</span></span>
<span data-ttu-id="48bcd-204"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="48bcd-204"></span></span>

<span data-ttu-id="48bcd-205">Im folgenden Codebeispiel wird veranschaulicht, wie mithilfe des Vorgangs [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) eine Dateianlage für eine vorhandene e-Mail-Nachricht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="48bcd-205">The following code example shows how to use the [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation to add a file attachment to an existing email message.</span></span> <span data-ttu-id="48bcd-206">Dies ist eine XML-Anforderung, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Hinzufügen einer Anlage zu einer vorhandenen e-Mail](#bk_createinlineattachewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="48bcd-206">This is also one of the XML requests that the EWS Managed API sends when you use the EWS Managed API to [add an attachment to an existing email](#bk_createinlineattachewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Central Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateAttachment>
      <m:ParentItemId Id="uqE2AAA=" />
      <m:Attachments>
        <t:FileAttachment>
          <t:Name>FileAttachment.txt</t:Name>
          <t:Content>VGhpcyBpcyBhIGZpbGUgYXR0YWNobWVudC4=</t:Content>
        </t:FileAttachment>
      </m:Attachments>
    </m:CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="48bcd-207">Der Server antwortet mit einer [CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) -Meldung, die den Wert [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **noError zurück**, der angibt, dass die Anlage erfolgreich erstellt wurde, und die [enthält die **CreateAttachment** -Anforderung AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) der neu erstellten Anlage.</span><span class="sxs-lookup"><span data-stu-id="48bcd-207">The server responds to the **CreateAttachment** request with a [CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was created successfully, and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) of the newly created attachment.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="yRLhCh8="
                              RootItemId="uqE2AAA="
                              RootItemChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXulcf" />
            </t:FileAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:CreateAttachmentResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="48bcd-208">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48bcd-208">See also</span></span>


- [<span data-ttu-id="48bcd-209">Attachments and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="48bcd-209">Attachments and EWS in Exchange</span></span>](attachments-and-ews-in-exchange.md)
    
- [<span data-ttu-id="48bcd-210">Hinzufügen von Anlagen im Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="48bcd-210">Add attachments by using EWS in Exchange</span></span>](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="48bcd-211">Löschen von Anlagen mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="48bcd-211">Delete attachments by using EWS in Exchange</span></span>](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="48bcd-212">Abrufen von Anlagen im Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="48bcd-212">Get attachments by using EWS in Exchange</span></span>](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="48bcd-213">Senden von e-Mail-Nachrichten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="48bcd-213">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

