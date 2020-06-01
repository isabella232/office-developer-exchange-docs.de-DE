---
title: Zugriff auf Kontakte als Delegat mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3cd34c14-18b0-4fe2-a4c2-d884318c88fc
description: Informationen zum Zugreifen auf Kontakte als Stellvertretung mithilfe der verwaltete EWS-API oder EWS in Exchange.
ms.openlocfilehash: 06faf7dd7459b14792abbea21761e909c8eb9fb6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455345"
---
# <a name="access-contacts-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="ec3c9-103">Zugriff auf Kontakte als Delegat mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec3c9-103">Access contacts as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="ec3c9-104">Informationen zum Zugreifen auf Kontakte als Stellvertretung mithilfe der verwaltete EWS-API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-104">Learn how to access contacts as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="ec3c9-105">Sie können die verwaltete EWS-API oder EWS verwenden, um einem Benutzer Zugriff auf den Ordner Kontakte eines Postfachbesitzers zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-105">You can use the EWS Managed API or EWS to give a user access to a mailbox owner's Contacts folder.</span></span> <span data-ttu-id="ec3c9-106">Der Stellvertreter kann dann Kontakte im Namen des Postfachbesitzers erstellen und Kontakte aus dem Kontaktordner des Postfachbesitzers abrufen, aktualisieren und löschen, je nachdem, welche Berechtigungen Sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-106">The delegate can then create contacts on behalf of the mailbox owner, and retrieve, update, and delete contacts from the mailbox owner's Contacts folder, depending on their permissions.</span></span>
  
<span data-ttu-id="ec3c9-107">Als Stellvertretung verwenden Sie dieselben Methoden und Vorgänge für den Zugriff auf den Ordner Kontakte eines Postfachbesitzers, den Sie für den Zugriff auf Ihren eigenen Kontaktordner verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-107">As a delegate, you use the same methods and operations to access a mailbox owner's Contacts folder that you use to access your own Contacts folder.</span></span> <span data-ttu-id="ec3c9-108">Der Hauptunterschied besteht darin, dass Sie [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicit) zum Suchen oder Erstellen eines Kontaktelements verwenden müssen, und nachdem Sie die Element-ID identifiziert haben, können Sie [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) zum Abrufen, aktualisieren oder Löschen des Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a contact item, and then after you identify the item ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="ec3c9-109">**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge für den Zugriff auf einen Kontakt als Stellvertretung**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-109">**Table 1. EWS Managed API methods and EWS operations for accessing a contact as a delegate**</span></span>

|<span data-ttu-id="ec3c9-110">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-110">**If you want to…**</span></span>|<span data-ttu-id="ec3c9-111">**Verwenden Sie diese verwaltete EWS-API-Methode...**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="ec3c9-112">**Verwenden Sie diesen EWS-Vorgang...**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec3c9-113">Erstellen eines Kontakts als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ec3c9-113">Create a contact as a delegate</span></span>  <br/> |<span data-ttu-id="ec3c9-114">[Item. Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) , wobei der [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Ordner "Kontakte" des Postfachbesitzers ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-114">[Item.Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="ec3c9-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt</span><span class="sxs-lookup"><span data-stu-id="ec3c9-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="ec3c9-116">Erstellen mehrerer Kontakte als Stellvertretung</span><span class="sxs-lookup"><span data-stu-id="ec3c9-116">Create multiple contacts as a delegate</span></span>  <br/> |<span data-ttu-id="ec3c9-117">[Datei "ExchangeService. CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , wobei der **Folder** -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Ordner" Kontakte "des Postfachbesitzers ermöglicht</span><span class="sxs-lookup"><span data-stu-id="ec3c9-117">[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="ec3c9-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt</span><span class="sxs-lookup"><span data-stu-id="ec3c9-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="ec3c9-119">Auflösen eines Kontakts als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ec3c9-119">Resolve a contact as a delegate</span></span>  <br/> |<span data-ttu-id="ec3c9-120">[Datei "ExchangeService. ResolveName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) , wobei der [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Ordner" Kontakte "des Postfachbesitzers ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-120">[ExchangeService.ResolveName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="ec3c9-121">[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt</span><span class="sxs-lookup"><span data-stu-id="ec3c9-121">[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="ec3c9-122">Suchen nach oder Suchen eines Kontakts als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ec3c9-122">Search for or find a contact as a delegate</span></span>  <br/> |<span data-ttu-id="ec3c9-123">[Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , wobei der **Folder** -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Ordner" Kontakte "des Postfachbesitzers ermöglicht</span><span class="sxs-lookup"><span data-stu-id="ec3c9-123">[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="ec3c9-124">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt</span><span class="sxs-lookup"><span data-stu-id="ec3c9-124">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="ec3c9-125">Abrufen eines Kontakts als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ec3c9-125">Get a contact as a delegate</span></span>  <br/> |[<span data-ttu-id="ec3c9-126">Contact.Bind</span><span class="sxs-lookup"><span data-stu-id="ec3c9-126">Contact.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ec3c9-127">GetItem</span><span class="sxs-lookup"><span data-stu-id="ec3c9-127">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ec3c9-128">Aktualisieren eines Kontakts als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ec3c9-128">Update a contact as a delegate</span></span>  <br/> |<span data-ttu-id="ec3c9-129">[Contact. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) gefolgt von [Contact. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec3c9-129">[Contact.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="ec3c9-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec3c9-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="ec3c9-131">Löschen eines Kontakts als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ec3c9-131">Delete a contact as a delegate</span></span>  <br/> |<span data-ttu-id="ec3c9-132">[Contact. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) gefolgt von [Contact. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec3c9-132">[Contact.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="ec3c9-133">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="ec3c9-133">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="ec3c9-134">In den Codebeispielen in diesem Artikel ist Primary@contoso.com der Postfachbesitzer.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-134">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 

<span data-ttu-id="ec3c9-135"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="ec3c9-135"><a name="bk_prereq"> </a></span></span>

## <a name="prerequisite-tasks"></a><span data-ttu-id="ec3c9-136">Erforderliche Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ec3c9-136">Prerequisite tasks</span></span>

<span data-ttu-id="ec3c9-137">Damit ein Benutzer als Stellvertreter auf den Ordner "Kontakte" des Postfachbesitzers zugreifen kann, muss er [als Stellvertreter mit Berechtigungen](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) für den Ordner "Kontakte" des Postfachbesitzers hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-137">Before a user can access the mailbox owner's Contacts folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Contacts folder.</span></span> 

<span data-ttu-id="ec3c9-138"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ec3c9-138"><a name="bk_createewsma"> </a></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="ec3c9-139">Erstellen eines Kontakts als Stellvertretung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ec3c9-139">Create a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="ec3c9-140">Mit dem verwaltete EWS-API können Sie das Dienstobjekt für den Stellvertreter Benutzer verwenden, um Kontakte für den Postfachbesitzer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-140">The EWS Managed API enables you to use the service object for the delegate user to create contacts for the mailbox owner.</span></span> <span data-ttu-id="ec3c9-141">In diesem Beispiel wird gezeigt, wie Sie mit der [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode eine Besprechung erstellen und Besprechungsanfragen an die Teilnehmer senden.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-141">This example shows how to use the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="ec3c9-142">In diesem Beispiel wird davon ausgegangen, dass **Service** ein gültiges [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für die Stellvertretung ist und dass der Stellvertretung die entsprechenden Berechtigungen für den Kontaktordner des Postfachbesitzers erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-142">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Contacts folder.</span></span> 
  
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

<span data-ttu-id="ec3c9-143">Beachten Sie, dass beim Speichern des Elements der Aufruf der [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode den Kontaktordner des Postfachbesitzers identifizieren muss.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-143">Note that when you save the item, the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="ec3c9-144">Wenn der Kontaktordner des Postfachbesitzers nicht angegeben ist, wird die Besprechungsanfrage im Kontakteordner des Stellvertreters und nicht im Ordner Kontakte des Postfachbesitzers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-144">If the mailbox owner's Contacts folder is not specified, the meeting request gets saved to the delegate's Contacts folder and not the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="ec3c9-145">Sie können den Kontaktordner des Postfachbesitzers in den **Save** -Methodenaufruf auf zweierlei Weise einschließen.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-145">You can include the mailbox owner's Contacts folder in the **Save** method call in two way.</span></span> <span data-ttu-id="ec3c9-146">Es wird empfohlen, dass Sie eine neue Instanz des [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Objekts mit dem [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) und der SMTP-Adresse des Postfachbesitzers instanziieren.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-146">We recommend that you instantiate a new instance of the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
contact.Save(new FolderId(WellKnownFolderName.Contacts, "primary@contoso.com"));
```

<span data-ttu-id="ec3c9-147">Sie können jedoch auch zuerst eine [Bindung](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) an den Ordner Kontakte herstellen und dann die ID des Ordners im Aufruf der **Save** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-147">However, you can also [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Contacts folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="ec3c9-148">Beachten Sie jedoch, dass dadurch ein zusätzlicher EWS-Aufruf erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
```cs
    // Identify the mailbox owner's SMTP address 
    // and bind to their Contacts folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryContacts = Folder.Bind(service, new FolderId(WellKnownFolderName.Contacts, primary)); 
…
    // Save the contact to the mailbox owner's Contacts folder.
    meeting.Save(primaryContacts.Id);
```

<span data-ttu-id="ec3c9-149"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="ec3c9-149"><a name="bk_createews"> </a></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="ec3c9-150">Erstellen eines Kontakts als Stellvertretung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="ec3c9-150">Create a contact as a delegate by using EWS</span></span>

<span data-ttu-id="ec3c9-151">Mit EWS können Sie das Dienstobjekt für den Stellvertreter-Benutzer verwenden, um Kontaktelemente für den Postfachbesitzer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-151">EWS enables you to use the service object for the delegate user to create contact items for the mailbox owner.</span></span> <span data-ttu-id="ec3c9-152">In diesem Beispiel wird gezeigt, wie Sie mithilfe des [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgangs einen Kontakt erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-152">This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a contact.</span></span> 
  
<span data-ttu-id="ec3c9-153">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die **Save** -Methode zum [Erstellen eines Kontakts](#bk_createewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a contact](#bk_createewsma).</span></span>
  
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

<span data-ttu-id="ec3c9-154">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass der Kontakt erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-154">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the contact was created successfully.</span></span> <span data-ttu-id="ec3c9-155">Die Antwort enthält auch die Element-ID des neu erstellten Kontakts.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-155">The response also contains the item ID of the newly created contact.</span></span>

<span data-ttu-id="ec3c9-156"><a name="bk_resolveewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ec3c9-156"><a name="bk_resolveewsma"> </a></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="ec3c9-157">Auflösen eines Kontakts als Stellvertretung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ec3c9-157">Resolve a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="ec3c9-158">Wenn Sie einen Kontakt basierend auf einem möglicherweise nicht eindeutigen Namen oder Ausdruck suchen möchten, müssen Sie eine der [Datei "ExchangeService. ResolveName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) -Methoden verwenden, die einen [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter enthält, sodass Sie den Kontaktordner des Postfachbesitzers angeben können.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-158">To find a contact based on a possibly ambiguous name or term, you must use one of the [ExchangeService.ResolveName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) methods that includes a [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Contacts folder.</span></span> 
  
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

<span data-ttu-id="ec3c9-159">Nachdem der **ResolveNames** -Methodenaufruf eine Antwort mit einer ID zurückgibt, können Sie den Kontakt mit der ID und dem [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) [abrufen, aktualisieren oder löschen](#bk_getewsma) , &mdash; und Sie müssen die SMTP-Adresse des Postfachbesitzers nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-159">After the **ResolveNames** method call returns a response with an ID, you can [get, update or delete the contact](#bk_getewsma) using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="ec3c9-160"><a name="bk_resolveews"> </a></span><span class="sxs-lookup"><span data-stu-id="ec3c9-160"><a name="bk_resolveews"> </a></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="ec3c9-161">Auflösen eines Kontakts als Stellvertretung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="ec3c9-161">Resolve a contact as a delegate by using EWS</span></span>

<span data-ttu-id="ec3c9-162">Mit EWS können Sie das Dienstobjekt für den Stellvertreter verwenden, um partielle Namen im Kontakteordner des Postfachbesitzers aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-162">EWS enables you to use the service object for the delegate user to resolve partial names in the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="ec3c9-163">In diesem Beispiel wird gezeigt, wie Sie mithilfe des [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) -Vorgangs Besprechungen im Kontakteordner des Postfachbesitzers finden, die das Wort "Johnson" enthalten.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-163">This example shows how to use the [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Contacts folder that contain the word "johnson".</span></span> 
  
<span data-ttu-id="ec3c9-164">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die **ResolveName** -Methode zum [Auflösen eines Kontakts](#bk_resolveewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-164">This is also the XML request that the EWS Managed API sends when you use the **ResolveName** method to [resolve a contact](#bk_resolveewsma).</span></span>
  
```xml
 <?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ec3c9-165">Der Server antwortet auf die **ResolveNames** -Anforderung mit einer [ResolveNamesResponse](https://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass der Vorgang erfolgreich abgeschlossen wurde und nur ein Ergebnis gefunden hat, oder **ErrorNameResolutionMultipleResults** , wenn mehrere Ergebnisse gefunden wurden-was im dritten Codebeispiel basierend auf dem Kontakt " [Erstellen eines Kontakts als Stellvertretung mithilfe der verwaltete EWS-API](#bk_createewsma)" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-165">The server responds to the **ResolveNames** request with a [ResolveNamesResponse](https://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the operation completed successfully and found only one result, or **ErrorNameResolutionMultipleResults** if multiple results were found - which is what's shown in third code example based on the contact [Create a contact as a delegate by using the EWS Managed API](#bk_createewsma).</span></span> <span data-ttu-id="ec3c9-166">Die Antwort enthält auch die [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) jedes Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-166">The response also contains the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of each result.</span></span> 
  
<span data-ttu-id="ec3c9-167">Der Wert des **ItemID** -Elements wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-167">The value of the **ItemId** element has been shortened for readability.</span></span> 
  
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
    <m:ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="ec3c9-168">Da Sie nun die **ItemID** für die Kontakte haben, die dem eindeutigen Namen entsprechen, können Sie Kontaktelemente mithilfe von EWS mithilfe von " **ItemID** " und " [impliziter Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit)" [als Stellvertretung abrufen, aktualisieren oder löschen](#bk_getews) , &mdash; und Sie müssen die SMTP-Adresse des Postfachbesitzers nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-168">Now that you have the **ItemId** for the contacts that match the ambiguous name, you can [Get, update, or delete contact items as a delegate by using EWS](#bk_getews) by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="ec3c9-169"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ec3c9-169"><a name="bk_getewsma"> </a></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="ec3c9-170">Abrufen, aktualisieren oder Löschen von Kontaktelementen als Stellvertretung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ec3c9-170">Get, update, or delete contact items as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="ec3c9-171">Mit dem verwaltete EWS-API können Sie einen Kontakt abrufen, aktualisieren oder löschen, genauso wie diese Aktionen ausgeführt werden, wenn Sie keinen Stellvertretungszugriff verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-171">You can use the EWS Managed API to get, update, or delete a contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="ec3c9-172">Der einzige Unterschied besteht darin, dass das Dienstobjekt für den Stellvertreter Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-172">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="ec3c9-173">Die im **Bindungs** Methodenaufruf enthaltene Element-ID identifiziert das Element im Postfachspeicher im Ordner Kontakte des Postfachbesitzers eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-173">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="ec3c9-174">**Tabelle 2. Verwaltete EWS-API Methoden, die mit einem Kontakt als Stellvertretung arbeiten**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-174">**Table 2. EWS Managed API methods working with a contact as a delegate**</span></span>

|<span data-ttu-id="ec3c9-175">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-175">**Task**</span></span>|<span data-ttu-id="ec3c9-176">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-176">**EWS Managed API method**</span></span>|<span data-ttu-id="ec3c9-177">**Codebeispiel**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-177">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec3c9-178">Abrufen eines Kontakts</span><span class="sxs-lookup"><span data-stu-id="ec3c9-178">Get a contact</span></span>  <br/> |[<span data-ttu-id="ec3c9-179">Bind</span><span class="sxs-lookup"><span data-stu-id="ec3c9-179">Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ec3c9-180">Abrufen eines Elements mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ec3c9-180">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="ec3c9-181">Einen Kontakt aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ec3c9-181">Update a contact</span></span>  <br/> |<span data-ttu-id="ec3c9-182">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec3c9-182">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="ec3c9-183">Aktualisieren eines Elements mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ec3c9-183">Update an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|<span data-ttu-id="ec3c9-184">Löschen eines Kontakts</span><span class="sxs-lookup"><span data-stu-id="ec3c9-184">Delete a contact</span></span>  <br/> |<span data-ttu-id="ec3c9-185">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec3c9-185">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="ec3c9-186">Löschen eines Elements mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ec3c9-186">Delete an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |

<span data-ttu-id="ec3c9-187"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="ec3c9-187"><a name="bk_getews"> </a></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="ec3c9-188">Abrufen, aktualisieren oder Löschen von Kontaktelementen als Stellvertretung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="ec3c9-188">Get, update, or delete contact items as a delegate by using EWS</span></span>

<span data-ttu-id="ec3c9-189">Sie können EWS verwenden, um einen Besprechungs-oder Termin Kontakt auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie diese Aktionen ausgeführt werden, wenn Sie keinen Stellvertretungszugriff verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-189">You can use EWS to get, update, or delete a meeting or appointment contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="ec3c9-190">Der einzige Unterschied besteht darin, dass das Dienstobjekt für den Stellvertreter Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-190">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="ec3c9-191">Die in der [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) -Anforderung enthaltene Element-ID identifiziert das Element im Postfachspeicher im Ordner Kontakte des Postfachbesitzers eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ec3c9-191">The item ID included in the [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) request uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="ec3c9-192">**Tabelle 3. EWS-Vorgänge für das Arbeiten mit einem Kontakt als Stellvertretung**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-192">**Table 3. EWS operations for working with a contact as a delegate**</span></span>

|<span data-ttu-id="ec3c9-193">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-193">**Task**</span></span>|<span data-ttu-id="ec3c9-194">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-194">**EWS operation**</span></span>|<span data-ttu-id="ec3c9-195">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="ec3c9-195">**Sample**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec3c9-196">Abrufen eines Kontakts</span><span class="sxs-lookup"><span data-stu-id="ec3c9-196">Get a contact</span></span>  <br/> |[<span data-ttu-id="ec3c9-197">GetItem</span><span class="sxs-lookup"><span data-stu-id="ec3c9-197">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="ec3c9-198">Abrufen eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="ec3c9-198">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="ec3c9-199">Einen Kontakt aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ec3c9-199">Update a contact</span></span>  <br/> |<span data-ttu-id="ec3c9-200">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec3c9-200">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="ec3c9-201">Aktualisieren eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="ec3c9-201">Update an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|<span data-ttu-id="ec3c9-202">Löschen eines Kontakts</span><span class="sxs-lookup"><span data-stu-id="ec3c9-202">Delete a contact</span></span>  <br/> |<span data-ttu-id="ec3c9-203">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="ec3c9-203">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |[<span data-ttu-id="ec3c9-204">Löschen eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="ec3c9-204">Delete an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec3c9-205">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec3c9-205">See also</span></span>

- [<span data-ttu-id="ec3c9-206">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec3c9-206">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
- [<span data-ttu-id="ec3c9-207">Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec3c9-207">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="ec3c9-208">Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec3c9-208">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
- [<span data-ttu-id="ec3c9-209">Personen und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec3c9-209">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
- [<span data-ttu-id="ec3c9-210">Auflösen von mehrdeutigen Namen mithilfe der EWS Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ec3c9-210">Resolve ambiguous names by using EWS in Exchange 2013</span></span>](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)
    

