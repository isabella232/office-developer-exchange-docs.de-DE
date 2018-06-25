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
# <a name="get-room-lists-by-using-ews-in-exchange"></a>Rufen Sie Raumlisten mithilfe von EWS in Exchange ab

Erfahren Sie, wie eine Liste mit den Chatroom Listen in Ihrer Organisation oder eine einzelne Raumliste von einem Exchange-Server mithilfe des EWS Managed API oder EWS erhalten möchten.
  
Sie können die EWS Managed API oder EWS zum Abrufen von Informationen zu Chatrooms und wie die Chatrooms in Ihrer Organisation gruppiert werden. Raumlisten vorhanden nicht standardmäßig. der Administrator muss erstellen und zu organisieren. In der Regel sind nach Standort oder Abteilung, organisiert, wie im folgenden Beispiel dargestellt.
  
**Auflisten von Contoso Raum-Namen und e-Mail-Adressen**

|**Name der Raumliste**|**E-Mail-Adresse des Raumliste**|
|:-----|:-----|
|Erstellen von 11 Raumliste  <br/> |Bldg11rooms@contoso.com  <br/> |
|Integrität Science Building Konferenz Raumliste  <br/> |HSbldgrooms@contoso.edu  <br/> |
|Floor-Besprechungsräumen Buchhaltung  <br/> |Acctfloor300@contoso.com  <br/> |
   
Jeder Chatroom in eine Raumliste weist eine Name und e-Mail-Adresse zugeordnet.
  
**Contoso Raum Namen und e-Mail-Adressen**

|**Name des Raums**|**E-Mail-Adresse des Raums**|
|:-----|:-----|
|Conf Raum 11/101 (8) Audio-Video  <br/> |Cf11101@contoso.com  <br/> |
|HS Demo Lab (100)  <br/> |Hs101@contoso.edu  <br/> |
|Accounting 305 WB  <br/> |Acct305@contoso.com  <br/> |
   
Sie können eine Liste abrufen, die alle Chatroom-Listen enthält, mithilfe der [ExchangeService.GetRoomLists](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) EWS Managed API-Methode oder die [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) EWS-Vorgang. 
  
Sie können eine einzelne Raumliste abrufen, die alle Chatrooms für einen Standort oder eine Abteilung durch Bereitstellen der e-Mail-Adresse mithilfe der [GetRooms](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) EWS Managed API-Methode oder die [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) EWS-Vorgang enthält. Wenn Sie eine Auflistung von Chatrooms, die eine Raumliste zugeordnet haben, können Sie dann durch die Auflistung zum Identifizieren der Raum- oder Chatrooms gewünschten, indem e-Mail-Adresse, oder suchen Sie nach Schlüsselwörtern in der Name, beispielsweise "AV" oder "Lab" suchen. 
  
## <a name="get-all-room-lists-by-using-the-ews-managed-api"></a>Rufen Sie alle Chatroom-Listen ab, indem Sie die EWS Managed API
<a name="bk_GetRoomListewsma"> </a>

Im folgenden Beispiel wird gezeigt, wie eine Liste abrufen, die alle Chatroom-Listen in Ihrer Organisation mithilfe der [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) -Methode enthält. 
  
In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. 
  
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

## <a name="get-all-room-lists-by-using-ews"></a>Rufen Sie aller Raumlisten mithilfe der Exchange-Webdienste ab
<a name="bk_GetRoomListews"> </a>

Im folgenden Beispiel wird gezeigt, wie eine Auflistung von Ihrer Organisation [RoomLists](http://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) mithilfe des Vorgangs [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) abrufen. Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Abrufen aller Raumlisten](#bk_GetRoomListewsma)verwenden.
  
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

Der Server antwortet auf die Anforderung [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) mit einer [GetRoomListsResponse](http://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) -Nachricht, die Listen Platz für Ihre Organisation enthält. 
  
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-the-ews-managed-api"></a>Rufen Sie alle Chatrooms in eine Raumliste ab, indem Sie die EWS Managed API
<a name="bk_FindRoomewsma"> </a>

Im folgenden Beispiel wird gezeigt, wie eine Auflistung von Chatrooms in eine Raumliste mithilfe der [GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) -Methode abrufen. 
  
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-ews"></a>Rufen Sie aller Chatrooms in eine Raumliste mithilfe der Exchange-Webdienste ab
<a name="bk_FindRoomews"> </a>

Im folgenden Beispiel wird gezeigt, wie eine Liste von [Chatrooms](http://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) mithilfe von [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) -Vorgang in einem [RoomList](http://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) abrufen. Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Abrufen aller Chatrooms in eine Raumliste](#bk_FindRoomewsma)verwenden.
  
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

Der Server antwortet auf die Anforderung [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) mit einer [GetRoomsResponse](http://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) -Nachricht, die die Räume in der Raumliste enthält. 
  
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

## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Abrufen von Frei/Gebucht-Informationen mithilfe von EWS in Exchange](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [Erstellen und Verwalten von Raumpostfächern](http://technet.microsoft.com/en-us/library/jj215781%28v=exchg.150%29.aspx)
    

