---
title: Verwalten des Benutzerzugriffs in Exchange mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: Hier finden Sie Informationen zu die Optionen für die Verwaltung von Benutzerkonten den Zugriff auf Ihren Exchange-Server.
ms.openlocfilehash: d93f521f08f93b44b4ecc1f258b03ed24ebdd3dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757031"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a>Verwalten des Benutzerzugriffs in Exchange mithilfe der Exchange-Webdienste

Hier finden Sie Informationen zu die Optionen für die Verwaltung von Benutzerkonten den Zugriff auf Ihren Exchange-Server.
  
Exchange-Webdienste (EWS) und die EWS managed API bieten eine begrenzte Anzahl von Operationen, die Sie zum Verwalten von Konten in Exchange Online, Exchange Online als Teil von Office 365 oder eine Version von Exchange, beginnend mit Exchange 2013 verwenden können. Sie können die Vorgänge in der folgenden Abbildung dargestellt, Stellvertretungen verwalten und Festlegen von Zugriffsberechtigungen für Ordner für andere Konten verwenden. 
  
**EWS-Vorgänge für den Delegaten und Ordner**

![EWS-Benutzerverwaltungsoptionen.](media/Exchange_ManagingUserAccess_1.png)
  
Wenn die Anwendung zusätzliche Kontrolle über die Konten auf einem Exchange-Server benötigt, können Sie die Exchange-Verwaltungsshell-Cmdlets zum Verwalten von Konten verwenden. Sie können die Exchange-Verwaltungsshell-Cmdlets aufrufen, indem Sie einen der folgenden Schritte ausführen:
  
- Schreiben einer Anwendung mit c# oder Visual Basic, die die Exchange-Verwaltungsshell-Cmdlets aufruft. Betrachten Sie im Beispielcode in der [Exchange Management Shell API-Dokumentation](../management/exchange-management-shell.md) erfahren, wie ein Cmdlet aufrufen. 
    
- Verwenden von Windows PowerShell und Windows PowerShell-Skripts zum Aufrufen der Exchange-Verwaltungsshell-Cmdlets. Finden Sie eine vollständige Liste mit den [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps), zusammen mit Beispielen, die zeigen, deren Verwendung. 
    
## <a name="see-also"></a>Siehe auch

- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)   
- [Exchange 2013-Cmdlets](https://docs.microsoft.com/en-us/powershell/exchange/?view=exchange-ps)  
    

