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
description: Hier finden Sie im Exchange Referenzinformationen für den AutoErmittlungsdienst POX.
ms.openlocfilehash: a8797fe714fd23049094c3ec2475b93fec4282c0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830867"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="bc2ec-103">POX AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="bc2ec-103">POX Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="bc2ec-104">Hier finden Sie im Exchange Referenzinformationen für den AutoErmittlungsdienst POX.</span><span class="sxs-lookup"><span data-stu-id="bc2ec-104">Find reference information for the POX Autodiscover service in Exchange.</span></span>
  
<span data-ttu-id="bc2ec-105">Er bietet die Konfigurationsinformationen, die die Anwendung wird verwendet, um eine Verbindung mit einem Exchange-Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="bc2ec-105">The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="bc2ec-106">Sie können die "einfache alte XML" (POX) AutoErmittlungsdienst zum Senden von Nachrichten, die nur aus XML-Nutzlast, ohne alle einschließenden SOAP Umschläge, um die Einstellungen zu suchen, die eine anderen Clientanwendung benötigen, um eine Verbindung zu Exchange bestehen.</span><span class="sxs-lookup"><span data-stu-id="bc2ec-106">You can use the "plain old XML" (POX) Autodiscover service to send messages that consist only of XML payloads, without any enclosing SOAP envelopes, in order to locate the settings that a client application must have in order to connect to Exchange.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bc2ec-107">Für Clients, die Versionen von Exchange, beginnend mit Exchange Server 2010, sollten Sie den SOAP-AutoErmittlungsdienst anstelle des AutoErmittlungsdiensts POX verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc2ec-107">For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service.</span></span> <span data-ttu-id="bc2ec-108">Clients, die auf Exchange 2007 abzielen müssen den AutoErmittlungsdienst POX verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc2ec-108">Clients that target Exchange 2007 have to use the POX Autodiscover service.</span></span> <span data-ttu-id="bc2ec-109">Es wird empfohlen, dass Clients, die .NET Framework verwenden, da es sich um eine stabile und gründlich getestete POX AutoErmittlung-Client enthält die EWS Managed API verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc2ec-109">We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested POX Autodiscover client.</span></span> <span data-ttu-id="bc2ec-110">Weitere Informationen zu den EWS Managed API finden Sie unter [Erste Schritte mit EWS Managed API-Clientanwendungen](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="bc2ec-110">For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="bc2ec-111">Dieser Abschnitt enthält Informationen über die XML-Elemente, die zwischen dem Client und Server gesendet werden, während der AutoErmittlung POX Anforderung Umleitung und benutzereinstellungen für, die in einer Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc2ec-111">This section provides information about the XML elements that are sent between the client and server during POX Autodiscover request redirections and the user settings that are returned in a response.</span></span> <span data-ttu-id="bc2ec-112">XML-Elementreferenz enthält Übersichten was die Elemente bedeuten und eine Beschreibung der potenziellen Element Hierarchien, die das Element verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc2ec-112">The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that use the element.</span></span> <span data-ttu-id="bc2ec-113">In dieser Dokumentation werden die XML-Instanzen erläutert, die zwischen Client und Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc2ec-113">This documentation covers the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="bc2ec-114">Eine explizite Schema keinen POX AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="bc2ec-114">The POX Autodiscover service does not have an explicit schema.</span></span>
  
<span data-ttu-id="bc2ec-115">Die Artikel in diesem Abschnitt enthalten Beispiele und eine Beschreibung der Nachrichten, die verwendet werden, für die AutoErmittlung Konfigurationsinformationen mithilfe des AutoErmittlungsdiensts POX abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bc2ec-115">The articles in this section provide examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the POX Autodiscover service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="bc2ec-116">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="bc2ec-116">In this section</span></span>
<span data-ttu-id="bc2ec-117"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="bc2ec-117"></span></span>

- [<span data-ttu-id="bc2ec-118">POX-Anforderung der AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="bc2ec-118">POX Autodiscover request for Exchange</span></span>](pox-autodiscover-request-for-exchange.md)
    
- [<span data-ttu-id="bc2ec-119">POX Antwort der AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="bc2ec-119">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)
    
- [<span data-ttu-id="bc2ec-120">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="bc2ec-120">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="bc2ec-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc2ec-121">See also</span></span>

- [<span data-ttu-id="bc2ec-122">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="bc2ec-122">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="bc2ec-123">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="bc2ec-123">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)   
- [<span data-ttu-id="bc2ec-124">SOAP-Webdienst-Verweis für die AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="bc2ec-124">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="bc2ec-125">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="bc2ec-125">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

