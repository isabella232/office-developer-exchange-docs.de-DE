---
title: SOAP-Webdienst-Verweis für die AutoErmittlung für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: Hier finden Sie im Exchange Referenzinformationen für die SOAP-AutoErmittlungsdienst.
ms.openlocfilehash: 1cb24a8667c71028f3dead78d9fa533dc9547a64
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831514"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a>SOAP-Webdienst-Verweis für die AutoErmittlung für Exchange

Hier finden Sie im Exchange Referenzinformationen für die SOAP-AutoErmittlungsdienst.
  
Er bietet die Konfigurationsinformationen, die die Anwendung wird verwendet, um eine Verbindung mit einem Exchange-Server erstellen. Den SOAP-AutoErmittlungsdienst können zum Senden von Nachrichten zwischen der Clientanwendung und dem Exchange-Server, um die Einstellungen zu suchen, dass die Anwendung zum Verbinden mit Exchange verwendet wird. Im Gegensatz zu den POX AutoErmittlungsdienst ermöglicht der SOAP-AutoErmittlungsdienst Batchanforderungen der AutoErmittlung für viele Benutzer Einstellungen und eine genauere Kontrolle über die Einstellungen in der Antwort zurückgegeben werden. 
  
> [!NOTE]
> Clients, die Versionen von Exchange, beginnend mit Exchange Server 2010, wird empfohlen, dass Sie den SOAP-AutoErmittlungsdienst (anstelle des AutoErmittlungsdiensts POX) verwenden. Clients, die auf Exchange 2007 abzielen müssen den AutoErmittlungsdienst POX verwenden. Es wird empfohlen, dass Clients, die .NET Framework verwenden, da es sich um eine stabile und gründlich getestete SOAP-AutoErmittlung-Client enthält die EWS Managed API verwenden. Weitere Informationen zu den EWS Managed API finden Sie unter [Erste Schritte mit EWS Managed API-Clientanwendungen](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
Dieser Abschnitt enthält Informationen über die XML-Elemente, die zwischen dem Client und Server gesendet werden, während der AutoErmittlung für SOAP-Anforderung Umleitung und benutzereinstellungen für, die in einer Antwort zurückgegeben werden. XML-Elementreferenz enthält Übersichten was die Elemente bedeuten und eine Beschreibung der potenziellen Element Hierarchien, die das Element enthalten. 
  
Die Artikel in diesem Abschnitt beschreiben die XML-Instanzen, die zwischen dem Client und Server gesendet werden. Im virtuellen Verzeichnis des Servers, der den SOAP-AutoErmittlungsdienst hostet, kann das Schema, das diese Elemente beschreibt, gefunden werden.
  
Der WSDL-Vorgang, in den Themen in diesem Abschnitt bieten eine Übersicht über die auszuführende Operation wird und die Operation-Anfrage und-Antwort Beispiele. Sie können die Informationen zur Version bereitgestellt, um zu bestimmen, ob die Features, die Sie verwenden möchten in der Version des Produkts verfügbar sind, auf dem Sie ausgeführt werden. Die Beispiele in den Themen Vorgang können Sie die XML-Struktur zu verstehen, die in die SOAP-Nachrichten enthalten ist, die zum und vom Server gesendet werden.
  
Dieser Abschnitt enthält auch Beispiele und eine Beschreibung der Nachrichten, die zum Abrufen von AutoErmittlung Konfigurationsinformationen mithilfe von SOAP-AutoErmittlungsdienst verwendet werden. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_InThisSection"> </a>

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)
    
- [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)
    
- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
    
- [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)
    
- [SOAP-Autodiscover XML-Elemente für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch


- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Mithilfe von AutoErmittlung Verbindungspunkte suchen](http://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung](http://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [Abrufen von domäneneinstellungen aus einem Exchange-server](http://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

