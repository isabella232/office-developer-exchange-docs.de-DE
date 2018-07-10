---
title: Legen Sie die Exchange-Webdienste-URL mithilfe der EWS Managed API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cddf6525-1c04-484b-a911-56c2f0f1f7b6
description: In diesem Artikel finden Sie Informationen zum Festlegen der EWS-Dienst-URL in der verwalteten EWS-API-Anwendung.
ms.openlocfilehash: e1a414f7c6f13bd61a58403c9d2be546c0226a69
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756993"
---
# <a name="set-the-ews-service-url-by-using-the-ews-managed-api"></a><span data-ttu-id="b33cd-103">Legen Sie die Exchange-Webdienste-URL mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="b33cd-103">Set the EWS service URL by using the EWS Managed API</span></span>

<span data-ttu-id="b33cd-104">In diesem Artikel finden Sie Informationen zum Festlegen der EWS-Dienst-URL in der verwalteten EWS-API-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b33cd-104">Find information about how to set the EWS service URL in your EWS Managed API application.</span></span>
  
<span data-ttu-id="b33cd-p101">Die Dienst-URL ist die Adresse, über die Exchange mit Exchange-Webdienste (EWS) kommuniziert. Wenn die verwaltete EWS-API-Anwendung über diese Adresse und entsprechenden Zugriff zum [Kommunizieren mit EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md) verfügt, kann sie Aufrufe an die [ExchangeService-Klasse](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) durchführen. Die Dienst-URL für einen lokalen Exchange-Server kann wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="b33cd-p101">The service URL is the address that Exchange uses to communicate with Exchange Web Services (EWS). After your EWS Managed API application has this address, and has appropriate access to [communicate with EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md), it can make calls to the [ExchangeService class](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx). The service URL for an on-premises Exchange server might look like the following.</span></span> 
  
```HTML
https://computer.domain.contoso.com/EWS/Exchange.asmx
```

<span data-ttu-id="b33cd-p102">Sie können die EWS-URL in der Anwendung auf verschiedene Weise festlegen. Empfohlen wird die Verwendung des [AutoErmittlungsdiensts](http://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx) zum Abrufen der URL, da sich die URL bei einer großen Gesamtstruktur von Servern ändern kann, wenn das Postfach auf einen anderen Server migriert wird. Da der Aufruf der AutoErmittlung jedoch einige Zeit in Anspruch nehmen und die Anwendung verlangsamen kann, sollten Sie, falls Sie mehrere Aufrufe innerhalb eines kurzen Zeitraums durchführen müssen, den von der AutoErmittlung abgerufenen URL-Wert zwischenspeichern und die EWS-Dienst-URL mit diesem zwischengespeicherten Wert manuell festlegen. Dies verbessert die Leistung der Anwendung; stellen Sie lediglich sicher, dass Sie den zwischengespeicherten Wert regelmäßig mithilfe der AutoErmittlung aktualisieren, falls sich der Wert auf dem Server ändert.</span><span class="sxs-lookup"><span data-stu-id="b33cd-p102">You can set the EWS URL in your application in a couple of ways. We recommend that you use the [Autodiscover service](http://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx) to get the URL because in a large forest of servers, the URL can change if the mailbox is migrated to another server. However, because calling Autodiscover can take some time and can slow down your application if you need to make multiple calls in a short period of time, you might want to cache the URL value you get from Autodiscover and manually set the EWS service URL with this cached value. This will improve the performance of your application; just make sure that you use Autodiscover to update your cached value periodically in case the value changes on the server.</span></span> 
  
## <a name="set-the-ews-service-url-by-using-the-autodiscover-service"></a><span data-ttu-id="b33cd-112">Festlegen der EWS-Dienst-URL mithilfe des AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="b33cd-112">Set the EWS service URL by using the Autodiscover service</span></span>
<span data-ttu-id="b33cd-113"><a name="bk_SetURLusingAutoDiscover"> </a></span><span class="sxs-lookup"><span data-stu-id="b33cd-113"></span></span>

<span data-ttu-id="b33cd-p103">Die [AutodiscoverUrl](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx)-Methode verwendet die E-Mail-Adresse zum Festlegen des [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Endpunkts und ermöglicht es der Anwendung, alle in den **ExchangeService** -Proxyklassen enthaltenen Methoden zu verwenden. Im folgenden Beispiel wird die Verwendung der **AutodiscoverURL** -Methode veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b33cd-p103">The [AutodiscoverUrl](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) method uses the email address to set the [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) endpoint and enables your application to use any methods included in the **ExchangeService** proxy classes. The following example shows how to use the **AutodiscoverURL** method.</span></span> 
  
```cs
// Create the binding.
ExchangeService service = new ExchangeService();
// Set the credentials for the on-premises server.
service.Credentials = new WebCredentials("user1@contoso.com", "password");
// Set the URL.
service.AutodiscoverUrl("User1@contoso.com");

```

## <a name="set-the-exchange-service-url-manually"></a><span data-ttu-id="b33cd-116">Manuelles Festlegen der Exchange-Dienst-URL</span><span class="sxs-lookup"><span data-stu-id="b33cd-116">Set the Exchange service URL manually</span></span>
<span data-ttu-id="b33cd-117"><a name="bk_SetURLmanually"> </a></span><span class="sxs-lookup"><span data-stu-id="b33cd-117"></span></span>

<span data-ttu-id="b33cd-p104">Im folgenden Beispiel wird gezeigt, wie Sie die EWS-Dienst-URL unter Verwendung eines zwischengespeicherten Werts festlegen. Vorher müssen Sie mithilfe des AutoErmittlungsdiensts die EWS-URL abrufen.</span><span class="sxs-lookup"><span data-stu-id="b33cd-p104">The following example shows you how to set the EWS service URL by using a cached value. Before you do this, make sure to use the Autodiscover service to get the EWS URL.</span></span>
  
```cs
// Create the binding.
ExchangeService service = new ExchangeService();
// Set the credentials for the on-premises server.
service.Credentials = new WebCredentials("user1@contoso.com", "password");
// Set the URL.
service.Url = new Uri("https://computername.domain.contoso.com/EWS/Exchange.asmx");

```

## <a name="see-also"></a><span data-ttu-id="b33cd-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b33cd-120">See also</span></span>

- [<span data-ttu-id="b33cd-121">Erste Schritte mit verwalteten EWS-API-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="b33cd-121">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md)   
- [<span data-ttu-id="b33cd-122">Einrichten der Entwicklungsumgebung für Exchange-Anwendung</span><span class="sxs-lookup"><span data-stu-id="b33cd-122">Setting up your Exchange application development environment</span></span>](setting-up-your-exchange-application-development-environment.md)   
- [<span data-ttu-id="b33cd-123">Steuern des Zugriffs auf EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="b33cd-123">Control access to EWS in Exchange</span></span>](how-to-control-access-to-ews-in-exchange.md) 
- [<span data-ttu-id="b33cd-124">Kommunizieren Sie mit Exchange-Webdienste mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="b33cd-124">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)  
- [<span data-ttu-id="b33cd-125">Mithilfe von AutoErmittlung Verbindungspunkte suchen</span><span class="sxs-lookup"><span data-stu-id="b33cd-125">Use Autodiscover to find connection points</span></span>](how-to-use-autodiscover-to-find-connection-points.md)
    

