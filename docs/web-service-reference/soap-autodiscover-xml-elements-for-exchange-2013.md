---
title: XML-Elemente der SOAP-AutoErmittlung für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: Finden Sie XML-Elementreferenz Informationen für den SOAP autodiscover-Webdienst in Exchange.
ms.openlocfilehash: 3b88429488dbecd4ed7c3adf56462f34fa0d4b17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465184"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a>XML-Elemente der SOAP-AutoErmittlung für Exchange 2013

Finden Sie XML-Elementreferenz Informationen für den SOAP autodiscover-Webdienst in Exchange.
  
Die Dokumentation in diesem Abschnitt basiert auf den SOAP-Auto Ermittlungs-XML-Elementinstanzen, die zwischen dem Client und dem Server gesendet werden. Diese XML-Instanzen Dokumentation basiert auf den WSDL-und Schemadateien, die sich im virtuellen Verzeichnis befinden, in dem der SOAP-AutoErmittlungsdienst gehostet wird. Authentifizierte Benutzer können die WSDL-und Schemadateien durchsuchen, indem Sie eine URL verwenden, die einer der folgenden ähnelt:
  
- Der Speicherort der WSDL-Datei: `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` oder`http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`
    
- Der Speicherort des Nachrichtenschemas: `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` oder`http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd` 
    
Der Speicherort der SOAP-Auto Ermittlungs-WSDL-und Schemadateien variiert je nach der Exchange-Installation.
  
Die Schemadatei Messages. xsd beschreibt die XML-Elemente, die in einem SOAP-Auto Ermittlungs Kopf und SOAP-Text gesendet werden können. Diese Datei bietet eine allgemeine Übersicht darüber, was die XML-Struktur für eine bestimmte Anforderungs-Antwort-Nachrichten Interaktion sein kann. Die tatsächliche XML-Struktur, die zwischen dem Client und dem Server gesendet wird, basiert auf den Optionen und dem Kontext, in dem Sie verwendet wird. In den Schemadateien wird definiert, welche XML-Daten möglich sind. Der tatsächliche Bereich von XML, der über den Draht gesendet wird, basiert auf dem aufgerufenen Vorgang, den angeforderten Informationen und den serverseitigen Einstellungen. 
  
## <a name="related-sections"></a>Verwandte Abschnitte

- [Referenz zum SOAP-AutoErmittlungwebdienst für Exchange](soap-autodiscover-web-service-reference-for-exchange.md)    
- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)    
- [Unified Messaging-Webdienst Referenz für Exchange](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

