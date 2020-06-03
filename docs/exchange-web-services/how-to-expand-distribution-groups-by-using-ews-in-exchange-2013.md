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
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a><span data-ttu-id="2302c-103">Erweitern von Verteilergruppen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="2302c-103">Expand distribution groups by using EWS in Exchange 2013</span></span>

<span data-ttu-id="2302c-104">Hier erfahren Sie, wie Sie eine Verteilergruppe mithilfe der verwaltete EWS-API oder EWS in Exchange erweitern.</span><span class="sxs-lookup"><span data-stu-id="2302c-104">Learn how to expand a distribution group by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="2302c-105">Sie können die [Datei "ExchangeService. expandgroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode oder den [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) -EWS-Vorgang verwenden, um eine Verteilergruppe zu erweitern, um alle Empfänger zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2302c-105">You can use the [ExchangeService.ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS Managed API method or the [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) EWS operation to expand a distribution group to identify all recipients.</span></span> 
  
<span data-ttu-id="2302c-106">Da die [expando](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) -Methode überladen ist, können Sie Sie auf verschiedene Arten aufrufen:</span><span class="sxs-lookup"><span data-stu-id="2302c-106">Because the [ExpandGroup](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) method is overloaded, you can call it in several ways:</span></span> 
  
- <span data-ttu-id="2302c-107">[Expandgroup (Zeichenfolge)](https://msdn.microsoft.com/library/office/ee343988%28v=exchg.80%29.aspx) – erweitert eine Gruppe, die durch eine SMTP-Adresse identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2302c-107">[ExpandGroup(String)](https://msdn.microsoft.com/library/office/ee343988%28v=exchg.80%29.aspx) - Expands a group identified by an SMTP address.</span></span> 
    
- <span data-ttu-id="2302c-108">[Expandgroup (](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) e-Mail-Adresse) – erweitert eine Gruppe, die durch eine e-Mail-Adresse identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2302c-108">[ExpandGroup(EmailAddress)](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) - Expands a group identified by an email address.</span></span> 
    
- <span data-ttu-id="2302c-109">[Expandgroup (Itemid)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) – erweitert eine Gruppe, die durch eine Gruppen-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2302c-109">[ExpandGroup(ItemId)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) - Expands a group identified by a group ID.</span></span> 
    
- <span data-ttu-id="2302c-110">[ExpanGroup (String, String)](https://msdn.microsoft.com/library/office/ee356468%28v=exchg.80%29.aspx) – erweitert eine Gruppe, die durch eine SMTP-Adresse und den Routingtyp dieser Adresse identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2302c-110">[ExpanGroup(String, String)](https://msdn.microsoft.com/library/office/ee356468%28v=exchg.80%29.aspx) - Expands a group identified by an SMTP address and the routing type of that address.</span></span> 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a><span data-ttu-id="2302c-111">Erweitern einer universellen Verteilergruppe oder Sicherheitsgruppe mithilfe von verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="2302c-111">Expand a universal distribution group or security group by using EWS Managed API</span></span>
<span data-ttu-id="2302c-112"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="2302c-112"><a name="bk_ExpandDGEWSMA"> </a></span></span>

<span data-ttu-id="2302c-113">Das folgende Beispiel zeigt, wie Sie eine universelle Verteilergruppe oder Sicherheitsgruppe mithilfe einer e-Mail-Adresse erweitern, was der einfachste Ansatz ist.</span><span class="sxs-lookup"><span data-stu-id="2302c-113">The following example shows how to expand a universal distribution group or security group by using an email address, which is the simplest approach.</span></span> <span data-ttu-id="2302c-114">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="2302c-114">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

<span data-ttu-id="2302c-115">Das ist nicht viel Code, aber es ist auch ziemlich einfach und möglicherweise nicht geben, was Sie suchen.</span><span class="sxs-lookup"><span data-stu-id="2302c-115">That's not a lot of code, but it's also pretty basic and might not give you what you are looking for.</span></span> <span data-ttu-id="2302c-116">Lassen Sie uns also einen Schritt weiter gehen.</span><span class="sxs-lookup"><span data-stu-id="2302c-116">So let's take it a step further.</span></span> <span data-ttu-id="2302c-117">Verteilergruppen können auch andere Verteilergruppen enthalten.</span><span class="sxs-lookup"><span data-stu-id="2302c-117">Distribution groups can also contain other distribution groups.</span></span> <span data-ttu-id="2302c-118">Durch einfaches erweitern wird die e-Mail-Adresse der enthaltenen Verteilergruppen ausgegeben, aber nicht erweitert.</span><span class="sxs-lookup"><span data-stu-id="2302c-118">Simply expanding it will output the email address of the contained distribution groups but not expand them.</span></span> <span data-ttu-id="2302c-119">Durch Hinzufügen einiger weiterer Codezeilen können Sie die Gruppen rekursiv erweitern, um jeden Kontakt auszugeben.</span><span class="sxs-lookup"><span data-stu-id="2302c-119">By adding a few more lines of code, you can recursively expand the groups to output every contact.</span></span>
  
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

<span data-ttu-id="2302c-120">Und jetzt können Sie diese neue Funktion in Ihrem Code aufrufen und alle in der ersten enthaltenen öffentlichen Verteilergruppen erweitern.</span><span class="sxs-lookup"><span data-stu-id="2302c-120">And now you can call this new function in the your code and expand all the public distribution groups contained within the first one.</span></span>
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a><span data-ttu-id="2302c-121">Erweitern einer Kontaktgruppe mithilfe von verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="2302c-121">Expand a contact group by using EWS Managed API</span></span>
<span data-ttu-id="2302c-122"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="2302c-122"><a name="bk_ExpandDGEWSMA"> </a></span></span>

<span data-ttu-id="2302c-123">Da Kontaktgruppen keine zugehörige e-Mail-Adresse haben, müssen Sie die Gruppe basierend auf dem Itemid mithilfe der [expandgroup (Itemid)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) -Methode erweitern.</span><span class="sxs-lookup"><span data-stu-id="2302c-123">Because contact groups do not have an associated email address, you need to expand the group based on the ItemId by using the [ExpandGroup(ItemId)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="2302c-124">Sie können eine Funktion erstellen, wie im vorherigen Beispiel gezeigt, und den zweiten Parametertyp von einer Zeichenfolge in ein [ItemID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)-Element ändern.</span><span class="sxs-lookup"><span data-stu-id="2302c-124">You can create a function, as shown in the previous example, and change the second parameter type from a string to an [ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx).</span></span>
  
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

<span data-ttu-id="2302c-125">Jetzt können Sie diese Funktion mit dem Exchange-Dienstobjekt und dem **ItemID** der Kontaktgruppe aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2302c-125">Now you can call this function by using the Exchange service object and the **ItemId** of the contact group.</span></span> <span data-ttu-id="2302c-126">Beachten Sie, dass die **ItemID** im Beispiel zur Lesbarkeit gekürzt wird.</span><span class="sxs-lookup"><span data-stu-id="2302c-126">Note that the **ItemId** in the example is shortened for readability.</span></span> 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a><span data-ttu-id="2302c-127">Erweitern einer universellen Verteilergruppe oder Sicherheitsgruppe mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="2302c-127">Expand a universal distribution group or security group by using EWS</span></span>
<span data-ttu-id="2302c-128"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="2302c-128"><a name="bk_ExpandDGEWSMA"> </a></span></span>

<span data-ttu-id="2302c-129">Das folgende Beispiel zeigt die XML-Anforderungsnachricht, die vom Client an den Server gesendet wird, wenn Sie den [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) -Vorgang verwenden.</span><span class="sxs-lookup"><span data-stu-id="2302c-129">The following example shows the XML request message that is sent from the client to the server when you use the [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="2302c-130">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API zum [Erweitern einer universellen Verteilergruppe](#bk_ExpandDGEWSMA)verwenden.</span><span class="sxs-lookup"><span data-stu-id="2302c-130">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [expand a universal distribution group](#bk_ExpandDGEWSMA).</span></span> 
  
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

<span data-ttu-id="2302c-131">Das folgende Beispiel zeigt die XML-Antwortnachricht, die vom Server an den Client gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="2302c-131">The following example shows the XML response message that is sent from the server to the client.</span></span> <span data-ttu-id="2302c-132">Beachten Sie, dass sowohl Postfächer als auch universelle Verteilergruppen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2302c-132">Notice that both mailboxes and universal distribution groups are returned.</span></span>
  
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

<span data-ttu-id="2302c-133">Anders als bei der Verwendung des verwaltete EWS-API, wenn Sie EWS zum Erweitern einer universellen Verteilergruppe verwenden, können Sie die zurückgegebenen Verteilergruppen nicht rekursiv erweitern.</span><span class="sxs-lookup"><span data-stu-id="2302c-133">Unlike when you use the EWS Managed API, when you use EWS to expand a universal distribution group, you can't recursively expand the distribution groups that are returned.</span></span> <span data-ttu-id="2302c-134">Sie müssen eine zusätzliche Anforderung senden, um die einzelnen Verteilergruppen zu erweitern, die in der Antwort enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="2302c-134">You will need to send an additional request to expand each of the distribution groups included in the response.</span></span>
  
## <a name="expand-a-contact-group-by-using-ews"></a><span data-ttu-id="2302c-135">Erweitern einer Kontaktgruppe mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="2302c-135">Expand a contact group by using EWS</span></span>
<span data-ttu-id="2302c-136"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="2302c-136"><a name="bk_ExpandDGEWSMA"> </a></span></span>

<span data-ttu-id="2302c-137">Die XML-Anforderung zum Erweitern einer Kontaktgruppe ähnelt einer Anforderung zum Erweitern einer Verteilergruppe.</span><span class="sxs-lookup"><span data-stu-id="2302c-137">The XML request to expand a contact group is similar to a request to expand a distribution group.</span></span> <span data-ttu-id="2302c-138">Anstelle einer e-Mail-Adresse verwenden Sie das [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der Kontaktgruppe.</span><span class="sxs-lookup"><span data-stu-id="2302c-138">Instead of an email address, you use the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the contact group.</span></span> <span data-ttu-id="2302c-139">Das **ItemID** in diesem Beispiel wird zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="2302c-139">The **ItemId** in this example is shortened for readability.</span></span> 
  
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

<span data-ttu-id="2302c-140">Die Struktur der XML-Antwort auf eine Anforderung zum Erweitern einer Kontaktgruppe ist identisch mit der Antwort auf eine Anforderung zum Erweitern einer universellen Verteilergruppe.</span><span class="sxs-lookup"><span data-stu-id="2302c-140">The structure of the XML response to a request to expand a contact group is the same as the response to a request to expand a universal distribution group.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2302c-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2302c-141">See also</span></span>


- [<span data-ttu-id="2302c-142">Verteilergruppen und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2302c-142">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="2302c-143">Erstellen von Kontaktgruppen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2302c-143">Create contact groups by using EWS in Exchange</span></span>](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

