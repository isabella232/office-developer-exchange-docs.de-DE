---
title: Einrichten der Entwicklungsumgebung für Exchange-Anwendung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 91b86e93-bdde-41c3-9680-45cf61420592
description: Erfahren Sie, wie Sie Ihre Entwicklungsumgebung einrichten, um eine EWS-Anwendung zu erstellen, die mit Exchange kommuniziert.
localization_priority: Priority
ms.openlocfilehash: 01a106817f29bd696991b8a0c5d7d9b7dd420b94
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463762"
---
# <a name="setting-up-your-exchange-application-development-environment"></a>Einrichten der Entwicklungsumgebung für Exchange-Anwendung

Erfahren Sie, wie Sie Ihre Entwicklungsumgebung einrichten, um eine EWS-Anwendung zu erstellen, die mit Exchange kommuniziert.
  
Bevor Sie mit dem Schreiben Ihrer Exchange-Webdienste-Anwendung beginnen, müssen Sie sicherstellen, dass Ihre Entwicklungsumgebung einige Mindestanforderungen erfüllt. Sie können die verwaltete EWS-API, die standardmäßige Clientzugriffs-API für .NET Framework-Anwendungen verwenden, um Ihre Anwendung zu entwickeln, oder Sie können EWS selbst verwenden, ohne einen automatisch generierten Proxy. Im Allgemeinen wird empfohlen, die verwaltete EWS-API zu verwenden; Sie können [den Unterschied zwischen diesen beiden Optionen](ews-client-design-overview-for-exchange.md) jedoch genauer untersuchen, um herauszufinden, welche für Sie geeignet ist. 
  
> [!NOTE]
> Die verwaltete EWS-API steht nun als Open Source-Projekt auf [GitHub](https://github.com/officedev/ews-managed-api) zur Verfügung. Sie können die Open Source-Bibliothek für Folgendes verwenden: 
> - Implementieren von Programmfehlerbehebungen und Verbesserungen in die API 
> - Abrufen von Fehlerbehebungen und Verbesserungen, bevor diese in einer offiziellen Version verfügbar sind 
> - Zugreifen auf die umfassendste und aktuellste Implementierung der API, um sie als Referenz zu verwenden oder neue Bibliotheken auf neuen Plattformen zu erstellen
> 
>  Wir freuen uns über Ihre [Beiträge](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) über GitHub. 
  
## <a name="development-environment-for-the-ews-managed-api"></a>Entwicklungsumgebung für die verwaltete EWS-API
<a name="bk_EWSMA"> </a>

Um eine verwaltete EWS-API Anwendung zu erstellen, benötigen Sie Zugriff auf Folgendes:
  
- Die [verwaltete EWS-API](https://aka.ms/ews-managed-api-readme). 
    
    Sie können die verwaltete EWS-API Dateien an einer beliebigen Stelle auf Ihrem Computer speichern; Standardmäßig werden Sie im Ordner "Program Files\Microsoft\Exchange\Web Services \\<Versionsnummer \> " installiert.
    
- Ein Postfach auf einem Exchange-Server, auf dem Exchange Online, Exchange Online als Teil Office 365 oder eine Version von Exchange, die mit Exchange Server 2007 beginnt, ausführt wird. 
    
    Sie können einen Exchange Online-Plan für Unternehmen, einschließlich einer kostenlosen Testversion, von der [Office 365-Website](https://office.microsoft.com/business/compare-office-365-for-business-plans-FX102918419.aspx#fbid=1tsGNIE7e3a)abrufen. Um eine Verbindung mit dem Postfach herzustellen, benötigen Sie den Benutzernamen und die Anmeldeinformationen des Kontos, das dem Postfach zugeordnet ist.

    
- Eine Version von Visual Studio, beginnend mit Visual Studio 2005. Wenn Sie derzeit keine Visual Studio haben, können Sie eine [﻿Kostenlose Version](https://visualstudio.microsoft.com/)herunterladen.
    
- Eine Version des .NET Framework, beginnend mit dem Microsoft .NET Framework 3.5. Sie können das Microsoft .NET Framework 3.5 aus dem [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=191777)herunterladen.
    
Darüber hinaus ist es hilfreich, wenn Sie mit C# vertraut sind. Obwohl Visual Studio neben c# auch andere Sprachen unterstützt, wird der Großteil des für das verwaltete EWS-API verfügbaren Beispielcodes in c# geschrieben.
  
## <a name="development-environment-for-ews"></a>Entwicklungsumgebung für EWS
<a name="bk_EWS"> </a>

Sie können EWS verwenden, um Ihre Anwendung auf eine Reihe von verschiedenen Arten zu entwickeln. Die einfachste Möglichkeit zum Verwenden von EWS besteht darin, Textdateien zu erstellen, die Ihre XML-Anforderungen enthalten, und diese an Exchange weiterzuleiten. Dafür benötigen Sie Folgendes: 
  
- Ein einfacher Text-Editor wie Notepad zum Bearbeiten Ihrer XML-Anforderung. Jeder Text-Editor wird durchführen, obwohl Sie möglicherweise eine verwenden möchten, die Ihnen bei der XML-Syntaxüberprüfung wie XMetaL helfen kann.
    
- Ein Tool oder eine Anwendung, mit der SOAP-XML-Anforderungen und-Antworten gesendet und empfangen werden können, um mit Exchange zu kommunizieren.
    
Wenn Sie mit RAW XML arbeiten, ist es auch hilfreich, ein grundlegendes Verständnis der XML-Formatierung zu haben.
  
Die zweite Möglichkeit zum Verwenden von EWS besteht darin, einen automatisch generierten Proxy zu erstellen, mit dem Sie mit den Vorgängen arbeiten können, indem Sie eine .NET-Sprache wie C# verwenden. Hier sehen Sie, was Sie mit einem automatisch generierten Proxy zusammenarbeiten müssen:
  
- Eine Version von Visual Studio, beginnend mit Visual Studio 2005, um einen Proxy Verweis zu erstellen. Sie können eine [﻿Kostenlose Version](https://visualstudio.microsoft.com/)herunterladen.
    
- Eine Version des .NET Framework beginnend mit dem .NET Framework 2,0. Sie können das Microsoft .NET Framework 3.5 aus dem [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=191777)herunterladen.
    
Wenn Sie einen automatisch generierten Proxy verwenden, sollten Sie sich mit der C#-Programmierung vertraut machen.
  
> [!NOTE]
> Wenn Sie ein .NET Framework Entwickler sind, empfehlen wir Ihnen, die verwaltete EWS-API anstelle von automatisch generierten Proxys zu verwenden, um sich gegen EWS zu entwickeln. Das verwaltete EWS-API Objektmodell ist einfacher zu verwenden als automatisch generierte Proxyobjekt Modelle. Außerdem implementiert die verwaltete EWS-API [AutoErmittlung](autodiscover-for-exchange.md) und enthält clientseitige Logik. 
  
## <a name="see-also"></a>Siehe auch

- [Einrichten der Entwicklungsumgebung für Exchange-Anwendung](setting-up-your-exchange-application-development-environment.md)   
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)  
- [Steuern des Zugriffs auf EWS in Exchange](how-to-control-access-to-ews-in-exchange.md)  
- [Für Exchange-Webdienste genierte Objektmodelle für Exchange](https://msdn.microsoft.com/library/jj190899)
    