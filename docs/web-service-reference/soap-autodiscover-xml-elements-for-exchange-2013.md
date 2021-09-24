---
title: SOAP AutoDiscover XML-Elemente für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: Suchen Sie nach XML-Elementreferenzinformationen für den SOAP-AutoErmittlungswebdienst in Exchange.
ms.openlocfilehash: 5dcf4d6cd7a2b0b2987e59530dfbaae7b9993242
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539094"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a>SOAP AutoDiscover XML-Elemente für Exchange 2013

Suchen Sie nach XML-Elementreferenzinformationen für den SOAP-AutoErmittlungswebdienst in Exchange.
  
Die Dokumentation in diesem Abschnitt basiert auf den XML-Elementinstanzen der SOAP-AutoErmittlung, die zwischen Client und Server gesendet werden. Diese XML-Instanzdokumentation basiert auf der WSDL und den Schemadateien, die sich im virtuellen Verzeichnis befinden, in dem der SOAP-AutoErmittlungsdienst gehostet wird. Authentifizierte Benutzer können mithilfe einer URL, die einer der folgenden ähnelt, zu WSDL- und Schemadateien navigieren:
  
- Der Speicherort der WSDL-Datei: `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` oder `http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`
    
- Der Speicherort des Nachrichtenschemas: `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` oder `http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd` 
    
Der Speicherort der WSDL- und Schemadateien der SOAP-AutoErmittlung variiert je nach Exchange Installation.
  
Die Schemadatei "messages.xsd" beschreibt die XML-Elemente, die in einem SOAP-Header und SOAP-Textkörper der AutoErmittlung gesendet werden können. Diese Datei enthält eine allgemeine Roadmap dazu, was die XML-Struktur für eine bestimmte Anforderung-Antwort-Nachrichteninteraktion sein kann. Die tatsächliche XML-Struktur, die zwischen dem Client und dem Server gesendet wird, basiert auf den Optionen und dem Kontext, in dem sie verwendet wird. Die Schemadateien definieren, welche XML-Daten möglich sind. Der tatsächliche XML-Bereich, der über das Kabel gesendet wird, basiert auf dem aufgerufenen Vorgang, den angeforderten Informationen und den serverseitigen Einstellungen. 
  
## <a name="related-sections"></a>Verwandte Abschnitte

- [Referenz zum SOAP-AutoErmittlungwebdienst für Exchange](soap-autodiscover-web-service-reference-for-exchange.md)    
- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)    
- [Unified Messaging-Webdienstreferenz für Exchange](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

