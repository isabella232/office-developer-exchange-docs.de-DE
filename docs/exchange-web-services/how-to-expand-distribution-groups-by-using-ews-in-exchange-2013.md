---
title: Erweitern von Verteilergruppen mithilfe von EWS in Exchange 2013
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 25ee84e7-63bc-4f51-9b7d-e7f46fd574d5
description: Erfahren Sie, wie Sie eine Verteilergruppe mithilfe der verwalteten EWS-API oder EWS in Exchange erweitern.
ms.openlocfilehash: 6aeebbd14604295bce46049f0e383663414c01a0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513185"
---
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a>Erweitern von Verteilergruppen mithilfe von EWS in Exchange 2013

Erfahren Sie, wie Sie eine Verteilergruppe mithilfe der verwalteten EWS-API oder EWS in Exchange erweitern.
  
Sie können die [ExchangeService.ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS Managed API-Methode oder den [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) EWS-Vorgang verwenden, um eine Verteilergruppe zu erweitern, um alle Empfänger zu identifizieren. 
  
Da die [ExpandGroup-Methode](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) überladen ist, können Sie sie auf verschiedene Arten aufrufen: 
  
- [ExpandGroup(String)](https://msdn.microsoft.com/library/office/ee343988%28v=exchg.80%29.aspx) – Erweitert eine Gruppe, die durch eine SMTP-Adresse identifiziert wird. 
    
- [ExpandGroup(EmailAddress)](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) – Erweitert eine Gruppe, die durch eine E-Mail-Adresse identifiziert wird. 
    
- [ExpandGroup(ItemId)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) – Erweitert eine Gruppe, die durch eine Gruppen-ID identifiziert wird. 
    
- [ExpanGroup(String, String)](https://msdn.microsoft.com/library/office/ee356468%28v=exchg.80%29.aspx) – Erweitert eine Gruppe, die durch eine SMTP-Adresse und den Routingtyp dieser Adresse identifiziert wird. 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a>Erweitern einer universellen Verteiler- oder Sicherheitsgruppe mithilfe der verwalteten EWS-API
<a name="bk_ExpandDGEWSMA"> </a>

Das folgende Beispiel zeigt, wie Sie eine universelle Verteiler- oder Sicherheitsgruppe mithilfe einer E-Mail-Adresse erweitern, was der einfachste Ansatz ist. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

Das ist nicht viel Code, aber es ist auch ziemlich einfach und bietet Ihnen möglicherweise nicht das, wonach Sie suchen. Lassen Sie uns also einen Schritt weiter gehen. Verteilergruppen können auch andere Verteilergruppen enthalten. Durch einfaches Erweitern wird die E-Mail-Adresse der enthaltenen Verteilergruppen ausgegeben, aber nicht erweitert. Durch Hinzufügen weiterer Codezeilen können Sie rekursiv die Gruppen erweitern, um jeden Kontakt auszugeben.
  
```cs
private static void ExpandDistributionLists(ExchangeService service, string Mailbox)
{
   // Return the expanded group.
      ExpandGroupResults myGroupMembers = service.ExpandGroup(Mailbox);
   // Display the group members.
      foreach (EmailAddress address in myGroupMembers.Members)
      {
         // Check to see if the mailbox is a public group
         if (address.MailboxType == MailboxType.PublicGroup)
      {
         // Call the function again to expand the contained
         // distribution group.
         ExpandDistributionLists(service, address.Address);
      }
      else
      {
         // Output the address of the mailbox.
         Console.WriteLine("Email Address: {0}", address);
      }
   }
}

```

Jetzt können Sie diese neue Funktion im Code aufrufen und alle öffentlichen Verteilergruppen erweitern, die in der ersten enthalten sind.
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a>Erweitern einer Kontaktgruppe mithilfe der verwalteten EWS-API
<a name="bk_ExpandDGEWSMA"> </a>

Da Kontaktgruppen keine E-Mail-Adresse zugeordnet ist, müssen Sie die Gruppe basierend auf der ItemId mithilfe der [ExpandGroup(ItemId)-Methode](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) erweitern. Sie können eine Funktion erstellen, wie im vorherigen Beispiel gezeigt, und den zweiten Parametertyp von einer Zeichenfolge in eine [ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)ändern.
  
```cs
private static void ExpandContactGroup(ExchangeService service, ItemId groupID)
{
   // Return the expanded group.
      ExpandGroupResults myGroupMembers = service.ExpandGroup(groupID);
   // Display the group members.
      foreach (EmailAddress address in myGroupMembers.Members)
      {
         if (address.MailboxType == MailboxType.PublicGroup)
         {
            ExpandDistributionLists(service, address.Address);
         }
         else
         {
            Console.WriteLine("Email Address: {0}", address);
         }
      }
}
```

Jetzt können Sie diese Funktion mithilfe des Exchange-Dienstobjekts und der **ItemId** der Kontaktgruppe aufrufen. Beachten Sie, dass die **ItemId** im Beispiel zur besseren Lesbarkeit gekürzt wurde. 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a>Erweitern einer universellen Verteiler- oder Sicherheitsgruppe mithilfe von EWS
<a name="bk_ExpandDGEWSMA"> </a>

Das folgende Beispiel zeigt die XML-Anforderungsnachricht, die vom Client an den Server gesendet wird, wenn Sie den [ExpandDL-Vorgang](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) verwenden. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die verwaltete EWS-API verwenden, um [eine universelle Verteilergruppe](#bk_ExpandDGEWSMA)zu erweitern. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>employees@contoso.com</t:EmailAddress>
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt die XML-Antwortnachricht, die vom Server an den Client gesendet wird. Beachten Sie, dass sowohl Postfächer als auch universelle Verteilergruppen zurückgegeben werden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:xsd="http://www.w3.org/2001/XMLSchema">
<ExpandDLResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                      xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <ExpandDLResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <DLExpansion IncludesLastItemInRange="true" TotalItemsInView="4">
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Sadie Daniels</Name>
          <EmailAddress>sadie@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Alfred Welker</Name>
          <EmailAddress>alfred@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Contoso Sales</Name>
          <EmailAddress>sales@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>PublicDL</MailboxType>
        </Mailbox>
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Contoso Support</Name>
          <EmailAddress>support@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>PublicDL</MailboxType>
        </Mailbox>
      </DLExpansion>
    </ExpandDLResponseMessage>
  </ResponseMessages>
</ExpandDLResponse>
</s:Body>
</s:Envelope>
```

Im Gegensatz zur Verwendung der verwalteten EWS-API können Sie bei Verwendung von EWS zum Erweitern einer universellen Verteilergruppe die zurückgegebenen Verteilergruppen nicht rekursiv erweitern. Sie müssen eine zusätzliche Anforderung senden, um jede der in der Antwort enthaltenen Verteilergruppen zu erweitern.
  
## <a name="expand-a-contact-group-by-using-ews"></a>Erweitern einer Kontaktgruppe mithilfe von EWS
<a name="bk_ExpandDGEWSMA"> </a>

Die XML-Anforderung zum Erweitern einer Kontaktgruppe ähnelt einer Anforderung zum Erweitern einer Verteilergruppe. Anstelle einer E-Mail-Adresse verwenden Sie die [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der Kontaktgruppe. Die **ItemId** in diesem Beispiel wird zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
         <ItemId xmlns="https://schemas.microsoft.com/exchange/services/2006/types" Id="AAMkADBlY…" />
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

Die Struktur der XML-Antwort auf eine Anforderung zum Erweitern einer Kontaktgruppe entspricht der Antwort auf eine Anforderung zum Erweitern einer universellen Verteilergruppe.
  
## <a name="see-also"></a>Siehe auch


- [Verteilergruppen und EWS in Exchange](distribution-groups-and-ews-in-exchange.md)
    
- [Erstellen von Kontaktgruppen mithilfe von EWS in Exchange](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

