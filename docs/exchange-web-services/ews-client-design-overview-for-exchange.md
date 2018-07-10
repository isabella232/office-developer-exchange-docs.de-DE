---
title: Übersicht über den EWS-Cliententwurf für Exchange
manager: sethgros
ms.date: 3/11/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: b26f67aa-7c66-4d7d-98b3-746f26ab37f4
description: Lernen Sie die Entwurfsaspekte für die Entwicklung mit EWS für Exchange kennen.
ms.openlocfilehash: ea0e1ad3f8402d19a6163f3320a2a17f08f3ea2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756837"
---
# <a name="ews-client-design-overview-for-exchange"></a><span data-ttu-id="890a0-103">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="890a0-103">EWS client design overview for Exchange</span></span>

<span data-ttu-id="890a0-104">Lernen Sie die Entwurfsaspekte für die Entwicklung mit EWS für Exchange kennen.</span><span class="sxs-lookup"><span data-stu-id="890a0-104">Learn about the design considerations for developing with EWS for Exchange.</span></span> 
  
<span data-ttu-id="890a0-p101">Dieser Artikel enthält eine Übersicht über das Entwerfen einer Exchange-Webdienste (EWS)-Anwendung. Mithilfe dieser Informationen können Sie bestimmen, ob EWS die richtigen API für Ihre Anwendung ist und (wenn dies der Fall ist) welche Art von Clientimplementierung verwendet werden sollte. Dieser Artikel enthält außerdem Informationen zu bewährten Methoden für das Entwerfen von Anwendungen mit Office 365, Exchange Online und Exchange-Versionen ab Exchange 2007 als Ziel in einer Codebasis sowie wichtige Entscheidungskriterien bei der Wahl von lokalen Exchange-Servern oder Exchange Online als Ziel.</span><span class="sxs-lookup"><span data-stu-id="890a0-p101">This article provides overview information about designing an Exchange Web Services (EWS) application. You can use this information to determine whether EWS is the right API for your application, and if so, what type of client implementation you should use. This article also provides best practice information for designing applications that can target Office 365, Exchange Online, and versions of Exchange starting with Exchange 2007, in one code base, and important decision points for targeting on-premises Exchange servers versus targeting Exchange Online.</span></span>
  
## <a name="is-ews-the-right-api-for-your-application"></a><span data-ttu-id="890a0-108">Ist EWS die richtige API für Ihre Anwendung?</span><span class="sxs-lookup"><span data-stu-id="890a0-108">Is EWS the right API for your application?</span></span>
<span data-ttu-id="890a0-109"><a name="IsEWSRight"> </a></span><span class="sxs-lookup"><span data-stu-id="890a0-109"></span></span>

<span data-ttu-id="890a0-p102">Bevor Sie mit der Entwicklung Ihrer Anwendung beginnen, müssen Sie überlegen, ob EWS die richtige API für Sie ist. Wenn Sie für Exchange Server oder Exchange Online entwickeln, ist EWS die bevorzugte Clientzugriffstechnologie. Die Entwicklung des Clientzugriffs für Exchange-Versionen ab Exchange 2007 konzentrierte sich primär auf EWS. Neue in Outlook implementierte Clientzugriffsfunktionen verwenden EWS, darunter auch die in Exchange 2007 eingeführten Features „Abwesend" und „Verfügbarkeit" sowie die Features „E-Mail-Info" und „GetRooms" aus Exchange 2010. Dies stellt eine konsequente Investition in EWS für interne und externe Partner dar, die Exchange-Clientanwendungen entwickeln.</span><span class="sxs-lookup"><span data-stu-id="890a0-p102">Before you begin to design your application, it is important to consider whether EWS is the right API for you. If you are developing against Exchange Server or Exchange Online, EWS is the preferred client access technology. Client access development for versions of Exchange starting with Exchange 2007 has primarily been focused on EWS. New client access functionality that is implemented in Outlook uses EWS, including the Out of Office (OOF) and Availability features introduced in Exchange 2007, and the MailTips and Get Rooms functionality introduced in Exchange 2010. This represents a committed investment in EWS for both internal and external partners who develop Exchange client applications.</span></span>
  
<span data-ttu-id="890a0-p103">EWS ist die primäre Clientzugriffs-API für Ihre Exchange-Clientanwendungen. In einigen Fällen empfiehlt sich jedoch eventuell der Einsatz anderer Exchange-APIs für die Entwicklung von Clientanwendungen. So bietet z. B. Exchange ActiveSync die folgenden Vorteile gegenüber EWS:</span><span class="sxs-lookup"><span data-stu-id="890a0-p103">EWS is the primary client access API for your Exchange client applications. However, in some cases, you might consider other Exchange APIs for client application development. For example, Exchange ActiveSync provides the following advantages over EWS:</span></span>
  
- <span data-ttu-id="890a0-118">Die XML-Struktur wurde mit Tokens versehen, um Exchange ActiveSync zu einem kompakteren Protokoll zu machen.</span><span class="sxs-lookup"><span data-stu-id="890a0-118">The XML structure has been tokenized to make Exchange ActiveSync a more compact protocol.</span></span>  
- <span data-ttu-id="890a0-119">Exchange ActiveSync enthält einen Richtlinienmechanismus zum Steuern des Clientzugriffs und zum Bereitstellen anderer robuster Unternehmenslösungen für mobile Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="890a0-119">Exchange ActiveSync contains a policy mechanism to control client access and to provide other robust enterprise mobile messaging solutions.</span></span>
    
> [!NOTE]
> <span data-ttu-id="890a0-120">Zum Entwickeln von Exchange ActiveSync-Clients benötigen Sie eine Lizenz.</span><span class="sxs-lookup"><span data-stu-id="890a0-120">You need a license in order to develop Exchange ActiveSync clients.</span></span> <span data-ttu-id="890a0-121">Informationen zu den Unterschieden zwischen Exchange ActiveSync und EWS finden Sie unter [Wählen zwischen Exchange ActiveSync und Exchange-Webdienste (EWS)](http://msdn.microsoft.com/de-de/library/dn144954%28v=exchg.140%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="890a0-121">To learn about the differences between Exchange ActiveSync and EWS, see [Choosing between Exchange ActiveSync and Exchange Web Services (EWS)](http://msdn.microsoft.com/de-de/library/dn144954%28v=exchg.140%29.aspx).</span></span> 
  
<span data-ttu-id="890a0-p105">MAPI-RPC über HTTP ist eine weitere Programmieroption für Exchange-Clientanwendungen. MAPI-RPC über HTTP bietet jedoch keine intuitive Schnittstelle für die Kommunikation zwischen Clients und dem Server.</span><span class="sxs-lookup"><span data-stu-id="890a0-p105">MAPI RPC over HTTP is another programmability option for Exchange client applications. However, MAPI RPC over HTTP does not provide an intuitive interface for communicating between clients and the server.</span></span>
  
<span data-ttu-id="890a0-124">Weitere Informationen zu Exchange-Entwicklungstechnologien finden Sie unter [Durchsuchen die EWS Managed API, EWS, und Web services im Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="890a0-124">For more information about Exchange development technologies, see [Explore the EWS Managed API, EWS, and web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span></span>
  
## <a name="options-for-ews-client-development"></a><span data-ttu-id="890a0-125">Optionen für die Entwicklung von EWS-Clients</span><span class="sxs-lookup"><span data-stu-id="890a0-125">Options for EWS client development</span></span>
<span data-ttu-id="890a0-126"><a name="EWSClientOptions"> </a></span><span class="sxs-lookup"><span data-stu-id="890a0-126"></span></span>

<span data-ttu-id="890a0-p106">Für die Entwicklung für Exchange mithilfe von EWS stehen mehrere Optionen zur Verfügung. Welche Option für Sie am besten geeignet ist, hängt von der Entwicklungsplattform, Tools, verfügbaren Implementierungen und Anwendungsanforderungen für Ihre Organisation ab. Im Folgenden finden Sie die vier primären Optionen, die zum Erstellen von EWS-Clientanwendungen zur Verfügung stehen:</span><span class="sxs-lookup"><span data-stu-id="890a0-p106">Several options are available for developing against Exchange by using EWS. The best option for you will depend on the development platform, tools, available implementations, and application requirements for your organization. The following are the four primary options that are available for building EWS client applications:</span></span>
  
- <span data-ttu-id="890a0-130">Verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="890a0-130">The EWS Managed API</span></span>
- <span data-ttu-id="890a0-131">Java-API der EWS</span><span class="sxs-lookup"><span data-stu-id="890a0-131">The EWS Java API</span></span>
- <span data-ttu-id="890a0-132">Automatisch generierte EWS-Proxys</span><span class="sxs-lookup"><span data-stu-id="890a0-132">The EWS autogenerated proxies</span></span>
- <span data-ttu-id="890a0-133">Benutzerdefinierte EWS-Client-API</span><span class="sxs-lookup"><span data-stu-id="890a0-133">A custom EWS client API</span></span>
    
### <a name="ews-managed-api"></a><span data-ttu-id="890a0-134">Verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="890a0-134">EWS Managed API</span></span>

<span data-ttu-id="890a0-p107">Die [verwaltete EWS-API](http://aka.ms/ews-managed-api-readme) ist ein benutzerdefinierter Webdienstclient und die standardmäßige Clientzugriffs-API für .NET Framework-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="890a0-p107">The [EWS Managed API](http://aka.ms/ews-managed-api-readme) is a custom web service client. It is the standard client access API for .NET Framework applications.</span></span> 
  
<span data-ttu-id="890a0-137">Im Folgenden werden einige Vorteile der Verwendung der verwalteten EWS-API aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="890a0-137">The following are some of the benefits of using the EWS Managed API:</span></span>
  
- <span data-ttu-id="890a0-138">Sie bietet ein intuitives Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="890a0-138">It provides an intuitive object model.</span></span>   
- <span data-ttu-id="890a0-139">Sie abstrahiert die Komplexität der Dienstbeschreibung in den WSDL- und Schemadateien.</span><span class="sxs-lookup"><span data-stu-id="890a0-139">It abstracts the complexities of the service description in the WSDL and schema files.</span></span>   
- <span data-ttu-id="890a0-140">Sie enthält clientseitige Geschäftslogik.</span><span class="sxs-lookup"><span data-stu-id="890a0-140">It includes client-side business logic.</span></span>   
- <span data-ttu-id="890a0-141">Sie verarbeitet die Webanforderungen und -antworten sowie die Objektserialisierung und -deserialisierung.</span><span class="sxs-lookup"><span data-stu-id="890a0-141">It handles the web requests and responses and object serialization and deserialization.</span></span>   
- <span data-ttu-id="890a0-142">Sie wird von Microsoft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="890a0-142">It is Microsoft-supported.</span></span>
    
<span data-ttu-id="890a0-p108">Beachten Sie jedoch, dass die verwaltete EWS-API keine vollständige Lösung ist. Einige Funktionen sind nicht in die verwaltete EWS-API implementiert. Obwohl die verwaltete EWS-API nicht alle EWS-Funktionen enthält, kann sie aus den folgenden Gründen trotzdem die beste Wahl für die Entwicklung von Clientanwendungen sein:</span><span class="sxs-lookup"><span data-stu-id="890a0-p108">Note, however, that the EWS Managed API is not a complete solution. Some functionality is not implemented in the EWS Managed API. Although the EWS Managed API doesn't implement all EWS functionality, it might be the best choice for your client application development, for the following reasons:</span></span>
  
- <span data-ttu-id="890a0-146">Sie können das .NET Framework für die Entwicklung verwenden.</span><span class="sxs-lookup"><span data-stu-id="890a0-146">You can use the .NET Framework for development.</span></span>
- <span data-ttu-id="890a0-147">Sie implementiert die AutoErmittlung sowie die meisten Teile des EWS-Objektmodells.</span><span class="sxs-lookup"><span data-stu-id="890a0-147">It implements Autodiscover in addition to most parts of the EWS object model.</span></span>
- <span data-ttu-id="890a0-148">Sie implementiert clientseitige Geschäftslogik für die Zusammenarbeit mit EWS in der [ExchangeService](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Klasse.</span><span class="sxs-lookup"><span data-stu-id="890a0-148">It implements client-side business logic for working with EWS, in the [ExchangeService](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) class.</span></span> 
    
<span data-ttu-id="890a0-149">Sie können die EWS-Webdienst-API aus folgenden Gründen anstelle der verwalteten EWS-API verwenden:</span><span class="sxs-lookup"><span data-stu-id="890a0-149">You might choose to use the EWS web service API instead of the EWS Managed API for any of the following reasons:</span></span>
  
- <span data-ttu-id="890a0-150">.NET Framework wird von Ihrer Anwendung nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="890a0-150">Your application does not use the .NET Framework.</span></span> 
- <span data-ttu-id="890a0-151">Sie möchten die verwaltete EWS-API-Assembly nicht verteilen.</span><span class="sxs-lookup"><span data-stu-id="890a0-151">You don't want to distribute the EWS Managed API assembly.</span></span> 
- <span data-ttu-id="890a0-152">Ihre Anwendung verwendet Features, die nicht in der verwalteten EWS-API implementiert sind.</span><span class="sxs-lookup"><span data-stu-id="890a0-152">Your application uses features that aren't implemented in the EWS Managed API.</span></span>
    
<span data-ttu-id="890a0-153">Weitere Informationen finden Sie unter [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](get-started-with-ews-managed-api-client-applications.md).</span><span class="sxs-lookup"><span data-stu-id="890a0-153">To learn more, see [Get started with EWS Managed API client applications](get-started-with-ews-managed-api-client-applications.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="890a0-154">Die EWS Managed API ist jetzt als open-Source-Projekt auf [GitHub](http://aka.ms/ews-managed-api-github)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="890a0-154">The EWS Managed API is now available as an open source project on [GitHub](http://aka.ms/ews-managed-api-github).</span></span> <span data-ttu-id="890a0-155">Sie können die open-Source-Bibliothek zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="890a0-155">You can use the open source library to:</span></span> 
> - <span data-ttu-id="890a0-156">Implementieren von Programmfehlerbehebungen und Verbesserungen in die API</span><span class="sxs-lookup"><span data-stu-id="890a0-156">Contribute bug fixes and enhancements to the API.</span></span> 
> - <span data-ttu-id="890a0-157">Abrufen von Fehlerbehebungen und Verbesserungen, bevor diese in einer offiziellen Version verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="890a0-157">Get fixes and enhancements before they are available in an official release.</span></span>
> - <span data-ttu-id="890a0-158">Zugreifen auf die umfassendste und aktuellste Implementierung der API, um sie als Referenz zu verwenden oder neue Bibliotheken auf neuen Plattformen zu erstellen</span><span class="sxs-lookup"><span data-stu-id="890a0-158">Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms.</span></span>
> 
> <span data-ttu-id="890a0-159">Wir freuen uns auf Ihre [Beiträge](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) über GitHub.</span><span class="sxs-lookup"><span data-stu-id="890a0-159">We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) via GitHub.</span></span> 
  
### <a name="ews-java-api"></a><span data-ttu-id="890a0-160">Java-API der EWS</span><span class="sxs-lookup"><span data-stu-id="890a0-160">EWS Java API</span></span>

<span data-ttu-id="890a0-p110">Die Java-API der EWS ist ein Open Source-Projekt auf [GitHub](https://github.com/OfficeDev/ews-java-api), das von der Community aktualisiert und erweitert werden kann. Sie ähnelt stilistisch der [verwalteten EWS-API](http://msdn.microsoft.com/de-de/library/office/jj220535%28v=exchg.80%29.aspx) und verwendet EWS-SOAP-Anforderungen und - Antworten über das Netzwerk. Obwohl Sie mit der Java-API der EWS nicht auf alle [EWS-SOAP-Vorgänge](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) zugreifen können, setzen wir mit der [aktuellen Erstellung](http://blogs.office.com/2014/08/28/open-sourcing-exchange-web-services-ews-java-api/) des Open Source-Projekts auf die Community, um diese Lücke zu schließen. Beachten Sie, dass der Microsoft-Support mit einem entsprechenden Supportvertrag alle Fragen im Zusammenhang mit dem EWS-SOAP-Protokoll, nicht jedoch mit der Java-API für EWS beantwortet. Die Java-API für EWS steht zum Download und für Communitybeiträge auf [GitHub](https://github.com/OfficeDev/ews-java-api) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="890a0-p110">The EWS Java API is an open source project on [GitHub](https://github.com/OfficeDev/ews-java-api) that can be updated and extended by the community. It is stylistically similar to the [EWS Managed API](http://msdn.microsoft.com/de-de/library/office/jj220535%28v=exchg.80%29.aspx) and uses EWS SOAP requests and responses over the wire. Although you can't access all [EWS SOAP operations](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) by using the EWS Java API, with the [recent creation](http://blogs.office.com/2014/08/28/open-sourcing-exchange-web-services-ews-java-api/) of the open source project, we are looking to the community to bridge this gap. Note that Microsoft Support, with an appropriate support contract, will address any questions related to the EWS SOAP protocol but not the EWS Java API itself. The EWS Java API is available for download and community contribution on [GitHub](https://github.com/OfficeDev/ews-java-api).</span></span>
  
### <a name="ews-autogenerated-proxies"></a><span data-ttu-id="890a0-166">Automatisch generierte EWS-Proxys</span><span class="sxs-lookup"><span data-stu-id="890a0-166">EWS autogenerated proxies</span></span>

<span data-ttu-id="890a0-p111">Automatisch generierte Client-APIs werden von den WSDL- und XML-Schemadefinitionen von EWS generiert. Client-Objektmodellgeneratoren sind für viele Sprachen verfügbar. Im Allgemeinen verwalten die automatisch generierten Objektmodelle die Objektserialisierung und -deserialisierung. Sie enthalten keine Geschäftslogik. Bei der automatischen Generierung werden häufig Artefakte erstellt, die die intuitive Nutzung des Objektmodells beeinträchtigen. Die Unterstützung für Exchange deckt den vom Client gesendeten und empfangenen XML-Code ab, nicht jedoch den des Objektmodells.</span><span class="sxs-lookup"><span data-stu-id="890a0-p111">Autogenerated client APIs are generated from the EWS WSDL and XML schema definitions. Client object model generators are available for many languages. In general, the autogenerated object models manage object serialization and deserialization. They do not include business logic and the autogeneration process often creates artifacts that make the object model less intuitive to use. Exchange support covers the XML that is sent and received by the client but not the object model.</span></span>
  
### <a name="custom-ews-client-api"></a><span data-ttu-id="890a0-172">Benutzerdefinierte EWS-Client-API</span><span class="sxs-lookup"><span data-stu-id="890a0-172">Custom EWS client API</span></span>

<span data-ttu-id="890a0-p112">Für einige Anwendungen, die nur einen kleinen Satz EWS-Funktionen verwenden, können Sie eine benutzerdefinierte Client-API für die Kommunikation mit Exchange erstellen. Dies ermöglicht es Ihnen, weniger Systemressourcen zu verbrauchen. Dies ist nützlich für Clients, die auf Geräten mit beschränktem Speicher ausgeführt werden, beispielsweise Clients mit .NET Micro Framework.</span><span class="sxs-lookup"><span data-stu-id="890a0-p112">For some applications that use a small set of EWS functionality, you might create a custom client API to communicate with Exchange. This enables you to consume fewer system resources. This is useful for clients that run on memory-constrained devices, such as clients running the .NET Micro Framework.</span></span>
  
## <a name="ews-client-features"></a><span data-ttu-id="890a0-176">EWS-Clientfeatures</span><span class="sxs-lookup"><span data-stu-id="890a0-176">EWS client features</span></span>
<span data-ttu-id="890a0-177"><a name="EWSFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="890a0-177"></span></span>

<span data-ttu-id="890a0-p113">Unabhängig von der gewählten Entwicklungsoption sollten Sie überlegen, wie EWS-Features im Client implementiert werden. Die Verfügbarkeit von Features basiert auf der EWS-Schemaversion, für die die Anwendung entwickelt wird. Da EWS-Schemas abwärts- und aufwärtskompatibel sind, können Anwendungen, die für eine frühere Schemaversion wie z. B. Exchange Server 2007 SP1 erstellt wurden, auch für höhere Schemaversionen verwendet werden, wie z. B. den Exchange Server 2013 SP1-Dienst sowie Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="890a0-p113">Regardless of the development option that you choose, you should consider how EWS features are implemented in your client. Feature availability is based on the EWS schema version that your application targets. Because EWS schemas are backward- and forward-compatible, if you create an application that targets an earlier schema version, such as Exchange Server 2007 SP1, your application will also work against a later schema version, such as the Exchange Server 2013 SP1 service, as well as Exchange Online.</span></span> 
  
<span data-ttu-id="890a0-p114">Da Features und Featureupdates vom Schema gesteuert werden, empfehlen wir die Verwendung der frühesten gemeinsamen Codebasis für die EWS-Features, die Sie in der Clientanwendung implementieren möchten. Viele Anwendungen können die Version Exchange2007_SP1 als Ziel verwenden, da das Schema von Exchange 2007 SP1 fast alle Exchange-Kernfunktionen für die Arbeit mit Elementen und Ordnern im Exchange-Informationsspeicher enthält. Es wird empfohlen, Codeverzweigungen für jede EWS-Schemaversion zu verwalten. Im Folgenden werden die derzeit verfügbaren Schemaversionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="890a0-p114">Because features and feature updates are driven by the schema, we recommend that you use the earliest common code base that targets the EWS features that you want to implement in your client application. Many applications can target the Exchange2007_SP1 version, because the Exchange 2007 SP1 schema contains almost all the core Exchange functionality for working with items and folders in the Exchange store. We recommend that you maintain code forks for each EWS schema version. The following are the schema versions that are currently available.</span></span> 
  
```XML
  <xs:simpleType name="ExchangeVersionType">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Exchange2007" />
      <xs:enumeration value="Exchange2007_SP1" />
      <xs:enumeration value="Exchange2010" />
      <xs:enumeration value="Exchange2010_SP1" />
      <xs:enumeration value="Exchange2010_SP2" />
      <xs:enumeration value="Exchange2013" />
      <xs:enumeration value="Exchange2013_SP1" />
    </xs:restriction>
  </xs:simpleType>
```

<span data-ttu-id="890a0-185">Die Schemaversionen werden im einfachen **ExchangeVersionType** -Typ verwaltet.</span><span class="sxs-lookup"><span data-stu-id="890a0-185">The schema versions are maintained in the **ExchangeVersionType** simple type.</span></span> 
  
<span data-ttu-id="890a0-186">Informationen zu den in den einzelnen EWS-Schemaversionen verfügbaren Features finden Sie unter [EWS-Schemaversionen in Exchange](ews-schema-versions-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="890a0-186">For information about the features that are available in each EWS schema version, see [EWS schema versions in Exchange](ews-schema-versions-in-exchange.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="890a0-187">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="890a0-187">In this section</span></span>
<span data-ttu-id="890a0-188"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="890a0-188"></span></span>

- [<span data-ttu-id="890a0-189">Verfügbarkeit von Web Service-API in Exchange und die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="890a0-189">Web service API feature availability in Exchange and the EWS Managed API</span></span>](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
    
- [<span data-ttu-id="890a0-190">EWS-Schemaversionen in Exchange</span><span class="sxs-lookup"><span data-stu-id="890a0-190">EWS schema versions in Exchange</span></span>](ews-schema-versions-in-exchange.md)
    
- [<span data-ttu-id="890a0-191">Konfigurationsoptionen für EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="890a0-191">Configuration options for EWS in Exchange</span></span>](configuration-options-for-ews-in-exchange.md)
    
- [<span data-ttu-id="890a0-192">Vergleich der Exchange Online und Exchange lokalen Clientprogrammierung</span><span class="sxs-lookup"><span data-stu-id="890a0-192">Comparing Exchange Online and Exchange on-premises client programming</span></span>](comparing-exchange-online-and-exchange-on-premises-client-programming.md)
    
- [<span data-ttu-id="890a0-193">EWS-Einschränkung in Exchange</span><span class="sxs-lookup"><span data-stu-id="890a0-193">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    
- [<span data-ttu-id="890a0-194">Redistribution Anforderungen für die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="890a0-194">Redistribution requirements for the EWS Managed API</span></span>](redistribution-requirements-for-the-ews-managed-api.md)
    
- [<span data-ttu-id="890a0-195">Instrumentieren Client-Anfragen für EWS und REST in Exchange</span><span class="sxs-lookup"><span data-stu-id="890a0-195">Instrumenting client requests for EWS and REST in Exchange</span></span>](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="890a0-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="890a0-196">See also</span></span>
 
- [<span data-ttu-id="890a0-197">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="890a0-197">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
- [<span data-ttu-id="890a0-198">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="890a0-198">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md) 
- [<span data-ttu-id="890a0-199">EWS-Anwendungstypen</span><span class="sxs-lookup"><span data-stu-id="890a0-199">EWS application types</span></span>](ews-application-types.md)
    

