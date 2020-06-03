---
title: XML-Elemente der SOAP-AutoErmittlung für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: Finden Sie XML-Elementreferenz Informationen für den SOAP autodiscover-Webdienst in Exchange.
ms.openlocfilehash: 3b88429488dbecd4ed7c3adf56462f34fa0d4b17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465184"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a><span data-ttu-id="5cf19-103">XML-Elemente der SOAP-AutoErmittlung für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="5cf19-103">SOAP Autodiscover XML elements for Exchange 2013</span></span>

<span data-ttu-id="5cf19-104">Finden Sie XML-Elementreferenz Informationen für den SOAP autodiscover-Webdienst in Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cf19-104">Find XML element reference information for the SOAP Autodiscover web service in Exchange.</span></span>
  
<span data-ttu-id="5cf19-105">Die Dokumentation in diesem Abschnitt basiert auf den SOAP-Auto Ermittlungs-XML-Elementinstanzen, die zwischen dem Client und dem Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="5cf19-105">The documentation in this section is based on the SOAP Autodiscover XML element instances that are sent between the client and server.</span></span> <span data-ttu-id="5cf19-106">Diese XML-Instanzen Dokumentation basiert auf den WSDL-und Schemadateien, die sich im virtuellen Verzeichnis befinden, in dem der SOAP-AutoErmittlungsdienst gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="5cf19-106">This XML instance documentation is based on the WSDL and schema files that are located in the virtual directory that hosts the SOAP Autodiscover service.</span></span> <span data-ttu-id="5cf19-107">Authentifizierte Benutzer können die WSDL-und Schemadateien durchsuchen, indem Sie eine URL verwenden, die einer der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="5cf19-107">Authenticated users can browse to the WSDL and schema files by using a URL that is similar to one of the following:</span></span>
  
- <span data-ttu-id="5cf19-108">Der Speicherort der WSDL-Datei: `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` oder`http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`</span><span class="sxs-lookup"><span data-stu-id="5cf19-108">The location of the WSDL file: `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` or `http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`</span></span>
    
- <span data-ttu-id="5cf19-109">Der Speicherort des Nachrichtenschemas: `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` oder`http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd`</span><span class="sxs-lookup"><span data-stu-id="5cf19-109">The location of the messages schema: `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` or `http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd`</span></span> 
    
<span data-ttu-id="5cf19-110">Der Speicherort der SOAP-Auto Ermittlungs-WSDL-und Schemadateien variiert je nach der Exchange-Installation.</span><span class="sxs-lookup"><span data-stu-id="5cf19-110">The location of the SOAP Autodiscover WSDL and schema files varies based on the Exchange installation.</span></span>
  
<span data-ttu-id="5cf19-111">Die Schemadatei Messages. xsd beschreibt die XML-Elemente, die in einem SOAP-Auto Ermittlungs Kopf und SOAP-Text gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5cf19-111">The messages.xsd schema file describes the XML elements that can be sent in an Autodiscover SOAP header and SOAP body.</span></span> <span data-ttu-id="5cf19-112">Diese Datei bietet eine allgemeine Übersicht darüber, was die XML-Struktur für eine bestimmte Anforderungs-Antwort-Nachrichten Interaktion sein kann.</span><span class="sxs-lookup"><span data-stu-id="5cf19-112">This file provides a general roadmap of what the XML structure can be for a given request-response message interaction.</span></span> <span data-ttu-id="5cf19-113">Die tatsächliche XML-Struktur, die zwischen dem Client und dem Server gesendet wird, basiert auf den Optionen und dem Kontext, in dem Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5cf19-113">The actual XML structure that is sent between the client and server is based on the options and the context in which it is used.</span></span> <span data-ttu-id="5cf19-114">In den Schemadateien wird definiert, welche XML-Daten möglich sind.</span><span class="sxs-lookup"><span data-stu-id="5cf19-114">The schema files define what XML is possible.</span></span> <span data-ttu-id="5cf19-115">Der tatsächliche Bereich von XML, der über den Draht gesendet wird, basiert auf dem aufgerufenen Vorgang, den angeforderten Informationen und den serverseitigen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5cf19-115">The actual range of XML that is sent over the wire is based on which operation is called, the requested information, and the server-side settings.</span></span> 
  
## <a name="related-sections"></a><span data-ttu-id="5cf19-116">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="5cf19-116">Related sections</span></span>

- [<span data-ttu-id="5cf19-117">Referenz zum SOAP-AutoErmittlungwebdienst für Exchange</span><span class="sxs-lookup"><span data-stu-id="5cf19-117">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)    
- [<span data-ttu-id="5cf19-118">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="5cf19-118">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)    
- [<span data-ttu-id="5cf19-119">Unified Messaging-Webdienst Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="5cf19-119">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="5cf19-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cf19-120">See also</span></span>

- [<span data-ttu-id="5cf19-121">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="5cf19-121">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="5cf19-122">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="5cf19-122">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="5cf19-123">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="5cf19-123">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

