---
title: Erste Schritte mit Webdiensten in Exchange
manager: sethgros
ms.date: 2/27/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b07a92-0595-4bf1-bd6b-c07e66a8c923
description: Suchen Sie nach Informationen für Ihre ersten Schritte mit EWS und anderen Webdiensten in Exchange.
ms.openlocfilehash: 2f203c5634c29105feb39220c3ebdd9624bb49ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757127"
---
# <a name="start-using-web-services-in-exchange"></a>Erste Schritte mit Webdiensten in Exchange

Suchen Sie nach Informationen für Ihre ersten Schritte mit EWS und anderen Webdiensten in Exchange.
  
Die [Webdienste in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) ermöglichen Zugriff auf Postfachdaten, die in Exchange Online, Exchange Online als Teil von Office 365 und lokalen Versionen von Exchange ab Exchange Server 2007 gespeichert sind. Mithilfe der Webdienste können Sie benutzerdefinierte Anwendungen erstellen, die Sie zum Verwalten dieser Informationen gemäß den Anforderungen Ihrer Organisation verwenden können. Der Umfang von EWS und Webdienstanwendungen ist zwar praktisch unendlich, für alle Typen von Anwendungen gelten jedoch bestimmte grundlegende Konzepte. Dieser Abschnitt enthält Informationen zu den Grundbegriffen, mit denen Sie vertraut sein müssen, um mit der Verwendung von EWS und anderen Webdiensten in Exchange beginnen zu können. 
  
## <a name="build-your-knowledge"></a>Ihre Kenntnisse erweitern
<a name="bk_Knowledge"> </a>

Unabhängig davon, ob Sie .NET Framework oder eine andere Plattform für die Entwicklung von Webdienstanwendungen verwenden, sollten Sie einige wichtige Konzepte verstehen, bevor Sie Ihr Entwicklungsprojekt beginnen. 
  
**Tabellle 1: Webdienstkonzepte**

|**Konzept**|**Zusammenfassung**|
|:-----|:-----|
|[Architektur](ews-applications-and-the-exchange-architecture.md) <br/> |Erfahren Sie mehr über die Funktionsweise von EWS und die von EWS verwendeten Protokolle.  <br/> |
|[EWS-Anwendungstypen](ews-application-types.md) <br/> |Informieren Sie sich über die am häufigsten verwendeten Arten von Anwendungen, die Sie mithilfe von EWS in Exchange erstellen können.  <br/> |
|[EWS-Zugriff](controlling-client-application-access-to-ews-in-exchange.md) <br/> |Exchange-Administratoren können den Zugriff auf EWS global für die gesamte Organisation, für einzelne Benutzer und für einzelne Anwendungen einschränken. Erfahren Sie, welche Zugriffsebene für Sie geeignet ist.  <br/> |
|[Einrichtung](setting-up-your-ews-application.md) <br/> |Finden Sie Informationen zu den Aufgaben, die Sie erledigen müssen, um Anwendungen zu erstellen, die die verwaltete EWS-API oder EWS verwenden, um mit Exchange zu kommunizieren.  <br/> |
|[Authentifizierung](authentication-and-ews-in-exchange.md) <br/> |Erfahren Sie mehr über die Authentifizierungsoptionen für die Herstellung einer Verbindung mit Exchange Online und lokalen Bereitstellungen von Exchange.  <br/> |
|[AutoErmittlung](autodiscover-for-exchange.md) <br/> |Erfahren Sie mehr über die Sammlung von Diensten, mit denen Sie den URL-Endpunkt ermitteln können, an dem das Konto eines Benutzers über EWS auf Informationen zugreifen kann.  <br/> |
|[Postfachserver](http://technet.microsoft.com/de-DE/library/jj150491%28v=exchg.150%29.aspx) <br/> |Erfahren Sie mehr über das primäre Informationsrepository, das einem EWS-Client zur Verfügung gestellt wird. EWS hat Zugriff auf eine beschränkte Sammlung von Informationen, die in Active Directory-Domänendiensten (AD DS) gespeichert sind.  <br/> |
|[Mail-Apps für Outlook und EWS](mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |In diesem Artikel finden Sie Informationen über Mail-Apps für Outlook und ihre Zusammenarbeit mit EWS in Exchange.  <br/> |
|[Office 365-REST-APIs für E-Mail, Kalender und Kontakte](office-365-rest-apis-for-mail-calendars-and-contacts.md) <br/> |Erfahren Sie mehr über die Office 365-APIs, die Sie verwenden können, um auf E-Mails, Kalender und Kontakte in Exchange Online als Teil von Office 365 zuzugreifen.  <br/> |
|[Die verwaltete EWS-API](get-started-with-ews-managed-api-client-applications.md) <br/> |Informieren Sie sich über die bevorzugte Client-API für .NET Framework-Entwickler.  <br/> |
|[EWS](get-started-with-ews-client-applications.md) <br/> |Informieren Sie sich über das Erstellen Ihrer ersten Anwendung mithilfe von EWS-XML-Anforderungen und -Antworten.  <br/> |
|[EWS-Funktionalität in Exchange-Produktversionen](ews-functionality-in-exchange-product-versions.md) <br/> |Erfahren Sie, welche EWS-Funktionen in Versionen von Exchange verfügbar sind.  <br/> |
|[Ablaufverfolgung und Problembehandlung](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) <br/> |Erfahren Sie, wie Sie EWS-Anforderungen und -Antworten nachverfolgen, um die Probleme mit Fehlern in Ihrer verwalteten EWS-API-Anwendung zu behandeln.  <br/> |
   
## <a name="create-your-first-application"></a>Erstellen Ihrer ersten Anwendung
<a name="create"> </a>

Wenn Sie bereit sind, Ihre erste .NET Framework- oder EWS-Clientanwendung zu entwickeln, finden Sie weitere Informationen unter [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](get-started-with-ews-managed-api-client-applications.md) oder [Erste Schritte mit EWS-Clientanwendungen](get-started-with-ews-client-applications.md).
  
## <a name="get-code-samples"></a>Abrufen von Codebeispielen
<a name="samples"> </a>

Codebeispiele und Beispiele, die zeigen, wie Sie mit EWS und anderen Webdiensten in Exchange arbeiten, finden Sie in den folgenden Ressourcen:
  
- [Exchange-Codebeispiele](http://code.msdn.microsoft.com/exchange)
    
- [CodePlex](http://www.codeplex.com/)
    
- [Dokumentation zur Exchange-API](develop-web-service-clients-for-exchange.md)
    
- [Forum zur Exchange-Entwicklung](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment)
    
Viele andere Beispiele sind in Blogs, auf Codedemowebsites und in Foren verfügbar. Wir empfehlen außerdem, den [EWSEditor](http://ewseditor.codeplex.com/) herunterzuladen. Dieses Projekt implementiert den größten Teil der EWS-Funktionen, und Sie finden hier Beispiele für alle EWS-Kernfunktionen.
  
Wenn Sie kein .NET Framework-Entwickler sind, stehen zahlreiche Clientbibliotheken für die EWS-Entwicklung zur Verfügung, die Java, Python, PHP und andere Sprachen verwenden. 
  
## <a name="ask-questions-and-solve-problems"></a>Fragen stellen und Probleme lösen
<a name="questions"> </a>

Sie benötigen Hilfe bei Ihren Aufgaben und finden keine Antworten? Durchsuchen Sie das [Exchange-Entwicklungsforum](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment), um herauszufinden, ob jemand anders auch dasselbe Problem hatte und dieses gelöst hat. Eine Community von Mitwirkenden hat Hunderte von Fragen zur Exchange-Entwicklung beantwortet. Sie finden außerdem Websites, Foren und Blogs von Drittanbietern, die Informationen zur Exchange-Entwicklung und möglicherweise die Lösung bereitstellen, nach der Sie suchen. 
  
Wenden Sie sich an den [Microsoft-Support](https://support.microsoft.com/), wenn Sie weitere Unterstützung benötigen. Das Exchange Developer-Supportteam ist mit erfahrenen Profis besetzt, die Ihre Fragen zur Exchange-Entwicklung beantworten können. 
  
## <a name="see-also"></a>Siehe auch

- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md) 
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md) 
- [Referenz für Webdienste für Exchange](../web-service-reference/web-services-reference-for-exchange.md)
    

