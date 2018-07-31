---
title: Access-e-Mail eine Stellvertretung mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a8123604-c7c0-405d-a0ed-7a9b4a431bfd
description: Erfahren Sie, wie e-Mail als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 23dd35f95b1303ff643e3760aa408e308725cb12
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354036"
---
# <a name="access-email-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="e92d6-103">Access-e-Mail eine Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e92d6-103">Access email as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="e92d6-104">Erfahren Sie, wie e-Mail als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="e92d6-104">Learn how to access email as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="e92d6-105">Sie können die EWS Managed API verwenden oder EWS so erteilen Sie einen Benutzer delegieren des Zugriffs auf eine Postfachbesitzer Posteingangsordner.</span><span class="sxs-lookup"><span data-stu-id="e92d6-105">You can use the EWS Managed API or EWS to give a user delegate access to a mailbox owner's Inbox folder.</span></span> <span data-ttu-id="e92d6-106">Die Stellvertretung kann Klicken Sie dann Erstellen von Besprechungsanfragen im Auftrag des Postfachbesitzers, für e-Mails, suchen und abrufen, aktualisieren, und löschen e-Mail aus dem Ordner Posteingang des Postfachbesitzers abhängig von ihren Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="e92d6-106">The delegate can then create meeting requests on behalf of the mailbox owner, search for email, and retrieve, update, and delete email from the mailbox owner's Inbox folder, depending on their permissions.</span></span>
  
<span data-ttu-id="e92d6-107">Als Stellvertretung verwenden Sie die gleichen Methoden und Vorgänge des Postfachbesitzers zum Zugreifen auf Posteingang, mit denen Sie einen Posteingangsordner ohne Stellvertretungszugriff zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e92d6-107">As a delegate, you use the same methods and operations to access a mailbox owner's Inbox folder that you use to access an Inbox folder without delegate access.</span></span> <span data-ttu-id="e92d6-108">Der Hauptunterschied ist, dass Sie mithilfe von [expliziten Access](delegate-access-and-ews-in-exchange.md#bk_explicit) suchen oder erstellen ein e-Mail-Element, und klicken Sie dann, nachdem Sie die Element-ID identifiziert haben, können [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) erhalten möchten, aktualisieren und Löschen des Elements.</span><span class="sxs-lookup"><span data-stu-id="e92d6-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create an email item, and then after you identify the item ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="e92d6-109">**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für den Zugriff auf e-Mail als Stellvertreter**</span><span class="sxs-lookup"><span data-stu-id="e92d6-109">**Table 1. EWS Managed API methods and EWS operations for accessing email as a delegate**</span></span>

|<span data-ttu-id="e92d6-110">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="e92d6-110">**If you want to…**</span></span>|<span data-ttu-id="e92d6-111">**Verwenden Sie diese Methode EWS Managed API...**</span><span class="sxs-lookup"><span data-stu-id="e92d6-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="e92d6-112">**Verwenden Sie diese Operation EWS...**</span><span class="sxs-lookup"><span data-stu-id="e92d6-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e92d6-113">Erstellen und Senden einer e-Mails als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="e92d6-113">Create and send an email as a delegate</span></span>  <br/> |<span data-ttu-id="e92d6-114">[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) , in dem der [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Ordner "Entwürfe" enthält</span><span class="sxs-lookup"><span data-stu-id="e92d6-114">[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Drafts folder</span></span>  <br/> <span data-ttu-id="e92d6-115">[EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) , in dem der Parameter [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer gesendete Objekte Ordner enthält</span><span class="sxs-lookup"><span data-stu-id="e92d6-115">[EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Sent Items folder</span></span>  <br/> |<span data-ttu-id="e92d6-116">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers</span><span class="sxs-lookup"><span data-stu-id="e92d6-116">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> <span data-ttu-id="e92d6-117">[Den SendItem](http://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers</span><span class="sxs-lookup"><span data-stu-id="e92d6-117">[SendItem](http://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="e92d6-118">Erstellen Sie mehrere e-Mail-Nachrichten als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="e92d6-118">Create multiple email messages as a delegate</span></span>  <br/> |<span data-ttu-id="e92d6-119">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Posteingangsordner enthält</span><span class="sxs-lookup"><span data-stu-id="e92d6-119">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Inbox folder</span></span>  <br/> |<span data-ttu-id="e92d6-120">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers</span><span class="sxs-lookup"><span data-stu-id="e92d6-120">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="e92d6-121">Suchen Sie nach oder suchen Sie nach einer e-Mail als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="e92d6-121">Search for or find an email as a delegate</span></span>  <br/> |<span data-ttu-id="e92d6-122">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Posteingangsordner enthält</span><span class="sxs-lookup"><span data-stu-id="e92d6-122">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Inbox folder</span></span>  <br/> |<span data-ttu-id="e92d6-123">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers</span><span class="sxs-lookup"><span data-stu-id="e92d6-123">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="e92d6-124">Abrufen einer e-Mails als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="e92d6-124">Get an email as a delegate</span></span>  <br/> |[<span data-ttu-id="e92d6-125">EmailMessage.Bind</span><span class="sxs-lookup"><span data-stu-id="e92d6-125">EmailMessage.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="e92d6-126">GetItem</span><span class="sxs-lookup"><span data-stu-id="e92d6-126">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="e92d6-127">Aktualisieren einer e-Mails als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="e92d6-127">Update an email as a delegate</span></span>  <br/> |<span data-ttu-id="e92d6-128">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e92d6-128">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="e92d6-129">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e92d6-129">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="e92d6-130">Löschen Sie eine e-Mail als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="e92d6-130">Delete an email as a delegate</span></span>  <br/> |<span data-ttu-id="e92d6-131">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [EmailMessage.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e92d6-131">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [EmailMessage.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="e92d6-132">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="e92d6-132">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |
   
<span data-ttu-id="e92d6-133">Beachten Sie Folgendes im Hinterkopf beim Arbeiten mit e-Mail-Nachrichten als Stellvertreter:</span><span class="sxs-lookup"><span data-stu-id="e92d6-133">Keep the following things in mind when working with emails as a delegate:</span></span>
  
- <span data-ttu-id="e92d6-134">Wenn nur eine Stellvertretung Besprechungsanfragen und-Antworten entwickelt muss, ist die Stellvertretung Zugriff auf den Ordner Posteingang nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e92d6-134">If a delegate only needs to work with meeting requests and responses, the delegate does not need access to the Inbox folder.</span></span> <span data-ttu-id="e92d6-135">Weitere Informationen finden Sie unter [erforderlichen Aufgaben für den Zugriff auf Kalender als Stellvertreter](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq).</span><span class="sxs-lookup"><span data-stu-id="e92d6-135">For more information, see [prerequisite tasks for accessing calendars as a delegate](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq).</span></span>
    
- <span data-ttu-id="e92d6-136">Wenn ein Empfänger eine Nachricht, die im Namen einer Postfachbesitzer gesendet wurde empfängt, ist der Absender " *Delegaten* im Namen *des Besitzers des Zielpostfachs* ."</span><span class="sxs-lookup"><span data-stu-id="e92d6-136">When a recipient receives a message that was sent on behalf of a mailbox owner, the sender appears as " *Delegate*  on behalf of  *mailbox owner*  ."</span></span> 
    
> [!NOTE]
> <span data-ttu-id="e92d6-137">In den Codebeispielen in diesem Artikel ist primary@contoso.com der Postfachbesitzer.</span><span class="sxs-lookup"><span data-stu-id="e92d6-137">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 
  
## <a name="prerequisite-tasks"></a><span data-ttu-id="e92d6-138">Erforderliche Aufgaben</span><span class="sxs-lookup"><span data-stu-id="e92d6-138">Prerequisite tasks</span></span>
<span data-ttu-id="e92d6-139"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="e92d6-139"></span></span>

<span data-ttu-id="e92d6-140">Bevor ein Benutzer des Postfachbesitzers Posteingangsordner als Stellvertreter zugreifen kann, muss der Benutzer des Postfachbesitzers Posteingangsordner [als Stellvertreter mit Berechtigungen hinzugefügt](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) .</span><span class="sxs-lookup"><span data-stu-id="e92d6-140">Before a user can access the mailbox owner's Inbox folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Inbox folder.</span></span> 
  
## <a name="create-and-send-an-email-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="e92d6-141">Erstellen und Senden einer e-Mails eine Stellvertretung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="e92d6-141">Create and send an email as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="e92d6-142"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e92d6-142"></span></span>

<span data-ttu-id="e92d6-143">Die EWS Managed API können Sie das Objekt für den Benutzer Delegaten erstellen und Senden von e-Mails im Auftrag des Postfachbesitzers verwenden.</span><span class="sxs-lookup"><span data-stu-id="e92d6-143">The EWS Managed API enables you to use the service object for the delegate user to create and send email on behalf of the mailbox owner.</span></span> <span data-ttu-id="e92d6-144">In diesem Beispiel wird gezeigt, wie die [Speichern](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) -Methode, um die Nachricht im Ordner "Entwürfe" des Postfachbesitzers speichern, und klicken Sie dann die [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) -Methode, um die e-Mail-Nachricht senden, und speichern Sie die Nachricht im Ordner des Postfachbesitzers-gesendete Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="e92d6-144">This example shows how to use the [Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) method to save the message in the mailbox owner's Drafts folder, and then the [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) method to send the mail and save the message in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="e92d6-145">In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Delegaten und, die der Stellvertreter die [entsprechenden Berechtigungen für den Postfachbesitzer Posteingang, Entwürfe und gesendete Objekte Ordner](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="e92d6-145">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the [appropriate permissions for the mailbox owner's Inbox, Drafts, and Sent Items folder](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
```cs
public static void DelegateAccessCreateEmail(ExchangeService service)
{
    // Create an email message and provide it with connection 
    // configuration information by using an ExchangeService 
    // object named service.
    EmailMessage message = new EmailMessage(service);
    // Set properties on the email message.
    message.Subject = "Company Soccer Team";
    message.Body = "Are you interested in joining?";
    message.ToRecipients.Add("sadie@contoso.com");
    // Save the email to the mailbox owner's Drafts folder.
    // This method call results in a CreateItem call to EWS.
    // The FolderId parameter contains the context for the 
    // mailbox owner's Inbox folder. Any additional actions 
    // taken on this message will be performed in the mailbox 
    // owner's mailbox. 
    message.Save(new FolderId(WellKnownFolderName.Drafts, new Mailbox("primary@contoso.com")));
    // Send the email and save the message in the mailbox owner's 
    // Sent Items folder.
    // This method call results in a SendItem call to EWS.
    message.SendAndSaveCopy(new FolderId(WellKnownFolderName.SentItems, new Mailbox("primary@contoso.com")));
    Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" 
    + message.ToRecipients[0] + "' and saved in the Sent Items folder of the mailbox owner.");
}
```

## <a name="create-and-send-an-email-as-a-delegate-by-using-ews"></a><span data-ttu-id="e92d6-146">Erstellen und Senden einer e-Mails eine Stellvertretung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="e92d6-146">Create and send an email as a delegate by using EWS</span></span>
<span data-ttu-id="e92d6-147"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="e92d6-147"></span></span>

<span data-ttu-id="e92d6-148">Exchange-Webdienste können Sie das Objekt für den Benutzer Delegaten erstellen und Senden von e-Mails im Auftrag des Postfachbesitzers verwenden.</span><span class="sxs-lookup"><span data-stu-id="e92d6-148">EWS enables you to use the service object for the delegate user to create and send email on behalf of the mailbox owner.</span></span> <span data-ttu-id="e92d6-149">Dieses Beispiel zeigt, wie Sie den [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgang verwenden, um eine e-Mail-Nachricht und [den SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang zum Senden der Zeit und speichern Sie sie im Ordner des Postfachbesitzers-gesendete Objekte erstellen.</span><span class="sxs-lookup"><span data-stu-id="e92d6-149">This example shows how to use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create an email and the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation to send the time and save it in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="e92d6-150">Dies ist auch der erste XML-Anforderung, die die EWS Managed API sendet, wenn Sie die **Speichern** -Methode zum [Erstellen und senden eine e-Mail](#bk_createewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="e92d6-150">This is also the first XML request that the EWS Managed API sends when you use the **Save** method to [create and send an email](#bk_createewsma).</span></span>
  
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
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
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

<span data-ttu-id="e92d6-151">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die e-Mail-Nachricht erstellt und erfolgreich gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="e92d6-151">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the email was created and saved successfully.</span></span> <span data-ttu-id="e92d6-152">Die Antwort enthält auch die Element-ID der neu erstellten e-Mail.</span><span class="sxs-lookup"><span data-stu-id="e92d6-152">The response also contains the item ID of the newly created email.</span></span>
  
<span data-ttu-id="e92d6-153">Der Wert **ItemId** wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="e92d6-153">The **ItemId** value has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="iNRaAAA="
                        ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
            </t:Message>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="e92d6-154">Verwenden Sie im nächsten Schritt **den SendItem** -Vorgang so senden Sie die Nachricht im Auftrag des Postfachbesitzers und speichern sie im Ordner des Postfachbesitzers-gesendete Objekte.</span><span class="sxs-lookup"><span data-stu-id="e92d6-154">Next, use the **SendItem** operation to send the message on behalf of the mailbox owner and save it in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="e92d6-155">Der Wert **ItemId** wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="e92d6-155">The **ItemId** value has been shortened for readability.</span></span> 
  
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
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="iNRaAAA="
                  ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e92d6-156">Der Server antwortet auf die Anforderung **den SendItem** mit einer [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die e-Mail-Nachricht gesendet und gesendete Elemente im Ordner des Postfachbesitzers gespeichert wurde erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e92d6-156">The server responds to the **SendItem** request with a [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the email was sent and saved to the mailbox owner's Sent Items folder successfully.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:SendItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </m:SendItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="search-for-an-email-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="e92d6-157">Suchen Sie nach einer e-Mail eine Stellvertretung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="e92d6-157">Search for an email as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="e92d6-158"><a name="bk_searchewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e92d6-158"></span></span>

<span data-ttu-id="e92d6-159">Um eine e-Mail-Nachricht zu suchen, müssen Sie eine der Methoden [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , die einen [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter enthält verwenden, damit Sie den Postfachbesitzer Posteingangsordner angeben können.</span><span class="sxs-lookup"><span data-stu-id="e92d6-159">To search for an email, you must use one of the [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) methods that includes a [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Inbox folder.</span></span> 
  
```cs
static void DelegateAccessSearchEmailWithFilter(ExchangeService service)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    // Define the search filter.
    SearchFilter.ContainsSubstring filter = new SearchFilter.ContainsSubstring(ItemSchema.Subject, 
        "soccer", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching Inbox items. 
        // The parameters of FindItems must denote the mailbox owner,
        // mailbox, and Inbox folder.
        // This call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(new 
            FolderId(WellKnownFolderName.Inbox, "primary@contoso.com"), 
            filter, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

<span data-ttu-id="e92d6-160">Nach Beendigung des **FindItems** Aufrufs eine Antwort mit einer ID, müssen Sie erhalten können, aktualisieren oder löschen, die per e-Mail mit der ID und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) – und Sie nicht die SMTP-Adresse des Postfachbesitzers angeben.</span><span class="sxs-lookup"><span data-stu-id="e92d6-160">After the **FindItems** call returns a response with an ID, you can get, update or delete that email by using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) - and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="search-for-an-email-as-a-delegate-by-using-ews"></a><span data-ttu-id="e92d6-161">Suchen Sie nach einer e-Mail eine Stellvertretung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="e92d6-161">Search for an email as a delegate by using EWS</span></span>
<span data-ttu-id="e92d6-162"><a name="bk_searchews"> </a></span><span class="sxs-lookup"><span data-stu-id="e92d6-162"></span></span>

<span data-ttu-id="e92d6-163">EWS können Sie mit dem Dienstobjekt für den Benutzer Delegaten-e-Mails zu suchen, die einen Satz von Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="e92d6-163">EWS enables you to use the service object for the delegate user to search for emails that meet a set of search criteria.</span></span> <span data-ttu-id="e92d6-164">In diesem Beispiel wird veranschaulicht, wie Sie den Vorgang [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) zum Suchen von Nachrichten in den Besitzer Posteingangsordner, die das Wort "Fußball" im Betreff enthalten.</span><span class="sxs-lookup"><span data-stu-id="e92d6-164">This example shows how to use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find messages in the owner's Inbox folder that contain the word "soccer" in the subject.</span></span> 
  
<span data-ttu-id="e92d6-165">Dies ist auch, dass die EWS Managed API, wenn gesendet die XML-Anfrage [Suchen nach einer e-Mail](#bk_searchewsma).</span><span class="sxs-lookup"><span data-stu-id="e92d6-165">This is also the XML request that the EWS Managed API sends when you [search for an email](#bk_searchewsma).</span></span>
  
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
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:Restriction>
        <t:Contains ContainmentMode="Substring"
                    ContainmentComparison="IgnoreCase">
          <t:FieldURI FieldURI="item:Subject" />
          <t:Constant Value="soccer" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e92d6-166">Der Server antwortet auf die Anforderung **FindItem** mit einer [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) Element **noError zurück**, das anzeigt, dass die Suche erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e92d6-166">The server responds to the **FindItem** request with a [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the search completed successfully.</span></span> <span data-ttu-id="e92d6-167">Die Antwort enthält das Element für eine [Nachricht](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) für alle e-Mails, die die Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="e92d6-167">The response contains a [Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) element for any emails that met the search criteria.</span></span> <span data-ttu-id="e92d6-168">In diesem Fall wird nur eine e-Mail-gefunden.</span><span class="sxs-lookup"><span data-stu-id="e92d6-168">In this case, only one email is found.</span></span> 
  
<span data-ttu-id="e92d6-169">Der Wert des Elements [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="e92d6-169">The value of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1"
                        TotalItemsInView="1"
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="iNwoAAA="
                          ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQuu" />
                <t:Subject>Soccer team</t:Subject>
                <t:DateTimeReceived>2014-03-10T06:16:55Z</t:DateTimeReceived>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="e92d6-170">Nun, da Sie die **ItemId** für die e-Mail-Nachricht verfügen, die die Kriterien erfüllt, müssen Sie erhalten können, Update- oder Delete, die mithilfe der **ItemId** und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) – und Sie per e-Mail nicht die SMTP-Adresse des Postfachbesitzers angeben.</span><span class="sxs-lookup"><span data-stu-id="e92d6-170">Now that you have the **ItemId** for the email that meets your criteria, you can get, update, or delete that email by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) - and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="e92d6-171">Abrufen, aktualisieren oder Löschen von e-Mail-Elementen als Stellvertretung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="e92d6-171">Get, update, or delete email items as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="e92d6-172"><a name="bk_geteswma"> </a></span><span class="sxs-lookup"><span data-stu-id="e92d6-172"></span></span>

<span data-ttu-id="e92d6-173">Die EWS Managed API können Sie abrufen, aktualisieren oder Löschen einer e-Mails in die gleiche Weise, die Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="e92d6-173">You can use the EWS Managed API to get, update, or delete an email in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="e92d6-174">Der einzige Unterschied ist, dass das **ExchangeService** -Objekt für den Benutzer Delegat ist.</span><span class="sxs-lookup"><span data-stu-id="e92d6-174">The only difference is that the **ExchangeService** object is for the delegate user.</span></span> <span data-ttu-id="e92d6-175">Die Element-ID im Methodenaufruf **binden** enthalten sind, eindeutig identifiziert das Element im Postfachspeicher im Posteingang des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="e92d6-175">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Inbox folder.</span></span> 
  
<span data-ttu-id="e92d6-176">**In Tabelle 2. Arbeiten mit e-Mail als Stellvertreter EWS Managed API-Methoden**</span><span class="sxs-lookup"><span data-stu-id="e92d6-176">**Table 2. EWS Managed API methods working with email as a delegate**</span></span>

|<span data-ttu-id="e92d6-177">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="e92d6-177">**Task**</span></span>|<span data-ttu-id="e92d6-178">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="e92d6-178">**EWS Managed API method**</span></span>|<span data-ttu-id="e92d6-179">**Code example**</span><span class="sxs-lookup"><span data-stu-id="e92d6-179">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e92d6-180">E-Mail senden</span><span class="sxs-lookup"><span data-stu-id="e92d6-180">Get an email</span></span>  <br/> |[<span data-ttu-id="e92d6-181">Bind</span><span class="sxs-lookup"><span data-stu-id="e92d6-181">Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="e92d6-182">Abrufen eines Elements mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="e92d6-182">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="e92d6-183">Aktualisieren einer e-Mails</span><span class="sxs-lookup"><span data-stu-id="e92d6-183">Update an email</span></span>  <br/> |<span data-ttu-id="e92d6-184">[Binden von](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e92d6-184">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="e92d6-185">Aktualisieren eines Elements mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="e92d6-185">Update an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|<span data-ttu-id="e92d6-186">Löschen einer e-Mails</span><span class="sxs-lookup"><span data-stu-id="e92d6-186">Delete an email</span></span>  <br/> |<span data-ttu-id="e92d6-187">[Binden von](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Löschen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e92d6-187">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="e92d6-188">Löschen eines Elements mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="e92d6-188">Delete an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |
   
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="e92d6-189">Abrufen, aktualisieren oder Löschen von e-Mail-Elementen als Stellvertretung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="e92d6-189">Get, update, or delete email items as a delegate by using EWS</span></span>
<span data-ttu-id="e92d6-190"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="e92d6-190"></span></span>

<span data-ttu-id="e92d6-191">Die EWS Managed API können Sie abrufen, aktualisieren oder Löschen einer e-Mails in die gleiche Weise, die Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="e92d6-191">You can use the EWS Managed API to get, update, or delete an email in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="e92d6-192">Der einzige Unterschied ist, dass das Objekt für den Benutzer Delegat ist.</span><span class="sxs-lookup"><span data-stu-id="e92d6-192">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="e92d6-193">Die Element-ID, enthalten in der **GetItem** -Anforderung eindeutig identifiziert das Element im Postfachspeicher im Posteingang des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="e92d6-193">The item ID included in the **GetItem** request uniquely identifies the item in the mailbox store, in the mailbox owner's Inbox folder.</span></span> 
  
<span data-ttu-id="e92d6-194">**Tabelle 3. EWS-Vorgänge für das Arbeiten mit e-Mail als Stellvertreter**</span><span class="sxs-lookup"><span data-stu-id="e92d6-194">**Table 3. EWS operations for working with email as a delegate**</span></span>

|<span data-ttu-id="e92d6-195">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="e92d6-195">**Task**</span></span>|<span data-ttu-id="e92d6-196">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="e92d6-196">**EWS operation**</span></span>|<span data-ttu-id="e92d6-197">**Code example**</span><span class="sxs-lookup"><span data-stu-id="e92d6-197">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e92d6-198">E-Mail senden</span><span class="sxs-lookup"><span data-stu-id="e92d6-198">Get an email</span></span>  <br/> |[<span data-ttu-id="e92d6-199">GetItem</span><span class="sxs-lookup"><span data-stu-id="e92d6-199">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="e92d6-200">Abrufen eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="e92d6-200">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="e92d6-201">Aktualisieren einer e-Mails</span><span class="sxs-lookup"><span data-stu-id="e92d6-201">Update an email</span></span>  <br/> |<span data-ttu-id="e92d6-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e92d6-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="e92d6-203">Aktualisieren eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="e92d6-203">Update an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|<span data-ttu-id="e92d6-204">Löschen einer e-Mails</span><span class="sxs-lookup"><span data-stu-id="e92d6-204">Delete an email</span></span>  <br/> |<span data-ttu-id="e92d6-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="e92d6-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |[<span data-ttu-id="e92d6-206">Löschen eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="e92d6-206">Delete an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e92d6-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e92d6-207">See also</span></span>

- [<span data-ttu-id="e92d6-208">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e92d6-208">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)    
- [<span data-ttu-id="e92d6-209">Hinzufügen und Entfernen von Stellvertretungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e92d6-209">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="e92d6-210">Legen Sie Berechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e92d6-210">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="e92d6-211">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e92d6-211">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    

