---
title: Verwalten der permanenten Anwendungseinstellungen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90f561f2-e40e-4f5b-b321-f86dbf4a1b71
description: Informationen Sie zum Erstellen, suchen, erhalten möchten, aktualisieren und löschen, indem Sie die EWS Managed API oder EWS in Exchange persistent Anwendungseinstellungen.
ms.openlocfilehash: ab5a9cc927bd0a6c4efacce622cc71db1a9b02a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756928"
---
# <a name="manage-persistent-application-settings-by-using-ews-in-exchange"></a><span data-ttu-id="b03e5-103">Verwalten der permanenten Anwendungseinstellungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="b03e5-103">Manage persistent application settings by using EWS in Exchange</span></span>

<span data-ttu-id="b03e5-104">Informationen Sie zum Erstellen, suchen, erhalten möchten, aktualisieren und löschen, indem Sie die EWS Managed API oder EWS in Exchange persistent Anwendungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="b03e5-104">Learn how to create, find, get, update, and delete persistent application settings by using the EWS Managed API or EWS in Exchange.</span></span> 
  
<span data-ttu-id="b03e5-105">Konfiguration der Benutzerobjekte sind die beste Möglichkeit zum Speichern von Konfigurationseinstellungen für Ihre Exchange-Client-Anwendung in erster Linie, da sie aus den Suchergebnissen in den meisten Clientanwendungen ausgeblendet sind.</span><span class="sxs-lookup"><span data-stu-id="b03e5-105">User configuration objects are the best option for storing configuration settings for your Exchange client application, primarily because they are hidden from search results in most client applications.</span></span> <span data-ttu-id="b03e5-106">Clientanwendungen ausblenden diese Einstellungen in der Regel, da finden sie unter der Endbenutzer müssen nicht und, damit der Benutzer nicht versehentlich auf diese Informationen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b03e5-106">Client applications typically hide these settings because the end user doesn't need to see them, and so that the user doesn't accidentally access this information.</span></span> <span data-ttu-id="b03e5-107">Die Codebeispiele in diesem Artikel zeigen Sie Konfiguration Benutzerobjekte Verwendungsmöglichkeiten persistente Einstellungen sowie zum Erstellen, verwalten finden, abrufen, aktualisieren und Löschen von persistent Anwendungseinstellungen, die in der Konfiguration der Benutzerobjekte gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="b03e5-107">The code examples in this article show you how you can use user configuration objects to manage persistent settings, including how to create, find, get, update, and delete persistent application settings that are stored in user configuration objects.</span></span>

<span data-ttu-id="b03e5-108"><a name="createconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="b03e5-108"></span></span>

## <a name="create-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="b03e5-109">Erstellen von anwendungseinstellung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="b03e5-109">Create an application setting by using the EWS Managed API</span></span>

<span data-ttu-id="b03e5-110">Sie können die [UserConfiguration.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) EWS Managed API-Methode verwenden, zum Erstellen einer benutzerdefinierten Konfiguration-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="b03e5-110">You can use the [UserConfiguration.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) EWS Managed API method to create a custom configuration setting.</span></span> <span data-ttu-id="b03e5-111">Ein Benutzer-Konfigurationsobjekt kann XML-Code enthalten binär, ein Datenwörterbuch oder eine Kombination dieser drei Datentypen.</span><span class="sxs-lookup"><span data-stu-id="b03e5-111">A user configuration object can contain XML, binary, a data dictionary, or a combination of those three data types.</span></span> <span data-ttu-id="b03e5-112">Im folgenden Beispiel wird veranschaulicht, wie ein Benutzer Configuration-Objekt mit dem Namen ContosoDraftSettings, die binäre Daten in dem Ordner Entwürfe enthält, mithilfe der EWS Managed API gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b03e5-112">The following example shows how to save a user configuration object named ContosoDraftSettings that contains binary data to your Drafts folder by using the EWS Managed API.</span></span> <span data-ttu-id="b03e5-113">Dies ist möglicherweise hilfreich, wenn Sie zum Speichern von Konfigurationsinformationen zu wie Entwurfselemente in der Clientanwendung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b03e5-113">This might be useful if you want to store configuration information about how draft items are displayed in your client application.</span></span> 
  
```cs
private static void CreateUserConfiguration(ExchangeService service, byte[] binaryData)
{
    // Create the user configuration object.
    UserConfiguration configDrafts = new UserConfiguration(service);
    // Add user configuration data to the BinaryData property.
    configDrafts.BinaryData = binaryData;
    // Name and save the user configuration object on the Drafts folder.
    // This results in a call to EWS.
    configDrafts.Save("ContosoDraftSettings", WellKnownFolderName.Drafts);
}
```

## <a name="create-an-application-setting-by-using-ews"></a><span data-ttu-id="b03e5-114">Erstellen von anwendungseinstellung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="b03e5-114">Create an application setting by using EWS</span></span>
<span data-ttu-id="b03e5-115"><a name="bk_createEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="b03e5-115"></span></span>

<span data-ttu-id="b03e5-116">Sie können zum Erstellen einer benutzerdefinierten Konfigurationseinstellung [CreateUserConfiguration](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) EWS-Vorgangs verwenden.</span><span class="sxs-lookup"><span data-stu-id="b03e5-116">You can use the [CreateUserConfiguration](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) EWS operation to create a custom configuration setting.</span></span> <span data-ttu-id="b03e5-117">Das folgende Beispiel zeigt die Anforderung XML für das Erstellen einer Benutzer-Konfigurationsobjekt mit dem Namen ContosoDraftSettings.</span><span class="sxs-lookup"><span data-stu-id="b03e5-117">The following example shows the request XML for creating a user configuration object named ContosoDraftSettings.</span></span> <span data-ttu-id="b03e5-118">Die Anforderung versucht, einen binären Datenstrom ein Benutzerobjekt-Konfiguration auf den Ordner "Entwürfe" speichern.</span><span class="sxs-lookup"><span data-stu-id="b03e5-118">The request attempts to save a binary stream to a user configuration object on the Drafts folder.</span></span> <span data-ttu-id="b03e5-119">Dies ist die denselben XML-Code, die von der EWS Managed API-Beispiel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="b03e5-119">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
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
    <m:CreateUserConfiguration>
      <m:UserConfiguration>
        <t:UserConfigurationName Name="ContosoDraftSettings">
          <t:DistinguishedFolderId Id="drafts" />
        </t:UserConfigurationName>
        <t:BinaryData>iVBORw0KGH5UhKquRSzaeAAAAAElFTkSuQmCC</t:BinaryData>
      </m:UserConfiguration>
    </m:CreateUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b03e5-120">Die [Antwort-XML-](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) ist einfach und gibt an, ob die Anforderung erstellen erfolgreich war oder ob ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b03e5-120">The [response XML](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) is simple and indicates whether the create request was successful or whether an error occurred.</span></span> 
  
## <a name="find-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="b03e5-121">Hier finden Sie eine anwendungseinstellung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="b03e5-121">Find an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="b03e5-122"><a name="findconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="b03e5-122"></span></span>

<span data-ttu-id="b03e5-123">Die [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS Managed API-Methode können mit der Option zugeordneten durchqueren Sie um Benutzerobjekte Konfiguration zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b03e5-123">You can use the [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS Managed API method with the associated traversal option to find user configuration objects.</span></span> <span data-ttu-id="b03e5-124">Im folgenden Codebeispiel veranschaulicht das Suchen Benutzerobjekte-Konfiguration mithilfe der EWS Managed API auf Ordner "Entwürfe" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b03e5-124">The following code example shows you how to find user configuration objects stored on the Drafts folder by using the EWS Managed API.</span></span> 
  
```cs
private static void FindAssociated(ExchangeService service)
{
    // This is the ItemClass prefix of user configuration objects that are created by using EWS.
    const string userConfigPrefix = "IPM.Configuration.";
            
    // This is the name of a configuration setting created by using EWS.
    string userConfigName = "TestConfig";
    // Return the first five items. 
    ItemView view = new ItemView(5);
    // Request only the properties that you need. Because all the results will be user configuration 
    // objects, you won't need to request the ItemSchema.IsAssociated property, which identifies 
    // user configuration objects.
    PropertySet props = new PropertySet(BasePropertySet.IdOnly, 
                                        ItemSchema.ItemClass);
    view.PropertySet = props;
            
    // Set the traversal to find user configuration objects. 
    view.Traversal = ItemTraversal.Associated;
    // Send the request to search the Drafts folder for all the user configuration objects 
    // in the folder. You do not have to use a search restriction because you will not return
    // a large number of search results. For this scenario, it is better to sort the results
    // on the client. This method results in a call to EWS.
    FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Drafts, view);
    // Output a list of the item classes for the associated items. 
    foreach (Item item in findResults)
    {
        if (item.ItemClass == userConfigPrefix + userConfigName)
        {
            Console.WriteLine("You found the configuration: " + userConfigPrefix + userConfigName);
        }
    }
}
```

## <a name="find-an-application-setting-by-using-ews"></a><span data-ttu-id="b03e5-125">Hier finden Sie eine anwendungseinstellung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="b03e5-125">Find an application setting by using EWS</span></span>
<span data-ttu-id="b03e5-126"><a name="bk_findEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="b03e5-126"></span></span>

<span data-ttu-id="b03e5-127">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS-Vorgangs können Sie die um Konfiguration Benutzerobjekte zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b03e5-127">You can use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation to find user configuration objects.</span></span> 
  
<span data-ttu-id="b03e5-128">Das folgende Beispiel zeigt die Anforderung XML für die Suche nach Benutzer Konfigurationsobjekte.</span><span class="sxs-lookup"><span data-stu-id="b03e5-128">The following example shows the request XML for finding user configuration objects.</span></span> <span data-ttu-id="b03e5-129">Dies ist die denselben XML-Code, die von der EWS Managed API-Beispiel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="b03e5-129">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
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
    <m:FindItem Traversal="Associated">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ItemClass" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="5" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="drafts" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b03e5-130">Das folgende Beispiel zeigt die erfolgreiche Antwort-XML für die Suche nach Benutzer Konfigurationsobjekte.</span><span class="sxs-lookup"><span data-stu-id="b03e5-130">The following example shows the successful response XML for finding user configuration objects.</span></span> <span data-ttu-id="b03e5-131">Dies ist die denselben XML-Code, der durch das Beispiel EWS Managed API verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b03e5-131">This is the same XML that is processed by the EWS Managed API example.</span></span> <span data-ttu-id="b03e5-132">Beachten Sie Folgendes in der XML-Antwort:</span><span class="sxs-lookup"><span data-stu-id="b03e5-132">Note the following in this response XML:</span></span> 
  
- <span data-ttu-id="b03e5-133">Wir verkürzt die Schlüssel-ID und ein Änderungsprotokoll zur besseren Lesbarkeit wurde.</span><span class="sxs-lookup"><span data-stu-id="b03e5-133">We shortened the identifier and change keys for readability.</span></span>
    
- <span data-ttu-id="b03e5-134">Die beiden Benutzerobjekte Konfiguration werden als Nachrichten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b03e5-134">The two user configuration objects are returned as messages.</span></span> <span data-ttu-id="b03e5-135">Dies ist, da die Operation **FindItem** gibt alle Elemente zurück, die nicht als Nachrichtenelemente in die EWS-Schema definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b03e5-135">This is because the **FindItem** operation returns all items that are not defined in the EWS schema as message items.</span></span> 
    
- <span data-ttu-id="b03e5-136">Die [ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) -Eigenschaften für die beiden Benutzerobjekte Konfiguration unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="b03e5-136">The [ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) properties for the two user configuration objects are different.</span></span> <span data-ttu-id="b03e5-137">Das erste Benutzerobjekt-Konfiguration wurde mithilfe von EWS erstellt.</span><span class="sxs-lookup"><span data-stu-id="b03e5-137">The first user configuration object was created by using EWS.</span></span> <span data-ttu-id="b03e5-138">Das zweite Objekt wurde durch eine andere API erstellt.</span><span class="sxs-lookup"><span data-stu-id="b03e5-138">The second object was created by another API.</span></span> 
    
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="2" 
                        TotalItemsInView="2" 
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkDEY9M6AAA=" ChangeKey="CQAAACYnYF5aFMwP0T" />
                <t:ItemClass>IPM.Configuration.TestConfig</t:ItemClass>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAkADEzOzFAAA=" ChangeKey="CQAAABQAAABAByOw==" />
                <t:ItemClass>IPM.Microsoft.FolderDesign.NamedView</t:ItemClass>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="get-and-update-application-settings-by-using-the-ews-managed-api"></a><span data-ttu-id="b03e5-139">Abrufen und Aktualisieren von Anwendungseinstellungen mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="b03e5-139">Get and update application settings by using the EWS Managed API</span></span>
<span data-ttu-id="b03e5-140"><a name="getconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="b03e5-140"></span></span>

<span data-ttu-id="b03e5-141">Wenn Sie eine Benutzer-Konfigurationsobjekt gefunden haben, können Sie die [UserConfiguration.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) EWS Managed API-Methode zum Abrufen des Configuration-Objekts aus dem Postfach verwenden.</span><span class="sxs-lookup"><span data-stu-id="b03e5-141">After you find a user configuration object, you can use the [UserConfiguration.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) EWS Managed API method to get the configuration object from the mailbox.</span></span> <span data-ttu-id="b03e5-142">Nachdem Sie das Konfigurationsobjekt erhalten möchten, können Sie die [UserConfiguration.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) -Methode verwenden, um zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b03e5-142">After you get the configuration object, you can use the [UserConfiguration.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) method to update it.</span></span> <span data-ttu-id="b03e5-143">Im folgenden Beispiel wird gezeigt, wie zum Abrufen und Aktualisieren einer Benutzer-Konfigurationsobjekt mithilfe der EWS Managed API.</span><span class="sxs-lookup"><span data-stu-id="b03e5-143">The following example shows how to get and update a user configuration object by using the EWS Managed API.</span></span> 
  
```cs
private static void GetAndUpdateUserConfiguration(ExchangeService service)
{
    // Binds to a user configuration object named "TestConfig" in the user's mailbox. 
    // Results in a call to EWS. You can also use the Load method to get the latest
    // server version of the user configuration object.
    UserConfiguration usrConfig = UserConfiguration.Bind(service,
                                                         "TestConfig",
                                                         WellKnownFolderName.Drafts,
                                                         UserConfigurationProperties.All);
            
    // Display the returned configuration object property values.
    if (usrConfig.XmlData != null)
    {
        Console.WriteLine("XmlData: " + Encoding.UTF8.GetString(usrConfig.XmlData));
    }
    if (usrConfig.BinaryData != null)
    {
        Console.WriteLine("BinaryData: " + Encoding.UTF8.GetString(usrConfig.BinaryData));
    }
    if (usrConfig.Dictionary.Count > 0)
    {
        Console.WriteLine("Contains {0} dictionary entries", usrConfig.Dictionary.Count);
    }
    // Add dictionary property values to the local copy of the object.
    usrConfig.Dictionary.Add("Key5", 1);
    // Updates the server version of the user configuration object 
    // if it has changed on the client. Results in a call to EWS.
    if (usrConfig.IsDirty)
    {
        usrConfig.Update();
    }
}
```

## <a name="get-and-update-application-settings-by-using-ews"></a><span data-ttu-id="b03e5-144">Abrufen und Aktualisieren von Anwendungseinstellungen mithilfe von Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="b03e5-144">Get and update application settings by using EWS</span></span>
<span data-ttu-id="b03e5-145"><a name="bk_getEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="b03e5-145"></span></span>

<span data-ttu-id="b03e5-146">[GetUserConfiguration](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS-Vorgangs können Sie das Configuration-Objekt aus dem Postfach und die [UpdateUserConfiguration](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) zum Aktualisieren des Objekts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b03e5-146">You can use the [GetUserConfiguration](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS operation to retrieve the configuration object from the mailbox, and the [UpdateUserConfiguration](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) to update the object.</span></span> <span data-ttu-id="b03e5-147">Das folgende Beispiel zeigt die Anforderung XML zum Abrufen einer Benutzer-Konfigurationsobjekt mit dem Namen TestConfig.</span><span class="sxs-lookup"><span data-stu-id="b03e5-147">The following example shows the request XML for getting a user configuration object named TestConfig.</span></span> <span data-ttu-id="b03e5-148">Die Anforderung besagt, dass alle Konfigurationen in der Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b03e5-148">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="b03e5-149">Dies ist die denselben XML-Code, die von der EWS Managed API-Beispiel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="b03e5-149">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
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
    <m:GetUserConfiguration>
      <m:UserConfigurationName Name="TestConfig">
        <t:DistinguishedFolderId Id="drafts" />
      </m:UserConfigurationName>
      <m:UserConfigurationProperties>All</m:UserConfigurationProperties>
    </m:GetUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b03e5-150">Das folgende Beispiel zeigt die erfolgreiche Antwort XML zum Abrufen eines Benutzers von Konfigurationsobjekten.</span><span class="sxs-lookup"><span data-stu-id="b03e5-150">The following example shows the successful response XML for getting a user configuration objects.</span></span> <span data-ttu-id="b03e5-151">Die Antwort enthält ein Datenwörterbuch.</span><span class="sxs-lookup"><span data-stu-id="b03e5-151">The response contains a data dictionary.</span></span> <span data-ttu-id="b03e5-152">Dies ist die denselben XML-Code, der durch das Beispiel EWS Managed API verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b03e5-152">This is the same XML that is processed by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetUserConfigurationResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetUserConfigurationResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:UserConfiguration>
            <t:UserConfigurationName Name="TestConfig">
              <t:DistinguishedFolderId Id="drafts" />
            </t:UserConfigurationName>
            <t:ItemId Id="AAMkDEY9M6AAA=" ChangeKey="CQAAACYnYF5aFMwP0T" />
            <t:Dictionary>
              <t:DictionaryEntry>
                <t:DictionaryKey>
                  <t:Type>String</t:Type>
                  <t:Value>Key1</t:Value>
                </t:DictionaryKey>
                <t:DictionaryValue>
                  <t:Type>Integer32</t:Type>
                  <t:Value>1</t:Value>
                </t:DictionaryValue>
              </t:DictionaryEntry>
              <t:DictionaryEntry>
                <t:DictionaryKey>
                  <t:Type>String</t:Type>
                  <t:Value>PhoneNumber</t:Value>
                </t:DictionaryKey>
                <t:DictionaryValue>
                  <t:Type>String</t:Type>
                  <t:Value>555-555-1111</t:Value>
                </t:DictionaryValue>
              </t:DictionaryEntry>
            </t:Dictionary>
          </m:UserConfiguration>
        </m:GetUserConfigurationResponseMessage>
      </m:ResponseMessages>
    </m:GetUserConfigurationResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="b03e5-153">Das folgende Beispiel zeigt die Anforderung XML für das Aktualisieren einer Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="b03e5-153">The following example shows the request XML for updating a user configuration object.</span></span> <span data-ttu-id="b03e5-154">Die Anforderung besagt, dass alle Konfigurationen in der Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b03e5-154">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="b03e5-155">Dies ist die denselben XML-Code, die von der EWS Managed API-Beispiel generiert wird, die die **UserConfiguration.Update** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="b03e5-155">This is the same XML that is generated by the EWS Managed API example that calls the **UserConfiguration.Update** method.</span></span> <span data-ttu-id="b03e5-156">Sie können sehen, dass das XML-Update enthält, die vorhandenen Wörterbucheinträge und zusätzliche diejenige, die vor der Aktualisierung hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b03e5-156">You can see that the update XML contains the existing dictionary entries and the additional one that was added before the update.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:UpdateUserConfiguration>
      <m:UserConfiguration>
        <t:UserConfigurationName Name="TestConfig">
          <t:DistinguishedFolderId Id="drafts" />
        </t:UserConfigurationName>
        <t:Dictionary>
          <t:DictionaryEntry>
            <t:DictionaryKey>
              <t:Type>String</t:Type>
              <t:Value>Key1</t:Value>
            </t:DictionaryKey>
            <t:DictionaryValue>
              <t:Type>Integer32</t:Type>
              <t:Value>1</t:Value>
            </t:DictionaryValue>
          </t:DictionaryEntry>
          <t:DictionaryEntry>
            <t:DictionaryKey>
              <t:Type>String</t:Type>
              <t:Value>PhoneNumber</t:Value>
            </t:DictionaryKey>
            <t:DictionaryValue>
              <t:Type>String</t:Type>
              <t:Value>555-555-1111</t:Value>
            </t:DictionaryValue>
          </t:DictionaryEntry>
          <t:DictionaryEntry>
            <t:DictionaryKey>
              <t:Type>String</t:Type>
              <t:Value>Key5</t:Value>
            </t:DictionaryKey>
            <t:DictionaryValue>
              <t:Type>Integer32</t:Type>
              <t:Value>1</t:Value>
            </t:DictionaryValue>
          </t:DictionaryEntry>
        </t:Dictionary>
      </m:UserConfiguration>
    </m:UpdateUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b03e5-157">Die [Antwort-XML-](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) ist einfach und gibt an, ob die Aktualisierung erfolgreich war oder ob ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b03e5-157">The [response XML](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) is simple and indicates whether the update was successful or whether an error occurred.</span></span> 
  
## <a name="delete-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="b03e5-158">Löschen von anwendungseinstellung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="b03e5-158">Delete an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="b03e5-159"><a name="deleteconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="b03e5-159"></span></span>

<span data-ttu-id="b03e5-160">Die [UserConfiguration.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS Managed API-Methode können Sie die Konfiguration Benutzerobjekte löschen.</span><span class="sxs-lookup"><span data-stu-id="b03e5-160">You can use the [UserConfiguration.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS Managed API method to delete user configuration objects.</span></span> <span data-ttu-id="b03e5-161">Das folgende Codebeispiel veranschaulicht das ContosoDraftSettings Benutzer Configuration-Objekt löschen, indem Sie die EWS Managed API.</span><span class="sxs-lookup"><span data-stu-id="b03e5-161">The following code example shows you how to delete the ContosoDraftSettings user configuration object by using the EWS Managed API.</span></span> 
  
```cs
private static void DeleteUserConfiguration(ExchangeService service)
{
    // Binds to a user configuration object. Results in a call to EWS.
    UserConfiguration usrConfig = UserConfiguration.Bind(service,
                                                        "ContosoDraftSettings",
                                                        WellKnownFolderName.Drafts,
                                                        UserConfigurationProperties.Id);
    // Deletes the user configuration object.
    // Results in a call to EWS.
    usrConfig.Delete();
}
```

## <a name="delete-an-application-setting-by-using-ews"></a><span data-ttu-id="b03e5-162">Löschen von anwendungseinstellung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="b03e5-162">Delete an application setting by using EWS</span></span>
<span data-ttu-id="b03e5-163"><a name="bk_deleteEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="b03e5-163"></span></span>

<span data-ttu-id="b03e5-164">[DeleteUserConfiguration](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) EWS-Vorgangs können Sie die Konfiguration der Benutzerobjekte löschen.</span><span class="sxs-lookup"><span data-stu-id="b03e5-164">You can use the [DeleteUserConfiguration](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) EWS operation to delete user configuration objects.</span></span> 
  
<span data-ttu-id="b03e5-165">Das folgende Beispiel zeigt die Anforderung XML zum Löschen einer Benutzer-Konfigurationsobjekt mit dem Namen ContosoDraftSettings, die im Ordner Entwürfe angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b03e5-165">The following example shows the request XML for deleting a user configuration object named ContosoDraftSettings that was applied to the Drafts folder.</span></span> <span data-ttu-id="b03e5-166">Dies ist die denselben XML-Code, die von der EWS Managed API-Beispiel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="b03e5-166">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:DeleteUserConfiguration>
      <m:UserConfigurationName Name="ContosoDraftSettings">
        <t:DistinguishedFolderId Id="drafts" />
      </m:UserConfigurationName>
    </m:DeleteUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b03e5-167">Die [Antwort-XML-](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) ist einfach und gibt an, ob die Delete-Anforderung erfolgreich war oder ob ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b03e5-167">The [response XML](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) is simple and indicates whether the delete request was a success or whether an error occurred.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b03e5-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b03e5-168">See also</span></span>

- [<span data-ttu-id="b03e5-169">Persistent Anwendungseinstellungen in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="b03e5-169">Persistent application settings in EWS in Exchange</span></span>](persistent-application-settings-in-ews-in-exchange.md)
- [<span data-ttu-id="b03e5-170">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="b03e5-170">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)   
- [<span data-ttu-id="b03e5-171">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="b03e5-171">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

