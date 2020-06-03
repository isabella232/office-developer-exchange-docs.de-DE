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
# <a name="process-contacts-in-batches-by-using-ews-in-exchange"></a>Verarbeiten von Kontakten in Batches mithilfe von EWS in Exchange

In diesem Artikel erfahren Sie, wie Sie in einem einzigen Aufruf Batches von Kontakten erstellen, abrufen, aktualisieren und löschen, indem Sie das verwaltete EWS-API oder EWS in Exchange verwenden.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um mit Batches von Kontakten zu arbeiten, um die Anzahl der Anrufe zu reduzieren, die ein Client an einen Exchange-Server macht. Wenn Sie die verwaltete EWS-API verwenden, um Kontakte in Batches zu erstellen, abzurufen, zu aktualisieren und zu löschen, verwenden Sie [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objektmethoden, während Sie bei der Arbeit mit einzelnen Kontakten [Kontakt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) Objektmethoden verwenden. Wenn Sie EWS verwenden, verwenden Sie dieselben Vorgänge, um sowohl mit einem einzelnen Kontakt als auch mit Batches von Kontakten zu arbeiten. 
  
**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge zum Arbeiten mit Batches von Kontakten**

|**Gewünschte Aktion**|**Verwenden Sie diese verwaltete EWS-API-Methode**|**Zu verwendender EWS-Vorgang**|
|:-----|:-----|:-----|
|Erstellen von Kontakten in Batches  <br/> |[Datei "ExchangeService. CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Abrufen von Kontakten in Batches  <br/> |[Datei "ExchangeService. BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) oder [Datei" ExchangeService. LoadPropertiesForItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|Aktualisieren von Kontakten in Batches  <br/> |[Datei "ExchangeService. Update Items](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen von Kontakten in Batches  <br/> |[Datei "ExchangeService. DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
In diesem Artikel erfahren Sie, wie Sie grundlegende Aufgaben für Batches von Kontakten mithilfe der verwaltete EWS-API oder EWS ausführen.
  
## <a name="create-contacts-in-batches-by-using-the-ews-managed-api"></a>Erstellen von Kontakten in Batches mithilfe der verwaltete EWS-API
<a name="bk_EWSMA"> </a>

Sie können Kontakte in Batches erstellen, indem Sie die verwaltete EWS-API [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) -Methode verwenden, wie im folgenden Beispiel gezeigt. In diesem Beispiel werden drei [Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) -Objekte lokal erstellt, jeder Kontakt wird einer Auflistung hinzugefügt, und anschließend wird die **CreateItems** -Methode für die Auflistung der Kontakte aufgerufen. 
  
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

Sie können Kontakte in Batches erstellen, indem Sie den [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -EWS-Vorgang verwenden, wie im folgenden Codebeispiel dargestellt. Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API verwenden, um [Kontakte in Batches zu erstellen](#bk_EWSMA).
  
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

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die einen [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert von **noError** für jeden der neuen Kontakte enthält, der angibt, dass jeder Kontakt erfolgreich erstellt und gespeichert wurde. 
  
## <a name="get-contacts-in-batches-by-using-the-ews-managed-api"></a>Abrufen von Kontakten in Batches mithilfe der verwaltete EWS-API
<a name="bk_EWSMAGet"> </a>

Sie können Kontakte in Batches abrufen, indem Sie die verwaltete EWS-API [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) -Methode verwenden, wie im folgenden Beispiel gezeigt. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde. 
  
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

Sie können Kontakte in Batches mit dem [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -EWS-Vorgang und dem Code im folgenden Beispiel abrufen. Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API zum [Abrufen von Kontakten in Batches](#bk_EWSMAGet)verwenden. Das **ItemID** -Attribut wurde zur Lesbarkeit gekürzt. 
  
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

Der Server antwortet auf die **GetItem** -Anforderung mit einer [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) -Nachricht, die die ID und den Anzeigenamen für jeden der angeforderten Kontakte enthält. 
  
## <a name="update-contacts-in-batches-by-using-the-ews-managed-api"></a>Aktualisieren von Kontakten in Batches mithilfe der verwaltete EWS-API
<a name="bk_EWSMAUpdate"> </a>

Sie können Kontakte in Batches aktualisieren, indem Sie die verwaltete EWS-API [Update Items](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) -Methode verwenden, wie im folgenden Beispiel gezeigt. Im vorherigen Beispiel wird der Kontakt erstellt, aber nicht angegeben, für wen er verwendet wird. Sie können den Code in diesem Beispiel verwenden, um alle Ihre Kontakte gleichzeitig zu aktualisieren, um den Namen Ihres Unternehmens einzubeziehen. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde. 
  
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

Sie können Kontakte in Batches aktualisieren, indem Sie den [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -EWS-Vorgang verwenden, wie im folgenden Codebeispiel dargestellt. Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie den verwaltete EWS-API verwenden, um [Kontakte in Batches zu aktualisieren](#bk_EWSMAUpdate). Das **ItemID** -Attribut wurde zur Lesbarkeit gekürzt. 
  
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

Der Server antwortet auf die **UpdateItem** -Anforderung mit einer [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert **noError**enthält, der angibt, dass jedes Update erfolgreich auf dem Server gespeichert wurde. Alle Konflikte werden im [ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) -Element gemeldet. 
  
## <a name="delete-contacts-in-batches-by-using-the-ews-managed-api"></a>Löschen von Kontakten in Batches mithilfe der verwaltete EWS-API
<a name="bk_EWSMADelete"> </a>

Sie können Kontakte in Batches löschen, indem Sie die [DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode verwenden, wie im folgenden Beispiel gezeigt. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde. 
  
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

Sie können Kontakte in Batches löschen, indem Sie den EWS-Vorgang [DeleteItem](../web-service-reference/deleteitem-operation.md) verwenden, wie im folgenden Codebeispiel dargestellt. Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API verwenden, um [Kontakte in Batches zu löschen](#bk_EWSMADelete). Das **ItemID** -Attribut wurde zur Lesbarkeit gekürzt. 
  
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

Der Server antwortet auf die **DeleteItem** -Anforderung mit einer [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert **noError** für jedes entfernte Element enthält. Beachten Sie, dass der Vorgang auch dann Success zurückgegeben wird, wenn die Element-ID nicht gefunden werden konnte. 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a>Überprüfen, ob ein Batchprozess erfolgreich abgeschlossen wurde
<a name="bk_successful"> </a>

Wenn ein oder mehrere Kontakte in einer Batchanforderung nicht wie angefordert verarbeitet werden können, wird für jeden Kontakt, der fehlgeschlagen ist, ein Fehler zurückgegeben, und die restlichen Kontakte im Batch werden wie erwartet verarbeitet. Fehler in der Batchverarbeitung können auftreten, wenn das Element gelöscht wurde und daher nicht abgerufen oder aktualisiert werden kann oder wenn das Element in einen anderen Ordner verschoben wurde und daher über eine neue Element-ID verfügt und nicht mit der gesendeten Element-ID geändert werden kann. Die Informationen in diesem Abschnitt zeigen, wie Fehlerdetails zu Fehlern bei der Batchverarbeitung von Kontakten abgerufen werden.
  
Um den Erfolg eines Batchprozesses mithilfe der verwaltete EWS-API zu überprüfen, können Sie überprüfen, ob die [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) -Eigenschaft des [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) gleich [ServiceResult. Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)ist. Wenn dies der Fall ist, wurden alle Kontakte erfolgreich verarbeitet. Wenn **OverallResult** nicht gleich **ServiceResult. Success**ist, wurden mindestens einer der Kontakte nicht erfolgreich verarbeitet. Jedes der Objekte, die in der **ServiceResponseCollection** zurückgegeben werden, enthält die folgenden Eigenschaften: 
  
- [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [Ergebnis](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
Diese Eigenschaften enthalten Informationen dazu, warum die Kontakte nicht wie angefordert verarbeitet werden konnten. In den Beispielen in diesem Artikel werden das **Ergebnis**, **errorCode**und **ErrorMessage** für jeden fehlerhaften Kontakt gedruckt. Sie können diese Ergebnisse verwenden, um das Problem zu untersuchen. 
  
Überprüfen Sie für EWS das [ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) -Attribut für jedes verarbeitete Element, um den Erfolg eines Batchprozesses zu überprüfen. Im folgenden finden Sie die grundlegende Struktur des **ResponseMessageType**, den Basistyp, von dem alle Antwortnachrichten abgeleitet werden. 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

Das **ResponseClass** -Attribut **ist auf "erfolgreich"** festgelegt, wenn der Kontakt erfolgreich verarbeitet wurde, oder **Fehler** , wenn der Kontakt nicht erfolgreich verarbeitet wurde. Bei Kontakten wird während der Batchverarbeitung keine **Warnung angezeigt** . Wenn der **ResponseClass** **erfolgreich**ist, wird das [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element, das folgt, auch immer auf **noError**festgelegt. Wenn das **ResponseClass** -Element **fehlerhaft**ist, müssen Sie die Werte der [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)-, **Response Code**-und [messagexml verwendet](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) -Elemente überprüfen, um zu ermitteln, was das Problem verursacht hat. [DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) wird derzeit nicht verwendet. 
  
## <a name="see-also"></a>Siehe auch


- [Personen und Kontakte in EWS in Exchange](people-and-contacts-in-ews-in-exchange.md)
    
- [Verarbeiten von E-Mails in Batches mithilfe von EWS in Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
- [Verarbeiten von Kalenderelementen in Batches in Exchange](how-to-process-calendar-items-in-batches-in-exchange.md)
    

