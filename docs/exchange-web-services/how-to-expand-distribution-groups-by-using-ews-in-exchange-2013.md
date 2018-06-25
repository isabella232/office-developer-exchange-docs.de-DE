---
title: Erweitern von Verteilergruppen durch Verwenden von EWS in Exchange 2013
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25ee84e7-63bc-4f51-9b7d-e7f46fd574d5
description: Hier erfahren Sie, wie Sie eine Verteilergruppe zu erweitern, indem Sie verwenden die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 0f9186fb71b3005c71a70e89aafb674ae15e4814
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756884"
---
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a>Erweitern von Verteilergruppen durch Verwenden von EWS in Exchange 2013

Hier erfahren Sie, wie Sie eine Verteilergruppe zu erweitern, indem Sie verwenden die EWS Managed API oder EWS in Exchange.
  
Die [ExchangeService.ExpandGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS Managed API-Methode oder [der ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) EWS-Vorgangs können Sie eine Verteilergruppe, um alle Empfänger ermitteln erweitern. 
  
Da die [ExpandGroup](http://msdn.microsoft.com/en-us/library/office/ee344007%28v=exchg.80%29.aspx) -Methode überlastet ist, können Sie es auf verschiedene Weise aufrufen: 
  
- [ExpandGroup(String)](http://msdn.microsoft.com/en-us/library/office/ee343988%28v=exchg.80%29.aspx) - wird eine Gruppe durch eine SMTP-Adresse identifizierten erweitert. 
    
- [ExpandGroup(EmailAddress)](http://msdn.microsoft.com/en-us/library/office/ee344007%28v=exchg.80%29.aspx) - erweitert eine Gruppe durch eine e-Mail-Adresse identifiziert. 
    
- [ExpandGroup(ItemId)](http://msdn.microsoft.com/en-us/library/office/ee356407%28v=exchg.80%29.aspx) - erweitert eine Gruppe, identifiziert durch eine Gruppe-ID. 
    
- [ExpanGroup (String, String)](http://msdn.microsoft.com/en-us/library/office/ee356468%28v=exchg.80%29.aspx) - erweitert eine Gruppe durch eine SMTP-Adresse und den Routingtyp dieser Adresse identifiziert. 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a>Erweitern Sie eine universelle Verteilergruppe oder Sicherheitsgruppe mithilfe von EWS Managed API
<a name="bk_ExpandDGEWSMA"> </a>

Im folgenden Beispiel wird gezeigt, wie, erweitern eine universelle Verteilergruppe oder Sicherheitsgruppe mithilfe einer e-Mail-Adresse, die am einfachsten ist. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

Das ist noch nicht viel Code, aber es ist auch recht grundlegender und möglicherweise nicht Ihnen wonach Sie suchen. So gehen wir noch einen Schritt weiter. Verteilergruppen können auch anderen Verteilergruppen enthalten. Einfach erweitern wird die e-Mail-Adresse der enthaltenen Verteilergruppen Ausgabe, aber nicht erweitern. Indem Sie ein paar weitere Codezeilen hinzufügen, können Sie rekursiv erweitern Sie die Gruppen, um jeden Kontakt auszugeben.
  
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

Und Sie können nun dieser neuen Funktion in Aufrufen der Ihr code, und erweitern Sie alle öffentlichen Verteilergruppen, die in der ersten enthalten sind.
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a>Erweitern Sie eine Gruppe von Kontakte mit EWS Managed API
<a name="bk_ExpandDGEWSMA"> </a>

Da Kontaktgruppen nicht über eine zugehörige e-Mail-Adresse verfügen, müssen Sie die Gruppe basierend auf der ItemId mithilfe der [ExpandGroup(ItemId)](http://msdn.microsoft.com/en-us/library/office/ee356407%28v=exchg.80%29.aspx) -Methode zu erweitern. Sie können eine Funktion erstellen, wie im vorherigen Beispiel gezeigt, und ändern Sie den zweiten Parametertyp aus einer Zeichenfolge in einer [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx).
  
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

Jetzt können Sie diese Funktion mithilfe der Exchange-Dienst-Objekt und die **ItemId** der Kontaktgruppe aufrufen. Beachten Sie, dass die **ItemId** im Beispiel zur besseren Lesbarkeit gekürzt wird. 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a>Erweitern Sie eine universelle Verteilergruppe oder Sicherheitsgruppe mithilfe der Exchange-Webdienste
<a name="bk_ExpandDGEWSMA"> </a>

Das folgende Beispiel zeigt die XML-Request-Nachricht, die vom Client an den Server gesendet wird, wenn Sie den Vorgang [der ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) verwenden. Dies ist auch die XML-Anfrage, die die EWS Managed API sendet bei Verwendung der EWS Managed API, um [eine universelle Verteilergruppe zu erweitern](#bk_ExpandDGEWSMA). 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>employees@contoso.com</t:EmailAddress>
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt die XML-Response-Nachricht, die vom Server an den Client gesendet wird. Beachten Sie, dass Postfächer und universelle Verteilergruppen zurückgegeben werden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:xsd="http://www.w3.org/2001/XMLSchema">
<ExpandDLResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                      xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <ExpandDLResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <DLExpansion IncludesLastItemInRange="true" TotalItemsInView="4">
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Sadie Daniels</Name>
          <EmailAddress>sadie@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Alfred Welker</Name>
          <EmailAddress>alfred@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Contoso Sales</Name>
          <EmailAddress>sales@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>PublicDL</MailboxType>
        </Mailbox>
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

Anders als bei der EWS Managed API Verwendung, wenn Sie Exchange-Webdienste verwenden, um eine universelle Verteilergruppe zu erweitern, können Sie nicht rekursiv erweitern die Verteilergruppen an, die zurückgegeben werden. Sie benötigen, senden eine zusätzliche Anforderung an die in der Antwort enthalten Verteilergruppen zu erweitern.
  
## <a name="expand-a-contact-group-by-using-ews"></a>Erweitern Sie eine Gruppe von Kontakte mithilfe der Exchange-Webdienste
<a name="bk_ExpandDGEWSMA"> </a>

Die XML-Anforderung an eine Kontaktgruppe erweitern ähnelt einer Anforderung an eine Verteilergruppe zu erweitern. Statt eine e-Mail-Adresse verwenden Sie die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der Kontaktgruppe. In diesem Beispiel wird die **ItemId** wird zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
         <ItemId xmlns="http://schemas.microsoft.com/exchange/services/2006/types" Id="AAMkADBlY…" />
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

Die Struktur der XML-Antwort auf eine Anforderung an eine Kontaktgruppe erweitern ist identisch mit der Antwort auf eine Anforderung an eine universelle Verteilergruppe zu erweitern.
  
## <a name="see-also"></a>Siehe auch


- [Verteilergruppen und EWS in Exchange](distribution-groups-and-ews-in-exchange.md)
    
- [Erstellen von Kontaktgruppen im Exchange mithilfe der Exchange-Webdienste](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

