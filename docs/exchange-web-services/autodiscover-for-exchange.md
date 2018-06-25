---
title: AutoErmittlung für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: da0f9402-4e35-42c7-a15e-1e9e4e966e8b
description: Erfahren Sie mehr über den AutoErmittlungsdienst in Exchange.
ms.openlocfilehash: f56717eaced5db9028c556c6c2d9aa7794f4988e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756845"
---
# <a name="autodiscover-for-exchange"></a>AutoErmittlung für Exchange

Erfahren Sie mehr über den AutoErmittlungsdienst in Exchange.
  
Der Exchange-AutoErmittlungsdienst bietet eine einfache Möglichkeit zur selbstständigen Konfiguration Ihrer Clientanwendung mit minimaler Benutzerinteraktion. Die meisten Benutzer kennen ihre E-Mail-Adresse und ihr Kennwort und diese beiden Angaben reichen aus, um alle anderen erforderlichen Informationen für den Einstieg abzurufen. Bei EWS-Clients (Exchange-Webdienste) wird AutoErmittlung normalerweise zum Suchen der EWS-Endpunkt-URL verwendet. Die AutoErmittlung kann ebenfalls Informationen zum Konfigurieren von Clients bereitstellen, die andere Protokolle verwenden. AutoErmittlung funktioniert für Clientanwendungen innerhalb und außerhalb von Firewalls sowie bei Topologien mit einer einzelnen oder mehreren Gesamtstrukturen.
  
## <a name="overview-of-the-autodiscover-process"></a>Übersicht über den Prozess der AutoErmittlung
<a name="bk_Before"> </a>

Der Prozess der AutoErmittlung besteht prinzipiell aus drei Phasen. In der ersten Phase generieren Sie eine Liste möglicher AutoErmittlungs-Server. In der zweiten Phase probieren Sie jeden Server auf der Liste aus und erhalten (hoffentlich) eine erfolgreiche Antwort. Sollte keiner der möglichen Server zum Erfolg führen, wird Phase drei initiiert. Dabei handelt es sich um das letzte Mittel zur Ermittlung eines AutoErmittlungs-Endpunkts.
  
Die [ExchangeService.AutodiscoverUrl](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx)-Methode der EWS Managed API implementiert alle drei Phasen dieses Prozesses für Sie. Sollten Sie also die EWS Managed API verwenden, müssen Sie sich nicht selbst um die Implementierung der AutoErmittlung kümmern. Die folgende Abbildung zeigt die drei Phasen des Prozesses der AutoErmittlung. 
  
**Abbildung 1. Die drei Phasen des Prozesses der AutoErmittlung**

![Illustration des AutoErmittlung-Prozesses mit drei Phasen: Definieren des Kandidatenpools, Ausprobieren der Endpunkte und Ausprobieren anderer Alternativen.](media/Ex15_Autodiscover_Overview.png)
  
### <a name="phase-1-defining-the-candidate-pool"></a>Phase 1: Festlegen der möglichen Kandidaten
<a name="bk_Phase1"> </a>

Bevor Sie die AutoErmittlung verwenden können, müssen Sie den richtigen Server für die AutoErmittlung für Ihren Benutzer suchen. Glücklicherweise definiert die AutoErmittlung eine Auswahl an Stellen für Sie, an denen Sie suchen können. Falls mehrere Kandidaten gefunden werden, kann die Liste auch [nach Priorität sortiert werden](how-to-generate-a-list-of-autodiscover-endpoints.md).
  
**Table 1: Quellen für die AutoErmittlung möglicher Endpunkte**

|**Informationsquelle**|**Was Sie dort finden**|
|:-----|:-----|
|Active Directory-Domänendienste (AD DS)  <br/> |Bei mit der Domäne verbundenen Clients sollten Sie zuerst hier suchen. Exchange veröffentlicht Objekte für Dienstverbindungspunkte (SCP) in AD DS, weshalb Anfragen der AutoErmittlung anhand von Active Directory-Standorten auf Server weitergeleitet werden können. Die Ergebnisse einer [SCP-Suche](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) sollte am Anfang Ihrer Kandidatenliste stehen.  <br/><br/>**Hinweis**: SCP-Suche nicht für Clients, die kein Mitglied einer Domäne oder, die keinen Zugriff auf Active Directory-Server, zur Verfügung. In diesem Fall sollten Sie die SCP-Suche überspringen. <br/>|
|Die Domäne der E-Mail-Adresse des Benutzers  <br/> | AutoErmittlung definiert zwei Standard-Endpunkt-URL-Formate, die aus dem Domänenteil der E-Mail-Adresse des Benutzers abgeleitet werden:  <br/>`"https://" + domain + "/autodiscover/autodiscover" +  *fileExtension*`  <br/>`"https://autodiscover." + domain + "/autodiscover/autodiscover" +  *fileExtension*`<br/><br/>  Der Wert für  *Dateierweiterung*  hängt von der Zugriffsemthode Sie für die AutoErmittlung verwenden: [SOAP](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx) oder [POX](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx). Der SOAP-Dienst verwendet die Dateierweiterung ".svc", POX ".xml".  <br/> |
   
Die folgende Abbildung zeigt, wie eine Liste der Endpunkte für die AutoErmittlung generiert wird.
  
**Abbildung 2. Prozess zum Generieren einer Liste der Endpunkte für die AutoErmittlung**

![Illustration des Prozesses zur Generierung einer Endpunktliste für die AutoErmittlung. Pfeile zeigen, dass die Liste der Endpunkte von der SCP-Suche oder der E-Mail-Adresse des Benutzers abgeleitet wurde.](media/Ex15_Autodiscover_Overview_Phase1.png)
  
### <a name="phase-2-trying-each-candidate"></a>Phase 2: Alle Kandidaten ausprobieren
<a name="bk_Phase2"> </a>

Nachdem Sie eine sortierte Liste der potenziellen Kandidaten generiert haben, wird im nächsten Schritt jeder Eintrag aus der Liste durch [Senden einer Anforderung an die URL](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) ausprobiert. Anschließend werden die Ergebnisse wie in Abbildung 3 dargestellt überprüft. Wenn Sie eine erfolgreiche Antwort erhalten, sind Sie fertig! 
  
**Abbildung 3. Ausprobieren der möglichen Endpunkte nacheinander**

![Eine Illustration, die zeigt, wie der Server jeden Endpunkt in Prioritätsreihenfolge ausprobiert, bis er eine erfolgreiche Antwort erhält.](media/Ex15_Autodiscover_Overview_Phase2.png)
  
Bevor Sie eine Anforderung an einen Kandidaten senden, sollten Sie sicherstellen, dass er vertrauenswürdig ist. Denken Sie daran, dass Sie bei diesem Vorgang die Anmeldeinformationen des Benutzers übermitteln. Daher ist es wichtig, diese Daten nur mit vertrauenswürdigen Servern zu teilen. Sie sollten mindestens die folgenden Punkte überprüfen:
  
- Dass es sich bei dem Endpunkt um einen HTTPS-Endpunkt handelt. Clientanwendungen sollten sich nicht bei Endpunkten ohne SSL anmelden oder dorthin Daten übermitteln.
    
- Dass das SSL-Zertifikat gültig ist und aus einer vertrauenswürdigen Quelle stammt.
    
> [!NOTE]
> [!HINWEIS] Hierbei handelt es sich nur um Vorschläge zur grundlegenden Sicherheit. Wenn Sie mit Authentifizierung arbeiten, stellen Sie sicher, dass Ihr Code die Sicherheitsanforderungen Ihrer Organisation erfüllt. 
  
DIe Art der Anforderung, die Sie senden, hängt davon ab, wie Sie auf den AutoErmittlungsdienst zugreifen.
  
**Tabelle 2. Arten von Anfragen der AutoErmittlung**

|**Bei Verwendung von...**|**Senden Sie eine Anforderung mit...**|
|:-----|:-----|
|EWS Managed API  <br/> |der [GetUserSettings](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx)-Methode.  <br/> |
|SOAP-AutoErmittlungsdienst  <br/> |dem [GetUserSettings](http://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx)-Vorgang.  <br/> |
|POX-AutoErmittlungsdienst  <br/> |HTTP POST mit einem [AutoErmittlung-Anforderungstext](http://msdn.microsoft.com/library/75671b1d-f35b-497b-8d8c-706f3f2535fd%28Office.15%29.aspx).  <br/> |
   
### <a name="phase-3-trying-other-alternatives"></a>Phase 3: Ausprobieren anderer Alternativen
<a name="bk_Phase3"> </a>

In einigen Fällen kann es vorkommen, dass Sie alle Endpunkte ausprobieren, ohne einen passenden zu finden. Bevor Sie aufgeben, können Sie andere Alternativen ausprobieren: Sie können eine nicht authentifizierte GET-Anforderung senden oder einen SRV-Eintrag vom DNS abfragen. Sollten diese Versuche auch ergebnislos sein, können Sie den AutoErmittlungsdienst nicht kontaktieren.
  
**Abbildung 4. Ausprobieren anderer Alternativen**

![Eine Illustration zusätzlicher Endpunkte, die über eine nicht authentifizierte GET-Anforderung und eine DNS-Anfrage generiert wurden.](media/Ex15_Autodiscover_Overview_Phase3.png)
  
#### <a name="sending-an-unauthenticated-get-request"></a>Senden einer nicht authentifizierten GET-Anforderung

Zunächst sollten Sie versuchen, eine nicht authentifizierte GET-Anforderung an einen Endpunkt zu senden, der aus der E-Mail-Adresse des Benutzers abgeleitet wird. Das Format dieses Endpunkts ist "http://autodiscover." + Domäne + "/autodiscover/autodiscover.xml". Beachten Sie, dass es sich dabei nicht um einen SSL-Endpunkt handelt. Wenn der Server eine 302-Weiterleitung als Antwort zurückgibt, können Sie das [Erneute Senden der Anforderung des AutoErmittlungsdiensts](handling-autodiscover-error-messages.md#bk_ResendRequest) an die Endpunkt-URL im Location-Header der Antwort probieren. 
  
#### <a name="querying-dns-for-an-srv-record"></a>Abfragen eines SRV-Eintrags beim DNS

Sollte die nicht authentifizierte GET-Anforderung keine Ergebnisse hervorbringen, ist die letzte Möglichkeit eine DNS-Abfrage von SRV-Einträgen für den AutoErmittlungsdienst. Ein solcher Eintrag hat die Form "_autodiscover._tcp." + Domäne. Bei einer solchen Abfrage werden möglicherweise mehrere Einträge zurückgegeben, Sie sollten allerdings nur Einträge verwenden, die auf einen SSL-Endpunkt zeigen und die höchste Priorität und Gewichtung haben.
  
## <a name="options-for-using-autodiscover"></a>Optionen für die Verwendung von AutoErmittlung
<a name="bk_Options"> </a>

Sie können entweder mithilfe des SOAP- oder des POX-Webdiensts auf die AutoErmittlung zugreifen. Die Methode, die Sie verwenden, hängt von Ihren Anforderungen und der Umgebung ab. Wir empfehlen jedoch den SOAP-Webdienst, falls möglich. Die EWS Managed API ist auch eine Option. Die API implementiert den Clientbereich für die AutoErmittlungsdienste über POX und SOAP implementiert.
  
**Tabelle 3: Optionen für den Zugriff auf die AutoErmittlung**

|**Option**|**Vorteile**|**Nachteile**|
|:-----|:-----|:-----|
|[EWS Managed API](get-started-with-ews-managed-api-client-applications.md) <br/> | Implementiert die AutoErmittlung für Sie.<br/><br/>Verwendet die AutoErmittlungsdienste über POX und SOAP.<br/><br/>Funktioniert mit Exchange Online, Exchange Online in Office 365 oder einer anderen Version von Exchange ab Exchange 2007 SP1.<br/><br/>Einfach zu verwenden.  <br/> | Beschränkt auf die verfügbaren Benutzereinstellungen in der [Microsoft.Exchange.WebServices.Autodiscover.UserSettingName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=EXCHG.80%29.aspx)-Enumeration.<br/><br/>Nur für .NET Framework-Anwendungen verfügbar.  <br/> |
|[SOAP-AutoErmittlung](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx) <br/> | Plattformunabhängig.<br/><br/>Ermöglicht Ihnen, nur die Einstellungen anzufordern, die Sie benötigen.  <br/> | Nicht in Exchange 2007 verfügbar.  <br/> |
|[POX-AutoErmittlung](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx) <br/> | Plattformunabhängig.<br/><br/>Wird in Exchange Online und allen Versionen von Exchange ab Exchange 2007 SP1 unterstützt.  <br/> | Bestimmte Einstellungen können nicht angefordert werden.  <br/> |
   
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Suchen Sie nach AutoErmittlung-Endpunkten mithilfe von SCP-Suche in Exchange](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [Generieren Sie eine Liste von Endpunkten für die AutoErmittlung](how-to-generate-a-list-of-autodiscover-endpoints.md)
    
- [Mithilfe von AutoErmittlung Verbindungspunkte suchen](how-to-use-autodiscover-to-find-connection-points.md)
    
- [Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [Abrufen von domäneneinstellungen aus einem Exchange-server](how-to-get-domain-settings-from-an-exchange-server.md)
    
- [Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)
    
- [Verbessern der Leistung bei Verwendung der AutoErmittlung für Exchange](improving-performance-when-using-autodiscover-for-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)    
- [Exchange 2013: Abrufen von Benutzereinstellungen mit der AutoErmittlung](http://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e)
- [Beispiel für die AutoErmittlung-Prüfung](http://code.msdn.microsoft.com/exchange/Autodiscover-Checker-e1ebca42)  
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

