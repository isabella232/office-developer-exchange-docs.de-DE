---
title: Senden von E-Mail-Nachrichten mit EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 5290fafe-8b51-4275-a27e-baf497fc969c
description: Erfahren Sie mehr darüber, wie Sie mithilfe der EWS Managed API oder mithilfe von EWS in Exchange neue E-Mails oder E-Mail-Nachrichtenentwürfe senden.
localization_priority: Priority
ms.openlocfilehash: b73327cc69db37028c0508af788bf5294e79206a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527726"
---
# <a name="send-email-messages-by-using-ews-in-exchange"></a>Senden von E-Mail-Nachrichten mit EWS in Exchange

Erfahren Sie mehr darüber, wie Sie mithilfe der EWS Managed API oder mithilfe von EWS in Exchange neue E-Mails oder E-Mail-Nachrichtenentwürfe senden.
  
Unabhängig davon, ob Sie die EWS Managed API oder EWS verwenden, können Sie E-Mail-Nachrichten auf zweierlei Weise senden. Sie können entweder eine vorhandene Nachricht senden, z. B. eine Nachricht, die im Ordner „Entwürfe“ gespeichert ist, oder Sie können eine E-Mail in einem Schritt erstellen und senden. Die Methoden und Vorgänge, die Sie verwenden, um die Nachricht zu senden, sind identisch, egal, ob Sie eine Nachricht sofort senden oder ob Sie eine verzögerte Nachricht senden.
  
**Tabelle 1. Methoden der verwalteten EWS-API-Methoden und EWS-Vorgänge zum Senden von E-Mail-Nachrichten**

|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Senden einer neuen E-Mail-Nachricht  <br/> |[EmailMessage.SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Senden einer vorhandenen E-Mail-Nachricht  <br/> |[EmailMessage.Send](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) <br/> |[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) <br/> |
   
## <a name="send-a-new-email-message-by-using-the-ews-managed-api"></a>Senden einer neuen E-Mail-Nachricht mithilfe der EWS Managed API
<a name="bk_sendnewewsma"> </a>

Im folgenden Codebeispiel wird gezeigt, wie Sie das [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)-Objekt zum Erstellen einer E-Mail-Nachricht und die [SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)-Methode zum Senden der Nachricht an den Empfänger und zum Speichern der Nachricht im Ordner „Gesendete Objekte“ verwenden. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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
Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" + message.ToRecipients[0] + "' and saved in the SendItems folder.");
```

## <a name="send-a-new-email-message-by-using-ews"></a>Senden einer neuen E-Mail-Nachricht mit EWS
<a name="bk_sendnewews"> </a>

Im folgenden Codebeispiel wird gezeigt, wie der [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)-Vorgang mit dem**MessageDisposition**-Wert **SendAndSaveCopy** verwendet wird, um eine E-Mail-Nachricht zu erstellen, die Nachricht an den Empfänger zu senden und die Nachricht im Ordner „Gesendete Objekte“ zu speichern. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie [eine neue E-Mail senden](#bk_sendnewewsma).
  
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

Der Server antwortet auf die **CreateItem**-Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)-Wert von **NoError** enthält, der darauf hinweist, dass die E-Mail erfolgreich erstellt wurde. Außerdem ist die [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht enthalten. 
  
## <a name="send-a-draft-email-message-by-using-the-ews-managed-api"></a>Senden einer Entwurfs-E-Mail-Nachricht mithilfe der verwalteten EWS-API
<a name="bk_senddraftewsma"> </a>

Im folgenden Codebeispiel wird gezeigt, wie Sie eine Nachricht senden, die im Ordner „Entwürfe“ gespeichert wurde, wie unter [Erstellen einer E-Mail-Nachricht mithilfe der EWS Managed API](email-and-ews-in-exchange.md#bk_createewsma) gezeigt. Verwenden Sie zunächst die [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)-Methode, um die Nachricht abzurufen, und verwenden Sie dann die [Send](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx)-Methode, um die E-Mail-Nachricht zu senden, wie im folgenden Beispiel gezeigt. Beachten Sie, dass bei dieser Methode die gesendete Nachricht nicht im Ordner „Gesendete Objekte“ gespeichert wird. 
  
In diesem Fall werden die Eigenschaften [EmailMessageSchema.Subject](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemschema.subject%28v=exchg.80%29.aspx) und [EmailMessageSchema.ToRecipients](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessageschema.torecipients%28v=exchg.80%29.aspx) dem [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) hinzugefügt, damit die Werte in die Konsolenausgabe eingeschlossen werden können. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
```cs
// As a best practice, create a property set that limits the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ToRecipients);
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, propSet);
// Send the email message.
// This method call results in a SendItem call to EWS.
message.Send();
Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" + message.ToRecipients[0] + "'.");
```

## <a name="send-a-draft-email-message-by-using-ews"></a>Senden einer Entwurfs-E-Mail-Nachricht mithilfe von EWS
<a name="bk_senddraftews"> </a>

Die folgenden Codebeispiele zeigen, wie Sie eine Nachricht, die zuvor im Ordner „Entwürfe“ gespeichert wurde, wie unter [Erstellen einer E-Mail-Nachricht mithilfe von EWS](email-and-ews-in-exchange.md#bk_createews) gezeigt. Verwenden Sie zunächst den Vorgang [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx), um die zu sendende E-Mail-Nachricht abzurufen. Verwenden Sie dann den Vorgang [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx), um die E-Mail-Nachricht an Empfänger zu senden und im Ordner „Gesendete Elemente“ zu speichern. 
  
Die erste Nachricht, die **GetItem**-Anforderungsnachricht, gibt die [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) des Entwurfs für die Bindung an, und die Elemente im [ItemShape](https://msdn.microsoft.com/library/c5604161-bbc0-40bc-ad75-ff7e837d745f%28Office.15%29.aspx)-Element beschränken die Ergebnisse so, dass sie in die **GetItem**-Antwort eingeschlossen werden können. Das **ItemShape**-Element weist die [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) **IdOnly** auf, und das [AdditionalProperties](https://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx)-Element umfasst die [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx)-Werte für die **Subject**-Eigenschaft aus dem Item-Schema und die **ToRecipients**-Eigenschaft aus dem Message-Schema, was bedeutet, dass nur die Elemente **ItemId**, [Subject](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) und [ToRecipients](https://msdn.microsoft.com/library/72dc3be8-30bb-4ae1-acf4-fb94ff490631%28Office.15%29.aspx) in der Antwort an den Client zurückgegeben werden. Weitere Informationen zur Einschränkung der in Aufrufen zurückgegebenen Werte und zur Bedeutung des **BaseShape**-Elements finden Sie unter [Eigenschaftensätze und Antwortshapes in EWS in Exchange](property-sets-and-response-shapes-in-ews-in-exchange.md).
  
Dies ist auch die XML-Anforderung, die von der verwalteten EWS-API gesendet wird, wenn die [bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)-Methode aufgerufen wird. Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt. 
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="message:ToRecipients" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADE4=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt die XML-Antwort, die der Server zurückgibt, nachdem der **GetItem**-Vorgang verarbeitet wurde. Die Antwort weist darauf hin, dass die E-Mail-Nachricht erfolgreich abgerufen wurde, und enthält, wie angefordert, die Elemente **Subject** und **ToRecipient**. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="842"
                         MinorBuildNumber="10"
                         Version="V2_8"
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
              <t:ItemId Id="AAMkADE4="
                        ChangeKey="CQAAABYA" />
              <t:Subject>Project priorities</t:Subject>
              <t:ToRecipients>
                <t:Mailbox>
                  <t:Name>sadie@contoso.com</t:Name>
                  <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                  <t:MailboxType>OneOff</t:MailboxType>
                </t:Mailbox>
              </t:ToRecipients>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

Die zweite Nachricht, die **SendItem**-Anforderungsnachricht, gibt die [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der zu sendenden E-Mail sowie die [SavedItemFolderId](https://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx) an, die den Ordner angibt, in dem das gesendete Objekt gespeichert werden soll.
  
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
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="AAMkADE4="
                  ChangeKey="CQAAABYA" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **SendItem**-Anforderung mit einer [SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx)-Nachricht, die den [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert **NoError** enthält, was darauf hinweist, dass die E-Mail erfolgreich gesendet wurde.
  
## <a name="send-a-delayed-email-message-by-using-the-ews-managed-api"></a>Senden einer verzögerten E-Mail-Nachricht mithilfe der verwalteten EWS-API
<a name="bk_senddelayedewsma"> </a>

Im folgenden Codebeispiel wird gezeigt, wie das [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)-Objekt zum Erstellen einer E-Mail-Nachricht, die [ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx)-Klasse zum Erstellen einer Eigenschaftsdefinition für die [PidTagDeferredSendTime](https://msdn.microsoft.com/library/cc840017.aspx)-Eigenschaft (0x3FEF0040) und die [SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)-Methode zum Senden einer verzögerten Nachricht und zum Speichern der Nachricht im Ordner „Entwürfe“ verwendet wird. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde. 
  
```cs
// Create a new email message. 
EmailMessage message = new EmailMessage(service);
// Specify the email recipient and subject. 
message.ToRecipients.Add("sadie@contoso.com");
message.Subject = "Delayed email";
// Identify the extended property that can be used to specify when to send the email. 
ExtendedPropertyDefinition PidTagDeferredSendTime = new ExtendedPropertyDefinition(16367, MapiPropertyType.SystemTime);
// Set the time that will be used to specify when the email is sent. 
// In this example, the email will be sent one minute after the next line executes, 
// provided that the message.SendAndSaveCopy request is processed by the server within one minute. 
string sendTime = DateTime.Now.AddMinutes(1).ToUniversalTime().ToString();
// Specify when to send the email by setting the value of the extended property. 
message.SetExtendedProperty(PidTagDeferredSendTime, sendTime);
// Specify the email body. 
StringBuilder str = new StringBuilder();
str.AppendLine("The client submitted the SendAndSaveCopy request at: " + DateTime.Now.ToUniversalTime().ToString() + ".");
str.AppendLine("The email message will be sent at: " + sendTime + ".");
message.Body = str.ToString();
Console.WriteLine("");
Console.WriteLine("The client submitted the SendAndSaveCopy request at: " + DateTime.Now.ToUniversalTime().ToString() + ".");
Console.WriteLine("The email message will be sent at: " + sendTime + ".");
// Submit the request to send the email message. 
message.SendAndSaveCopy();
```

## <a name="send-a-delayed-email-message-by-using-ews"></a>Senden einer verzögerten E-Mail-Nachricht mithilfe von EWS
<a name="bk_senddelayedews"> </a>

Im folgenden Codebeispiel wird gezeigt, wie der [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)-Vorgang mit dem **MessageDisposition**-Wert **SendAndSaveCopy** zum Erstellen einer E-Mail-Nachricht, das [ ExtendedProperty](https://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx)-Element zum Erstellen einer Eigenschaftsdefinition für die [PidTagDeferredSendTime](https://msdn.microsoft.com/library/cc840017.aspx)-Eigenschaft (0x3FEF0040) zum Festlegen einer Uhrzeit für das Senden der Nachricht und das [ SavedItemFolderId](https://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx)-Element zum Speichern der gesendeten Nachricht im Ordner „Gesendete Objekte“ verwendet wird. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange207_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Delayed email</t:Subject>
          <t:Body BodyType="HTML">
            The client submitted the SendAndSaveCopy request at: 1/2/2014 9:08:52 PM.
            The email message will be sent at: 1/2/2014 9:09:52 PM.
          </t:Body>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI PropertyTag="16367"
                                PropertyType="SystemTime" />
            <t:Value>2014-01-02T21:09:52.000</t:Value>
          </t:ExtendedProperty>
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

Der Server antwortet auf die **CreateItem**-Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert von **NoError** enthält, der darauf hinweist, dass die E-Mail erfolgreich erstellt wurde. Außerdem ist die [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht enthalten. 
  
## <a name="see-also"></a>Siehe auch


- [E-Mails und EWS in Exchange](email-and-ews-in-exchange.md)
    
- [Antworten auf E-Mail-Nachrichten mithilfe von EWS in Exchange](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    

