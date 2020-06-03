---
title: Hinzufügen und Entfernen von E-Mail-Adressen von der Liste blockierter Absender mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b88288ee-6af7-45b5-a55c-5929cd0c16f1
description: Hier erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um e-Mail-Adressen hinzuzufügen und aus der Liste blockierter Absender zu entfernen.
ms.openlocfilehash: 270613a739acba165c7bac1bd2c1ef275b5d3aca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528279"
---
# <a name="add-and-remove-email-addresses-from-the-blocked-senders-list-by-using-ews-in-exchange"></a>Hinzufügen und Entfernen von E-Mail-Adressen von der Liste blockierter Absender mithilfe von EWS in Exchange

Hier erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um e-Mail-Adressen hinzuzufügen und aus der Liste blockierter Absender zu entfernen.
  
Die Liste blockierter Absender in den Junk-e-Mail-Optionen eines Benutzers bietet eine Möglichkeit, alle e-Mail-Nachrichten von bestimmten Absendern in den Junk-e-Mail-Ordner zu übertragen. Sie können Ihrer verwaltete EWS-API oder EWS-Anwendung das Hinzufügen von e-Mail-Adressen oder deren Entfernung aus der Liste blockierter Absender ermöglichen.
  
Beachten Sie, dass eine Nachricht von der e-Mail-Adresse im Postfach des Benutzers vorhanden sein muss, bevor Sie die e-Mail-Adresse hinzufügen oder aus der Liste blockierter Absender entfernen können. Die [Datei "ExchangeService. MarkAsJunk](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode und der [MarkAsJunk](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) -EWS-Vorgang verwenden eine Auflistung von Element-IDs. Die Element-IDs in der Auflistung geben Nachrichten im Postfach an, für die der Junk-e-Mail-Status geändert werden soll. 
  
Sie können die Exchange-Verwaltungsshell Cmdlets " [Get-MailboxJunkEmailConfiguration](https://technet.microsoft.com/library/dd979784%28v=exchg.150%29.aspx) " und " [MailboxJunkEmailConfiguration](https://technet.microsoft.com/library/dd979780%28v=exchg.150%29.aspx) " verwenden, um direkt auf die Liste blockierter Absender zuzugreifen. 
  
## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-the-ews-managed-api"></a>Hinzufügen einer e-Mail-Adresse zur Liste blockierter Absender oder Entfernen dieser Adresse mithilfe der verwaltete EWS-API
<a name="bk_AddRemoveEWSMA"> </a>

Wenn Sie den Absender einer e-Mail-Nachricht der Liste blockierter Absender hinzufügen möchten, verwenden Sie die **MarkAsJunk** -Methode, und legen Sie den Parameter **isjunk** auf **true**fest. Wenn Sie den Absender einer e-Mail-Nachricht aus der Liste blockierter Absender entfernen möchten, legen Sie den Parameter **isjunk** auf **false**fest.
  
Im folgenden Beispiel wird gezeigt, wie Sie mit der **MarkAsJunk** -Methode den Junk-Status einer Nachricht ändern. 
  
```cs
private static void MarkMessageAsJunk(ExchangeService service, ItemId messageId, bool isJunk, bool moveItem)
{
    List<ItemId> junkItemIds = new List<ItemId>();
    junkItemIds.Add(messageId);
    ServiceResponseCollection<MarkAsJunkResponse> responseCollection = null;
    try
    {
        // If isJunk is true, the sender of the email message is added to 
        // the Blocked Senders List. If isJunk is false, the sender is removed
        // from the list (if present).
        responseCollection = service.MarkAsJunk(junkItemIds, isJunk, moveItem);
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error marking item as junk: {0}", ex.ErrorCode);
        return;
    }
    foreach (MarkAsJunkResponse response in responseCollection)
    {
        if (response.Result == ServiceResult.Success)
        {
            Console.WriteLine("Successfully marked message as {0}junk.", isJunk ? "": "NOT ");
            if (moveItem)
            {
                Console.WriteLine("New item ID: {0}", response.MovedItemId.ToString());
            }
        }
        else
        {
            Console.WriteLine("[{0}]: {1}", response.Result.ToString(),
                response.ErrorCode.ToString());
        }
    }
}
```

## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-ews"></a>Hinzufügen einer e-Mail-Adresse zur Liste der blockierten Absender mithilfe von EWS oder Entfernen dieser Adresse
<a name="bk_AddRemoveEWS"> </a>

Die folgende EWS SOAP-Anforderung kennzeichnet ein Element als Junk, indem das **isjunk** -Attribut für das [MarkAsJunk](https://msdn.microsoft.com/library/f06bafc6-7ee3-4b2b-9fd1-7c51328f4729%28Office.15%29.aspx) -Element auf **true**festgelegt wird. Außerdem wird die Nachricht in den Junk-e-Mail-Ordner verschoben, indem das **MoveItem** -Attribut für das **MarkAsJunk** -Element auf **true**festgelegt wird.
  
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
    <m:MarkAsJunk IsJunk="true" MoveItem="true">
      <m:ItemIds>
        <t:ItemId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwBGAAAAAADPriAxh444TpHj2GoQxWQNBwAN+VjmVZl5Rq1ymCq5eFKOAAAAAAENAAAN+VjmVZl5Rq1ymCq5eFKOAAAAAAEuAAA=" 
            ChangeKey="CQAAABYAAAAN+VjmVZl5Rq1ymCq5eFKOAAAAAADi" />
      </m:ItemIds>
    </m:MarkAsJunk>
  </soap:Body>
</soap:Envelope>
```

Die folgende EWS-SOAP-Antwort zeigt die erfolgreiche Antwort. Das [MovedItemId](https://msdn.microsoft.com/library/7d5425ab-1e75-43d1-b801-802ff5139df6%28Office.15%29.aspx) -Element in der Antwort enthält die Element-ID für das Element, nachdem es verschoben wurde. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:MarkAsJunkResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:MovedItemId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwBGAAAAAADPriAxh444TpHj2GoQxWQNBwAN+VjmVZl5Rq1ymCq5eFKOAAAAAAEbAAAN+VjmVZl5Rq1ymCq5eFKOAAAE59DIAAA="
              ChangeKey="CQAAABYAAAAN+VjmVZl5Rq1ymCq5eFKOAAAE59E+" />
        </m:MarkAsJunkResponseMessage>
      </m:ResponseMessages>
    </m:MarkAsJunkResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Siehe auch

- [Posteingangsverwaltung und EWS in Exchange](inbox-management-and-ews-in-exchange.md)   
- [Datei "ExchangeService. MarkAsJunk](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx)   
- [MarkAsJunk-Vorgang](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)   
- [Get-MailboxJunkEmailConfiguration](https://technet.microsoft.com/library/dd979784%28v=exchg.150%29.aspx)   
- [Gruppe-MailboxJunkEmailConfiguration](https://technet.microsoft.com/library/dd979780%28v=exchg.150%29.aspx) 
- [Exchange-Verwaltungsshell](../management/exchange-management-shell.md)
    

