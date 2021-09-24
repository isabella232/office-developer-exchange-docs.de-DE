---
title: Verarbeiten von Kontakten in Batches mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 455f475b-cb19-4e7a-8ff3-92f7028fceb0
description: Erfahren Sie, wie Sie Mithilfe der verwalteten EWS-API oder von EWS in Exchange Batches von Kontakten in einem einzigen Aufruf erstellen, abrufen, aktualisieren und löschen.
ms.openlocfilehash: e70618dc0a9ea3f2d534c79fff627393ced8f1cb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522222"
---
# <a name="process-contacts-in-batches-by-using-ews-in-exchange"></a>Verarbeiten von Kontakten in Batches mithilfe von EWS in Exchange

Erfahren Sie, wie Sie Mithilfe der verwalteten EWS-API oder von EWS in Exchange Batches von Kontakten in einem einzigen Aufruf erstellen, abrufen, aktualisieren und löschen.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um mit Batches von Kontakten zu arbeiten, um die Anzahl der Aufrufe zu verringern, die ein Client an einen Exchange Server sendet. Wenn Sie die verwaltete EWS-API zum Erstellen, Abrufen, Aktualisieren und Löschen von Kontakten in Batches verwenden, verwenden Sie [ExchangeService-Objektmethoden,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) während Sie bei der Arbeit mit einzelnen Kontakten [Contact-Objektmethoden](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) verwenden. Wenn Sie EWS verwenden, verwenden Sie die gleichen Vorgänge, um sowohl mit einem einzelnen Kontakt als auch mit Batches von Kontakten zu arbeiten. 
  
**Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge zum Arbeiten mit Batches von Kontakten**

|**Gewünschte Aktion**|**Verwenden dieser verwalteten EWS-API-Methode**|**Zu verwendender EWS-Vorgang**|
|:-----|:-----|:-----|
|Erstellen von Kontakten in Batches  <br/> |[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Abrufen von Kontakten in Batches  <br/> |[ExchangeService.BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) oder [ExchangeService.LoadPropertiesForItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|Aktualisieren von Kontakten in Batches  <br/> |[ExchangeService.UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen von Kontakten in Batches  <br/> |[ExchangeService.DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
In diesem Artikel erfahren Sie, wie Sie grundlegende Aufgaben für Batches von Kontakten mithilfe der verwalteten EWS-API oder EWS ausführen.
  
## <a name="create-contacts-in-batches-by-using-the-ews-managed-api"></a>Erstellen von Kontakten in Batches mithilfe der verwalteten EWS-API
<a name="bk_EWSMA"> </a>

Sie können Kontakte in Batches mithilfe der [CreateItems-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) der verwalteten EWS-API erstellen, wie im folgenden Beispiel gezeigt. In diesem Beispiel werden drei [Contact-Objekte](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) lokal erstellt, jeder Kontakt zu einer Auflistung hinzugefügt und anschließend die **CreateItems-Methode** für die Kontaktauflistung aufgerufen. 
  
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

## <a name="create-contacts-in-batches-by-using-ews"></a>Erstellen von Kontakten in Batches mithilfe von EWS
<a name="bk_EWSMA"> </a>

Sie können Kontakte in Batches mithilfe des [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS-Vorgangs erstellen, wie im folgenden Codebeispiel gezeigt. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die verwaltete EWS-API zum Erstellen von [Kontakten in Batches](#bk_EWSMA)verwenden.
  
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

Der Server antwortet auf die **CreateItem-Anforderung** mit einer [CreateItemResponse-Nachricht,](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) die den [ResponseCode-Wert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** für jeden neuen Kontakt enthält, der angibt, dass jeder Kontakt erstellt und erfolgreich gespeichert wurde. 
  
## <a name="get-contacts-in-batches-by-using-the-ews-managed-api"></a>Abrufen von Kontakten in Batches mithilfe der verwalteten EWS-API
<a name="bk_EWSMAGet"> </a>

Sie können Kontakte in Batches abrufen, indem Sie die EWS Managed API [BindToItems-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) verwenden, wie im folgenden Beispiel gezeigt. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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

## <a name="get-contacts-in-batches-by-using-ews"></a>Abrufen von Kontakten in Batches mithilfe von EWS
<a name="bk_EWSMAGet"> </a>

Sie können Kontakte in Batches abrufen, indem Sie den [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS-Vorgang und den Code im folgenden Beispiel verwenden. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die verwaltete EWS-API zum Abrufen von [Kontakten in Batches](#bk_EWSMAGet)verwenden. Das **ItemId-Attribut** wurde zur besseren Lesbarkeit gekürzt. 
  
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

Der Server antwortet auf die **GetItem-Anforderung** mit einer [GetItemResponse-Nachricht,](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) die die ID und den Anzeigenamen für jeden der angeforderten Kontakte enthält. 
  
## <a name="update-contacts-in-batches-by-using-the-ews-managed-api"></a>Aktualisieren von Kontakten in Batches mithilfe der verwalteten EWS-API
<a name="bk_EWSMAUpdate"> </a>

Sie können Kontakte in Batches aktualisieren, indem Sie die EWS Managed API [UpdateItems-Methode](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) verwenden, wie im folgenden Beispiel gezeigt. Im vorherigen Beispiel wird der Kontakt erstellt, aber nicht angegeben, für wen er arbeitet. Sie können den Code in diesem Beispiel verwenden, um alle Kontakte gleichzeitig so zu aktualisieren, dass sie den Firmennamen enthalten. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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

## <a name="update-contacts-in-batches-by-using-ews"></a>Aktualisieren von Kontakten in Batches mithilfe von EWS
<a name="bk_EWSMAUpdate"> </a>

Sie können Kontakte in Batches aktualisieren, indem Sie den [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS-Vorgang verwenden, wie im folgenden Codebeispiel gezeigt. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die verwaltete EWS-API zum Aktualisieren von [Kontakten in Batches](#bk_EWSMAUpdate)verwenden. Das **ItemId-Attribut** wurde zur besseren Lesbarkeit gekürzt. 
  
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

Der Server antwortet auf die **UpdateItem-Anforderung** mit einer [UpdateItemResponse-Nachricht,](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) die den [ResponseCode-Wert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** enthält, der angibt, dass jedes der Updates erfolgreich auf dem Server gespeichert wurde. Alle Konflikte werden im [ConflictResult-Element](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) gemeldet. 
  
## <a name="delete-contacts-in-batches-by-using-the-ews-managed-api"></a>Löschen von Kontakten in Batches mithilfe der verwalteten EWS-API
<a name="bk_EWSMADelete"> </a>

Sie können Kontakte in Batches löschen, indem Sie die verwaltete EWS-API-Methode ["DeleteItems"](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) verwenden, wie im folgenden Beispiel gezeigt. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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

## <a name="delete-contacts-in-batches-by-using-ews"></a>Löschen von Kontakten in Batches mithilfe von EWS
<a name="bk_EWSMADelete"> </a>

Sie können Kontakte in Batches mithilfe des [DeleteItem](../web-service-reference/deleteitem-operation.md) EWS-Vorgangs löschen, wie im folgenden Codebeispiel gezeigt. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die verwaltete EWS-API zum Löschen von [Kontakten in Batches](#bk_EWSMADelete)verwenden. Das **ItemId-Attribut** wurde zur besseren Lesbarkeit gekürzt. 
  
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

Der Server antwortet auf die **DeleteItem-Anforderung** mit einer [DeleteItemResponse-Nachricht,](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) die den [ResponseCode-Wert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **"NoError"** für jedes entfernte Element enthält. Beachten Sie, dass der Vorgang auch erfolglos zurückgibt, wenn die Element-ID nicht gefunden werden konnte. 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a>Überprüfen, ob ein Batchprozess erfolgreich abgeschlossen wurde
<a name="bk_successful"> </a>

Wenn ein oder mehrere Kontakte in einer Batchanforderung nicht wie angefordert verarbeitet werden können, wird für jeden fehlgeschlagenen Kontakt ein Fehler zurückgegeben, und die restlichen Kontakte im Batch werden wie erwartet verarbeitet. Fehler bei der Batchverarbeitung können auftreten, wenn das Element gelöscht wurde und daher nicht abgerufen oder aktualisiert werden kann oder wenn das Element in einen anderen Ordner verschoben wurde und daher über eine neue Element-ID verfügt und nicht mit der gesendeten Element-ID geändert werden kann. Die Informationen in diesem Abschnitt zeigen, wie Fehlerdetails zu Fehlern bei der Batchverarbeitung von Kontakten abgerufen werden.
  
Um den Erfolg eines Batchprozesses mithilfe der verwalteten EWS-API zu überprüfen, können Sie überprüfen, ob die [OverallResult-Eigenschaft](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) der [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) gleich [ServiceResult.Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)ist. Wenn ja, wurden alle Kontakte erfolgreich verarbeitet. Wenn das **OverallResult** nicht gleich **ServiceResult.Success** ist, wurden mindestens einer der Kontakte nicht erfolgreich verarbeitet. Jedes der in **ServiceResponseCollection** zurückgegebenen Objekte enthält die folgenden Eigenschaften: 
  
- [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [Ergebnis](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
Diese Eigenschaften enthalten Informationen dazu, warum die Kontakte nicht wie angefordert verarbeitet werden konnten. Die Beispiele in diesem Artikel drucken die **Ergebnisse**, **ErrorCode** und **ErrorMessage** für jeden fehlgeschlagenen Kontakt aus. Sie können diese Ergebnisse verwenden, um das Problem zu untersuchen. 
  
Um den Erfolg eines Batchprozesses zu überprüfen, überprüfen Sie für EWS das [ResponseClass-Attribut](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) für jedes verarbeitete Element. Es folgt die grundlegende Struktur von **ResponseMessageType**, dem Basistyp, von dem alle Antwortnachrichten abgeleitet werden. 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

The **ResponseClass** attribute is set to **Success** if the contact was processed successfully, or **Error** if the contact was not processed successfully. Bei Kontakten tritt während der Batchverarbeitung keine **Warnung auf.** Wenn **responseClass** **erfolgreich** ist, wird das folgende [ResponseCode -Element](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) auch immer auf **NoError** festgelegt. Wenn **responseClass** **error** ist, müssen Sie die Werte der [Elemente MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode** und [MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) überprüfen, um zu ermitteln, was das Problem verursacht hat. [DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) wird derzeit nicht verwendet. 
  
## <a name="see-also"></a>Siehe auch


- [Personen und Kontakte in EWS in Exchange](people-and-contacts-in-ews-in-exchange.md)
    
- [Verarbeiten von E-Mails in Batches mithilfe von EWS in Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
- [Verarbeiten von Kalenderelementen in Batches in Exchange](how-to-process-calendar-items-in-batches-in-exchange.md)
    

