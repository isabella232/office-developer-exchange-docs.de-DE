---
title: Steuern des Zugriffs auf EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: Erfahren Sie, wie Sie den Zugriff auf EWS für Benutzer, Anwendungen oder die gesamte Organisation steuern.
ms.openlocfilehash: 956c28faba105ecf2a6b1452abe629ea2fc930e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756870"
---
# <a name="control-access-to-ews-in-exchange"></a>Steuern des Zugriffs auf EWS in Exchange

Erfahren Sie, wie Sie den Zugriff auf EWS für Benutzer, Anwendungen oder die gesamte Organisation steuern.
  
Unabhängig davon, ob Sie die verwaltete EWS-API oder EWS direkt in Ihrer Anwendung verwenden, können Sie den Zugriff auf Exchange-Webdienste (EWS) steuern. Wenn Sie über Administratorrechte auf Ihrem Exchange-Server verfügen, können Sie den Zugriff auf EWS mithilfe der Exchange-Verwaltungsshell verwalten und den Zugriff global, für jeden Benutzer und für jede Anwendung steuern.
  
## <a name="exchange-management-shell-cmdlets-for-configuring-access-control"></a>Cmdlets der Exchange-Verwaltungsshell zum Konfigurieren der Zugriffssteuerung
<a name="bk_Cmdlets"> </a>

Mit den folgenden Cmdlets der Exchange-Verwaltungsshell können Sie die aktuelle Zugriffskonfiguration anzeigen und EWS-Zugriffssteuerungen festlegen:
  
- [Get-CASMailbox](http://technet.microsoft.com/en-us/library/bb124754.aspx): Zeigt an, welche Parameter für ein bestimmtes Postfach festgelegt sind.   
- [Set-CASMailbox](http://technet.microsoft.com/en-us/library/bb125264.aspx): Legt Parameter für ein bestimmtes Postfach fest.    
- [Get-OrganizationConfig](http://technet.microsoft.com/en-us/library/aa997571.aspx): Zeigt die Parameter für die gesamte Organisation an.    
- [Set-OrganizationConfig](http://technet.microsoft.com/en-us/library/aa997443.aspx): Legt die Parameter für die gesamte Organisation fest. 

<a name="bk_Examples"> </a>

## <a name="examples-controlling-access-to-ews"></a>Beispiele: Steuern des Zugriffs auf EWS

Lassen Sie uns jetzt einige Szenarien ansehen, die zeigen, wie Sie den Zugriff auf Ihre Anwendung steuern können.
  
**Tabelle 1: Befehle zum Steuern des Zugriffs auf EWS**

|Zweck |Verwenden Sie diesen Befehl|
|:-----|:-----|
|Blockieren der Verwendung von EWS für alle Clientanwendungen | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList`<br/><br/>Damit können in der AllowList aufgeführte Anwendungen eine Verbindung herstellen. In diesem Beispiel sind keine Anwendungen in der AllowList enthalten, was bedeutet, dass keine Anwendungen EWS verwenden können. |
|Zulassen der Verwendung von EWS für eine Liste von Clientanwendungen | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/>Damit können bestimmte Anwendungen EWS verwenden. In diesem Beispiel wird der Zugriff für jede Anwendung gewährt, deren Zeichenfolge des Benutzer-Agenten mit „OWA/" beginnt.   |
|Zulassen der Verwendung von EWS für alle Clientanwendungen, mit Ausnahme der Anwendungen, die spezifisch blockiert wurden | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/>In diesem Beispiel wird die Verwendung von EWS nur für die Anwendungen blockiert, deren Zeichenfolge des Benutzer-Agenten mit „OWA/" beginnt. |
|Zulassen der Verwendung von EWS für alle Clientanwendungen | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList` <br/><br/> Da keine BlockList angegeben ist, können alle Anwendungen EWS verwenden. |
|Blockieren der Verwendung von EWS für die gesamte Organisation | `Set-OrganizationConfig -EwsEnabled:$false` |
|Zulassen der Verwendung von EWS für die gesamte Organisation | `Set-OrganizationConfig -EwsEnabled:$true`|
|Blockieren der Verwendung von EWS für ein einzelnes Postfach | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|Zulassen der Verwendung von EWS für ein einzelnes Postfach | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|
   
## <a name="see-also"></a>Siehe auch

- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)    
- [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md)   
- [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
- [Windows PowerShell](http://msdn.microsoft.com/en-us/library/dd835506%28v=vs.85%29.aspx)
    

