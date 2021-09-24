---
title: Referenz zum SOAP-AutoErmittlungwebdienst für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: Suchen Sie Referenzinformationen für den SOAP-AutoErmittlungsdienst in Exchange.
ms.openlocfilehash: 488862f5797abfd71d33c916fa96970ab300a2c0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521354"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a>Referenz zum SOAP-AutoErmittlungwebdienst für Exchange

Suchen Sie Referenzinformationen für den SOAP-AutoErmittlungsdienst in Exchange.
  
Der AutoErmittlungsdienst stellt die Konfigurationsinformationen bereit, die Ihre Anwendung zum Erstellen einer Verbindung mit einem Exchange Server verwendet. Sie können den SOAP-AutoErmittlungsdienst verwenden, um Nachrichten zwischen der Clientanwendung und dem Exchange Server zu senden, um die Einstellungen zu finden, die die Anwendung zum Herstellen einer Verbindung mit Exchange verwendet. Im Gegensatz zum POX-AutoErmittlungsdienst ermöglicht der SOAP-AutoErmittlungsdienst batchweise AutoErmittlungsanforderungen für die Einstellungen vieler Benutzer und eine präzisere Kontrolle darüber, welche Einstellungen in der Antwort zurückgegeben werden. 
  
> [!NOTE]
> Für Clients, die auf Versionen von Exchange ab Exchange Server 2010 abzielen, wird empfohlen, den SOAP-AutoErmittlungsdienst (anstelle des POX-AutoErmittlungsdiensts) zu verwenden. Clients für Exchange 2007 müssen den POX-AutoErmittlungsdienst verwenden. Clients, die die .NET Framework verwenden, sollten die verwaltete EWS-API verwenden, da sie einen robusten und gut getesteten SOAP-AutoErmittlungsclient enthält. Weitere Informationen zur verwalteten EWS-API finden Sie unter [Erste Schritte mit EWS Managed API-Clientanwendungen.](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx) 
  
Dieser Abschnitt enthält Informationen zu den XML-Elementen, die während der Umleitung der SOAP-AutoErmittlungsanforderung zwischen Client und Server gesendet werden, und zu den Benutzereinstellungen, die in einer Antwort zurückgegeben werden. Der XML-Elementverweis enthält Zusammenfassungen der Elemente und eine Beschreibung der potenziellen Elementhierarchien, die das Element enthalten. 
  
In den Artikeln in diesem Abschnitt werden die XML-Instanzen beschrieben, die zwischen dem Client und dem Server gesendet werden. Das Schema, das diese Elemente beschreibt, befindet sich im virtuellen Verzeichnis des Servers, der den SOAP-AutoErmittlungsdienst hostet.
  
Die WSDL-Vorgangsthemen in diesem Abschnitt bieten eine Übersicht über die Funktionsweise des Vorgangs sowie Beispiele für Vorgangsanfragen und -antworten. Anhand der bereitgestellten Versionsinformationen können Sie ermitteln, ob die features, die Sie verwenden möchten, in der ausgeführten Produktversion verfügbar sind. Die Beispiele in den Betriebsthemen helfen Ihnen auch, die Struktur der XML zu verstehen, die in den SOAP-Nachrichten enthalten ist, die an den und vom Server gesendet werden.
  
Dieser Abschnitt enthält auch Beispiele und Beschreibungen der Nachrichten, die zum Abrufen von AutoErmittlungs-Konfigurationsinformationen mithilfe des SOAP-AutoErmittlungsdiensts verwendet werden. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_InThisSection"> </a>

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)
    
- [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)
    
- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
    
- [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)
    
- [SOAP AutoDiscover XML-Elemente für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch


- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten](https://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung](https://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [Abrufen von Domäneneinstellungen von einem Exchange-Server](https://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

