---
title: Abrufen von Raumlisten mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 15980e4a-e41c-4194-829a-cadbdf365bf1
description: In diesem Artikel erfahren Sie, wie Sie eine Liste aller Raumlisten in Ihrer Organisation oder eine einzelne Raumliste von einem Exchange-Server mithilfe der verwaltete EWS-API oder EWS abrufen.
localization_priority: Priority
ms.openlocfilehash: 7c571b0550f861552cdbe8c5b30138101c9fc788
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455793"
---
# <a name="get-room-lists-by-using-ews-in-exchange"></a><span data-ttu-id="14849-103">Abrufen von Raumlisten mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="14849-103">Get room lists by using EWS in Exchange</span></span>

<span data-ttu-id="14849-104">In diesem Artikel erfahren Sie, wie Sie eine Liste aller Raumlisten in Ihrer Organisation oder eine einzelne Raumliste von einem Exchange-Server mithilfe der verwaltete EWS-API oder EWS abrufen.</span><span class="sxs-lookup"><span data-stu-id="14849-104">Learn how to get a list of all the room lists in your organization or a single room list from an Exchange server by using the EWS Managed API or EWS.</span></span>
  
<span data-ttu-id="14849-105">Sie können die verwaltete EWS-API oder EWS verwenden, um Informationen zu den Räumen zu erhalten und zu erfahren, wie die Räume in Ihrer Organisation gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="14849-105">You can use the EWS Managed API or EWS to get information about rooms and how the rooms are grouped in your organization.</span></span> <span data-ttu-id="14849-106">Raumlisten sind standardmäßig nicht vorhanden; Ihr Administrator muss diese erstellen und organisieren.</span><span class="sxs-lookup"><span data-stu-id="14849-106">Room lists don't exist by default; your administrator needs to create and organize them.</span></span> <span data-ttu-id="14849-107">Normalerweise sind Sie nach Standort oder Abteilung organisiert, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="14849-107">Typically, they're organized by location or department, as shown in the following example.</span></span>
  
<span data-ttu-id="14849-108">**Namen und e-Mail-Adressen von Contoso Room List**</span><span class="sxs-lookup"><span data-stu-id="14849-108">**Contoso room list names and email addresses**</span></span>

|<span data-ttu-id="14849-109">**Name der Raumliste**</span><span class="sxs-lookup"><span data-stu-id="14849-109">**Name of room list**</span></span>|<span data-ttu-id="14849-110">**E-Mail-Adresse der Raumliste**</span><span class="sxs-lookup"><span data-stu-id="14849-110">**Email address of room list**</span></span>|
|:-----|:-----|
|<span data-ttu-id="14849-111">Erstellen von 11 Raumlisten</span><span class="sxs-lookup"><span data-stu-id="14849-111">Building 11 room list</span></span>  <br/> |<span data-ttu-id="14849-112">Bldg11rooms@contoso.com</span><span class="sxs-lookup"><span data-stu-id="14849-112">Bldg11rooms@contoso.com</span></span>  <br/> |
|<span data-ttu-id="14849-113">Health Science Building Konferenzraum Liste</span><span class="sxs-lookup"><span data-stu-id="14849-113">Health Science Building Conference Room List</span></span>  <br/> |<span data-ttu-id="14849-114">HSbldgrooms@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="14849-114">HSbldgrooms@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="14849-115">Besprechungsräume für die Buchhaltung</span><span class="sxs-lookup"><span data-stu-id="14849-115">Accounting Floor Meeting Rooms</span></span>  <br/> |<span data-ttu-id="14849-116">Acctfloor300@contoso.com</span><span class="sxs-lookup"><span data-stu-id="14849-116">Acctfloor300@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="14849-117">Jedem Raum in einer Raumliste ist ein Name und eine e-Mail-Adresse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="14849-117">Each room in a room list has a name and email address associated with it.</span></span>
  
<span data-ttu-id="14849-118">**Namen und e-Mail-Adressen des Contoso-Raums**</span><span class="sxs-lookup"><span data-stu-id="14849-118">**Contoso room names and email addresses**</span></span>

|<span data-ttu-id="14849-119">**Name des Raums**</span><span class="sxs-lookup"><span data-stu-id="14849-119">**Name of room**</span></span>|<span data-ttu-id="14849-120">**E-Mail-Adresse des Raums**</span><span class="sxs-lookup"><span data-stu-id="14849-120">**Email address of room**</span></span>|
|:-----|:-----|
|<span data-ttu-id="14849-121">Conf Room 11/101 (8) AV</span><span class="sxs-lookup"><span data-stu-id="14849-121">Conf Room 11/101 (8) AV</span></span>  <br/> |<span data-ttu-id="14849-122">Cf11101@contoso.com</span><span class="sxs-lookup"><span data-stu-id="14849-122">Cf11101@contoso.com</span></span>  <br/> |
|<span data-ttu-id="14849-123">HS-demonstrationslabor (100)</span><span class="sxs-lookup"><span data-stu-id="14849-123">HS Demonstration Lab (100)</span></span>  <br/> |<span data-ttu-id="14849-124">Hs101@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="14849-124">Hs101@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="14849-125">Buchhaltung 305 WB</span><span class="sxs-lookup"><span data-stu-id="14849-125">Accounting 305 WB</span></span>  <br/> |<span data-ttu-id="14849-126">Acct305@contoso.com</span><span class="sxs-lookup"><span data-stu-id="14849-126">Acct305@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="14849-127">Sie können eine Liste abrufen, die alle Raumlisten enthält, indem Sie entweder die [Datei "ExchangeService. GetRoomLists](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode oder den [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) -EWS-Vorgang verwenden.</span><span class="sxs-lookup"><span data-stu-id="14849-127">You can get a list that contains all room lists by using either the [ExchangeService.GetRoomLists](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) EWS operation.</span></span> 
  
<span data-ttu-id="14849-128">Sie können eine einzelne Raumliste abrufen, die alle Räume für einen Standort oder eine Abteilung enthält, indem Sie Ihre e-Mail-Adresse mithilfe der [getrooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode oder der [getrooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) -EWS-Operation angeben.</span><span class="sxs-lookup"><span data-stu-id="14849-128">You can retrieve a single room list that contains all the rooms for a location or department by supplying its email address by using the [GetRooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="14849-129">Wenn Sie eine Sammlung von Räumen haben, die einer Raumliste zugeordnet sind, können Sie die Sammlung durchsuchen, um den gewünschten Raum oder die Räume zu identifizieren, entweder per e-Mail-Adresse oder nach Schlüsselwörtern im Namen, beispielsweise "AV" oder "Lab".</span><span class="sxs-lookup"><span data-stu-id="14849-129">When you have a collection of rooms associated with a room list, you can then search through the collection to identify the room or rooms you want, either by email address, or by looking for key words in the name, such as "AV", or "Lab".</span></span> 
  
## <a name="get-all-room-lists-by-using-the-ews-managed-api"></a><span data-ttu-id="14849-130">Abrufen aller Raumlisten mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="14849-130">Get all room lists by using the EWS Managed API</span></span>
<span data-ttu-id="14849-131"><a name="bk_GetRoomListewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="14849-131"><a name="bk_GetRoomListewsma"> </a></span></span>

<span data-ttu-id="14849-132">Im folgenden Beispiel wird gezeigt, wie Sie mithilfe der [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) -Methode eine Liste mit allen Raumlisten in Ihrer Organisation abrufen.</span><span class="sxs-lookup"><span data-stu-id="14849-132">The following example shows how to get a list that contains all the room lists in your organization by using the [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) method.</span></span> 
  
<span data-ttu-id="14849-133">In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="14849-133">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

## <a name="get-all-room-lists-by-using-ews"></a><span data-ttu-id="14849-134">Abrufen aller Raumlisten mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="14849-134">Get all room lists by using EWS</span></span>
<span data-ttu-id="14849-135"><a name="bk_GetRoomListews"> </a></span><span class="sxs-lookup"><span data-stu-id="14849-135"><a name="bk_GetRoomListews"> </a></span></span>

<span data-ttu-id="14849-136">Im folgenden Beispiel wird gezeigt, wie eine Auflistung aller [RoomLists](https://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) Ihrer Organisation mithilfe des [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) -Vorgangs abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="14849-136">The following example shows how to get a collection of all your organization's [RoomLists](https://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) by using the [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="14849-137">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API zum [Abrufen aller Raumlisten](#bk_GetRoomListewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="14849-137">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all room lists](#bk_GetRoomListewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="14849-138">Der Server antwortet auf die [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) -Anforderung mit einer [GetRoomListsResponse](https://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) -Nachricht, die die Raumlisten für Ihre Organisation enthält.</span><span class="sxs-lookup"><span data-stu-id="14849-138">The server responds to the [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) request with a [GetRoomListsResponse](https://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) message that contains the room lists for your organization.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="868" MinorBuildNumber="8" Version="V2_9" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomListsResponse ResponseClass="Success" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-the-ews-managed-api"></a><span data-ttu-id="14849-139">Abrufen aller Räume in einer Raumliste mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="14849-139">Get all the rooms in a room list by using the EWS Managed API</span></span>
<span data-ttu-id="14849-140"><a name="bk_FindRoomewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="14849-140"><a name="bk_FindRoomewsma"> </a></span></span>

<span data-ttu-id="14849-141">Im folgenden Beispiel wird gezeigt, wie eine Auflistung von Räumen in einer Raumliste mithilfe der [getrooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) -Methode abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="14849-141">The following example shows how to get a collection of rooms in a room list by using the [GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) method.</span></span> 
  
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-ews"></a><span data-ttu-id="14849-142">Abrufen aller Räume in einer Raumliste mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="14849-142">Get all the rooms in a room list by using EWS</span></span>
<span data-ttu-id="14849-143"><a name="bk_FindRoomews"> </a></span><span class="sxs-lookup"><span data-stu-id="14849-143"><a name="bk_FindRoomews"> </a></span></span>

<span data-ttu-id="14849-144">Im folgenden Beispiel wird gezeigt, wie Sie eine Liste von [Räumen](https://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) in einer [RoomList](https://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) mithilfe der [getrooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) -Operation abrufen.</span><span class="sxs-lookup"><span data-stu-id="14849-144">The following example shows how to get a list of [rooms](https://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) in a [RoomList](https://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) by using the [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="14849-145">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API verwenden, um [Alle Räume in einer Raumliste abzurufen](#bk_FindRoomewsma).</span><span class="sxs-lookup"><span data-stu-id="14849-145">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all the rooms in a room list](#bk_FindRoomewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="14849-146">Der Server antwortet auf die [getrooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) -Anforderung mit einer [GetRoomsResponse](https://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) -Nachricht, die die Chatrooms in der Raumliste enthält.</span><span class="sxs-lookup"><span data-stu-id="14849-146">The server responds to the [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) request with a [GetRoomsResponse](https://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) message that contains the rooms in the room list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="873" MinorBuildNumber="9" 
                         Version="V2_9" xmlns:h="http://scemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomsResponse ResponseClass="Success" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
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

## <a name="see-also"></a><span data-ttu-id="14849-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14849-147">See also</span></span>


- [<span data-ttu-id="14849-148">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="14849-148">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="14849-149">Abrufen von Frei/Gebucht-Informationen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="14849-149">Get free/busy information by using EWS in Exchange</span></span>](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="14849-150">Erstellen und Verwalten von Raumpostfächern</span><span class="sxs-lookup"><span data-stu-id="14849-150">Create and Manage Room Mailboxes</span></span>](https://technet.microsoft.com/library/jj215781%28v=exchg.150%29.aspx)
    

