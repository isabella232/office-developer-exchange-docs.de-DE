---
title: EWS-Anwendungen und die Exchange-Architektur
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c10f308a-65bb-4a0b-8fdd-b4a61503f0fd
description: Erfahren Sie mehr über die Funktionsweise von EWS innerhalb der Exchange-Architektur und finden Sie heraus, welche Protokolle EWS verwendet.
ms.openlocfilehash: 1fbc1e68edbca829555fbbf1b9f0bc4723da9524
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756843"
---
# <a name="ews-applications-and-the-exchange-architecture"></a>EWS-Anwendungen und die Exchange-Architektur

Erfahren Sie mehr über die Funktionsweise von EWS innerhalb der Exchange-Architektur und finden Sie heraus, welche Protokolle EWS verwendet.
  
Exchange-Webdienste (EWS) ist eine plattformübergreifende-API, die ermöglicht, dass Postfachelemente wie e-Mail-Nachrichten, Besprechungen und Kontakten aus Exchange Online, Exchange Online als Teil von Office 365, Zugriff auf Anwendungen oder lokale Versionen von Exchange beginnend mit Exchange Server 2007. [EWS-Applikationen](ews-application-types.md) möglich Postfachelemente lokal oder Remote durch Senden einer Anforderung in einer XML-basierte SOAP-Nachricht. Die SOAP-Nachricht ist in einer HTTP-Nachricht, wenn zwischen der Anwendung und dem Server, d. h., solange Ihre Anwendung XML über HTTP vornehmen kann, können sie EWS verwenden, Zugriff auf Exchange gesendet eingebettet. 
  
## <a name="exchange-architecture-overview"></a>Übersicht über die Exchange-Architektur
<a name="bk_techarch"> </a>

Das folgende Diagramm zeigt die Authentifizierungsmethoden und Kommunikationspfade von EWS-Anwendungen bei der Kommunikation mit Exchange 2013 und Exchange Online. Aus Sicht der EWS-Anwendung sind die Kommunikationspfade identisch, und die Authentifizierungsmethoden variieren nur geringfügig. Der Hauptunterschied besteht aus der Transparenz in das Exchange-Back-End.
  
**Abbildung 1. EWS-Anwendung und der lokalen Exchange-Architektur**

![Abbildung einer EWS-Anwendung im Kontext der lokalen Exchange-Architektur. Eine Beschreibung der Komponenten dieses Diagramms finden Sie bei den Elementen 1-8 im Text, der auf diese Abbildung und die folgende Abbildung folgt.](media/Ex2013_ArchitecturesOverview.png)
  
Abbildung 2 zeigt die gleichen Kommunikationspfade wie in Abbildung 1, die von EWS-Anwendungen bei der Kommunikation mit Exchange Online verwendet werden.
  
**Abbildung 2. EWS-Anwendung und der Exchange Online-Architektur**

![Abbildung einer EWS-Anwendung im Kontext der Exchange Online-Architektur für eine EWS-Anwendung. Eine Beschreibung der Komponenten dieses Diagramms finden Sie bei den Elementen 1, 2, 3, 6 und 9 im Text, der auf diese Abbildung folgt.](media/Ex2013_Architectures_Online.png)
  
Folgende Komponenten werden in den Diagrammen gezeigt:
  
1. EWS-Anwendung – dies kann ein [Client, -Portal oder Service-Anwendung](ews-application-types.md) sein und auf einem Client oder auf einem Exchange lokalen Client Access Server installiert werden kann. Wenn Sie die EWS Managed API verwenden, die EWS-Anwendung zu entwickeln, müssen die EWS Managed API-Assemblys auf dem Client und [verteilt Sie von der Anwendung](redistribution-requirements-for-the-ews-managed-api.md)installiert werden.
    
2. Die SOAP-XML-Nachricht – eine XML-Nachricht in einem SOAP-Umschlag, eingebettet in einer HTTP/S-Nachricht, die der „Datei Services.wsdl“ auf dem Clientzugriffsserver entspricht. HTTPS empfiehlt sich für Exchange lokal und ist für Exchange Online erforderlich.  
    
3. Authentifizierungsmethoden – EWS-Nachrichten umfassen grundlegende, NTLM- (integrierte Windows-Authentifizierung) oder OAuth-Authentifizierungsinformationen als Teil des HTTP-Datenverkehrs.  
    
4. Lastenausgleich – Lastenausgleich verteilt die Nachricht an einen Clientzugriffsserver im Clientzugriffsserver-Array. Diese Komponente wird nur in der lokalen Exchange-Architektur angezeigt.
    
5. Clientzugriffsserver-Arrays –-Clientzugriffsservern in einen Lastenausgleich Gruppe mit der Bezeichnung ein Clientzugriffsserver-Arrays organisiert sind. Einzelne Clientzugriffs-Servern finden Sie Authentifizierung, beschränkt Umleitung und Proxy-Dienste. Die Clientzugriffsserver selbst keine Rendern von Daten und keine Daten in der Warteschlange oder auf einem Clientzugriffsserver gespeichert ist - ist es dünne und statusfreie. es einfach authentifiziert die Anforderung, führt eine AutoErmittlung-Suche und leitet die Anforderung an den Postfachserver. Der Clientzugriffsserver behält eine 1:1-Beziehung mit dem Postfachserver, der die Daten des Benutzers hostet. Das HTTP-Protokoll (über ein selbstsigniertes Zertifikat mit SSL gesichert) wird zwischen dem Clientzugriffsserver und Postfachserver. Diese Komponente wird nur angezeigt, in der lokalen Exchange-Architektur.
    
6. AutoErmittlungsdienst – der AutoErmittlungsdienst führt eine Suche durch den Zugriff auf Active Directory-Domänendienste (AD DS) zum Abrufen der Postfachversion und den Speicherort des Postfachservers an, die die aktive Kopie der Daten des Benutzers hostet.
    
7. EWS-Dienst – der EWS-Dienst wird von drei Dateien beschrieben: „Services.WSDL“, „Messages.xsd“, „Types.xsd“ sowie die verwalteten EWS-API-Assemblys. „Services.WSDL“ beschreibt den Vertrag zwischen Client und Server, „Messages.xsd“ definiert die Anforderungs- und Antwort-SOAP-Nachrichten, und „Types.xsd“ definiert die Elemente, die in den SOAP-Nachrichten verwendet werden. „Messages.xsd“ und „Types.xsd“ enthalten immer die neuesten Versionen des Schemas, obwohl frühere Versionen des Schemas vorhanden sind. Beachten Sie, dass „Services.wsdl“, „Messages.xsd“ und „Types.xsd“ auf dem Clientzugriffsserver zur Verfügung gestellt werden, aber eigentlich nicht für die Schemavalidierung verwendet werden – sie werden nur zu Informationszwecken bereitgestellt. Die verwalteten EWS-API-Assemblys werden für serverseitige EWS-Clientanwendungen bereitgestellt und werden auf allen Exchange Server-Rollen bereitgestellt, nicht nur auf den Clientzugriffsservern. Diese Komponente wird nur in der lokalen Exchange-Architektur angezeigt.
    
    Verfügbarkeit von Features basiert auf der EWS-Schema-Version, die Ihre Anwendung abzielt. Da EWS-Schemas und Forward-abwärtskompatible, sind, wenn Sie eine Anwendung erstellen, die eine frühere Schemaversion, wie Exchange 2007 SP1 abzielt Ihrer Anwendung funktioniert auch für eine höhere Schemaversion, wie der Exchange 2010 SP2-Dienst als auch Exchange Online. Da Features und Featureupdates vom Schema gesteuert werden, empfehlen wir die Verwendung der frühesten gemeinsamen Codebasis für die EWS-Features, die Sie in der Clientanwendung implementieren möchten. Viele Anwendungen können die Version Exchange2007_SP1 als Ziel verwenden, da das Schema von Exchange 2007 SP1 fast alle Exchange-Kernfunktionen für die Arbeit mit Elementen und Ordnern im Exchange-Informationsspeicher enthält. Weitere Informationen finden Sie unter [EWS-Client-Features](ews-client-design-overview-for-exchange.md#EWSFeatures).
    
8. Database Availability Group (DAG) – Postfachserver sind in einer hochgradig verfügbaren DAG organisiert, die in einem oder mehrerem Rechenzentren bereitgestellt werden können. Der Postfachserver enthält die Postfachdatenbank und verarbeitet alle Vorgänge für die aktiven Postfächer auf diesem Server. Alle Komponenten, die Daten verarbeiten, rendern und speichern, befinden sich auf dem Postfachserver. Clients stellen keine direkte Verbindung mit dem Postfachserver her. Alle Verbindungen werden vom Clientzugriffsserver verarbeitet. Diese Komponente wird nur in der lokalen Exchange-Architektur angezeigt.
    
9. Exchange Online und Exchange Online als Teil von Office 365 – die gehostete messaging-Lösung, die Exchange-Features als Cloud-basierten Dienst bietet.
    
Wenn eine EWS-Anwendung Informationen aus dem Exchange-Speicher anfordert, wird eine XML-Anforderungsnachricht erstellt, die dem SOAP-Standard entspricht, und an den Exchange-Server gesendet. Wenn der Exchange-Server die Anforderung empfängt, überprüft er die Anmeldeinformationen, die vom Client bereitgestellt werden, und analysiert automatisch die XML-Daten für die angeforderten Daten. Der Server erstellt dann eine SOAP-Antwort, die XML-Daten enthält, die die angeforderten starken Objekttypen und deren Eigenschaften darstellt. Die XML-Daten werden in einer HTTP-Antwort zurück an die Anwendung gesendet. Die Anwendung deserialisiert dann die XML-Elemente und verwendet die Daten, um die starken Objekttypen neu zu erstellen.
  
## <a name="protocols-and-standards-that-ews-applications-must-support"></a>Protokolle und Standards, die EWS-Anwendungen unterstützen müssen
<a name="bk_standards"> </a>

Für die Kommunikation mit einem Exchange-Server müssen EWS-Anwendungen die folgenden Protokolle und Standards unterstützen.
  
**In Tabelle 1. Protokolle**

|**Protocol**|**Wie sie verwendet wird**|
|:-----|:-----|
|HTTP/S  <br/> |Ermöglicht EWS-Anwendungen den Zugriff auf Exchange-Datenbankdaten über das Netzwerk, unabhängig davon, ob sich der Client im Internet oder Intranet befindet.  <br/> |
|SOAP 1.0  <br/> |Bildet einen Umschlag um die Messaging-Nutzdaten. EWS implementiert das SOAP-Protokoll mit verschiedenen Teilen des SOAP-Umschlags, um andere Funktionen zu aktivieren. Der SOAP-Header wird für den Identitätswechsel und zum Bereitstellen von Versionsverwaltungsdaten verwendet. Der SOAP-Text enthält Informationen zum auszuführenden Vorgang und zu den Daten, die an den Vorgang gesendet werden. SOAP basiert auf WSDL, um die aufzurufenden Vorgänge zu beschreiben.  <br/> |
|WSDL 1.0  <br/> |Beschreibt die Bindungen, die Vorgänge und die Eigenschaften, die verwendet werden, um EWS-Vorgänge in der Datei „Services.wsdl“ aufzurufen. Diese Datei bildet zusammen mit den referenzierten Schemadateien den Vertrag zwischen einer EWS-Anwendung und dem Exchange-Server und wird häufig zusammen mit anbieterspezifischen Tools verwendet, um plattformspezifische Anwendungen zu erstellen. Die WSDL-Datei befindet sich im virtuellen EWS-Verzeichnis, das sich im Stammverzeichnis der Website befindet.  <br/> |
|Transport Layer Security (TLS)/SSL  <br/> |Stellt sichere Webkommunikation im Internet oder Intranet bereit. TLS ermöglicht Anwendungen das Authentifizieren von Servern oder (optional) Servern das Authentifizieren von EWS-Anwendungen. Es stellt ferner durch Verschlüsseln der Kommunikation einen Sicherheitskanal bereit. TLS ist die aktuelle Version des SSL-Protokolls (Secure Sockets Layer).  <br/> |
|XML/XSD  <br/> |Stellt ein universelles Nachrichtenformat für den Austausch von Informationen zwischen dem Exchange-Server und dem Client bereit. XML stellt komplexe Exchange-Datenbankdaten für Clientanwendungen in einer definierten Struktur bereit. Der Vorteil von XML besteht darin, dass es den Austausch von Daten auch dann ermöglicht, wenn eine EWS-Anwendung und ein Server keine gemeinsame Plattform nutzen.  <br/> |
   
Darüber hinaus müssen EWS-Anwendungen folgende Authentifizierungsstandards unterstützen:
  
- Standardauthentifizierung über SSL für Anwendungen, die Exchange Online oder lokales Exchange nutzen.
    
- NTLM-Authentifizierung über SSL für Anwendungen, die lokales Exchange unterstützen.
    
- OAuth 2.0-Tokenauthentifizierung, vertrauenswürdigen Partner Applications und Interoperabilität mit Lync Server 2013 und SharePoint Server 2013.
    
## <a name="see-also"></a>Siehe auch


- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [EWS-Anwendungstypen](ews-application-types.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    

