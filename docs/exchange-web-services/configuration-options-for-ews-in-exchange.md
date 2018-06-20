---
title: Konfigurationsoptionen für EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6562639-9366-4a13-9fdb-2fa737833329
description: Hier finden Sie Informationen zu Konfigurationseinstellungen, die Ihre EWS-Client zugreifen kann, und die konfigurierbaren Exchange-Einstellungen, die Ihre EWS-Client beeinflussen können.
ms.openlocfilehash: d6c2866abf3dc16c77d84355afb9d86b0a9934c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756824"
---
# <a name="configuration-options-for-ews-in-exchange"></a>Konfigurationsoptionen für EWS in Exchange

Hier finden Sie Informationen zu Konfigurationseinstellungen, die Ihre EWS-Client zugreifen kann, und die konfigurierbaren Exchange-Einstellungen, die Ihre EWS-Client beeinflussen können. 
  
Viele Konfigurationseinstellungen können beeinflusst die EWS-Clientanwendung. Diese Konfigurationseinstellungen sind entweder: 
  
- Schreibgeschützt oder vom Client lesen schreibgeschützt.
    
- Zugreifen auf dem Exchange-Server, der Ihren EWS-Dienst gehostet wird.
    
Ein Client kann Einstellungen auf Exchange Online, Exchange Online als Teil von Office 365 und einem lokalen Exchange-Server zugreifen. Alle lokalen Exchange Server-Einstellungen stehen Exchange-Administratoren zur Verfügung. Allerdings sind nicht alle diese Einstellungen für Exchange Online-Mandantenadministratoren zur Verfügung. In diesem Artikel wird beschrieben, welche Konfiguration auf Clients, Exchange Server-Administratoren und Exchange Online-Mandanten Administratoren zugreifen können.
  
## <a name="configuration-settings-that-clients-can-access"></a>Konfigurationseinstellungen, die Clients zugreifen können

Die Clientanwendung abgerufen und eine Reihe von Konfigurationsoptionen vom Exchange-Server. Konfigurationseinstellungen, die alle EWS-Anwendungen werden von den AutoErmittlungsdienst bereitgestellt. Andere Konfigurationseinstellungen werden für bestimmte Anwendungsszenarien verwendet. 
  
**In Tabelle 1. Web-Service-Features, die Konfigurationsoptionen für EWS-Clients bereitstellen**

|**Funktion**|**Beschreibung**|
|:-----|:-----|
|AutoErmittlungsdienst  <br/> |Der [AutoErmittlungsdienst](autodiscover-for-exchange.md) bietet Ihrer Client-Anwendungen mit Konfigurationsinformationen, damit Ihr Client automatisch selbst mit EWS kommunizieren kann.  <br/> |
|Benutzerdefinierte Konfigurationsinformationen, die in einem Postfach gespeichert  <br/> |Sie können verschiedene Optionen zum [Speichern von benutzerdefinierten Konfigurationsinformationen](persistent-application-settings-in-ews-in-exchange.md) in Ihrem Postfach verwenden: Konfiguration Benutzerobjekte, benutzerdefinierte Elemente oder erweiterte Eigenschaften.  <br/> |
|Delegieren der Verwaltung  <br/> | EWS bietet CRUD-Vorgänge für die Verwaltung delegieren des Zugriffs auf ein Postfach. Stellvertretungen handelt es sich Benutzer, die Berechtigung zum Postfach eines anderen Benutzers zugreifen auf erteilt wurden.<br/><br/>  Sie können die [Stellvertretung Verwaltungsvorgänge](http://msdn.microsoft.com/en-us/library/bb409286%28v=exchg.150%29.aspx#bk_delegate_management) Delegieren der Verwaltung mithilfe der Exchange-Webdienste oder, wenn Sie die EWS Managed API verwenden, können Sie die folgenden Methoden verwenden:<br/><br/>- [ExchangeService.AddDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.GetDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getdelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.UpdateDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.RemoveDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |
|Konfiguration von eDiscovery-Suche  <br/> |eDiscovery-Clientanwendungen können [Search-Konfigurationsinformationen](http://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) , die eine eDiscovery Search-Abfrage eine Liste der Postfächer durchsucht, abrufen und der Bezeichner des Postfachs Compliance-Archive.  <br/> |
|Berechtigungen für Ordner  <br/> |Ordnerberechtigungen beschränkt, was ein Benutzer in einem öffentlichen Ordner möglich ist, und im Fall von Stellvertretungszugriff, welche Stellvertreter Möglichkeiten im Ordner eines anderen Benutzers. Die [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) -Methode oder der [GetFolder-Vorgang](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) können den Berechtigungssatz jedem Ordner, einschließlich öffentlichen Ordnern, freigegebene private Ordner oder Ordner für die Benutzer Stellvertretungszugriff haben Zugriff auf.  <br/> |
|E-Mail-Infos, Unified Messaging oder -Schutzregeln  <br/> |Der [Vorgang GetServiceConfiguration](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) enthält nur-Lese- [Service-Konfigurationsinformationen](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) für e-Mail-Infos, Unified Messaging und Regeln für den Schutz.  <br/> |
   
## <a name="configuration-settings-that-administrators-can-access-on-the-exchange-server"></a>Konfigurationseinstellungen, die Administratoren auf dem Exchange-Server zugreifen können

Die meisten Client Application Szenarien erfordern keine Änderungen an den Konfigurationseinstellungen für; Führen Sie jedoch einige Szenarien. Um eine Anwendung der mittleren Ebene, fungiert als Benutzer zu aktivieren, müssen Sie beispielsweise Exchange-Identitätswechsel auf dem Server festgelegt. Beachten Sie, dass einige Einstellungen nur auf Exchange-Servern am Standort zugegriffen werden können. Wenn Sie Exchange Online verwenden möchten, müssen die Clientanwendung entwickelt die Standardeinstellungen.
  
**In Tabelle 2. Exchange Server-Konfigurationsoptionen, die Auswirkung auf EWS-clients**

|**Funktion**|**Von Exchange Online möglich?**|**Weitere Informationen finden Sie unter...**|
|:-----|:-----|:-----|
|Einstellungen für virtuelle Verzeichnisse (einschließlich Authentifizierung)  <br/> |Nein  <br/> |[Get-WebServicesVirtualDirectory](http://technet.microsoft.com/en-us/library/aa998810%28v=exchg.150%29.aspx) <br/> [Set-WebServicesVirtualDirectory](http://technet.microsoft.com/en-us/library/aa997233%28v=exchg.150%29.aspx) <br/> |
|AutoErmittlung  <br/> |Nein  <br/> |[Get-AutodiscoverVirtualDirectory](http://technet.microsoft.com/en-us/library/aa996819%28v=exchg.150%29.aspx) <br/> [Set-AutodiscoverVirtualDirectory](http://technet.microsoft.com/en-us/library/aa998601%28v=exchg.150%29.aspx) <br/> |
|Compliance  <br/> |Ja  <br/> |[Archivierung](http://technet.microsoft.com/en-us/library/dd979800%28v=exchg.150%29.aspx) <br/> [eDiscovery](http://technet.microsoft.com/en-us/library/dd298021%28v=exchg.150%29.aspx) <br/> [Anhalten der Aufbewahrungszeit](http://technet.microsoft.com/en-us/library/dd335168%28v=exchg.150%29.aspx) <br/> [Verhinderung von Datenverlust](http://technet.microsoft.com/en-us/library/jj150527%28v=exchg.150%29.aspx) <br/> |
|Delegieren der Verwaltung  <br/> |Ja  <br/> |[Verwalten von Berechtigungen für Empfänger](http://technet.microsoft.com/en-us/library/jj919240%28v=exchg.150%29.aspx) <br/> |
|Exchange-Identitätswechsel  <br/> |Ja  <br/> |[Konfigurieren des Exchange-Identitätswechsels](http://msdn.microsoft.com/en-us/library/bb204095%28EXCHG.140%29.aspx) <br/> |
|E-Mail-Infos, Unified Messaging oder -Schutzregeln  <br/> |Ja  <br/> |[E-Mail-Infos](http://technet.microsoft.com/en-us/library/jj649091%28v=exchg.150%29.aspx) <br/> [Unified Messaging-Cmdlets](http://technet.microsoft.com/en-us/library/aa997665%28v=exchg.150%29.aspx) <br/> [Outlook-Schutzregeln](http://technet.microsoft.com/en-us/library/dd638178%28v=exchg.150%29.aspx) <br/> |
|Drosselung  <br/> |Nein  <br/> |[Einschränkungseinstellungen für](ews-throttling-in-exchange.md) <br/> |
|Filtern von Benutzer-agent  <br/> |Ja  <br/> |[Filtern von Benutzer-agent](how-to-control-access-to-ews-in-exchange.md) <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Abrufen von Service-Konfigurationsinformationen mithilfe der EWS in Exchange](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)   
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)   
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

