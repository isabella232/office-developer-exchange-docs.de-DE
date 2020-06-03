---
title: Bereitstellen von x-Headern mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 45a99a14-a85f-47f8-af48-18eb6c6cc230
description: Erfahren Sie, wie Sie X-Header für ein Postfach mithilfe der verwalteten EWS-API oder EWS in Exchange bereitstellen.
ms.openlocfilehash: 409ddb944bbac7a60242de39cdf7ae13b17cc76a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527768"
---
# <a name="provision-x-headers-by-using-ews-in-exchange"></a>Bereitstellen von x-Headern mithilfe von EWS in Exchange

Erfahren Sie, wie Sie X-Header für ein Postfach mithilfe der verwalteten EWS-API oder EWS in Exchange bereitstellen.
  
X-headers are non-standard headers that are added to the header collection of an email to communicate information. For example, Exchange stamps messages with the **X-MS-Exchange-Organization-SCL** header to indicate the spam confidence level (SCL) attributed to the email. Email clients like Outlook can use that information to determine what type of action to take on the email (for example, Outlook can prevent images from displaying unless the user takes an action). 
  
Exchange fügt eingehende X-Header dem Postfachschema als benannte Eigenschaft zu, wenn das erste Mal eine E-Mail mit diesem X-Header eingeht. Der Wert des X-Headers wird in dieser ersten E-Mail nicht gespeichert. Er wird jedoch in allen nachfolgenden E-Mails mit diesem X-Header gespeichert. Aus diesem Grund sollte Ihre Anwendung X-Header bereitstellen, bevor Sie diese verwenden möchten. Die Zuordnung zwischen einer benannten Eigenschaft und einem X-Header erfolgt bei der Transportzustellung der E-Mail an das Postfach. Dies bedeutet, dass die E-Mail über die Transportzustellung empfangen werden muss; Sie können nicht einfach eine E-Mail mit dem X-Header in einem Postfach speichern, um die Zuordnung zu einer benannten Eigenschaft zu erstellen.
  
> [!NOTE]
> [!HINWEIS] Wenn Sie feststellen, dass die X-Header nicht gespeichert werden, müssen Sie ermitteln, ob ein [Transport-Agent](https://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) oder eine [Header-Firewall](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx) die X-Header herausfiltern, bevor sie das Postfach erreichen. r
  
## <a name="provision-an-x-header-by-using-the-ews-managed-api"></a>Bereitstellen eines X-Headers mithilfe der EWS Managed API
<a name="bk_example1"> </a>

Im folgenden Codebeispiel wird gezeigt, wie die [EmailMessage.Send](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx)-Methode der EWS Managed API zur Bereitstellung eines X-Headers für ein Postfach verwendet wird. In diesem Beispiel wird vorausgesetzt, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass dieses Zielpostfach nicht das [Kontingent für benannte Eigenschaften](https://technet.microsoft.com/library/bb851492%28v=EXCHG.80%29.aspx)überschritten hat.
  
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

## <a name="provision-an-x-header-by-using-ews"></a>Bereitstellen eines X-Headers mithilfe von EWS
<a name="bk_example1"> </a>

Im folgenden Codebeispiel wird gezeigt, wie der [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)-Vorgang von EWS zum Erstellen und Senden eine E-Mail verwendet wird, um einen X-Header für ein Postfach bereitzustellen. Dies ist die XML-Anforderung, die von der EWS Managed API gesendet wird, wenn Sie [Bereitstellen eines X-Headers mithilfe der EWS Managed API](#bk_example1).
  
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

## <a name="version-differences"></a>Versionsunterschiede
<a name="bk_example1"> </a>

Wenn Sie das erste Mal einen X-Header in Exchange Online, Exchange Online als Teil von Office 365 oder auf einer lokalen Version von Exchange ab Exchange Server 2010 bereitstellen, wird der Wert eines neuen benutzerdefinierten X-Headers nicht in die gespeicherte Nachricht geschrieben. Dies liegt daran, dass der X-Header zuerst einer benannten Eigenschaft im Postfach des Benutzers zugeordnet werden muss. Die Zuordnung erfolgt bei der ersten Anforderung zum Hinzufügen der benannten Eigenschaften. Wenn eine nachfolgende Anforderung zum Erstellen der benannten Eigenschaft auftritt, werden die Eigenschaft und der Wert für die Nachricht gespeichert. In Exchange 2007 wird eine Zuordnung für den X-Header zu einer benannten Eigenschaft über die Postfachdatenbank hinweg erstellt, wenn ein X-Header das erste Mal in eine Postfachdatenbank geschrieben wird. Wenn eine nachfolgende Anforderung zum Erstellen der benannten Eigenschaft auftritt, wird der X-Header verarbeitet und für jedes Postfach in der Exchange 2007-Datenbank gespeichert.
  
## <a name="next-steps"></a>Nächste Schritte
<a name="bk_example1"> </a>

In diesem Artikel wird gezeigt, wie ein X-Header für ein einzelnes Postfach durch Senden einer E-Mail an einen Benutzer bereitgestellt wird. Sie können einen X-Header auch für viele Benutzer bereitstellen, indem Sie [eine Stapel-E-Mail an eine Liste von Empfängern](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) in der Organisation des Anrufers senden. 
  
## <a name="see-also"></a>Siehe auch


- [Eigenschaften und erweiterte Eigenschaften in EWS in Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Exchange 2013: Programmgesteuertes Bereitstellen von benutzerdefinierten X-Headern](https://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [Benannte Eigenschaften, X-Header und Sie](https://blogs.technet.com/b/exchange/archive/2009/04/06/3407221.aspx)
    
- [Benannte Eigenschaften, 2. Teil: Was die Zukunft bringt](https://blogs.technet.com/b/exchange/archive/2009/06/12/3407672.aspx)
    
- [Header-Firewall](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx)
    
- [EWS, MIME und die fehlenden Nachrichtenkopfzeilen](https://msdn.microsoft.com/library/office/hh545614%28v=exchg.140%29.aspx)
    
- [Verarbeiten von E-Mails in Batches mithilfe von EWS in Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    

