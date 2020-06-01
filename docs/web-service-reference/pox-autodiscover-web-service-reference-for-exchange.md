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
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a>POX AutoErmittlung Webdienstverweis für Exchange

Hier finden Sie Referenzinformationen für den POX-AutoErmittlungsdienst in Exchange.
  
Der AutoErmittlungsdienst stellt die Konfigurationsinformationen bereit, die Ihre Anwendung zum Erstellen einer Verbindung mit einem Exchange-Server verwendet. Sie können den "Plain Old XML" (POX)-AutoErmittlungsdienst verwenden, um Nachrichten zu senden, die nur aus XML-Nutzdaten bestehen, ohne einschließende SOAP-Umschläge, um die Einstellungen zu finden, die eine Clientanwendung zum Herstellen einer Verbindung mit Exchange benötigen muss.
  
> [!NOTE]
> Für Clients, die auf Versionen von Exchange ab Exchange Server 2010 abzielen, wird empfohlen, den SOAP-AutoErmittlungsdienst anstelle des POX-AutoErmittlungsdiensts zu verwenden. Clients, die auf Exchange 2007 Zielen, müssen den POX-AutoErmittlungsdienst verwenden. Es wird empfohlen, dass Clients, die das .NET Framework verwenden, den verwaltete EWS-API verwenden, da er einen robusten und bewährten POX-Auto Ermittlungs Client enthält. Weitere Informationen zum verwaltete EWS-API finden Sie unter [Erste Schritte mit verwaltete EWS-API-Clientanwendungen](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
Dieser Abschnitt enthält Informationen zu den XML-Elementen, die zwischen dem Client und dem Server während POX Auto Ermittlungs Anforderungs Umleitungen und den Benutzereinstellungen gesendet werden, die in einer Antwort zurückgegeben werden. Die XML-Elementreferenz enthält Zusammenfassungen darüber, was die Elemente darstellen, und eine Beschreibung der potenziellen Element Hierarchien, die das Element verwenden. In dieser Dokumentation werden die XML-Instanzen erläutert, die zwischen Client und Server gesendet werden. Der POX-AutoErmittlungsdienst verfügt nicht über ein explizites Schema.
  
Die Artikel in diesem Abschnitt enthalten Beispiele und Beschreibungen der Nachrichten, die zum Abrufen von Konfigurationsinformationen für die AutoErmittlung mithilfe des POX-AutoErmittlungsdiensts verwendet werden. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_InThisSection"> </a>

- [POX-Anforderung der AutoErmittlung für Exchange](pox-autodiscover-request-for-exchange.md)
    
- [POX-Auto Ermittlungs Antwort für Exchange](pox-autodiscover-response-for-exchange.md)
    
- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)   
- [Referenz zum SOAP-AutoErmittlungwebdienst für Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

