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
# <a name="manage-persistent-application-settings-by-using-ews-in-exchange"></a>Verwalten der permanenten Anwendungseinstellungen mithilfe von EWS in Exchange

Informationen Sie zum Erstellen, suchen, erhalten möchten, aktualisieren und löschen, indem Sie die EWS Managed API oder EWS in Exchange persistent Anwendungseinstellungen. 
  
Konfiguration der Benutzerobjekte sind die beste Möglichkeit zum Speichern von Konfigurationseinstellungen für Ihre Exchange-Client-Anwendung in erster Linie, da sie aus den Suchergebnissen in den meisten Clientanwendungen ausgeblendet sind. Clientanwendungen ausblenden diese Einstellungen in der Regel, da finden sie unter der Endbenutzer müssen nicht und, damit der Benutzer nicht versehentlich auf diese Informationen zugreifen. Die Codebeispiele in diesem Artikel zeigen Sie Konfiguration Benutzerobjekte Verwendungsmöglichkeiten persistente Einstellungen sowie zum Erstellen, verwalten finden, abrufen, aktualisieren und Löschen von persistent Anwendungseinstellungen, die in der Konfiguration der Benutzerobjekte gespeichert sind.

<a name="createconfiguration"> </a>

## <a name="create-an-application-setting-by-using-the-ews-managed-api"></a>Erstellen von anwendungseinstellung mithilfe der EWS Managed API

Sie können die [UserConfiguration.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) EWS Managed API-Methode verwenden, zum Erstellen einer benutzerdefinierten Konfiguration-Einstellung. Ein Benutzer-Konfigurationsobjekt kann XML-Code enthalten binär, ein Datenwörterbuch oder eine Kombination dieser drei Datentypen. Im folgenden Beispiel wird veranschaulicht, wie ein Benutzer Configuration-Objekt mit dem Namen ContosoDraftSettings, die binäre Daten in dem Ordner Entwürfe enthält, mithilfe der EWS Managed API gespeichert. Dies ist möglicherweise hilfreich, wenn Sie zum Speichern von Konfigurationsinformationen zu wie Entwurfselemente in der Clientanwendung angezeigt werden soll. 
  
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

## <a name="create-an-application-setting-by-using-ews"></a>Erstellen von anwendungseinstellung mithilfe der Exchange-Webdienste
<a name="bk_createEWS"> </a>

Sie können zum Erstellen einer benutzerdefinierten Konfigurationseinstellung [CreateUserConfiguration](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) EWS-Vorgangs verwenden. Das folgende Beispiel zeigt die Anforderung XML für das Erstellen einer Benutzer-Konfigurationsobjekt mit dem Namen ContosoDraftSettings. Die Anforderung versucht, einen binären Datenstrom ein Benutzerobjekt-Konfiguration auf den Ordner "Entwürfe" speichern. Dies ist die denselben XML-Code, die von der EWS Managed API-Beispiel generiert wird. 
  
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

Die [Antwort-XML-](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) ist einfach und gibt an, ob die Anforderung erstellen erfolgreich war oder ob ein Fehler aufgetreten ist. 
  
## <a name="find-an-application-setting-by-using-the-ews-managed-api"></a>Hier finden Sie eine anwendungseinstellung mithilfe der EWS Managed API
<a name="findconfiguration"> </a>

Die [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS Managed API-Methode können mit der Option zugeordneten durchqueren Sie um Benutzerobjekte Konfiguration zu suchen. Im folgenden Codebeispiel veranschaulicht das Suchen Benutzerobjekte-Konfiguration mithilfe der EWS Managed API auf Ordner "Entwürfe" gespeichert. 
  
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

## <a name="find-an-application-setting-by-using-ews"></a>Hier finden Sie eine anwendungseinstellung mithilfe der Exchange-Webdienste
<a name="bk_findEWS"> </a>

[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS-Vorgangs können Sie die um Konfiguration Benutzerobjekte zu suchen. 
  
Das folgende Beispiel zeigt die Anforderung XML für die Suche nach Benutzer Konfigurationsobjekte. Dies ist die denselben XML-Code, die von der EWS Managed API-Beispiel generiert wird.
  
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

Das folgende Beispiel zeigt die erfolgreiche Antwort-XML für die Suche nach Benutzer Konfigurationsobjekte. Dies ist die denselben XML-Code, der durch das Beispiel EWS Managed API verarbeitet wird. Beachten Sie Folgendes in der XML-Antwort: 
  
- Wir verkürzt die Schlüssel-ID und ein Änderungsprotokoll zur besseren Lesbarkeit wurde.
    
- Die beiden Benutzerobjekte Konfiguration werden als Nachrichten zurückgegeben. Dies ist, da die Operation **FindItem** gibt alle Elemente zurück, die nicht als Nachrichtenelemente in die EWS-Schema definiert sind. 
    
- Die [ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) -Eigenschaften für die beiden Benutzerobjekte Konfiguration unterscheiden. Das erste Benutzerobjekt-Konfiguration wurde mithilfe von EWS erstellt. Das zweite Objekt wurde durch eine andere API erstellt. 
    
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

## <a name="get-and-update-application-settings-by-using-the-ews-managed-api"></a>Abrufen und Aktualisieren von Anwendungseinstellungen mithilfe der EWS Managed API
<a name="getconfiguration"> </a>

Wenn Sie eine Benutzer-Konfigurationsobjekt gefunden haben, können Sie die [UserConfiguration.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) EWS Managed API-Methode zum Abrufen des Configuration-Objekts aus dem Postfach verwenden. Nachdem Sie das Konfigurationsobjekt erhalten möchten, können Sie die [UserConfiguration.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) -Methode verwenden, um zu aktualisieren. Im folgenden Beispiel wird gezeigt, wie zum Abrufen und Aktualisieren einer Benutzer-Konfigurationsobjekt mithilfe der EWS Managed API. 
  
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

## <a name="get-and-update-application-settings-by-using-ews"></a>Abrufen und Aktualisieren von Anwendungseinstellungen mithilfe von Exchange-Webdienste
<a name="bk_getEWS"> </a>

[GetUserConfiguration](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS-Vorgangs können Sie das Configuration-Objekt aus dem Postfach und die [UpdateUserConfiguration](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) zum Aktualisieren des Objekts abgerufen. Das folgende Beispiel zeigt die Anforderung XML zum Abrufen einer Benutzer-Konfigurationsobjekt mit dem Namen TestConfig. Die Anforderung besagt, dass alle Konfigurationen in der Antwort zurückgegeben werden sollen. Dies ist die denselben XML-Code, die von der EWS Managed API-Beispiel generiert wird. 
  
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

Das folgende Beispiel zeigt die erfolgreiche Antwort XML zum Abrufen eines Benutzers von Konfigurationsobjekten. Die Antwort enthält ein Datenwörterbuch. Dies ist die denselben XML-Code, der durch das Beispiel EWS Managed API verarbeitet wird. 
  
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

Das folgende Beispiel zeigt die Anforderung XML für das Aktualisieren einer Benutzer-Konfigurationsobjekt. Die Anforderung besagt, dass alle Konfigurationen in der Antwort zurückgegeben werden sollen. Dies ist die denselben XML-Code, die von der EWS Managed API-Beispiel generiert wird, die die **UserConfiguration.Update** -Methode aufruft. Sie können sehen, dass das XML-Update enthält, die vorhandenen Wörterbucheinträge und zusätzliche diejenige, die vor der Aktualisierung hinzugefügt wurde. 
  
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

Die [Antwort-XML-](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) ist einfach und gibt an, ob die Aktualisierung erfolgreich war oder ob ein Fehler aufgetreten ist. 
  
## <a name="delete-an-application-setting-by-using-the-ews-managed-api"></a>Löschen von anwendungseinstellung mithilfe der EWS Managed API
<a name="deleteconfiguration"> </a>

Die [UserConfiguration.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS Managed API-Methode können Sie die Konfiguration Benutzerobjekte löschen. Das folgende Codebeispiel veranschaulicht das ContosoDraftSettings Benutzer Configuration-Objekt löschen, indem Sie die EWS Managed API. 
  
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

## <a name="delete-an-application-setting-by-using-ews"></a>Löschen von anwendungseinstellung mithilfe der Exchange-Webdienste
<a name="bk_deleteEWS"> </a>

[DeleteUserConfiguration](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) EWS-Vorgangs können Sie die Konfiguration der Benutzerobjekte löschen. 
  
Das folgende Beispiel zeigt die Anforderung XML zum Löschen einer Benutzer-Konfigurationsobjekt mit dem Namen ContosoDraftSettings, die im Ordner Entwürfe angewendet wurde. Dies ist die denselben XML-Code, die von der EWS Managed API-Beispiel generiert wird.
  
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

Die [Antwort-XML-](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) ist einfach und gibt an, ob die Delete-Anforderung erfolgreich war oder ob ein Fehler aufgetreten ist. 
  
## <a name="see-also"></a>Siehe auch

- [Persistent Anwendungseinstellungen in EWS in Exchange](persistent-application-settings-in-ews-in-exchange.md)
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)   
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

