---
title: Reagieren Sie auf e-Mail-Nachrichten mithilfe der EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9d584991-4d67-4d36-ae2f-99970af8488f
description: Erfahren Sie, wie durch Verwenden der EWS Managed API oder EWS in Exchange auf e-Mail-Nachrichten reagieren.
ms.openlocfilehash: 2f1428251084a7f2bf8d589a788c143f34b64d5c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756994"
---
# <a name="respond-to-email-messages-by-using-ews-in-exchange"></a>Reagieren Sie auf e-Mail-Nachrichten mithilfe der EWS in Exchange

Erfahren Sie, wie durch Verwenden der EWS Managed API oder EWS in Exchange auf e-Mail-Nachrichten reagieren.
  
Der EWS Managed API oder EWS können Sie auf Nachrichten antworten, indem sie beantworten oder Weiterleiten an Empfänger.
  
**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für die Reaktion auf e-Mail-Nachrichten**

|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Antworten Sie auf eine e-Mail-Nachricht  <br/> |[EmailMessage.Reply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> [EmailMessage.CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), wobei [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) -Element ein untergeordnetes Element des [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) oder [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx)hat.  <br/> |
|Weiterleiten einer e-Mail-Nachricht  <br/> |[EmailMessage.Forward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) <br/> [EmailMessage.CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), wobei [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) -Element ein untergeordnetes Element des [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx)hat.  <br/> |
   
## <a name="reply-to-an-email-message-by-using-the-ews-managed-api"></a>Antworten Sie auf eine e-Mail-Nachricht mithilfe der EWS Managed API
<a name="bk_replyewsma"> </a>

Die EWS Managed API bietet zwei Methoden, mit denen Sie Antworten auf Nachrichten: [Antworten](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) und [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx). Die **Reply** -Methode hat nur zwei Parameter: die Antwortnachricht vorangestellt vorhandenen Text und ein **boolescher** Wert, der angibt, ob die Antwort an alle Empfänger (True) oder nur an den Absender (False) eingefügt werden sollen. Wenn Sie benötigen weitere Empfänger einer Nachricht hinzufügen zu einer Antwort zusätzliche Eigenschaften festlegen oder einer Anlage hinzufügen, verwenden Sie die **CreateReply** -Methode, wodurch Sie legen Sie alle [Eigenschaften der ersten Klasse](email-properties-and-elements-in-ews-in-exchange.md) , die auf ein ["EmailMessage" verfügbar sind ](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)Objekt. 
  
Im folgenden Codebeispiel wird veranschaulicht, wie die **Reply** -Methode verwenden, um auf eine e-Mail-Nachricht zu reagieren. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. Die lokale Variable *ItemId* ist die [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des Elements zu beantworten. Das Beispiel ruft die [FindRecentlySent-Methode](#bk_findlast) , um sicherzustellen, dass die Nachricht als geantwortet markiert wurde. 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.LastModifiedTime);
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, propSet);
string myReply = "This is the message body of the email reply.";
bool replyToAll = false;
// Send the response message.
// This method call results in a CreateItem call to EWS.
message.Reply(myReply, replyToAll);
// Verify that the response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

Im folgenden Codebeispiel wird veranschaulicht, wie die **CreateReply** -Methode verwenden, um auf eine e-Mail-Nachricht zu reagieren. 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
// Create the reply response message from the original email message.
// Indicate whether the message is a reply or reply all type of reply.
bool replyToAll = true;
ResponseMessage responseMessage = message.CreateReply(replyToAll);
// Prepend the reply to the message body. 
string myReply = "This is the message body of the email reply.";
responseMessage.BodyPrefix = myReply;
// Send the response message.
// This method call results in a CreateItem call to EWS.
responseMessage.SendAndSaveCopy();
// Check that the response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

Wenn Sie, um die Response-Nachricht eine Anlage hinzuzufügen müssen, ersetzen Sie den Anruf an die **SendAndSaveCopy** -Methode durch den folgenden Code. 
  
```cs
EmailMessage reply = responseMessage.Save();
reply.Attachments.AddFileAttachment("attachmentname.txt");
reply.Update(ConflictResolutionMode.AutoResolve);
reply.SendAndSaveCopy();
```

## <a name="reply-to-an-email-message-by-using-ews"></a>Antworten Sie auf eine e-Mail-Nachricht mithilfe der Exchange-Webdienste
<a name="bk_replyews"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie mithilfe der Exchange-Webdienste auf eine Nachricht zu antworten. Verwenden Sie die [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) Operation mit dem festgelegten **SendAndSaveCopy** **"MessageDisposition"** -Attribut senden die Nachricht, und speichern die Antwort im Ordner "Gesendete Elemente". Das [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) -Element als untergeordnetes Element des Elements [Elemente](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) für alle Benutzer in der Nachricht Thread Antworten enthalten, oder das [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) -Element, um nur dem Absender Antworten enthalten. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn die [Antwort](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) oder die [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) -Methode aufrufen. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:ReplyAllToItem>
          <t:ReferenceItemId Id="AAMkADE4="
                             ChangeKey="CQAAABYA" />
          <t:NewBodyContent BodyType="HTML">This is the message body of the email reply.</t:NewBodyContent>
        </t:ReplyAllToItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Antwort erstellt und erfolgreich gesendet wurde.
  
Wenn Sie Ihre Antwortnachricht eine Anlage hinzufügen möchten, rufen Sie die **CreateItem** Operation wie oben angegeben, aber ändern Sie die **"MessageDisposition"** in **SaveOnly**. Rufen Sie dann den [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) -Vorgang, gefolgt von [den SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang. 
  
## <a name="forward-an-email-message-by-using-the-ews-managed-api"></a>Weiterleiten einer e-Mail-Nachricht mithilfe der EWS Managed API
<a name="bk_forwardewsma"> </a>

Die EWS Managed API bietet zwei Methoden, die Sie zum Weiterleiten von Nachrichten verwenden können: [Vorwärts-](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) und [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx). Die **Forward** -Methode hat nur zwei Parameter: die Nachricht vorangestellt, um die vorhandenen Text und ein Array oder eine Auflistung von Empfängern, je nach der Überladung, die Sie verwenden möchten. Wenn Sie zum Hinzufügen einer Anlage an die Nachricht, die Sie weiterleiten, oder klicken Sie auf die neue Nachricht zusätzliche Eigenschaften festlegen müssen, verwenden Sie die **CreateForward** -Methode, wodurch Sie alle Eigenschaften festgelegt, die für ein Objekt ["EmailMessage"](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) verfügbar sind. 
  
Im folgenden Codebeispiel wird veranschaulicht, wie die **Forward** -Methode verwendet, an einen Empfänger eine e-Mail-Nachricht weiterzuleiten. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. Die lokale Variable *ItemId* ist die [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des Elements, weiterzuleiten. Das Beispiel ruft die [FindRecentlySent-Methode](#bk_findlast) , um sicherzustellen, dass die Nachricht als weitergeleitet markiert wurde. 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
string myForward = "This is the message body of the forwarded email.";
// Send the response message.
// This method call results in a CreateItem call to EWS.
message.Forward(myForward, "sadie@contoso.com");
// Verify that the forwarded response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

Im folgenden Codebeispiel wird veranschaulicht, wie mit der **CreateForward** -Methode eine e-Mail-Nachricht an einen Empfänger weitergeleitet. 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
// Create the reply response message from the original email message.
// Indicate whether the message is a reply or reply all type of reply.
ResponseMessage forwardMessage = message.CreateForward();
// Set properties on the email message.
forwardMessage.ToRecipients.Add("sadie@contoso.com");
forwardMessage.Body = "Sadie,<br><br>I thought you'd be interested in this thread.<br><br>-Mack";
// Send and save a copy of the replied email message in the default Sent Items folder. 
forwardMessage.SendAndSaveCopy();
// Verify that the forwarded message was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

Wenn Sie eine Anlage an die weitergeleitete Nachricht hinzufügen müssen, ersetzen Sie den Anruf an die **SendAndSaveCopy** -Methode durch den folgenden Code. 
  
```cs
EmailMessage forward = forwardMessage.Save();
forward.Attachments.AddFileAttachment("attachmentname.txt");
forward.Update(ConflictResolutionMode.AutoResolve);
forward.SendAndSaveCopy();
```

## <a name="forward-an-email-message-by-using-ews"></a>Weiterleiten einer e-Mail-Nachricht mithilfe der Exchange-Webdienste
<a name="bk_forwardews"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie eine Nachricht weiterleiten mithilfe der Exchange-Webdienste. Verwenden Sie die [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) Operation mit dem festgelegten **SendAndSaveCopy** **"MessageDisposition"** -Attribut senden die Nachricht, und speichern die Antwort im Ordner "Gesendete Elemente". Das [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) -Element gibt an, dass das Element einer weitergeleiteten Nachricht ist. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn die [Weiterleiten](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) oder die [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) -Methode aufrufen. 
  
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
      <m:Items>
        <t:ForwardItem>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
          <t:ReferenceItemId Id="AAAMkADE="
                             ChangeKey="CQAAABYA" />
          <t:NewBodyContent BodyType="HTML">This is the message body of the forwarded email.</t:NewBodyContent>
        </t:ForwardItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die weitergeleitete Nachricht erstellt und gesendet wurde.
  
Wenn Sie Ihre Antwortnachricht eine Anlage hinzufügen möchten, rufen Sie den **CreateItem** -Vorgang, aber ändern Sie die **"MessageDisposition"** in **SaveOnly**. Rufen Sie dann den [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) -Vorgang, gefolgt von [den SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang. 
  
## <a name="find-the-message-last-replied-to-or-forwarded-by-using-the-ews-managed-api"></a>Hier finden Sie die Nachricht zuletzt beantwortet oder mithilfe der EWS Managed API weitergeleitet
<a name="bk_findlast"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie das letzte Verb ausgeführt suchen und die Uhrzeit das letzte Verb ausgeführt wurde auf das angegebene Element festgelegt. Diese Methode wird aufgerufen, von anderen EWS Managed API-Codebeispiele in diesem Thema, um sicherzustellen, dass die Elemente an die Sie weitergeleitet oder darauf geantwortet als geantwortet markiert oder in Ihrem Posteingang weitergeleitet wurden. 
  
Im Beispiel wird die [PidTagLastVerbExecuted](http://msdn.microsoft.com/en-us/library/cc841968.aspx) (0x10820003) extended-Eigenschaft verwendet, um festzustellen, ob die Nachricht eine Antwort, eine allen Antworten oder eine Weiterleitung wurde und [PidTagLastVerbExecutionTime](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x10820040) Eigenschaft erweiterten, um zu bestimmen, wann die Antworten oder Weiterleiten gesendet wurde. 
  
```cs
public static void FindRecentlySent(EmailMessage messageToCheck)
{
    // Create extended property definitions for PidTagLastVerbExecuted and PidTagLastVerbExecutionTime.
    ExtendedPropertyDefinition PidTagLastVerbExecuted = new ExtendedPropertyDefinition(0x1081, MapiPropertyType.Integer);
    ExtendedPropertyDefinition PidTagLastVerbExecutionTime = new ExtendedPropertyDefinition(0x1082, MapiPropertyType.SystemTime);
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, PidTagLastVerbExecutionTime, PidTagLastVerbExecuted);
    messageToCheck = EmailMessage.Bind(service, messageToCheck.Id, propSet);
    // Determine the last verb executed on the message and display output.
    object responseType;
    if (messageToCheck.TryGetProperty(PidTagLastVerbExecuted, out responseType))
    {
        object ReplyTime = null;
        switch (((Int32)responseType))
        {
            case 102: Console.WriteLine("A reply was sent to the '" + messageToCheck.Subject.ToString() + "' email message at");
                break;
            case 103: Console.WriteLine("A reply all was sent to the '" + messageToCheck.Subject.ToString() + "' email message at");
                break;
            case 104: Console.WriteLine("The '" + messageToCheck.Subject.ToString() + "' email message was forwarded at");
                break;
        }
        if (messageToCheck.TryGetProperty(PidTagLastVerbExecutionTime, out ReplyTime))
        {
            Console.WriteLine(((DateTime)ReplyTime).ToString() + ".");
        }
    }
    else
    {
        Console.WriteLine("No changes were made to  '" + messageToCheck.Subject.ToString() + "'.");
    }
}
```

## <a name="see-also"></a>Siehe auch


- [E-Mail- und EWS in Exchange](email-and-ews-in-exchange.md)
    
- [Senden von e-Mail-Nachrichten mithilfe der EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

