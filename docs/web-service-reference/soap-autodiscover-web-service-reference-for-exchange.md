---
title: SOAP-Webdienst-Verweis für die AutoErmittlung für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: Hier finden Sie im Exchange Referenzinformationen für die SOAP-AutoErmittlungsdienst.
ms.openlocfilehash: 1cb24a8667c71028f3dead78d9fa533dc9547a64
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831514"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="7d846-103">SOAP-Webdienst-Verweis für die AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="7d846-103">SOAP Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="7d846-104">Hier finden Sie im Exchange Referenzinformationen für die SOAP-AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="7d846-104">Find reference information for the SOAP Autodiscover service in Exchange.</span></span>
  
<span data-ttu-id="7d846-105">Er bietet die Konfigurationsinformationen, die die Anwendung wird verwendet, um eine Verbindung mit einem Exchange-Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d846-105">The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="7d846-106">Den SOAP-AutoErmittlungsdienst können zum Senden von Nachrichten zwischen der Clientanwendung und dem Exchange-Server, um die Einstellungen zu suchen, dass die Anwendung zum Verbinden mit Exchange verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d846-106">You can use the SOAP Autodiscover service to send messages between the client application and the Exchange server to locate the settings the application will use to connect to Exchange.</span></span> <span data-ttu-id="7d846-107">Im Gegensatz zu den POX AutoErmittlungsdienst ermöglicht der SOAP-AutoErmittlungsdienst Batchanforderungen der AutoErmittlung für viele Benutzer Einstellungen und eine genauere Kontrolle über die Einstellungen in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7d846-107">Unlike the POX Autodiscover service, the SOAP Autodiscover service allows for batched Autodiscover requests for many users' settings and more granular control over which settings are returned in the response.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7d846-108">Clients, die Versionen von Exchange, beginnend mit Exchange Server 2010, wird empfohlen, dass Sie den SOAP-AutoErmittlungsdienst (anstelle des AutoErmittlungsdiensts POX) verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d846-108">For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service (instead of the POX Autodiscover service).</span></span> <span data-ttu-id="7d846-109">Clients, die auf Exchange 2007 abzielen müssen den AutoErmittlungsdienst POX verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d846-109">Clients that target Exchange 2007 have to use the POX Autodiscover service.</span></span> <span data-ttu-id="7d846-110">Es wird empfohlen, dass Clients, die .NET Framework verwenden, da es sich um eine stabile und gründlich getestete SOAP-AutoErmittlung-Client enthält die EWS Managed API verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d846-110">We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested SOAP Autodiscover client.</span></span> <span data-ttu-id="7d846-111">Weitere Informationen zu den EWS Managed API finden Sie unter [Erste Schritte mit EWS Managed API-Clientanwendungen](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7d846-111">For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="7d846-112">Dieser Abschnitt enthält Informationen über die XML-Elemente, die zwischen dem Client und Server gesendet werden, während der AutoErmittlung für SOAP-Anforderung Umleitung und benutzereinstellungen für, die in einer Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7d846-112">This section provides information about the XML elements that are sent between the client and server during SOAP Autodiscover request redirections and the user settings that are returned in a response.</span></span> <span data-ttu-id="7d846-113">XML-Elementreferenz enthält Übersichten was die Elemente bedeuten und eine Beschreibung der potenziellen Element Hierarchien, die das Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="7d846-113">The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that contain the element.</span></span> 
  
<span data-ttu-id="7d846-114">Die Artikel in diesem Abschnitt beschreiben die XML-Instanzen, die zwischen dem Client und Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d846-114">The articles in this section describe the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="7d846-115">Im virtuellen Verzeichnis des Servers, der den SOAP-AutoErmittlungsdienst hostet, kann das Schema, das diese Elemente beschreibt, gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="7d846-115">The schema that describes these elements can be found in the virtual directory of the server that hosts the SOAP Autodiscover service.</span></span>
  
<span data-ttu-id="7d846-116">Der WSDL-Vorgang, in den Themen in diesem Abschnitt bieten eine Übersicht über die auszuführende Operation wird und die Operation-Anfrage und-Antwort Beispiele.</span><span class="sxs-lookup"><span data-stu-id="7d846-116">The WSDL operation topics in this section provide an overview of what the operation does and operation request and response examples.</span></span> <span data-ttu-id="7d846-117">Sie können die Informationen zur Version bereitgestellt, um zu bestimmen, ob die Features, die Sie verwenden möchten in der Version des Produkts verfügbar sind, auf dem Sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7d846-117">You can use the version information provided to determine whether the features that you want to use are available in the product version that you are running.</span></span> <span data-ttu-id="7d846-118">Die Beispiele in den Themen Vorgang können Sie die XML-Struktur zu verstehen, die in die SOAP-Nachrichten enthalten ist, die zum und vom Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d846-118">The examples in the operation topics also help you to understand the structure of the XML that is included in the SOAP messages that are sent to and from the server.</span></span>
  
<span data-ttu-id="7d846-119">Dieser Abschnitt enthält auch Beispiele und eine Beschreibung der Nachrichten, die zum Abrufen von AutoErmittlung Konfigurationsinformationen mithilfe von SOAP-AutoErmittlungsdienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d846-119">This section also provides examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the SOAP Autodiscover service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="7d846-120">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="7d846-120">In this section</span></span>
<span data-ttu-id="7d846-121"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="7d846-121"></span></span>

- [<span data-ttu-id="7d846-122">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7d846-122">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
    
- [<span data-ttu-id="7d846-123">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7d846-123">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)
    
- [<span data-ttu-id="7d846-124">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7d846-124">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
    
- [<span data-ttu-id="7d846-125">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7d846-125">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)
    
- [<span data-ttu-id="7d846-126">SOAP-Autodiscover XML-Elemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7d846-126">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="7d846-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d846-127">See also</span></span>


- [<span data-ttu-id="7d846-128">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="7d846-128">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="7d846-129">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="7d846-129">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="7d846-130">Mithilfe von AutoErmittlung Verbindungspunkte suchen</span><span class="sxs-lookup"><span data-stu-id="7d846-130">Use Autodiscover to find connection points</span></span>](http://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [<span data-ttu-id="7d846-131">Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="7d846-131">Get user settings from Exchange by using Autodiscover</span></span>](http://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [<span data-ttu-id="7d846-132">Abrufen von domäneneinstellungen aus einem Exchange-server</span><span class="sxs-lookup"><span data-stu-id="7d846-132">Get domain settings from an Exchange server</span></span>](http://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [<span data-ttu-id="7d846-133">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="7d846-133">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

