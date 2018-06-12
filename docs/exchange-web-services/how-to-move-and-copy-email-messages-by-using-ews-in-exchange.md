---
title: Verschieben und Kopieren von e-Mail-Nachrichten mithilfe der EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4771668f-5623-4397-a5c0-b75a7ba01698
description: Erfahren Sie, wie E-Mail-Nachrichten mithilfe der verwalteten EWS-API oder EWS in Exchange verschoben und kopiert werden können.
ms.openlocfilehash: 16f0604a16785c34dd04bdabedeedd331668a479
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756966"
---
# <a name="move-and-copy-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="8952c-103">Verschieben und Kopieren von e-Mail-Nachrichten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8952c-103">Move and copy email messages by using EWS in Exchange</span></span>

<span data-ttu-id="8952c-104">Erfahren Sie, wie E-Mail-Nachrichten mithilfe der verwalteten EWS-API oder EWS in Exchange verschoben und kopiert werden können.</span><span class="sxs-lookup"><span data-stu-id="8952c-104">Learn how to move and copy email messages by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="8952c-105">Sie können die verwaltete EWS-API oder EWS zum Verschieben und Kopieren von E-Mail-Nachrichten in einem Postfach verwenden.</span><span class="sxs-lookup"><span data-stu-id="8952c-105">You can use the EWS Managed API or EWS to move and copy email messages in a mailbox.</span></span>
  
<span data-ttu-id="8952c-106">**Tabelle 1. Verwaltete EWS-API-Methoden und EWS-Operationen zum Verschieben und Kopieren von E-Mail-Nachrichten**</span><span class="sxs-lookup"><span data-stu-id="8952c-106">**Table 1. EWS Managed API methods and EWS operations for moving and copying email messages**</span></span>

|<span data-ttu-id="8952c-107">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="8952c-107">**Task**</span></span>|<span data-ttu-id="8952c-108">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="8952c-108">**EWS Managed API method**</span></span>|<span data-ttu-id="8952c-109">**EWS-Operation**</span><span class="sxs-lookup"><span data-stu-id="8952c-109">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8952c-110">Verschieben einer E-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8952c-110">Move an email message</span></span>  <br/> |[<span data-ttu-id="8952c-111">EmailMessage.Move</span><span class="sxs-lookup"><span data-stu-id="8952c-111">EmailMessage.Move</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="8952c-112">MoveItem</span><span class="sxs-lookup"><span data-stu-id="8952c-112">MoveItem</span></span>](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="8952c-113">Kopieren einer E-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8952c-113">Copy an email message</span></span>  <br/> |[<span data-ttu-id="8952c-114">EmailMessage.Copy</span><span class="sxs-lookup"><span data-stu-id="8952c-114">EmailMessage.Copy</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="8952c-115">CopyItem</span><span class="sxs-lookup"><span data-stu-id="8952c-115">CopyItem</span></span>](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="8952c-p101">Es ist wichtig zu beachten, dass beim Verschieben oder Kopieren einer E-Mail-Nachricht in einen anderen Ordner ein neues Element in dem neuen Ordner mit einer eindeutigen Element-ID erstellt wird, und die ursprüngliche Nachricht wird gelöscht. Wenn Sie eine E-Mail-Nachricht zwischen zwei Ordnern in demselben Postfach verschieben oder kopieren, wird das neue Element in der Antwort zurückgegeben, mit dem Sie Zugriff auf die neue Element-ID erhalten. Wenn Sie jedoch eine E-Mail zwischen zwei Postfächern oder zwischen einem Postfach und einem öffentlichen Ordner verschieben oder kopieren, wird das neue Element nicht in der Antwort zurückgegeben. Verwenden Sie für den Zugriff auf die verschobene Nachricht in dem Szenario die verwaltete EWS-API-[FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)-Methode oder EWS-[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)-Operation, [erstellen Sie eine erweiterte Eigenschaftsdefinition](properties-and-extended-properties-in-ews-in-exchange.md) für die [PidTagSearchKey](http://msdn.microsoft.com/en-us/library/cc839918.aspx)-Eigenschaft (0x300B0102), oder erstellen Sie eine benutzerdefinierte erweiterte Eigenschaft, legen Sie sie fest und suchen Sie dann in dem neuen Ordner nach der benutzerdefinierten erweiterten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8952c-p101">It's important to note that when you move or copy an email message into a different folder, a new item is created in the new folder with a unique item ID, and the original message is deleted. If you're moving or copying an email message between two folders in the same mailbox, the new item is returned in the response, which gives you access to the new item ID. However, if you're moving or copying an email message between two mailboxes or between a mailbox and a public folder, the new item is not returned in the response. To access the moved message in that scenario, use the EWS Managed API [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) method or EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation, [create an extended property definition](properties-and-extended-properties-in-ews-in-exchange.md) for the [PidTagSearchKey](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x300B0102) property, or create and set a custom extended property and then search for the custom extended property in the new folder.</span></span> 
  
<span data-ttu-id="8952c-p102">Das Löschen einer E-Mail-Nachricht unterscheidet sich vom Verschieben eines Elements in den Ordner „Gelöscht Elemente". Wenn Sie die verwaltete EWS-API-[Item.Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx)-Methode oder die EWS-[DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)-Operation verwenden, wird das in der Anfrage angegebene Element aus dem ursprünglichen Ordner verschoben und eine Kopie wird mit der neuen Element-ID im Ordner „Gelöschte Elemente" abgelegt. Anders als beim Verschieben oder Kopieren eines Elements wird das neue Element nicht in der **Delete** -Methode oder **DeleteItem**-Operationsantwort zurückgegeben. Die zum [Löschen einer E-Mail mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) oder [EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) erforderlichen Schritte sind die gleichen wie beim Löschen eines generischen Elements aus dem Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="8952c-p102">Deleting an email message is different than moving an item to the Deleted Items folder. If you use the EWS Managed API [Item.Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) method or the EWS [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) operation, the item specified in the request is removed from the original folder, and a copy is placed in the Deleted Items folder with a new item ID. Unlike when you move or copy any item, the new item is not returned in the **Delete** method or the **DeleteItem** operation response. The steps involved in [deleting an email by using the EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) or [EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) are the same as those for deleting any generic item from the Exchange store.</span></span> 
  
## <a name="move-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="8952c-124">Verschieben einer E-Mail-Nachricht mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8952c-124">Move an email message by using the EWS Managed API</span></span>
<span data-ttu-id="8952c-125"><a name="bk_moveewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="8952c-125"></span></span>

<span data-ttu-id="8952c-126">Im folgenden Codebeispiel wird veranschaulicht, wie die [EmailMessage.Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx)-Methode zum Verschieben einer vorhandenen E-Mail-Nachricht von einem in einen anderen Ordner verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8952c-126">The following code example shows how to use the [EmailMessage.Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) method to move an existing email message from one folder to another.</span></span> 
  
<span data-ttu-id="8952c-127">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist, und dass **ItemId** die [ID](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) der zu verschiebenden oder kopierenden E-Mail-Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="8952c-127">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to move or copy.</span></span> 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ParentFolderId);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage beforeMessage = EmailMessage.Bind(service, ItemId, propSet);
// Move the specified mail to the JunkEmail folder and store the returned item.
Item item = beforeMessage.Move(WellKnownFolderName.JunkEmail);
// Check that the item was moved by binding to the moved email message 
// and retrieving the new ParentFolderId.
// This method call results in a GetItem call to EWS.
EmailMessage movedMessage = EmailMessage.Bind(service, item.Id, propSet);
Console.WriteLine("An email message with the subject '" + beforeMessage.Subject + "' has been moved from the '" + beforeMessage.ParentFolderId + "' folder to the '" + movedMessage.ParentFolderId + "' folder.");
```

## <a name="move-an-email-message-by-using-ews"></a><span data-ttu-id="8952c-128">Verschieben einer E-Mail-Nachricht mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="8952c-128">Move an email message by using EWS</span></span>
<span data-ttu-id="8952c-129"><a name="bk_moveews"> </a></span><span class="sxs-lookup"><span data-stu-id="8952c-129"></span></span>

<span data-ttu-id="8952c-130">Im folgenden Codebeispiel wird veranschaulicht, wie die [MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)-Operation zum Verschieben einer E-Mail-Nachricht in den Junk-E-Mail-Ordner verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8952c-130">The following code example shows how to use the [MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) operation to move an email message to the Junk Email folder.</span></span> 
  
<span data-ttu-id="8952c-p103">Dies ist auch die XML-Anforderung, die beim Aufrufen der [Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx)-Methode an die verwaltete EWS-API gesendet wird. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="8952c-p103">This is also the XML request that is sent by the EWS Managed API when calling the [Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) method. The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:MoveItem>
      <m:ToFolderId>
        <t:DistinguishedFolderId Id="junkemail" />
      </m:ToFolderId>
      <m:ItemIds>
        <t:ItemId Id="AfwDoAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF25sM1" />
      </m:ItemIds>
    </m:MoveItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="8952c-p104">Der Server antwortet auf die **MoveItem**-Anforderung mit einer [MoveItemResponse](http://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert **NoError** umfasst, der angibt, dass die E-Mail-Nachricht erfolgreich verschoben wurde. Die Antwort enthält außerdem die **ItemId** für die E-Mail-Nachricht in dem neuen Ordner, die zum Speichern relevant ist, da die **ItemId** im neuen Ordner anders lautet.</span><span class="sxs-lookup"><span data-stu-id="8952c-p104">The server responds to the **MoveItem** request with a [MoveItemResponse](http://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email message was moved successfully. The response also includes the **ItemId** for the email message in the new folder, which is important to store because the **ItemId** is different in the new folder.</span></span> 
  
## <a name="copy-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="8952c-135">Kopieren einer E-Mail-Nachricht mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8952c-135">Copy an email message by using the EWS Managed API</span></span>
<span data-ttu-id="8952c-136"><a name="bk_copyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="8952c-136"></span></span>

<span data-ttu-id="8952c-137">Im folgenden Codebeispiel wird veranschaulicht, wie die [EmailMessage.Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx)-Methode zum Kopieren einer vorhandenen E-Mail-Nachricht aus einem in einen anderen Ordner verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8952c-137">The following code example shows how to use the [EmailMessage.Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) method to copy an existing email message from one folder to another.</span></span> 
  
<span data-ttu-id="8952c-p105">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt, und **ItemId** die [ID](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) der zu kopierenden E-Mail-Nachricht ist. Die Werte einiger Parameter wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="8952c-p105">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to copy. The values of some parameters have been shortened for readability.</span></span> 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ParentFolderId);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage originalMessage = EmailMessage.Bind(service, ItemId, propSet);
// Copy the orignal message into another folder in the mailbox and store the returned item.
Item item = originalMessage.Copy("epQ/3AAA=");
// Check that the item was copied by binding to the copied email message 
// and retrieving the new ParentFolderId.
// This method call results in a GetItem call to EWS.
EmailMessage copiedMessage = EmailMessage.Bind(service, item.Id, propSet);
Console.WriteLine("An email message with the subject '" + originalMessage.Subject + "' has been copied from the '" + originalMessage.ParentFolderId + "' folder to the '" + copiedMessage.ParentFolderId + "' folder.");
```

## <a name="copy-an-email-message-by-using-ews"></a><span data-ttu-id="8952c-140">Kopieren einer E-Mail-Nachricht mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="8952c-140">Copy an email message by using EWS</span></span>
<span data-ttu-id="8952c-141"><a name="bk_copyews"> </a></span><span class="sxs-lookup"><span data-stu-id="8952c-141"></span></span>

<span data-ttu-id="8952c-142">Im folgenden Codebeispiel wird veranschaulicht, wie die [CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx)-Operation zum Kopieren einer E-Mail-Nachricht in einen anderen Ordner desselben Postfachs verwendet werden kann, indem die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der zu verschiebenden E-Mailnachricht gesendet und dabei der Zielordner im [ToFolderId](http://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx)-Element angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8952c-142">The following code example shows how to use the [CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) operation to copy an email message to different folder in the same mailbox by sending the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the email message to move, and specifying the destination folder in the [ToFolderId](http://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="8952c-p106">Dies ist die XML-Anforderung, die beim Aufrufen der [Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx)-Methode von der verwalteten EWS-API gesendet wird. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="8952c-p106">This is also the XML request that is sent by the EWS Managed API when calling the [Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) method. The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:CopyItem>
      <m:ToFolderId>
        <t:FolderId Id="pQ/3AAA=" />
      </m:ToFolderId>
      <m:ItemIds>
        <t:ItemId Id="2TSeSAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF2d+3+" />
      </m:ItemIds>
    </m:CopyItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="8952c-p107">Der Server antwortet auf die **CopyItem**-Anforderung mit einer [CopyItemResponse](http://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert **NoError** umfasst, der angibt, dass die E-Mail-Nachricht erfolgreich kopiert wurde. Die Antwort umfasst außerdem die **ItemId** für die E-Mail-Nachricht im neuen Ordner, die zum Speichern relevant ist, da die **ItemId** im neuen Ordner anders lautet.</span><span class="sxs-lookup"><span data-stu-id="8952c-p107">The server responds to the **CopyItem** request with a [CopyItemResponse](http://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email message was copied successfully. The response also includes the **ItemId** for the email message in the new folder, which is important to store because the **ItemId** is different in the new folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8952c-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8952c-147">See also</span></span>


- [<span data-ttu-id="8952c-148">E-Mail- und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8952c-148">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="8952c-149">Senden von e-Mail-Nachrichten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8952c-149">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

