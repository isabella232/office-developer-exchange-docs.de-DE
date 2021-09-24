---
title: Exchange-Verwaltungsshell
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0
description: Hier finden Sie Informationen zur Verwendung der Exchange-Verwaltungsshell zum Entwickeln von Tools für Exchange Serververwaltung.
ms.openlocfilehash: ee1cbcb174c7153ca6cd9bb089580b372bf9029b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516153"
---
# <a name="exchange-management-shell"></a>Exchange-Verwaltungsshell

Hier finden Sie Informationen zur Verwendung der Exchange-Verwaltungsshell zum Entwickeln von Tools für Exchange Serververwaltung.
  
**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365
  
Die Exchange-Verwaltungsshell bietet einen umfangreichen Satz von Befehlen, die auf der Windows PowerShell Plattform basieren, zum Verwalten von Exchange Online, Exchange Online als Teil Office 365 oder einer lokalen Version von Exchange beginnend mit Exchange 2013. Mit der Exchange-Verwaltungsshell können Sie zwei Arten von Tools erstellen: Befehlszeilenskripts, die innerhalb der Windows PowerShell umgebung funktionieren, und Tools, die die Cmdlets der Exchange Verwaltungsshell über eine verwaltete Schnittstelle verwenden. Sie können verwaltete Anwendungen verwenden, um eine standardmäßige Windows oder webbasierte Benutzeroberfläche zum Verwalten eines Exchange Servers zu erstellen. 
  
## <a name="what-you-need-to-know-about-the-exchange-management-shell"></a>Was Sie über die Exchange-Verwaltungsshell wissen müssen

|Wenn Sie sich fragen|Lesen Sie diesen Artikel|
|:-----|:-----|
|Verfügbarkeit  <br/> |Exchange Verwaltungsshell-Befehle werden auf allen Servern installiert, auf denen Versionen von Exchange ab Exchange 2007 ausgeführt werden.<br/>Clientanwendungen können auf jedem Computer bereitgestellt werden, auf dem Windows PowerShell 2.0 ausgeführt wird.<br/> Informationen zum Zugriff auf die Shell finden Sie unter [Exchange Server PowerShell (Exchange-Verwaltungsshell).](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)  <br/> |
|Sprachen und Tools  <br/> |Sie können Exchange Verwaltungsshell-Skripts in einem beliebigen Text-Editor erstellen.<br/>Sie können eines von vielen Drittanbietertools zum Erstellen Windows PowerShell Skripts verwenden, die mit der Exchange-Verwaltungsshell verwendet werden können.  <br/> Das [Exchange Verwaltungsshell-Objektmodell](exchange-management-shell-namespaces.md) basiert auf dem .NET Framework.<br/>Sie können eine beliebige .NET-Sprache verwenden, um Exchange Verwaltungsshell-Anwendungen zu entwickeln.  <br/> |
|Verfügbare Test- und Debuggingtools  <br/> |Sie können eine von vielen Drittanbieteranwendungen verwenden, um Exchange Verwaltungsshell-Skripts zu testen und zu debuggen.  <br/> Sie können Visual Studio und Tools von Drittanbietern verwenden, um verwaltete Exchange Verwaltungsshell-Anwendungen zu testen und zu debuggen.  <br/> |
|Anforderungen an die Serverplattform  <br/> |Sie können die Exchange Verwaltungsshell auf jedem Exchange Server verwenden, auf dem Windows PowerShell 2.0 installiert ist.  <br/> |
|Anforderungen an die Clientplattform  <br/> |Exchange Für Clientanwendungen der Verwaltungsshell ist Windows PowerShell 2.0 erforderlich.  <br/> |
|Berechtigungen  <br/> |Das Ausführen einer Exchange Verwaltungsshell-Anwendung erfordert, dass der Benutzer über rollenbasierte Zugriffssteuerungsrechte für die betroffenen Daten im Exchange Speicher verfügt.<br/>Weitere Informationen zur rollenbasierten Zugriffssteuerung finden Sie unter Grundlegendes zur [rollenbasierten Zugriffssteuerung.](https://technet.microsoft.com/library/dd298183.aspx)  <br/> |
   
In den Artikeln in diesem Abschnitt werden Exchange Verwaltungsshell-Features beschrieben, die für die Erstellung Exchange Verwaltungstools wichtig sind. Informationen zum Planen, Konfigurieren oder Verwalten von Exchange finden Sie auf der [Exchange](https://docs.microsoft.com/exchange/) Website.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen von Exchange-Verwaltungsshell-Tools](create-exchange-management-shell-tools.md)
    
- [Namespaces für Exchange-Verwaltungsshell](exchange-management-shell-namespaces.md)
    
## <a name="see-also"></a>Siehe auch
  
- [Windows PowerShell Dokumentation](https://docs.microsoft.com/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6)
- [PowerShell-Skripting](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6)
    

