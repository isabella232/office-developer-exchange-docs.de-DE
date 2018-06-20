---
title: Vergleich der Exchange Online und Exchange lokalen Clientprogrammierung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3c2eabe4-52bc-461e-a6dd-f65f22f16e50
description: Lernen Sie die Entwurfsaspekte für die Erstellung einer EWS Managed API oder EWS-Clientanwendung, die mit Exchange Online und Exchange lokal funktioniert.
ms.openlocfilehash: 87c6ee476e06b50c339901bf61020b0fc98f8486
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756847"
---
# <a name="comparing-exchange-online-and-exchange-on-premises-client-programming"></a>Vergleich der Exchange Online und Exchange lokalen Clientprogrammierung

Lernen Sie die Entwurfsaspekte für die Erstellung einer EWS Managed API oder EWS-Clientanwendung, die mit Exchange Online und Exchange lokal funktioniert.
  
Für die meisten Teil, Clients und das Web Services in Exchange, die sie als Ziel unabhängig davon, ob das Ziel ein Exchange Online, Exchange Online als Teil von Office 365, ist die gleiche Weise arbeiten oder lokale Exchange-Server. Es gibt jedoch einige Ausnahmen, und Sie sollten sicherstellen, dass die Anwendung, die sie behandeln kann. Verwenden Sie die Informationen in diesem Artikel zur einfacheren Entwerfen Ihrer Client sowohl Exchange Online als Ziel und lokale Exchange-Organisation.

<a name="autodiscover"> </a>

## <a name="autodiscover-client-programming-considerations"></a>AutoErmittlung clientbezogene Aspekte der Programmierung

[AutoErmittlung](autodiscover-for-exchange.md) stellt Konfigurationsinformationen für Exchange-Clients bereit. Eine Clientanwendung kann erkennen, dessen Konfigurationsinformationen in drei Möglichkeiten, je nachdem, ob der Client Exchange Online oder Exchange lokal gerichtet ist. 
  
**In Tabelle 1. AutoErmittlung Diensttypen und Exchange-Anwendungsbereich**

|**Diensttyp AutoErmittlung**|**Betrifft**|
|:-----|:-----|
|[SOAP-AutoErmittlung](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online und Versionen von Exchange lokal beginnend mit Exchange 2010  <br/> |
|[POX-AutoErmittlung](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online und Versionen von Exchange lokal beginnend mit Exchange 2007  <br/> |
|[Service Connection Point (SCP)-Suche](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) <br/> |Lokale Exchange-Organisation beginnend mit Exchange 2007-Versionen  <br/> |
   
Zusätzlich zu den Client Konfigurationsinformationen, SOAP POX AutoErmittlung auch die Exchange-Version-Dienst und zu anzugeben, ob der Dienst von Exchange Online gehostet wird. Diese Informationen wird in anderen Elementen, abhängig von der Art der AutoErmittlung zurückgegeben, die Sie verwenden.
  
**In Tabelle 2. AutoErmittlung-Elemente, die Service-Version und Exchange Online hosten Informationen zurückgeben**

|**Diensttyp AutoErmittlung**|**XML-Element, das Service-Version enthält**|**XML-Element, der angibt, ob der Benutzer ein Konto mit Exchange Online**|
|:-----|:-----|:-----|
|SOAP-AutoErmittlung  <br/> |[Einstellung (SOAP)](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) -Element mit dem **CasVersion** -Textwert.  <br/> |[Einstellung (SOAP)](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) -Element mit dem **UserMSOnline** -Textwert.  <br/> |
|POX-AutoErmittlung  <br/> |[ServerVersion (POX)](http://msdn.microsoft.com/library/2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a%28Office.15%29.aspx) <br/> |**MicrosoftOnline** <br/> |
   
Stellen Sie sicher, dass Ihre Clients diese Informationen erfasst wird, damit die [Featuregruppe](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md) ausgerichtet werden können, die auf dem Exchange-Server verfügbar ist. Dies ist nützlich, um zu bestimmen, ob Ihr Client unterschiedlichem Verhalten basierend erwarten kann auf gibt an, ob das Postfach des Benutzers in Exchange Online befindet oder lokale Exchange-Organisation. 

<a name="testing"> </a>

## <a name="testing-and-log-files-in-applications-that-target-exchange-online"></a>Testen und Log-Dateien in Anwendungen, die Exchange Online als Ziel

Exchange Online bietet keinen Zugriff auf die Protokolldateien für EWS-Protokoll, EWS-Leistungsindikatoren und Service EWS-bezogenen Ereignisse, die auf lokalen Exchange-Servern verfügbar sind. Zugriff auf diese eignet sich jedoch in ermitteln, wie die Anwendung ausgeführt wird, bei einer Interaktion mit Exchange-Webdienste. Stellen Sie sicher, dass Sie die Anwendung für einen Test Exchange lokale Server testen, damit Sie die Leistung optimieren können. Wenn möglich, können Sie [ändern die begrenzungseinstellungen](http://technet.microsoft.com/en-us/library/bb232205%28v=exchg.150%29.aspx#Policies) auf dem Testserver entsprechend die begrenzungseinstellungen für Exchange Online, damit das Verhalten der Anwendung beim Herstellen einer zu Exchange Online Verbindung ausgewertet werden kann. 
  
> [!TIP]
> Das [EWSRelentless](https://ewsrelentless.codeplex.com/) -Tool können Sie einen EWS-Auslastungstest ausführen. Können dieses Tool mit einem Testserver, die EWS-Protokolle, EWS-Leistungsindikatoren, Dienstereignisse und die EWS-Einschränkung Einstellungen Sie um besser zu verstehen, wie unter Last EWS ausgeführt wird. 

<a name="throttling"> </a>

## <a name="throttling-settings-and-exchange-online"></a>Begrenzungseinstellungen und Exchange Online

Die Standardwerte für die [EWS-begrenzungseinstellungen](ews-throttling-in-exchange.md) unterscheiden sich für Exchange Online als sie für lokale Exchange-Organisation sind. Darüber hinaus können Sie nicht Exchange Online begrenzungseinstellungen ändern. Exchange-Verwaltungsshell-Cmdlets können Sie um die begrenzungseinstellungen für lokale Exchange-Organisation zu ermitteln. Diese Cmdlets sind jedoch nicht für Exchange Online aktiviert. 

<a name="ems"> </a>

## <a name="exchange-management-shell-cmdlets-and-configuration-settings"></a>Einstellungen für Exchange-Verwaltungsshell-Cmdlets und Konfiguration

Eine Reihe von Cmdlets kann direkt oder indirekt Einfluss auf die Web-Service-APIs in Exchange Online und lokalen Exchange. Cmdlets sind nicht verfügbar für in Exchange Online Folgendes:
  
- Einschränkungseinstellungen für 
    
- Einstellungen für virtuelle Verzeichnisse 
    
- Authentifizierungseinstellungen
    
Ausführliche Informationen zu den Cmdlets, die für Exchange Online zur Verfügung stehen, finden Sie unter [PowerShell-Cmdlets in Exchange Online](http://help.outlook.com/en-us/140/dd575549.aspx). Weitere Informationen zu Cmdlets aufgeführt, die für lokale Exchange-Organisation zur Verfügung stehen, finden Sie unter [Exchange 2013 Cmdlets](http://technet.microsoft.com/en-us/library/bb124413%28v=exchg.150%29.aspx).
  
## <a name="client-affinity-and-network-load-balancers"></a>Clientaffinität und Netzwerk-Lastenausgleichsmodule
<a name="affinity"> </a>

Die meisten EWS-Kommunikation erfordert nicht, dass der Client Aufrechterhaltung der Affinität mit Exchange teilnehmen. Die Abonnements für Ereignisse Postfach erfordern, dass der Client Cookies und andere Informationen, die Affinität mit dem Exchange-Server zu verwalten, die verwaltet die Warteschlange der Postfach-Ereignisse für einen Benutzer bereitstellen. Exchange Server 2010 verwendet die Exchangecookie um Clientaffinität über das Netzwerk zum Lastenausgleich zu verwalten. Exchange Online und Versionen von Exchange lokal beginnend mit Exchange 2013 mithilfe der [X-AnchorMailbox-Header, X-PreferServerAffinity-Header und X BackEndOverrideCookie Cookie](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howmaintained) Affinität für Postfach Benachrichtigungen verwalten. 
  
## <a name="authentication"></a>Authentifizierung
<a name="auth"> </a>

Clients können mit Exchange Online mithilfe von Basic oder OAuth authentifizieren. Lokale Exchange-Organisation beginnend mit Exchange 2013-Versionen verwenden NTLM standardmäßig; Es ist jedoch möglich, lokale Exchange-Organisation Standardauthentifizierung sowie zu konfigurieren. 
  
## <a name="client-latency-diagnostics"></a>Client Wartezeit Diagnose
<a name="diag"> </a>

Exchange Online erfasst Client Wartezeit Diagnose, wenn sie gemeldet werden. Auf diese Weise der Behandlung von Verbindungsproblemen mit Exchange Online Support von Microsoft. Lokale Exchange-erfasst Client Wartezeit Diagnose nicht. Wenn der Client Exchange lokal bezieht, kann nicht der Client Wartezeit Diagnose an den Server angeben.
  
## <a name="functionality-in-the-ews-managed-api"></a>Funktionalität in die EWS Managed API
<a name="ewsma"> </a>

Die EWS Managed API macht einige Funktionen, die speziell für Exchange lokal, wie Service Punkt Verbindung-Suche und einige Funktionen, die speziell für Exchange Online, wie beispielsweise Client Wartezeit gemeldet wird. Beachten Sie, dass es ist möglich, dass einige Funktionen in Exchange Online implementiert werden, bevor es in die EWS Managed API implementiert wird. 
  
Die folgende Funktionalität EWS Managed API gilt nur für Exchange Online:
  
- Client Wartezeit reporting
    
- Vor dem Standardauthentifizierung
    
- Die Möglichkeit zum anfordern, dass die RequestId in Antworten zurückgegeben werden
    
## <a name="api-features-in-exchange-online-plans-and-exchange-server-editions"></a>API-Funktionen in Exchange Online-Plänen und Exchange Server-Editionen
<a name="exo"> </a>

Unterschiedliche Featuregruppen in verschiedenen Office 365 und Exchange Online-Plänen oder in der Standard- und Enterprise-Versionen von Exchange Server möglicherweise verfügbar. Beachten Sie, dass einige API-Funktionen möglicherweise nicht verfügbar, an die Clientanwendung je nach der Exchange Online-Plan oder Exchange Server-Edition, das Postfach des Benutzers hostet. 
  
**Tabelle 3. API-Funktion Varianten über Editionen und Pläne**

|**API-Funktion**|**Plan oder Edition Aspekte**|
|:-----|:-----|
|EWS wird der Zugriff auf Konten, mit Ausnahme der über den Exchange-Identitätswechsel  <br/> |Nicht zulässig, der [Office 365 für Unternehmen – Kiosk Pläne](http://office.microsoft.com/en-us/business/compare-office-365-kiosk-plans-FX103178917.aspx).  <br/> |
|Unified Messaging (UM)  <br/> |Nur mit Office 365 Enterprise (E3) planen, Exchange Online – Plan 2 und Exchange Server 2013 Enterprise Edition verfügbar.  <br/> |
|Integration des Active Directory-Domänendienste (AD DS)  <br/> |Mit dem Office 365 Small Business und Office 365 Small Business Premium Plan nicht verfügbar.  <br/> |
|Enthält Information Rights Management, Archivierung und gesetzliche  <br/> |Nur verfügbar in den Plänen Office 365 Enterprise (E3 und E4).  <br/> |
|Schutz vor Datenverlust  <br/> |Nur mit Office 365 Enterprise Pläne, Exchange Online – Plan 2 und Exchange Server 2013 Enterprise Edition verfügbar.  <br/> |
   
Da die Verfügbarkeit von Features ändern kann, sollten Sie überprüfen, die Exchange Online-Plänen und Exchange Server-Editionen bewerten, wie die Verfügbarkeit Ihrer Client auswirken kann. Sie können auch Entwerfen Ihrer Client überprüft Verfügbarkeit von Features mithilfe der [GetServiceConfiguration-Vorgang](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) oder zusenden Test für die Vorgänge, die die Funktionen zu implementieren. Wenn das Feature nicht verfügbar ist, wird die Antwort vom Server als solche angegeben. 
  
## <a name="other-considerations"></a>Weitere Aspekte
<a name="other"> </a>

Sie können folgende Aktion für lokale Exchange-Organisation, jedoch nicht Exchange Online ausführen:
  
- Erstellen Sie einen Client, der auf dem Exchange-Server installiert ist. 
    
- Installieren Sie [benutzerdefinierte Transport-Agents](../transport-agents/transport-agents-in-exchange-2013.md) , die die Bereitstellung und den Inhalt von Nachrichten, die Sie erstellen und senden mit EWS und anderen Clients auswirken können. 
    
## <a name="see-also"></a>Siehe auch

- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
- [Vergleich der Exchange Online und Exchange Server 2013](http://blogs.technet.com/b/exchange/archive/2012/09/19/comparing-exchange-online-and-exchange-server-2013.aspx)  
- [Alle Office 365 für Geschäftspläne vergleichen](http://office.microsoft.com/en-us/business/compare-all-office-365-for-business-plans-FX104051403.aspx)
- [EwsRelentless - laden EWS-Tool zum Generieren von](https://ewsrelentless.codeplex.com/)
- [Verfügbarkeit von Web Service-API in Exchange und die EWS Managed API](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
- [EWS-Einschränkung in Exchange](ews-throttling-in-exchange.md)
    

