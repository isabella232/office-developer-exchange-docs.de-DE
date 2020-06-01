---
title: Vergleich der Exchange Online und Exchange lokalen Clientprogrammierung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3c2eabe4-52bc-461e-a6dd-f65f22f16e50
description: In diesem Artikel erfahren Sie mehr über die Entwurfsüberlegungen zum Erstellen einer verwaltete EWS-API-oder EWS-Clientanwendung, die für die lokale Exchange Online und Exchange geeignet ist.
ms.openlocfilehash: 8b4dbae5cadfed377aa3a7179144a7cea68bc35c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456164"
---
# <a name="comparing-exchange-online-and-exchange-on-premises-client-programming"></a>Vergleich der Exchange Online und Exchange lokalen Clientprogrammierung

In diesem Artikel erfahren Sie mehr über die Entwurfsüberlegungen zum Erstellen einer verwaltete EWS-API-oder EWS-Clientanwendung, die für die lokale Exchange Online und Exchange geeignet ist.
  
In den meisten Fällen funktionieren Clients und die in Exchange angestrebten Webdienste auf die gleiche Weise, unabhängig davon, ob es sich bei dem Ziel um eine Exchange Online, Exchange Online als Teil von Office 365 oder lokalen Exchange-Server handelt. Es gibt jedoch einige Ausnahmen, und Sie sollten sicherstellen, dass Ihre Anwendung Sie verarbeiten kann. Verwenden Sie die Informationen in diesem Artikel, um Ihren Client so zu gestalten, dass er sowohl auf Exchange Online als auch auf lokale Exchange-Bereitstellung ausgerichtet ist.

<a name="autodiscover"> </a>

## <a name="autodiscover-client-programming-considerations"></a>Überlegungen zur Programmierung von Clients

Die [AutoErmittlung](autodiscover-for-exchange.md) stellt Konfigurationsinformationen für Exchange-Clients bereit. Eine Clientanwendung kann ihre Konfigurationsinformationen auf eine von drei Arten ermitteln, je nachdem, ob der Client auf Exchange Online oder lokale Exchange zielt. 
  
**Tabelle 1. AutoErmittlungsdienst Typen und Exchange-Anwendbarkeit**

|**AutoErmittlungsdienst-Typ**|**Gilt für**|
|:-----|:-----|
|[SOAP-AutoErmittlung](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online und Versionen von Exchange lokal, beginnend mit Exchange 2010  <br/> |
|[POX-AutoErmittlung](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online und Versionen von Exchange lokal, beginnend mit Exchange 2007  <br/> |
|[Dienstverbindungspunkt-Suche (Service Connection Points, SCP)](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) <br/> |Lokale Exchange-Versionen, beginnend mit Exchange 2007  <br/> |
   
Zusätzlich zu den Clientkonfigurationsinformationen gibt die SOAP-und POX-AutoErmittlung auch die Exchange-Dienstversion zurück und gibt an, ob der Dienst von Exchange Online gehostet wird. Diese Informationen werden je nach Typ der AutoErmittlung, die Sie verwenden, in verschiedenen Elementen zurückgegeben.
  
**Tabelle 2. Auto Ermittlungselemente, die Dienst Versions-und Exchange Online-Host Informationen zurückgeben**

|**AutoErmittlungsdienst-Typ**|**XML-Element, das die Dienstversion enthält**|**XML-Element, das angibt, ob der Benutzer über ein Exchange Online Konto verfügt**|
|:-----|:-----|:-----|
|SOAP-AutoErmittlung  <br/> |[Setting (SOAP)-](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) Element mit dem Textwert **CasVersion** .  <br/> |[Setting (SOAP)-](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) Element mit dem Textwert **UserMSOnline** .  <br/> |
|POX-AutoErmittlung  <br/> |[ServerVersion (POX)](https://msdn.microsoft.com/library/2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a%28Office.15%29.aspx) <br/> |**Microsoft Online** <br/> |
   
Stellen Sie sicher, dass der Client diese Informationen erfasst, damit er auf den auf dem Exchange-Server verfügbaren [Featuresatz](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md) ausgerichtet werden kann. Dies kann hilfreich sein, um festzustellen, ob Ihr Client ein anderes Verhalten erwarten kann, je nachdem, ob sich das Postfach des Benutzers in einem Exchange Online oder einer lokalen Exchange-Organisation befindet. 

<a name="testing"> </a>

## <a name="testing-and-log-files-in-applications-that-target-exchange-online"></a>Testen und Protokollieren von Dateien in Anwendungen, die auf Exchange Online Zielen

Exchange Online bietet keinen Zugriff auf die EWS-Protokolldateien, EWS-Leistungsindikatoren und Dienstereignisse im Zusammenhang mit EWS, die auf lokalen Exchange-Servern zur Verfügung stehen. Der Zugriff auf diese Informationen ist jedoch hilfreich, um zu ermitteln, wie Ihre Anwendung bei der Interaktion mit EWS ausgeführt wird. Stellen Sie sicher, dass Sie Ihre Anwendung mit einem lokalen Test Exchange-Server testen, um die Leistung zu optimieren. Wenn möglich, können Sie [die Einschränkungseinstellungen](https://technet.microsoft.com/library/bb232205%28v=exchg.150%29.aspx#Policies) auf dem Testserver so ändern, dass Sie den Drosselungseinstellungen für Exchange Online entsprechen, sodass Sie auswerten können, wie sich Ihre Anwendung beim Herstellen einer Verbindung mit Exchange Online verhält. 
  
> [!TIP]
> Sie können das [EWSRelentless](https://ewsrelentless.codeplex.com/) -Tool verwenden, um einen EWS-Auslastungstest auszuführen. Sie können dieses Tool mit einem Testserver, den EWS-Protokoll Protokollen, EWS-Leistungsindikatoren, Dienst Ereignissen und den EWS-Einschränkungseinstellungen verwenden, um besser zu verstehen, wie EWS unter Last ausgeführt wird. 

<a name="throttling"> </a>

## <a name="throttling-settings-and-exchange-online"></a>Einschränkungseinstellungen und Exchange Online

Die Standardwerte für die [EWS-Einschränkungseinstellungen](ews-throttling-in-exchange.md) sind für Exchange Online als für lokale Exchange-Umgebungen unterschiedlich. Außerdem können Sie Exchange Online Einschränkungseinstellungen nicht ändern. Sie können Exchange-Verwaltungsshell-Cmdlets verwenden, um die Einschränkungseinstellungen für Exchange lokal zu ermitteln. Diese Cmdlets sind jedoch für Exchange Online nicht aktiviert. 

<a name="ems"> </a>

## <a name="exchange-management-shell-cmdlets-and-configuration-settings"></a>Exchange-Verwaltungsshell-Cmdlets und Konfigurationseinstellungen

Eine Reihe von Cmdlets kann sich direkt oder indirekt auf die Webdienst-APIs in Exchange Online und lokale Exchange-Dienste auswirken. Cmdlets stehen in Exchange Online für Folgendes nicht zur Verfügung:
  
- Einschränkungseinstellungen 
    
- Einstellungen für das virtuelle Verzeichnis 
    
- Authentifizierungseinstellungen
    
Ausführliche Informationen zu den Cmdlets, die für Exchange Online zur Verfügung stehen, finden Sie unter [PowerShell-Cmdlets in Exchange Online](http://help.outlook.com/140/dd575549.aspx). Weitere Informationen zu Cmdlets, die für Exchange lokal verfügbar sind, finden Sie unter [Exchange 2013-Cmdlets](https://technet.microsoft.com/library/bb124413%28v=exchg.150%29.aspx).
  
## <a name="client-affinity-and-network-load-balancers"></a>Client Affinität und Netzwerklastenausgleich
<a name="affinity"> </a>

Für die meisten EWS-Kommunikation ist es nicht erforderlich, dass der Client an der Beibehaltung der Affinität mit Exchange teilnimmt. Die Abonnements für Post Fach Ereignisse erfordern, dass der Client Cookies und andere Informationen bereitstellt, um die Affinität mit dem Exchange-Server beizubehalten, der die Warteschlange von Post Fach Ereignissen für einen Benutzer verwaltet. Exchange Server 2010 verwendet die exchangecookie, um die Clientaffinität für Netzwerklastenausgleichs beizubehalten. Exchange Online und Versionen von Exchange lokal, beginnend mit Exchange 2013 verwenden Sie die [x-AnchorMailbox-Kopfzeile, die x-PreferServerAffinity-Kopfzeile und das x-BackEndOverrideCookie-Cookie](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howmaintained) , um die Affinität für Post Fach Benachrichtigungen beizubehalten. 
  
## <a name="authentication"></a>Authentifizierung
<a name="auth"> </a>

Clients können sich mit Exchange Online authentifizieren, indem Sie entweder Basic oder OAuth verwenden. Versionen von Exchange lokal, beginnend mit Exchange 2013 verwenden standardmäßig NTLM; Es ist jedoch möglich, Exchange lokal so zu konfigurieren, dass auch die Standardauthentifizierung verwendet wird. 
  
## <a name="client-latency-diagnostics"></a>Diagnose der Client Wartezeit
<a name="diag"> </a>

Exchange Online sammelt die Client Latenz Diagnose, wenn Sie gemeldet werden. Dies hilft dem Microsoft-Support bei der Behandlung von Verbindungsproblemen mit Exchange Online. Exchange lokal erfasst keine Client Latenz Diagnose. Wenn Ihr Client Exchange lokal anwendet, kann der Client keine Latenz Diagnose an den Server melden.
  
## <a name="functionality-in-the-ews-managed-api"></a>Funktionalität im verwaltete EWS-API
<a name="ewsma"> </a>

Das verwaltete EWS-API stellt einige Funktionen zur Verfügung, die speziell für lokale Exchange-Dienste, wie beispielsweise Service Points-Verbindungssuche, und einige spezifische Funktionen für Exchange Online, wie etwa die Berichterstellung über die Clientwartezeit, verfügbar sind. Beachten Sie, dass einige Funktionen in Exchange Online implementiert werden können, bevor Sie in der verwaltete EWS-API implementiert werden. 
  
Die folgende verwaltete EWS-API Funktionalität gilt nur für Exchange Online:
  
- Client Wartezeit-Berichterstellung
    
- Grundlegende vorab Authentifizierung
    
- Die Möglichkeit, anzufordern, dass die Anforderungs-Nr in Antworten zurückgegeben wird
    
## <a name="api-features-in-exchange-online-plans-and-exchange-server-editions"></a>API-Features in Exchange Online Plänen und Exchange Server-Editionen
<a name="exo"> </a>

Unterschiedliche Funktionsgruppen können in unterschiedlichen Office 365-und Exchange Online-Plänen oder in den Standard-und Enterprise-Versionen von Exchange Server verfügbar sein. Beachten Sie, dass je nach Exchange Online Plan oder Exchange Server Edition, die das Postfach eines Benutzers hostet, möglicherweise einige API-Funktionen für Ihre Clientanwendung nicht verfügbar sind. 
  
**Tabelle 3. Variationen von API-Features in Plänen und Editionen**

|**API-Feature**|**Überlegungen zu Plan oder Edition**|
|:-----|:-----|

| EWS-Zugriff auf Konten, außer über Exchange-Identitätswechsel  <br/> | Im Office 365 für Unternehmen nicht zulässig [– Kiosk Pläne](https://office.microsoft.com/business/compare-office-365-kiosk-plans-FX103178917.aspx).  <br/> |


| Unified Messaging (um)  <br/> | Nur verfügbar mit Office 365 Enterprise-Plan (E3), Exchange Onlineplan 2 und den Exchange Server 2013 Enterprise-Editionen.  <br/> | | Active Directory-Domänendienste (AD DS) Integration  <br/> | Nicht verfügbar im Office 365 Small Business-und Office 365 Small Business Premium-Plan.  <br/> | | Verwaltung von Informationsrechten, Archivierung und Rechtliche Aufbewahrungspflicht  <br/> | Nur mit den Plänen Office 365 Enterprise (E3 und E4) verfügbar.  <br/> | | Schutz vor Datenverlust  <br/> | Nur mit den Office 365 Enterprise Plänen, Exchange Online Plan 2 und Exchange Server 2013 Enterprise Editions verfügbar.  <br/> |
   
Da sich die Verfügbarkeit von Features ändern kann, wird empfohlen, dass Sie die Exchange Online Pläne und Exchange Server Editionen überprüfen, um auszuwerten, wie sich die Funktionsverfügbarkeit auf Ihren Client auswirken kann Sie können den Client auch so entwerfen, dass die Verfügbarkeit der Funktionen mithilfe des [GetServiceConfiguration-Vorgangs](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) überprüft wird, oder indem Sie Testanforderungen für die Vorgänge senden, die die Features implementieren. Wenn das Feature nicht verfügbar ist, wird die Antwort vom Server als solches angegeben. 
  
## <a name="other-considerations"></a>Andere Überlegungen
<a name="other"> </a>

Sie können die folgenden Aktionen ausführen, wenn Sie lokal auf Exchange, jedoch nicht auf Exchange Online Zielen:
  
- Erstellen Sie einen Client, der auf dem Exchange-Server installiert ist. 
    
- Installieren von [benutzerdefinierten Transport-Agents](../transport-agents/transport-agents-in-exchange-2013.md) , die sich auf die Zustellung und den Inhalt von Nachrichten auswirken können, die Sie mit EWS und anderen Clients erstellen und senden. 
    
## <a name="see-also"></a>Siehe auch

- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
- [Vergleichen von Exchange Online und Exchange Server 2013](https://blogs.technet.com/b/exchange/archive/2012/09/19/comparing-exchange-online-and-exchange-server-2013.aspx)  
- [Alle Office 365 für Unternehmen Pläne vergleichen](https://office.microsoft.com/business/compare-all-office-365-for-business-plans-FX104051403.aspx)
- [EwsRelentless-EWS-Tool zur Lastgenerierung](https://ewsrelentless.codeplex.com/)
- [Verfügbarkeit von Web Service-API in Exchange und die EWS Managed API](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
- [EWS-Einschränkung in Exchange](ews-throttling-in-exchange.md)
    

