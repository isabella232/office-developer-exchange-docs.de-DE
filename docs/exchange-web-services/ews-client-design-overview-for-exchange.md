---
title: Übersicht über den EWS-Cliententwurf für Exchange
manager: sethgros
ms.date: 3/11/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: b26f67aa-7c66-4d7d-98b3-746f26ab37f4
description: Lernen Sie die Entwurfsaspekte für die Entwicklung mit EWS für Exchange kennen.
ms.openlocfilehash: ea0e1ad3f8402d19a6163f3320a2a17f08f3ea2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756837"
---
# <a name="ews-client-design-overview-for-exchange"></a>Übersicht über den EWS-Cliententwurf für Exchange

Lernen Sie die Entwurfsaspekte für die Entwicklung mit EWS für Exchange kennen. 
  
Dieser Artikel enthält eine Übersicht über das Entwerfen einer Exchange-Webdienste (EWS)-Anwendung. Mithilfe dieser Informationen können Sie bestimmen, ob EWS die richtigen API für Ihre Anwendung ist und (wenn dies der Fall ist) welche Art von Clientimplementierung verwendet werden sollte. Dieser Artikel enthält außerdem Informationen zu bewährten Methoden für das Entwerfen von Anwendungen mit Office 365, Exchange Online und Exchange-Versionen ab Exchange 2007 als Ziel in einer Codebasis sowie wichtige Entscheidungskriterien bei der Wahl von lokalen Exchange-Servern oder Exchange Online als Ziel.
  
## <a name="is-ews-the-right-api-for-your-application"></a>Ist EWS die richtige API für Ihre Anwendung?
<a name="IsEWSRight"> </a>

Bevor Sie mit der Entwicklung Ihrer Anwendung beginnen, müssen Sie überlegen, ob EWS die richtige API für Sie ist. Wenn Sie für Exchange Server oder Exchange Online entwickeln, ist EWS die bevorzugte Clientzugriffstechnologie. Die Entwicklung des Clientzugriffs für Exchange-Versionen ab Exchange 2007 konzentrierte sich primär auf EWS. Neue in Outlook implementierte Clientzugriffsfunktionen verwenden EWS, darunter auch die in Exchange 2007 eingeführten Features „Abwesend" und „Verfügbarkeit" sowie die Features „E-Mail-Info" und „GetRooms" aus Exchange 2010. Dies stellt eine konsequente Investition in EWS für interne und externe Partner dar, die Exchange-Clientanwendungen entwickeln.
  
EWS ist die primäre Clientzugriffs-API für Ihre Exchange-Clientanwendungen. In einigen Fällen empfiehlt sich jedoch eventuell der Einsatz anderer Exchange-APIs für die Entwicklung von Clientanwendungen. So bietet z. B. Exchange ActiveSync die folgenden Vorteile gegenüber EWS:
  
- Die XML-Struktur wurde mit Tokens versehen, um Exchange ActiveSync zu einem kompakteren Protokoll zu machen.  
- Exchange ActiveSync enthält einen Richtlinienmechanismus zum Steuern des Clientzugriffs und zum Bereitstellen anderer robuster Unternehmenslösungen für mobile Nachrichten.
    
> [!NOTE]
> [!HINWEIS] Zum Entwickeln von Exchange ActiveSync-Clients benötigen Sie eine Lizenz. Informationen zu den Unterschieden zwischen Exchange ActiveSync und EWS finden Sie unter [Wählen zwischen Exchange ActiveSync und Exchange-Webdienste (EWS)](http://msdn.microsoft.com/en-us/library/dn144954%28v=exchg.140%29.aspx). 
  
MAPI-RPC über HTTP ist eine weitere Programmieroption für Exchange-Clientanwendungen. MAPI-RPC über HTTP bietet jedoch keine intuitive Schnittstelle für die Kommunikation zwischen Clients und dem Server.
  
Weitere Informationen zu Exchange-Entwicklungstechnologien finden Sie unter [Durchsuchen die EWS Managed API, EWS, und Web services im Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).
  
## <a name="options-for-ews-client-development"></a>Optionen für die Entwicklung von EWS-Clients
<a name="EWSClientOptions"> </a>

Für die Entwicklung für Exchange mithilfe von EWS stehen mehrere Optionen zur Verfügung. Welche Option für Sie am besten geeignet ist, hängt von der Entwicklungsplattform, Tools, verfügbaren Implementierungen und Anwendungsanforderungen für Ihre Organisation ab. Im Folgenden finden Sie die vier primären Optionen, die zum Erstellen von EWS-Clientanwendungen zur Verfügung stehen:
  
- Verwaltete EWS-API
- Java-API der EWS
- Automatisch generierte EWS-Proxys
- Benutzerdefinierte EWS-Client-API
    
### <a name="ews-managed-api"></a>Verwaltete EWS-API

Die [verwaltete EWS-API](http://aka.ms/ews-managed-api-readme) ist ein benutzerdefinierter Webdienstclient und die standardmäßige Clientzugriffs-API für .NET Framework-Anwendungen. 
  
Im Folgenden werden einige Vorteile der Verwendung der verwalteten EWS-API aufgeführt:
  
- Sie bietet ein intuitives Objektmodell.   
- Sie abstrahiert die Komplexität der Dienstbeschreibung in den WSDL- und Schemadateien.   
- Sie enthält clientseitige Geschäftslogik.   
- Sie verarbeitet die Webanforderungen und -antworten sowie die Objektserialisierung und -deserialisierung.   
- Sie wird von Microsoft unterstützt.
    
Beachten Sie jedoch, dass die verwaltete EWS-API keine vollständige Lösung ist. Einige Funktionen sind nicht in die verwaltete EWS-API implementiert. Obwohl die verwaltete EWS-API nicht alle EWS-Funktionen enthält, kann sie aus den folgenden Gründen trotzdem die beste Wahl für die Entwicklung von Clientanwendungen sein:
  
- Sie können das .NET Framework für die Entwicklung verwenden.
- Sie implementiert die AutoErmittlung sowie die meisten Teile des EWS-Objektmodells.
- Sie implementiert clientseitige Geschäftslogik für die Zusammenarbeit mit EWS in der [ExchangeService](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Klasse. 
    
Sie können die EWS-Webdienst-API aus folgenden Gründen anstelle der verwalteten EWS-API verwenden:
  
- .NET Framework wird von Ihrer Anwendung nicht verwendet. 
- Sie möchten die verwaltete EWS-API-Assembly nicht verteilen. 
- Ihre Anwendung verwendet Features, die nicht in der verwalteten EWS-API implementiert sind.
    
Weitere Informationen finden Sie unter [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](get-started-with-ews-managed-api-client-applications.md).
  
> [!NOTE]
> Die EWS Managed API ist jetzt als open-Source-Projekt auf [GitHub](http://aka.ms/ews-managed-api-github)verfügbar. Sie können die open-Source-Bibliothek zu verwenden: 
> - Implementieren von Programmfehlerbehebungen und Verbesserungen in die API 
> - Abrufen von Fehlerbehebungen und Verbesserungen, bevor diese in einer offiziellen Version verfügbar sind
> - Zugreifen auf die umfassendste und aktuellste Implementierung der API, um sie als Referenz zu verwenden oder neue Bibliotheken auf neuen Plattformen zu erstellen
> 
> Wir freuen uns auf Ihre [Beiträge](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) über GitHub. 
  
### <a name="ews-java-api"></a>Java-API der EWS

Die Java-API der EWS ist ein Open Source-Projekt auf [GitHub](https://github.com/OfficeDev/ews-java-api), das von der Community aktualisiert und erweitert werden kann. Sie ähnelt stilistisch der [verwalteten EWS-API](http://msdn.microsoft.com/en-us/library/office/jj220535%28v=exchg.80%29.aspx) und verwendet EWS-SOAP-Anforderungen und - Antworten über das Netzwerk. Obwohl Sie mit der Java-API der EWS nicht auf alle [EWS-SOAP-Vorgänge](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) zugreifen können, setzen wir mit der [aktuellen Erstellung](http://blogs.office.com/2014/08/28/open-sourcing-exchange-web-services-ews-java-api/) des Open Source-Projekts auf die Community, um diese Lücke zu schließen. Beachten Sie, dass der Microsoft-Support mit einem entsprechenden Supportvertrag alle Fragen im Zusammenhang mit dem EWS-SOAP-Protokoll, nicht jedoch mit der Java-API für EWS beantwortet. Die Java-API für EWS steht zum Download und für Communitybeiträge auf [GitHub](https://github.com/OfficeDev/ews-java-api) zur Verfügung.
  
### <a name="ews-autogenerated-proxies"></a>Automatisch generierte EWS-Proxys

Automatisch generierte Client-APIs werden von den WSDL- und XML-Schemadefinitionen von EWS generiert. Client-Objektmodellgeneratoren sind für viele Sprachen verfügbar. Im Allgemeinen verwalten die automatisch generierten Objektmodelle die Objektserialisierung und -deserialisierung. Sie enthalten keine Geschäftslogik. Bei der automatischen Generierung werden häufig Artefakte erstellt, die die intuitive Nutzung des Objektmodells beeinträchtigen. Die Unterstützung für Exchange deckt den vom Client gesendeten und empfangenen XML-Code ab, nicht jedoch den des Objektmodells.
  
### <a name="custom-ews-client-api"></a>Benutzerdefinierte EWS-Client-API

Für einige Anwendungen, die nur einen kleinen Satz EWS-Funktionen verwenden, können Sie eine benutzerdefinierte Client-API für die Kommunikation mit Exchange erstellen. Dies ermöglicht es Ihnen, weniger Systemressourcen zu verbrauchen. Dies ist nützlich für Clients, die auf Geräten mit beschränktem Speicher ausgeführt werden, beispielsweise Clients mit .NET Micro Framework.
  
## <a name="ews-client-features"></a>EWS-Clientfeatures
<a name="EWSFeatures"> </a>

Unabhängig von der gewählten Entwicklungsoption sollten Sie überlegen, wie EWS-Features im Client implementiert werden. Die Verfügbarkeit von Features basiert auf der EWS-Schemaversion, für die die Anwendung entwickelt wird. Da EWS-Schemas abwärts- und aufwärtskompatibel sind, können Anwendungen, die für eine frühere Schemaversion wie z. B. Exchange Server 2007 SP1 erstellt wurden, auch für höhere Schemaversionen verwendet werden, wie z. B. den Exchange Server 2013 SP1-Dienst sowie Exchange Online. 
  
Da Features und Featureupdates vom Schema gesteuert werden, empfehlen wir die Verwendung der frühesten gemeinsamen Codebasis für die EWS-Features, die Sie in der Clientanwendung implementieren möchten. Viele Anwendungen können die Version Exchange2007_SP1 als Ziel verwenden, da das Schema von Exchange 2007 SP1 fast alle Exchange-Kernfunktionen für die Arbeit mit Elementen und Ordnern im Exchange-Informationsspeicher enthält. Es wird empfohlen, Codeverzweigungen für jede EWS-Schemaversion zu verwalten. Im Folgenden werden die derzeit verfügbaren Schemaversionen aufgeführt. 
  
```XML
  <xs:simpleType name="ExchangeVersionType">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Exchange2007" />
      <xs:enumeration value="Exchange2007_SP1" />
      <xs:enumeration value="Exchange2010" />
      <xs:enumeration value="Exchange2010_SP1" />
      <xs:enumeration value="Exchange2010_SP2" />
      <xs:enumeration value="Exchange2013" />
      <xs:enumeration value="Exchange2013_SP1" />
    </xs:restriction>
  </xs:simpleType>
```

Die Schemaversionen werden im einfachen **ExchangeVersionType** -Typ verwaltet. 
  
Informationen zu den in den einzelnen EWS-Schemaversionen verfügbaren Features finden Sie unter [EWS-Schemaversionen in Exchange](ews-schema-versions-in-exchange.md).
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Verfügbarkeit von Web Service-API in Exchange und die EWS Managed API](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
    
- [EWS-Schemaversionen in Exchange](ews-schema-versions-in-exchange.md)
    
- [Konfigurationsoptionen für EWS in Exchange](configuration-options-for-ews-in-exchange.md)
    
- [Vergleich der Exchange Online und Exchange lokalen Clientprogrammierung](comparing-exchange-online-and-exchange-on-premises-client-programming.md)
    
- [EWS-Einschränkung in Exchange](ews-throttling-in-exchange.md)
    
- [Redistribution Anforderungen für die EWS Managed API](redistribution-requirements-for-the-ews-managed-api.md)
    
- [Instrumentieren Client-Anfragen für EWS und REST in Exchange](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch
 
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md) 
- [EWS-Anwendungstypen](ews-application-types.md)
    

