---
title: Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: cc7760bf-633b-483a-84ae-b52f437af2d3
description: Erfahren Sie, wie Sie Mithilfe der verwalteten EWS-API oder EWS in Exchange Stellvertretungen zu den Postfächern von Benutzern hinzufügen oder Stellvertretungen aus den Postfächern von Benutzern entfernen.
ms.openlocfilehash: 67370360e24da55b7a908d0a34b7ac1ec949877d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520206"
---
# <a name="add-and-remove-delegates-by-using-ews-in-exchange"></a>Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange

Erfahren Sie, wie Sie Mithilfe der verwalteten EWS-API oder EWS in Exchange Stellvertretungen zu den Postfächern von Benutzern hinzufügen oder Stellvertretungen aus den Postfächern von Benutzern entfernen.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um Stellvertretungen zu ermöglichen, im Namen eines Postfachbesitzers zu handeln oder den Zugriff eines Stellvertreters auf ein Postfach zu entfernen. Benutzer, die als Stellvertretung hinzugefügt werden und Berechtigungen erhalten, können Aufgaben im Namen des Postfachbesitzers ausführen. Sie können beispielsweise Besprechungseinladungen erstellen und senden, E-Mails senden und im Namen des Postfachbesitzers auf Besprechungsanfragen antworten. 
  
**Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge zum Hinzufügen und Entfernen von Delegaten**

|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Hinzufügen von Delegaten  <br/> |[ExchangeService.AddDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/> |[AddDelegate](https://msdn.microsoft.com/library/646fb994-229e-4d90-8b95-6541191cb3ae%28Office.15%29.aspx) <br/> |
|Entfernen von Delegaten  <br/> |[ExchangeService.RemoveDelegates](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |[RemoveDelegate](https://msdn.microsoft.com/library/f21c5171-62e7-47c8-99b1-22e1ff5883bb%28Office.15%29.aspx) <br/> |
   
Nachdem einem Delegaten Berechtigungen für einen Ordner erteilt wurden, kann er auf Elemente im Ordner und alle Unterordner entsprechend ihren [Stellvertretungsberechtigungen](delegate-access-and-ews-in-exchange.md#bk_delegateperms)reagieren. Berechtigungen für Stellvertretungen gelten nur für Unterordner, die erstellt werden, nachdem der Stellvertretungszugriff gewährt wurde. Informationen zum Aktualisieren von Ordnerberechtigungen für bereits vorhandene Ordner oder andere Ordner finden Sie unter [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe von EWS in Exchange.](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
  
Beachten Sie, dass Stellvertretungen nur postfachaktivierten Konten hinzugefügt werden können, einschließlich E-Mail-aktivierter Sicherheitsgruppen. Standardmäßig kann ein einzelner EWS-Delegatzugriffsaufruf auf maximal 255 verschiedene Postfächer zugreifen.

<a name="bk_adddelegateewsma"> </a>

## <a name="add-delegates-by-using-the-ews-managed-api"></a>Hinzufügen von Delegaten mithilfe der verwalteten EWS-API

Sie können Stellvertretungen zu einem Postfach hinzufügen, indem Sie die verwaltete EWS-API-Methode ["AddDelegates"](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) verwenden. In diesem Beispiel wird ein neues [DelegateUser-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegateuser%28v=exchg.80%29.aspx) für Kalender, Kontakt und E-Mail erstellt, und jedem Delegaten werden [Editorberechtigungen](delegate-access-and-ews-in-exchange.md#bk_delegateperms) für den jeweiligen Ordner erteilt. Sie können das Beispiel so ändern, dass einem der durch die [DelegatePermissions-Eigenschaften angegebenen](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegatepermissions_properties%28v=exchg.80%29.aspx)Ordner ein Delegat hinzugefügt wird, und Sie können die Berechtigungen auf einen der durch die [DelegateFolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) -Enumeration angegebenen Werte festlegen. 
  
In diesem Beispiel wird davon ausgegangen, dass der **Dienst** ein gültiges [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) für den Postfachbesitzer ist und dass der Benutzer bei einem Exchange Server authentifiziert wurde. 
  
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

## <a name="add-delegates-by-using-ews"></a>Hinzufügen von Delegaten mithilfe von EWS

Das folgende Codebeispiel zeigt, wie Sie mithilfe des EWS-Vorgangs ["AddDelegate"](https://msdn.microsoft.com/library/012d8cc5-648c-4ba0-a155-15c422b1e994%28Office.15%29.aspx) separate Kalender-, Kontakt- und E-Mail-Stellvertretungen hinzufügen. Das zu ändernde Postfach wird durch das [Mailbox-Element](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) angegeben, und die [Berechtigungseinstellungen](delegate-access-and-ews-in-exchange.md#bk_delegateperms) für jeden Delegaten sind im [DelegateUser-Element](https://msdn.microsoft.com/library/aac4e74e-f69b-4c41-a0c9-489610330fbf%28Office.15%29.aspx) enthalten. Jeder Stellvertretung wurden Editorberechtigungen für ihren Zielordner gewährt. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **AddDelegates** -Methode zum [Hinzufügen von Delegaten](#bk_adddelegateewsma)verwenden.
  
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

Der Server antwortet auf die **AddDelegate-Anforderung** mit einer [AddDelegateResponse-Nachricht,](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **"NoError"** enthält, der angibt, dass die Delegaten erfolgreich erstellt wurden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="888"
                         MinorBuildNumber="9"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:AddDelegateResponse ResponseClass="Success"
                           xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="remove-delegates-by-using-the-ews-managed-api"></a>Entfernen von Delegaten mithilfe der verwalteten EWS-API

Sie können Stellvertretungen aus einem Zielpostfach mithilfe der [ExchangeService.RemoveDelegates](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) EWS Managed API-Methode entfernen. In diesem Beispiel werden die im Beispiel zum [Hinzufügen eines Delegaten](#bk_adddelegateewsma) festgelegten Stellvertretungsberechtigungen entfernt. 
  
In diesem Beispiel wird davon ausgegangen, dass der **Dienst** ein gültiges [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) für den Postfachbesitzer ist und dass der Benutzer bei einem Exchange Server authentifiziert wurde. 
  
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

## <a name="remove-delegates-by-using-ews"></a>Entfernen von Delegaten mithilfe von EWS

Mithilfe des EWS-Vorgangs ["RemoveDelegate"](https://msdn.microsoft.com/library/1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a%28Office.15%29.aspx) können Sie Stellvertretungen aus einem Postfach entfernen. In diesem Beispiel werden die im Beispiel zum [Hinzufügen eines Delegaten](#bk_adddelegateews) festgelegten Stellvertretungsberechtigungen entfernt. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **RemoveDelegates** -Methode zum [Entfernen von Delegaten](#bk_removedelegateewsma)verwenden.
  
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

Der Server antwortet auf die **RemoveDelegate-Anforderung** mit einer [AddDelegateResponse-Nachricht,](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **"NoError"** enthält, der angibt, dass die Delegaten erfolgreich entfernt wurden.

<a name="bk_nextsteps"> </a>

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie Stellvertretungen zu Kalender-, E-Mail- und Aufgabenordnern hinzugefügt haben, kann der Stellvertreter auf die Elemente in den Ordnern zugreifen. Weitere Informationen finden Sie in den folgenden Artikeln:
  
- [Zugreifen auf E-Mails als Stellvertretung mithilfe der EWS in Exchange](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Zugriff auf einen Kalender als Delegat mithilfe der EWS in Exchange](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Zugriff auf Kontakte als Delegat mithilfe der EWS in Exchange](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
Wenn die Ordner, für die Sie Stellvertretungen hinzugefügt haben, untergeordnete Ordner enthalten, die erstellt wurden, bevor Sie der Stellvertretung Zugriff gewährt haben, kann der Delegat ohne zusätzliche Berechtigungen nicht auf diese Ordner zugreifen. Informationen zum Hinzufügen dieser Berechtigungen oder Ändern von Berechtigungen für andere Ordner finden Sie unter [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe von EWS in Exchange.](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
  
## <a name="see-also"></a>Siehe auch

- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)
- [Exchange 2013: Programmgesteuertes Hinzufügen von Stellvertretungsbenutzern zu einem E-Mail-Konto](https://code.msdn.microsoft.com/exchange/Exchange-2013-Adding-1024511f)   
- [Exchange 2013: Programmgesteuertes Aktualisieren von E-Mail-Konten zugeordneten Delegaten](https://code.msdn.microsoft.com/exchange/Exchange-2013-Update-b40d3bac)   
- [Exchange 2013: Programmgesteuertes Entfernen von E-Mail-Konten zugeordneten Delegaten](https://code.msdn.microsoft.com/exchange/Exchange-2013-Remove-686f7714)
    

