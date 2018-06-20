---
title: SOAP-Autodiscover XML-Elemente für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: Hier finden Sie im Exchange XML-Element Referenzinformationen für die AutoErmittlung SOAP-Webdienst.
ms.openlocfilehash: 7201ef33060691df70b63d06b2045e1120b0610f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831517"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a><span data-ttu-id="6ee17-103">SOAP-Autodiscover XML-Elemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="6ee17-103">SOAP Autodiscover XML elements for Exchange 2013</span></span>

<span data-ttu-id="6ee17-104">Hier finden Sie im Exchange XML-Element Referenzinformationen für die AutoErmittlung SOAP-Webdienst.</span><span class="sxs-lookup"><span data-stu-id="6ee17-104">Find XML element reference information for the SOAP Autodiscover web service in Exchange.</span></span>
  
<span data-ttu-id="6ee17-105">In diesem Abschnitt die Dokumentation basiert auf die SOAP-AutoErmittlung-XML-Element-Instanzen, die zwischen dem Client und Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ee17-105">The documentation in this section is based on the SOAP Autodiscover XML element instances that are sent between the client and server.</span></span> <span data-ttu-id="6ee17-106">Dieses XML-Instanz Dokumentation basiert auf die WSDL-Datei und Schema-Dateien, die sich in dem virtuellen Verzeichnis befinden, die den SOAP-AutoErmittlungsdienst gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="6ee17-106">This XML instance documentation is based on the WSDL and schema files that are located in the virtual directory that hosts the SOAP Autodiscover service.</span></span> <span data-ttu-id="6ee17-107">Authentifizierte Benutzer können Sie die WSDL-Datei und Schema-Dateien suchen, mithilfe einen URL, die einer der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="6ee17-107">Authenticated users can browse to the WSDL and schema files by using a URL that is similar to one of the following:</span></span>
  
- <span data-ttu-id="6ee17-108">http://\<Yourclientaccessserver\>.com/autodiscover/services.wsdl oder http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/services.wsdl – den Speicherort der WSDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="6ee17-108">http://\<yourclientaccessserver\>.com/autodiscover/services.wsdl or http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/services.wsdl — The location of the WSDL file.</span></span>
    
- <span data-ttu-id="6ee17-109">http://\<Yourclientaccessserver\>.com/autodiscover/messages.xsd oder http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/messages.xsd – die Position des Schemas Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="6ee17-109">http://\<yourclientaccessserver\>.com/autodiscover/messages.xsd or http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/messages.xsd — The location of the messages schema.</span></span>
    
<span data-ttu-id="6ee17-110">Der Speicherort der Dateien SOAP-AutoErmittlung WSDL und Schema richtet sich nach der Installation von Exchange.</span><span class="sxs-lookup"><span data-stu-id="6ee17-110">The location of the SOAP Autodiscover WSDL and schema files varies based on the Exchange installation.</span></span>
  
<span data-ttu-id="6ee17-111">Die messages.xsd-Schemadatei beschreibt die XML-Elemente, die in einer AutoErmittlung SOAP-Header und SOAP-Body gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6ee17-111">The messages.xsd schema file describes the XML elements that can be sent in an Autodiscover SOAP header and SOAP body.</span></span> <span data-ttu-id="6ee17-112">Diese Datei enthält eine allgemeine Übersicht über was die XML-Struktur für die Interaktion einer bestimmten Anforderung und Antwort-Nachricht werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ee17-112">This file provides a general roadmap of what the XML structure can be for a given request-response message interaction.</span></span> <span data-ttu-id="6ee17-113">Die eigentliche XML-Struktur, die zwischen dem Client und Server gesendet wird basiert auf die Optionen und den Kontext, in dem sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ee17-113">The actual XML structure that is sent between the client and server is based on the options and the context in which it is used.</span></span> <span data-ttu-id="6ee17-114">Die Schemadateien definieren, was XML möglich ist.</span><span class="sxs-lookup"><span data-stu-id="6ee17-114">The schema files define what XML is possible.</span></span> <span data-ttu-id="6ee17-115">Der Bereich der XML-Code, die über das Netzwerk gesendet wird basiert auf welche Operation aufgerufen wird, die angeforderten Informationen und die serverseitige-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="6ee17-115">The actual range of XML that is sent over the wire is based on which operation is called, the requested information, and the server-side settings.</span></span> 
  
## <a name="related-sections"></a><span data-ttu-id="6ee17-116">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="6ee17-116">Related sections</span></span>
<span data-ttu-id="6ee17-117"><a name="bk_RelatedSections"> </a></span><span class="sxs-lookup"><span data-stu-id="6ee17-117"></span></span>

- [<span data-ttu-id="6ee17-118">SOAP-Webdienst-Verweis für die AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="6ee17-118">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [<span data-ttu-id="6ee17-119">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="6ee17-119">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
    
- [<span data-ttu-id="6ee17-120">Unified Messaging-webdienstreferenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="6ee17-120">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="6ee17-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ee17-121">See also</span></span>

- [<span data-ttu-id="6ee17-122">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="6ee17-122">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="6ee17-123">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="6ee17-123">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="6ee17-124">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="6ee17-124">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

