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
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a><span data-ttu-id="aa34a-103">Erweitern von Verteilergruppen durch Verwenden von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="aa34a-103">Expand distribution groups by using EWS in Exchange 2013</span></span>

<span data-ttu-id="aa34a-104">Hier erfahren Sie, wie Sie eine Verteilergruppe zu erweitern, indem Sie verwenden die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa34a-104">Learn how to expand a distribution group by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="aa34a-105">Die [ExchangeService.ExpandGroup](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS Managed API-Methode oder [der ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) EWS-Vorgangs können Sie eine Verteilergruppe, um alle Empfänger ermitteln erweitern.</span><span class="sxs-lookup"><span data-stu-id="aa34a-105">You can use the [ExchangeService.ExpandGroup](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS Managed API method or the [ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) EWS operation to expand a distribution group to identify all recipients.</span></span> 
  
<span data-ttu-id="aa34a-106">Da die [ExpandGroup](http://msdn.microsoft.com/de-de/library/office/ee344007%28v=exchg.80%29.aspx) -Methode überlastet ist, können Sie es auf verschiedene Weise aufrufen:</span><span class="sxs-lookup"><span data-stu-id="aa34a-106">Because the [ExpandGroup](http://msdn.microsoft.com/de-de/library/office/ee344007%28v=exchg.80%29.aspx) method is overloaded, you can call it in several ways:</span></span> 
  
- <span data-ttu-id="aa34a-107">[ExpandGroup(String)](http://msdn.microsoft.com/de-de/library/office/ee343988%28v=exchg.80%29.aspx) - wird eine Gruppe durch eine SMTP-Adresse identifizierten erweitert.</span><span class="sxs-lookup"><span data-stu-id="aa34a-107">[ExpandGroup(String)](http://msdn.microsoft.com/de-de/library/office/ee343988%28v=exchg.80%29.aspx) - Expands a group identified by an SMTP address.</span></span> 
    
- <span data-ttu-id="aa34a-108">[ExpandGroup(EmailAddress)](http://msdn.microsoft.com/de-de/library/office/ee344007%28v=exchg.80%29.aspx) - erweitert eine Gruppe durch eine e-Mail-Adresse identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aa34a-108">[ExpandGroup(EmailAddress)](http://msdn.microsoft.com/de-de/library/office/ee344007%28v=exchg.80%29.aspx) - Expands a group identified by an email address.</span></span> 
    
- <span data-ttu-id="aa34a-109">[ExpandGroup(ItemId)](http://msdn.microsoft.com/de-de/library/office/ee356407%28v=exchg.80%29.aspx) - erweitert eine Gruppe, identifiziert durch eine Gruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="aa34a-109">[ExpandGroup(ItemId)](http://msdn.microsoft.com/de-de/library/office/ee356407%28v=exchg.80%29.aspx) - Expands a group identified by a group ID.</span></span> 
    
- <span data-ttu-id="aa34a-110">[ExpanGroup (String, String)](http://msdn.microsoft.com/de-de/library/office/ee356468%28v=exchg.80%29.aspx) - erweitert eine Gruppe durch eine SMTP-Adresse und den Routingtyp dieser Adresse identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aa34a-110">[ExpanGroup(String, String)](http://msdn.microsoft.com/de-de/library/office/ee356468%28v=exchg.80%29.aspx) - Expands a group identified by an SMTP address and the routing type of that address.</span></span> 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a><span data-ttu-id="aa34a-111">Erweitern Sie eine universelle Verteilergruppe oder Sicherheitsgruppe mithilfe von EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="aa34a-111">Expand a universal distribution group or security group by using EWS Managed API</span></span>
<span data-ttu-id="aa34a-112"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="aa34a-112"></span></span>

<span data-ttu-id="aa34a-113">Im folgenden Beispiel wird gezeigt, wie, erweitern eine universelle Verteilergruppe oder Sicherheitsgruppe mithilfe einer e-Mail-Adresse, die am einfachsten ist.</span><span class="sxs-lookup"><span data-stu-id="aa34a-113">The following example shows how to expand a universal distribution group or security group by using an email address, which is the simplest approach.</span></span> <span data-ttu-id="aa34a-114">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="aa34a-114">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

<span data-ttu-id="aa34a-115">Das ist noch nicht viel Code, aber es ist auch recht grundlegender und möglicherweise nicht Ihnen wonach Sie suchen.</span><span class="sxs-lookup"><span data-stu-id="aa34a-115">That's not a lot of code, but it's also pretty basic and might not give you what you are looking for.</span></span> <span data-ttu-id="aa34a-116">So gehen wir noch einen Schritt weiter.</span><span class="sxs-lookup"><span data-stu-id="aa34a-116">So let's take it a step further.</span></span> <span data-ttu-id="aa34a-117">Verteilergruppen können auch anderen Verteilergruppen enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa34a-117">Distribution groups can also contain other distribution groups.</span></span> <span data-ttu-id="aa34a-118">Einfach erweitern wird die e-Mail-Adresse der enthaltenen Verteilergruppen Ausgabe, aber nicht erweitern.</span><span class="sxs-lookup"><span data-stu-id="aa34a-118">Simply expanding it will output the email address of the contained distribution groups but not expand them.</span></span> <span data-ttu-id="aa34a-119">Indem Sie ein paar weitere Codezeilen hinzufügen, können Sie rekursiv erweitern Sie die Gruppen, um jeden Kontakt auszugeben.</span><span class="sxs-lookup"><span data-stu-id="aa34a-119">By adding a few more lines of code, you can recursively expand the groups to output every contact.</span></span>
  
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

<span data-ttu-id="aa34a-120">Und Sie können nun dieser neuen Funktion in Aufrufen der Ihr code, und erweitern Sie alle öffentlichen Verteilergruppen, die in der ersten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="aa34a-120">And now you can call this new function in the your code and expand all the public distribution groups contained within the first one.</span></span>
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a><span data-ttu-id="aa34a-121">Erweitern Sie eine Gruppe von Kontakte mit EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="aa34a-121">Expand a contact group by using EWS Managed API</span></span>
<span data-ttu-id="aa34a-122"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="aa34a-122"></span></span>

<span data-ttu-id="aa34a-123">Da Kontaktgruppen nicht über eine zugehörige e-Mail-Adresse verfügen, müssen Sie die Gruppe basierend auf der ItemId mithilfe der [ExpandGroup(ItemId)](http://msdn.microsoft.com/de-de/library/office/ee356407%28v=exchg.80%29.aspx) -Methode zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="aa34a-123">Because contact groups do not have an associated email address, you need to expand the group based on the ItemId by using the [ExpandGroup(ItemId)](http://msdn.microsoft.com/de-de/library/office/ee356407%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="aa34a-124">Sie können eine Funktion erstellen, wie im vorherigen Beispiel gezeigt, und ändern Sie den zweiten Parametertyp aus einer Zeichenfolge in einer [ItemId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aa34a-124">You can create a function, as shown in the previous example, and change the second parameter type from a string to an [ItemId](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx).</span></span>
  
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

<span data-ttu-id="aa34a-125">Jetzt können Sie diese Funktion mithilfe der Exchange-Dienst-Objekt und die **ItemId** der Kontaktgruppe aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aa34a-125">Now you can call this function by using the Exchange service object and the **ItemId** of the contact group.</span></span> <span data-ttu-id="aa34a-126">Beachten Sie, dass die **ItemId** im Beispiel zur besseren Lesbarkeit gekürzt wird.</span><span class="sxs-lookup"><span data-stu-id="aa34a-126">Note that the **ItemId** in the example is shortened for readability.</span></span> 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a><span data-ttu-id="aa34a-127">Erweitern Sie eine universelle Verteilergruppe oder Sicherheitsgruppe mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="aa34a-127">Expand a universal distribution group or security group by using EWS</span></span>
<span data-ttu-id="aa34a-128"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="aa34a-128"></span></span>

<span data-ttu-id="aa34a-129">Das folgende Beispiel zeigt die XML-Request-Nachricht, die vom Client an den Server gesendet wird, wenn Sie den Vorgang [der ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa34a-129">The following example shows the XML request message that is sent from the client to the server when you use the [ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="aa34a-130">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet bei Verwendung der EWS Managed API, um [eine universelle Verteilergruppe zu erweitern](#bk_ExpandDGEWSMA).</span><span class="sxs-lookup"><span data-stu-id="aa34a-130">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [expand a universal distribution group](#bk_ExpandDGEWSMA).</span></span> 
  
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

<span data-ttu-id="aa34a-131">Das folgende Beispiel zeigt die XML-Response-Nachricht, die vom Server an den Client gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa34a-131">The following example shows the XML response message that is sent from the server to the client.</span></span> <span data-ttu-id="aa34a-132">Beachten Sie, dass Postfächer und universelle Verteilergruppen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa34a-132">Notice that both mailboxes and universal distribution groups are returned.</span></span>
  
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

<span data-ttu-id="aa34a-133">Anders als bei der EWS Managed API Verwendung, wenn Sie Exchange-Webdienste verwenden, um eine universelle Verteilergruppe zu erweitern, können Sie nicht rekursiv erweitern die Verteilergruppen an, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa34a-133">Unlike when you use the EWS Managed API, when you use EWS to expand a universal distribution group, you can't recursively expand the distribution groups that are returned.</span></span> <span data-ttu-id="aa34a-134">Sie benötigen, senden eine zusätzliche Anforderung an die in der Antwort enthalten Verteilergruppen zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="aa34a-134">You will need to send an additional request to expand each of the distribution groups included in the response.</span></span>
  
## <a name="expand-a-contact-group-by-using-ews"></a><span data-ttu-id="aa34a-135">Erweitern Sie eine Gruppe von Kontakte mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="aa34a-135">Expand a contact group by using EWS</span></span>
<span data-ttu-id="aa34a-136"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="aa34a-136"></span></span>

<span data-ttu-id="aa34a-137">Die XML-Anforderung an eine Kontaktgruppe erweitern ähnelt einer Anforderung an eine Verteilergruppe zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="aa34a-137">The XML request to expand a contact group is similar to a request to expand a distribution group.</span></span> <span data-ttu-id="aa34a-138">Statt eine e-Mail-Adresse verwenden Sie die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der Kontaktgruppe.</span><span class="sxs-lookup"><span data-stu-id="aa34a-138">Instead of an email address, you use the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the contact group.</span></span> <span data-ttu-id="aa34a-139">In diesem Beispiel wird die **ItemId** wird zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="aa34a-139">The **ItemId** in this example is shortened for readability.</span></span> 
  
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

<span data-ttu-id="aa34a-140">Die Struktur der XML-Antwort auf eine Anforderung an eine Kontaktgruppe erweitern ist identisch mit der Antwort auf eine Anforderung an eine universelle Verteilergruppe zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="aa34a-140">The structure of the XML response to a request to expand a contact group is the same as the response to a request to expand a universal distribution group.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa34a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa34a-141">See also</span></span>


- [<span data-ttu-id="aa34a-142">Verteilergruppen und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="aa34a-142">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="aa34a-143">Erstellen von Kontaktgruppen im Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="aa34a-143">Create contact groups by using EWS in Exchange</span></span>](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

