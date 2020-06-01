---
title: Exchange-Verwaltungsshell
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0
description: Hier finden Sie Informationen zum Verwenden des Exchange-Verwaltungsshell zum Entwickeln von Tools für die Exchange Server-Verwaltung.
ms.openlocfilehash: 38e75339a4ad97cf8ff99e1cbe9c01059e157941
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44435807"
---
# <a name="exchange-management-shell"></a>Exchange-Verwaltungsshell

Hier finden Sie Informationen zum Verwenden des Exchange-Verwaltungsshell zum Entwickeln von Tools für die Exchange Server-Verwaltung.
  
**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365
  
Das Exchange-Verwaltungsshell bietet eine umfangreiche Reihe von Befehlen auf der Grundlage der Windows PowerShell Plattform zum Verwalten von Exchange Online, Exchange Online im Rahmen von Office 365 oder einer lokalen Exchange-Version, die mit Exchange 2013 beginnt. Mit dem Exchange-Verwaltungsshell können Sie zwei Arten von Tools erstellen: Befehlszeilenskripts, die in der Windows PowerShell Umgebung funktionieren, und Tools, die die Exchange-Verwaltungsshell-Cmdlets über eine verwaltete Schnittstelle verwenden. Sie können verwaltete Anwendungen zum Erstellen einer standardmäßigen Windows-oder webbasierten Benutzeroberfläche zum Verwalten eines Exchange-Servers verwenden. 
  
## <a name="what-you-need-to-know-about-the-exchange-management-shell"></a>Was Sie über die Exchange-Verwaltungsshell wissen müssen

|Wenn Sie sich Gedanken über|Lesen Sie diesen Artikel|
|:-----|:-----|
|Verfügbarkeit  <br/> |Exchange-Verwaltungsshell-Befehle werden auf allen Servern installiert, auf denen Versionen von Exchange mit Exchange 2007 gestartet werden.<br/>Client Anwendungen können auf jedem Computer mit Windows PowerShell 2,0 bereitgestellt werden.<br/> Informationen zum Zugriff auf die Shell finden Sie unter [Exchange Server PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).  <br/> |
|Sprachen und Tools  <br/> |Sie können Exchange-Verwaltungsshell Skripts in einem beliebigen Text-Editor erstellen.<br/>Sie können eines der zahlreichen Tools von Drittanbietern verwenden, um Windows PowerShell Skripts zu erstellen, die mit dem Exchange-Verwaltungsshell verwendet werden können.  <br/> Das [Exchange-Verwaltungsshell-Objektmodell](exchange-management-shell-namespaces.md) basiert auf dem .NET Framework.<br/>Sie können alle .NET-Sprachen verwenden, um Exchange-Verwaltungsshell Anwendungen zu entwickeln.  <br/> |
|Verfügbare Test- und Debuggingtools  <br/> |Sie können eine von vielen Anwendungen von Drittanbietern verwenden, um Exchange-Verwaltungsshell Skripts zu testen und zu debuggen.  <br/> Sie können Visual Studio-und Drittanbietertools verwenden, um verwaltete Exchange-Verwaltungsshell-Anwendungen zu testen und zu debuggen.  <br/> |
|Anforderungen an die Serverplattform  <br/> |Sie können die Exchange-Verwaltungsshell auf jedem Exchange-Server verwenden, auf dem Windows PowerShell 2,0 installiert ist.  <br/> |
|Anforderungen an die Clientplattform  <br/> |Exchange-Verwaltungsshell Clientanwendungen erfordern Windows PowerShell 2,0.  <br/> |
|Berechtigungen  <br/> |Für die Ausführung einer Exchange-Verwaltungsshell Anwendung muss der Benutzer über rollenbasierte Zugriffssteuerungsrechte für die betroffenen Daten im Exchange-Informationsspeicher verfügen.<br/>Weitere Informationen zur rollenbasierten Zugriffssteuerung finden Sie unter [Grundlegendes zur rollenbasierten Zugriffssteuerung](https://technet.microsoft.com/library/dd298183.aspx).  <br/> |
   
In den Artikeln in diesem Abschnitt werden Exchange-Verwaltungsshell Features beschrieben, die für die Erstellung von Exchange-Verwaltungstools wichtig sind. Informationen zum Planen, konfigurieren oder Verwalten von Exchange finden Sie auf dem [Exchange](https://docs.microsoft.com/exchange/) -Standort.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen von Exchange-Verwaltungsshell Tools](create-exchange-management-shell-tools.md)
    
- [Exchange-Verwaltungsshell Namespaces](exchange-management-shell-namespaces.md)
    
## <a name="see-also"></a>Siehe auch
  
- [Windows PowerShell Dokumentation](https://docs.microsoft.com/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6)
- [PowerShell-Skripterstellung](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6)
    

