---
title: EWS-XML-Elemente in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- Exchange
api_type:
- schema
ms.assetid: 4653466a-a596-456f-bbff-7da4ef1d18d3
description: Suchen nach Verweisinformationen für EWS-XML-Elemente in Exchange
localization_priority: Priority
ms.openlocfilehash: 29b90ad137141e30484ef804b6fcb6bb049ef3e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526116"
---
# <a name="ews-xml-elements-in-exchange"></a><span data-ttu-id="efbaf-103">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="efbaf-103">EWS XML elements in Exchange</span></span>

<span data-ttu-id="efbaf-104">Suchen nach Verweisinformationen für EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="efbaf-104">Find reference information for the EWS XML elements in Exchange.</span></span>
  
<span data-ttu-id="efbaf-105">Exchange-Webdienste ist ein SOAP-basierter Webdienst, was bedeutet, dass die Anforderungs-und Antwortnachrichten, die zwischen dem Client und dem Server gesendet werden, aus XML-Elementen bestehen.</span><span class="sxs-lookup"><span data-stu-id="efbaf-105">Exchange Web Services (EWS) is a SOAP-based web service, which means that the request and response messages that are sent between the client and server are comprised of XML elements.</span></span> <span data-ttu-id="efbaf-106">Die Dokumentation in diesem Abschnitt basiert auf den XML-Instanzen, die zwischen dem Client und dem Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="efbaf-106">The documentation in this section is based on the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="efbaf-107">Die XML-Instanzen werden in den WSDL-und Schemadateien definiert, die sich im virtuellen Verzeichnis befinden, in dem EWS gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="efbaf-107">The XML instances are defined in the WSDL and schema files that are located in the virtual directory that hosts EWS.</span></span> <span data-ttu-id="efbaf-108">Wenn Sie ein authentifizierter Benutzer sind, können Sie zu den WSDL-und Schemadateien navigieren, indem Sie die folgenden URLs verwenden, wobei \<yourclientaccessserver\> der Name des Client Zugriffsservers lautet:</span><span class="sxs-lookup"><span data-stu-id="efbaf-108">If you are an authenticated user, you can browse to the WSDL and schema files by using the following URLs, where \<yourclientaccessserver\> is the name of your Client Access server:</span></span>
  
- <span data-ttu-id="efbaf-109">http:// \<yourclientaccessserver\> . com/EWS/Services. WSDL – der Speicherort der WSDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="efbaf-109">http://\<yourclientaccessserver\>.com/ews/services.wsdl — The location of the WSDL file.</span></span>
    
- <span data-ttu-id="efbaf-110">http:// \<yourclientaccessserver\> . com/EWS/Messages. xsd – der Speicherort des Nachrichtenschemas.</span><span class="sxs-lookup"><span data-stu-id="efbaf-110">http://\<yourclientaccessserver\>.com/ews/messages.xsd — The location of the messages schema.</span></span>
    
- <span data-ttu-id="efbaf-111">http:// \<yourclientaccessserver\> . com/EWS/Types. xsd – der Speicherort des Typen Schemas.</span><span class="sxs-lookup"><span data-stu-id="efbaf-111">http://\<yourclientaccessserver\>.com/ews/types.xsd — The location of the types schema.</span></span>
    
<span data-ttu-id="efbaf-p102">Die Schemadateien, die die EWS-XML-Elemente beschreiben, stellen eine allgemeine Roadmap der XML-Struktur bereit, die für Anforderung-Antwort-Nachrichteninteraktionen möglich sind. Die tatsächliche XML-Struktur, die zwischen Client und Server gesendet wird, unterscheidet sich entsprechend des aufgerufenen Vorgangs, der angeforderten Informationen und der serverseitigen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="efbaf-p102">The schema files that describe the EWS XML elements provide a general roadmap of the XML structure that is possible for request-response message interactions. The actual XML structure that is sent between client and server varies according to the operation that is called, the information requested, and the server-side settings.</span></span>
  
<span data-ttu-id="efbaf-p103">Die EWS-WSDL-Datei „services.wsdl" erfüllt nicht vollständig den WSDL-Standard, da sie keine WSDL-Dienstdefinition enthält. Das liegt daran, dass EWS nicht dafür ausgelegt ist, auf einem Computer gehostet zu werden, der über eine vordefinierte Adresse verfügt. Sie können den AutoErmittlung-Dienst verwenden, um die EWS-Endpunktadresse abzurufen. Einige clientseitige Objektmodellgeneratoren analysieren die WSDL-Datei und können einen Fehlerstatus ausgeben, da die WSDL-Datei keine WSDL-Dienstdefinition enthält. Wenn der Objektmodellgenerator einen Fehler ausgibt, können Sie eine Platzhalter-WSDL-Dienstdefinition einfügen.</span><span class="sxs-lookup"><span data-stu-id="efbaf-p103">The EWS WSDL file, services.wsdl, does not fully conform to the WSDL standard because it does not include a WSDL service definition. This is because EWS is not designed to be hosted on a computer that has a predefined address. You can use the Autodiscover service to get the EWS endpoint address. Some client-side object model generators parse the WSDL and can encounter an error condition because the WSDL file does not contain a WSDL service definition. If your object model generator encounters an error, you can insert a placeholder WSDL service definition.</span></span>
  
> [!TIP]
> <span data-ttu-id="efbaf-p104">[!TIPP] Wenn Sie zum Entwickeln einer Anwendung .NET Framework einsetzen, empfehlen wir, die [verwaltete EWS-API](http://aka.ms/ews-managed-api-readme) zu verwenden, statt einen Objektmodellgenerator. Die verwaltete EWS-API stellt ein einfaches Objektmodell zum Verarbeiten der Serialisierung und Deserialisierung der EWS-XML. Weitere Informationen finden Sie unter [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="efbaf-p104">If you are using the .NET Framework to develop your application, we recommend that you use the [EWS Managed API](http://aka.ms/ews-managed-api-readme), rather than an object model generator. The EWS Managed API provides an easy-to-use object model to handle the serialization and deserialization of the EWS XML. For more information, see [Get started with EWS Managed API client applications](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="efbaf-p105">Die messages.xsd-Schemadatei enthält die Elementdefinitionen für Elemente auf oberster Ebene im SOAP-Text. Mit Ausnahme der Fehlerantwortcodes dienen die meisten Definitionen in der Datei „messages.xsd" für einen bestimmten Vorgang. Das types.xsd-Schema enthält die Definitionen für die SOAP-Header und alle häufig verwendeten Definitionen, die bei mehreren Vorgängen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="efbaf-p105">The messages.xsd schema file contains the element definitions for the top-level elements in the SOAP body. With the exception of the error response codes, most of the definitions in messages.xsd are specific to an operation. The types.xsd schema contains the definitions for the SOAP headers and all the common definitions that are shared across operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="efbaf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efbaf-125">See also</span></span>

- [<span data-ttu-id="efbaf-126">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="efbaf-126">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="efbaf-127">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="efbaf-127">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="efbaf-128">Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="efbaf-128">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [<span data-ttu-id="efbaf-129">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="efbaf-129">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
- [<span data-ttu-id="efbaf-130">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="efbaf-130">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
    

