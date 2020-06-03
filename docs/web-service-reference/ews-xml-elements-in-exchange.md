---
title: EWS-XML-Elemente in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- Exchange
api_type:
- schema
ms.assetid: 4653466a-a596-456f-bbff-7da4ef1d18d3
description: Suchen nach Verweisinformationen für EWS-XML-Elemente in Exchange
localization_priority: Priority
ms.openlocfilehash: 29b90ad137141e30484ef804b6fcb6bb049ef3e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526116"
---
# <a name="ews-xml-elements-in-exchange"></a>EWS-XML-Elemente in Exchange

Suchen nach Verweisinformationen für EWS-XML-Elemente in Exchange
  
Exchange-Webdienste ist ein SOAP-basierter Webdienst, was bedeutet, dass die Anforderungs-und Antwortnachrichten, die zwischen dem Client und dem Server gesendet werden, aus XML-Elementen bestehen. Die Dokumentation in diesem Abschnitt basiert auf den XML-Instanzen, die zwischen dem Client und dem Server gesendet werden. Die XML-Instanzen werden in den WSDL-und Schemadateien definiert, die sich im virtuellen Verzeichnis befinden, in dem EWS gehostet wird. Wenn Sie ein authentifizierter Benutzer sind, können Sie zu den WSDL-und Schemadateien navigieren, indem Sie die folgenden URLs verwenden, wobei \<yourclientaccessserver\> der Name des Client Zugriffsservers lautet:
  
- http:// \<yourclientaccessserver\> . com/EWS/Services. WSDL – der Speicherort der WSDL-Datei.
    
- http:// \<yourclientaccessserver\> . com/EWS/Messages. xsd – der Speicherort des Nachrichtenschemas.
    
- http:// \<yourclientaccessserver\> . com/EWS/Types. xsd – der Speicherort des Typen Schemas.
    
Die Schemadateien, die die EWS-XML-Elemente beschreiben, stellen eine allgemeine Roadmap der XML-Struktur bereit, die für Anforderung-Antwort-Nachrichteninteraktionen möglich sind. Die tatsächliche XML-Struktur, die zwischen Client und Server gesendet wird, unterscheidet sich entsprechend des aufgerufenen Vorgangs, der angeforderten Informationen und der serverseitigen Einstellungen.
  
Die EWS-WSDL-Datei „services.wsdl" erfüllt nicht vollständig den WSDL-Standard, da sie keine WSDL-Dienstdefinition enthält. Das liegt daran, dass EWS nicht dafür ausgelegt ist, auf einem Computer gehostet zu werden, der über eine vordefinierte Adresse verfügt. Sie können den AutoErmittlung-Dienst verwenden, um die EWS-Endpunktadresse abzurufen. Einige clientseitige Objektmodellgeneratoren analysieren die WSDL-Datei und können einen Fehlerstatus ausgeben, da die WSDL-Datei keine WSDL-Dienstdefinition enthält. Wenn der Objektmodellgenerator einen Fehler ausgibt, können Sie eine Platzhalter-WSDL-Dienstdefinition einfügen.
  
> [!TIP]
> [!TIPP] Wenn Sie zum Entwickeln einer Anwendung .NET Framework einsetzen, empfehlen wir, die [verwaltete EWS-API](http://aka.ms/ews-managed-api-readme) zu verwenden, statt einen Objektmodellgenerator. Die verwaltete EWS-API stellt ein einfaches Objektmodell zum Verarbeiten der Serialisierung und Deserialisierung der EWS-XML. Weitere Informationen finden Sie unter [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
Die messages.xsd-Schemadatei enthält die Elementdefinitionen für Elemente auf oberster Ebene im SOAP-Text. Mit Ausnahme der Fehlerantwortcodes dienen die meisten Definitionen in der Datei „messages.xsd" für einen bestimmten Vorgang. Das types.xsd-Schema enthält die Definitionen für die SOAP-Header und alle häufig verwendeten Definitionen, die bei mehreren Vorgängen gleich sind.
  
## <a name="see-also"></a>Siehe auch

- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)
- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)
    

