---
title: E-Mail- und EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d7bdb37-f7f1-409f-9749-f8bcde7dc52a
description: Erfahren Sie mehr darüber, wie Sie mit E-Mail-Nachrichten arbeiten, z. B. wie Sie eine E-Mail-Nachricht erstellen und wie Sie andere E-Mail-bezogene Aufgaben mithilfe der EWS Managed API oder von ESW in Exchange durchführen.
ms.openlocfilehash: 2cd4613635bd2a5ecc061b50b0aecbdde1d32d46
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353672"
---
# <a name="email-and-ews-in-exchange"></a>E-Mail- und EWS in Exchange

Erfahren Sie mehr darüber, wie Sie mit E-Mail-Nachrichten arbeiten, z. B. wie Sie eine E-Mail-Nachricht erstellen und wie Sie andere E-Mail-bezogene Aufgaben mithilfe der EWS Managed API oder von ESW in Exchange durchführen.
  

  
In Kern dreht sich bei Exchange alles um E-Mail. Aber was macht eine E-Mail zu einer E-Mail? Nun, E-Mail-Nachrichten sind eins der [stark typisierten Elemente](folders-and-items-in-ews-in-exchange.md#bk_item) in Exchange, was bedeutet, dass sie einen bestimmten [Satz von Eigenschaften](email-properties-and-elements-in-ews-in-exchange.md) enthalten, schon bevor sie gesendet werden. E-Mail-Nachrichten werden von der Klasse [EmailMessage ](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) in der EWS Managed API und vom Element [Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) und dessen untergeordneten Elementen in EWS dargestellt. 
  
In der EWS Managed API wird das Objekt **EmailMessage** vom Objekt [Item](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) abgeleitet. Die Klasse **EmailMessage** erweitert die Klasse **Item** durch die Bereitstellung zusätzlicher Eigenschaften wie [EmailMessage.Sender](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.sender%28v=exchg.80%29.aspx) und [EmailMessage.IsRead](http://msdn.microsoft.com/de-DE/library/office/microsoft.exchange.webservices.data.emailmessage.isread%28v=exchg.80%29.aspx), die jetzt für nahezu alle Messagingszenarien typisch sind. Wenn Sie eine E-Mail-Nachricht abrufen, aktualisieren oder löschen, können Sie dies in den meisten Fällen mit dem Objekt **EmailMessage** oder dem Basisobjekt **Item** tun, je nachdem, ob sich die Eigenschaften, mit denen Sie arbeiten, in der Klasse [EmailMessageSchema](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessageschema%28v=exchg.80%29.aspx) oder der Klasse [ItemSchema](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx) befinden. Die Elementerstellung ist unterschiedlich, da die Klasse **Item** nicht über einen Konstruktor verfügt, deshalb verwenden Sie beim Erstellen einer E-Mail den [EmailMessage-Konstruktor](http://msdn.microsoft.com/de-DE/library/office/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx), um die E-Mail zu erstellen, und die Methode [EmailMessage.Save](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) oder [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx), um sie zu speichern oder zu senden und zu speichern. 
  
Auf ähnliche Weise verwenden Sie in EWS den Vorgang [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) mit dem Element [Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx), um eine E-Mail-Nachricht zu erstellen. Zum Abrufen, Aktualisieren oder Löschen von E-Mails mithilfe von EWS ist die Tatsache, dass das zu ändernde Element eine E-Mail-Nachricht ist, nicht wichtig, trotz der Tatsache, dass zusätzliche Eigenschaften für E-Mail-Nachrichten verfügbar sind. Dieselben Vorgänge, die für andere stark typisierte Elemente verwendet werden, werden auch für E-Mail-Nachrichten benutzt. 
  
|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Erstellen  <br/> |[EmailMessage.Save](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Abrufen  <br/> |[EmailMessage.Bind](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|Aktualisieren  <br/> |[Item.Update](http://msdn.microsoft.com/de-DE/library/dd635915%28v=exchg.80%29.aspx) <br/> |[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen  <br/> |[Item.Delete](http://msdn.microsoft.com/de-DE/library/dd635072%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
Da E-Mail-Nachrichten einfach [stark typisierte Elemente](folders-and-items-in-ews-in-exchange.md#bk_item) sind, arbeiten Sie mit ihnen in einigen Fällen auf dieselbe Weise wie beim [Arbeiten mit generischen Elementen](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md). 
  
## <a name="create-an-email-message-by-using-the-ews-managed-api"></a>Erstellen einer E-Mail-Nachricht mithilfe der EWS Managed API
<a name="bk_createewsma"> </a>

Sie können eine E-Mail-Nachricht erstellen, indem Sie die EWS Managed API-Methode [Save](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) verwenden, wie im Code im folgenden Beispiel gezeigt. Beachten Sie, dass im Beispiel die Nachricht nur im Ordner „Entwürfe“ gespeichert wird, ohne sie zu senden. Informationen zum Senden der Nachricht oder zum Erstellen und Senden der Nachricht in einem Schritt finden Sie unter [Senden von E-Mail-Nachrichten mithilfe von EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde. 
  
```cs
// Create a new email message.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.ToRecipients.Add("mack@contoso.com");
message.Subject = "Project priorities";
message.Body = "(1) Buy pizza, (2) Eat pizza";
// Save the email message to the Drafts folder (where it can be retrieved, updated, and sent at a later time).
// This method call results in a CreateItem call to EWS.
message.Save(WellKnownFolderName.Drafts);
Console.WriteLine("A draft email message with the subject '" + message.Subject + "' has been saved to the Drafts folder.");
```

## <a name="create-an-email-message-by-using-ews"></a>Erstellen einer E-Mail-Nachricht mithilfe von EWS
<a name="bk_createews"> </a>

Sie können eine E-Mail-Nachricht erstellen, indem Sie den EWS-Vorgang [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) verwenden, wie im folgenden Beispiel gezeigt. Dies ist auch die XML-Anforderung, die von der EWS Managed API gesendet wird, wenn Sie [eine E-Mail-Nachricht erstellen](#bk_createewsma). Beachten Sie, dass im folgenden Beispiel die Nachricht nur im Ordner „Entwürfe“ gespeichert wird, ohne sie zu senden. Informationen zum Senden der Nachricht oder zum Erstellen und Senden der Nachricht in einem Schritt finden Sie unter [Senden von E-Mail-Nachrichten mithilfe von EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP2" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Project priorities</t:Subject>
          <t:Body BodyType="HTML">(1) Buy pizza, (2) Eat pizza</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>mack@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

Der Server antwortet auf die **CreateItem**-Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert von **NoError** enthält, der darauf hinweist, dass die E-Mail erfolgreich erstellt wurde. Außerdem ist die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht enthalten. 
  
## <a name="get-update-and-delete-an-email-message-by-using-the-ews-managed-api"></a>Abrufen, Aktualisieren und Löschen einer E-Mail-Nachricht mithilfe der EWS Managed API
<a name="bk_getewsma"> </a>

Sie können die EWS Managed API verwenden, um eine E-Mail-Nachricht auf dieselbe Weise abzurufen, zu aktualisieren oder zu löschen, in der Sie diese Aktionen für jedes generische Element aus dem Exchange-Informationsspeicher durchführen. Weitere Informationen finden Sie unter [Arbeiten mit Exchange-Postfachelementen mithilfe von EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).
  
Wenn Sie eine E-Mail-Nachricht aktualisieren, finden Sie unter [E-Mail-Eigenschaften und Elemente in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md) eine Liste der schreibbaren Eigenschaften für E-Mail-Nachrichten. Informationen zum Senden eines Nachrichtenentwurfs nach dem Aktualisieren finden Sie unter [Senden eines E-Mail-Nachrichtenentwurfs mithilfe der EWS Managed API](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftewsma).
  
## <a name="get-update-and-delete-an-email-message-by-using-ews"></a>Abrufen, Aktualisieren und Löschen einer E-Mail-Nachricht mithilfe von EWS
<a name="bk_getews"> </a>

Sie können EWS verwenden, um eine E-Mail-Nachricht auf dieselbe Weise abzurufen, zu aktualisieren und zu löschen, in der Sie diese Aktionen für jedes generische Element aus dem Exchange-Informationsspeicher durchführen. Weitere Informationen finden Sie unter [Arbeiten mit Exchange-Postfachelementen mithilfe von EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).
  
Wenn Sie eine E-Mail-Nachricht aktualisieren, finden Sie unter [E-Mail-Eigenschaften und Elemente in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md) eine Liste der schreibbaren Eigenschaften für E-Mail-Nachrichten. Informationen zum Senden eines Nachrichtenentwurfs nach dem Aktualisieren finden Sie unter [Senden eines E-Mail-Nachrichtenentwurfs mithilfe von EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [E-Mail-Eigenschaften und Elemente in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md)
    
- [Senden von E-Mail-Nachrichten mit EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)
    
- [Antworten auf E-Mail-Nachrichten mithilfe von EWS in Exchange](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    
- [Verschieben und Kopieren von E-Mail-Nachrichten mithilfe von EWS in Exchange](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)
    
- [Arbeiten mit Unterhaltungen unter Verwendung von EWS in Exchange](how-to-work-with-conversations-by-using-ews-in-exchange.md)
    
- [Extrahieren einer Entität aus einer E-Mail-Nachricht mithilfe von EWS in Exchange](how-to-extract-an-entity-from-an-email-message-by-using-ews-in-exchange.md)
    
- [Verarbeiten von E-Mails in Batches mithilfe von EWS in Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    

