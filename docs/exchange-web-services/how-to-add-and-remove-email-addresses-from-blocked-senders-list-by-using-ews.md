---
title: Hinzufügen und Entfernen von e-Mail-Adressen aus der Liste blockierter Absender mithilfe der EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b88288ee-6af7-45b5-a55c-5929cd0c16f1
description: Erfahren Sie, wie Sie die EWS Managed API oder EWS verwenden, um e-Mail-Adressen hinzufügen und entfernen sie aus der Liste blockierter Absender.
ms.openlocfilehash: c03ed585ebd62802000179d8c837786ba5f9aab4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756841"
---
# <a name="add-and-remove-email-addresses-from-the-blocked-senders-list-by-using-ews-in-exchange"></a>Hinzufügen und Entfernen von e-Mail-Adressen aus der Liste blockierter Absender mithilfe der EWS in Exchange

Erfahren Sie, wie Sie die EWS Managed API oder EWS verwenden, um e-Mail-Adressen hinzufügen und entfernen sie aus der Liste blockierter Absender.
  
Die Liste blockierter Absender in den Junk-e-Mail-Optionen eines Benutzers bietet die Möglichkeit, alle e-Mail-Nachrichten vom angegebenen Absender in den Junk-e-Mail-Ordner verschieben. Sie können die EWS Managed API oder EWS-Anwendung zum e-Mail-Adressen hinzufügen oder entfernen sie aus der Liste blockierter Absender aktivieren.
  
Beachten Sie, dass eine Nachricht aus der e-Mail-Adresse in das Postfach des Benutzers vorhanden sein muss, bevor Sie die e-Mail-Adresse hinzufügen oder aus der Liste blockierter Absender entfernen können. Verwenden die [ExchangeService.MarkAsJunk](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS Managed API-Methode und die [MarkAsJunk](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS-Vorgang eine Auflistung von Element-IDs. Das Element-IDs in der Auflistung anzugeben Nachrichten im Postfach für das Junk-e-Mail-Status geändert werden soll. 
  
Die Cmdlets [Get-MailboxJunkEmailConfiguration](http://technet.microsoft.com/en-us/library/dd979784%28v=exchg.150%29.aspx) und [Set-MailboxJunkEmailConfiguration](http://technet.microsoft.com/en-us/library/dd979780%28v=exchg.150%29.aspx) Exchange-Verwaltungsshell können Sie direkt auf die Liste der blockierten Absender zugreifen. 
  
## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-the-ews-managed-api"></a>Eine e-Mail-Adresse hinzufügen oder Entfernen von es aus der Liste blockierter Absender mithilfe der EWS Managed API
<a name="bk_AddRemoveEWSMA"> </a>

Um den Absender einer e-Mail-Nachricht zur Liste blockierten Absender hinzuzufügen, verwenden Sie die **MarkAsJunk** -Methode und den **IsJunk** -Parameter auf **true**festgelegt. Um den Absender einer e-Mail-Nachricht aus der Liste blockierter Absender entfernen möchten, legen Sie den **IsJunk** -Parameter auf **false festgelegt**.
  
Im folgenden Beispiel wird gezeigt, wie Sie die **MarkAsJunk** -Methode, um zu den Junk-e-Status einer Nachricht ändern. 
  
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

## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-ews"></a>Eine e-Mail-Adresse hinzufügen oder Entfernen von es aus der Liste blockierter Absender mithilfe der Exchange-Webdienste
<a name="bk_AddRemoveEWS"> </a>

Die folgenden EWS-SOAP-Anforderung markiert ein Element als Junk-e-durch das **IsJunk** -Attribut für das [MarkAsJunk](http://msdn.microsoft.com/library/f06bafc6-7ee3-4b2b-9fd1-7c51328f4729%28Office.15%29.aspx) -Element auf **true**festlegen. Es wird auch die Nachricht in den Junk-e-Mail-Ordner nach der **MoveItem** -Attribut für das **MarkAsJunk** -Element auf **true**festlegen verschoben.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Die folgenden EWS-SOAP-Antwort zeigt die erfolgreiche Antwort. Das [MovedItemId](http://msdn.microsoft.com/library/7d5425ab-1e75-43d1-b801-802ff5139df6%28Office.15%29.aspx) -Element in der Antwort enthält die Element-ID für das Element, nachdem er verschoben wurde. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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
- [ExchangeService.MarkAsJunk](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx)   
- [MarkAsJunk Operation](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)   
- [Get-MailboxJunkEmailConfiguration](http://technet.microsoft.com/en-us/library/dd979784%28v=exchg.150%29.aspx)   
- [Set-MailboxJunkEmailConfiguration](http://technet.microsoft.com/en-us/library/dd979780%28v=exchg.150%29.aspx) 
- [Exchange-Verwaltungsshell](../management/exchange-management-shell.md)
    

