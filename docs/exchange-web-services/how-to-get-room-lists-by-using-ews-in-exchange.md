---
title: Rufen Sie Raumlisten mithilfe von EWS in Exchange ab
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 15980e4a-e41c-4194-829a-cadbdf365bf1
description: Erfahren Sie, wie eine Liste mit den Chatroom Listen in Ihrer Organisation oder eine einzelne Raumliste von einem Exchange-Server mithilfe des EWS Managed API oder EWS erhalten möchten.
ms.openlocfilehash: 404a31fb6c8d98bdbba4c79ed6912c333a44d04b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756895"
---
# <a name="get-room-lists-by-using-ews-in-exchange"></a><span data-ttu-id="1101d-103">Rufen Sie Raumlisten mithilfe von EWS in Exchange ab</span><span class="sxs-lookup"><span data-stu-id="1101d-103">Get room lists by using EWS in Exchange</span></span>

<span data-ttu-id="1101d-104">Erfahren Sie, wie eine Liste mit den Chatroom Listen in Ihrer Organisation oder eine einzelne Raumliste von einem Exchange-Server mithilfe des EWS Managed API oder EWS erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="1101d-104">Learn how to get a list of all the room lists in your organization or a single room list from an Exchange server by using the EWS Managed API or EWS.</span></span>
  
<span data-ttu-id="1101d-105">Sie können die EWS Managed API oder EWS zum Abrufen von Informationen zu Chatrooms und wie die Chatrooms in Ihrer Organisation gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="1101d-105">You can use the EWS Managed API or EWS to get information about rooms and how the rooms are grouped in your organization.</span></span> <span data-ttu-id="1101d-106">Raumlisten vorhanden nicht standardmäßig. der Administrator muss erstellen und zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="1101d-106">Room lists don't exist by default; your administrator needs to create and organize them.</span></span> <span data-ttu-id="1101d-107">In der Regel sind nach Standort oder Abteilung, organisiert, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1101d-107">Typically, they're organized by location or department, as shown in the following example.</span></span>
  
<span data-ttu-id="1101d-108">**Auflisten von Contoso Raum-Namen und e-Mail-Adressen**</span><span class="sxs-lookup"><span data-stu-id="1101d-108">**Contoso room list names and email addresses**</span></span>

|<span data-ttu-id="1101d-109">**Name der Raumliste**</span><span class="sxs-lookup"><span data-stu-id="1101d-109">**Name of room list**</span></span>|<span data-ttu-id="1101d-110">**E-Mail-Adresse des Raumliste**</span><span class="sxs-lookup"><span data-stu-id="1101d-110">**Email address of room list**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1101d-111">Erstellen von 11 Raumliste</span><span class="sxs-lookup"><span data-stu-id="1101d-111">Building 11 room list</span></span>  <br/> |<span data-ttu-id="1101d-112">Bldg11rooms@contoso.com</span><span class="sxs-lookup"><span data-stu-id="1101d-112">Bldg11rooms@contoso.com</span></span>  <br/> |
|<span data-ttu-id="1101d-113">Integrität Science Building Konferenz Raumliste</span><span class="sxs-lookup"><span data-stu-id="1101d-113">Health Science Building Conference Room List</span></span>  <br/> |<span data-ttu-id="1101d-114">HSbldgrooms@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="1101d-114">HSbldgrooms@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="1101d-115">Floor-Besprechungsräumen Buchhaltung</span><span class="sxs-lookup"><span data-stu-id="1101d-115">Accounting Floor Meeting Rooms</span></span>  <br/> |<span data-ttu-id="1101d-116">Acctfloor300@contoso.com</span><span class="sxs-lookup"><span data-stu-id="1101d-116">Acctfloor300@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="1101d-117">Jeder Chatroom in eine Raumliste weist eine Name und e-Mail-Adresse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1101d-117">Each room in a room list has a name and email address associated with it.</span></span>
  
<span data-ttu-id="1101d-118">**Contoso Raum Namen und e-Mail-Adressen**</span><span class="sxs-lookup"><span data-stu-id="1101d-118">**Contoso room names and email addresses**</span></span>

|<span data-ttu-id="1101d-119">**Name des Raums**</span><span class="sxs-lookup"><span data-stu-id="1101d-119">**Name of room**</span></span>|<span data-ttu-id="1101d-120">**E-Mail-Adresse des Raums**</span><span class="sxs-lookup"><span data-stu-id="1101d-120">**Email address of room**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1101d-121">Conf Raum 11/101 (8) Audio-Video</span><span class="sxs-lookup"><span data-stu-id="1101d-121">Conf Room 11/101 (8) AV</span></span>  <br/> |<span data-ttu-id="1101d-122">Cf11101@contoso.com</span><span class="sxs-lookup"><span data-stu-id="1101d-122">Cf11101@contoso.com</span></span>  <br/> |
|<span data-ttu-id="1101d-123">HS Demo Lab (100)</span><span class="sxs-lookup"><span data-stu-id="1101d-123">HS Demonstration Lab (100)</span></span>  <br/> |<span data-ttu-id="1101d-124">Hs101@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="1101d-124">Hs101@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="1101d-125">Accounting 305 WB</span><span class="sxs-lookup"><span data-stu-id="1101d-125">Accounting 305 WB</span></span>  <br/> |<span data-ttu-id="1101d-126">Acct305@contoso.com</span><span class="sxs-lookup"><span data-stu-id="1101d-126">Acct305@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="1101d-127">Sie können eine Liste abrufen, die alle Chatroom-Listen enthält, mithilfe der [ExchangeService.GetRoomLists](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) EWS Managed API-Methode oder die [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1101d-127">You can get a list that contains all room lists by using either the [ExchangeService.GetRoomLists](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) EWS operation.</span></span> 
  
<span data-ttu-id="1101d-128">Sie können eine einzelne Raumliste abrufen, die alle Chatrooms für einen Standort oder eine Abteilung durch Bereitstellen der e-Mail-Adresse mithilfe der [GetRooms](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) EWS Managed API-Methode oder die [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) EWS-Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="1101d-128">You can retrieve a single room list that contains all the rooms for a location or department by supplying its email address by using the [GetRooms](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="1101d-129">Wenn Sie eine Auflistung von Chatrooms, die eine Raumliste zugeordnet haben, können Sie dann durch die Auflistung zum Identifizieren der Raum- oder Chatrooms gewünschten, indem e-Mail-Adresse, oder suchen Sie nach Schlüsselwörtern in der Name, beispielsweise "AV" oder "Lab" suchen.</span><span class="sxs-lookup"><span data-stu-id="1101d-129">When you have a collection of rooms associated with a room list, you can then search through the collection to identify the room or rooms you want, either by email address, or by looking for key words in the name, such as "AV", or "Lab".</span></span> 
  
## <a name="get-all-room-lists-by-using-the-ews-managed-api"></a><span data-ttu-id="1101d-130">Rufen Sie alle Chatroom-Listen ab, indem Sie die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="1101d-130">Get all room lists by using the EWS Managed API</span></span>
<span data-ttu-id="1101d-131"><a name="bk_GetRoomListewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="1101d-131"></span></span>

<span data-ttu-id="1101d-132">Im folgenden Beispiel wird gezeigt, wie eine Liste abrufen, die alle Chatroom-Listen in Ihrer Organisation mithilfe der [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) -Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="1101d-132">The following example shows how to get a list that contains all the room lists in your organization by using the [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) method.</span></span> 
  
<span data-ttu-id="1101d-133">In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="1101d-133">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
// Return all the room lists in the organization.
// This method call results in a GetRoomLists call to EWS.
EmailAddressCollection myRoomLists = service.GetRoomLists();
// Display the room lists.
foreach (EmailAddress address in myRoomLists)
{
    Console.WriteLine("Email Address: {0} Mailbox Type: {1}", address.Address, address.MailboxType);
}

```

## <a name="get-all-room-lists-by-using-ews"></a><span data-ttu-id="1101d-134">Rufen Sie aller Raumlisten mithilfe der Exchange-Webdienste ab</span><span class="sxs-lookup"><span data-stu-id="1101d-134">Get all room lists by using EWS</span></span>
<span data-ttu-id="1101d-135"><a name="bk_GetRoomListews"> </a></span><span class="sxs-lookup"><span data-stu-id="1101d-135"></span></span>

<span data-ttu-id="1101d-136">Im folgenden Beispiel wird gezeigt, wie eine Auflistung von Ihrer Organisation [RoomLists](http://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) mithilfe des Vorgangs [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) abrufen.</span><span class="sxs-lookup"><span data-stu-id="1101d-136">The following example shows how to get a collection of all your organization's [RoomLists](http://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) by using the [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="1101d-137">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Abrufen aller Raumlisten](#bk_GetRoomListewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="1101d-137">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all room lists](#bk_GetRoomListewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="1101d-138">Der Server antwortet auf die Anforderung [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) mit einer [GetRoomListsResponse](http://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) -Nachricht, die Listen Platz für Ihre Organisation enthält.</span><span class="sxs-lookup"><span data-stu-id="1101d-138">The server responds to the [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) request with a [GetRoomListsResponse](http://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) message that contains the room lists for your organization.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="868" MinorBuildNumber="8" Version="V2_9" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomListsResponse ResponseClass="Success" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:RoomLists>
        <t:Address>
          <t:Name>Contoso Building 1 Room List</t:Name>
          <t:EmailAddress>bldg1rooms@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
        <t:Address>
          <t:Name>Contoso Building 2 Room List</t:Name>
          <t:EmailAddress>bldg2rooms@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
        <t:Address>
          <t:Name>Contoso Building 3 Room List</t:Name>
          <t:EmailAddress>bldg3rooms@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
      </m:RoomLists>
    </m:GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="get-all-the-rooms-in-a-room-list-by-using-the-ews-managed-api"></a><span data-ttu-id="1101d-139">Rufen Sie alle Chatrooms in eine Raumliste ab, indem Sie die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="1101d-139">Get all the rooms in a room list by using the EWS Managed API</span></span>
<span data-ttu-id="1101d-140"><a name="bk_FindRoomewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="1101d-140"></span></span>

<span data-ttu-id="1101d-141">Im folgenden Beispiel wird gezeigt, wie eine Auflistung von Chatrooms in eine Raumliste mithilfe der [GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="1101d-141">The following example shows how to get a collection of rooms in a room list by using the [GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) method.</span></span> 
  
```cs
EmailAddress myRoomList = "bldg3rooms@contoso.com";
// This method call results in a GetRooms call to EWS.
System.Collections.ObjectModel.Collection<EmailAddress> myRoomAddresses = service.GetRooms(myRoomList);
// Display the individual rooms.
foreach (EmailAddress address in myRoomAddresses)
{
    Console.WriteLine("Email Address: {0}", address.Address);
}

```

## <a name="get-all-the-rooms-in-a-room-list-by-using-ews"></a><span data-ttu-id="1101d-142">Rufen Sie aller Chatrooms in eine Raumliste mithilfe der Exchange-Webdienste ab</span><span class="sxs-lookup"><span data-stu-id="1101d-142">Get all the rooms in a room list by using EWS</span></span>
<span data-ttu-id="1101d-143"><a name="bk_FindRoomews"> </a></span><span class="sxs-lookup"><span data-stu-id="1101d-143"></span></span>

<span data-ttu-id="1101d-144">Im folgenden Beispiel wird gezeigt, wie eine Liste von [Chatrooms](http://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) mithilfe von [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) -Vorgang in einem [RoomList](http://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) abrufen.</span><span class="sxs-lookup"><span data-stu-id="1101d-144">The following example shows how to get a list of [rooms](http://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) in a [RoomList](http://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) by using the [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="1101d-145">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Abrufen aller Chatrooms in eine Raumliste](#bk_FindRoomewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="1101d-145">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all the rooms in a room list](#bk_FindRoomewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetRooms>
      <m:RoomList>
        <t:EmailAddress>bldg3rooms@contoso.com</t:EmailAddress>
      </m:RoomList>
    </m:GetRooms>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="1101d-146">Der Server antwortet auf die Anforderung [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) mit einer [GetRoomsResponse](http://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) -Nachricht, die die Räume in der Raumliste enthält.</span><span class="sxs-lookup"><span data-stu-id="1101d-146">The server responds to the [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) request with a [GetRoomsResponse](http://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) message that contains the rooms in the room list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="873" MinorBuildNumber="9" 
                         Version="V2_9" xmlns:h="http://scemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomsResponse ResponseClass="Success" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://scemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:Rooms>
        <t:Room>
          <t:Id>
            <t:Name>Conf Room 3/101 (16) AV</t:Name>
            <t:EmailAddress>cf3101@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room>
          <t:Id>
            <t:Name>Conf Room 3/102 (8) AV</t:Name>
            <t:EmailAddress>cf3102@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room>
          <t:Id>
            <t:Name>Conf Room 3/103 (14) AV RoundTable</t:Name>
            <t:EmailAddress>cf3103@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
      </m:Rooms>
    </m:GetRoomsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="1101d-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1101d-147">See also</span></span>


- [<span data-ttu-id="1101d-148">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1101d-148">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="1101d-149">Abrufen von Frei/Gebucht-Informationen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1101d-149">Get free/busy information by using EWS in Exchange</span></span>](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="1101d-150">Erstellen und Verwalten von Raumpostfächern</span><span class="sxs-lookup"><span data-stu-id="1101d-150">Create and Manage Room Mailboxes</span></span>](http://technet.microsoft.com/en-us/library/jj215781%28v=exchg.150%29.aspx)
    

