---
title: Verwalten des Benutzerzugriffs mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: Erfahren Sie, welche Optionen Sie für die Verwaltung des Benutzerkontozugriffs auf Ihren Exchange-Server haben.
ms.openlocfilehash: 431f61a0cbdfcc522eb1481399ffab1f31df9e62
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520976"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a>Verwalten des Benutzerzugriffs mithilfe von EWS in Exchange

Erfahren Sie, welche Optionen Sie für die Verwaltung des Benutzerkontozugriffs auf Ihren Exchange-Server haben.
  
Exchange Webdienste (EWS) und die verwaltete EWS-API bieten eine begrenzte Anzahl von Vorgängen, die Sie zum Verwalten von Konten auf Exchange Online, Exchange Online als Teil Office 365 oder einer Version von Exchange ab Exchange 2013 verwenden können. Mit den in der folgenden Abbildung dargestellten Vorgängen können Sie Stellvertretungen verwalten und Ordnerzugriffsberechtigungen für andere Konten festlegen. 
  
**EWS-Vorgänge für Stellvertretungs- und Ordnerzugriff**

![EWS-Benutzerverwaltungsoptionen.](media/Exchange_ManagingUserAccess_1.png)
  
Wenn Ihre Anwendung zusätzliche Kontrolle über die Konten auf einem Exchange Server benötigt, können Sie Exchange Verwaltungsshell-Cmdlets verwenden, um die Konten zu verwalten. Sie können die Cmdlets der Exchange Verwaltungsshell aufrufen, indem Sie eine der folgenden Aktionen ausführen:
  
- Schreiben einer Anwendung mit C# oder Visual Basic, die die Cmdlets der Exchange Verwaltungsshell aufruft. Sie können sich den Beispielcode in der [Dokumentation zur Exchange Verwaltungsshell-API](../management/exchange-management-shell.md) ansehen, um zu erfahren, wie Sie ein Cmdlet aufrufen. 
    
- Verwenden Windows PowerShell und Windows PowerShell Skripts zum Aufrufen Exchange Verwaltungsshell-Cmdlets. Sie finden eine vollständige Liste der [Exchange Server PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)sowie Beispiele für deren Verwendung. 
    
## <a name="see-also"></a>Siehe auch

- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)   
- [Cmdlets für Exchange 2013](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)  
    

