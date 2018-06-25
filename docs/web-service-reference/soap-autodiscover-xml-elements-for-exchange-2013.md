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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831517"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a>SOAP-Autodiscover XML-Elemente für Exchange 2013

Hier finden Sie im Exchange XML-Element Referenzinformationen für die AutoErmittlung SOAP-Webdienst.
  
In diesem Abschnitt die Dokumentation basiert auf die SOAP-AutoErmittlung-XML-Element-Instanzen, die zwischen dem Client und Server gesendet werden. Dieses XML-Instanz Dokumentation basiert auf die WSDL-Datei und Schema-Dateien, die sich in dem virtuellen Verzeichnis befinden, die den SOAP-AutoErmittlungsdienst gehostet wird. Authentifizierte Benutzer können Sie die WSDL-Datei und Schema-Dateien suchen, mithilfe einen URL, die einer der folgenden ähnelt:
  
- http://\<Yourclientaccessserver\>.com/autodiscover/services.wsdl oder http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/services.wsdl – den Speicherort der WSDL-Datei.
    
- http://\<Yourclientaccessserver\>.com/autodiscover/messages.xsd oder http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/messages.xsd – die Position des Schemas Nachrichten.
    
Der Speicherort der Dateien SOAP-AutoErmittlung WSDL und Schema richtet sich nach der Installation von Exchange.
  
Die messages.xsd-Schemadatei beschreibt die XML-Elemente, die in einer AutoErmittlung SOAP-Header und SOAP-Body gesendet werden können. Diese Datei enthält eine allgemeine Übersicht über was die XML-Struktur für die Interaktion einer bestimmten Anforderung und Antwort-Nachricht werden kann. Die eigentliche XML-Struktur, die zwischen dem Client und Server gesendet wird basiert auf die Optionen und den Kontext, in dem sie verwendet wird. Die Schemadateien definieren, was XML möglich ist. Der Bereich der XML-Code, die über das Netzwerk gesendet wird basiert auf welche Operation aufgerufen wird, die angeforderten Informationen und die serverseitige-Einstellungen. 
  
## <a name="related-sections"></a>Verwandte Abschnitte
<a name="bk_RelatedSections"> </a>

- [SOAP-Webdienst-Verweis für die AutoErmittlung für Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)
    
- [Unified Messaging-webdienstreferenz für Exchange](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

