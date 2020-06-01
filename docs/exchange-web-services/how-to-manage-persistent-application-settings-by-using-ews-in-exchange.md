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
# <a name="manage-persistent-application-settings-by-using-ews-in-exchange"></a>Persistente Anwendungseinstellungen mithilfe von EWS in Exchange verwalten

In diesem Artikel erfahren Sie, wie Sie persistente Anwendungseinstellungen mithilfe der verwaltete EWS-API oder EWS in Exchange erstellen, suchen, abrufen, aktualisieren und löschen können. 
  
Benutzer Konfigurationsobjekte sind die beste Option zum Speichern von Konfigurationseinstellungen für Ihre Exchange-Clientanwendung, vor allem, weil Sie in den meisten Clientanwendungen in Suchergebnissen verborgen sind. Client Anwendungen blenden diese Einstellungen in der Regel aus, da Sie vom Endbenutzer nicht angezeigt werden müssen und der Benutzer nicht versehentlich auf diese Informationen zugreift. In den Codebeispielen in diesem Artikel erfahren Sie, wie Sie Benutzer Konfigurationsobjekte zum Verwalten beständiger Einstellungen verwenden können, einschließlich der Vorgehensweise zum Erstellen, suchen, abrufen, aktualisieren und Löschen von Einstellungen für beständige Anwendungen, die in Benutzer Konfigurationsobjekten gespeichert sind.

<a name="createconfiguration"> </a>

## <a name="create-an-application-setting-by-using-the-ews-managed-api"></a>Erstellen einer Anwendungseinstellung mithilfe der verwaltete EWS-API

Sie können die [UserConfiguration. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode verwenden, um eine benutzerdefinierte Konfigurationseinstellung zu erstellen. Ein Benutzer Konfigurationsobjekt kann XML, binär, ein Datenwörterbuch oder eine Kombination dieser drei Datentypen enthalten. Im folgenden Beispiel wird gezeigt, wie Sie ein Benutzer Konfigurationsobjekt mit dem Namen ContosoDraftSettings speichern, das Binärdaten im Ordner Entwürfe mithilfe der verwaltete EWS-API enthält. Dies kann hilfreich sein, wenn Sie Konfigurationsinformationen zur Anzeige von Entwurfselementen in Ihrer Clientanwendung speichern möchten. 
  
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

Sie können den [CreateUserConfiguration](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) -EWS-Vorgang verwenden, um eine benutzerdefinierte Konfigurationseinstellung zu erstellen. Das folgende Beispiel zeigt den Anforderungs-XML-Code zum Erstellen eines Benutzer Konfigurationsobjekts namens ContosoDraftSettings. Die Anforderung versucht, einen binären Datenstrom in einem Benutzer Konfigurationsobjekt im Ordner "Entwürfe" zu speichern. Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel generiert wird. 
  
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

Der [Antwort-XML-Code](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) ist einfach und gibt an, ob die CREATE-Anforderung erfolgreich war oder ob ein Fehler aufgetreten ist. 
  
## <a name="find-an-application-setting-by-using-the-ews-managed-api"></a>Suchen einer Anwendungseinstellung mithilfe der verwaltete EWS-API
<a name="findconfiguration"> </a>

Sie können die [Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode mit der zugeordneten Traversal-Option verwenden, um Benutzer Konfigurationsobjekte zu finden. Im folgenden Codebeispiel wird veranschaulicht, wie Sie mithilfe der verwaltete EWS-API im Ordner Entwürfe gespeicherte Benutzer Konfigurationsobjekte finden. 
  
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

Sie können den [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -EWS-Vorgang verwenden, um Benutzer Konfigurationsobjekte zu finden. 
  
Im folgenden Beispiel wird die Anforderungs-XML für die Suche nach Benutzer Konfigurationsobjekten dargestellt. Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel generiert wird.
  
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

Das folgende Beispiel zeigt die erfolgreiche Antwort-XML für die Suche nach Benutzer Konfigurationsobjekten. Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel verarbeitet wird. Beachten Sie Folgendes in dieser Antwort XML: 
  
- Wir haben den Bezeichner und die Änderungsschlüssel zur Lesbarkeit gekürzt.
    
- Die beiden Benutzer Konfigurationsobjekte werden als Nachrichten zurückgegeben. Dies liegt daran, dass der **FindItem** -Vorgang alle Elemente zurückgibt, die nicht im EWS-Schema als Nachrichtenelemente definiert sind. 
    
- Die [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) -Eigenschaften für die beiden Benutzer Konfigurationsobjekte sind unterschiedlich. Das erste Benutzer Konfigurationsobjekt wurde mithilfe von EWS erstellt. Das zweite Objekt wurde von einer anderen API erstellt. 
    
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

## <a name="get-and-update-application-settings-by-using-the-ews-managed-api"></a>Abrufen und Aktualisieren von Anwendungseinstellungen mithilfe der verwaltete EWS-API
<a name="getconfiguration"> </a>

Nachdem Sie ein Benutzer Konfigurationsobjekt gefunden haben, können Sie die [UserConfiguration. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode verwenden, um das Configuration-Objekt aus dem Postfach abzurufen. Nachdem Sie das Configuration-Objekt abgerufen haben, können Sie es mithilfe der [UserConfiguration. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) -Methode aktualisieren. Im folgenden Beispiel wird gezeigt, wie ein Benutzer Konfigurationsobjekt mithilfe der verwaltete EWS-API abgerufen und aktualisiert wird. 
  
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

Sie können den [GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) -EWS-Vorgang verwenden, um das Configuration-Objekt aus dem Postfach abzurufen, und die [UpdateUserConfiguration](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) , um das Objekt zu aktualisieren. Das folgende Beispiel zeigt die Anforderungs-XML für das erhalten eines Benutzer Konfigurationsobjekts namens TestConfig. Die Anforderung besagt, dass alle Konfigurationen in der Antwort zurückgegeben werden sollen. Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel generiert wird. 
  
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

Im folgenden Beispiel wird die erfolgreiche Antwort-XML für das Aufrufen von Benutzer Konfigurationsobjekten veranschaulicht. Die Antwort enthält ein Datenwörterbuch. Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel verarbeitet wird. 
  
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

Im folgenden Beispiel wird die Anforderungs-XML zum Aktualisieren eines Benutzer Konfigurationsobjekts dargestellt. Die Anforderung besagt, dass alle Konfigurationen in der Antwort zurückgegeben werden sollen. Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel generiert wird, das die **UserConfiguration. Update** -Methode aufruft. Sie können sehen, dass die Update-XML-Datei die vorhandenen Wörterbucheinträge enthält und die zusätzliche, die vor der Aktualisierung hinzugefügt wurde. 
  
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

Der [Antwort-XML-Code](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) ist einfach und gibt an, ob das Update erfolgreich war oder ob ein Fehler aufgetreten ist. 
  
## <a name="delete-an-application-setting-by-using-the-ews-managed-api"></a>Löschen einer Anwendungseinstellung mithilfe der verwaltete EWS-API
<a name="deleteconfiguration"> </a>

Sie können die [UserConfiguration. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode verwenden, um Benutzer Konfigurationsobjekte zu löschen. Im folgenden Codebeispiel wird veranschaulicht, wie Sie das ContosoDraftSettings-Benutzer Konfigurationsobjekt mithilfe der verwaltete EWS-API löschen. 
  
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

Sie können den [DeleteUserConfiguration](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) -EWS-Vorgang verwenden, um Benutzer Konfigurationsobjekte zu löschen. 
  
Das folgende Beispiel zeigt den Anforderungs-XML-Code zum Löschen eines Benutzer Konfigurationsobjekts namens ContosoDraftSettings, das auf den Ordner Entwürfe angewendet wurde. Dies ist derselbe XML-Code, der vom verwaltete EWS-API-Beispiel generiert wird.
  
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

Der [Antwort-XML-Code](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) ist einfach und gibt an, ob die DELETE-Anforderung erfolgreich war oder ob ein Fehler aufgetreten ist. 
  
## <a name="see-also"></a>Siehe auch

- [Persistent Anwendungseinstellungen in EWS in Exchange](persistent-application-settings-in-ews-in-exchange.md)
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)   
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

