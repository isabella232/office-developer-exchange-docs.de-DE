---
title: Bereitstellen von x-Headern mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 45a99a14-a85f-47f8-af48-18eb6c6cc230
description: Erfahren Sie, wie Sie X-Header für ein Postfach mithilfe der verwalteten EWS-API oder EWS in Exchange bereitstellen.
ms.openlocfilehash: de572764921da432cfa203b3dcf166d1d34dd0cd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756983"
---
# <a name="provision-x-headers-by-using-ews-in-exchange"></a><span data-ttu-id="77dc0-103">Bereitstellen von x-Headern mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="77dc0-103">How to: Provision x-headers by using EWS in Exchange</span></span>

<span data-ttu-id="77dc0-104">Erfahren Sie, wie Sie X-Header für ein Postfach mithilfe der verwalteten EWS-API oder EWS in Exchange bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="77dc0-104">Learn how to provision x-headers for a mailbox by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="77dc0-105">X-Header sind nicht standardmäßige Kopfzeilen, die der Headerauflistung einer E-Mail für die Kommunikation von Informationen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="77dc0-105">X-headers are non-standard headers that are added to the header collection of an email to communicate information.</span></span> <span data-ttu-id="77dc0-106">Exchange versieht Nachrichten beispielsweise mit dem Header **X-MS-Exchange-Organization-SCL**, um die SCL-Bewertung (Spam Confidence Level) der E-Mail anzugeben.</span><span class="sxs-lookup"><span data-stu-id="77dc0-106">For example, Exchange stamps messages with the **X-MS-Exchange-Organization-SCL** header to indicate the spam confidence level (SCL) attributed to the email.</span></span> <span data-ttu-id="77dc0-107">E-Mail-Clients wie Outlook können diese Informationen verwenden, um festzustellen, welche Art von Aktion für E-Mails ausgeführt werden soll (in Outlook kann beispielsweise eingestellt werden, dass Bilder erst dann angezeigt werden, wenn der Benutzer eine Aktion ausführt).</span><span class="sxs-lookup"><span data-stu-id="77dc0-107">X-headers are non-standard headers that are added to the header collection of an email to communicate information. For example, Exchange stamps messages with the X-MS-Exchange-Organization-SCL header to indicate the spam confidence level (SCL) attributed to the email. Email clients like Outlook can use that information to determine what type of action to take on the email (for example, Outlook can prevent images from displaying unless the user takes an action).</span></span> 
  
<span data-ttu-id="77dc0-p102">Exchange fügt eingehende X-Header dem Postfachschema als benannte Eigenschaft zu, wenn das erste Mal eine E-Mail mit diesem X-Header eingeht. Der Wert des X-Headers wird in dieser ersten E-Mail nicht gespeichert. Er wird jedoch in allen nachfolgenden E-Mails mit diesem X-Header gespeichert. Aus diesem Grund sollte Ihre Anwendung X-Header bereitstellen, bevor Sie diese verwenden möchten. Die Zuordnung zwischen einer benannten Eigenschaft und einem X-Header erfolgt bei der Transportzustellung der E-Mail an das Postfach. Dies bedeutet, dass die E-Mail über die Transportzustellung empfangen werden muss; Sie können nicht einfach eine E-Mail mit dem X-Header in einem Postfach speichern, um die Zuordnung zu einer benannten Eigenschaft zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77dc0-p102">Exchange adds incoming x-headers to the mailbox schema as a named property the first time it receives an email with that x-header. The x-header value is not saved on that first email; however, it is saved on all subsequent emails that include the x-header. For this reason, your application should provision x-headers before you expect to use them. The mapping between a named property and an x-header occurs in the transport delivery of the email to the mailbox. This means that you need to receive the email via transport delivery; you cannot just save an email that includes the x-header to a mailbox to create the mapping to a named property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="77dc0-113">Wenn Sie feststellen, dass die X-Header nicht gespeichert werden, müssen Sie ermitteln, ob ein [Transport-Agent](http://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) oder eine [Header-Firewall](http://technet.microsoft.com/de-DE/library/bb232136%28v=exchg.150%29.aspx) die X-Header herausfiltern, bevor sie das Postfach erreichen.</span><span class="sxs-lookup"><span data-stu-id="77dc0-113">If you find that x-headers aren't being saved, determine whether a [transport agent](http://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) or [header firewall](http://technet.microsoft.com/de-DE/library/bb232136%28v=exchg.150%29.aspx) is filtering out your x-headers before they get to the mailbox.</span></span> 
  
## <a name="provision-an-x-header-by-using-the-ews-managed-api"></a><span data-ttu-id="77dc0-114">Bereitstellen eines X-Headers mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="77dc0-114">Provision an x-header by using the EWS Managed API</span></span>
<span data-ttu-id="77dc0-115"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="77dc0-115"></span></span>

<span data-ttu-id="77dc0-p103">Im folgenden Codebeispiel wird gezeigt, wie die [EmailMessage.Send](http://msdn.microsoft.com/de-DE/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx)-Methode der EWS Managed API zur Bereitstellung eines X-Headers für ein Postfach verwendet wird. In diesem Beispiel wird vorausgesetzt, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass dieses Zielpostfach nicht das [Kontingent für benannte Eigenschaften](http://technet.microsoft.com/de-DE/library/bb851492%28v=EXCHG.80%29.aspx)überschritten hat.</span><span class="sxs-lookup"><span data-stu-id="77dc0-p103">The following code example shows how to use the EWS Managed API [EmailMessage.Send](http://msdn.microsoft.com/de-DE/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) method to provision an x-header for a mailbox. This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the target mailbox hasn't exceeded the [quota for named properties](http://technet.microsoft.com/de-DE/library/bb851492%28v=EXCHG.80%29.aspx).</span></span>
  
```cs
private static void ProvisionCustomXHeaderByEmail(ExchangeService service)
{
    // Create a definition for an extended property that will represent a custom x-header. X-headers must be created in the
    // InternetHeaders property set. The x-header name must match the name of the x-header sent in the subsequent emails so
    // the x-header and value are saved on the email.
    ExtendedPropertyDefinition xExperimentalHeader = new ExtendedPropertyDefinition(DefaultExtendedPropertySet.InternetHeaders,
                                                                                            "X-Experimental",
                                                                                            MapiPropertyType.String);
    // Create an item that is used to provision the custom x-header.
    EmailMessage email = new EmailMessage(service);
    email.ToRecipients.Add("user@contoso.com");
    email.SetExtendedProperty(xExperimentalHeader, "Provision X-Experimental Internet message header");
    try
    {
        // The mapping of the named property happens in transport delivery.
        email.Send();
        if (service.ServerInfo.MajorVersion == 12)
        {
            Console.WriteLine("Provisioned the X-Experimental across the mailbox database that hosts the user's mailbox.");
        }
        else // For versions of Exchange starting with Exchange 2010
        {
            Console.WriteLine("Provisioned the X-Experimental for the user's mailbox. You will need to run this " +
                                "for each mailbox that needs to process this x-header.");
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error: {0}", ex.Message);
    }
}
```

## <a name="provision-an-x-header-by-using-ews"></a><span data-ttu-id="77dc0-118">Bereitstellen eines X-Headers mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="77dc0-118">Provision an x-header by using EWS</span></span>
<span data-ttu-id="77dc0-119"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="77dc0-119"></span></span>

<span data-ttu-id="77dc0-p104">Im folgenden Codebeispiel wird gezeigt, wie der [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)-Vorgang von EWS zum Erstellen und Senden eine E-Mail verwendet wird, um einen X-Header für ein Postfach bereitzustellen. Dies ist die XML-Anforderung, die von der EWS Managed API gesendet wird, wenn Sie [Bereitstellen eines X-Headers mithilfe der EWS Managed API](#bk_example1).</span><span class="sxs-lookup"><span data-stu-id="77dc0-p104">The following code example shows how to use the EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) operation to create and send an email to provision a mailbox with an x-header. This is the XML request that is sent by the EWS Managed API when you [Provision an x-header by using the EWS Managed API](#bk_example1).</span></span>
  
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
    <m:CreateItem MessageDisposition="SendOnly">
      <m:Items>
        <t:Message>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="InternetHeaders"
                                PropertyName="X-Experimental"
                                PropertyType="String" />
            <t:Value>Provision X-Experimental Internet message header</t:Value>
          </t:ExtendedProperty>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>user@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

## <a name="version-differences"></a><span data-ttu-id="77dc0-122">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="77dc0-122">Version differences</span></span>
<span data-ttu-id="77dc0-123"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="77dc0-123"></span></span>

<span data-ttu-id="77dc0-p105">Wenn Sie das erste Mal einen X-Header in Exchange Online, Exchange Online als Teil von Office 365 oder auf einer lokalen Version von Exchange ab Exchange Server 2010 bereitstellen, wird der Wert eines neuen benutzerdefinierten X-Headers nicht in die gespeicherte Nachricht geschrieben. Dies liegt daran, dass der X-Header zuerst einer benannten Eigenschaft im Postfach des Benutzers zugeordnet werden muss. Die Zuordnung erfolgt bei der ersten Anforderung zum Hinzufügen der benannten Eigenschaften. Wenn eine nachfolgende Anforderung zum Erstellen der benannten Eigenschaft auftritt, werden die Eigenschaft und der Wert für die Nachricht gespeichert. In Exchange 2007 wird eine Zuordnung für den X-Header zu einer benannten Eigenschaft über die Postfachdatenbank hinweg erstellt, wenn ein X-Header das erste Mal in eine Postfachdatenbank geschrieben wird. Wenn eine nachfolgende Anforderung zum Erstellen der benannten Eigenschaft auftritt, wird der X-Header verarbeitet und für jedes Postfach in der Exchange 2007-Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="77dc0-p105">The first time that you provision an x-header in Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2010, the value of a new custom x-header will not be written to the stored message. This is because the x-header must first be mapped to a named property in the user's mailbox. The mapping occurs upon the first request to add the named properties. When a subsequent request to create the named property occurs, the property and value are stored on the message. In Exchange 2007, the first time an x-header is written to a mailbox database, a mapping is created for the x-header to a named property across the mailbox database. When a subsequent request to create the named property occurs, the x-header is processed and stored for any mailbox in the Exchange 2007 database.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="77dc0-130">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="77dc0-130">Next steps</span></span>
<span data-ttu-id="77dc0-131"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="77dc0-131"></span></span>

<span data-ttu-id="77dc0-p106">In diesem Artikel wird gezeigt, wie ein X-Header für ein einzelnes Postfach durch Senden einer E-Mail an einen Benutzer bereitgestellt wird. Sie können einen X-Header auch für viele Benutzer bereitstellen, indem Sie [eine Stapel-E-Mail an eine Liste von Empfängern](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) in der Organisation des Anrufers senden.</span><span class="sxs-lookup"><span data-stu-id="77dc0-p106">This article shows you how to provision an x-header for a single mailbox by sending an email to a user. You can also provision an x-header for many users by [sending a batch email to a list of recipients](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) in the caller's organization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="77dc0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77dc0-134">See also</span></span>


- [<span data-ttu-id="77dc0-135">Eigenschaften und erweiterte Eigenschaften in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="77dc0-135">Properties and extended properties in EWS in Exchange</span></span>](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [<span data-ttu-id="77dc0-136">Exchange 2013: Programmgesteuertes Bereitstellen von benutzerdefinierten X-Headern</span><span class="sxs-lookup"><span data-stu-id="77dc0-136">Exchange 2013: Provision custom X-headers programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [<span data-ttu-id="77dc0-137">Benannte Eigenschaften, X-Header und Sie</span><span class="sxs-lookup"><span data-stu-id="77dc0-137">Named Properties, X-Headers, and You</span></span>](http://blogs.technet.com/b/exchange/archive/2009/04/06/3407221.aspx)
    
- [<span data-ttu-id="77dc0-138">Benannte Eigenschaften, 2. Teil: Was die Zukunft bringt</span><span class="sxs-lookup"><span data-stu-id="77dc0-138">Named Properties, Round 2: What lies Ahead</span></span>](http://blogs.technet.com/b/exchange/archive/2009/06/12/3407672.aspx)
    
- [<span data-ttu-id="77dc0-139">Header-Firewall</span><span class="sxs-lookup"><span data-stu-id="77dc0-139">Header Firewall</span></span>](http://technet.microsoft.com/de-DE/library/bb232136%28v=exchg.150%29.aspx)
    
- [<span data-ttu-id="77dc0-140">EWS, MIME und die fehlenden Nachrichtenkopfzeilen</span><span class="sxs-lookup"><span data-stu-id="77dc0-140">EWS, MIME, and the missing Internet message headers</span></span>](http://msdn.microsoft.com/library/office/hh545614%28v=exchg.140%29.aspx)
    
- [<span data-ttu-id="77dc0-141">Verarbeiten von E-Mails in Batches mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="77dc0-141">How to: Process email messages in batches by using EWS in Exchange</span></span>](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    

