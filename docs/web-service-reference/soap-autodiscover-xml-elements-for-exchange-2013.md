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
ms.openlocfilehash: 3b88429488dbecd4ed7c3adf56462f34fa0d4b17
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353392"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a>SOAP-Autodiscover XML-Elemente für Exchange 2013

Hier finden Sie im Exchange XML-Element Referenzinformationen für die AutoErmittlung SOAP-Webdienst.
  
In diesem Abschnitt die Dokumentation basiert auf die SOAP-AutoErmittlung-XML-Element-Instanzen, die zwischen dem Client und Server gesendet werden. Dieses XML-Instanz Dokumentation basiert auf die WSDL-Datei und Schema-Dateien, die sich in dem virtuellen Verzeichnis befinden, die den SOAP-AutoErmittlungsdienst gehostet wird. Authentifizierte Benutzer können Sie die WSDL-Datei und Schema-Dateien suchen, mithilfe einen URL, die einer der folgenden ähnelt:
  
- Den Speicherort der WSDL-Datei: `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` oder`http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`
    
- Der Speicherort des Schemas Nachrichten: `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` oder`http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd` 
    
Der Speicherort der Dateien SOAP-AutoErmittlung WSDL und Schema richtet sich nach der Installation von Exchange.
  
Die messages.xsd-Schemadatei beschreibt die XML-Elemente, die in einer AutoErmittlung SOAP-Header und SOAP-Body gesendet werden können. Diese Datei enthält eine allgemeine Übersicht über was die XML-Struktur für die Interaktion einer bestimmten Anforderung und Antwort-Nachricht werden kann. Die eigentliche XML-Struktur, die zwischen dem Client und Server gesendet wird basiert auf die Optionen und den Kontext, in dem sie verwendet wird. Die Schemadateien definieren, was XML möglich ist. Der Bereich der XML-Code, die über das Netzwerk gesendet wird basiert auf welche Operation aufgerufen wird, die angeforderten Informationen und die serverseitige-Einstellungen. 
  
## <a name="related-sections"></a>Verwandte Abschnitte

- [SOAP-Webdienst-Verweis für die AutoErmittlung für Exchange](soap-autodiscover-web-service-reference-for-exchange.md)    
- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)    
- [Unified Messaging-webdienstreferenz für Exchange](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

