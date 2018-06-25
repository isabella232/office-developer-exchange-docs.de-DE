---
title: Exchange-Verwaltungsshell
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0
description: Hier finden Sie Informationen dazu, wie Sie die Exchange-Verwaltungsshell verwenden, um die Tools für die Verwaltung von Exchange Server zu entwickeln.
ms.openlocfilehash: 1cb0328bdb0eebda0ce4eda929e1bfb21be451f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757138"
---
# <a name="exchange-management-shell"></a>Exchange-Verwaltungsshell

Hier finden Sie Informationen dazu, wie Sie die Exchange-Verwaltungsshell verwenden, um die Tools für die Verwaltung von Exchange Server zu entwickeln.
  
**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365
  
Die Exchange-Verwaltungsshell bietet einen umfassenden Satz von Befehlen, basierend auf der Windows PowerShell-Plattform für die Verwaltung von Exchange Online, Exchange Online als Teil von Office 365 oder eine lokale Version von Exchange, beginnend mit Exchange 2013. Sie können die Exchange-Verwaltungsshell verwenden, erstellen Sie zwei Arten von Tools: Befehlszeilenskripts, die innerhalb der Windows PowerShell-Umgebung arbeiten und Tools, die die Exchange-Verwaltungsshell-Cmdlets über eine verwaltete Schnittstelle verwenden. Sie können verwaltete Anwendungen zum Erstellen eines standardmäßigen Windows- oder webbasierte Benutzeroberfläche zum Verwalten von eines Exchange-Servers verwenden. 
  
## <a name="what-you-need-to-know-about-the-exchange-management-shell"></a>Sie müssen über die Exchange-Verwaltungsshell wissen sollten

|Wenn Sie wissen möchten, zu|Lesen Sie diesen Artikel|
|:-----|:-----|
|Verfügbarkeit  <br/> |Exchange-Verwaltungsshell-Befehle werden auf allen Servern mit Exchange, beginnend mit Exchange 2007-Versionen installiert.<br/>Clientanwendungen können auf Computern unter Windows PowerShell 2.0 bereitgestellt werden.<br/> Informationen zum Zugreifen auf die Shell finden Sie unter [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).  <br/> |
|Sprachen und Tools  <br/> |Sie können die Exchange-Verwaltungsshell-Skripts in einem beliebigen Texteditor erstellen.<br/>Verwenden eines viele Drittanbieter-Tools zum Erstellen von Windows PowerShell-Skripts, die mit der Exchange-Verwaltungsshell verwendet werden können.  <br/> Der [Exchange-Verwaltungsshell-Objektmodell](exchange-management-shell-namespaces.md) basiert auf .NET Framework.<br/>Jeder können Sie die Exchange-Verwaltungsshell Anwendungsentwicklung.  <br/> |
|Verfügbare Test- und Debuggingtools  <br/> |Verwenden eines viele Drittanbieter-Clientanwendungen zum Testen und Debuggen von Skripts für Exchange-Verwaltungsshell.  <br/> Visual Studio können und Drittanbieter-Tools zum Testen und Debuggen von verwalteten Exchange-Verwaltungsshell Applications.  <br/> |
|Anforderungen an die Serverplattform  <br/> |Sie können die Exchange-Verwaltungsshell auf allen Exchange-Servern, die Windows PowerShell 2.0 installiert ist.  <br/> |
|Anforderungen an die Clientplattform  <br/> |Exchange-Verwaltungsshell-Clientanwendungen erfordern Windows PowerShell 2.0.  <br/> |
|Berechtigungen  <br/> |Ausführen einer Exchange-Verwaltungsshell erfordert Anwendung an, dass der Benutzer über rollenbasierte Steuerelement Zugriffsrechte für die betroffenen Daten auf dem Exchange-Speicher.<br/>Weitere Informationen zu den rollenbasierte Zugriffssteuerung finden Sie unter [Understanding Role Based Access Control](http://technet.microsoft.com/en-us/library/dd298183.aspx).  <br/> |
   
Die Artikel in diesem Abschnitt beschreiben Exchange-Verwaltungsshell-Features, die für das Erstellen von Exchange-Verwaltungstools eine wichtige Rolle spielen. Informationen zum Planen, konfigurieren oder Verwalten von Exchange finden Sie unter [Exchange](https://docs.microsoft.com/en-us/exchange/) -Standort.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen von Exchange-Verwaltungsshell-tools](create-exchange-management-shell-tools.md)
    
- [Exchange-Verwaltungsshell-namespaces](exchange-management-shell-namespaces.md)
    
## <a name="see-also"></a>Siehe auch
  
- [Windows PowerShell-Dokumentation](https://docs.microsoft.com/en-us/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6)
- [PowerShell-Skripts](https://docs.microsoft.com/en-us/powershell/scripting/powershell-scripting?view=powershell-6)
    

