---
title: Hinzufügen von Anlagen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 0cbce436-2ae6-4fcc-bd8b-f517a0724e55
description: Hier erfahren Sie, wie Sie mit Anlagen neue Elemente erstellen oder vorhandenen Elementen Anlagen mithilfe der verwaltete EWS-API oder EWS in Exchange hinzufügen.
localization_priority: Priority
ms.openlocfilehash: fa98eb437d1289f25cfb827b6fa9b351d842bd40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528265"
---
# <a name="add-attachments-by-using-ews-in-exchange"></a>Hinzufügen von Anlagen mithilfe von EWS in Exchange

Hier erfahren Sie, wie Sie mit Anlagen neue Elemente erstellen oder vorhandenen Elementen Anlagen mithilfe der verwaltete EWS-API oder EWS in Exchange hinzufügen.
  
Sie können neue oder vorhandene Elemente mithilfe der verwaltete EWS-API oder EWS Dateianlagen oder Element Anlagen hinzufügen. Wenn Sie die verwaltete EWS-API verwenden, verwenden Sie die gleiche Methode, um Anlagen zu neuen oder vorhandenen Elementen hinzuzufügen. die Methode ändert sich jedoch, wenn Sie eine Datei oder eine Elementanlage verwenden. Wenn Sie EWS verwenden, verwenden Sie umgekehrt denselben Vorgang, um einem Element entweder eine Datei oder eine Elementanlage hinzuzufügen, aber der Vorgang ändert sich, wenn Sie die Anlage einem neuen oder vorhandenen Element hinzufügen.
  
**Tabelle 1. Verwaltete EWS-API-Methoden und EWS-Operationen für das Hinzufügen von Anlagen**

|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Hinzufügen einer Dateianlage zu einer neuen oder vorhandenen e-Mail  <br/> |[AttachmentCollection. AddFileAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) für eine neue e-Mail  <br/> [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) zum Hinzufügen zu einer vorhandenen e-Mail  <br/> |
|Hinzufügen einer Elementanlage zu einer neuen oder vorhandenen e-Mail  <br/> |[AttachmentCollection. AddItemAttachment](https://msdn.microsoft.com/library/dd634986%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) für eine neue e-Mail  <br/> [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) zum Hinzufügen zu einer vorhandenen e-Mail  <br/> |
   
## <a name="create-an-email-with-file-and-item-attachments-by-using-the-ews-managed-api"></a>Erstellen einer e-Mail mit Datei-und Element Anlagen mithilfe der verwaltete EWS-API
<a name="bk_createattachewsma"> </a>

Das folgende Codebeispiel zeigt, wie Sie eine e-Mail mit mehreren Dateianlagen und einer Elementanlage erstellen: 
  
1. Verwenden des [Email Message](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objekts zum Erstellen einer e-Mail-Nachricht. 
    
2. Verwenden der [AttachmentCollection. AddFileAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) -und [AttachmentCollection. AddItemAttachment](https://msdn.microsoft.com/library/dd634986%28v=exchg.80%29.aspx) -Methoden zum Hinzufügen von Anlagen zur Nachricht. 
    
3. Verwenden der [Email Message. SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) -Methode, um die Nachricht an die Empfänger zu senden und die Nachricht im Ordner "Gesendete Elemente" zu speichern. 
    
Dieses Codebeispiel zeigt die vier Methoden, mit denen eine Dateianlage einem Element mithilfe der verwaltete EWS-API hinzugefügt werden kann:
  
- Mithilfe eines vollqualifizierten Dateispeicherorts.
    
- Mithilfe eines vollqualifizierten Dateispeicherorts und eines neuen Anlagennamens.
    
- Mithilfe eines Bytearrays.
    
- Mithilfe eines Streams.
    
Beachten Sie, dass die Elementanlage in diesem Beispiel gleichzeitig mit der e-Mail-Nachricht erstellt wird. Informationen zum Hinzufügen einer vorhandenen e-Mail-Nachricht als Elementanlage finden Sie unter [Hinzufügen eines vorhandenen Elements zu einer neuen e-Mail mithilfe der MimeContent und der verwaltete EWS-API](#bk_addexistingemailewsma).
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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

## <a name="create-an-email-with-file-and-item-attachments-by-using-ews"></a>Erstellen einer e-Mail mit Datei-und Element Anlagen mithilfe von EWS
<a name="bk_createattachews"> </a>

Im folgenden Codebeispiel wird die Verwendung des [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -Vorgangs zum Erstellen einer e-Mail-Nachricht mit vier Dateianlagen und einer Elementanlage veranschaulicht. Dies ist auch eine der XML-Anforderungen, die vom verwaltete EWS-API gesendet werden, wenn Sie [eine e-Mail mit Datei-und Element Anlagen erstellen](#bk_createattachewsma).
  
Beachten Sie, dass die Elementanlage in diesem Beispiel gleichzeitig mit der e-Mail-Nachricht erstellt wird. Informationen zum Hinzufügen einer vorhandenen e-Mail-Nachricht als Elementanlage finden Sie unter [Hinzufügen eines vorhandenen Elements zu einer neuen e-Mail mithilfe der MimeContent und der verwaltete EWS-API](#bk_addexistingemailewsma).
  
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

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die einen [Response Code](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) -Wert von **noError**enthält, der angibt, dass die e-Mail-und die Anlagen erfolgreich erstellt wurden. Die [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht und die Werte der [Attachments](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) für jede der Anlagen sind ebenfalls in der Antwort enthalten. Die Werte einiger Attribute wurden zur Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

Um [diese neu erstellte Nachricht zu senden](how-to-send-email-messages-by-using-ews-in-exchange.md), rufen Sie den [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang auf. 
  
## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-the-ews-managed-api"></a>Hinzufügen eines vorhandenen Elements zu einer neuen e-Mail-Nachricht mithilfe der MimeContent und der verwaltete EWS-API
<a name="bk_addexistingemailewsma"> </a>

Wenn Sie ein vorhandenes Element als Elementanlage zu einem anderen Element hinzufügen möchten, müssen Sie eine neue Elementanlage erstellen und den Inhalt des vorhandenen Elements in das neue Element kopieren. Sie können auf zwei Arten vorgehen: 
  
1. Wenn Sie speziell mit e-Mail-Nachrichten arbeiten, können Sie den Wert der [MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) -Eigenschaft aus der e-Mail in die neu erstellte Elementanlage kopieren. Während dieses Prozesses gehen einige Eigenschaften verloren, beispielsweise Nachverfolgungskennzeichen und Kategorien, aber es funktioniert gut für Standard-e-Mail-Nachrichten. 
    
2. Wenn Sie eine vollständige Genauigkeit für alle Elementtypen benötigen, können Sie an ein vorhandenes Element binden und alle Eigenschaften und erweiterten Eigenschaften in die neue Anlage kopieren.
    
Im folgenden Codebeispiel wird der erste Ansatz veranschaulicht, indem das **MimeContent** in die neue Elementanlage kopiert wird. Im folgenden Beispiel wird gezeigt, wie Sie den Code so ändern können, dass der zweite Ansatz verwendet wird. 
  
In diesem Beispiel wird davon ausgegangen, dass der **Dienst** ein gültiges [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt ist und dass der Benutzer bei einem Exchange-Server authentifiziert wurde und dass das **ItemID** -Element das [ItemID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) des anzufügenden Elements ist. 
  
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

Führen Sie die folgenden Schritte aus, um dieses Beispiel so zu ändern, dass alle Eigenschaften des vorhandenen Elements in die neue Elementanlage kopiert werden: 
  
1. Ändern Sie den festgelegten Eigenschaftswert in include **PropertySet. FirstClassProperties** und alle zusätzlichen Eigenschaften oder erweiterten Eigenschaften, die Sie benötigen. 
    
  ```cs
  // Add additional properties to the PropertySet.
  EmailMessage msgToAttach = EmailMessage.Bind(service, itemId, new PropertySet(PropertySet.FirstClassProperties));
  ```

2. Entfernen Sie die folgende Verbindung, da Sie die **MimeContent** -Eigenschaft nicht benötigen. 
    
  ```cs
  itemAttachment.Item.MimeContent = msgToAttach.MimeContent;
  ```

3. Wiederholen Sie diese Position für jede Eigenschaft, die aus dem vorhandenen Element in die neue Anlage kopiert werden soll. Kopieren Sie das **ItemID** nicht in die neue Elementanlage, da es sich um eine schreibgeschützte Eigenschaft handelt. 
    
  ```cs
  itemAttachment.Item.Subject = msgToAttach.Subject;
  ```

4. Legen Sie die [PidTagMessageFlags](https://msdn.microsoft.com/library/cc839733.aspx) (0x0E070003)-Eigenschaft für die Anlage auf **sent**fest.
    
  ```cs
  ExtendedPropertyDefinition sent = new ExtendedPropertyDefinition(3591, MapiPropertyType.Integer);
  msgToAttach.Item.SetExtendedProperty(sent, "1");
  ```

## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-ews"></a>Hinzufügen eines vorhandenen Elements zu einer neuen e-Mail-Nachricht mithilfe der MimeContent und EWS
<a name="bk_addexistingemailews"> </a>

Es gibt zwei Möglichkeiten, einem neuen Element ein vorhandenes Element hinzuzufügen: 
  
1. Wenn Sie speziell mit e-Mail-Nachrichten arbeiten, können Sie den Wert des [MimeContent](https://msdn.microsoft.com/library/4f472a08-5653-4c54-ba65-831dfe32f20f%28Office.15%29.aspx) -Elements aus der e-Mail in die neu erstellte Elementanlage kopieren. Während dieses Prozesses gehen einige Eigenschaften verloren, beispielsweise Nachverfolgungskennzeichen und Kategorien, aber es funktioniert gut für Standard-e-Mail-Nachrichten. 
    
2. Wenn Sie eine vollständige Genauigkeit für alle Elementtypen benötigen, können Sie an ein vorhandenes Element binden und alle Eigenschaften und erweiterten Eigenschaften in die neue Anlage kopieren.
    
Im folgenden Codebeispiel wird veranschaulicht, wie das **MimeContent** -Element verwendet wird, um den Inhalt des ursprünglichen Elements in den **MimeContent** -Wert der neuen Elementanlage zu kopieren. Im Beispiel werden die folgenden Vorgänge verwendet: 
  
1. [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) -zum Abrufen des **MimeContent** und des [betreffs](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) der Nachricht, die als Elementanlage für die neue Nachricht verwendet wird. 
    
2. [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) – um die neue e-Mail-Nachricht zu erstellen. 
    
3. [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)– zum Erstellen der neuen Anlage mit dem **MimeContent** und dem **Betreff** , der vom **GetItem** -Vorgang abgerufen wurde. 
    
4. [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) – zum Senden und Speichern der Nachricht. 
    
Das Beispiel beginnt mit dem Abrufen des **MimeContent** und des **betreffs** des vorhandenen Elements. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die **GetItem** -Anforderung mit einer [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) -Wert **noError**enthält, der angibt, dass die e-Mail erfolgreich abgerufen wurde, und **MimeContent** und **Betreff** der e-Mail. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="944"
                         MinorBuildNumber="11"
                         Version="V2_12"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
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

Rufen Sie als nächstes den **CreateItem** -Vorgang auf, um die neue e-Mail zu erstellen. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die einen [Response Code](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) -Wert von **noError**enthält, der angibt, dass die e-Mail erfolgreich erstellt wurde.
  
Erstellen Sie als nächstes die neue Elementanlage mithilfe des **MimeContent** und des **betreffs** , der vom **GetItem** -Vorgang abgerufen wurde. Der Wert des [ParentItemId](https://msdn.microsoft.com/library/72dc4391-72db-44d2-85d9-4718d59886a7%28Office.15%29.aspx) -Elements wird mithilfe des **ItemID** -Werts aufgefüllt, der in der **CreateItem** -Antwort zurückgegeben wird. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die **CreateAttachment** -Anforderung mit einer [CreateAttachmentResponse](https://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) -Wert **noError**enthält, der angibt, dass die Anlage erfolgreich erstellt wurde, und die [Attachment](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) -Nr der neu erstellten Anlage. 
  
Nachdem die neue Nachricht erstellt wurde und das Element angefügt wurde, können Sie [diese neu erstellte Nachricht senden](how-to-send-email-messages-by-using-ews-in-exchange.md) , indem Sie den [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang aufrufen. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die **SendItem**-Anforderung mit einer [SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx)-Nachricht, die den [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert **NoError** enthält, was darauf hinweist, dass die E-Mail erfolgreich gesendet wurde.
  
## <a name="create-an-email-with-an-inline-attachment-by-using-the-ews-managed-api"></a>Erstellen einer e-Mail mit einer Inline Anlage mithilfe der verwaltete EWS-API
<a name="bk_createinlineattachewsma"> </a>

Das folgende Codebeispiel zeigt, wie Sie eine e-Mail mit einer Inline Anlage erstellen:
  
1. Verwenden des [Email Message](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objekts zum Erstellen einer e-Mail-Nachricht. 
    
2. Festlegen der [Email Message. Body](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) -Eigenschaft auf einen HTML-Textkörper, der eine Inline Anlage enthält. 
    
3. Verwenden der [AttachmentCollection. AddFileAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) -Methode zum Hinzufügen der Anlage zur Nachricht. 
    
4. Verwenden der [Email Message. SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) -Methode, um die Nachricht an den Empfänger zu senden und die Nachricht im Ordner "Gesendete Elemente" zu speichern. 
    
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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

## <a name="create-an-email-with-an-inline-attachment-by-using-ews"></a>Erstellen einer e-Mail mit einer Inline Anlage mithilfe von EWS
<a name="bk_createinlineattachewsma"> </a>

Im folgenden Codebeispiel wird die Verwendung des [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -Vorgangs zum Erstellen einer e-Mail-Nachricht mit einer Inlinedatei Anlage veranschaulicht. Das **BodyType** -Attribut des [Body](https://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) -Elements gibt an, dass der Inhalt im HTML-Format vorliegt und die Bildquelle enthält. Dies ist auch eine der XML-Anforderungen, die von der verwaltete EWS-API gesendet werden, wenn Sie die verwaltete EWS-API verwenden, um [eine e-Mail-Nachricht mit einer Inline Anlage zu erstellen](#bk_createinlineattachewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die **CreateItem**-Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)-Wert von **NoError** enthält, der darauf hinweist, dass die E-Mail erfolgreich erstellt wurde. Außerdem ist die [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht enthalten. 
  
Um [diese neu erstellte Nachricht zu senden](how-to-send-email-messages-by-using-ews-in-exchange.md), rufen Sie den [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang auf. 
  
## <a name="add-an-attachment-to-an-existing-email-by-using-the-ews-managed-api"></a>Hinzufügen einer Anlage zu einer vorhandenen e-Mail mithilfe der verwaltete EWS-API
<a name="bk_createinlineattachewsma"> </a>

Im folgenden Codebeispiel wird gezeigt, wie eine Anlage zu einer vorhandenen e-Mail hinzugefügt wird: 
  
1. Verwenden der [Email Message. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) -Methode zum Binden an eine vorhandene e-Mail-Nachricht. 
    
2. Hinzufügen einer Dateianlage zur Nachricht mithilfe der **AddFileAttachment** -Methode. 
    
3. Speichern der Updates durch Aufrufen der [Email Message. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) -Methode. 
    
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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

## <a name="add-an-attachment-to-an-existing-email-by-using-ews"></a>Hinzufügen einer Anlage zu einer vorhandenen e-Mail mithilfe von EWS
<a name="bk_createinlineattachewsma"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie Sie mit dem [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) -Vorgang einer vorhandenen e-Mail-Nachricht eine Dateianlage hinzufügen. Dies ist auch eine der XML-Anforderungen, die von der verwaltete EWS-API gesendet werden, wenn Sie die verwaltete EWS-API verwenden, um eine [Anlage zu einer vorhandenen e-Mail hinzuzufügen](#bk_createinlineattachewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die **CreateAttachment** -Anforderung mit einer [CreateAttachmentResponse](https://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) -Wert **noError**enthält, der angibt, dass die Anlage erfolgreich erstellt wurde, und die [Attachment](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) -Nr der neu erstellten Anlage. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a>Siehe auch


- [Anlagen und EWS in Exchange](attachments-and-ews-in-exchange.md)
    
- [Hinzufügen von Anlagen mithilfe von EWS in Exchange](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [Löschen von Anlagen mithilfe von EWS in Exchange](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
- [Abrufen von Anlagen mithilfe von EWS in Exchange](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [Senden von E-Mail-Nachrichten mit EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

