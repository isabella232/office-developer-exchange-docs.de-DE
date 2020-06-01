---
title: POX AutoErmittlung Webdienstverweis für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 877152f0-f4b1-4f63-b2ce-924f4bdf2d20
description: Hier finden Sie Referenzinformationen für den POX-AutoErmittlungsdienst in Exchange.
ms.openlocfilehash: 3c0ca368f4427be7759e2db58fb418b4822dea8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465653"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="69b27-103">POX AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="69b27-103">POX Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="69b27-104">Hier finden Sie Referenzinformationen für den POX-AutoErmittlungsdienst in Exchange.</span><span class="sxs-lookup"><span data-stu-id="69b27-104">Find reference information for the POX Autodiscover service in Exchange.</span></span>
  
<span data-ttu-id="69b27-105">Der AutoErmittlungsdienst stellt die Konfigurationsinformationen bereit, die Ihre Anwendung zum Erstellen einer Verbindung mit einem Exchange-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="69b27-105">The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="69b27-106">Sie können den "Plain Old XML" (POX)-AutoErmittlungsdienst verwenden, um Nachrichten zu senden, die nur aus XML-Nutzdaten bestehen, ohne einschließende SOAP-Umschläge, um die Einstellungen zu finden, die eine Clientanwendung zum Herstellen einer Verbindung mit Exchange benötigen muss.</span><span class="sxs-lookup"><span data-stu-id="69b27-106">You can use the "plain old XML" (POX) Autodiscover service to send messages that consist only of XML payloads, without any enclosing SOAP envelopes, in order to locate the settings that a client application must have in order to connect to Exchange.</span></span>
  
> [!NOTE]
> <span data-ttu-id="69b27-107">Für Clients, die auf Versionen von Exchange ab Exchange Server 2010 abzielen, wird empfohlen, den SOAP-AutoErmittlungsdienst anstelle des POX-AutoErmittlungsdiensts zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="69b27-107">For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service.</span></span> <span data-ttu-id="69b27-108">Clients, die auf Exchange 2007 Zielen, müssen den POX-AutoErmittlungsdienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="69b27-108">Clients that target Exchange 2007 have to use the POX Autodiscover service.</span></span> <span data-ttu-id="69b27-109">Es wird empfohlen, dass Clients, die das .NET Framework verwenden, den verwaltete EWS-API verwenden, da er einen robusten und bewährten POX-Auto Ermittlungs Client enthält.</span><span class="sxs-lookup"><span data-stu-id="69b27-109">We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested POX Autodiscover client.</span></span> <span data-ttu-id="69b27-110">Weitere Informationen zum verwaltete EWS-API finden Sie unter [Erste Schritte mit verwaltete EWS-API-Clientanwendungen](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="69b27-110">For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="69b27-111">Dieser Abschnitt enthält Informationen zu den XML-Elementen, die zwischen dem Client und dem Server während POX Auto Ermittlungs Anforderungs Umleitungen und den Benutzereinstellungen gesendet werden, die in einer Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="69b27-111">This section provides information about the XML elements that are sent between the client and server during POX Autodiscover request redirections and the user settings that are returned in a response.</span></span> <span data-ttu-id="69b27-112">Die XML-Elementreferenz enthält Zusammenfassungen darüber, was die Elemente darstellen, und eine Beschreibung der potenziellen Element Hierarchien, die das Element verwenden.</span><span class="sxs-lookup"><span data-stu-id="69b27-112">The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that use the element.</span></span> <span data-ttu-id="69b27-113">In dieser Dokumentation werden die XML-Instanzen erläutert, die zwischen Client und Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="69b27-113">This documentation covers the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="69b27-114">Der POX-AutoErmittlungsdienst verfügt nicht über ein explizites Schema.</span><span class="sxs-lookup"><span data-stu-id="69b27-114">The POX Autodiscover service does not have an explicit schema.</span></span>
  
<span data-ttu-id="69b27-115">Die Artikel in diesem Abschnitt enthalten Beispiele und Beschreibungen der Nachrichten, die zum Abrufen von Konfigurationsinformationen für die AutoErmittlung mithilfe des POX-AutoErmittlungsdiensts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69b27-115">The articles in this section provide examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the POX Autodiscover service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="69b27-116">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="69b27-116">In this section</span></span>
<span data-ttu-id="69b27-117"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="69b27-117"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="69b27-118">POX-Anforderung der AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="69b27-118">POX Autodiscover request for Exchange</span></span>](pox-autodiscover-request-for-exchange.md)
    
- [<span data-ttu-id="69b27-119">POX-Auto Ermittlungs Antwort für Exchange</span><span class="sxs-lookup"><span data-stu-id="69b27-119">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)
    
- [<span data-ttu-id="69b27-120">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="69b27-120">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="69b27-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69b27-121">See also</span></span>

- [<span data-ttu-id="69b27-122">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="69b27-122">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="69b27-123">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="69b27-123">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)   
- [<span data-ttu-id="69b27-124">Referenz zum SOAP-AutoErmittlungwebdienst für Exchange</span><span class="sxs-lookup"><span data-stu-id="69b27-124">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="69b27-125">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="69b27-125">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

