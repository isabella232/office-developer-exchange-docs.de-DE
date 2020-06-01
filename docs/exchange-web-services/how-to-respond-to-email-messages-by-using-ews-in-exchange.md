---
title: Antworten auf E-Mail-Nachrichten mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9d584991-4d67-4d36-ae2f-99970af8488f
description: In diesem Artikel erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS in Exchange auf e-Mail-Nachrichten reagieren.
ms.openlocfilehash: 81599051f603654cdf8a50b789b37d7e76664a53
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455709"
---
# <a name="respond-to-email-messages-by-using-ews-in-exchange"></a>Antworten auf E-Mail-Nachrichten mithilfe von EWS in Exchange

In diesem Artikel erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS in Exchange auf e-Mail-Nachrichten reagieren.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um auf Nachrichten zu antworten, indem Sie Ihnen Antworten oder Sie an Empfänger weiterleiten.
  
**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge für die Reaktion auf e-Mail-Nachrichten**

|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Antworten auf eine e-Mail-Nachricht  <br/> |[Email Message. Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> [Email Message. createreply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), wobei das [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) -Element ein untergeordnetes Element von entweder [ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) oder [ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx).  <br/> |
|Weiterleiten einer e-Mail-Nachricht  <br/> |[Email Message. Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) <br/> [Email Message. createforward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), wobei das [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) -Element ein untergeordnetes Element von [ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx)hat.  <br/> |
   
## <a name="reply-to-an-email-message-by-using-the-ews-managed-api"></a>Antworten auf eine e-Mail-Nachricht mithilfe der verwaltete EWS-API
<a name="bk_replyewsma"> </a>

Das verwaltete EWS-API bietet zwei Methoden, mit denen Sie auf Nachrichten reagieren können: [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) und [createreply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx). Die **Reply** -Methode akzeptiert nur zwei Parameter: die Antwortnachricht, die dem vorhandenen Text vorangestellt werden soll, und einen **booleschen** Wert, der angibt, ob die Antwort an alle Empfänger (true) oder nur an den Absender (false) gesendet werden soll. Wenn Sie einer Nachricht zusätzliche Empfänger hinzufügen müssen, zusätzliche Eigenschaften für eine Antwort festlegen oder eine Anlage hinzufügen möchten, verwenden Sie die **createreply** -Methode, mit der Sie alle [Eigenschaften der First-Klasse](email-properties-and-elements-in-ews-in-exchange.md) festlegen können, die für ein [Email Message](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objekt verfügbar sind. 
  
Im folgenden Codebeispiel wird gezeigt, wie Sie mit der **Reply** -Methode auf eine e-Mail-Nachricht reagieren. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. Die lokale Variable *ItemID* ist die [ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des Elements, auf das reagiert werden soll. Im Beispiel wird die [FindRecentlySent-Methode](#bk_findlast) aufgerufen, um zu überprüfen, ob die Nachricht als beantwortet markiert wurde. 
  
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

Im folgenden Codebeispiel wird veranschaulicht, wie die **createreply** -Methode verwendet wird, um auf eine e-Mail-Nachricht zu antworten. 
  
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

Wenn Sie eine Anlage zur Antwortnachricht hinzufügen müssen, ersetzen Sie den Aufruf der **SendAndSaveCopy** -Methode durch den folgenden Code. 
  
```cs
EmailMessage reply = responseMessage.Save();
reply.Attachments.AddFileAttachment("attachmentname.txt");
reply.Update(ConflictResolutionMode.AutoResolve);
reply.SendAndSaveCopy();
```

## <a name="reply-to-an-email-message-by-using-ews"></a>Antworten auf eine e-Mail-Nachricht mithilfe von EWS
<a name="bk_replyews"> </a>

Im folgenden Codebeispiel wird gezeigt, wie eine Nachricht mithilfe von EWS beantwortet wird. Verwenden Sie den [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -Vorgang, wobei das **MessageDisposition** -Attribut auf **SendAndSaveCopy** festgelegt ist, um die Nachricht zu senden und die Antwort im Ordner "Gesendete Elemente" zu speichern. Fügen Sie das [ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) -Element als untergeordnetes Element des [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) -Elements ein, das jeder Person im Nachrichtenthread antworten soll, oder fügen Sie das [ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) -Element hinzu, um nur dem Absender zu antworten. 
  
Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn die [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) -oder die [createreply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) -Methode aufgerufen wird. 
  
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

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die Antwort erstellt und erfolgreich gesendet wurde.
  
Wenn Sie eine Anlage zur Antwortnachricht hinzufügen müssen, rufen Sie den **CreateItem** -Vorgang wie oben angegeben auf, ändern Sie jedoch die **MessageDisposition** in **SaveOnly**. Rufen Sie dann den [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) -Vorgang, gefolgt von der [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Operation auf. 
  
## <a name="forward-an-email-message-by-using-the-ews-managed-api"></a>Weiterleiten einer e-Mail-Nachricht mithilfe der verwaltete EWS-API
<a name="bk_forwardewsma"> </a>

Das verwaltete EWS-API stellt zwei Methoden bereit, die Sie zum Weiterleiten von Nachrichten verwenden können: [Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) und [createforward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx). Die **Forward** -Methode benötigt nur zwei Parameter: die Nachricht, die dem vorhandenen Text vorangestellt werden soll, und ein Array oder eine Auflistung von Empfängern, je nach der zu verwendenden Überladung. Wenn Sie der weiterzuleitenden Nachricht eine Anlage hinzufügen oder zusätzliche Eigenschaften für die neue Nachricht festlegen möchten, verwenden Sie die **createforward** -Methode, mit der Sie alle Eigenschaften festlegen können, die für ein [Email Message](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objekt verfügbar sind. 
  
Im folgenden Codebeispiel wird gezeigt, wie Sie mit der **Forward** -Methode eine e-Mail-Nachricht an einen Empfänger weiterleiten. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. Die lokale Variable *ItemID* ist die [ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des Elements, das weitergeleitet werden soll. Im Beispiel wird die [FindRecentlySent-Methode](#bk_findlast) aufgerufen, um zu überprüfen, ob die Nachricht als weitergeleitet markiert wurde. 
  
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

Im folgenden Codebeispiel wird gezeigt, wie Sie mit der **createforward** -Methode eine e-Mail-Nachricht an einen Empfänger weiterleiten. 
  
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

Wenn Sie eine Anlage zur weitergeleiteten Nachricht hinzufügen müssen, ersetzen Sie den Aufruf der **SendAndSaveCopy** -Methode durch den folgenden Code. 
  
```cs
EmailMessage forward = forwardMessage.Save();
forward.Attachments.AddFileAttachment("attachmentname.txt");
forward.Update(ConflictResolutionMode.AutoResolve);
forward.SendAndSaveCopy();
```

## <a name="forward-an-email-message-by-using-ews"></a>Weiterleiten einer e-Mail-Nachricht mithilfe von EWS
<a name="bk_forwardews"> </a>

Im folgenden Codebeispiel wird gezeigt, wie eine Nachricht mithilfe von EWS weitergeleitet wird. Verwenden Sie den [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -Vorgang, wobei das **MessageDisposition** -Attribut auf **SendAndSaveCopy** festgelegt ist, um die Nachricht zu senden und die Antwort im Ordner "Gesendete Elemente" zu speichern. Das [ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) -Element gibt an, dass das Element eine weitergeleitete Nachricht ist. 
  
Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn die [Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) -oder die [createforward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) -Methode aufgerufen wird. 
  
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

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die weitergeleitete Nachricht erfolgreich erstellt und gesendet wurde.
  
Wenn Sie eine Anlage zur Antwortnachricht hinzufügen müssen, rufen Sie den **CreateItem** -Vorgang auf, ändern Sie jedoch die **MessageDisposition** in **SaveOnly**. Rufen Sie dann den [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) -Vorgang, gefolgt von der [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Operation auf. 
  
## <a name="find-the-message-last-replied-to-or-forwarded-by-using-the-ews-managed-api"></a>Suchen Sie die Nachricht, die zuletzt mit dem verwaltete EWS-API beantwortet oder weitergeleitet wurde.
<a name="bk_findlast"> </a>

Im folgenden Codebeispiel wird gezeigt, wie das zuletzt ausgeführte Verb und die Uhrzeit, zu der das letzte Verb für das angegebene Element ausgeführt wurde, gefunden werden. Diese Methode wird aus anderen verwaltete EWS-API Codebeispielen in diesem Thema aufgerufen, um sicherzustellen, dass die geantworteten oder weitergeleiteten Elemente als beantwortet oder weitergeleitet in Ihrem Posteingang markiert wurden. 
  
Im Beispiel wird die erweiterte Eigenschaft [pidtaglastverbexecuted (](https://msdn.microsoft.com/library/cc841968.aspx) (0x10820003) verwendet, um zu bestimmen, ob die Nachricht eine Antwort, eine Antwort all oder eine Forward-und die [pidtaglastverbexecutiontime (](https://msdn.microsoft.com/library/cc839918.aspx) (0x10820040)-erweiterte Eigenschaft war, um zu bestimmen, wann die Antwort oder der Forward gesendet wurde. 
  
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
    

