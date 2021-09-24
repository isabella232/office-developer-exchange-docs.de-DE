---
title: Antworten auf E-Mail-Nachrichten mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9d584991-4d67-4d36-ae2f-99970af8488f
description: Erfahren Sie, wie Sie auf E-Mail-Nachrichten mithilfe der verwalteten EWS-API oder EWS in Exchange antworten.
ms.openlocfilehash: 97928420a304e6683bc571230650e2756083ccf5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513094"
---
# <a name="respond-to-email-messages-by-using-ews-in-exchange"></a>Antworten auf E-Mail-Nachrichten mithilfe von EWS in Exchange

Erfahren Sie, wie Sie auf E-Mail-Nachrichten mithilfe der verwalteten EWS-API oder EWS in Exchange antworten.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um auf Nachrichten zu antworten, indem Sie ihnen antworten oder sie an Empfänger weiterleiten.
  
**Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für die Reaktion auf E-Mail-Nachrichten**

|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Antworten auf eine E-Mail-Nachricht  <br/> |[EmailMessage.Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> [EmailMessage.CreateReply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), wobei das [Items -Element](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) ein untergeordnetes Element von [ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) oder [ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx)hat.  <br/> |
|Weiterleiten einer E-Mail-Nachricht  <br/> |[EmailMessage.Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) <br/> [EmailMessage.CreateForward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), wobei das [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) -Element ein untergeordnetes Element von [ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx)hat.  <br/> |
   
## <a name="reply-to-an-email-message-by-using-the-ews-managed-api"></a>Antworten auf eine E-Mail-Nachricht mithilfe der verwalteten EWS-API
<a name="bk_replyewsma"> </a>

Die verwaltete EWS-API bietet zwei Methoden, mit denen Sie auf Nachrichten antworten können: [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) und [CreateReply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx). Die **Reply-Methode** verwendet nur zwei Parameter: die Antwortnachricht, die dem vorhandenen Textkörper vorangestellt wird, und einen **booleschen** Wert, der angibt, ob die Antwort an alle Empfänger (true) oder nur an den Absender (false) gesendet werden soll. Wenn Sie einer Nachricht zusätzliche Empfänger hinzufügen, zusätzliche Eigenschaften für eine Antwort festlegen oder eine Anlage hinzufügen müssen, verwenden Sie die **CreateReply-Methode,** mit der Sie alle erstklassigen Eigenschaften festlegen können, die für ein [EmailMessage-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) verfügbar sind. [](email-properties-and-elements-in-ews-in-exchange.md) 
  
Das folgende Codebeispiel zeigt, wie die **Reply-Methode** zum Antworten auf eine E-Mail-Nachricht verwendet wird. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. Die lokale Variable  *ItemId*  ist die [ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des Elements, auf das reagiert werden soll. Im Beispiel wird die [FindRecentlySent-Methode](#bk_findlast) aufgerufen, um zu überprüfen, ob die Nachricht als beantwortet markiert wurde. 
  
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

Das folgende Codebeispiel zeigt, wie die **CreateReply-Methode** zum Antworten auf eine E-Mail-Nachricht verwendet wird. 
  
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

Wenn Sie der Antwortnachricht eine Anlage hinzufügen müssen, ersetzen Sie den Aufruf der **SendAndSaveCopy-Methode** durch den folgenden Code. 
  
```cs
EmailMessage reply = responseMessage.Save();
reply.Attachments.AddFileAttachment("attachmentname.txt");
reply.Update(ConflictResolutionMode.AutoResolve);
reply.SendAndSaveCopy();
```

## <a name="reply-to-an-email-message-by-using-ews"></a>Antworten auf eine E-Mail-Nachricht mithilfe von EWS
<a name="bk_replyews"> </a>

Das folgende Codebeispiel zeigt, wie Sie mithilfe von EWS auf eine Nachricht antworten. Verwenden Sie den [CreateItem-Vorgang,](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) wobei das **MessageDisposition-Attribut** auf **SendAndSaveCopy** festgelegt ist, um die Nachricht zu senden und die Antwort im Ordner "Gesendete Elemente" zu speichern. Schließen Sie entweder das [ReplyAllToItem-Element](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) als untergeordnetes Element des [Items-Elements](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) ein, um allen Personen im Nachrichtenthread zu antworten, oder fügen Sie das [ReplyToItem-Element](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) ein, um nur an den Absender zu antworten. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn sie die [Reply-](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) oder die [CreateReply-Methode aufruft.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die **CreateItem-Anforderung** mit einer [CreateItemResponse-Nachricht,](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** enthält, der angibt, dass die Antwort erstellt und erfolgreich gesendet wurde.
  
Wenn Sie Ihrer Antwortnachricht eine Anlage hinzufügen müssen, rufen Sie den **CreateItem-Vorgang** wie oben angegeben auf, ändern Sie die **MessageDisposition** jedoch in **"SaveOnly".** Rufen Sie dann den [CreateAttachment-Vorgang](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) auf, gefolgt vom [SendItem-Vorgang.](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) 
  
## <a name="forward-an-email-message-by-using-the-ews-managed-api"></a>Weiterleiten einer E-Mail-Nachricht mithilfe der verwalteten EWS-API
<a name="bk_forwardewsma"> </a>

Die verwaltete EWS-API bietet zwei Methoden, die Sie zum Weiterleiten von Nachrichten verwenden können: [Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) und [CreateForward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx). Die **Forward-Methode** verwendet nur zwei Parameter: die Nachricht, die dem vorhandenen Text vorangestellt werden soll, und ein Array oder eine Sammlung von Empfängern, je nach der gewählten Überladung. Wenn Sie der Nachricht, die Sie weiterleiten, eine Anlage hinzufügen oder zusätzliche Eigenschaften für die neue Nachricht festlegen müssen, verwenden Sie die **CreateForward-Methode,** mit der Sie alle Eigenschaften festlegen können, die für ein [EmailMessage-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) verfügbar sind. 
  
Das folgende Codebeispiel zeigt, wie die **Forward-Methode** verwendet wird, um eine E-Mail-Nachricht an einen Empfänger weiterzuleiten. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. Die lokale Variable  *ItemId*  ist die [ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des weiterzuleitenden Elements. Im Beispiel wird die [FindRecentlySent-Methode](#bk_findlast) aufgerufen, um zu überprüfen, ob die Nachricht als weitergeleitet markiert wurde. 
  
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

Im folgenden Codebeispiel wird gezeigt, wie die **CreateForward-Methode** verwendet wird, um eine E-Mail-Nachricht an einen Empfänger weiterzuleiten. 
  
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

Wenn Sie der weitergeleiteten Nachricht eine Anlage hinzufügen müssen, ersetzen Sie den Aufruf der **SendAndSaveCopy-Methode** durch den folgenden Code. 
  
```cs
EmailMessage forward = forwardMessage.Save();
forward.Attachments.AddFileAttachment("attachmentname.txt");
forward.Update(ConflictResolutionMode.AutoResolve);
forward.SendAndSaveCopy();
```

## <a name="forward-an-email-message-by-using-ews"></a>Weiterleiten einer E-Mail-Nachricht mithilfe von EWS
<a name="bk_forwardews"> </a>

Das folgende Codebeispiel zeigt, wie eine Nachricht mithilfe von EWS weitergeleitet wird. Verwenden Sie den [CreateItem-Vorgang,](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) wobei das **MessageDisposition-Attribut** auf **SendAndSaveCopy** festgelegt ist, um die Nachricht zu senden und die Antwort im Ordner "Gesendete Elemente" zu speichern. Das [ForwardItem-Element](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) gibt an, dass es sich bei dem Element um eine weitergeleitete Nachricht handelt. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn sie die [Forward-](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) oder [createForward-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) aufruft. 
  
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

Der Server antwortet auf die **CreateItem-Anforderung** mit einer [CreateItemResponse-Nachricht,](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** enthält, der angibt, dass die weitergeleitete Nachricht erstellt und erfolgreich gesendet wurde.
  
Wenn Sie Ihrer Antwortnachricht eine Anlage hinzufügen müssen, rufen Sie den **CreateItem-Vorgang auf,** ändern Sie die **MessageDisposition** jedoch in **"SaveOnly".** Rufen Sie dann den [CreateAttachment-Vorgang](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) auf, gefolgt vom [SendItem-Vorgang.](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) 
  
## <a name="find-the-message-last-replied-to-or-forwarded-by-using-the-ews-managed-api"></a>Suchen der Nachricht, auf die zuletzt mithilfe der verwalteten EWS-API geantwortet oder weitergeleitet wurde
<a name="bk_findlast"> </a>

Das folgende Codebeispiel zeigt, wie Sie das letzte ausgeführte Verb und den Zeitpunkt finden, zu dem das letzte Verb für das angegebene Element ausgeführt wurde. Diese Methode wird aus anderen Codebeispielen der verwalteten EWS-API in diesem Thema aufgerufen, um zu überprüfen, ob die Elemente, auf die Sie geantwortet oder weitergeleitet haben, als beantwortet oder in Ihrem Posteingang weitergeleitet wurden. 
  
Im Beispiel wird die erweiterte Eigenschaft [PidTagLastVerbExecuted](https://msdn.microsoft.com/library/cc841968.aspx) (0x10820003) verwendet, um zu bestimmen, ob es sich bei der Nachricht um eine Antwort, eine Allen-Antwort oder eine Weiterleitung handelt, und um die erweiterte [Eigenschaft PidTagLastVerbExecutionTime](https://msdn.microsoft.com/library/cc839918.aspx) (0x10820040), um zu bestimmen, wann die Antwort oder der Weiterleitung gesendet wurde. 
  
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
    
- [Senden von E-Mail-Nachrichten mit EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

