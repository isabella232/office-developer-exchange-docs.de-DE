---
title: Hinzufügen und Entfernen von Stellvertretungen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cc7760bf-633b-483a-84ae-b52f437af2d3
description: Erfahren Sie, wie Stellvertretungen auf Hinzufügen oder Entfernen von Stellvertretungen aus den Postfächern der Benutzer verwenden die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: d55ef6c5c4e434603d293dbe30c6147ceb73b08b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756854"
---
# <a name="add-and-remove-delegates-by-using-ews-in-exchange"></a>Hinzufügen und Entfernen von Stellvertretungen mithilfe von EWS in Exchange

Erfahren Sie, wie Stellvertretungen auf Hinzufügen oder Entfernen von Stellvertretungen aus den Postfächern der Benutzer verwenden die EWS Managed API oder EWS in Exchange.
  
Sie können die EWS Managed API oder EWS verwenden, um Delegaten Zustimmung des Besitzers des Zielpostfachs oder Entfernen eines Stellvertreters Zugriff auf ein Postfach zu aktivieren. Benutzer, die eine Stellvertretung hinzugefügt wurden, und erhalten Berechtigungen können im Namen der Postfachbesitzer Aufgaben auszuführen. Sie können beispielsweise erstellen und Senden von Besprechungsanfragen, e-Mails senden und Antworten auf Besprechungsanfragen im Auftrag des Postfachbesitzers. 
  
**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge zum Hinzufügen und Entfernen von Stellvertretungen**

|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Hinzufügen von Stellvertretungen  <br/> |[ExchangeService.AddDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/> |[AddDelegate](http://msdn.microsoft.com/library/646fb994-229e-4d90-8b95-6541191cb3ae%28Office.15%29.aspx) <br/> |
|Entfernen von Stellvertretungen  <br/> |[ExchangeService.RemoveDelegates](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |[RemoveDelegate](http://msdn.microsoft.com/library/f21c5171-62e7-47c8-99b1-22e1ff5883bb%28Office.15%29.aspx) <br/> |
   
Nachdem eine Stellvertretung Berechtigungen für einen Ordner gewährt wurde, können sie gemäß ihren [Delegieren von Berechtigungen](delegate-access-and-ews-in-exchange.md#bk_delegateperms)für Elemente im Ordner und alle Unterordner fungieren. Berechtigungen für Stellvertretungen gelten nur für Unterordner, die erstellt werden, nachdem der Stellvertretungszugriff eingeholt wurde. Um Ordnerberechtigungen für vorhandenem Ordner oder andere Ordner zu aktualisieren, finden Sie unter [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der Exchange-Webdienste im Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).
  
Beachten Sie, dass Delegaten nur postfachaktivierten Konten, einschließlich e-Mail-aktivierte Sicherheitsgruppen hinzugefügt werden können. In der Standardeinstellung kann ein einzigen EWS-Delegaten Access Anruf maximal 255 verschiedene Postfächer zugreifen.

<a name="bk_adddelegateewsma"> </a>

## <a name="add-delegates-by-using-the-ews-managed-api"></a>Hinzufügen von Stellvertretungen mithilfe der EWS Managed API

Sie können Delegaten an ein Postfach mithilfe der [AddDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) EWS Managed API-Methode hinzufügen. In den in diesem Beispiel wird, einen neuen Kalender, Kontakt- und e-Mail- [Beauftragte Benutzer](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegateuser%28v=exchg.80%29.aspx) -Objekt erstellt wurde, und jeder Delegaten [Editor-Berechtigungen](delegate-access-and-ews-in-exchange.md#bk_delegateperms) für die entsprechenden Ordner angegeben wird. Sie können das Beispiel eine Stellvertretung hinzu, der die durch die [DelegatePermissions-Eigenschaften](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatepermissions_properties%28v=exchg.80%29.aspx)angegebenen Ordner ändern, und Sie können die Berechtigungen festlegen, um einen der Werte der [DelegateFolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) -Enumeration angegeben. 
  
In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Besitzer des Postfachs und der Benutzer wurde an einen Exchange-Server authentifiziert wurden. 
  
```cs
public static Collection<DelegateUserResponse> AddDelegates(ExchangeService service)
{
    // Create a list to hold the new delegates to add.
    List<DelegateUser> newDelegates = new System.Collections.Generic.List<DelegateUser>();
    // Create a new delegate that has editor access to the mailbox owner's Calendar folder.
    DelegateUser calendarDelegate = new DelegateUser("calendardelegate@contoso.com");
    calendarDelegate.Permissions.CalendarFolderPermissionLevel = DelegateFolderPermissionLevel.Editor;
    // Add the delegate to the list of new delegates.
    newDelegates.Add(calendarDelegate);
    // Create a new delegate that has editor access to the mailbox owner's Contacts folder.
    DelegateUser contactDelegate = new DelegateUser("contactdelegate@contoso.com");
    contactDelegate.Permissions.ContactsFolderPermissionLevel = DelegateFolderPermissionLevel.Editor;
    // Add the delegate to the list of new delegates.
    newDelegates.Add(contactDelegate);
            
    // Create a new delegate that has editor access to the mailbox owner's Inbox folder.
    DelegateUser emailDelegate = new DelegateUser("emaildelegate@contoso.com");
    emailDelegate.Permissions.InboxFolderPermissionLevel = DelegateFolderPermissionLevel.Editor;
    // Add the delegate to the list of new delegates.
    newDelegates.Add(emailDelegate);
    // Create a mailbox object that represents the mailbox owner.
    Mailbox mailbox = new Mailbox("primary@contoso.com");
    // Call the AddDelegates method to add the delegates to the target mailbox.
    Collection<DelegateUserResponse> response = service.AddDelegates(mailbox, MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe, newDelegates);
            
    foreach (DelegateUserResponse resp in response)
    {
        // Print out the result and the last eight characters of the item ID.
        Console.WriteLine("For delegate " + resp.DelegateUser.UserId.PrimarySmtpAddress.ToString());
        Console.WriteLine("Result: {0}", resp.Result);
        Console.WriteLine("Error Code: {0}", resp.ErrorCode);
        Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
        Console.WriteLine("\r\n");
    }
    return response;
}
```

<a name="bk_adddelegateews"> </a>

## <a name="add-delegates-by-using-ews"></a>Hinzufügen von Stellvertretungen mithilfe von Exchange-Webdienste

Das folgende Codebeispiel veranschaulicht das Hinzufügen separater Kalender, Kontakte und e-Mail-Delegaten mithilfe von [AddDelegate](http://msdn.microsoft.com/library/012d8cc5-648c-4ba0-a155-15c422b1e994%28Office.15%29.aspx) EWS-Vorgangs. So ändern Sie das Postfach vom [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element angegeben ist, und [die berechtigungseinstellungen für jeden Delegaten](delegate-access-and-ews-in-exchange.md#bk_delegateperms) in der [Beauftragte Benutzer](http://msdn.microsoft.com/library/aac4e74e-f69b-4c41-a0c9-489610330fbf%28Office.15%29.aspx) -Element enthalten sind. Jeder der Delegaten wurde Editorberechtigungen für ihre Zielordner erteilt. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **AddDelegates** -Methode zum [Hinzufügen von Delegaten](#bk_adddelegateewsma)verwenden.
  
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
    <m:AddDelegate>
      <m:Mailbox>
        <t:EmailAddress>primary@contoso.com</t:EmailAddress>
      </m:Mailbox>
      <m:DelegateUsers>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>calendardelegate@contoso.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>Editor</t:CalendarFolderPermissionLevel>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
            <t:InboxFolderPermissionLevel>None</t:InboxFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>None</t:ContactsFolderPermissionLevel>
            <t:NotesFolderPermissionLevel>None</t:NotesFolderPermissionLevel>
            <t:JournalFolderPermissionLevel>None</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>contactdelegate@contoso.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>None</t:CalendarFolderPermissionLevel>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
            <t:InboxFolderPermissionLevel>None</t:InboxFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>Editor</t:ContactsFolderPermissionLevel>
            <t:NotesFolderPermissionLevel>None</t:NotesFolderPermissionLevel>
            <t:JournalFolderPermissionLevel>None</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>emaildelegate@contoso.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>None</t:CalendarFolderPermissionLevel>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
            <t:InboxFolderPermissionLevel>Editor</t:InboxFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>None</t:ContactsFolderPermissionLevel>
            <t:NotesFolderPermissionLevel>None</t:NotesFolderPermissionLevel>
            <t:JournalFolderPermissionLevel>None</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
      </m:DelegateUsers>
      <m:DeliverMeetingRequests>DelegatesAndSendInformationToMe</m:DeliverMeetingRequests>
    </m:AddDelegate>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die Anforderung **AddDelegate** mit einer [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Stellvertretungen erfolgreich erstellt wurden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="888"
                         MinorBuildNumber="9"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:AddDelegateResponse ResponseClass="Success"
                           xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1337771579-694202782-848329751-1535221</t:SID>
              <t:PrimarySmtpAddress>calendardelegate@contoso.com</t:PrimarySmtpAddress>
              <t:DisplayName>calendardelegate</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1337771579-694202782-848329751-1535264</t:SID>
              <t:PrimarySmtpAddress>contactdelegate@contoso.com</t:PrimarySmtpAddress>
              <t:DisplayName>contactdelegate</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1337771579-694202782-848329751-1535223</t:SID>
              <t:PrimarySmtpAddress>emaildelegate@contoso.com</t:PrimarySmtpAddress>
              <t:DisplayName>emaildelegate</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:AddDelegateResponse>
  </s:Body>
</s:Envelope>
```

<a name="bk_removedelegateewsma"> </a>

## <a name="remove-delegates-by-using-the-ews-managed-api"></a>Entfernen von Stellvertretungen mithilfe der EWS Managed API

Sie können Delegaten aus einer Zielpostfach mithilfe der [ExchangeService.RemoveDelegates](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) EWS Managed API-Methode entfernen. In diesem Beispiel werden die Stellvertretung Berechtigungssatz [Hinzufügen ein Beispiel für einen Delegaten](#bk_adddelegateewsma) entfernt. 
  
In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Besitzer des Postfachs und der Benutzer wurde an einen Exchange-Server authentifiziert wurden. 
  
```cs
public static Collection<DelegateUserResponse> RemoveDelegates(ExchangeService service)
{
    // Create a list to hold the delegates to delete.
    List<UserId> deletedDelegates = new System.Collections.Generic.List<UserId>();
    // Add the delegate to the list of new delegates.
    deletedDelegates.Add("calendardelegate@contoso.com");
    // Add the delegate to the list of new delegates.
    deletedDelegates.Add("contactdelegate@contoso.com");
    // Add the delegate to the list of new delegates.
    deletedDelegates.Add("emaildelegate@contoso.com");
    // Create a mailbox object that represents the mailbox owner.
    Mailbox mailbox = new Mailbox("primary@contoso.com");
    // Call the AddDelegates method to add the delegates to the target mailbox.
    Collection<DelegateUserResponse> response = service.RemoveDelegates(mailbox, deletedDelegates);
    foreach (DelegateUserResponse resp in response)
    {
        // Print out the result and the last eight characters of the item ID.
        Console.WriteLine("Result: {0}", resp.Result);
        Console.WriteLine("Error Code: {0}", resp.ErrorCode);
        Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
    }
    return response;
}
```

<a name="bk_removedelegateews"> </a>

## <a name="remove-delegates-by-using-ews"></a>Entfernen von Stellvertretungen mithilfe von Exchange-Webdienste

Sie können Delegaten aus einem Postfach mithilfe des [RemoveDelegate](http://msdn.microsoft.com/library/1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a%28Office.15%29.aspx) EWS-Vorgangs entfernen. In diesem Beispiel werden die Stellvertretung Berechtigungssatz [Hinzufügen ein Beispiel für einen Delegaten](#bk_adddelegateews) entfernt. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **RemoveDelegates** -Methode zum [Entfernen von Delegaten](#bk_removedelegateewsma)verwenden.
  
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
    <m:RemoveDelegate>
      <m:Mailbox>
        <t:EmailAddress>primary@contoso.com</t:EmailAddress>
      </m:Mailbox>
      <m:UserIds>
        <t:UserId>
          <t:PrimarySmtpAddress>calendardelegate@contoso.com</t:PrimarySmtpAddress>
        </t:UserId>
        <t:UserId>
          <t:PrimarySmtpAddress>contactdelegate@contoso.com</t:PrimarySmtpAddress>
        </t:UserId>
        <t:UserId>
          <t:PrimarySmtpAddress>emaildelegate@contoso.com</t:PrimarySmtpAddress>
        </t:UserId>
      </m:UserIds>
    </m:RemoveDelegate>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die Anforderung **RemoveDelegate** mit einer [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Stellvertretungen erfolgreich entfernt wurden.

<a name="bk_nextsteps"> </a>

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie Kalender, e-Mail und Aufgabenordner Stellvertretungen hinzufügen, kann die Stellvertretung die Elemente in den Ordnern zugreifen. Finden Sie weitere Informationen finden Sie in den folgenden Artikeln:
  
- [Access-e-Mail eine Stellvertretung mithilfe der EWS in Exchange](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Zugriff auf einen Kalender als Stellvertretung mithilfe der EWS in Exchange](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Access-Kontakte als Stellvertretung mithilfe der EWS in Exchange](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
Wenn die Ordner, für die Stellvertretungen hinzugefügt, untergeordneten Ordner, die erstellt wurden enthalten, bevor Sie den Stellvertretungszugriff gewährt, werden die Stellvertretung nicht auf diese Ordner ohne zusätzliche Berechtigungen zugreifen. Um diese Berechtigungen hinzufügen oder Ändern von Berechtigungen für alle anderen Ordner, finden Sie unter [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der Exchange-Webdienste im Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).
  
## <a name="see-also"></a>Siehe auch

- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)
- [Exchange 2013: Hinzufügen Benutzer ein e-Mail-Konto programmgesteuert delegieren](http://code.msdn.microsoft.com/exchange/Exchange-2013-Adding-1024511f)   
- [Exchange 2013: Aktualisieren von e-Mail-Konten programmgesteuert zugeordnete Delegaten](http://code.msdn.microsoft.com/exchange/Exchange-2013-Update-b40d3bac)   
- [Exchange 2013: Zugeordnete e-Mail-Konten programmgesteuert Delegaten entfernen](http://code.msdn.microsoft.com/exchange/Exchange-2013-Remove-686f7714)
    

