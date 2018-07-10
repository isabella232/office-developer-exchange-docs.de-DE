---
title: Access-Kontakte als Stellvertretung mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3cd34c14-18b0-4fe2-a4c2-d884318c88fc
description: Hier erfahren Sie, wie Sie Kontakte als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: a7f695dcbe0693809817de84284294dff872aa9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756855"
---
# <a name="access-contacts-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="203ef-103">Access-Kontakte als Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="203ef-103">Access contacts as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="203ef-104">Hier erfahren Sie, wie Sie Kontakte als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="203ef-104">Learn how to access contacts as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="203ef-105">Der EWS Managed API oder EWS können Sie um einem Benutzer den Zugriff auf eine Postfachbesitzer Kontakteordner zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="203ef-105">You can use the EWS Managed API or EWS to give a user access to a mailbox owner's Contacts folder.</span></span> <span data-ttu-id="203ef-106">Die Stellvertretung kann Klicken Sie dann Kontakte im Auftrag des Postfachbesitzers erstellen und abrufen, aktualisieren und Löschen von Kontakten aus dem Ordner Kontakte des Postfachbesitzers abhängig von ihren Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="203ef-106">The delegate can then create contacts on behalf of the mailbox owner, and retrieve, update, and delete contacts from the mailbox owner's Contacts folder, depending on their permissions.</span></span>
  
<span data-ttu-id="203ef-107">Als Stellvertretung verwenden Sie die gleichen Methoden und Vorgänge auf des Postfachbesitzers Kontakteordner zugreifen, mit denen Sie Ihre eigenen Ordner Kontakte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="203ef-107">As a delegate, you use the same methods and operations to access a mailbox owner's Contacts folder that you use to access your own Contacts folder.</span></span> <span data-ttu-id="203ef-108">Der Hauptunterschied ist, dass Sie mithilfe von [expliziten Access](delegate-access-and-ews-in-exchange.md#bk_explicit) suchen oder erstellen ein Kontaktelement, und klicken Sie dann, nachdem Sie die Element-ID identifiziert haben, können [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) erhalten möchten, aktualisieren und Löschen des Elements.</span><span class="sxs-lookup"><span data-stu-id="203ef-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a contact item, and then after you identify the item ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="203ef-109">**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für den Zugriff auf einen Kontakt als Stellvertreter**</span><span class="sxs-lookup"><span data-stu-id="203ef-109">**Table 1. EWS Managed API methods and EWS operations for accessing a contact as a delegate**</span></span>

|<span data-ttu-id="203ef-110">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="203ef-110">**If you want to…**</span></span>|<span data-ttu-id="203ef-111">**Verwenden Sie diese Methode EWS Managed API...**</span><span class="sxs-lookup"><span data-stu-id="203ef-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="203ef-112">**Verwenden Sie diese Operation EWS...**</span><span class="sxs-lookup"><span data-stu-id="203ef-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="203ef-113">Erstellen Sie einen Kontakt als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="203ef-113">Create a contact as a delegate</span></span>  <br/> |<span data-ttu-id="203ef-114">[Item.Save](http://msdn.microsoft.com/de-de/library/dd635209%28v=exchg.80%29.aspx) , in dem der Parameter [FolderId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kontakteordner bietet</span><span class="sxs-lookup"><span data-stu-id="203ef-114">[Item.Save](http://msdn.microsoft.com/de-de/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="203ef-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers</span><span class="sxs-lookup"><span data-stu-id="203ef-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="203ef-116">Erstellen Sie mehrere Kontakte als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="203ef-116">Create multiple contacts as a delegate</span></span>  <br/> |<span data-ttu-id="203ef-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kontakteordner bietet</span><span class="sxs-lookup"><span data-stu-id="203ef-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="203ef-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers</span><span class="sxs-lookup"><span data-stu-id="203ef-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="203ef-119">Beheben Sie einen Kontakt als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="203ef-119">Resolve a contact as a delegate</span></span>  <br/> |<span data-ttu-id="203ef-120">[ExchangeService.ResolveName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) , in dem der Parameter [FolderId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kontakteordner bietet</span><span class="sxs-lookup"><span data-stu-id="203ef-120">[ExchangeService.ResolveName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="203ef-121">[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers</span><span class="sxs-lookup"><span data-stu-id="203ef-121">[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="203ef-122">Suchen Sie nach oder Suchen nach einem Kontakt als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="203ef-122">Search for or find a contact as a delegate</span></span>  <br/> |<span data-ttu-id="203ef-123">[ExchangeService.FindItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kontakteordner bietet</span><span class="sxs-lookup"><span data-stu-id="203ef-123">[ExchangeService.FindItems](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="203ef-124">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers</span><span class="sxs-lookup"><span data-stu-id="203ef-124">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="203ef-125">Abrufen eines Kontakts als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="203ef-125">Get a contact as a delegate</span></span>  <br/> |[<span data-ttu-id="203ef-126">Contact.Bind</span><span class="sxs-lookup"><span data-stu-id="203ef-126">Contact.Bind</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="203ef-127">GetItem</span><span class="sxs-lookup"><span data-stu-id="203ef-127">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="203ef-128">Aktualisieren eines Kontakts als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="203ef-128">Update a contact as a delegate</span></span>  <br/> |<span data-ttu-id="203ef-129">[Contact.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) gefolgt von [Contact.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="203ef-129">[Contact.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="203ef-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="203ef-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="203ef-131">Löschen eines Kontakts als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="203ef-131">Delete a contact as a delegate</span></span>  <br/> |<span data-ttu-id="203ef-132">[Contact.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) gefolgt von [Contact.Delete](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="203ef-132">[Contact.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Delete](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="203ef-133">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="203ef-133">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="203ef-134">In den Codebeispielen in diesem Artikel ist primary@contoso.com der Postfachbesitzer.</span><span class="sxs-lookup"><span data-stu-id="203ef-134">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 

<span data-ttu-id="203ef-135"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="203ef-135"></span></span>

## <a name="prerequisite-tasks"></a><span data-ttu-id="203ef-136">Erforderliche Aufgaben</span><span class="sxs-lookup"><span data-stu-id="203ef-136">Prerequisite tasks</span></span>

<span data-ttu-id="203ef-137">Bevor ein Benutzer des Postfachbesitzers Kontakteordner als Stellvertreter zugreifen kann, muss der Benutzer des Postfachbesitzers Kontakteordner [als Stellvertreter mit Berechtigungen hinzugefügt](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) .</span><span class="sxs-lookup"><span data-stu-id="203ef-137">Before a user can access the mailbox owner's Contacts folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Contacts folder.</span></span> 

<span data-ttu-id="203ef-138"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="203ef-138"></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="203ef-139">Erstellen eines Kontakts eine Stellvertretung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="203ef-139">Create a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="203ef-140">Die EWS Managed API können Sie das Objekt für den Benutzer Delegaten verwenden, um Kontakte für den Besitzer des Postfachs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="203ef-140">The EWS Managed API enables you to use the service object for the delegate user to create contacts for the mailbox owner.</span></span> <span data-ttu-id="203ef-141">In diesem Beispiel wird veranschaulicht, wie mit der [Save](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode erstellen Sie eine Besprechung und Besprechungsanfragen an die Teilnehmer senden.</span><span class="sxs-lookup"><span data-stu-id="203ef-141">This example shows how to use the [Save](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="203ef-142">In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Delegaten und, die der Stellvertreter die entsprechenden Berechtigungen für den Postfachbesitzer Kontakteordner gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="203ef-142">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Contacts folder.</span></span> 
  
```cs
 public static void DelegateAccessCreateContact(ExchangeService service)
{
    // Create the contact.
    Contact contact = new Contact(service);
    // Specify the name and how the contact should be filed.
    contact.GivenName = "Brian";
    contact.MiddleName = "David";
    contact.Surname = "Johnson";
    contact.FileAsMapping = FileAsMapping.SurnameCommaGivenName;
    // Specify the company name.
    contact.CompanyName = "Contoso";
    // Specify the business, home, and car phone numbers.
    contact.PhoneNumbers[PhoneNumberKey.BusinessPhone] = "425-555-0110";
    contact.PhoneNumbers[PhoneNumberKey.HomePhone] = "425-555-0120";
    contact.PhoneNumbers[PhoneNumberKey.CarPhone] = "425-555-0130";
    // Specify two email addresses.
    contact.EmailAddresses[EmailAddressKey.EmailAddress1] = 
        new EmailAddress("brian_1@contoso.com");
    contact.EmailAddresses[EmailAddressKey.EmailAddress2] = 
        new EmailAddress("brian_2@contoso.com");
    // Save the contact in the mailbox owner's Contacts folder.
    // This method call results in a CreateItem call to EWS. 
    // The contact identifier contains the context for the mailbox owner's 
    // Contact folder. Any additional actions take on this contact will 
    // be performed in the mailbox owner's mailbox. 
    contact.Save(new FolderId(WellKnownFolderName.Contacts, 
        "primary@contoso.com"));
    // Verify that the contact was created.
    // This method call results in a GetItem call to EWS
    // to load the display name property on the contact. 
    contact.Load(new PropertySet (ContactSchema.DisplayName));
    Console.WriteLine("\nContact created: " + contact.DisplayName + "\n");
}
```

<span data-ttu-id="203ef-143">Beachten Sie, dass beim Speichern des Elements Methodenaufruf [Speichern](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) des Postfachbesitzers Kontakteordner bestimmen muss.</span><span class="sxs-lookup"><span data-stu-id="203ef-143">Note that when you save the item, the [Save](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="203ef-144">Wenn der Postfachbesitzer Kontakteordner nicht angegeben ist, ruft die Besprechungsanfrage Kontakteordner der Stellvertretung und nicht des Postfachbesitzers Kontakteordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="203ef-144">If the mailbox owner's Contacts folder is not specified, the meeting request gets saved to the delegate's Contacts folder and not the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="203ef-145">Sie können den Postfachbesitzer Kontaktordners im Methodenaufruf **Speichern** in zwei-Wege-einschließen.</span><span class="sxs-lookup"><span data-stu-id="203ef-145">You can include the mailbox owner's Contacts folder in the **Save** method call in two way.</span></span> <span data-ttu-id="203ef-146">Es wird empfohlen, dass Sie eine neue Instanz des Objekts [FolderId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) instanziieren, mithilfe der [WellKnownFolderName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) und die SMTP-Adresse des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="203ef-146">We recommend that you instantiate a new instance of the [FolderId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
contact.Save(new FolderId(WellKnownFolderName.Contacts, "primary@contoso.com"));
```

<span data-ttu-id="203ef-147">Sie können jedoch auch [gebunden werden](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) in den Ordner Kontakte zuerst, und verwenden Sie die ID des Ordners in den Methodenaufruf **zu speichern** .</span><span class="sxs-lookup"><span data-stu-id="203ef-147">However, you can also [Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Contacts folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="203ef-148">Beachten Sie jedoch, dass dieser einen zusätzlichen EWS-Aufruf erstellt.</span><span class="sxs-lookup"><span data-stu-id="203ef-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
```cs
    // Identify the mailbox owner's SMTP address 
    // and bind to their Contacts folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryContacts = Folder.Bind(service, new FolderId(WellKnownFolderName.Contacts, primary)); 
…
    // Save the contact to the mailbox owner's Contacts folder.
    meeting.Save(primaryContacts.Id);
```

<span data-ttu-id="203ef-149"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="203ef-149"></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="203ef-150">Erstellen eines Kontakts eine Stellvertretung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="203ef-150">Create a contact as a delegate by using EWS</span></span>

<span data-ttu-id="203ef-151">Exchange-Webdienste können Sie das Objekt für den Benutzer Delegaten verwenden Sie zum Erstellen von Kontaktelementen (engl.) für den Besitzer des Postfachs.</span><span class="sxs-lookup"><span data-stu-id="203ef-151">EWS enables you to use the service object for the delegate user to create contact items for the mailbox owner.</span></span> <span data-ttu-id="203ef-152">Dieses Beispiel zeigt, wie Sie den [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgang verwenden, um einen Kontakt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="203ef-152">This example shows how to use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a contact.</span></span> 
  
<span data-ttu-id="203ef-153">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Speichern** -Methode erstellen Sie [einen Kontakt](#bk_createewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="203ef-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a contact](#bk_createewsma).</span></span>
  
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
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="contacts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:Contact>
          <t:FileAsMapping>LastCommaFirst</t:FileAsMapping>
          <t:GivenName>Brian</t:GivenName>
          <t:MiddleName>David</t:MiddleName>
          <t:CompanyName>Contoso</t:CompanyName>
          <t:EmailAddresses>
            <t:Entry Key="EmailAddress1">brian_1@contoso.com</t:Entry>
            <t:Entry Key="EmailAddress2">brian_2@contoso.com</t:Entry>
          </t:EmailAddresses>
          <t:PhoneNumbers>
            <t:Entry Key="BusinessPhone">425-555-0110</t:Entry>
            <t:Entry Key="HomePhone">425-555-0120</t:Entry>
            <t:Entry Key="CarPhone">425-555-0130</t:Entry>
          </t:PhoneNumbers>
          <t:Surname>Johnson</t:Surname>
        </t:Contact>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="203ef-154">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Kontakt erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="203ef-154">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the contact was created successfully.</span></span> <span data-ttu-id="203ef-155">Die Antwort enthält auch die Element-ID des neu erstellten Kontakts.</span><span class="sxs-lookup"><span data-stu-id="203ef-155">The response also contains the item ID of the newly created contact.</span></span>

<span data-ttu-id="203ef-156"><a name="bk_resolveewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="203ef-156"></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="203ef-157">Beheben Sie einen Kontakt als Stellvertretung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="203ef-157">Resolve a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="203ef-158">Um einen Kontakt basierend auf möglicherweise mehrdeutige Namen oder einen Ausdruck ermittelt wird, müssen Sie eine der Methoden [ExchangeService.ResolveName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) , die einen [FolderId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter verwenden, damit Sie den Postfachbesitzer Kontakteordner angeben können.</span><span class="sxs-lookup"><span data-stu-id="203ef-158">To find a contact based on a possibly ambiguous name or term, you must use one of the [ExchangeService.ResolveName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) methods that includes a [FolderId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Contacts folder.</span></span> 
  
```cs
private static void DelegateAccessResolveContacts(ExchangeService service)
{
    // Create a list to store folders to search.
    List<FolderId> folders = new List<FolderId>();
   
    // Add the mailbox owner's folder to the list.
    folders.Add(new FolderId(WellKnownFolderName.Contacts, 
        "primary@contoso.com"));
    
    // Resolve the ambiguous name "Johnson".
    // This method call results in a ResolveNames call to EWS.
    NameResolutionCollection resolvedNames = service.ResolveName(
        "johnson", folders, ResolveNameSearchLocation.ContactsOnly, true);
    // Output the list of candidate email addresses and contact names.
    foreach (NameResolution nameRes in resolvedNames)
    {
        Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
        Console.WriteLine("Contact ID: " + nameRes.Mailbox.Id);
    }
}
```

<span data-ttu-id="203ef-159">Nachdem eine Antwort mit einer ID **ResolveNames** Methodenaufruf zurückgegeben wird, können Sie [abrufen, aktualisieren oder löschen Sie den Kontakt](#bk_getewsma) mit der ID und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;und müssen nicht die SMTP-Adresse des Postfachbesitzers angeben.</span><span class="sxs-lookup"><span data-stu-id="203ef-159">After the **ResolveNames** method call returns a response with an ID, you can [get, update or delete the contact](#bk_getewsma) using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="203ef-160"><a name="bk_resolveews"> </a></span><span class="sxs-lookup"><span data-stu-id="203ef-160"></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="203ef-161">Beheben Sie einen Kontakt als Stellvertreter mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="203ef-161">Resolve a contact as a delegate by using EWS</span></span>

<span data-ttu-id="203ef-162">EWS können Sie das Objekt für den Benutzer Delegaten verwenden, um im Ordner "Kontakte" des Postfachbesitzers partiellen Namen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="203ef-162">EWS enables you to use the service object for the delegate user to resolve partial names in the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="203ef-163">In diesem Beispiel wird veranschaulicht, wie mit den Vorgang [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) finden Besprechungen in der Postfachbesitzer Kontakteordner, die das Wort "Johnson" enthalten.</span><span class="sxs-lookup"><span data-stu-id="203ef-163">This example shows how to use the [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Contacts folder that contain the word "johnson".</span></span> 
  
<span data-ttu-id="203ef-164">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **ResolveName** -Methode zum [Auflösen eines Kontakts](#bk_resolveewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="203ef-164">This is also the XML request that the EWS Managed API sends when you use the **ResolveName** method to [resolve a contact](#bk_resolveewsma).</span></span>
  
```xml
 <?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ResolveNames ReturnFullContactData="true"
                    SearchScope="Contacts">
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="contacts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
      <m:UnresolvedEntry>johnson</m:UnresolvedEntry>
    </m:ResolveNames>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="203ef-165">Der Server antwortet auf die Anforderung **ResolveNames** mit einer [ResolveNamesResponse](http://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) Element **noError zurück**, das anzeigt, dass den Vorgang erfolgreich abgeschlossen wurde und nur eine gefunden Ergebnis oder **ErrorNameResolutionMultipleResults** mehrere Ergebnisse gefunden – das ist, was im dritten Codebeispiel wird basierend auf den Kontakt, [Erstellen Sie einen Kontakt als Stellvertretung mithilfe der EWS Managed API](#bk_createewsma)angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="203ef-165">The server responds to the **ResolveNames** request with a [ResolveNamesResponse](http://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the operation completed successfully and found only one result, or **ErrorNameResolutionMultipleResults** if multiple results were found - which is what's shown in third code example based on the contact [Create a contact as a delegate by using the EWS Managed API](#bk_createewsma).</span></span> <span data-ttu-id="203ef-166">Die Antwort enthält auch die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) jedes Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="203ef-166">The response also contains the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of each result.</span></span> 
  
<span data-ttu-id="203ef-167">Der Wert des Elements **ItemId** wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="203ef-167">The value of the **ItemId** element has been shortened for readability.</span></span> 
  
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
    <m:ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Warning">
          <m:MessageText>Multiple results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionMultipleResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:ResolutionSet TotalItemsInView="2"
                           IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>brian_1@contoso.com</t:Name>
                <t:EmailAddress>brian_1@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Contact</t:MailboxType>
                <t:ItemId Id="iMihAAA="
                          ChangeKey="EQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiPQo" />
              </t:Mailbox>
            </t:Resolution>
            <t:Resolution>
              <t:Mailbox>
                <t:Name>brian_2@contoso.com</t:Name>
                <t:EmailAddress>brian_2@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Contact</t:MailboxType>
                <t:ItemId Id="iMihAAA="
                          ChangeKey="EQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiPQo" />
              </t:Mailbox>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </m:ResolveNamesResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="203ef-168">Nun, da Sie die **ItemId** für die Kontakte verfügen, mehrdeutigen Name entsprechen, können Sie [abrufen, aktualisieren oder Löschen von Kontaktelementen als Stellvertretung mithilfe der Exchange-Webdienste](#bk_getews) mithilfe der **ItemId** und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;und müssen nicht angeben SMTP-Adresse des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="203ef-168">Now that you have the **ItemId** for the contacts that match the ambiguous name, you can [Get, update, or delete contact items as a delegate by using EWS](#bk_getews) by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="203ef-169"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="203ef-169"></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="203ef-170">Abrufen, aktualisieren oder Löschen von Kontaktelementen als Stellvertretung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="203ef-170">Get, update, or delete contact items as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="203ef-171">Die EWS Managed API können Sie abrufen, aktualisieren oder Löschen eines Kontakts auf die gleiche Weise, die Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="203ef-171">You can use the EWS Managed API to get, update, or delete a contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="203ef-172">Der einzige Unterschied ist, dass das Objekt für den Benutzer Delegat ist.</span><span class="sxs-lookup"><span data-stu-id="203ef-172">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="203ef-173">Die Element-ID im Methodenaufruf **binden** enthalten sind, eindeutig identifiziert das Element im Postfachspeicher im Ordner "Kontakte" des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="203ef-173">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="203ef-174">**In Tabelle 2. Arbeiten mit einem Kontakt eine Stellvertretung EWS Managed API-Methoden**</span><span class="sxs-lookup"><span data-stu-id="203ef-174">**Table 2. EWS Managed API methods working with a contact as a delegate**</span></span>

|<span data-ttu-id="203ef-175">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="203ef-175">**Task**</span></span>|<span data-ttu-id="203ef-176">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="203ef-176">**EWS Managed API method**</span></span>|<span data-ttu-id="203ef-177">**Codebeispiel**</span><span class="sxs-lookup"><span data-stu-id="203ef-177">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="203ef-178">Abrufen eines Kontakts</span><span class="sxs-lookup"><span data-stu-id="203ef-178">Get a contact</span></span>  <br/> |[<span data-ttu-id="203ef-179">Bind</span><span class="sxs-lookup"><span data-stu-id="203ef-179">Bind</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="203ef-180">Abrufen eines Elements mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="203ef-180">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="203ef-181">Aktualisieren eines Kontakts</span><span class="sxs-lookup"><span data-stu-id="203ef-181">Update a contact</span></span>  <br/> |<span data-ttu-id="203ef-182">[Binden von](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="203ef-182">[Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="203ef-183">Aktualisieren eines Elements mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="203ef-183">Update an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|<span data-ttu-id="203ef-184">Löschen eines Kontakts</span><span class="sxs-lookup"><span data-stu-id="203ef-184">Delete a contact</span></span>  <br/> |<span data-ttu-id="203ef-185">[Binden von](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Löschen](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="203ef-185">[Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="203ef-186">Löschen eines Elements mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="203ef-186">Delete an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |

<span data-ttu-id="203ef-187"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="203ef-187"></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="203ef-188">Erhalten möchten, aktualisieren oder Löschen von Kontaktelementen als Stellvertreter mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="203ef-188">Get, update, or delete contact items as a delegate by using EWS</span></span>

<span data-ttu-id="203ef-189">Exchange-Webdienste können Sie abrufen, aktualisieren oder Löschen eines Besprechung oder eines Termins Kontakts auf die gleiche Weise, dass Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="203ef-189">You can use EWS to get, update, or delete a meeting or appointment contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="203ef-190">Der einzige Unterschied ist, dass das Objekt für den Benutzer Delegat ist.</span><span class="sxs-lookup"><span data-stu-id="203ef-190">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="203ef-191">Die Element-ID, enthalten in der [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) -Anforderung eindeutig identifiziert das Element im Postfachspeicher im Ordner "Kontakte" des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="203ef-191">The item ID included in the [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) request uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="203ef-192">**Tabelle 3. EWS-Vorgänge für die Arbeit mit einem Kontakt als Stellvertreter**</span><span class="sxs-lookup"><span data-stu-id="203ef-192">**Table 3. EWS operations for working with a contact as a delegate**</span></span>

|<span data-ttu-id="203ef-193">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="203ef-193">**Task**</span></span>|<span data-ttu-id="203ef-194">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="203ef-194">**EWS operation**</span></span>|<span data-ttu-id="203ef-195">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="203ef-195">**Sample**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="203ef-196">Abrufen eines Kontakts</span><span class="sxs-lookup"><span data-stu-id="203ef-196">Get a contact</span></span>  <br/> |[<span data-ttu-id="203ef-197">GetItem</span><span class="sxs-lookup"><span data-stu-id="203ef-197">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="203ef-198">Abrufen eines Elements mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="203ef-198">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="203ef-199">Aktualisieren eines Kontakts</span><span class="sxs-lookup"><span data-stu-id="203ef-199">Update a contact</span></span>  <br/> |<span data-ttu-id="203ef-200">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="203ef-200">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="203ef-201">Aktualisieren eines Elements mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="203ef-201">Update an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|<span data-ttu-id="203ef-202">Löschen eines Kontakts</span><span class="sxs-lookup"><span data-stu-id="203ef-202">Delete a contact</span></span>  <br/> |<span data-ttu-id="203ef-203">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="203ef-203">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="203ef-204">Löschen eines Elements mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="203ef-204">Delete an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="203ef-205">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="203ef-205">See also</span></span>

- [<span data-ttu-id="203ef-206">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="203ef-206">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
- [<span data-ttu-id="203ef-207">Hinzufügen und Entfernen von Stellvertretungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="203ef-207">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="203ef-208">Legen Sie Berechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="203ef-208">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
- [<span data-ttu-id="203ef-209">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="203ef-209">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
- [<span data-ttu-id="203ef-210">Lösen Sie mehrdeutige Namen auf, mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="203ef-210">Resolve ambiguous names by using EWS in Exchange 2013</span></span>](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)
    

