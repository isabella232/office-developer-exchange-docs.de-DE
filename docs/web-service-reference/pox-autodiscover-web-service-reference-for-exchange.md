---
title: POX AutoErmittlung Webdienstverweis für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 877152f0-f4b1-4f63-b2ce-924f4bdf2d20
description: Hier finden Sie Referenzinformationen für den POX-AutoErmittlungsdienst in Exchange.
ms.openlocfilehash: b28ea64a82960a84dee06c5055ee915614f4fde7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516419"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a>POX AutoErmittlung Webdienstverweis für Exchange

Hier finden Sie Referenzinformationen für den POX-AutoErmittlungsdienst in Exchange.
  
Der AutoErmittlungsdienst stellt die Konfigurationsinformationen bereit, die ihre Anwendung zum Erstellen einer Verbindung mit einem Exchange Server verwendet. Sie können den POX-AutoErmittlungsdienst (Plain Old XML) verwenden, um Nachrichten zu senden, die nur aus XML-Nutzlasten bestehen, ohne SOAP-Umschläge einzuschließen, um die Einstellungen zu finden, die eine Clientanwendung haben muss, um eine Verbindung mit Exchange herzustellen.
  
> [!NOTE]
> Für Clients, die auf Versionen von Exchange ab Exchange Server 2010 abzielen, wird empfohlen, den SOAP-AutoErmittlungsdienst anstelle des POX-AutoErmittlungsdiensts zu verwenden. Clients für Exchange 2007 müssen den POX-AutoErmittlungsdienst verwenden. Clients, die die .NET Framework verwenden, sollten die verwaltete EWS-API verwenden, da sie einen robusten und gut getesteten POX-AutoErmittlungsclient enthält. Weitere Informationen zur verwalteten EWS-API finden Sie unter [Erste Schritte mit EWS Managed API-Clientanwendungen.](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx) 
  
Dieser Abschnitt enthält Informationen zu den XML-Elementen, die während der PoX-AutoErmittlungsanforderungsumleitung zwischen Client und Server gesendet werden, und zu den Benutzereinstellungen, die in einer Antwort zurückgegeben werden. Der XML-Elementverweis enthält Zusammenfassungen der Elemente und eine Beschreibung der potenziellen Elementhierarchien, die das Element verwenden. In dieser Dokumentation werden die XML-Instanzen erläutert, die zwischen Client und Server gesendet werden. Der POX-AutoErmittlungsdienst verfügt nicht über ein explizites Schema.
  
Die Artikel in diesem Abschnitt enthalten Beispiele und Beschreibungen der Nachrichten, die zum Abrufen von AutoErmittlungs-Konfigurationsinformationen mithilfe des POX-AutoErmittlungsdiensts verwendet werden. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_InThisSection"> </a>

- [POX-Anforderung der AutoErmittlung für Exchange](pox-autodiscover-request-for-exchange.md)
    
- [POX-AutoErmittlungsantwort für Exchange](pox-autodiscover-response-for-exchange.md)
    
- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)   
- [Referenz zum SOAP-AutoErmittlungwebdienst für Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

