---
title: Verarbeiten von Kontakten in Batches mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 455f475b-cb19-4e7a-8ff3-92f7028fceb0
description: In diesem Artikel erfahren Sie, wie Sie in einem einzigen Aufruf Batches von Kontakten erstellen, abrufen, aktualisieren und löschen, indem Sie das verwaltete EWS-API oder EWS in Exchange verwenden.
ms.openlocfilehash: 2e122f67693b4ba46120104d9a1f6d36b4d86f97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527803"
---
# <a name="process-contacts-in-batches-by-using-ews-in-exchange"></a><span data-ttu-id="20412-103">Verarbeiten von Kontakten in Batches mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="20412-103">Process contacts in batches by using EWS in Exchange</span></span>

<span data-ttu-id="20412-104">In diesem Artikel erfahren Sie, wie Sie in einem einzigen Aufruf Batches von Kontakten erstellen, abrufen, aktualisieren und löschen, indem Sie das verwaltete EWS-API oder EWS in Exchange verwenden.</span><span class="sxs-lookup"><span data-stu-id="20412-104">Learn how to create, get, update, and delete batches of contacts in a single call by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="20412-105">Sie können die verwaltete EWS-API oder EWS verwenden, um mit Batches von Kontakten zu arbeiten, um die Anzahl der Anrufe zu reduzieren, die ein Client an einen Exchange-Server macht.</span><span class="sxs-lookup"><span data-stu-id="20412-105">You can use the EWS Managed API or EWS to work with batches of contacts to reduce the number of calls a client makes to an Exchange server.</span></span> <span data-ttu-id="20412-106">Wenn Sie die verwaltete EWS-API verwenden, um Kontakte in Batches zu erstellen, abzurufen, zu aktualisieren und zu löschen, verwenden Sie [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objektmethoden, während Sie bei der Arbeit mit einzelnen Kontakten [Kontakt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) Objektmethoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="20412-106">When you use the EWS Managed API to create, get, update, and delete contacts in batches, you use [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object methods, whereas when you work with single contacts, you use [Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) object methods.</span></span> <span data-ttu-id="20412-107">Wenn Sie EWS verwenden, verwenden Sie dieselben Vorgänge, um sowohl mit einem einzelnen Kontakt als auch mit Batches von Kontakten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="20412-107">If you are using EWS, you use the same operations to work with both a single contact and batches of contacts.</span></span> 
  
<span data-ttu-id="20412-108">**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge zum Arbeiten mit Batches von Kontakten**</span><span class="sxs-lookup"><span data-stu-id="20412-108">**Table 1. EWS Managed API methods and EWS operations for working with batches of contacts**</span></span>

|<span data-ttu-id="20412-109">**Gewünschte Aktion**</span><span class="sxs-lookup"><span data-stu-id="20412-109">**In order to…**</span></span>|<span data-ttu-id="20412-110">**Verwenden Sie diese verwaltete EWS-API-Methode**</span><span class="sxs-lookup"><span data-stu-id="20412-110">**Use this EWS Managed API method**</span></span>|<span data-ttu-id="20412-111">**Zu verwendender EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="20412-111">**Use this EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="20412-112">Erstellen von Kontakten in Batches</span><span class="sxs-lookup"><span data-stu-id="20412-112">Create contacts in batches</span></span>  <br/> |[<span data-ttu-id="20412-113">Datei "ExchangeService. CreateItems</span><span class="sxs-lookup"><span data-stu-id="20412-113">ExchangeService.CreateItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="20412-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="20412-114">CreateItem</span></span>](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="20412-115">Abrufen von Kontakten in Batches</span><span class="sxs-lookup"><span data-stu-id="20412-115">Get contacts in batches</span></span>  <br/> |<span data-ttu-id="20412-116">[Datei "ExchangeService. BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) oder [Datei" ExchangeService. LoadPropertiesForItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20412-116">[ExchangeService.BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) or [ExchangeService.LoadPropertiesForItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="20412-117">GetItem</span><span class="sxs-lookup"><span data-stu-id="20412-117">GetItem</span></span>](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="20412-118">Aktualisieren von Kontakten in Batches</span><span class="sxs-lookup"><span data-stu-id="20412-118">Update contacts in batches</span></span>  <br/> |[<span data-ttu-id="20412-119">Datei "ExchangeService. Update Items</span><span class="sxs-lookup"><span data-stu-id="20412-119">ExchangeService.UpdateItems</span></span>](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="20412-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="20412-120">UpdateItem</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="20412-121">Löschen von Kontakten in Batches</span><span class="sxs-lookup"><span data-stu-id="20412-121">Delete contacts in batches</span></span>  <br/> |[<span data-ttu-id="20412-122">Datei "ExchangeService. DeleteItems</span><span class="sxs-lookup"><span data-stu-id="20412-122">ExchangeService.DeleteItems</span></span>](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="20412-123">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="20412-123">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> |
   
<span data-ttu-id="20412-124">In diesem Artikel erfahren Sie, wie Sie grundlegende Aufgaben für Batches von Kontakten mithilfe der verwaltete EWS-API oder EWS ausführen.</span><span class="sxs-lookup"><span data-stu-id="20412-124">In this article, you'll learn how to complete basic tasks for batches of contacts by using the EWS Managed API or EWS.</span></span>
  
## <a name="create-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="20412-125">Erstellen von Kontakten in Batches mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="20412-125">Create contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="20412-126"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="20412-126"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="20412-127">Sie können Kontakte in Batches erstellen, indem Sie die verwaltete EWS-API [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) -Methode verwenden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="20412-127">You can create contacts in batches by using the EWS Managed API [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="20412-128">In diesem Beispiel werden drei [Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) -Objekte lokal erstellt, jeder Kontakt wird einer Auflistung hinzugefügt, und anschließend wird die **CreateItems** -Methode für die Auflistung der Kontakte aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="20412-128">This example creates three [Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) objects locally, adds each contact to a collection, then calls the **CreateItems** method on the collection of contacts.</span></span> 
  
```cs
public static Collection<ItemId> CreateContactsInBatch(ExchangeService service)
{
    // These are unsaved local instances of a Contact object.
    // Despite the required parameter of an ExchangeService object (service), no call
    // to an Exchange server is made when the objects are instantiated.
    // A call to the Exchange server is made when the service.CreateItems() method is called.
    Contact contact1 = new Contact(service);
    Contact contact2 = new Contact(service);
    Contact contact3 = new Contact(service);
    // Set the properties on the first contact.
    contact1.DisplayName = "Sadie Daniels";
    contact1.EmailAddresses[EmailAddressKey.EmailAddress1] = new EmailAddress("sadie@contoso.com");
    
    // Set the properties on the second contact.
    contact2.DisplayName = "Alfred Welker";
    contact2.EmailAddresses[EmailAddressKey.EmailAddress1] = new EmailAddress("alfred@contoso.com");
    // Set the properties on the third contact.
    contact3.DisplayName = "Hope Gross";
    contact3.EmailAddresses[EmailAddressKey.EmailAddress1] = new EmailAddress("hope@contoso.com");
    // Add the Contact objects to a collection.
    Collection<Contact> contactItems = new Collection<Contact>() { contact1, contact2, contact3 };
    // Create the batch of contacts on the server.
    // This method call results in an CreateItem call to EWS.
    ServiceResponseCollection<ServiceResponse> response = service.CreateItems(contactItems, WellKnownFolderName.Contacts, null, null);
    // Instantiate a collection of item IDs to populate from the values that are returned by the Exchange server.
    Collection<ItemId> itemIds = new Collection<ItemId>();
    // Collect the item IDs from the created contacts.
    foreach (Contact contact in contactItems)
    {
        try
        {
            itemIds.Add(contact.Id);
            Console.WriteLine("Contact '{0}' created successfully.", contact.DisplayName);
        }
        catch (Exception ex)
        {
            // Print out the exception and the last eight characters of the item ID.
            Console.WriteLine("Exception while creating contact {0}: {1}", contact.Id.ToString().Substring(144), ex.Message);
        }
    }
    // Determine whether the CreateItems method call completed successfully.
    if (response.OverallResult == ServiceResult.Success)
    {
            Console.WriteLine("All locally created contacts were successfully created in the Contacts folder.");
            Console.WriteLine("\r\n");
    }
   
    // If the method did not return success, print the result message for each contact.
    else
    {
        int counter = 1;
        foreach (ServiceResponse resp in response)
        {
            // Print out the result and the last eight characters of the item ID.
            Console.WriteLine("Result (contact {0}), id {1}: {2}", counter, itemIds[counter - 1].ToString().Substring(144), resp.Result);
            Console.WriteLine("Error Code: {0}", resp.ErrorCode);
            Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
            Console.WriteLine("\r\n");
            counter++;
        }
    }
    return itemIds;
}
```

## <a name="create-contacts-in-batches-by-using-ews"></a><span data-ttu-id="20412-129">Erstellen von Kontakten in Batches mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="20412-129">Create contacts in batches by using EWS</span></span>
<span data-ttu-id="20412-130"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="20412-130"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="20412-131">Sie können Kontakte in Batches erstellen, indem Sie den [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -EWS-Vorgang verwenden, wie im folgenden Codebeispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="20412-131">You can create contacts in batches by using the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="20412-132">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API verwenden, um [Kontakte in Batches zu erstellen](#bk_EWSMA).</span><span class="sxs-lookup"><span data-stu-id="20412-132">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [create contacts in batches](#bk_EWSMA).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:CreateItem>
        <m:SavedItemFolderId>
          <t:DistinguishedFolderId Id="contacts" />
        </m:SavedItemFolderId>
        <m:Items>
          <t:Contact>
            <t:DisplayName>Sadie Daniels</t:DisplayName>
            <t:EmailAddresses>
              <t:Entry Key="EmailAddress1">sadie@contoso.com</t:Entry>
            </t:EmailAddresses>
          </t:Contact>
          <t:Contact>
            <t:DisplayName>Alfred Welker</t:DisplayName>
            <t:EmailAddresses>
              <t:Entry Key="EmailAddress1">alfred@contoso.com</t:Entry>
            </t:EmailAddresses>
          </t:Contact>
          <t:Contact>
            <t:DisplayName>Hope Gross</t:DisplayName>
            <t:EmailAddresses>
              <t:Entry Key="EmailAddress1">hope@contoso.com</t:Entry>
            </t:EmailAddresses>
          </t:Contact>
        </m:Items>
      </m:CreateItem>
    </soap:Body>
  </soap:Envelope>
```

<span data-ttu-id="20412-133">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die einen [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert von **noError** für jeden der neuen Kontakte enthält, der angibt, dass jeder Kontakt erfolgreich erstellt und gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="20412-133">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new contacts, which indicates that each contact was created and saved successfully.</span></span> 
  
## <a name="get-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="20412-134">Abrufen von Kontakten in Batches mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="20412-134">Get contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="20412-135"><a name="bk_EWSMAGet"> </a></span><span class="sxs-lookup"><span data-stu-id="20412-135"><a name="bk_EWSMAGet"> </a></span></span>

<span data-ttu-id="20412-136">Sie können Kontakte in Batches abrufen, indem Sie die verwaltete EWS-API [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) -Methode verwenden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="20412-136">You can get contacts in batches by using the EWS Managed API [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="20412-137">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="20412-137">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<Contact> BatchGetContactItems(ExchangeService service, Collection<ItemId> itemIds)
        {
            // Create a property set that limits the properties returned by the Bind method to only those that are required.
            PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ContactSchema.DisplayName);
            // Get the items from the server.
            // This method call results in a GetItem call to EWS.
            ServiceResponseCollection<GetItemResponse> response = service.BindToItems(itemIds, propSet);
            // Instantiate a collection of Contact objects to populate from the values that are returned by the Exchange server.
            Collection<Contact> contactItems = new Collection<Contact>();
            foreach (GetItemResponse getItemResponse in response)
            {
                try
                {
                    Item item = getItemResponse.Item;
                    Contact contact = (Contact)item;
                    contactItems.Add(contact);
                    // Print out confirmation and the last eight characters of the item ID.
                    Console.WriteLine("Found item {0}.", contact.Id.ToString().Substring(144));
                }
                catch (Exception ex)
                {
                    Console.WriteLine("Exception while getting a contact: {0}", ex.Message);
                }
            }
            // Check for success of the BindToItems method call.
            if (response.OverallResult == ServiceResult.Success)
            {
                Console.WriteLine("All contacts retrieved successfully.");
                Console.WriteLine("\r\n");
            }
            return contactItems;
        }

```

## <a name="get-contacts-in-batches-by-using-ews"></a><span data-ttu-id="20412-138">Abrufen von Kontakten in Batches mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="20412-138">Get contacts in batches by using EWS</span></span>
<span data-ttu-id="20412-139"><a name="bk_EWSMAGet"> </a></span><span class="sxs-lookup"><span data-stu-id="20412-139"><a name="bk_EWSMAGet"> </a></span></span>

<span data-ttu-id="20412-140">Sie können Kontakte in Batches mit dem [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -EWS-Vorgang und dem Code im folgenden Beispiel abrufen.</span><span class="sxs-lookup"><span data-stu-id="20412-140">You can get contacts in batches by using the [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation and the code in the following example.</span></span> <span data-ttu-id="20412-141">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API zum [Abrufen von Kontakten in Batches](#bk_EWSMAGet)verwenden.</span><span class="sxs-lookup"><span data-stu-id="20412-141">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get contacts in batches](#bk_EWSMAGet).</span></span> <span data-ttu-id="20412-142">Das **ItemID** -Attribut wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="20412-142">The **ItemId** attribute has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:GetItem>
        <m:ItemShape>
          <t:BaseShape>IdOnly</t:BaseShape>
          <t:AdditionalProperties>
            <t:FieldURI FieldURI="contacts:DisplayName" />
          </t:AdditionalProperties>
        </m:ItemShape>
        <m:ItemIds>
          <t:ItemId Id="ceJwVAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yS" />
          <t:ItemId Id="ceJwWAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yT" />
          <t:ItemId Id="ceJwXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yU" />
        </m:ItemIds>
      </m:GetItem>
    </soap:Body>
  </soap:Envelope>
```

<span data-ttu-id="20412-143">Der Server antwortet auf die **GetItem** -Anforderung mit einer [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) -Nachricht, die die ID und den Anzeigenamen für jeden der angeforderten Kontakte enthält.</span><span class="sxs-lookup"><span data-stu-id="20412-143">The server responds to the **GetItem** request with a [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes the ID and the display name for each of the requested contacts.</span></span> 
  
## <a name="update-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="20412-144">Aktualisieren von Kontakten in Batches mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="20412-144">Update contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="20412-145"><a name="bk_EWSMAUpdate"> </a></span><span class="sxs-lookup"><span data-stu-id="20412-145"><a name="bk_EWSMAUpdate"> </a></span></span>

<span data-ttu-id="20412-146">Sie können Kontakte in Batches aktualisieren, indem Sie die verwaltete EWS-API [Update Items](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) -Methode verwenden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="20412-146">You can update contacts in batches by using the EWS Managed API [UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="20412-147">Im vorherigen Beispiel wird der Kontakt erstellt, aber nicht angegeben, für wen er verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="20412-147">The previous example creates the contact but does not specify who they work for.</span></span> <span data-ttu-id="20412-148">Sie können den Code in diesem Beispiel verwenden, um alle Ihre Kontakte gleichzeitig zu aktualisieren, um den Namen Ihres Unternehmens einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="20412-148">You can use the code in this example to update all your contacts at once to include their company name.</span></span> 
  
<span data-ttu-id="20412-149">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="20412-149">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<Contact> BatchUpdateContactItems(ExchangeService service, Collection<Contact> contactItems)
        {
            // Update the company name of each contact locally.
            foreach (Contact contact in contactItems)
            {
                // Update the company name of the contact.
                contact.CompanyName = "Contoso";
                // Print out confirmation with the last eight characters of the item ID and the contact company name.
                Console.WriteLine("Updated local contact {0} with the company name '{1}'.", contact.Id.ToString().Substring(144), contact.CompanyName);
            }
            
            // Send the item updates to the server.
            // This method call results in an UpdateItem call to EWS.
            ServiceResponseCollection<UpdateItemResponse> response = service.UpdateItems(contactItems, WellKnownFolderName.Contacts, ConflictResolutionMode.AutoResolve, null, null);
            // Verify the success of the UpdateItems method call.
            if (response.OverallResult == ServiceResult.Success)
            {
                Console.WriteLine("All contacts updated successfully.\r\n");
            }
            // If the method did not return success, print the result message for each contact.
            else
            {
                Console.WriteLine("All contacts were not successfully saved on the server.\r\n");
                int counter = 1;
                foreach (ServiceResponse resp in response)
                {
                    Console.WriteLine("Result for (contact {0}): {1}", counter, resp.Result);
                    Console.WriteLine("Error Code: {0}", resp.ErrorCode);
                    Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
                    counter++;
                }
            }
            return contactItems;
        }    

```

## <a name="update-contacts-in-batches-by-using-ews"></a><span data-ttu-id="20412-150">Aktualisieren von Kontakten in Batches mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="20412-150">Update contacts in batches by using EWS</span></span>
<span data-ttu-id="20412-151"><a name="bk_EWSMAUpdate"> </a></span><span class="sxs-lookup"><span data-stu-id="20412-151"><a name="bk_EWSMAUpdate"> </a></span></span>

<span data-ttu-id="20412-152">Sie können Kontakte in Batches aktualisieren, indem Sie den [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -EWS-Vorgang verwenden, wie im folgenden Codebeispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="20412-152">You can update contacts in batches by using the [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation, as shown in following code example.</span></span> <span data-ttu-id="20412-153">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie den verwaltete EWS-API verwenden, um [Kontakte in Batches zu aktualisieren](#bk_EWSMAUpdate).</span><span class="sxs-lookup"><span data-stu-id="20412-153">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [update contacts in batches](#bk_EWSMAUpdate).</span></span> <span data-ttu-id="20412-154">Das **ItemID** -Attribut wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="20412-154">The **ItemId** attribute has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:UpdateItem ConflictResolution="AutoResolve">
        <m:SavedItemFolderId>
          <t:DistinguishedFolderId Id="contacts" />
        </m:SavedItemFolderId>
        <m:ItemChanges>
          <t:ItemChange>
            <t:ItemId Id="ceJwVAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yS" />
            <t:Updates>
              <t:SetItemField>
                <t:FieldURI FieldURI="contacts:CompanyName" />
                <t:Contact>
                  <t:CompanyName>Contoso</t:CompanyName>
                </t:Contact>
              </t:SetItemField>
            </t:Updates>
          </t:ItemChange>
          <t:ItemChange>
            <t:ItemId Id="ceJwWAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yT" />
            <t:Updates>
              <t:SetItemField>
                <t:FieldURI FieldURI="contacts:CompanyName" />
                <t:Contact>
                  <t:CompanyName>Contoso</t:CompanyName>
                </t:Contact>
              </t:SetItemField>
            </t:Updates>
          </t:ItemChange>
          <t:ItemChange>
            <t:ItemId Id="ceJwXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yU" />
            <t:Updates>
              <t:SetItemField>
                <t:FieldURI FieldURI="contacts:CompanyName" />
                <t:Contact>
                  <t:CompanyName>Contoso</t:CompanyName>
                </t:Contact>
              </t:SetItemField>
            </t:Updates>
          </t:ItemChange>
        </m:ItemChanges>
      </m:UpdateItem>
    </soap:Body>
  </soap:Envelope>
```

<span data-ttu-id="20412-155">Der Server antwortet auf die **UpdateItem** -Anforderung mit einer [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert **noError**enthält, der angibt, dass jedes Update erfolgreich auf dem Server gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="20412-155">The server responds to the **UpdateItem** request with an [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that each of the updates was saved successfully on the server.</span></span> <span data-ttu-id="20412-156">Alle Konflikte werden im [ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) -Element gemeldet.</span><span class="sxs-lookup"><span data-stu-id="20412-156">Any conflicts are reported in the [ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) element.</span></span> 
  
## <a name="delete-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="20412-157">Löschen von Kontakten in Batches mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="20412-157">Delete contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="20412-158"><a name="bk_EWSMADelete"> </a></span><span class="sxs-lookup"><span data-stu-id="20412-158"><a name="bk_EWSMADelete"> </a></span></span>

<span data-ttu-id="20412-159">Sie können Kontakte in Batches löschen, indem Sie die [DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode verwenden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="20412-159">You can delete contacts in batches by using the [DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) EWS Managed API method, as shown in the following example.</span></span> <span data-ttu-id="20412-160">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="20412-160">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void BatchDeleteContactItems(ExchangeService service, Collection<ItemId> itemIds)
        {
            // Delete the batch of contact objects.
            // This method call results in an DeleteItem call to EWS.
            ServiceResponseCollection<ServiceResponse> response = service.DeleteItems(itemIds, DeleteMode.SoftDelete, null, AffectedTaskOccurrence.AllOccurrences);
            // Check for success of the DeleteItems method call.
            // DeleteItems returns success even if it does not find all the item IDs.
            if (response.OverallResult == ServiceResult.Success)
            {
                Console.WriteLine("Contacts deleted successfully.\r\n");
            }
            // If the method did not return success, print a message.
            else
            {
                Console.WriteLine("Not all contacts deleted successfully.\r\n");
            }
        }

```

## <a name="delete-contacts-in-batches-by-using-ews"></a><span data-ttu-id="20412-161">Löschen von Kontakten in Batches mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="20412-161">Delete contacts in batches by using EWS</span></span>
<span data-ttu-id="20412-162"><a name="bk_EWSMADelete"> </a></span><span class="sxs-lookup"><span data-stu-id="20412-162"><a name="bk_EWSMADelete"> </a></span></span>

<span data-ttu-id="20412-163">Sie können Kontakte in Batches löschen, indem Sie den EWS-Vorgang [DeleteItem](../web-service-reference/deleteitem-operation.md) verwenden, wie im folgenden Codebeispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="20412-163">You can delete contacts in batches by using the [DeleteItem](../web-service-reference/deleteitem-operation.md) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="20412-164">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API verwenden, um [Kontakte in Batches zu löschen](#bk_EWSMADelete).</span><span class="sxs-lookup"><span data-stu-id="20412-164">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [delete contacts in batches](#bk_EWSMADelete).</span></span> <span data-ttu-id="20412-165">Das **ItemID** -Attribut wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="20412-165">The **ItemId** attribute has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:DeleteItem DeleteType="SoftDelete" AffectedTaskOccurrences="AllOccurrences">
        <m:ItemIds>
          <t:ItemId Id="ceJwYAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yY" />
          <t:ItemId Id="ceJwZAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yZ" />
          <t:ItemId Id="ceJwaAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51ya" />
        </m:ItemIds>
      </m:DeleteItem>
    </soap:Body>
  </soap:Envelope>
```

<span data-ttu-id="20412-166">Der Server antwortet auf die **DeleteItem** -Anforderung mit einer [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert **noError** für jedes entfernte Element enthält.</span><span class="sxs-lookup"><span data-stu-id="20412-166">The server responds to the **DeleteItem** request with a [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each item that was removed.</span></span> <span data-ttu-id="20412-167">Beachten Sie, dass der Vorgang auch dann Success zurückgegeben wird, wenn die Element-ID nicht gefunden werden konnte.</span><span class="sxs-lookup"><span data-stu-id="20412-167">Note that the operation also returns success if the item ID could not be found.</span></span> 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a><span data-ttu-id="20412-168">Überprüfen, ob ein Batchprozess erfolgreich abgeschlossen wurde</span><span class="sxs-lookup"><span data-stu-id="20412-168">Verifying that a batch process completed successfully</span></span>
<span data-ttu-id="20412-169"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="20412-169"><a name="bk_successful"> </a></span></span>

<span data-ttu-id="20412-170">Wenn ein oder mehrere Kontakte in einer Batchanforderung nicht wie angefordert verarbeitet werden können, wird für jeden Kontakt, der fehlgeschlagen ist, ein Fehler zurückgegeben, und die restlichen Kontakte im Batch werden wie erwartet verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="20412-170">When one or more contacts in a batched request can't be processed as requested, an error is returned for each contact that failed, and the rest of the contacts in the batch are processed as expected.</span></span> <span data-ttu-id="20412-171">Fehler in der Batchverarbeitung können auftreten, wenn das Element gelöscht wurde und daher nicht abgerufen oder aktualisiert werden kann oder wenn das Element in einen anderen Ordner verschoben wurde und daher über eine neue Element-ID verfügt und nicht mit der gesendeten Element-ID geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="20412-171">Failures in batch processing can occur if the item was deleted, and therefore can't be retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID, and cannot be modified with the item ID sent.</span></span> <span data-ttu-id="20412-172">Die Informationen in diesem Abschnitt zeigen, wie Fehlerdetails zu Fehlern bei der Batchverarbeitung von Kontakten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="20412-172">The information in this section shows how to get error details about failures in batch processing of contacts.</span></span>
  
<span data-ttu-id="20412-173">Um den Erfolg eines Batchprozesses mithilfe der verwaltete EWS-API zu überprüfen, können Sie überprüfen, ob die [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) -Eigenschaft des [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) gleich [ServiceResult. Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)ist.</span><span class="sxs-lookup"><span data-stu-id="20412-173">To verify the success of a batch process by using the EWS Managed API, you can check that the [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) property of the [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) is equal to [ServiceResult.Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="20412-174">Wenn dies der Fall ist, wurden alle Kontakte erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="20412-174">If so, all the contacts were processed successfully.</span></span> <span data-ttu-id="20412-175">Wenn **OverallResult** nicht gleich **ServiceResult. Success**ist, wurden mindestens einer der Kontakte nicht erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="20412-175">If the **OverallResult** is not equal to **ServiceResult.Success**, one or more of the contacts were not processed successfully.</span></span> <span data-ttu-id="20412-176">Jedes der Objekte, die in der **ServiceResponseCollection** zurückgegeben werden, enthält die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="20412-176">Each of the objects returned in the **ServiceResponseCollection** contains the following properties:</span></span> 
  
- [<span data-ttu-id="20412-177">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="20412-177">ErrorCode</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="20412-178">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="20412-178">ErrorDetails</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="20412-179">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="20412-179">ErrorMessage</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="20412-180">ErrorProperties</span><span class="sxs-lookup"><span data-stu-id="20412-180">ErrorProperties</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="20412-181">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="20412-181">Result</span></span>](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
<span data-ttu-id="20412-182">Diese Eigenschaften enthalten Informationen dazu, warum die Kontakte nicht wie angefordert verarbeitet werden konnten.</span><span class="sxs-lookup"><span data-stu-id="20412-182">These properties contain information about why the contacts could not be processed as requested.</span></span> <span data-ttu-id="20412-183">In den Beispielen in diesem Artikel werden das **Ergebnis**, **errorCode**und **ErrorMessage** für jeden fehlerhaften Kontakt gedruckt.</span><span class="sxs-lookup"><span data-stu-id="20412-183">The examples in this article print out the **Result**, **ErrorCode**, and **ErrorMessage** for each failed contact.</span></span> <span data-ttu-id="20412-184">Sie können diese Ergebnisse verwenden, um das Problem zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="20412-184">You can use these results to investigate the issue.</span></span> 
  
<span data-ttu-id="20412-185">Überprüfen Sie für EWS das [ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) -Attribut für jedes verarbeitete Element, um den Erfolg eines Batchprozesses zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="20412-185">For EWS, to verify the success of a batched process, check the [ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) attribute for each item being processed.</span></span> <span data-ttu-id="20412-186">Im folgenden finden Sie die grundlegende Struktur des **ResponseMessageType**, den Basistyp, von dem alle Antwortnachrichten abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="20412-186">The following is the basic structure of the **ResponseMessageType**, the base type from which all response messages are derived.</span></span> 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

<span data-ttu-id="20412-187">Das **ResponseClass** -Attribut **ist auf "erfolgreich"** festgelegt, wenn der Kontakt erfolgreich verarbeitet wurde, oder **Fehler** , wenn der Kontakt nicht erfolgreich verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="20412-187">The **ResponseClass** attribute is set to **Success** if the contact was processed successfully, or **Error** if the contact was not processed successfully.</span></span> <span data-ttu-id="20412-188">Bei Kontakten wird während der Batchverarbeitung keine **Warnung angezeigt** .</span><span class="sxs-lookup"><span data-stu-id="20412-188">For contacts, you will not encounter a **Warning** during batch processing.</span></span> <span data-ttu-id="20412-189">Wenn der **ResponseClass** **erfolgreich**ist, wird das [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element, das folgt, auch immer auf **noError**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="20412-189">If the **ResponseClass** is **Success**, the [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element that follows is also always set to **NoError**.</span></span> <span data-ttu-id="20412-190">Wenn das **ResponseClass** -Element **fehlerhaft**ist, müssen Sie die Werte der [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)-, **Response Code**-und [messagexml verwendet](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) -Elemente überprüfen, um zu ermitteln, was das Problem verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="20412-190">If the **ResponseClass** is **Error**, you need to check the values of the [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**, and [MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) elements to determine what caused the problem.</span></span> <span data-ttu-id="20412-191">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) wird derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="20412-191">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) is currently unused.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20412-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20412-192">See also</span></span>


- [<span data-ttu-id="20412-193">Personen und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="20412-193">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
    
- [<span data-ttu-id="20412-194">Verarbeiten von E-Mails in Batches mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="20412-194">Process email messages in batches by using EWS in Exchange</span></span>](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="20412-195">Verarbeiten von Kalenderelementen in Batches in Exchange</span><span class="sxs-lookup"><span data-stu-id="20412-195">Process calendar items in batches in Exchange</span></span>](how-to-process-calendar-items-in-batches-in-exchange.md)
    

