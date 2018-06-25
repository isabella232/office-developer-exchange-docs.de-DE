---
title: Einrichten der Entwicklungsumgebung für Exchange-Anwendung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 91b86e93-bdde-41c3-9680-45cf61420592
description: Erhalten Sie Informationen zum Einrichten Ihrer Entwicklungsumgebung zum Erstellen einer EWS-Anwendung, die kommuniziert mit Exchange.
ms.openlocfilehash: 0c7d4c6d37b28b6797bdb638930b8582f31ffc5e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757125"
---
# <a name="setting-up-your-exchange-application-development-environment"></a>Einrichten der Entwicklungsumgebung für Exchange-Anwendung

Erhalten Sie Informationen zum Einrichten Ihrer Entwicklungsumgebung zum Erstellen einer EWS-Anwendung, die kommuniziert mit Exchange.
  
Bevor Sie beginnen, Ihre Exchange-Webdienste (EWS) Anwendung schreiben, müssen Sie sicherstellen, dass die Entwicklungsumgebung einige Mindestanforderungen erfüllt. Sie können die EWS Managed API, die standard-Client Access API für .NET Framework-Clientanwendungen für die Anwendungsentwicklung, oder Verwenden von EWS eigenständig, mit unseren ohne eine automatisch generierte Proxy. Im Allgemeinen empfehlen wir, dass Sie die EWS Managed API verwenden; Sie können jedoch [erkunden den Unterschied zwischen diesen beiden Optionen](ews-client-design-overview-for-exchange.md) ausführlich zu suchen, die welche einer für Sie geeignet ist. 
  
> [!NOTE]
>  [!HINWEIS]  Die EWS Managed API ist jetzt als Open Source-Projekt auf [GitHub](https://github.com/officedev/ews-managed-api) verfügbar. Sie können die Open Source-Bibliothek für Folgendes verwenden: >  Implementieren von Programmfehlerbehebungen und Verbesserungen der API >  Abrufen von Fehlerbehebungen und Verbesserungen, bevor diese in einer offiziellen Version verfügbar sind >  Zugreifen auf die umfassendste und aktuellste Implementierung der API, um sie als Referenz zu verwenden oder neue Bibliotheken auf neuen Plattformen zu erstellen >  Wir freuen uns auf Ihre [Beiträge](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) über GitHub. 
  
## <a name="development-environment-for-the-ews-managed-api"></a>Entwicklungsumgebung für die EWS Managed API
<a name="bk_EWSMA"> </a>

Um eine EWS Managed API-Anwendung zu erstellen, benötigen Sie Zugriff auf die folgenden:
  
- Die [verwaltete EWS-API](http://aka.ms/ews-managed-api-readme). 
    
    Sie können die EWS Managed API-Dateien an einer beliebigen Stelle auf Ihrem Computer speichern. in der Standardeinstellung, die sie in der Anwendung Files\Microsoft\Exchange\Web Dienste installiert sind\\< Versionsnummer\> Ordner.
    
- Ein Postfach auf einem Exchange-Server, der Exchange Online, Exchange Online als Teil von Office 365 oder eine Version von Exchange ausgeführt wird, beginnend mit Exchange Server 2007. 
    
    Sie können einen Exchange Online-Plan für Unternehmen, einschließlich eine kostenlose Testversion, von der [Office 365-Website](http://office.microsoft.com/en-us/business/compare-office-365-for-business-plans-FX102918419.aspx#fbid=1tsGNIE7e3a)abrufen. Um mit dem Postfach verbinden zu können, müssen Sie den Benutzernamen und die Anmeldeinformationen des Kontos, das dem Postfach zugeordnete verfügen.
    
- Eine Version von Visual Studio beginnend mit Visual Studio 2005. Wenn Sie derzeit nicht über Visual Studio verfügen, können Sie eine kostenlose Version von [Visual Studio 2010 Express](http://www.microsoft.com/visualstudio/eng/products/visual-studio-2010-express)herunterladen.
    
- Eine Version von .NET Framework beginnend mit .NET Framework 3.5. Sie können die .NET Framework 3.5 aus dem [Microsoft Download Center](http://go.microsoft.com/fwlink/?LinkId=191777)herunterladen.
    
Darüber hinaus ist es hilfreich, wenn Sie mit c# vertraut sind. Visual Studio andere Sprachen neben c# unterstützt, zwar werden die meisten der im Beispielcode für die EWS Managed API verfügbar in c# geschriebenen.
  
## <a name="development-environment-for-ews"></a>Entwicklungsumgebung für EWS
<a name="bk_EWS"> </a>

EWS können Sie um Ihre Anwendung in einigen auf verschiedene Weise zu entwickeln. Die einfachste Möglichkeit zum Verwenden der Exchange-Webdienste ist Textdateien, in denen Ihre XML-Anforderungen erstellen und zu Exchange zu senden. Zu diesem Zweck sieht, was Sie benötigen: 
  
- Einen einfachen Text-Editor wie Notepad ein, zum Bearbeiten Ihrer XML-Anforderung. Einem beliebigen Texteditor wird tun, obwohl sollten Sie die eine, die mit Ihrer XML-Syntax Überprüfung wie XMetal helfen.
    
- Ein Tool oder eine Anwendung, die senden und Empfangen von SOAP-XML-Anforderungen und Antworten, um die Kommunikation mit Exchange kann.
    
Beim Arbeiten mit XML-Rohdaten, ist es auch hilfreich, grundlegend XML-Formatierung haben.
  
Die zweite Möglichkeit zum Verwenden der Exchange-Webdienste ist die Erstellung ein automatisch generierten Proxys, mit das Sie die Vorgänge unter Verwendung einer .NET Sprache wie c# entwickelt werden können. Hier ist, was Sie benötigen einen Proxy automatisch generierten entwickelt:
  
- Eine Version von Visual Studio beginnend mit Visual Studio 2005, um einen Proxyverweis zu erstellen. Sie können eine kostenlose Version von [Visual Studio 2010 Express](http://www.microsoft.com/visualstudio/eng/products/visual-studio-2010-express)herunterladen.
    
- Eine Version von .NET Framework beginnend mit .NET Framework 2.0. Sie können die .NET Framework 3.5 aus dem [Microsoft Download Center](http://go.microsoft.com/fwlink/?LinkId=191777)herunterladen.
    
Wenn Sie einen automatisch generierte Proxy verwenden, sollten Sie mit C#-Programmierung vertraut sind.
  
> [!NOTE]
> Wenn Sie .NET Framework-Entwickler sind, empfehlen wir Ihnen, die EWS Managed API und nicht automatisch generierten Proxys verwenden, um EWS zu entwickeln. Das EWS Managed API-Objektmodell ist einfacher zu verwenden als automatisch generierten Proxy-Objektmodellen. Darüber hinaus die EWS Managed API [AutoErmittlung](autodiscover-for-exchange.md) implementiert und clientseitige Logik enthält. 
  
## <a name="see-also"></a>Siehe auch


- [Einrichten der Entwicklungsumgebung für Exchange-Anwendung](setting-up-your-exchange-application-development-environment.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    
- [Steuern des Zugriffs auf EWS in Exchange](how-to-control-access-to-ews-in-exchange.md)
    
- [EWS-Objektmodellen für Exchange generiert.](https://msdn.microsoft.com/en-us/library/jj190899)
    

