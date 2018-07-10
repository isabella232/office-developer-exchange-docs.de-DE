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
# <a name="add-and-remove-delegates-by-using-ews-in-exchange"></a><span data-ttu-id="96bef-103">Hinzufügen und Entfernen von Stellvertretungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="96bef-103">Add and remove delegates by using EWS in Exchange</span></span>

<span data-ttu-id="96bef-104">Erfahren Sie, wie Stellvertretungen auf Hinzufügen oder Entfernen von Stellvertretungen aus den Postfächern der Benutzer verwenden die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="96bef-104">Learn how to add delegates to or remove delegates from users' mailboxes by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="96bef-105">Sie können die EWS Managed API oder EWS verwenden, um Delegaten Zustimmung des Besitzers des Zielpostfachs oder Entfernen eines Stellvertreters Zugriff auf ein Postfach zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="96bef-105">You can use the EWS Managed API or EWS to enable delegates to act on behalf of a mailbox owner or remove a delegate's access to a mailbox.</span></span> <span data-ttu-id="96bef-106">Benutzer, die eine Stellvertretung hinzugefügt wurden, und erhalten Berechtigungen können im Namen der Postfachbesitzer Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="96bef-106">Users who are added as a delegate, and are given permissions, can perform tasks on behalf of the mailbox owner.</span></span> <span data-ttu-id="96bef-107">Sie können beispielsweise erstellen und Senden von Besprechungsanfragen, e-Mails senden und Antworten auf Besprechungsanfragen im Auftrag des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="96bef-107">For example, they can create and send meeting invitations, send emails, and respond to meeting requests on the mailbox owner's behalf.</span></span> 
  
<span data-ttu-id="96bef-108">**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge zum Hinzufügen und Entfernen von Stellvertretungen**</span><span class="sxs-lookup"><span data-stu-id="96bef-108">**Table 1. EWS Managed API methods and EWS operations for adding and removing delegates**</span></span>

|<span data-ttu-id="96bef-109">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="96bef-109">**Task**</span></span>|<span data-ttu-id="96bef-110">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="96bef-110">**EWS Managed API method**</span></span>|<span data-ttu-id="96bef-111">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="96bef-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="96bef-112">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="96bef-112">Add delegates</span></span>  <br/> |[<span data-ttu-id="96bef-113">ExchangeService.AddDelegates</span><span class="sxs-lookup"><span data-stu-id="96bef-113">ExchangeService.AddDelegates</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="96bef-114">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="96bef-114">AddDelegate</span></span>](http://msdn.microsoft.com/library/646fb994-229e-4d90-8b95-6541191cb3ae%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="96bef-115">Entfernen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="96bef-115">Remove delegates</span></span>  <br/> |[<span data-ttu-id="96bef-116">ExchangeService.RemoveDelegates</span><span class="sxs-lookup"><span data-stu-id="96bef-116">ExchangeService.RemoveDelegates</span></span>](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="96bef-117">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="96bef-117">RemoveDelegate</span></span>](http://msdn.microsoft.com/library/f21c5171-62e7-47c8-99b1-22e1ff5883bb%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="96bef-118">Nachdem eine Stellvertretung Berechtigungen für einen Ordner gewährt wurde, können sie gemäß ihren [Delegieren von Berechtigungen](delegate-access-and-ews-in-exchange.md#bk_delegateperms)für Elemente im Ordner und alle Unterordner fungieren.</span><span class="sxs-lookup"><span data-stu-id="96bef-118">After a delegate is granted permissions to a folder, they can act on items in the folder and any subfolders, according to their [delegate permissions](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span></span> <span data-ttu-id="96bef-119">Berechtigungen für Stellvertretungen gelten nur für Unterordner, die erstellt werden, nachdem der Stellvertretungszugriff eingeholt wurde.</span><span class="sxs-lookup"><span data-stu-id="96bef-119">Permissions for delegates only apply to subfolders that are created after the delegate access was granted.</span></span> <span data-ttu-id="96bef-120">Um Ordnerberechtigungen für vorhandenem Ordner oder andere Ordner zu aktualisieren, finden Sie unter [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der Exchange-Webdienste im Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="96bef-120">To update folder permissions for pre-existing folders, or other folders, see [Set folder permissions for another user by using EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="96bef-121">Beachten Sie, dass Delegaten nur postfachaktivierten Konten, einschließlich e-Mail-aktivierte Sicherheitsgruppen hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="96bef-121">Note that delegates can only be added to mailbox-enabled accounts, including mail-enabled security groups.</span></span> <span data-ttu-id="96bef-122">In der Standardeinstellung kann ein einzigen EWS-Delegaten Access Anruf maximal 255 verschiedene Postfächer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="96bef-122">By default, a single EWS delegate access call can access a maximum of 255 different mailboxes.</span></span>

<span data-ttu-id="96bef-123"><a name="bk_adddelegateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="96bef-123"></span></span>

## <a name="add-delegates-by-using-the-ews-managed-api"></a><span data-ttu-id="96bef-124">Hinzufügen von Stellvertretungen mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="96bef-124">Add delegates by using the EWS Managed API</span></span>

<span data-ttu-id="96bef-125">Sie können Delegaten an ein Postfach mithilfe der [AddDelegates](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) EWS Managed API-Methode hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="96bef-125">You can add delegates to a mailbox by using the [AddDelegates](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) EWS Managed API method.</span></span> <span data-ttu-id="96bef-126">In den in diesem Beispiel wird, einen neuen Kalender, Kontakt- und e-Mail- [Beauftragte Benutzer](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.delegateuser%28v=exchg.80%29.aspx) -Objekt erstellt wurde, und jeder Delegaten [Editor-Berechtigungen](delegate-access-and-ews-in-exchange.md#bk_delegateperms) für die entsprechenden Ordner angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="96bef-126">In this example, a new calendar, contact, and email [DelegateUser](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.delegateuser%28v=exchg.80%29.aspx) object is created, and each delegate is given [Editor permissions](delegate-access-and-ews-in-exchange.md#bk_delegateperms) for their respective folder.</span></span> <span data-ttu-id="96bef-127">Sie können das Beispiel eine Stellvertretung hinzu, der die durch die [DelegatePermissions-Eigenschaften](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.delegatepermissions_properties%28v=exchg.80%29.aspx)angegebenen Ordner ändern, und Sie können die Berechtigungen festlegen, um einen der Werte der [DelegateFolderPermissionLevel](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) -Enumeration angegeben.</span><span class="sxs-lookup"><span data-stu-id="96bef-127">You can modify the example to add a delegate to any of the folders specified by the [DelegatePermissions properties](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.delegatepermissions_properties%28v=exchg.80%29.aspx), and you can set the permissions to any of the values specified by the [DelegateFolderPermissionLevel](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) enumeration.</span></span> 
  
<span data-ttu-id="96bef-128">In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Besitzer des Postfachs und der Benutzer wurde an einen Exchange-Server authentifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="96bef-128">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="96bef-129"><a name="bk_adddelegateews"> </a></span><span class="sxs-lookup"><span data-stu-id="96bef-129"></span></span>

## <a name="add-delegates-by-using-ews"></a><span data-ttu-id="96bef-130">Hinzufügen von Stellvertretungen mithilfe von Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="96bef-130">Add delegates by using EWS</span></span>

<span data-ttu-id="96bef-131">Das folgende Codebeispiel veranschaulicht das Hinzufügen separater Kalender, Kontakte und e-Mail-Delegaten mithilfe von [AddDelegate](http://msdn.microsoft.com/library/012d8cc5-648c-4ba0-a155-15c422b1e994%28Office.15%29.aspx) EWS-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="96bef-131">The following code example shows how to add separate calendar, contact, and email delegates by using the [AddDelegate](http://msdn.microsoft.com/library/012d8cc5-648c-4ba0-a155-15c422b1e994%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="96bef-132">So ändern Sie das Postfach vom [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element angegeben ist, und [die berechtigungseinstellungen für jeden Delegaten](delegate-access-and-ews-in-exchange.md#bk_delegateperms) in der [Beauftragte Benutzer](http://msdn.microsoft.com/library/aac4e74e-f69b-4c41-a0c9-489610330fbf%28Office.15%29.aspx) -Element enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="96bef-132">The mailbox to modify is specified by the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element, and the [permission](delegate-access-and-ews-in-exchange.md#bk_delegateperms) settings for each delegate are contained in the [DelegateUser](http://msdn.microsoft.com/library/aac4e74e-f69b-4c41-a0c9-489610330fbf%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="96bef-133">Jeder der Delegaten wurde Editorberechtigungen für ihre Zielordner erteilt.</span><span class="sxs-lookup"><span data-stu-id="96bef-133">Each of the delegates has been granted Editor permissions to their target folder.</span></span> 
  
<span data-ttu-id="96bef-134">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **AddDelegates** -Methode zum [Hinzufügen von Delegaten](#bk_adddelegateewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="96bef-134">This is also the XML request that the EWS Managed API sends when you use the **AddDelegates** method to [add delegates](#bk_adddelegateewsma).</span></span>
  
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

<span data-ttu-id="96bef-135">Der Server antwortet auf die Anforderung **AddDelegate** mit einer [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Stellvertretungen erfolgreich erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="96bef-135">The server responds to the **AddDelegate** request with an [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the delegates were successfully created.</span></span>
  
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

<span data-ttu-id="96bef-136"><a name="bk_removedelegateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="96bef-136"></span></span>

## <a name="remove-delegates-by-using-the-ews-managed-api"></a><span data-ttu-id="96bef-137">Entfernen von Stellvertretungen mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="96bef-137">Remove delegates by using the EWS Managed API</span></span>

<span data-ttu-id="96bef-138">Sie können Delegaten aus einer Zielpostfach mithilfe der [ExchangeService.RemoveDelegates](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) EWS Managed API-Methode entfernen.</span><span class="sxs-lookup"><span data-stu-id="96bef-138">You can remove delegates from a target mailbox by using the [ExchangeService.RemoveDelegates](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) EWS Managed API method.</span></span> <span data-ttu-id="96bef-139">In diesem Beispiel werden die Stellvertretung Berechtigungssatz [Hinzufügen ein Beispiel für einen Delegaten](#bk_adddelegateewsma) entfernt.</span><span class="sxs-lookup"><span data-stu-id="96bef-139">In this example, the delegate permissions set in the [add a delegate example](#bk_adddelegateewsma) are removed.</span></span> 
  
<span data-ttu-id="96bef-140">In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Besitzer des Postfachs und der Benutzer wurde an einen Exchange-Server authentifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="96bef-140">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="96bef-141"><a name="bk_removedelegateews"> </a></span><span class="sxs-lookup"><span data-stu-id="96bef-141"></span></span>

## <a name="remove-delegates-by-using-ews"></a><span data-ttu-id="96bef-142">Entfernen von Stellvertretungen mithilfe von Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="96bef-142">Remove delegates by using EWS</span></span>

<span data-ttu-id="96bef-143">Sie können Delegaten aus einem Postfach mithilfe des [RemoveDelegate](http://msdn.microsoft.com/library/1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a%28Office.15%29.aspx) EWS-Vorgangs entfernen.</span><span class="sxs-lookup"><span data-stu-id="96bef-143">You can remove delegates from a mailbox by using the [RemoveDelegate](http://msdn.microsoft.com/library/1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="96bef-144">In diesem Beispiel werden die Stellvertretung Berechtigungssatz [Hinzufügen ein Beispiel für einen Delegaten](#bk_adddelegateews) entfernt.</span><span class="sxs-lookup"><span data-stu-id="96bef-144">In this example, the delegate permissions set in the [add a delegate example](#bk_adddelegateews) are removed.</span></span> 
  
<span data-ttu-id="96bef-145">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **RemoveDelegates** -Methode zum [Entfernen von Delegaten](#bk_removedelegateewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="96bef-145">This is also the XML request that the EWS Managed API sends when you use the **RemoveDelegates** method to [remove delegates](#bk_removedelegateewsma).</span></span>
  
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

<span data-ttu-id="96bef-146">Der Server antwortet auf die Anforderung **RemoveDelegate** mit einer [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Stellvertretungen erfolgreich entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="96bef-146">The server responds to the **RemoveDelegate** request with a [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the delegates were successfully removed.</span></span>

<span data-ttu-id="96bef-147"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="96bef-147"></span></span>

## <a name="next-steps"></a><span data-ttu-id="96bef-148">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="96bef-148">Next steps</span></span>

<span data-ttu-id="96bef-149">Nachdem Sie Kalender, e-Mail und Aufgabenordner Stellvertretungen hinzufügen, kann die Stellvertretung die Elemente in den Ordnern zugreifen.</span><span class="sxs-lookup"><span data-stu-id="96bef-149">After you add delegates to calendar, email, and task folders, the delegate can access the items in the folders.</span></span> <span data-ttu-id="96bef-150">Finden Sie weitere Informationen finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="96bef-150">To learn more, see the following articles:</span></span>
  
- [<span data-ttu-id="96bef-151">Access-e-Mail eine Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="96bef-151">Access email as a delegate by using EWS in Exchange</span></span>](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="96bef-152">Zugriff auf einen Kalender als Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="96bef-152">Access a calendar as a delegate by using EWS in Exchange</span></span>](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="96bef-153">Access-Kontakte als Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="96bef-153">Access contacts as a delegate by using EWS in Exchange</span></span>](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
<span data-ttu-id="96bef-154">Wenn die Ordner, für die Stellvertretungen hinzugefügt, untergeordneten Ordner, die erstellt wurden enthalten, bevor Sie den Stellvertretungszugriff gewährt, werden die Stellvertretung nicht auf diese Ordner ohne zusätzliche Berechtigungen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="96bef-154">If the folders for which you added delegates include child folders that were created before you granted the delegate access, the delegate will not be able to access those folders without additional permissions.</span></span> <span data-ttu-id="96bef-155">Um diese Berechtigungen hinzufügen oder Ändern von Berechtigungen für alle anderen Ordner, finden Sie unter [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der Exchange-Webdienste im Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="96bef-155">To add these permissions, or modify permissions for any other folders, see [Set folder permissions for another user by using EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="96bef-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96bef-156">See also</span></span>

- [<span data-ttu-id="96bef-157">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="96bef-157">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
- [<span data-ttu-id="96bef-158">Exchange 2013: Hinzufügen Benutzer ein e-Mail-Konto programmgesteuert delegieren</span><span class="sxs-lookup"><span data-stu-id="96bef-158">Exchange 2013: Add delegate users to an email account programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Adding-1024511f)   
- [<span data-ttu-id="96bef-159">Exchange 2013: Aktualisieren von e-Mail-Konten programmgesteuert zugeordnete Delegaten</span><span class="sxs-lookup"><span data-stu-id="96bef-159">Exchange 2013: Update delegates associated with email accounts programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Update-b40d3bac)   
- [<span data-ttu-id="96bef-160">Exchange 2013: Zugeordnete e-Mail-Konten programmgesteuert Delegaten entfernen</span><span class="sxs-lookup"><span data-stu-id="96bef-160">Exchange 2013: Remove delegates associated with email accounts programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Remove-686f7714)
    

