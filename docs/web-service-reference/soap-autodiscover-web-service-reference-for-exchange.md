---
title: Referenz zum SOAP-AutoErmittlungwebdienst für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: Hier finden Sie Referenzinformationen für den SOAP-AutoErmittlungsdienst in Exchange.
ms.openlocfilehash: bfca8e8e260a6262d12542bd6834894a2375453f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468425"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="d902b-103">Referenz zum SOAP-AutoErmittlungwebdienst für Exchange</span><span class="sxs-lookup"><span data-stu-id="d902b-103">SOAP Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="d902b-104">Hier finden Sie Referenzinformationen für den SOAP-AutoErmittlungsdienst in Exchange.</span><span class="sxs-lookup"><span data-stu-id="d902b-104">Find reference information for the SOAP Autodiscover service in Exchange.</span></span>
  
<span data-ttu-id="d902b-105">Der AutoErmittlungsdienst stellt die Konfigurationsinformationen bereit, die Ihre Anwendung zum Erstellen einer Verbindung mit einem Exchange-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="d902b-105">The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="d902b-106">Sie können den SOAP-AutoErmittlungsdienst zum Senden von Nachrichten zwischen der Clientanwendung und dem Exchange-Server verwenden, um die Einstellungen zu finden, die von der Anwendung zum Herstellen einer Verbindung mit Exchange verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d902b-106">You can use the SOAP Autodiscover service to send messages between the client application and the Exchange server to locate the settings the application will use to connect to Exchange.</span></span> <span data-ttu-id="d902b-107">Im Gegensatz zum POX-AutoErmittlungsdienst ermöglicht der SOAP-AutoErmittlungsdienst die Batchverarbeitung von Auto Ermittlungsanforderungen für viele Benutzereinstellungen und eine präzisere Kontrolle darüber, welche Einstellungen in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d902b-107">Unlike the POX Autodiscover service, the SOAP Autodiscover service allows for batched Autodiscover requests for many users' settings and more granular control over which settings are returned in the response.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d902b-108">Für Clients, die auf Exchange-Versionen mit Exchange Server 2010 abzielen, wird empfohlen, den SOAP-AutoErmittlungsdienst (anstelle des POX-AutoErmittlungsdiensts) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d902b-108">For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service (instead of the POX Autodiscover service).</span></span> <span data-ttu-id="d902b-109">Clients, die auf Exchange 2007 Zielen, müssen den POX-AutoErmittlungsdienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="d902b-109">Clients that target Exchange 2007 have to use the POX Autodiscover service.</span></span> <span data-ttu-id="d902b-110">Es wird empfohlen, dass Clients, die das .NET Framework verwenden, den verwaltete EWS-API verwenden, da er einen robusten und bewährten SOAP-Auto Ermittlungs Client enthält.</span><span class="sxs-lookup"><span data-stu-id="d902b-110">We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested SOAP Autodiscover client.</span></span> <span data-ttu-id="d902b-111">Weitere Informationen zum verwaltete EWS-API finden Sie unter [Erste Schritte mit verwaltete EWS-API-Clientanwendungen](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d902b-111">For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="d902b-112">Dieser Abschnitt enthält Informationen zu den XML-Elementen, die zwischen dem Client und dem Server während der SOAP-Auto Ermittlungs Anforderungs Umleitung gesendet werden, und den Benutzereinstellungen, die in einer Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d902b-112">This section provides information about the XML elements that are sent between the client and server during SOAP Autodiscover request redirections and the user settings that are returned in a response.</span></span> <span data-ttu-id="d902b-113">Die XML-Elementreferenz enthält Zusammenfassungen darüber, was die Elemente darstellen, und eine Beschreibung der potenziellen Element Hierarchien, die das-Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="d902b-113">The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that contain the element.</span></span> 
  
<span data-ttu-id="d902b-114">In den Artikeln in diesem Abschnitt werden die XML-Instanzen beschrieben, die zwischen dem Client und dem Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d902b-114">The articles in this section describe the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="d902b-115">Das Schema, in dem diese Elemente beschrieben werden, befindet sich im virtuellen Verzeichnis des Servers, auf dem der SOAP-AutoErmittlungsdienst gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="d902b-115">The schema that describes these elements can be found in the virtual directory of the server that hosts the SOAP Autodiscover service.</span></span>
  
<span data-ttu-id="d902b-116">Die Themen des WSDL-Vorgangs in diesem Abschnitt bieten einen Überblick über die Funktionsweise des Vorgangs sowie Beispiele für Vorgangsanforderungen und-Antworten.</span><span class="sxs-lookup"><span data-stu-id="d902b-116">The WSDL operation topics in this section provide an overview of what the operation does and operation request and response examples.</span></span> <span data-ttu-id="d902b-117">Sie können die bereitgestellten Versionsinformationen verwenden, um zu bestimmen, ob die Features, die Sie verwenden möchten, in der Produktversion verfügbar sind, die Sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="d902b-117">You can use the version information provided to determine whether the features that you want to use are available in the product version that you are running.</span></span> <span data-ttu-id="d902b-118">Die Beispiele in den Vorgangs Themen helfen Ihnen auch, die Struktur der XML zu verstehen, die in den SOAP-Nachrichten enthalten ist, die an den und vom Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d902b-118">The examples in the operation topics also help you to understand the structure of the XML that is included in the SOAP messages that are sent to and from the server.</span></span>
  
<span data-ttu-id="d902b-119">Dieser Abschnitt enthält auch Beispiele und Beschreibungen der Nachrichten, die zum Abrufen von Konfigurationsinformationen für die AutoErmittlung mithilfe des SOAP-AutoErmittlungsdiensts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d902b-119">This section also provides examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the SOAP Autodiscover service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="d902b-120">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="d902b-120">In this section</span></span>
<span data-ttu-id="d902b-121"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="d902b-121"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="d902b-122">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d902b-122">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
    
- [<span data-ttu-id="d902b-123">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d902b-123">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)
    
- [<span data-ttu-id="d902b-124">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d902b-124">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
    
- [<span data-ttu-id="d902b-125">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d902b-125">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)
    
- [<span data-ttu-id="d902b-126">XML-Elemente der SOAP-AutoErmittlung für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="d902b-126">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="d902b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d902b-127">See also</span></span>


- [<span data-ttu-id="d902b-128">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="d902b-128">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="d902b-129">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="d902b-129">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="d902b-130">Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten</span><span class="sxs-lookup"><span data-stu-id="d902b-130">Use Autodiscover to find connection points</span></span>](https://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [<span data-ttu-id="d902b-131">Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="d902b-131">Get user settings from Exchange by using Autodiscover</span></span>](https://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [<span data-ttu-id="d902b-132">Abrufen von Domäneneinstellungen von einem Exchange-Server</span><span class="sxs-lookup"><span data-stu-id="d902b-132">Get domain settings from an Exchange server</span></span>](https://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [<span data-ttu-id="d902b-133">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="d902b-133">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

