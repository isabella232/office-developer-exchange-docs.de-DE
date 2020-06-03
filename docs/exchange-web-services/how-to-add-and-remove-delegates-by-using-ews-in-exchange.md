---
title: Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cc7760bf-633b-483a-84ae-b52f437af2d3
description: In diesem Artikel erfahren Sie, wie Sie Stellvertretungen für Benutzerpostfächer mithilfe der verwaltete EWS-API oder EWS in Exchange hinzufügen oder entfernen.
ms.openlocfilehash: 9db0171db51c0847d54bbcec7e28937eaed18d43
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455338"
---
# <a name="add-and-remove-delegates-by-using-ews-in-exchange"></a><span data-ttu-id="27672-103">Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="27672-103">Add and remove delegates by using EWS in Exchange</span></span>

<span data-ttu-id="27672-104">In diesem Artikel erfahren Sie, wie Sie Stellvertretungen für Benutzerpostfächer mithilfe der verwaltete EWS-API oder EWS in Exchange hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="27672-104">Learn how to add delegates to or remove delegates from users' mailboxes by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="27672-105">Sie können die verwaltete EWS-API oder EWS verwenden, um Stellvertretungen zu aktivieren, die im Auftrag eines Postfachbesitzers agieren oder den Zugriff einer Stellvertretung auf ein Postfach entfernen.</span><span class="sxs-lookup"><span data-stu-id="27672-105">You can use the EWS Managed API or EWS to enable delegates to act on behalf of a mailbox owner or remove a delegate's access to a mailbox.</span></span> <span data-ttu-id="27672-106">Benutzer, die als Stellvertretung hinzugefügt und Berechtigungen erteilt werden, können Aufgaben im Namen des Postfachbesitzers ausführen.</span><span class="sxs-lookup"><span data-stu-id="27672-106">Users who are added as a delegate, and are given permissions, can perform tasks on behalf of the mailbox owner.</span></span> <span data-ttu-id="27672-107">Sie können beispielsweise Besprechungseinladungen erstellen und senden, e-Mails senden und auf Besprechungsanfragen im Namen des Postfachbesitzers Antworten.</span><span class="sxs-lookup"><span data-stu-id="27672-107">For example, they can create and send meeting invitations, send emails, and respond to meeting requests on the mailbox owner's behalf.</span></span> 
  
<span data-ttu-id="27672-108">**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge zum Hinzufügen und Entfernen von Delegaten**</span><span class="sxs-lookup"><span data-stu-id="27672-108">**Table 1. EWS Managed API methods and EWS operations for adding and removing delegates**</span></span>

|<span data-ttu-id="27672-109">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="27672-109">**Task**</span></span>|<span data-ttu-id="27672-110">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="27672-110">**EWS Managed API method**</span></span>|<span data-ttu-id="27672-111">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="27672-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="27672-112">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="27672-112">Add delegates</span></span>  <br/> |[<span data-ttu-id="27672-113">Datei "ExchangeService. adddelegates</span><span class="sxs-lookup"><span data-stu-id="27672-113">ExchangeService.AddDelegates</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="27672-114">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="27672-114">AddDelegate</span></span>](https://msdn.microsoft.com/library/646fb994-229e-4d90-8b95-6541191cb3ae%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="27672-115">Entfernen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="27672-115">Remove delegates</span></span>  <br/> |[<span data-ttu-id="27672-116">Datei "ExchangeService. RemoveDelegates</span><span class="sxs-lookup"><span data-stu-id="27672-116">ExchangeService.RemoveDelegates</span></span>](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="27672-117">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="27672-117">RemoveDelegate</span></span>](https://msdn.microsoft.com/library/f21c5171-62e7-47c8-99b1-22e1ff5883bb%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="27672-118">Nachdem einer Stellvertretung Berechtigungen für einen Ordner erteilt wurden, können Sie Elemente im Ordner und alle Unterordner entsprechend den [Berechtigungen des Stellvertreters](delegate-access-and-ews-in-exchange.md#bk_delegateperms)bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="27672-118">After a delegate is granted permissions to a folder, they can act on items in the folder and any subfolders, according to their [delegate permissions](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span></span> <span data-ttu-id="27672-119">Berechtigungen für Stellvertretungen gelten nur für Unterordner, die erstellt werden, nachdem der Stell Vertretungszugriff erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="27672-119">Permissions for delegates only apply to subfolders that are created after the delegate access was granted.</span></span> <span data-ttu-id="27672-120">Informationen zum Aktualisieren von Ordnerberechtigungen für bereits vorhandene Ordner oder andere Ordner finden Sie unter [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe von EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="27672-120">To update folder permissions for pre-existing folders, or other folders, see [Set folder permissions for another user by using EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="27672-121">Beachten Sie, dass Stellvertretungen nur postfachaktivierten Konten hinzugefügt werden können, einschließlich e-Mail-aktivierter Sicherheitsgruppen.</span><span class="sxs-lookup"><span data-stu-id="27672-121">Note that delegates can only be added to mailbox-enabled accounts, including mail-enabled security groups.</span></span> <span data-ttu-id="27672-122">Standardmäßig kann ein einzelner Rückruf für einen EWS-Stellvertreter auf maximal 255 unterschiedliche Postfächer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="27672-122">By default, a single EWS delegate access call can access a maximum of 255 different mailboxes.</span></span>

<span data-ttu-id="27672-123"><a name="bk_adddelegateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="27672-123"><a name="bk_adddelegateewsma"> </a></span></span>

## <a name="add-delegates-by-using-the-ews-managed-api"></a><span data-ttu-id="27672-124">Hinzufügen von Stellvertretungen mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="27672-124">Add delegates by using the EWS Managed API</span></span>

<span data-ttu-id="27672-125">Sie können Delegaten zu einem Postfach hinzufügen, indem Sie die [adddelegats](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="27672-125">You can add delegates to a mailbox by using the [AddDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) EWS Managed API method.</span></span> <span data-ttu-id="27672-126">In diesem Beispiel wird ein neues [DelegateUser](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegateuser%28v=exchg.80%29.aspx) -Objekt für Kalender, Kontakt und e-Mail erstellt, und jeder Stellvertretung werden [Editor Berechtigungen](delegate-access-and-ews-in-exchange.md#bk_delegateperms) für den jeweiligen Ordner zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="27672-126">In this example, a new calendar, contact, and email [DelegateUser](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegateuser%28v=exchg.80%29.aspx) object is created, and each delegate is given [Editor permissions](delegate-access-and-ews-in-exchange.md#bk_delegateperms) for their respective folder.</span></span> <span data-ttu-id="27672-127">Sie können das Beispiel so ändern, dass einem der durch die [DelegatePermissions-Eigenschaften](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegatepermissions_properties%28v=exchg.80%29.aspx)angegebenen Ordner eine Stellvertretung hinzugefügt wird, und Sie können die Berechtigungen auf einen der in der [DelegateFolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) -Aufzählung angegebenen Werte festlegen.</span><span class="sxs-lookup"><span data-stu-id="27672-127">You can modify the example to add a delegate to any of the folders specified by the [DelegatePermissions properties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegatepermissions_properties%28v=exchg.80%29.aspx), and you can set the permissions to any of the values specified by the [DelegateFolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) enumeration.</span></span> 
  
<span data-ttu-id="27672-128">In diesem Beispiel wird davon ausgegangen, dass **Service** ein gültiges [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Postfachbesitzer ist und dass der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="27672-128">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="27672-129"><a name="bk_adddelegateews"> </a></span><span class="sxs-lookup"><span data-stu-id="27672-129"><a name="bk_adddelegateews"> </a></span></span>

## <a name="add-delegates-by-using-ews"></a><span data-ttu-id="27672-130">Hinzufügen von Stellvertretungen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="27672-130">Add delegates by using EWS</span></span>

<span data-ttu-id="27672-131">Im folgenden Codebeispiel wird gezeigt, wie Sie mit dem EWS-Vorgang [AddDelegate](https://msdn.microsoft.com/library/012d8cc5-648c-4ba0-a155-15c422b1e994%28Office.15%29.aspx) separate Kalender-, Kontakt-und e-Mail-Delegaten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="27672-131">The following code example shows how to add separate calendar, contact, and email delegates by using the [AddDelegate](https://msdn.microsoft.com/library/012d8cc5-648c-4ba0-a155-15c422b1e994%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="27672-132">Das zu ändernde Postfach wird durch das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element angegeben, und die [Berechtigungs](delegate-access-and-ews-in-exchange.md#bk_delegateperms) Einstellungen für die einzelnen Delegaten sind im [DelegateUser](https://msdn.microsoft.com/library/aac4e74e-f69b-4c41-a0c9-489610330fbf%28Office.15%29.aspx) -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="27672-132">The mailbox to modify is specified by the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element, and the [permission](delegate-access-and-ews-in-exchange.md#bk_delegateperms) settings for each delegate are contained in the [DelegateUser](https://msdn.microsoft.com/library/aac4e74e-f69b-4c41-a0c9-489610330fbf%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="27672-133">Jeder Stellvertretung wurden Editor Berechtigungen für ihren Zielordner erteilt.</span><span class="sxs-lookup"><span data-stu-id="27672-133">Each of the delegates has been granted Editor permissions to their target folder.</span></span> 
  
<span data-ttu-id="27672-134">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die **adddelegates** -Methode zum [Hinzufügen von Stellvertretungen](#bk_adddelegateewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="27672-134">This is also the XML request that the EWS Managed API sends when you use the **AddDelegates** method to [add delegates](#bk_adddelegateewsma).</span></span>
  
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

<span data-ttu-id="27672-135">Der Server antwortet auf die **AddDelegate** -Anforderung mit einer [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die Stellvertretungen erfolgreich erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="27672-135">The server responds to the **AddDelegate** request with an [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the delegates were successfully created.</span></span>
  
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

<span data-ttu-id="27672-136"><a name="bk_removedelegateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="27672-136"><a name="bk_removedelegateewsma"> </a></span></span>

## <a name="remove-delegates-by-using-the-ews-managed-api"></a><span data-ttu-id="27672-137">Entfernen von Stellvertretungen mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="27672-137">Remove delegates by using the EWS Managed API</span></span>

<span data-ttu-id="27672-138">Sie können Delegaten aus einem Zielpostfach mithilfe der [Datei "ExchangeService. RemoveDelegates](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode entfernen.</span><span class="sxs-lookup"><span data-stu-id="27672-138">You can remove delegates from a target mailbox by using the [ExchangeService.RemoveDelegates](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) EWS Managed API method.</span></span> <span data-ttu-id="27672-139">In diesem Beispiel werden die im [Beispiel zum Hinzufügen eines Stellvertreters](#bk_adddelegateewsma) festgelegten Stell Vertretungs Berechtigungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="27672-139">In this example, the delegate permissions set in the [add a delegate example](#bk_adddelegateewsma) are removed.</span></span> 
  
<span data-ttu-id="27672-140">In diesem Beispiel wird davon ausgegangen, dass **Service** ein gültiges [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Postfachbesitzer ist und dass der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="27672-140">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="27672-141"><a name="bk_removedelegateews"> </a></span><span class="sxs-lookup"><span data-stu-id="27672-141"><a name="bk_removedelegateews"> </a></span></span>

## <a name="remove-delegates-by-using-ews"></a><span data-ttu-id="27672-142">Entfernen von Stellvertretungen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="27672-142">Remove delegates by using EWS</span></span>

<span data-ttu-id="27672-143">Sie können Delegaten aus einem Postfach mithilfe des [RemoveDelegate](https://msdn.microsoft.com/library/1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a%28Office.15%29.aspx) -EWS-Vorgangs entfernen.</span><span class="sxs-lookup"><span data-stu-id="27672-143">You can remove delegates from a mailbox by using the [RemoveDelegate](https://msdn.microsoft.com/library/1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="27672-144">In diesem Beispiel werden die im [Beispiel zum Hinzufügen eines Stellvertreters](#bk_adddelegateews) festgelegten Stell Vertretungs Berechtigungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="27672-144">In this example, the delegate permissions set in the [add a delegate example](#bk_adddelegateews) are removed.</span></span> 
  
<span data-ttu-id="27672-145">Dies ist auch die XML-Anforderung, die der verwaltete EWS-API sendet, wenn Sie die **RemoveDelegates** -Methode verwenden, um [Stellvertretungen zu entfernen](#bk_removedelegateewsma).</span><span class="sxs-lookup"><span data-stu-id="27672-145">This is also the XML request that the EWS Managed API sends when you use the **RemoveDelegates** method to [remove delegates](#bk_removedelegateewsma).</span></span>
  
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

<span data-ttu-id="27672-146">Der Server antwortet auf die **RemoveDelegate** -Anforderung mit einer [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die Stellvertretungen erfolgreich entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="27672-146">The server responds to the **RemoveDelegate** request with a [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the delegates were successfully removed.</span></span>

<span data-ttu-id="27672-147"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="27672-147"><a name="bk_nextsteps"> </a></span></span>

## <a name="next-steps"></a><span data-ttu-id="27672-148">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="27672-148">Next steps</span></span>

<span data-ttu-id="27672-149">Nachdem Sie Stellvertretungen zu Kalender-, e-Mail-und Aufgabenordnern hinzugefügt haben, kann die Stellvertretung auf die Elemente in den Ordnern zugreifen.</span><span class="sxs-lookup"><span data-stu-id="27672-149">After you add delegates to calendar, email, and task folders, the delegate can access the items in the folders.</span></span> <span data-ttu-id="27672-150">Weitere Informationen finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="27672-150">To learn more, see the following articles:</span></span>
  
- [<span data-ttu-id="27672-151">Zugreifen auf E-Mails als Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="27672-151">Access email as a delegate by using EWS in Exchange</span></span>](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="27672-152">Zugriff auf einen Kalender als Delegat mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="27672-152">Access a calendar as a delegate by using EWS in Exchange</span></span>](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="27672-153">Zugriff auf Kontakte als Delegat mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="27672-153">Access contacts as a delegate by using EWS in Exchange</span></span>](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
<span data-ttu-id="27672-154">Wenn es sich bei den Ordnern, für die Sie Delegaten hinzugefügt haben, um untergeordnete Ordner handelt, die erstellt wurden, bevor Sie dem Stellvertreter Zugriff erteilt haben, kann der Stellvertreter nicht ohne zusätzliche Berechtigungen auf diese Ordner zugreifen.</span><span class="sxs-lookup"><span data-stu-id="27672-154">If the folders for which you added delegates include child folders that were created before you granted the delegate access, the delegate will not be able to access those folders without additional permissions.</span></span> <span data-ttu-id="27672-155">Informationen zum Hinzufügen dieser Berechtigungen oder zum Ändern von Berechtigungen für andere Ordner finden Sie unter [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe von EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="27672-155">To add these permissions, or modify permissions for any other folders, see [Set folder permissions for another user by using EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="27672-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27672-156">See also</span></span>

- [<span data-ttu-id="27672-157">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="27672-157">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
- [<span data-ttu-id="27672-158">Exchange 2013: Programmgesteuertes Hinzufügen von Delegate-Benutzern zu einem e-Mail-Konto</span><span class="sxs-lookup"><span data-stu-id="27672-158">Exchange 2013: Add delegate users to an email account programmatically</span></span>](https://code.msdn.microsoft.com/exchange/Exchange-2013-Adding-1024511f)   
- [<span data-ttu-id="27672-159">Exchange 2013: Programmgesteuertes Aktualisieren von Stellvertretungen für e-Mail-Konten</span><span class="sxs-lookup"><span data-stu-id="27672-159">Exchange 2013: Update delegates associated with email accounts programmatically</span></span>](https://code.msdn.microsoft.com/exchange/Exchange-2013-Update-b40d3bac)   
- [<span data-ttu-id="27672-160">Exchange 2013: Programmgesteuertes Entfernen von Stellvertretern für e-Mail-Konten</span><span class="sxs-lookup"><span data-stu-id="27672-160">Exchange 2013: Remove delegates associated with email accounts programmatically</span></span>](https://code.msdn.microsoft.com/exchange/Exchange-2013-Remove-686f7714)
    

