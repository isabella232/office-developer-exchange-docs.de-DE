---
title: Vergleichen der lokalen Exchange Online- und Exchange-Clientprogrammierung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3c2eabe4-52bc-461e-a6dd-f65f22f16e50
description: Erfahren Sie mehr über die Entwurfsüberlegungen zum Erstellen einer verwalteten EWS-API oder EWS-Clientanwendung, die mit Exchange Online und lokalen Exchange arbeitet.
ms.openlocfilehash: 438965656e31eca586d06a5e0b6794c0eda87621
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512288"
---
# <a name="comparing-exchange-online-and-exchange-on-premises-client-programming"></a>Vergleichen der lokalen Exchange Online- und Exchange-Clientprogrammierung

Erfahren Sie mehr über die Entwurfsüberlegungen zum Erstellen einer verwalteten EWS-API oder EWS-Clientanwendung, die mit Exchange Online und lokalen Exchange arbeitet.
  
In den meisten Fällen funktionieren Clients und die Webdienste in Exchange, auf die sie abzielen, auf die gleiche Weise, unabhängig davon, ob das Ziel ein Exchange Online, Exchange Online als Teil Office 365 oder Exchange lokalen Server ist. Es gibt jedoch einige Ausnahmen, und Sie sollten sicherstellen, dass ihre Anwendung diese behandeln kann. Verwenden Sie die Informationen in diesem Artikel, um Ihren Client so zu gestalten, dass er sowohl Exchange Online als auch Exchange lokal ausgerichtet ist.

<a name="autodiscover"> </a>

## <a name="autodiscover-client-programming-considerations"></a>Überlegungen zur Programmierung von AutoErmittlungsclients

[Die AutoErmittlung](autodiscover-for-exchange.md) stellt Konfigurationsinformationen für Exchange Clients bereit. Eine Clientanwendung kann ihre Konfigurationsinformationen auf eine von drei Arten ermitteln, je nachdem, ob der Client Exchange Online oder Exchange lokal ausgerichtet ist. 
  
**Tabelle 1. AutoErmittlungsdiensttypen und Exchange Anwendbarkeit**

|**AutoErmittlungsdiensttyp**|**Gilt für**|
|:-----|:-----|
|[SOAP-AutoErmittlung](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online und Versionen von Exchange lokal ab Exchange 2010  <br/> |
|[POX-AutoErmittlung](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online und Versionen von Exchange lokal ab Exchange 2007  <br/> |
|[Dienstverbindungspunkt(SCP)-Nachschlagevorgang](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) <br/> |Lokale Versionen von Exchange ab Exchange 2007  <br/> |
   
Zusätzlich zu den Clientkonfigurationsinformationen gibt die SOAP- und POX-AutoErmittlung auch die Exchange Dienstversion zurück und gibt an, ob der Dienst von Exchange Online gehostet wird. Diese Informationen werden in verschiedenen Elementen zurückgegeben, je nach Typ der autoErmittlung, die Sie verwenden.
  
**Tabelle 2. AutoErmittlungselemente, die Dienstversion und Exchange Online Hostinginformationen zurückgeben**

|**AutoErmittlungsdiensttyp**|**XML-Element, das die Dienstversion enthält**|**XML-Element, das angibt, ob der Benutzer über ein Exchange Online Konto verfügt**|
|:-----|:-----|:-----|
|SOAP-AutoErmittlung  <br/> |[Setting (SOAP)-Element](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) mit dem **CasVersion-Textwert.**  <br/> |[Setting (SOAP)-Element](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) mit dem **UserMSOnline-Textwert.**  <br/> |
|POX-AutoErmittlung  <br/> |[ServerVersion (POX)](https://msdn.microsoft.com/library/2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a%28Office.15%29.aspx) <br/> |**MicrosoftOnline** <br/> |
   
Stellen Sie sicher, dass Ihr Client diese Informationen erfasst, damit er auf den [Featuresatz](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md) abzielen kann, der auf dem Exchange Server verfügbar ist. Dies kann hilfreich sein, um zu bestimmen, ob Ihr Client ein anderes Verhalten erwarten kann, je nach dem, ob sich das Postfach des Benutzers in einer Exchange Online oder Exchange lokalen Organisation befindet. 

<a name="testing"> </a>

## <a name="testing-and-log-files-in-applications-that-target-exchange-online"></a>Testen und Protokollieren von Dateien in Anwendungen, die auf Exchange Online abzielen

Exchange Online bietet keinen Zugriff auf die EWS-Protokollprotokolldateien, EWS-Leistungsindikatoren und EWS-bezogenen Dienstereignisse, die auf lokalen Exchange Servern verfügbar sind. Der Zugriff darauf ist jedoch hilfreich, wenn Sie ermitteln, wie Ihre Anwendung bei der Interaktion mit EWS funktioniert. Stellen Sie sicher, dass Sie Ihre Anwendung mit einem Test Exchange lokalen Server testen, damit Sie die Leistung optimieren können. Wenn möglich, können Sie [die Einschränkungseinstellungen](https://technet.microsoft.com/library/bb232205%28v=exchg.150%29.aspx#Policies) auf Dem Testserver so ändern, dass sie den Einschränkungseinstellungen für Exchange Online entsprechen. Sie können daher bewerten, wie sich Ihre Anwendung verhält, wenn sie eine Verbindung mit Exchange Online herstellt. 
  
> [!TIP]
> Sie können das [EWSRelentless-Tool](https://ewsrelentless.codeplex.com/) verwenden, um einen EWS-Auslastungstest durchzuführen. Sie können dieses Tool mit einem Testserver, den EWS-Protokollprotokollen, EWS-Leistungsindikatoren, Dienstereignissen und den EWS-Einschränkungseinstellungen verwenden, um besser zu verstehen, wie EWS bei Auslastung funktioniert. 

<a name="throttling"> </a>

## <a name="throttling-settings-and-exchange-online"></a>Einschränkungseinstellungen und Exchange Online

Die Standardwerte für die [EWS-Einschränkungseinstellungen](ews-throttling-in-exchange.md) sind für Exchange Online anders als für Exchange lokal. Außerdem können Sie Exchange Online Einschränkungseinstellungen nicht ändern. Sie können Exchange Verwaltungsshell-Cmdlets verwenden, um die Einschränkungseinstellungen für Exchange lokal zu ermitteln. Diese Cmdlets sind jedoch nicht für Exchange Online aktiviert. 

<a name="ems"> </a>

## <a name="exchange-management-shell-cmdlets-and-configuration-settings"></a>Exchange Cmdlets und Konfigurationseinstellungen der Verwaltungsshell

Eine Reihe von Cmdlets kann sich direkt oder indirekt auf die Webdienst-APIs in Exchange Online und Exchange lokal auswirken. Cmdlets sind in Exchange Online nicht für Folgendes verfügbar:
  
- Einschränkungseinstellungen 
    
- Einstellungen für virtuelles Verzeichnis 
    
- Authentifizierungseinstellungen
    
Ausführliche Informationen zu den Cmdlets, die für Exchange Online verfügbar sind, finden Sie [unter PowerShell-Cmdlets in Exchange Online.](http://help.outlook.com/140/dd575549.aspx) Weitere Informationen zu Cmdlets, die für Exchange lokal verfügbar sind, finden Sie unter [Exchange 2013-Cmdlets.](https://technet.microsoft.com/library/bb124413%28v=exchg.150%29.aspx)
  
## <a name="client-affinity-and-network-load-balancers"></a>Clientaffinität und Netzwerklastenausgleich
<a name="affinity"> </a>

Die meisten EWS-Kommunikationen erfordern nicht, dass der Client an der Aufrechterhaltung der Affinität mit Exchange teilnimmt. Die Abonnements für Postfachereignisse erfordern, dass der Client Cookies und andere Informationen bereitstellt, um die Affinität mit dem Exchange-Server beizubehalten, der die Warteschlange mit Postfachereignissen für einen Benutzer verwaltet. Exchange Server 2010 verwendet exchangecookie, um die Clientaffinität über Netzwerklastenausgleichsmodule hinweg aufrechtzuerhalten. Exchange Online und Versionen von Exchange lokal ab Exchange 2013 verwenden den [X-AnchorMailbox-Header, den X-PreferServerAffinity-Header und das X-BackEndOverrideCookie-Cookie,](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howmaintained) um die Affinität für Postfachbenachrichtigungen aufrechtzuerhalten. 
  
## <a name="authentication"></a>Authentifizierung
<a name="auth"> </a>

Clients können sich mit Exchange Online mithilfe von Basic oder OAuth authentifizieren. Versionen von Exchange lokal ab Exchange 2013 verwenden standardmäßig NTLM. Es ist jedoch möglich, Exchange lokal für die Verwendung der Standardauthentifizierung zu konfigurieren. 
  
## <a name="client-latency-diagnostics"></a>Clientlatenzdiagnose
<a name="diag"> </a>

Exchange Online erfasst die Clientlatenzdiagnose, wenn sie gemeldet werden. Dies hilft Microsoft bei der Behandlung von Konnektivitätsproblemen mit Exchange Online. Exchange lokal erfasst keine Clientlatenzdiagnose. Wenn Ihr Client Exchange lokalen Ziel hat, kann der Client keine Latenzdiagnose an den Server melden.
  
## <a name="functionality-in-the-ews-managed-api"></a>Funktionalität in der verwalteten EWS-API
<a name="ewsma"> </a>

Die verwaltete EWS-API macht einige Funktionen verfügbar, die spezifisch für Exchange lokalen Dienstpunkt sind, z. B. die Dienstpunktverbindungssuche, und einige Funktionen, die für Exchange Online spezifisch sind, z. B. Clientlatenzberichte. Beachten Sie, dass einige Funktionen in Exchange Online implementiert werden können, bevor sie in der verwalteten EWS-API implementiert werden. 
  
Die folgende verwaltete EWS-API-Funktionalität gilt nur für Exchange Online:
  
- Clientlatenzberichterstellung
    
- Standard-Vorauthentifizierung
    
- Die Möglichkeit, die Rückgabe der RequestId in Antworten anzufordern
    
## <a name="api-features-in-exchange-online-plans-and-exchange-server-editions"></a>API-Features in Exchange Online Plänen und Exchange Server Editionen
<a name="exo"> </a>

Unterschiedliche Featuresätze sind möglicherweise in verschiedenen Office 365 und Exchange Online Plänen oder in den Standard- und Unternehmensversionen von Exchange Server verfügbar. Beachten Sie, dass einige API-Funktionen je nach Exchange Online Plan oder Exchange Server Edition, die das Postfach eines Benutzers hostet, möglicherweise nicht für Ihre Clientanwendung verfügbar sind. 
   
Da sich die Verfügbarkeit von Features ändern kann, empfehlen wir, die Exchange Online Pläne zu überprüfen und Exchange Server Editionen zu überprüfen, um zu bewerten, wie sich die Verfügbarkeit von Features auf Ihren Client auswirken kann. Sie können Ihren Client auch so entwerfen, dass die Verfügbarkeit von Features mithilfe des [GetServiceConfiguration-Vorgangs](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) überprüft wird, oder indem Sie Testanforderungen für die Vorgänge senden, die die Features implementieren. Wenn das Feature nicht verfügbar ist, wird die Antwort vom Server als solches angegeben. 
  
## <a name="other-considerations"></a>Andere Überlegungen
<a name="other"> </a>

Sie können die folgenden Aktionen ausführen, wenn Sie auf Exchange lokalen, aber nicht Exchange Online abzielen:
  
- Erstellen Sie einen Client, der auf dem Exchange Server installiert ist. 
    
- Installieren Sie [benutzerdefinierte Transport-Agents,](../transport-agents/transport-agents-in-exchange-2013.md) die sich auf die Zustellung und den Inhalt von Nachrichten auswirken können, die Sie mit EWS und anderen Clients erstellen und senden. 
    
## <a name="see-also"></a>Siehe auch

- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
- [Vergleich von Exchange Online und Exchange Server 2013](https://blogs.technet.com/b/exchange/archive/2012/09/19/comparing-exchange-online-and-exchange-server-2013.aspx)  
- [Vergleichen aller Office 365 für Business-Pläne](https://office.microsoft.com/business/compare-all-office-365-for-business-plans-FX104051403.aspx)
- [EwsRelentless – EWS-Tool zur Generierung von Lasten](https://ewsrelentless.codeplex.com/)
- [Verfügbarkeit von Web Service-API in Exchange und die EWS Managed API](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
- [EWS-Einschränkung in Exchange](ews-throttling-in-exchange.md)
    

