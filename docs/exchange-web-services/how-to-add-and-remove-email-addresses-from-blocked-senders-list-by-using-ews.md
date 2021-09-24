---
title: Hinzufügen und Entfernen von E-Mail-Adressen von der Liste blockierter Absender mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: b88288ee-6af7-45b5-a55c-5929cd0c16f1
description: Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um E-Mail-Adressen hinzuzufügen und aus der Liste blockierter Absender zu entfernen.
ms.openlocfilehash: 4deacbfa6e146675e3248e3932734a1492645246
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512205"
---
# <a name="add-and-remove-email-addresses-from-the-blocked-senders-list-by-using-ews-in-exchange"></a>Hinzufügen und Entfernen von E-Mail-Adressen von der Liste blockierter Absender mithilfe von EWS in Exchange

Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um E-Mail-Adressen hinzuzufügen und aus der Liste blockierter Absender zu entfernen.
  
Die Liste blockierter Absender in den Junk-E-Mail-Optionen eines Benutzers bietet eine Möglichkeit, alle E-Mail-Nachrichten von angegebenen Absendern in den Junk-E-Mail-Ordner zu verschieben. Sie können Ihre verwaltete EWS-API oder EWS-Anwendung aktivieren, um E-Mail-Adressen hinzuzufügen oder aus der Liste blockierter Absender zu entfernen.
  
Beachten Sie, dass eine Nachricht von der E-Mail-Adresse im Postfach des Benutzers vorhanden sein muss, bevor Sie die E-Mail-Adresse zur Liste blockierter Absender hinzufügen oder aus der Liste blockierter Absender entfernen können. Die [ExchangeService.MarkAsJunk](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS Managed API-Methode und der [MarkAsJunk](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS-Vorgang verwenden eine Auflistung von Element-IDs. Die Element-IDs in der Auflistung geben Nachrichten im Postfach an, für die der Junk-E-Mail-Status geändert werden soll. 
  
Sie können die Cmdlets ["Get-MailboxJunkEmailConfiguration"](https://technet.microsoft.com/library/dd979784%28v=exchg.150%29.aspx) und ["Set-MailboxJunkEmailConfiguration"](https://technet.microsoft.com/library/dd979780%28v=exchg.150%29.aspx) Exchange Verwaltungsshell verwenden, um direkt auf die Liste blockierter Absender zuzugreifen. 
  
## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-the-ews-managed-api"></a>Hinzufügen einer E-Mail-Adresse zur Liste blockierter Absender oder Entfernen dieser Adresse aus der Liste blockierter Absender mithilfe der verwalteten EWS-API
<a name="bk_AddRemoveEWSMA"> </a>

Um den Absender einer E-Mail-Nachricht zur Liste blockierter Absender hinzuzufügen, verwenden Sie die **MarkAsJunk** -Methode, und legen Sie den **isJunk** -Parameter auf **"true"** fest. Um den Absender einer E-Mail-Nachricht aus der Liste blockierter Absender zu entfernen, legen Sie den **Parameter "isJunk"** auf **"false"** fest.
  
Das folgende Beispiel zeigt, wie Sie die **MarkAsJunk-Methode** verwenden, um den Junk-Status einer Nachricht zu ändern. 
  
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

## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-ews"></a>Hinzufügen einer E-Mail-Adresse zur Liste blockierter Absender oder Entfernen dieser Adresse aus der Liste blockierter Absender mithilfe von EWS
<a name="bk_AddRemoveEWS"> </a>

Mit der folgenden EWS SOAP-Anforderung wird ein Element als Junk gekennzeichnet, indem das **IsJunk-Attribut** für das [MarkAsJunk-Element](https://msdn.microsoft.com/library/f06bafc6-7ee3-4b2b-9fd1-7c51328f4729%28Office.15%29.aspx) auf **"true"** festgelegt wird. Außerdem wird die Nachricht in den Junk-E-Mail-Ordner verschoben, indem das **MoveItem-Attribut** für das **MarkAsJunk-Element** auf **"true"** festgelegt wird.
  
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

Die folgende EWS SOAP-Antwort zeigt die erfolgreiche Antwort. Das [MovedItemId-Element](https://msdn.microsoft.com/library/7d5425ab-1e75-43d1-b801-802ff5139df6%28Office.15%29.aspx) in der Antwort enthält die Element-ID für das Element, nachdem es verschoben wurde. 
  
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
- [ExchangeService.MarkAsJunk](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx)   
- [MarkAsJunk-Vorgang](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)   
- [Get-MailboxJunkEmailConfiguration](https://technet.microsoft.com/library/dd979784%28v=exchg.150%29.aspx)   
- [Set-MailboxJunkEmailConfiguration](https://technet.microsoft.com/library/dd979780%28v=exchg.150%29.aspx) 
- [Exchange-Verwaltungsshell](../management/exchange-management-shell.md)
    

