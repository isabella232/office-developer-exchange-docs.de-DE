---
title: Löschen von Anlagen mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 71871ac7-ee1a-4f93-9e81-77f312d432f4
description: Erfahren Sie, wie Anlagen aus Elementen löschen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 458331f81493283efc20d24c7e2bebe0e74bbdbd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756888"
---
# <a name="delete-attachments-by-using-ews-in-exchange"></a><span data-ttu-id="945bc-103">Löschen von Anlagen mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="945bc-103">Delete attachments by using EWS in Exchange</span></span>

<span data-ttu-id="945bc-104">Erfahren Sie, wie Anlagen aus Elementen löschen, indem Sie die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="945bc-104">Learn how to delete attachments from items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="945bc-105">Wenn es zum Löschen der Datei und Anlagen aus Elementen geht mithilfe der EWS Managed API, stehen Ihnen eine Reihe von Optionen.</span><span class="sxs-lookup"><span data-stu-id="945bc-105">You have a number of options when it comes to deleting file and item attachments from items by using the EWS Managed API.</span></span> <span data-ttu-id="945bc-106">Sie können Löschen aller Anlagen aus der Nachricht, löschen, indem Sie einen Dateinamen ein, oder löschen, indem Sie Position in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="945bc-106">You can delete all the attachments from the message, delete by a file name, or delete by position in the collection.</span></span> <span data-ttu-id="945bc-107">Für jede dieser Optionen gibt es eine [AttachmentCollection](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection%28v=exchg.80%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="945bc-107">For each of these options, there is an [AttachmentCollection](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="945bc-108">Im Gegensatz dazu entspricht unabhängig davon, ob Sie alle Anlagen aus einem Element oder nur ein einziges, löschen möchten, dem mit Exchange-Webdienste, die Reihenfolge der Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="945bc-108">Conversely, with EWS, no matter whether you're deleting all attachments from an item or just one, the sequence of operations is same.</span></span> <span data-ttu-id="945bc-109">Im Gegensatz zu EWS Managed API enthält EWS getrennte Vorgänge zu löschenden keinen basierend auf den Namen oder die Position im Array Anlagen.</span><span class="sxs-lookup"><span data-stu-id="945bc-109">Unlike the EWS Managed API, EWS does not include separate operations to delete based on name or position in the attachments array.</span></span>
  
<span data-ttu-id="945bc-110">**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge zum Löschen von Anlagen**</span><span class="sxs-lookup"><span data-stu-id="945bc-110">**Table 1. EWS Managed API methods and EWS operations for deleting attachments**</span></span>

|<span data-ttu-id="945bc-111">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="945bc-111">**Task**</span></span>|<span data-ttu-id="945bc-112">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="945bc-112">**EWS Managed API method**</span></span>|<span data-ttu-id="945bc-113">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="945bc-113">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="945bc-114">Löschen Sie alle Anlagen aus einem Element.</span><span class="sxs-lookup"><span data-stu-id="945bc-114">Delete all attachments from an item.</span></span>  <br/> |<span data-ttu-id="945bc-115">[Item.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), gefolgt von [AttachmentCollection.Clear](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx), gefolgt von [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="945bc-115">[Item.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), followed by [AttachmentCollection.Clear](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx), followed by [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="945bc-116">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) gefolgt von [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="945bc-116">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) followed by [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="945bc-117">Löschen einer Anlage aus einem Element nach Namen.</span><span class="sxs-lookup"><span data-stu-id="945bc-117">Delete an attachment from an item by name.</span></span>  <br/> |<span data-ttu-id="945bc-118">[Item.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), gefolgt von [AttachmentCollection.Remove](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx), gefolgt von [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="945bc-118">[Item.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), followed by [AttachmentCollection.Remove](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx), followed by [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="945bc-119">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) gefolgt von [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="945bc-119">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) followed by [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="945bc-120">Löschen einer Anlage aus einem Element nach Position in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="945bc-120">Delete an attachment from an item by position in the collection.</span></span>  <br/> |<span data-ttu-id="945bc-121">[Item.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), gefolgt von [AttachmentCollection.RemoveAt](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.removeat%28v=exchg.80%29.aspx), gefolgt von [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="945bc-121">[Item.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), followed by [AttachmentCollection.RemoveAt](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.removeat%28v=exchg.80%29.aspx), followed by [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="945bc-122">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) gefolgt von [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="945bc-122">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) followed by [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span></span> <br/> |
   
## <a name="delete-all-attachments-from-an-email-by-using-the-ews-managed-api"></a><span data-ttu-id="945bc-123">Löschen Sie alle Anlagen aus einer e-Mail mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="945bc-123">Delete all attachments from an email by using the EWS Managed API</span></span>
<span data-ttu-id="945bc-124"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="945bc-124"></span></span>

<span data-ttu-id="945bc-125">Im folgenden Codebeispiel wird veranschaulicht, wie alle Anlagen aus einer e-Mail durch Löschen:</span><span class="sxs-lookup"><span data-stu-id="945bc-125">The following code example shows how to delete all attachments from an email by:</span></span>
  
1. <span data-ttu-id="945bc-126">Mithilfe der Methode [EmailMessage.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) Binden an eine vorhandene e-Mail-Nachricht und Abrufen der Auflistung von [Anlagen](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="945bc-126">Using the [EmailMessage.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message and retrieve the collection of [Attachments](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).</span></span>
    
2. <span data-ttu-id="945bc-127">Verwenden die [AttachmentCollection.Clear](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx) -Methode zum Löschen aller Anlagen aus der e-Mail.</span><span class="sxs-lookup"><span data-stu-id="945bc-127">Using the [AttachmentCollection.Clear](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx) method to delete all the attachments from the email.</span></span> 
    
3. <span data-ttu-id="945bc-128">Verwenden die [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) -Methode, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="945bc-128">Using the [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
    
<span data-ttu-id="945bc-129">In diesem Beispiel wird davon ausgegangen, dass **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, **ItemId** ist die [ItemId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) der Nachricht aus der Anlagen gelöscht werden, und der Benutzer an einen Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="945bc-129">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, **itemId** is the [ItemId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the message from which attachments will be deleted, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void DeleteAllAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Delete all attachments from the message.
    message.Attachments.Clear();
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-an-attachment-by-name-from-an-email-by-using-the-ews-managed-api"></a><span data-ttu-id="945bc-130">Löschen einer Anlage nach Namen aus einer e-Mail mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="945bc-130">Delete an attachment by name from an email by using the EWS Managed API</span></span>
<span data-ttu-id="945bc-131"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="945bc-131"></span></span>

<span data-ttu-id="945bc-132">Das folgende Beispiel zeigt für Code Löschen einer Anlage wie namentlich durch:</span><span class="sxs-lookup"><span data-stu-id="945bc-132">The following code example shows how delete an attachment by name by:</span></span>
  
1. <span data-ttu-id="945bc-133">Mithilfe der Methode [EmailMessage.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) Binden an eine vorhandene e-Mail-Nachricht und Abrufen der Auflistung von [Anlagen](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="945bc-133">Using the [EmailMessage.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message and retrieve the collection of [Attachments](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).</span></span>
    
2. <span data-ttu-id="945bc-134">Verwenden die [AttachmentCollection.Remove](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) -Methode zum Löschen einer Anlage, die mit dem Namen FileAttachment.txt.</span><span class="sxs-lookup"><span data-stu-id="945bc-134">Using the [AttachmentCollection.Remove](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) method to delete an attachment named FileAttachment.txt.</span></span> 
    
3. <span data-ttu-id="945bc-135">Verwenden die [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) -Methode, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="945bc-135">Using the [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
    
<span data-ttu-id="945bc-136">In diesem Beispiel wird davon ausgegangen, dass **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, **ItemId** ist die [ItemId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) der Nachricht aus der Anlage gelöscht werden soll, und der Benutzer an einen Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="945bc-136">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, **itemId** is the [ItemId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the message from which the attachment will be deleted, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void DeleteNamedAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Iterate through the attachments collection and delete the attachment named "FileAttachment.txt," if it exists.
    foreach (Attachment attachment in message.Attachments)
    {
        if (attachment.Name == "FileAttachment.txt")
        {
            message.Attachments.Remove(attachment);
            break;
        }
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-by-position-by-using-the-ews-managed-api"></a><span data-ttu-id="945bc-137">Löschen von Anlagen mit einem Position mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="945bc-137">Delete attachments by position by using the EWS Managed API</span></span>
<span data-ttu-id="945bc-138"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="945bc-138"></span></span>

<span data-ttu-id="945bc-139">Im folgenden Codebeispiel wird veranschaulicht, wie eine Anlage nach Position durch Löschen:</span><span class="sxs-lookup"><span data-stu-id="945bc-139">The following code example shows how to delete an attachment by position by:</span></span>
  
1. <span data-ttu-id="945bc-140">Mithilfe der Methode [EmailMessage.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) Binden an eine vorhandene e-Mail-Nachricht und Abrufen der Auflistung von [Anlagen](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) und die [EmailMessage.HasAttachments](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="945bc-140">Using the [EmailMessage.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message and retrieve the collection of [Attachments](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) and the [EmailMessage.HasAttachments](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) property.</span></span> 
    
2. <span data-ttu-id="945bc-141">Verwenden die [AttachmentCollection.Remove](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) -Methode die erste Anlage in der Auflistung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="945bc-141">Using the [AttachmentCollection.Remove](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) method to delete the first attachment in the collection.</span></span> 
    
3. <span data-ttu-id="945bc-142">Verwenden die [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) -Methode, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="945bc-142">Using the [EmailMessage.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
    
<span data-ttu-id="945bc-143">In diesem Beispiel wird davon ausgegangen, dass **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, **ItemId** ist die [ItemId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) der Nachricht aus der Anlage gelöscht werden soll, und der Benutzer an einen Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="945bc-143">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, **itemId** is the [ItemId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the message from which the attachment will be deleted, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void DeleteAttachmentByPosition(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting the HasAttachments property and the attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(EmailMessageSchema.HasAttachments, ItemSchema.Attachments));
    // Remove attachments using the zero-based index position of the attachment in the attachments collection.
    if (message.HasAttachments)
    {
        message.Attachments.RemoveAt(0);
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-from-an-item-by-using-ews"></a><span data-ttu-id="945bc-144">Löschen von Anlagen aus einem Element mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="945bc-144">Delete attachments from an item by using EWS</span></span>
<span data-ttu-id="945bc-145"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="945bc-145"></span></span>

<span data-ttu-id="945bc-146">Zum Löschen von Anlagen mithilfe der Exchange-Webdienste, müssen Sie zuerst die Nachricht und die Anlage-Auflistung zum Bestimmen der [AttachmentId (GetAttachment und DeleteAttachment)](http://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) der Anlage zu löschenden abrufen.</span><span class="sxs-lookup"><span data-stu-id="945bc-146">To delete attachments by using EWS, you first need to retrieve the message and the attachment collection to determine the [AttachmentId (GetAttachment and DeleteAttachment)](http://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) of the attachment to delete.</span></span> <span data-ttu-id="945bc-147">Nachdem Sie einen oder mehrere **AttachmentId** Werte zu löschenden haben, rufen Sie den Vorgang [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) , um die angegebenen Anlagen aus der Nachricht zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="945bc-147">After you have one or more **AttachmentId** values to delete, call the [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) operation to remove the specified attachments from the message.</span></span> 
  
<span data-ttu-id="945bc-148">Im folgenden Codebeispiel wird veranschaulicht, wie der [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)-Vorgang zum Abrufen einer E-Mail und der Anlagenauflistung in der Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="945bc-148">The following code example shows how to use the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation to get an email message and the collection of attachments on the message.</span></span> <span data-ttu-id="945bc-149">Dies ist auch der erste XML-Anforderung, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Löschen aller Anlagen aus einer e-Mail](#bk_deleteattachewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="945bc-149">This is also the first XML request that the EWS Managed API sends when you use the EWS Managed API to [delete all attachments from an email](#bk_deleteattachewsma).</span></span> <span data-ttu-id="945bc-150">Die Werte einiger Attribute wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="945bc-150">The values of some attributes are shortened for readability.</span></span>
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Attachments" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="uqE1AAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="945bc-151">Der Server antwortet auf die **GetItem**-Anforderung mit einer [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/de-de/library/aa580757%28v=exchg.150%29.aspx)-Wert **NoError** umfasst, der angibt, dass die E-Mail erfolgreich abgerufen wurde, sowie [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)-Werte der vorhandenen Anlagen.</span><span class="sxs-lookup"><span data-stu-id="945bc-151">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/de-de/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was retrieved successfully, and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) values of the existing attachments.</span></span> 
  
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
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="uqE1AAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXulcd" />
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="IpHLObE=" />
                  <t:Name>FileAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="QuHSSmY=" />
                  <t:Name>SecondAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="qf2KoPo=" />
                  <t:Name>ThirdAttachment.jpg</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="NFQMnMc=" />
                  <t:Name>FourthAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:ItemAttachment>
                  <t:AttachmentId Id="jJvbLXQ=" />
                  <t:Name>Attached Message Item</t:Name>
                </t:ItemAttachment>
              </t:Attachments>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="945bc-152">Nach dem bestimmen Sie, welche Anlage zu löschen, rufen Sie den Vorgang [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) und gehören zu den Werten **AttachmentId** Anlagen löschen.</span><span class="sxs-lookup"><span data-stu-id="945bc-152">After you determine which attachment to delete, call the [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) operation and include the **AttachmentId** values of the attachments to delete.</span></span> 
  
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
    <m:DeleteAttachment>
      <m:AttachmentIds>
        <t:AttachmentId Id="IpHLObE=" />
        <t:AttachmentId Id="QuHSSmY=" />
        <t:AttachmentId Id="qf2KoPo=" />
        <t:AttachmentId Id="NFQMnMc=" />
        <t:AttachmentId Id="jJvbLXQ=" />
      </m:AttachmentIds>
    </m:DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die Anforderung **DeleteAttachment** mit einer [DeleteAttachmentResponse](http://msdn.microsoft.com/library/24099a88-4ab6-4bf3-8ed5-efec8e07b9b9%28Office.15%29.aspx) -Nachricht, die [ResponseCode](http://msdn.microsoft.com/de-de/library/aa580757%28v=exchg.150%29.aspx) Wert **NoError** für jede [DeleteAttachmentResponseMessage](http://msdn.microsoft.com/library/1edb085f-1674-48e5-8ec3-42351adeac7d%28Office.15%29.aspx)enthält, die jede Anlage wurde gelöscht. <span data-ttu-id="945bc-154">Die Werte einiger Attribute wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="945bc-154">The values of some attributes are shortened for readability.</span></span>
  
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
    <m:DeleteAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:DeleteAttachmentResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="945bc-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="945bc-155">See also</span></span>


- [<span data-ttu-id="945bc-156">Attachments and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="945bc-156">Attachments and EWS in Exchange</span></span>](attachments-and-ews-in-exchange.md)
    
- [<span data-ttu-id="945bc-157">Hinzufügen von Anlagen im Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="945bc-157">Add attachments by using EWS in Exchange</span></span>](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="945bc-158">Abrufen von Anlagen im Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="945bc-158">Get attachments by using EWS in Exchange</span></span>](how-to-get-attachments-by-using-ews-in-exchange.md)
    

