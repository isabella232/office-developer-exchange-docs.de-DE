---
title: Persistente Anwendungseinstellungen mithilfe von EWS in Exchange verwalten
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 90f561f2-e40e-4f5b-b321-f86dbf4a1b71
description: Erfahren Sie, wie Sie persistente Anwendungseinstellungen mithilfe der verwalteten EWS-API oder EWS in Exchange erstellen, suchen, abrufen, aktualisieren und löschen.
ms.openlocfilehash: 0756f8dabe5f0b898619102b8565b65a536791b9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522278"
---
# <a name="manage-persistent-application-settings-by-using-ews-in-exchange"></a>Persistente Anwendungseinstellungen mithilfe von EWS in Exchange verwalten

Erfahren Sie, wie Sie persistente Anwendungseinstellungen mithilfe der verwalteten EWS-API oder EWS in Exchange erstellen, suchen, abrufen, aktualisieren und löschen. 
  
Benutzerkonfigurationsobjekte sind die beste Option zum Speichern von Konfigurationseinstellungen für Ihre Exchange Clientanwendung, in erster Linie, weil sie in den meisten Clientanwendungen vor Suchergebnissen verborgen sind. Clientanwendungen blenden diese Einstellungen in der Regel aus, da der Endbenutzer sie nicht sehen muss und der Benutzer nicht versehentlich auf diese Informationen zugreift. Die Codebeispiele in diesem Artikel zeigen, wie Sie mithilfe von Benutzerkonfigurationsobjekten persistente Einstellungen verwalten können, einschließlich des Erstellens, Suchens, Abrufens, Aktualisierens und Löschens persistenter Anwendungseinstellungen, die in Benutzerkonfigurationsobjekten gespeichert sind.

<a name="createconfiguration"> </a>

## <a name="create-an-application-setting-by-using-the-ews-managed-api"></a>Erstellen einer Anwendungseinstellung mithilfe der verwalteten EWS-API

Sie können die verwaltete EWS-API-Methode [UserConfiguration.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) verwenden, um eine benutzerdefinierte Konfigurationseinstellung zu erstellen. Ein Benutzerkonfigurationsobjekt kann XML, binär, ein Datenwörterbuch oder eine Kombination dieser drei Datentypen enthalten. Das folgende Beispiel zeigt, wie Sie mithilfe der verwalteten EWS-API ein Benutzerkonfigurationsobjekt namens "ContosoDraftSettings" speichern, das Binärdaten in Ihrem Ordner "Entwürfe" enthält. Dies kann hilfreich sein, wenn Sie Konfigurationsinformationen darüber speichern möchten, wie Entwurfselemente in Ihrer Clientanwendung angezeigt werden. 
  
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

## <a name="create-an-application-setting-by-using-ews"></a>Erstellen einer Anwendungseinstellung mithilfe von EWS
<a name="bk_createEWS"> </a>

Sie können den EWS-Vorgang ["CreateUserConfiguration"](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) verwenden, um eine benutzerdefinierte Konfigurationseinstellung zu erstellen. Das folgende Beispiel zeigt den Anforderungs-XML-Code zum Erstellen eines Benutzerkonfigurationsobjekts namens ContosoDraftSettings. Die Anforderung versucht, einen binären Datenstrom in einem Benutzerkonfigurationsobjekt im Ordner "Entwürfe" zu speichern. Dies ist derselbe XML-Code, der vom Beispiel der verwalteten EWS-API generiert wird. 
  
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

Der [Antwort-XML-Code](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) ist einfach und gibt an, ob die Erstellungsanforderung erfolgreich war oder ob ein Fehler aufgetreten ist. 
  
## <a name="find-an-application-setting-by-using-the-ews-managed-api"></a>Suchen einer Anwendungseinstellung mithilfe der verwalteten EWS-API
<a name="findconfiguration"> </a>

Sie können die verwaltete EWS-API-Methode [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) mit der zugeordneten Traversierungsoption verwenden, um Benutzerkonfigurationsobjekte zu suchen. Im folgenden Codebeispiel wird gezeigt, wie Sie benutzerkonfigurationsobjekte finden, die mithilfe der verwalteten EWS-API im Ordner "Entwürfe" gespeichert sind. 
  
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

## <a name="find-an-application-setting-by-using-ews"></a>Suchen einer Anwendungseinstellung mithilfe von EWS
<a name="bk_findEWS"> </a>

Sie können den [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS-Vorgang verwenden, um Benutzerkonfigurationsobjekte zu suchen. 
  
Das folgende Beispiel zeigt den Anforderungs-XML-Code zum Suchen von Benutzerkonfigurationsobjekten. Dies ist derselbe XML-Code, der vom Beispiel der verwalteten EWS-API generiert wird.
  
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

Das folgende Beispiel zeigt die erfolgreiche Antwort-XML zum Suchen von Benutzerkonfigurationsobjekten. Dies ist derselbe XML-Code, der vom Beispiel der verwalteten EWS-API verarbeitet wird. Beachten Sie Folgendes in dieser Antwort-XML: 
  
- Der Bezeichner und die Änderungsschlüssel wurden zur besseren Lesbarkeit gekürzt.
    
- Die beiden Benutzerkonfigurationsobjekte werden als Nachrichten zurückgegeben. Dies liegt daran, dass der **FindItem-Vorgang** alle Elemente zurückgibt, die nicht im EWS-Schema als Nachrichtenelemente definiert sind. 
    
- Die [ItemClass-Eigenschaften](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) für die beiden Benutzerkonfigurationsobjekte unterscheiden sich. Das erste Benutzerkonfigurationsobjekt wurde mithilfe von EWS erstellt. Das zweite Objekt wurde von einer anderen API erstellt. 
    
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

## <a name="get-and-update-application-settings-by-using-the-ews-managed-api"></a>Abrufen und Aktualisieren von Anwendungseinstellungen mithilfe der verwalteten EWS-API
<a name="getconfiguration"> </a>

Nachdem Sie ein Benutzerkonfigurationsobjekt gefunden haben, können Sie die verwaltete EWS-API-Methode [UserConfiguration.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) verwenden, um das Konfigurationsobjekt aus dem Postfach abzurufen. Nachdem Sie das Konfigurationsobjekt abgerufen haben, können Sie es mit der [UserConfiguration.Update-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) aktualisieren. Das folgende Beispiel zeigt, wie Sie ein Benutzerkonfigurationsobjekt mithilfe der verwalteten EWS-API abrufen und aktualisieren. 
  
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

## <a name="get-and-update-application-settings-by-using-ews"></a>Abrufen und Aktualisieren von Anwendungseinstellungen mithilfe von EWS
<a name="bk_getEWS"> </a>

Sie können den [GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS-Vorgang verwenden, um das Konfigurationsobjekt aus dem Postfach abzurufen, und [updateUserConfiguration,](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) um das Objekt zu aktualisieren. Das folgende Beispiel zeigt den Anforderungs-XML-Code zum Abrufen eines Benutzerkonfigurationsobjekts mit dem Namen "TestConfig". Die Anforderung gibt an, dass alle Konfigurationen in der Antwort zurückgegeben werden sollen. Dies ist derselbe XML-Code, der vom Beispiel der verwalteten EWS-API generiert wird. 
  
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

Das folgende Beispiel zeigt die erfolgreiche Antwort-XML zum Abrufen von Benutzerkonfigurationsobjekten. Die Antwort enthält ein Datenwörterbuch. Dies ist derselbe XML-Code, der vom Beispiel der verwalteten EWS-API verarbeitet wird. 
  
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

Das folgende Beispiel zeigt die XML-Anforderung zum Aktualisieren eines Benutzerkonfigurationsobjekts. Die Anforderung gibt an, dass alle Konfigurationen in der Antwort zurückgegeben werden sollen. Dies ist derselbe XML-Code, der vom EWS Managed API-Beispiel generiert wird, das die **UserConfiguration.Update-Methode** aufruft. Sie können sehen, dass der Update-XML-Code die vorhandenen Wörterbucheinträge und die zusätzlichen Einträge enthält, die vor der Aktualisierung hinzugefügt wurden. 
  
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

Der [Antwort-XML-Code](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) ist einfach und gibt an, ob die Aktualisierung erfolgreich war oder ob ein Fehler aufgetreten ist. 
  
## <a name="delete-an-application-setting-by-using-the-ews-managed-api"></a>Löschen einer Anwendungseinstellung mithilfe der verwalteten EWS-API
<a name="deleteconfiguration"> </a>

Sie können die verwaltete EWS-API-Methode [UserConfiguration.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) verwenden, um Benutzerkonfigurationsobjekte zu löschen. Das folgende Codebeispiel zeigt, wie Sie das ContosoDraftSettings-Benutzerkonfigurationsobjekt mithilfe der verwalteten EWS-API löschen. 
  
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

## <a name="delete-an-application-setting-by-using-ews"></a>Löschen einer Anwendungseinstellung mithilfe von EWS
<a name="bk_deleteEWS"> </a>

Sie können den EWS-Vorgang ["DeleteUserConfiguration"](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) verwenden, um Benutzerkonfigurationsobjekte zu löschen. 
  
Das folgende Beispiel zeigt den Anforderungs-XML-Code zum Löschen eines Benutzerkonfigurationsobjekts namens ContosoDraftSettings, das auf den Ordner "Entwürfe" angewendet wurde. Dies ist derselbe XML-Code, der vom Beispiel der verwalteten EWS-API generiert wird.
  
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

Der [Antwort-XML-Code](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) ist einfach und gibt an, ob die Löschanforderung erfolgreich war oder ob ein Fehler aufgetreten ist. 
  
## <a name="see-also"></a>Siehe auch

- [Persistent Anwendungseinstellungen in EWS in Exchange](persistent-application-settings-in-ews-in-exchange.md)
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)   
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

