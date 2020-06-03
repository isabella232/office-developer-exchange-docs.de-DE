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
# <a name="get-room-lists-by-using-ews-in-exchange"></a>Abrufen von Raumlisten mithilfe von EWS in Exchange

In diesem Artikel erfahren Sie, wie Sie eine Liste aller Raumlisten in Ihrer Organisation oder eine einzelne Raumliste von einem Exchange-Server mithilfe der verwaltete EWS-API oder EWS abrufen.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um Informationen zu den Räumen zu erhalten und zu erfahren, wie die Räume in Ihrer Organisation gruppiert sind. Raumlisten sind standardmäßig nicht vorhanden; Ihr Administrator muss diese erstellen und organisieren. Normalerweise sind Sie nach Standort oder Abteilung organisiert, wie im folgenden Beispiel dargestellt.
  
**Namen und e-Mail-Adressen von Contoso Room List**

|**Name der Raumliste**|**E-Mail-Adresse der Raumliste**|
|:-----|:-----|
|Erstellen von 11 Raumlisten  <br/> |Bldg11rooms@contoso.com  <br/> |
|Health Science Building Konferenzraum Liste  <br/> |HSbldgrooms@contoso.edu  <br/> |
|Besprechungsräume für die Buchhaltung  <br/> |Acctfloor300@contoso.com  <br/> |
   
Jedem Raum in einer Raumliste ist ein Name und eine e-Mail-Adresse zugeordnet.
  
**Namen und e-Mail-Adressen des Contoso-Raums**

|**Name des Raums**|**E-Mail-Adresse des Raums**|
|:-----|:-----|
|Conf Room 11/101 (8) AV  <br/> |Cf11101@contoso.com  <br/> |
|HS-demonstrationslabor (100)  <br/> |Hs101@contoso.edu  <br/> |
|Buchhaltung 305 WB  <br/> |Acct305@contoso.com  <br/> |
   
Sie können eine Liste abrufen, die alle Raumlisten enthält, indem Sie entweder die [Datei "ExchangeService. GetRoomLists](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode oder den [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) -EWS-Vorgang verwenden. 
  
Sie können eine einzelne Raumliste abrufen, die alle Räume für einen Standort oder eine Abteilung enthält, indem Sie Ihre e-Mail-Adresse mithilfe der [getrooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode oder der [getrooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) -EWS-Operation angeben. Wenn Sie eine Sammlung von Räumen haben, die einer Raumliste zugeordnet sind, können Sie die Sammlung durchsuchen, um den gewünschten Raum oder die Räume zu identifizieren, entweder per e-Mail-Adresse oder nach Schlüsselwörtern im Namen, beispielsweise "AV" oder "Lab". 
  
## <a name="get-all-room-lists-by-using-the-ews-managed-api"></a>Abrufen aller Raumlisten mithilfe der verwaltete EWS-API
<a name="bk_GetRoomListewsma"> </a>

Im folgenden Beispiel wird gezeigt, wie Sie mithilfe der [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) -Methode eine Liste mit allen Raumlisten in Ihrer Organisation abrufen. 
  
In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. 
  
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

## <a name="get-all-room-lists-by-using-ews"></a>Abrufen aller Raumlisten mithilfe von EWS
<a name="bk_GetRoomListews"> </a>

Im folgenden Beispiel wird gezeigt, wie eine Auflistung aller [RoomLists](https://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) Ihrer Organisation mithilfe des [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) -Vorgangs abgerufen wird. Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API zum [Abrufen aller Raumlisten](#bk_GetRoomListewsma)verwenden.
  
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

Der Server antwortet auf die [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) -Anforderung mit einer [GetRoomListsResponse](https://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) -Nachricht, die die Raumlisten für Ihre Organisation enthält. 
  
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-the-ews-managed-api"></a>Abrufen aller Räume in einer Raumliste mithilfe der verwaltete EWS-API
<a name="bk_FindRoomewsma"> </a>

Im folgenden Beispiel wird gezeigt, wie eine Auflistung von Räumen in einer Raumliste mithilfe der [getrooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) -Methode abgerufen wird. 
  
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-ews"></a>Abrufen aller Räume in einer Raumliste mithilfe von EWS
<a name="bk_FindRoomews"> </a>

Im folgenden Beispiel wird gezeigt, wie Sie eine Liste von [Räumen](https://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) in einer [RoomList](https://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) mithilfe der [getrooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) -Operation abrufen. Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API verwenden, um [Alle Räume in einer Raumliste abzurufen](#bk_FindRoomewsma).
  
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

Der Server antwortet auf die [getrooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) -Anforderung mit einer [GetRoomsResponse](https://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) -Nachricht, die die Chatrooms in der Raumliste enthält. 
  
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

## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Abrufen von Frei/Gebucht-Informationen mithilfe von EWS in Exchange](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [Erstellen und Verwalten von Raumpostfächern](https://technet.microsoft.com/library/jj215781%28v=exchg.150%29.aspx)
    

