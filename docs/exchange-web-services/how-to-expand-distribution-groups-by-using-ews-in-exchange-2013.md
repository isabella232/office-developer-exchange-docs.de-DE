---
title: Erweitern von Verteilergruppen mithilfe von EWS in Exchange 2013
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25ee84e7-63bc-4f51-9b7d-e7f46fd574d5
description: Hier erfahren Sie, wie Sie eine Verteilergruppe mithilfe der verwaltete EWS-API oder EWS in Exchange erweitern.
ms.openlocfilehash: 2cbeb65b5a722bce4d5cab8fd716230874a6afca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528118"
---
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a>Erweitern von Verteilergruppen mithilfe von EWS in Exchange 2013

Hier erfahren Sie, wie Sie eine Verteilergruppe mithilfe der verwaltete EWS-API oder EWS in Exchange erweitern.
  
Sie können die [Datei "ExchangeService. expandgroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode oder den [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) -EWS-Vorgang verwenden, um eine Verteilergruppe zu erweitern, um alle Empfänger zu identifizieren. 
  
Da die [expando](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) -Methode überladen ist, können Sie Sie auf verschiedene Arten aufrufen: 
  
- [Expandgroup (Zeichenfolge)](https://msdn.microsoft.com/library/office/ee343988%28v=exchg.80%29.aspx) – erweitert eine Gruppe, die durch eine SMTP-Adresse identifiziert wird. 
    
- [Expandgroup (](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) e-Mail-Adresse) – erweitert eine Gruppe, die durch eine e-Mail-Adresse identifiziert wird. 
    
- [Expandgroup (Itemid)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) – erweitert eine Gruppe, die durch eine Gruppen-ID identifiziert wird. 
    
- [ExpanGroup (String, String)](https://msdn.microsoft.com/library/office/ee356468%28v=exchg.80%29.aspx) – erweitert eine Gruppe, die durch eine SMTP-Adresse und den Routingtyp dieser Adresse identifiziert wird. 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a>Erweitern einer universellen Verteilergruppe oder Sicherheitsgruppe mithilfe von verwaltete EWS-API
<a name="bk_ExpandDGEWSMA"> </a>

Das folgende Beispiel zeigt, wie Sie eine universelle Verteilergruppe oder Sicherheitsgruppe mithilfe einer e-Mail-Adresse erweitern, was der einfachste Ansatz ist. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde. 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

Das ist nicht viel Code, aber es ist auch ziemlich einfach und möglicherweise nicht geben, was Sie suchen. Lassen Sie uns also einen Schritt weiter gehen. Verteilergruppen können auch andere Verteilergruppen enthalten. Durch einfaches erweitern wird die e-Mail-Adresse der enthaltenen Verteilergruppen ausgegeben, aber nicht erweitert. Durch Hinzufügen einiger weiterer Codezeilen können Sie die Gruppen rekursiv erweitern, um jeden Kontakt auszugeben.
  
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

Und jetzt können Sie diese neue Funktion in Ihrem Code aufrufen und alle in der ersten enthaltenen öffentlichen Verteilergruppen erweitern.
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a>Erweitern einer Kontaktgruppe mithilfe von verwaltete EWS-API
<a name="bk_ExpandDGEWSMA"> </a>

Da Kontaktgruppen keine zugehörige e-Mail-Adresse haben, müssen Sie die Gruppe basierend auf dem Itemid mithilfe der [expandgroup (Itemid)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) -Methode erweitern. Sie können eine Funktion erstellen, wie im vorherigen Beispiel gezeigt, und den zweiten Parametertyp von einer Zeichenfolge in ein [ItemID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)-Element ändern.
  
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

Jetzt können Sie diese Funktion mit dem Exchange-Dienstobjekt und dem **ItemID** der Kontaktgruppe aufrufen. Beachten Sie, dass die **ItemID** im Beispiel zur Lesbarkeit gekürzt wird. 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a>Erweitern einer universellen Verteilergruppe oder Sicherheitsgruppe mithilfe von EWS
<a name="bk_ExpandDGEWSMA"> </a>

Das folgende Beispiel zeigt die XML-Anforderungsnachricht, die vom Client an den Server gesendet wird, wenn Sie den [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) -Vorgang verwenden. Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API zum [Erweitern einer universellen Verteilergruppe](#bk_ExpandDGEWSMA)verwenden. 
  
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

Anders als bei der Verwendung des verwaltete EWS-API, wenn Sie EWS zum Erweitern einer universellen Verteilergruppe verwenden, können Sie die zurückgegebenen Verteilergruppen nicht rekursiv erweitern. Sie müssen eine zusätzliche Anforderung senden, um die einzelnen Verteilergruppen zu erweitern, die in der Antwort enthalten sein sollen.
  
## <a name="expand-a-contact-group-by-using-ews"></a>Erweitern einer Kontaktgruppe mithilfe von EWS
<a name="bk_ExpandDGEWSMA"> </a>

Die XML-Anforderung zum Erweitern einer Kontaktgruppe ähnelt einer Anforderung zum Erweitern einer Verteilergruppe. Anstelle einer e-Mail-Adresse verwenden Sie das [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der Kontaktgruppe. Das **ItemID** in diesem Beispiel wird zur Lesbarkeit gekürzt. 
  
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

Die Struktur der XML-Antwort auf eine Anforderung zum Erweitern einer Kontaktgruppe ist identisch mit der Antwort auf eine Anforderung zum Erweitern einer universellen Verteilergruppe.
  
## <a name="see-also"></a>Siehe auch


- [Verteilergruppen und EWS in Exchange](distribution-groups-and-ews-in-exchange.md)
    
- [Erstellen von Kontaktgruppen mithilfe von EWS in Exchange](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

