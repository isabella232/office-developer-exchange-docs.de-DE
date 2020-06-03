---
title: Steuern des Clientanwendungszugriffs auf EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 60ac3f7b-ba8a-4c93-99f7-c27002caff93
description: Erfahren Sie mehr zu den Optionen für die Verwaltung des Clientanwendungszugriffs auf EWS.
localization_priority: Priority
ms.openlocfilehash: b887b8167e3d38946b1d6caffe12655ded89569f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528461"
---
# <a name="controlling-client-application-access-to-ews-in-exchange"></a>Steuern des Clientanwendungszugriffs auf EWS in Exchange

Erfahren Sie mehr zu den Optionen für die Verwaltung des Clientanwendungszugriffs auf EWS.
  
Jeder EWS-Clientanwendung, die Sie erstellen, muss Zugriff auf Exchange Online, Exchange Online als Teil von Office 365 oder eine Version von Exchange beginnend mit Exchange 2013, bevor diese EWS-Vorgänge aufrufen kann. Test- oder Produktionsserveradministratoren können die Exchange-Verwaltungsshell verwenden, um den Zugriff auf EWS entweder für alle Benutzer und Anwendungen, für einzelne Benutzer oder für einzelne Anwendungen zu beschränken. Die Zugriffssteuerung für EWS basiert auf Control EWS basiert auf Domänenkonten. Wenn eine Verbindung mit Anmeldeinformationen hergestellt wird, die von der lokalen Sicherheitsautorität authentifiziert wurden, gibt der Server einen Fehler zurück, der angibt, dass nur Domänenkonten eine Verbindung herstellen können. 
  
## <a name="access-control-for-ews-clients-and-users"></a>Zugriffssteuerung für EWS-Clients und Benutzer
<a name="bk_configure"> </a>

Ihr Test- und Produktionsserveradministrator kann die Zugriffssteuerung für Clients, die eine Verbindung zu EWS herstellen, folgendermaßen konfigurieren: 
  
- Indem für alle Clientanwendungen verhindert wird, dass eine Verbindung hergestellt wird.
    
- Indem nur bestimmten Clientanwendungen ermöglicht wird, eine Verbindung herzustellen.
    
- Indem allen Clientanwendungen ermöglicht wird, eine Verbindung herzustellen, mit Ausnahme derjenigen, die speziell blockiert werden.
    
- Indem allen Clientanwendungen ermöglicht wird, eine Verbindung herzustellen.
    
Anwendungen werden von der Benutzer-Agent-Zeichenfolge identifiziert, die sie in der HTTP-Webanforderung senden.
  
> [!IMPORTANT]
> Das Blockieren auf Anwendungsebene ist kein Sicherheitsfeature. Die Benutzer-Agent-Zeichenfolge kann ganz einfach gefälscht werden. Wenn einer Anwendung Zugriff auf EWS gewährt wird, muss die Anwendung dennoch Anmeldeinformationen bereitstellen, die der Server authentifiziert, bevor die Anwendung eine Verbindung zu EWS herstellen kann.  
  
Administratoren können über die folgenden Methoden die Zugriffssteuerung auch für Postfachbesitzer konfigurieren, die eine Verbindung zu EWS herstellen: 
  
- Durch Blockieren oder Zulassen ein ganzen Unternehmens.
    
- Durch das Blockieren oder Zulassen einer Gruppe von Benutzern, die durch einen rollenbasierten Authentifizierungsbereich identifiziert werden, der Postfachbesitzer ein- oder ausschließt, die keinen Zugriff auf EWS haben.
    
- Durch Blockieren oder Zulassen eines einzelnen Postfachbesitzers.
    
Bestimmte Zugriffssteuerungseinstellungen setzen allgemeine Zugriffssteuerungseinstellungen außer Kraft. Wenn eine Organisation beispielsweise EWS-Zugriff verweigert, einem einzelnen Postfachbesitzer jedoch Anwendungszugriff gewährt wird, hat die einzelne Einstellung Vorrang und der Zugriff wird gewährt. 
  
## <a name="delegation-and-ews-access-management"></a>Delegierung und EWS-Zugriffsverwaltung
<a name="bk_delegation"> </a>

Wenn stellvertretende Benutzer, die keinen Zugriff auf EWS haben, Ihre Clientanwendung verwenden, können sie mithilfe von EWS nicht auf das Postfach des Hauptbenutzers zugreifen, auch dann nicht, wenn der Hauptbenutzer Zugriff auf EWS hat. Wenn der stellvertretende Benutzer über EWS-Zugriff verfügt, kann der Stellvertreter Ihre EWS-Clientanwendung verwenden, um auf das Postfach des Hauptbenutzers zuzugreifen, auch wenn der Hauptbenutzer keinen Zugriff auf EWS hat. 
  
## <a name="impersonation-and-ews-access-management"></a>Identitätswechsel und EWS-Zugriffsverwaltung
<a name="bk_impersonation"> </a>

Clientanwendungen, die im Auftrag von Postfachbesitzern eine Verbindung zu EWS herstellen, können die EWS-Einstellungen des Postfachbesitzers möglicherweise nicht verwenden. Angenommen, eine Anwendung, die E-Mails für ein Unternehmen archiviert, muss, unabhängig von den Einstellungen des Postfachbenutzers eine Verbindung zu EWS herstellen. Andere Programme, z. B. E-Mail-Clients, müssen die EWS-Einstellungen des Postfachbesitzers verwenden. 
  
Administratoren sollten ein Konto für den Identitätswechsel für jede Anwendung oder Anwendungsklasse erstellen, das bzw. die auf dem Server verwendet wird. Auf diese Weise kann der Administrator den rollenbasierten Zugriffssteuerungsbereich für alle Benutzer konfigurieren, die nicht über EWS-Berechtigungen verfügen. 
  
Um Identitätswechselkonten zu aktivieren, sollte der Test- oder Produktionsserveradministrator eine der folgenden Aktionen ausführen: 
  
- Hinzufügen der Gruppe der authentifizierten Benutzer zur Gruppe „Prä-Windows 2000 kompatibler Zugriff". 
    
- Hinzufügen der Exchange Server-Gruppe zur Windows-Autorisierungszugriffsgruppe. 
    
## <a name="exchange-management-shell-cmdlets-for-access-management"></a>Cmdlets der Exchange-Verwaltungsshell für Zugriffssteuerung
<a name="bk_cmdlets"> </a>

Administratoren verwenden die folgenden Cmdlets der Exchange-Verwaltungsshell, um die EWS-Zugriffssteuerung zu konfigurieren: 
  
- [Get-CASMailbox](https://technet.microsoft.com/library/bb124754.aspx)   
- [Set-CASMailbox](https://technet.microsoft.com/library/bb125264.aspx)   
- [Get-OrganizationConfig](https://technet.microsoft.com/library/aa997571.aspx)   
- [Set-OrganizationConfig](https://technet.microsoft.com/library/aa997443.aspx)
    
## <a name="see-also"></a>Siehe auch

- [Verwenden von Webdiensten in Exchange](start-using-web-services-in-exchange.md)  
- [Steuern des Zugriffs auf EWS in Exchange](how-to-control-access-to-ews-in-exchange.md)
- [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

