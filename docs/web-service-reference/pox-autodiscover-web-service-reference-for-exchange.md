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
description: Hier finden Sie im Exchange Referenzinformationen für den AutoErmittlungsdienst POX.
ms.openlocfilehash: a8797fe714fd23049094c3ec2475b93fec4282c0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830867"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a>POX AutoErmittlung Webdienstverweis für Exchange

Hier finden Sie im Exchange Referenzinformationen für den AutoErmittlungsdienst POX.
  
Er bietet die Konfigurationsinformationen, die die Anwendung wird verwendet, um eine Verbindung mit einem Exchange-Server erstellen. Sie können die "einfache alte XML" (POX) AutoErmittlungsdienst zum Senden von Nachrichten, die nur aus XML-Nutzlast, ohne alle einschließenden SOAP Umschläge, um die Einstellungen zu suchen, die eine anderen Clientanwendung benötigen, um eine Verbindung zu Exchange bestehen.
  
> [!NOTE]
> Für Clients, die Versionen von Exchange, beginnend mit Exchange Server 2010, sollten Sie den SOAP-AutoErmittlungsdienst anstelle des AutoErmittlungsdiensts POX verwenden. Clients, die auf Exchange 2007 abzielen müssen den AutoErmittlungsdienst POX verwenden. Es wird empfohlen, dass Clients, die .NET Framework verwenden, da es sich um eine stabile und gründlich getestete POX AutoErmittlung-Client enthält die EWS Managed API verwenden. Weitere Informationen zu den EWS Managed API finden Sie unter [Erste Schritte mit EWS Managed API-Clientanwendungen](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
Dieser Abschnitt enthält Informationen über die XML-Elemente, die zwischen dem Client und Server gesendet werden, während der AutoErmittlung POX Anforderung Umleitung und benutzereinstellungen für, die in einer Antwort zurückgegeben werden. XML-Elementreferenz enthält Übersichten was die Elemente bedeuten und eine Beschreibung der potenziellen Element Hierarchien, die das Element verwenden. In dieser Dokumentation werden die XML-Instanzen erläutert, die zwischen Client und Server gesendet werden. Eine explizite Schema keinen POX AutoErmittlungsdienst.
  
Die Artikel in diesem Abschnitt enthalten Beispiele und eine Beschreibung der Nachrichten, die verwendet werden, für die AutoErmittlung Konfigurationsinformationen mithilfe des AutoErmittlungsdiensts POX abzurufen. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_InThisSection"> </a>

- [POX-Anforderung der AutoErmittlung für Exchange](pox-autodiscover-request-for-exchange.md)
    
- [POX Antwort der AutoErmittlung für Exchange](pox-autodiscover-response-for-exchange.md)
    
- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)   
- [SOAP-Webdienst-Verweis für die AutoErmittlung für Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

