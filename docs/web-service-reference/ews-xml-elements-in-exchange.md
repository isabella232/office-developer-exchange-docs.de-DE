---
title: EWS-XML-Elemente in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exchange
api_type:
- schema
ms.assetid: 4653466a-a596-456f-bbff-7da4ef1d18d3
description: Suchen nach Verweisinformationen für EWS-XML-Elemente in Exchange
ms.openlocfilehash: 046a985ae4696616d28a0891ffe0aa8cc0552307
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758296"
---
# <a name="ews-xml-elements-in-exchange"></a>EWS-XML-Elemente in Exchange

Suchen nach Verweisinformationen für EWS-XML-Elemente in Exchange
  
Die Exchange-Webdienste sind ein SOAP-basierter Webdienst, d. h. die zwischen Client und Server gesendeten Anforderungs- und Antwortnachrichten bestehen aus XML-Elementen. Die Dokumentation in diesem Abschnitt basiert auf den XML-Instanzen, die zwischen Client und Server gesendet werden. Die XML-Instanzen sind in den WSDL- und Schemadateien definiert, die sich im virtuellen Verzeichnis des Servers befinden, der EWS hostet. Wenn Sie ein authentifizierter Benutzer sind, können Sie zu den WSDL- und Schemadateien navigieren, indem Sie folgende URLs verwenden, dabei ist \<yourclientaccessserver\> der Name Ihres Clientzugriffsservers:
  
- http://\<yourclientaccessserver\>.com/ews/services.wsdl - Der Speicherort der WSDL-Datei.
    
- http://\<yourclientaccessserver\>.com/ews/messages.xsd - Der Speicherort des Nachrichtenschemas.
    
- http://\<yourclientaccessserver\>.com/ews/types.xsd - Der Speicherort des Typenschemas.
    
Die Schemadateien, die die EWS-XML-Elemente beschreiben, stellen eine allgemeine Roadmap der XML-Struktur bereit, die für Anforderung-Antwort-Nachrichteninteraktionen möglich sind. Die tatsächliche XML-Struktur, die zwischen Client und Server gesendet wird, unterscheidet sich entsprechend des aufgerufenen Vorgangs, der angeforderten Informationen und der serverseitigen Einstellungen.
  
Die EWS-WSDL-Datei „services.wsdl" erfüllt nicht vollständig den WSDL-Standard, da sie keine WSDL-Dienstdefinition enthält. Das liegt daran, dass EWS nicht dafür ausgelegt ist, auf einem Computer gehostet zu werden, der über eine vordefinierte Adresse verfügt. Sie können den AutoErmittlung-Dienst verwenden, um die EWS-Endpunktadresse abzurufen. Einige clientseitige Objektmodellgeneratoren analysieren die WSDL-Datei und können einen Fehlerstatus ausgeben, da die WSDL-Datei keine WSDL-Dienstdefinition enthält. Wenn der Objektmodellgenerator einen Fehler ausgibt, können Sie eine Platzhalter-WSDL-Dienstdefinition einfügen.
  
> [!TIP]
> [!TIPP] Wenn Sie zum Entwickeln einer Anwendung .NET Framework einsetzen, empfehlen wir, die [verwaltete EWS-API](http://aka.ms/ews-managed-api-readme) zu verwenden, statt einen Objektmodellgenerator. Die verwaltete EWS-API stellt ein einfaches Objektmodell zum Verarbeiten der Serialisierung und Deserialisierung der EWS-XML. Weitere Informationen finden Sie unter [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
Die messages.xsd-Schemadatei enthält die Elementdefinitionen für Elemente auf oberster Ebene im SOAP-Text. Mit Ausnahme der Fehlerantwortcodes dienen die meisten Definitionen in der Datei „messages.xsd" für einen bestimmten Vorgang. Das types.xsd-Schema enthält die Definitionen für die SOAP-Header und alle häufig verwendeten Definitionen, die bei mehreren Vorgängen gleich sind.
  
## <a name="see-also"></a>Siehe auch

- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)
- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
- [Erkunden von EWS Managed API, EWS und Webdiensten in Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)
    

