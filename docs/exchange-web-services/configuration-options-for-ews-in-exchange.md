---
title: Konfigurationsoptionen für EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: f6562639-9366-4a13-9fdb-2fa737833329
description: Hier finden Sie Informationen zu Konfigurationseinstellungen, auf die Ihr EWS-Client zugreifen kann, und zu den konfigurierbaren Exchange Einstellungen, die sich auf Ihren EWS-Client auswirken können.
ms.openlocfilehash: ed7667086b36897fd07031526e5a4657a120d505
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522285"
---
# <a name="configuration-options-for-ews-in-exchange"></a>Konfigurationsoptionen für EWS in Exchange

Hier finden Sie Informationen zu Konfigurationseinstellungen, auf die Ihr EWS-Client zugreifen kann, und zu den konfigurierbaren Exchange Einstellungen, die sich auf Ihren EWS-Client auswirken können. 
  
Viele Konfigurationseinstellungen können sich darauf auswirken, was Ihre EWS-Clientanwendung tun kann. Die folgenden Konfigurationseinstellungen sind: 
  
- Schreibgeschützt oder schreibgeschützt vom Client.
    
- Zugriff auf den Exchange Server, der Ihren EWS-Dienst hostet.
    
Ein Client kann auf Einstellungen auf Exchange Online, Exchange Online als Teil Office 365 und auf einem lokalen Exchange-Server zugreifen. Alle lokalen Exchange Servereinstellungen stehen Exchange Administratoren zur Verfügung. Allerdings stehen nicht alle diese Einstellungen Exchange Online Mandantenadministratoren zur Verfügung. In diesem Artikel wird beschrieben, auf welche Konfigurationseinstellungen Clients, Exchange Server Administratoren und Exchange Online Mandantenadministratoren zugreifen können.
  
## <a name="configuration-settings-that-clients-can-access"></a>Konfigurationseinstellungen, auf die Clients zugreifen können

Ihre Clientanwendung kann eine Reihe von Konfigurationsoptionen vom Exchange Server abrufen und festlegen. Konfigurationseinstellungen, die alle EWS-Anwendungen benötigen, werden vom AutoErmittlungsdienst bereitgestellt. Andere Konfigurationseinstellungen werden für bestimmte Anwendungsszenarien verwendet. 
  
**Tabelle 1. Webdienstfeatures, die Konfigurationsoptionen für EWS-Clients bereitstellen**

|**Feature**|**Beschreibung**|
|:-----|:-----|
|AutoErmittlungsdienst  <br/> |Der [AutoErmittlungsdienst](autodiscover-for-exchange.md) stellt Ihren Clientanwendungen Konfigurationsinformationen bereit, sodass der Client sich automatisch für die Kommunikation mit EWS konfigurieren kann.  <br/> |
|In einem Postfach gespeicherte benutzerdefinierte Konfigurationsinformationen  <br/> |Sie können eine von mehreren Optionen verwenden, um [benutzerdefinierte Konfigurationsinformationen](persistent-application-settings-in-ews-in-exchange.md) in Ihrem Postfach zu speichern: Benutzerkonfigurationsobjekte, benutzerdefinierte Elemente oder erweiterte Eigenschaften.  <br/> |
|Stellvertretungsverwaltung  <br/> | EWS bietet CRUD-Vorgänge zum Verwalten des Delegatenzugriffs auf ein Postfach. Stellvertretungen sind Benutzer, denen die Berechtigung für den Zugriff auf das Postfach eines anderen Benutzers erteilt wurde.<br/><br/>  Sie können die [Delegatverwaltungsvorgänge](https://msdn.microsoft.com/library/bb409286%28v=exchg.150%29.aspx#bk_delegate_management) verwenden, um die Stellvertretungsverwaltung mithilfe von EWS zu aktivieren, oder wenn Sie die verwaltete EWS-API verwenden, können Sie die folgenden Methoden verwenden:<br/><br/>- [ExchangeService.AddDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.GetDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getdelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.RemoveDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |
|eDiscovery-Suchkonfiguration  <br/> |eDiscovery-Clientanwendungen können [Suchkonfigurationsinformationen](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) abrufen, die eine eDiscovery-Suchabfrage, eine Liste durchsuchbarer Postfächer und den Bezeichner von in-situ-Postfachspeichern enthalten.  <br/> |
|Ordnerberechtigungen  <br/> |Ordnerberechtigungen beschränken, was ein Benutzer in einem öffentlichen Ordner tun kann, und im Falle des Stellvertretungszugriffs, was ein Delegat im Ordner eines anderen Benutzers tun kann. Sie können entweder die [Folder.Bind-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) oder den [GetFolder-Vorgang](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) verwenden, um auf den Berechtigungssatz jedes Ordners zuzugreifen, einschließlich öffentlicher Ordner, freigegebener privater Ordner oder Ordner, auf die Benutzer Stellvertretungszugriff haben.  <br/> |
|E-Mail-Tipps, Unified Messaging oder Schutzregeln  <br/> |Der [GetServiceConfiguration-Vorgang](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) enthält schreibgeschützte [Dienstkonfigurationsinformationen](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) für E-Mail-Tipps, Unified Messaging und Schutzregeln.  <br/> |
   
## <a name="configuration-settings-that-administrators-can-access-on-the-exchange-server"></a>Konfigurationseinstellungen, auf die Administratoren auf dem Exchange Server zugreifen können

Die meisten Clientanwendungsszenarien erfordern keine Änderungen an den Serverkonfigurationseinstellungen. In einigen Szenarien ist dies jedoch der Fall. Um beispielsweise zu ermöglichen, dass eine Anwendung auf der mittleren Ebene als Benutzer fungiert, müssen Sie Exchange Identitätswechsel auf dem Server festlegen. Beachten Sie, dass auf einige Einstellungen nur auf lokalen Exchange Servern zugegriffen werden kann. Wenn Sie auf Exchange Online abzielen, muss Ihre Clientanwendung möglicherweise mit den Standardeinstellungen arbeiten.
  
**Tabelle 2. Exchange Serverkonfigurationsoptionen, die sich auf EWS-Clients auswirken**

|**Feature**|**Von Exchange Online aus zugänglich?**|**Weitere Informationen finden Sie unter...**|
|:-----|:-----|:-----|
|Einstellungen für virtuelles Verzeichnis (einschließlich Authentifizierung)  <br/> |Nein  <br/> |[Get-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa998810%28v=exchg.150%29.aspx) <br/> [Set-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx) <br/> |
|AutoErmittlung  <br/> |Nein  <br/> |[Get-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa996819%28v=exchg.150%29.aspx) <br/> [Set-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa998601%28v=exchg.150%29.aspx) <br/> |
|Compliance  <br/> |Ja  <br/> |[Archivierung](https://technet.microsoft.com/library/dd979800%28v=exchg.150%29.aspx) <br/> [eDiscovery](https://technet.microsoft.com/library/dd298021%28v=exchg.150%29.aspx) <br/> [Anhalten der Aufbewahrungszeit](https://technet.microsoft.com/library/dd335168%28v=exchg.150%29.aspx) <br/> [Verhinderung von Datenverlust](https://technet.microsoft.com/library/jj150527%28v=exchg.150%29.aspx) <br/> |
|Stellvertretungsverwaltung  <br/> |Ja  <br/> |[Manage Permissions for Recipients](https://technet.microsoft.com/library/jj919240%28v=exchg.150%29.aspx) <br/> |
|Exchange Identitätswechsel  <br/> |Ja  <br/> |[Konfigurieren Exchange Identitätswechsels](https://msdn.microsoft.com/library/bb204095%28EXCHG.140%29.aspx) <br/> |
|E-Mail-Tipps, Unified Messaging oder Schutzregeln  <br/> |Ja  <br/> |[E-Mail-Info](https://technet.microsoft.com/library/jj649091%28v=exchg.150%29.aspx) <br/> [Unified Messaging-Cmdlets](https://technet.microsoft.com/library/aa997665%28v=exchg.150%29.aspx) <br/> [Outlook Schutzregeln](https://technet.microsoft.com/library/dd638178%28v=exchg.150%29.aspx) <br/> |
|Einschränkung  <br/> |Nein  <br/> |[Einschränkungseinstellungen](ews-throttling-in-exchange.md) <br/> |
|Benutzer-Agent-Filterung  <br/> |Ja  <br/> |[Benutzer-Agent-Filterung](how-to-control-access-to-ews-in-exchange.md) <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Abrufen von Dienstkonfigurationsinformationen mithilfe von EWS in Exchange](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)   
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)   
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

