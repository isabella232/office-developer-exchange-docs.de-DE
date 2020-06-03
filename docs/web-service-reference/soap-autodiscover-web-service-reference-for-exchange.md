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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468425"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a>Referenz zum SOAP-AutoErmittlungwebdienst für Exchange

Hier finden Sie Referenzinformationen für den SOAP-AutoErmittlungsdienst in Exchange.
  
Der AutoErmittlungsdienst stellt die Konfigurationsinformationen bereit, die Ihre Anwendung zum Erstellen einer Verbindung mit einem Exchange-Server verwendet. Sie können den SOAP-AutoErmittlungsdienst zum Senden von Nachrichten zwischen der Clientanwendung und dem Exchange-Server verwenden, um die Einstellungen zu finden, die von der Anwendung zum Herstellen einer Verbindung mit Exchange verwendet werden. Im Gegensatz zum POX-AutoErmittlungsdienst ermöglicht der SOAP-AutoErmittlungsdienst die Batchverarbeitung von Auto Ermittlungsanforderungen für viele Benutzereinstellungen und eine präzisere Kontrolle darüber, welche Einstellungen in der Antwort zurückgegeben werden. 
  
> [!NOTE]
> Für Clients, die auf Exchange-Versionen mit Exchange Server 2010 abzielen, wird empfohlen, den SOAP-AutoErmittlungsdienst (anstelle des POX-AutoErmittlungsdiensts) zu verwenden. Clients, die auf Exchange 2007 Zielen, müssen den POX-AutoErmittlungsdienst verwenden. Es wird empfohlen, dass Clients, die das .NET Framework verwenden, den verwaltete EWS-API verwenden, da er einen robusten und bewährten SOAP-Auto Ermittlungs Client enthält. Weitere Informationen zum verwaltete EWS-API finden Sie unter [Erste Schritte mit verwaltete EWS-API-Clientanwendungen](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
Dieser Abschnitt enthält Informationen zu den XML-Elementen, die zwischen dem Client und dem Server während der SOAP-Auto Ermittlungs Anforderungs Umleitung gesendet werden, und den Benutzereinstellungen, die in einer Antwort zurückgegeben werden. Die XML-Elementreferenz enthält Zusammenfassungen darüber, was die Elemente darstellen, und eine Beschreibung der potenziellen Element Hierarchien, die das-Element enthalten. 
  
In den Artikeln in diesem Abschnitt werden die XML-Instanzen beschrieben, die zwischen dem Client und dem Server gesendet werden. Das Schema, in dem diese Elemente beschrieben werden, befindet sich im virtuellen Verzeichnis des Servers, auf dem der SOAP-AutoErmittlungsdienst gehostet wird.
  
Die Themen des WSDL-Vorgangs in diesem Abschnitt bieten einen Überblick über die Funktionsweise des Vorgangs sowie Beispiele für Vorgangsanforderungen und-Antworten. Sie können die bereitgestellten Versionsinformationen verwenden, um zu bestimmen, ob die Features, die Sie verwenden möchten, in der Produktversion verfügbar sind, die Sie ausführen. Die Beispiele in den Vorgangs Themen helfen Ihnen auch, die Struktur der XML zu verstehen, die in den SOAP-Nachrichten enthalten ist, die an den und vom Server gesendet werden.
  
Dieser Abschnitt enthält auch Beispiele und Beschreibungen der Nachrichten, die zum Abrufen von Konfigurationsinformationen für die AutoErmittlung mithilfe des SOAP-AutoErmittlungsdiensts verwendet werden. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_InThisSection"> </a>

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)
    
- [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)
    
- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
    
- [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)
    
- [XML-Elemente der SOAP-AutoErmittlung für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch


- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten](https://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung](https://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [Abrufen von Domäneneinstellungen von einem Exchange-Server](https://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

