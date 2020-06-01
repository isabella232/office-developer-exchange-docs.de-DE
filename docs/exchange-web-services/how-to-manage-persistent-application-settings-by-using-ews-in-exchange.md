---
title: Persistente Anwendungseinstellungen mithilfe von EWS in Exchange verwalten
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90f561f2-e40e-4f5b-b321-f86dbf4a1b71
description: In diesem Artikel erfahren Sie, wie Sie persistente Anwendungseinstellungen mithilfe der verwaltete EWS-API oder EWS in Exchange erstellen, suchen, abrufen, aktualisieren und löschen können.
ms.openlocfilehash: ab7b3ef5f87d8a26a412ca7187dc93c58d73112f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455730"
---
# <a name="manage-persistent-application-settings-by-using-ews-in-exchange"></a><span data-ttu-id="5803e-103">Persistente Anwendungseinstellungen mithilfe von EWS in Exchange verwalten</span><span class="sxs-lookup"><span data-stu-id="5803e-103">Manage persistent application settings by using EWS in Exchange</span></span>

<span data-ttu-id="5803e-104">In diesem Artikel erfahren Sie, wie Sie persistente Anwendungseinstellungen mithilfe der verwaltete EWS-API oder EWS in Exchange erstellen, suchen, abrufen, aktualisieren und löschen können.</span><span class="sxs-lookup"><span data-stu-id="5803e-104">Learn how to create, find, get, update, and delete persistent application settings by using the EWS Managed API or EWS in Exchange.</span></span> 
  
<span data-ttu-id="5803e-105">Benutzer Konfigurationsobjekte sind die beste Option zum Speichern von Konfigurationseinstellungen für Ihre Exchange-Clientanwendung, vor allem, weil Sie in den meisten Clientanwendungen in Suchergebnissen verborgen sind.</span><span class="sxs-lookup"><span data-stu-id="5803e-105">User configuration objects are the best option for storing configuration settings for your Exchange client application, primarily because they are hidden from search results in most client applications.</span></span> <span data-ttu-id="5803e-106">Client Anwendungen blenden diese Einstellungen in der Regel aus, da Sie vom Endbenutzer nicht angezeigt werden müssen und der Benutzer nicht versehentlich auf diese Informationen zugreift.</span><span class="sxs-lookup"><span data-stu-id="5803e-106">Client applications typically hide these settings because the end user doesn't need to see them, and so that the user doesn't accidentally access this information.</span></span> <span data-ttu-id="5803e-107">In den Codebeispielen in diesem Artikel erfahren Sie, wie Sie Benutzer Konfigurationsobjekte zum Verwalten beständiger Einstellungen verwenden können, einschließlich der Vorgehensweise zum Erstellen, suchen, abrufen, aktualisieren und Löschen von Einstellungen für beständige Anwendungen, die in Benutzer Konfigurationsobjekten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="5803e-107">The code examples in this article show you how you can use user configuration objects to manage persistent settings, including how to create, find, get, update, and delete persistent application settings that are stored in user configuration objects.</span></span>

<span data-ttu-id="5803e-108"><a name="createconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="5803e-108"><a name="createconfiguration"> </a></span></span>

## <a name="create-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="5803e-109">Erstellen einer Anwendungseinstellung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="5803e-109">Create an application setting by using the EWS Managed API</span></span>

<span data-ttu-id="5803e-110">Sie können die [UserConfiguration. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode verwenden, um eine benutzerdefinierte Konfigurationseinstellung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5803e-110">You can use the [UserConfiguration.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) EWS Managed API method to create a custom configuration setting.</span></span> <span data-ttu-id="5803e-111">Ein Benutzer Konfigurationsobjekt kann XML, binär, ein Datenwörterbuch oder eine Kombination dieser drei Datentypen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5803e-111">A user configuration object can contain XML, binary, a data dictionary, or a combination of those three data types.</span></span> <span data-ttu-id="5803e-112">Im folgenden Beispiel wird gezeigt, wie Sie ein Benutzer Konfigurationsobjekt mit dem Namen ContosoDraftSettings speichern, das Binärdaten im Ordner Entwürfe mithilfe der verwaltete EWS-API enthält.</span><span class="sxs-lookup"><span data-stu-id="5803e-112">The following example shows how to save a user configuration object named ContosoDraftSettings that contains binary data to your Drafts folder by using the EWS Managed API.</span></span> <span data-ttu-id="5803e-113">Dies kann hilfreich sein, wenn Sie Konfigurationsinformationen zur Anzeige von Entwurfselementen in Ihrer Clientanwendung speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="5803e-113">This might be useful if you want to store configuration information about how draft items are displayed in your client application.</span></span> 
  
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

## <a name="create-an-application-setting-by-using-ews"></a><span data-ttu-id="5803e-114">Erstellen einer Anwendungseinstellung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="5803e-114">Create an application setting by using EWS</span></span>
<span data-ttu-id="5803e-115"><a name="bk_createEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="5803e-115"><a name="bk_createEWS"> </a></span></span>

<span data-ttu-id="5803e-116">Sie können den [CreateUserConfiguration](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) -EWS-Vorgang verwenden, um eine benutzerdefinierte Konfigurationseinstellung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5803e-116">You can use the [CreateUserConfiguration](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) EWS operation to create a custom configuration setting.</span></span> <span data-ttu-id="5803e-117">Das folgende Beispiel zeigt den Anforderungs-XML-Code zum Erstellen eines Benutzer Konfigurationsobjekts namens ContosoDraftSettings.</span><span class="sxs-lookup"><span data-stu-id="5803e-117">The following example shows the request XML for creating a user configuration object named ContosoDraftSettings.</span></span> <span data-ttu-id="5803e-118">Die Anforderung versucht, einen binären Datenstrom in einem Benutzer Konfigurationsobjekt im Ordner "Entwürfe" zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5803e-118">The request attempts to save a binary stream to a user configuration object on the Drafts folder.</span></span> <span data-ttu-id="5803e-119">Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="5803e-119">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="5803e-120">Der [Antwort-XML-Code](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) ist einfach und gibt an, ob die CREATE-Anforderung erfolgreich war oder ob ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5803e-120">The [response XML](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) is simple and indicates whether the create request was successful or whether an error occurred.</span></span> 
  
## <a name="find-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="5803e-121">Suchen einer Anwendungseinstellung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="5803e-121">Find an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="5803e-122"><a name="findconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="5803e-122"><a name="findconfiguration"> </a></span></span>

<span data-ttu-id="5803e-123">Sie können die [Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode mit der zugeordneten Traversal-Option verwenden, um Benutzer Konfigurationsobjekte zu finden.</span><span class="sxs-lookup"><span data-stu-id="5803e-123">You can use the [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS Managed API method with the associated traversal option to find user configuration objects.</span></span> <span data-ttu-id="5803e-124">Im folgenden Codebeispiel wird veranschaulicht, wie Sie mithilfe der verwaltete EWS-API im Ordner Entwürfe gespeicherte Benutzer Konfigurationsobjekte finden.</span><span class="sxs-lookup"><span data-stu-id="5803e-124">The following code example shows you how to find user configuration objects stored on the Drafts folder by using the EWS Managed API.</span></span> 
  
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

## <a name="find-an-application-setting-by-using-ews"></a><span data-ttu-id="5803e-125">Suchen einer Anwendungseinstellung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="5803e-125">Find an application setting by using EWS</span></span>
<span data-ttu-id="5803e-126"><a name="bk_findEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="5803e-126"><a name="bk_findEWS"> </a></span></span>

<span data-ttu-id="5803e-127">Sie können den [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -EWS-Vorgang verwenden, um Benutzer Konfigurationsobjekte zu finden.</span><span class="sxs-lookup"><span data-stu-id="5803e-127">You can use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation to find user configuration objects.</span></span> 
  
<span data-ttu-id="5803e-128">Im folgenden Beispiel wird die Anforderungs-XML für die Suche nach Benutzer Konfigurationsobjekten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5803e-128">The following example shows the request XML for finding user configuration objects.</span></span> <span data-ttu-id="5803e-129">Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="5803e-129">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="5803e-130">Das folgende Beispiel zeigt die erfolgreiche Antwort-XML für die Suche nach Benutzer Konfigurationsobjekten.</span><span class="sxs-lookup"><span data-stu-id="5803e-130">The following example shows the successful response XML for finding user configuration objects.</span></span> <span data-ttu-id="5803e-131">Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5803e-131">This is the same XML that is processed by the EWS Managed API example.</span></span> <span data-ttu-id="5803e-132">Beachten Sie Folgendes in dieser Antwort XML:</span><span class="sxs-lookup"><span data-stu-id="5803e-132">Note the following in this response XML:</span></span> 
  
- <span data-ttu-id="5803e-133">Wir haben den Bezeichner und die Änderungsschlüssel zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="5803e-133">We shortened the identifier and change keys for readability.</span></span>
    
- <span data-ttu-id="5803e-134">Die beiden Benutzer Konfigurationsobjekte werden als Nachrichten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5803e-134">The two user configuration objects are returned as messages.</span></span> <span data-ttu-id="5803e-135">Dies liegt daran, dass der **FindItem** -Vorgang alle Elemente zurückgibt, die nicht im EWS-Schema als Nachrichtenelemente definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5803e-135">This is because the **FindItem** operation returns all items that are not defined in the EWS schema as message items.</span></span> 
    
- <span data-ttu-id="5803e-136">Die [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) -Eigenschaften für die beiden Benutzer Konfigurationsobjekte sind unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="5803e-136">The [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) properties for the two user configuration objects are different.</span></span> <span data-ttu-id="5803e-137">Das erste Benutzer Konfigurationsobjekt wurde mithilfe von EWS erstellt.</span><span class="sxs-lookup"><span data-stu-id="5803e-137">The first user configuration object was created by using EWS.</span></span> <span data-ttu-id="5803e-138">Das zweite Objekt wurde von einer anderen API erstellt.</span><span class="sxs-lookup"><span data-stu-id="5803e-138">The second object was created by another API.</span></span> 
    
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="get-and-update-application-settings-by-using-the-ews-managed-api"></a><span data-ttu-id="5803e-139">Abrufen und Aktualisieren von Anwendungseinstellungen mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="5803e-139">Get and update application settings by using the EWS Managed API</span></span>
<span data-ttu-id="5803e-140"><a name="getconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="5803e-140"><a name="getconfiguration"> </a></span></span>

<span data-ttu-id="5803e-141">Nachdem Sie ein Benutzer Konfigurationsobjekt gefunden haben, können Sie die [UserConfiguration. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode verwenden, um das Configuration-Objekt aus dem Postfach abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5803e-141">After you find a user configuration object, you can use the [UserConfiguration.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) EWS Managed API method to get the configuration object from the mailbox.</span></span> <span data-ttu-id="5803e-142">Nachdem Sie das Configuration-Objekt abgerufen haben, können Sie es mithilfe der [UserConfiguration. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) -Methode aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5803e-142">After you get the configuration object, you can use the [UserConfiguration.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) method to update it.</span></span> <span data-ttu-id="5803e-143">Im folgenden Beispiel wird gezeigt, wie ein Benutzer Konfigurationsobjekt mithilfe der verwaltete EWS-API abgerufen und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="5803e-143">The following example shows how to get and update a user configuration object by using the EWS Managed API.</span></span> 
  
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

## <a name="get-and-update-application-settings-by-using-ews"></a><span data-ttu-id="5803e-144">Abrufen und Aktualisieren von Anwendungseinstellungen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="5803e-144">Get and update application settings by using EWS</span></span>
<span data-ttu-id="5803e-145"><a name="bk_getEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="5803e-145"><a name="bk_getEWS"> </a></span></span>

<span data-ttu-id="5803e-146">Sie können den [GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) -EWS-Vorgang verwenden, um das Configuration-Objekt aus dem Postfach abzurufen, und die [UpdateUserConfiguration](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) , um das Objekt zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5803e-146">You can use the [GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS operation to retrieve the configuration object from the mailbox, and the [UpdateUserConfiguration](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) to update the object.</span></span> <span data-ttu-id="5803e-147">Das folgende Beispiel zeigt die Anforderungs-XML für das erhalten eines Benutzer Konfigurationsobjekts namens TestConfig.</span><span class="sxs-lookup"><span data-stu-id="5803e-147">The following example shows the request XML for getting a user configuration object named TestConfig.</span></span> <span data-ttu-id="5803e-148">Die Anforderung besagt, dass alle Konfigurationen in der Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5803e-148">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="5803e-149">Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="5803e-149">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="5803e-150">Im folgenden Beispiel wird die erfolgreiche Antwort-XML für das Aufrufen von Benutzer Konfigurationsobjekten veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5803e-150">The following example shows the successful response XML for getting a user configuration objects.</span></span> <span data-ttu-id="5803e-151">Die Antwort enthält ein Datenwörterbuch.</span><span class="sxs-lookup"><span data-stu-id="5803e-151">The response contains a data dictionary.</span></span> <span data-ttu-id="5803e-152">Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5803e-152">This is the same XML that is processed by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetUserConfigurationResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="5803e-153">Im folgenden Beispiel wird die Anforderungs-XML zum Aktualisieren eines Benutzer Konfigurationsobjekts dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5803e-153">The following example shows the request XML for updating a user configuration object.</span></span> <span data-ttu-id="5803e-154">Die Anforderung besagt, dass alle Konfigurationen in der Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5803e-154">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="5803e-155">Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel generiert wird, das die **UserConfiguration. Update** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="5803e-155">This is the same XML that is generated by the EWS Managed API example that calls the **UserConfiguration.Update** method.</span></span> <span data-ttu-id="5803e-156">Sie können sehen, dass die Update-XML-Datei die vorhandenen Wörterbucheinträge enthält und die zusätzliche, die vor der Aktualisierung hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="5803e-156">You can see that the update XML contains the existing dictionary entries and the additional one that was added before the update.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="5803e-157">Der [Antwort-XML-Code](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) ist einfach und gibt an, ob das Update erfolgreich war oder ob ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5803e-157">The [response XML](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) is simple and indicates whether the update was successful or whether an error occurred.</span></span> 
  
## <a name="delete-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="5803e-158">Löschen einer Anwendungseinstellung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="5803e-158">Delete an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="5803e-159"><a name="deleteconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="5803e-159"><a name="deleteconfiguration"> </a></span></span>

<span data-ttu-id="5803e-160">Sie können die [UserConfiguration. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode verwenden, um Benutzer Konfigurationsobjekte zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5803e-160">You can use the [UserConfiguration.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS Managed API method to delete user configuration objects.</span></span> <span data-ttu-id="5803e-161">Im folgenden Codebeispiel wird veranschaulicht, wie Sie das ContosoDraftSettings-Benutzer Konfigurationsobjekt mithilfe der verwaltete EWS-API löschen.</span><span class="sxs-lookup"><span data-stu-id="5803e-161">The following code example shows you how to delete the ContosoDraftSettings user configuration object by using the EWS Managed API.</span></span> 
  
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

## <a name="delete-an-application-setting-by-using-ews"></a><span data-ttu-id="5803e-162">Löschen einer Anwendungseinstellung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="5803e-162">Delete an application setting by using EWS</span></span>
<span data-ttu-id="5803e-163"><a name="bk_deleteEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="5803e-163"><a name="bk_deleteEWS"> </a></span></span>

<span data-ttu-id="5803e-164">Sie können den [DeleteUserConfiguration](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) -EWS-Vorgang verwenden, um Benutzer Konfigurationsobjekte zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5803e-164">You can use the [DeleteUserConfiguration](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) EWS operation to delete user configuration objects.</span></span> 
  
<span data-ttu-id="5803e-165">Das folgende Beispiel zeigt den Anforderungs-XML-Code zum Löschen eines Benutzer Konfigurationsobjekts namens ContosoDraftSettings, das auf den Ordner Entwürfe angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5803e-165">The following example shows the request XML for deleting a user configuration object named ContosoDraftSettings that was applied to the Drafts folder.</span></span> <span data-ttu-id="5803e-166">Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="5803e-166">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="5803e-167">Der [Antwort-XML-Code](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) ist einfach und gibt an, ob die DELETE-Anforderung erfolgreich war oder ob ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5803e-167">The [response XML](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) is simple and indicates whether the delete request was a success or whether an error occurred.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5803e-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5803e-168">See also</span></span>

- [<span data-ttu-id="5803e-169">Persistent Anwendungseinstellungen in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="5803e-169">Persistent application settings in EWS in Exchange</span></span>](persistent-application-settings-in-ews-in-exchange.md)
- [<span data-ttu-id="5803e-170">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="5803e-170">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)   
- [<span data-ttu-id="5803e-171">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="5803e-171">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

