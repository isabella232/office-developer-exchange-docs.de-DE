---
title: Zugreifen auf E-Mails als Stellvertretung mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a8123604-c7c0-405d-a0ed-7a9b4a431bfd
description: Informationen zum Zugreifen auf e-Mails als Stellvertretung mithilfe der verwaltete EWS-API oder EWS in Exchange.
ms.openlocfilehash: 0c26f69042c568fe7d877778c7d8f1e689e5b372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528286"
---
# <a name="access-email-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="31e61-103">Zugreifen auf E-Mails als Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="31e61-103">Access email as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="31e61-104">Informationen zum Zugreifen auf e-Mails als Stellvertretung mithilfe der verwaltete EWS-API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="31e61-104">Learn how to access email as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="31e61-105">Sie können die verwaltete EWS-API oder EWS verwenden, um einem Benutzer Stellvertretungszugriff auf den Posteingangsordner eines Postfachbesitzers zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="31e61-105">You can use the EWS Managed API or EWS to give a user delegate access to a mailbox owner's Inbox folder.</span></span> <span data-ttu-id="31e61-106">Der Stellvertreter kann dann Besprechungsanfragen im Auftrag des Postfachbesitzers erstellen, nach e-Mails suchen und e-Mails aus dem Posteingang-Ordner des Postfachbesitzers abrufen, aktualisieren und löschen, je nach den Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="31e61-106">The delegate can then create meeting requests on behalf of the mailbox owner, search for email, and retrieve, update, and delete email from the mailbox owner's Inbox folder, depending on their permissions.</span></span>
  
<span data-ttu-id="31e61-107">Als Stellvertretung verwenden Sie dieselben Methoden und Vorgänge, um auf den Posteingangsordner eines Postfachbesitzers zuzugreifen, den Sie für den Zugriff auf einen Posteingangsordner ohne Stellvertretungszugriff verwenden.</span><span class="sxs-lookup"><span data-stu-id="31e61-107">As a delegate, you use the same methods and operations to access a mailbox owner's Inbox folder that you use to access an Inbox folder without delegate access.</span></span> <span data-ttu-id="31e61-108">Der Hauptunterschied besteht darin, dass Sie [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicit) zum Suchen oder Erstellen eines e-Mail-Elements verwenden müssen, und nachdem Sie die Element-ID identifiziert haben, können Sie [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) zum Abrufen, aktualisieren oder Löschen des Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="31e61-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create an email item, and then after you identify the item ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="31e61-109">**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge für den Zugriff auf e-Mails als Stellvertretung**</span><span class="sxs-lookup"><span data-stu-id="31e61-109">**Table 1. EWS Managed API methods and EWS operations for accessing email as a delegate**</span></span>

|<span data-ttu-id="31e61-110">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="31e61-110">**If you want to…**</span></span>|<span data-ttu-id="31e61-111">**Verwenden Sie diese verwaltete EWS-API-Methode...**</span><span class="sxs-lookup"><span data-stu-id="31e61-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="31e61-112">**Verwenden Sie diesen EWS-Vorgang...**</span><span class="sxs-lookup"><span data-stu-id="31e61-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="31e61-113">Erstellen und Senden einer e-Mail als Stellvertretung</span><span class="sxs-lookup"><span data-stu-id="31e61-113">Create and send an email as a delegate</span></span>  <br/> |<span data-ttu-id="31e61-114">[Email Message. Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) , wobei der [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Ordner "Entwürfe" des Postfachbesitzers bereitstellt</span><span class="sxs-lookup"><span data-stu-id="31e61-114">[EmailMessage.Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Drafts folder</span></span>  <br/> <span data-ttu-id="31e61-115">[Email Message. SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) , wobei der [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Ordner "Gesendete Elemente" des Postfachbesitzers bereitstellt</span><span class="sxs-lookup"><span data-stu-id="31e61-115">[EmailMessage.SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Sent Items folder</span></span>  <br/> |<span data-ttu-id="31e61-116">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt</span><span class="sxs-lookup"><span data-stu-id="31e61-116">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> <span data-ttu-id="31e61-117">[SendItem](https://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt</span><span class="sxs-lookup"><span data-stu-id="31e61-117">[SendItem](https://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="31e61-118">Erstellen mehrerer e-Mail-Nachrichten als Stellvertretung</span><span class="sxs-lookup"><span data-stu-id="31e61-118">Create multiple email messages as a delegate</span></span>  <br/> |<span data-ttu-id="31e61-119">[Datei "ExchangeService. CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , wobei der **Folder** -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Posteingangsordner des Postfachbesitzers ermöglicht</span><span class="sxs-lookup"><span data-stu-id="31e61-119">[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Inbox folder</span></span>  <br/> |<span data-ttu-id="31e61-120">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt</span><span class="sxs-lookup"><span data-stu-id="31e61-120">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="31e61-121">Suchen nach oder Suchen einer e-Mail als Stellvertretung</span><span class="sxs-lookup"><span data-stu-id="31e61-121">Search for or find an email as a delegate</span></span>  <br/> |<span data-ttu-id="31e61-122">[Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , wobei der **Folder** -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Posteingangsordner des Postfachbesitzers ermöglicht</span><span class="sxs-lookup"><span data-stu-id="31e61-122">[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Inbox folder</span></span>  <br/> |<span data-ttu-id="31e61-123">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt</span><span class="sxs-lookup"><span data-stu-id="31e61-123">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="31e61-124">Abrufen einer e-Mail als Stellvertretung</span><span class="sxs-lookup"><span data-stu-id="31e61-124">Get an email as a delegate</span></span>  <br/> |[<span data-ttu-id="31e61-125">EmailMessage.Bind</span><span class="sxs-lookup"><span data-stu-id="31e61-125">EmailMessage.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="31e61-126">GetItem</span><span class="sxs-lookup"><span data-stu-id="31e61-126">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="31e61-127">Aktualisieren einer e-Mail als Stellvertretung</span><span class="sxs-lookup"><span data-stu-id="31e61-127">Update an email as a delegate</span></span>  <br/> |<span data-ttu-id="31e61-128">[Email Message. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Email Message. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31e61-128">[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="31e61-129">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31e61-129">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="31e61-130">Löschen einer e-Mail als Stellvertretung</span><span class="sxs-lookup"><span data-stu-id="31e61-130">Delete an email as a delegate</span></span>  <br/> |<span data-ttu-id="31e61-131">[Email Message. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Email Message. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31e61-131">[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [EmailMessage.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="31e61-132">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="31e61-132">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |
   
<span data-ttu-id="31e61-133">Beachten Sie beim Arbeiten mit e-Mails als Stellvertretung Folgendes:</span><span class="sxs-lookup"><span data-stu-id="31e61-133">Keep the following things in mind when working with emails as a delegate:</span></span>
  
- <span data-ttu-id="31e61-134">Wenn eine Stellvertretung nur mit Besprechungsanfragen und-Antworten arbeiten muss, benötigt die Stellvertretung keinen Zugriff auf den Ordner Posteingang.</span><span class="sxs-lookup"><span data-stu-id="31e61-134">If a delegate only needs to work with meeting requests and responses, the delegate does not need access to the Inbox folder.</span></span> <span data-ttu-id="31e61-135">Weitere Informationen finden Sie unter [erforderliche Aufgaben für den Zugriff auf Kalender als Stellvertreter](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq).</span><span class="sxs-lookup"><span data-stu-id="31e61-135">For more information, see [prerequisite tasks for accessing calendars as a delegate](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq).</span></span>
    
- <span data-ttu-id="31e61-136">Wenn ein Empfänger eine Nachricht empfängt, die im Auftrag eines Postfachbesitzers gesendet wurde, wird der Absender als " *Stellvertreter* im Auftrag des *Postfachbesitzers* " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31e61-136">When a recipient receives a message that was sent on behalf of a mailbox owner, the sender appears as " *Delegate*  on behalf of  *mailbox owner*  ."</span></span> 
    
> [!NOTE]
> <span data-ttu-id="31e61-137">In den Codebeispielen in diesem Artikel ist Primary@contoso.com der Postfachbesitzer.</span><span class="sxs-lookup"><span data-stu-id="31e61-137">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 
  
## <a name="prerequisite-tasks"></a><span data-ttu-id="31e61-138">Erforderliche Aufgaben</span><span class="sxs-lookup"><span data-stu-id="31e61-138">Prerequisite tasks</span></span>
<span data-ttu-id="31e61-139"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="31e61-139"><a name="bk_prereq"> </a></span></span>

<span data-ttu-id="31e61-140">Bevor ein Benutzer als Stellvertreter auf den Posteingangsordner des Postfachbesitzers zugreifen kann, muss der Benutzer [als Stellvertreter mit Berechtigungen](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) für den Posteingang-Ordner des Postfachbesitzers hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="31e61-140">Before a user can access the mailbox owner's Inbox folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Inbox folder.</span></span> 
  
## <a name="create-and-send-an-email-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="31e61-141">Erstellen und Senden einer e-Mail als Stellvertretung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="31e61-141">Create and send an email as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="31e61-142"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="31e61-142"><a name="bk_createewsma"> </a></span></span>

<span data-ttu-id="31e61-143">Mit dem verwaltete EWS-API können Sie das Dienstobjekt für den Stellvertreter verwenden, um e-Mails im Auftrag des Postfachbesitzers zu erstellen und zu senden.</span><span class="sxs-lookup"><span data-stu-id="31e61-143">The EWS Managed API enables you to use the service object for the delegate user to create and send email on behalf of the mailbox owner.</span></span> <span data-ttu-id="31e61-144">In diesem Beispiel wird gezeigt, wie Sie die [Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) -Methode verwenden, um die Nachricht im Ordner "Entwürfe" des Postfachbesitzers zu speichern, und dann die [SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) -Methode zum Senden der e-Mail und Speichern der Nachricht im Ordner "Gesendete Elemente" des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="31e61-144">This example shows how to use the [Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) method to save the message in the mailbox owner's Drafts folder, and then the [SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) method to send the mail and save the message in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="31e61-145">In diesem Beispiel wird davon ausgegangen, dass **Service** ein gültiges [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für die Stellvertretung ist und dass der Stellvertretung die [entsprechenden Berechtigungen für den Ordner" Posteingang "," Entwürfe "und" Gesendete Elemente "des Postfachbesitzers](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="31e61-145">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the [appropriate permissions for the mailbox owner's Inbox, Drafts, and Sent Items folder](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
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

## <a name="create-and-send-an-email-as-a-delegate-by-using-ews"></a><span data-ttu-id="31e61-146">Erstellen und Senden einer e-Mail als Stellvertretung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="31e61-146">Create and send an email as a delegate by using EWS</span></span>
<span data-ttu-id="31e61-147"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="31e61-147"><a name="bk_createews"> </a></span></span>

<span data-ttu-id="31e61-148">EWS ermöglicht die Verwendung des Dienstobjekts für den Stellvertreter Benutzer zum Erstellen und Senden von e-Mails im Auftrag des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="31e61-148">EWS enables you to use the service object for the delegate user to create and send email on behalf of the mailbox owner.</span></span> <span data-ttu-id="31e61-149">In diesem Beispiel wird gezeigt, wie Sie mithilfe des [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgangs eine e-Mail und den [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang erstellen, um die Uhrzeit zu senden und im Ordner "Gesendete Elemente" des Postfachbesitzers zu speichern.</span><span class="sxs-lookup"><span data-stu-id="31e61-149">This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create an email and the [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation to send the time and save it in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="31e61-150">Dies ist auch die erste XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die **Save** -Methode zum [Erstellen und Senden einer e-Mail](#bk_createewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="31e61-150">This is also the first XML request that the EWS Managed API sends when you use the **Save** method to [create and send an email](#bk_createewsma).</span></span>
  
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

<span data-ttu-id="31e61-151">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die e-Mail erstellt und erfolgreich gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="31e61-151">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the email was created and saved successfully.</span></span> <span data-ttu-id="31e61-152">Die Antwort enthält auch die Element-ID der neu erstellten e-Mail.</span><span class="sxs-lookup"><span data-stu-id="31e61-152">The response also contains the item ID of the newly created email.</span></span>
  
<span data-ttu-id="31e61-153">Der **ItemID** -Wert wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="31e61-153">The **ItemId** value has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="31e61-154">Verwenden Sie als nächstes den **SendItem** -Vorgang, um die Nachricht im Auftrag des Postfachbesitzers zu senden und im Ordner "Gesendete Elemente" des Postfachbesitzers zu speichern.</span><span class="sxs-lookup"><span data-stu-id="31e61-154">Next, use the **SendItem** operation to send the message on behalf of the mailbox owner and save it in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="31e61-155">Der **ItemID** -Wert wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="31e61-155">The **ItemId** value has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="31e61-156">Der Server antwortet auf die **SendItem** -Anforderung mit einer [SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die e-Mail erfolgreich an den Ordner "Gesendete Elemente" des Postfachbesitzers gesendet und gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="31e61-156">The server responds to the **SendItem** request with a [SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the email was sent and saved to the mailbox owner's Sent Items folder successfully.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </m:SendItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="search-for-an-email-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="31e61-157">Suchen nach einer e-Mail als Stellvertretung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="31e61-157">Search for an email as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="31e61-158"><a name="bk_searchewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="31e61-158"><a name="bk_searchewsma"> </a></span></span>

<span data-ttu-id="31e61-159">Um nach einer e-Mail zu suchen, müssen Sie eine der [Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methoden verwenden, die einen [foldercode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter enthält, sodass Sie den Posteingangsordner des Postfachbesitzers angeben können.</span><span class="sxs-lookup"><span data-stu-id="31e61-159">To search for an email, you must use one of the [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) methods that includes a [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Inbox folder.</span></span> 
  
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

<span data-ttu-id="31e61-160">Nachdem der **FindItems** -Aufruf eine Antwort mit einer ID zurückgibt, können Sie diese e-Mails abrufen, aktualisieren oder löschen, indem Sie die ID und den [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) verwenden – und Sie müssen die SMTP-Adresse des Postfachbesitzers nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="31e61-160">After the **FindItems** call returns a response with an ID, you can get, update or delete that email by using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) - and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="search-for-an-email-as-a-delegate-by-using-ews"></a><span data-ttu-id="31e61-161">Suchen nach einer e-Mail als Stellvertretung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="31e61-161">Search for an email as a delegate by using EWS</span></span>
<span data-ttu-id="31e61-162"><a name="bk_searchews"> </a></span><span class="sxs-lookup"><span data-stu-id="31e61-162"><a name="bk_searchews"> </a></span></span>

<span data-ttu-id="31e61-163">Mit EWS können Sie das Dienstobjekt für den Stellvertreter-Benutzer verwenden, um nach e-Mails zu suchen, die eine Reihe von Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="31e61-163">EWS enables you to use the service object for the delegate user to search for emails that meet a set of search criteria.</span></span> <span data-ttu-id="31e61-164">In diesem Beispiel wird gezeigt, wie Sie mithilfe des [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Vorgangs Nachrichten im Posteingangsordner des Besitzers suchen, die das Wort "Soccer" im Betreff enthalten.</span><span class="sxs-lookup"><span data-stu-id="31e61-164">This example shows how to use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find messages in the owner's Inbox folder that contain the word "soccer" in the subject.</span></span> 
  
<span data-ttu-id="31e61-165">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie [nach einer e-Mail suchen](#bk_searchewsma).</span><span class="sxs-lookup"><span data-stu-id="31e61-165">This is also the XML request that the EWS Managed API sends when you [search for an email](#bk_searchewsma).</span></span>
  
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

<span data-ttu-id="31e61-166">Der Server antwortet auf die **FindItem** -Anforderung mit einer [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die Suche erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="31e61-166">The server responds to the **FindItem** request with a [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the search completed successfully.</span></span> <span data-ttu-id="31e61-167">Die Antwort enthält ein [Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) -Element für alle e-Mails, die die Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="31e61-167">The response contains a [Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) element for any emails that met the search criteria.</span></span> <span data-ttu-id="31e61-168">In diesem Fall wird nur eine e-Mail gefunden.</span><span class="sxs-lookup"><span data-stu-id="31e61-168">In this case, only one email is found.</span></span> 
  
<span data-ttu-id="31e61-169">Der Wert des [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Elements wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="31e61-169">The value of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="31e61-170">Da Sie nun die **ItemID** für die e-Mail haben, die Ihre Kriterien erfüllt, können Sie diese e-Mails mithilfe des **ItemID** -und [impliziten Zugriffs](delegate-access-and-ews-in-exchange.md#bk_implicit) abrufen, aktualisieren oder löschen, und Sie müssen die SMTP-Adresse des Postfachbesitzers nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="31e61-170">Now that you have the **ItemId** for the email that meets your criteria, you can get, update, or delete that email by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) - and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="31e61-171">Abrufen, aktualisieren oder Löschen von e-Mail-Elementen als Stellvertretung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="31e61-171">Get, update, or delete email items as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="31e61-172"><a name="bk_geteswma"> </a></span><span class="sxs-lookup"><span data-stu-id="31e61-172"><a name="bk_geteswma"> </a></span></span>

<span data-ttu-id="31e61-173">Sie können die verwaltete EWS-API verwenden, um eine e-Mail auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie diese Aktionen ausgeführt werden, wenn Sie keinen Stellvertretungszugriff verwenden.</span><span class="sxs-lookup"><span data-stu-id="31e61-173">You can use the EWS Managed API to get, update, or delete an email in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="31e61-174">Der einzige Unterschied besteht darin, dass das **Datei "ExchangeService** -Objekt für den Stellvertreter-Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="31e61-174">The only difference is that the **ExchangeService** object is for the delegate user.</span></span> <span data-ttu-id="31e61-175">Die im **Bindungs** Methodenaufruf enthaltene Element-ID identifiziert das Element im Postfachspeicher im Posteingangsordner des Postfachbesitzers eindeutig.</span><span class="sxs-lookup"><span data-stu-id="31e61-175">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Inbox folder.</span></span> 
  
<span data-ttu-id="31e61-176">**Tabelle 2. Verwaltete EWS-API Methoden, die mit e-Mail als Stellvertretung arbeiten**</span><span class="sxs-lookup"><span data-stu-id="31e61-176">**Table 2. EWS Managed API methods working with email as a delegate**</span></span>

|<span data-ttu-id="31e61-177">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="31e61-177">**Task**</span></span>|<span data-ttu-id="31e61-178">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="31e61-178">**EWS Managed API method**</span></span>|<span data-ttu-id="31e61-179">**Codebeispiel**</span><span class="sxs-lookup"><span data-stu-id="31e61-179">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="31e61-180">Abrufen einer e-Mail</span><span class="sxs-lookup"><span data-stu-id="31e61-180">Get an email</span></span>  <br/> |[<span data-ttu-id="31e61-181">Bind</span><span class="sxs-lookup"><span data-stu-id="31e61-181">Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="31e61-182">Abrufen eines Elements mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="31e61-182">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="31e61-183">Aktualisieren einer e-Mail</span><span class="sxs-lookup"><span data-stu-id="31e61-183">Update an email</span></span>  <br/> |<span data-ttu-id="31e61-184">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31e61-184">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="31e61-185">Aktualisieren eines Elements mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="31e61-185">Update an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|<span data-ttu-id="31e61-186">Löschen einer e-Mail</span><span class="sxs-lookup"><span data-stu-id="31e61-186">Delete an email</span></span>  <br/> |<span data-ttu-id="31e61-187">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31e61-187">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="31e61-188">Löschen eines Elements mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="31e61-188">Delete an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |
   
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="31e61-189">Abrufen, aktualisieren oder Löschen von e-Mail-Elementen als Stellvertretung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="31e61-189">Get, update, or delete email items as a delegate by using EWS</span></span>
<span data-ttu-id="31e61-190"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="31e61-190"><a name="bk_getews"> </a></span></span>

<span data-ttu-id="31e61-191">Sie können die verwaltete EWS-API verwenden, um eine e-Mail auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie diese Aktionen ausgeführt werden, wenn Sie keinen Stellvertretungszugriff verwenden.</span><span class="sxs-lookup"><span data-stu-id="31e61-191">You can use the EWS Managed API to get, update, or delete an email in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="31e61-192">Der einzige Unterschied besteht darin, dass das Dienstobjekt für den Stellvertreter Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="31e61-192">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="31e61-193">Die in der **GetItem** -Anforderung enthaltene Element-ID identifiziert das Element im Postfachspeicher im Posteingangsordner des Postfachbesitzers eindeutig.</span><span class="sxs-lookup"><span data-stu-id="31e61-193">The item ID included in the **GetItem** request uniquely identifies the item in the mailbox store, in the mailbox owner's Inbox folder.</span></span> 
  
<span data-ttu-id="31e61-194">**Tabelle 3. EWS-Vorgänge für das Arbeiten mit e-Mail als Stellvertretung**</span><span class="sxs-lookup"><span data-stu-id="31e61-194">**Table 3. EWS operations for working with email as a delegate**</span></span>

|<span data-ttu-id="31e61-195">**Task**</span><span class="sxs-lookup"><span data-stu-id="31e61-195">**Task**</span></span>|<span data-ttu-id="31e61-196">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="31e61-196">**EWS operation**</span></span>|<span data-ttu-id="31e61-197">**Codebeispiel**</span><span class="sxs-lookup"><span data-stu-id="31e61-197">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="31e61-198">Abrufen einer e-Mail</span><span class="sxs-lookup"><span data-stu-id="31e61-198">Get an email</span></span>  <br/> |[<span data-ttu-id="31e61-199">GetItem</span><span class="sxs-lookup"><span data-stu-id="31e61-199">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="31e61-200">Abrufen eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="31e61-200">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="31e61-201">Aktualisieren einer e-Mail</span><span class="sxs-lookup"><span data-stu-id="31e61-201">Update an email</span></span>  <br/> |<span data-ttu-id="31e61-202">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31e61-202">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="31e61-203">Aktualisieren eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="31e61-203">Update an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|<span data-ttu-id="31e61-204">Löschen einer e-Mail</span><span class="sxs-lookup"><span data-stu-id="31e61-204">Delete an email</span></span>  <br/> |<span data-ttu-id="31e61-205">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="31e61-205">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |[<span data-ttu-id="31e61-206">Löschen eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="31e61-206">Delete an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31e61-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31e61-207">See also</span></span>

- [<span data-ttu-id="31e61-208">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="31e61-208">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)    
- [<span data-ttu-id="31e61-209">Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="31e61-209">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="31e61-210">Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="31e61-210">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="31e61-211">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="31e61-211">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    

