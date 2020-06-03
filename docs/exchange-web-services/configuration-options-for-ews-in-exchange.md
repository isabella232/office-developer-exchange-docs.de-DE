---
title: Konfigurationsoptionen für EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6562639-9366-4a13-9fdb-2fa737833329
description: Hier finden Sie Informationen zu Konfigurationseinstellungen, auf die ihr EWS-Client zugreifen kann, und die konfigurierbaren Exchange-Einstellungen, die sich auf Ihren EWS-Client auswirken können.
ms.openlocfilehash: 55f927b7b301bdfaa298bcd254b18a00cf1692d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456157"
---
# <a name="configuration-options-for-ews-in-exchange"></a>Konfigurationsoptionen für EWS in Exchange

Hier finden Sie Informationen zu Konfigurationseinstellungen, auf die ihr EWS-Client zugreifen kann, und die konfigurierbaren Exchange-Einstellungen, die sich auf Ihren EWS-Client auswirken können. 
  
Viele Konfigurationseinstellungen können sich auf die Funktionen Ihrer EWS-Clientanwendung auswirken. Diese Konfigurationseinstellungen sind entweder: 
  
- Schreibgeschützt oder Lese-/Schreibzugriff vom Client.
    
- Zugriff auf den Exchange-Server, auf dem der EWS-Dienst gehostet wird.
    
Ein Client kann auf Einstellungen auf Exchange Online, Exchange Online im Rahmen von Office 365 und auf einem lokalen Exchange-Server zugreifen. Alle lokalen Exchange Server-Einstellungen stehen Exchange-Administratoren zur Verfügung. Allerdings stehen nicht alle diese Einstellungen für Exchange Online mandantenadministratoren zur Verfügung. In diesem Artikel wird beschrieben, auf welche Konfigurationseinstellungen Clients, Exchange Server Administratoren und Exchange Online mandantenadministratoren zugreifen können.
  
## <a name="configuration-settings-that-clients-can-access"></a>Konfigurationseinstellungen, auf die Clients zugreifen können

Ihre Clientanwendung kann eine Reihe von Konfigurationsoptionen vom Exchange-Server abrufen und festlegen. Die Konfigurationseinstellungen, die alle EWS-Anwendungen benötigen, werden vom AutoErmittlungsdienst bereitgestellt. Andere Konfigurationseinstellungen werden für bestimmte Anwendungsszenarien verwendet. 
  
**Tabelle 1. Webdienstfeatures, die Konfigurationsoptionen für EWS-Clients bereitstellen**

|**Feature**|**Beschreibung**|
|:-----|:-----|
|AutoErmittlungsdienst  <br/> |Der [AutoErmittlungsdienst](autodiscover-for-exchange.md) stellt ihren Clientanwendungen Konfigurationsinformationen zur Verfügung, damit der Client sich automatisch für die Kommunikation mit EWS konfigurieren kann.  <br/> |
|In einem Postfach gespeicherte benutzerdefinierte Konfigurationsinformationen  <br/> |Sie können eine von mehreren Optionen verwenden, um [benutzerdefinierte Konfigurationsinformationen](persistent-application-settings-in-ews-in-exchange.md) in Ihrem Postfach zu speichern: Benutzer Konfigurationsobjekte, benutzerdefinierte Elemente oder erweiterte Eigenschaften.  <br/> |
|Delegieren der Verwaltung  <br/> | EWS stellt CRUD-Vorgänge für die Verwaltung des Stellvertreter Zugriffs auf ein Postfach bereit. Stellvertretungen sind Benutzer, denen die Berechtigung für den Zugriff auf das Postfach eines anderen Benutzers erteilt wurde.<br/><br/>  Sie können die Delegate- [Verwaltungsvorgänge](https://msdn.microsoft.com/library/bb409286%28v=exchg.150%29.aspx#bk_delegate_management) verwenden, um die Stellvertretungs Verwaltung mithilfe von EWS zu aktivieren, oder wenn Sie die verwaltete EWS-API verwenden, können Sie die folgenden Methoden verwenden:<br/><br/>- [Datei "ExchangeService. adddelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/>- [Datei "ExchangeService. getdelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getdelegates%28v=exchg.80%29.aspx) <br/>- [Datei "ExchangeService. UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) <br/>- [Datei "ExchangeService. RemoveDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |
|eDiscovery-Suchkonfiguration  <br/> |eDiscovery-Clientanwendungen können [Such Konfigurationsinformationen](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) abrufen, die eine eDiscovery-Suchabfrage, eine Liste mit durchsuchbaren Postfächern und den Bezeichner des in-Place-Postfachs enthält.  <br/> |
|Ordnerberechtigungen  <br/> |Ordnerberechtigungen begrenzen, was ein Benutzer in einem öffentlichen Ordner ausführen kann, und im Fall von Stellvertretungs Zugriffen, was eine Stellvertretung im Ordner eines anderen Benutzers ausführen kann. Sie können entweder die [Folder. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) -Methode oder den [GetFolder-Vorgang](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) verwenden, um auf den Berechtigungssätzen aller Ordner zuzugreifen, einschließlich öffentlicher Ordner, freigegebener privater Ordner oder Ordner, für die Benutzer über Stellvertretungszugriff verfügen.  <br/> |
|E-Mail-Tipps, Unified Messaging oder Schutzregeln  <br/> |Der [GetServiceConfiguration-Vorgang](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) stellt schreibgeschützte [Dienstkonfigurationsinformationen](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) für Mail-Tipps, Unified Messaging und Schutzregeln bereit.  <br/> |
   
## <a name="configuration-settings-that-administrators-can-access-on-the-exchange-server"></a>Konfigurationseinstellungen, auf die Administratoren auf dem Exchange-Server zugreifen können

Für die meisten Client Anwendungsszenarien sind keine Änderungen an den Serverkonfigurationseinstellungen erforderlich. Einige Szenarien werden jedoch durchführen. Wenn Sie beispielsweise eine Middle-Tier-Anwendung als Benutzer aktivieren möchten, müssen Sie den Exchange-Identitätswechsel auf dem Server festlegen. Beachten Sie, dass auf einige Einstellungen nur auf lokalen Exchange-Servern zugegriffen werden kann. Wenn Sie Exchange Online ausrichten, muss Ihre Clientanwendung möglicherweise mit den Standardeinstellungen arbeiten.
  
**Tabelle 2. Exchange Server-Konfigurationsoptionen, die EWS-Clients betreffen**

|**Feature**|**Auf Exchange Online zugänglich?**|**Weitere Informationen finden Sie unter...**|
|:-----|:-----|:-----|
|Einstellungen für das virtuelle Verzeichnis (einschließlich Authentifizierung)  <br/> |Nein  <br/> |[Get-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa998810%28v=exchg.150%29.aspx) <br/> [Set-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx) <br/> |
|AutoErmittlung  <br/> |Nein  <br/> |[Get-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa996819%28v=exchg.150%29.aspx) <br/> [Gruppe-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa998601%28v=exchg.150%29.aspx) <br/> |
|Compliance  <br/> |Ja  <br/> |[Archivierung](https://technet.microsoft.com/library/dd979800%28v=exchg.150%29.aspx) <br/> [eDiscovery](https://technet.microsoft.com/library/dd298021%28v=exchg.150%29.aspx) <br/> [Anhalten der Aufbewahrungszeit](https://technet.microsoft.com/library/dd335168%28v=exchg.150%29.aspx) <br/> [Verhinderung von Datenverlust](https://technet.microsoft.com/library/jj150527%28v=exchg.150%29.aspx) <br/> |
|Delegieren der Verwaltung  <br/> |Ja  <br/> |[Manage Permissions for Recipients](https://technet.microsoft.com/library/jj919240%28v=exchg.150%29.aspx) <br/> |
|Exchange-Identitätswechsel  <br/> |Ja  <br/> |[Konfigurieren des Exchange-Identitätswechsels](https://msdn.microsoft.com/library/bb204095%28EXCHG.140%29.aspx) <br/> |
|E-Mail-Tipps, Unified Messaging oder Schutzregeln  <br/> |Ja  <br/> |[E-Mail-Info](https://technet.microsoft.com/library/jj649091%28v=exchg.150%29.aspx) <br/> [Unified Messaging-Cmdlets](https://technet.microsoft.com/library/aa997665%28v=exchg.150%29.aspx) <br/> [Outlook-Schutzregeln](https://technet.microsoft.com/library/dd638178%28v=exchg.150%29.aspx) <br/> |
|Einschränkung  <br/> |Nein  <br/> |[Einschränkungseinstellungen](ews-throttling-in-exchange.md) <br/> |
|Benutzer-Agent-Filterung  <br/> |Ja  <br/> |[Benutzer-Agent-Filterung](how-to-control-access-to-ews-in-exchange.md) <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Abrufen von Dienstkonfigurationsinformationen mithilfe von EWS in Exchange](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)   
- [Verwenden von Webdiensten in Exchange](start-using-web-services-in-exchange.md)   
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

