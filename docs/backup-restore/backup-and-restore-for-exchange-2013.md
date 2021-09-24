---
title: Sicherung und Wiederherstellung für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 329902d9-0ecb-4cfb-86dd-5ce863deff3f
description: Hier finden Sie Informationen zum Erstellen von Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013.
ms.openlocfilehash: 2be8295985651319860ab2d2a143d69f663bf932
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514900"
---
# <a name="backup-and-restore-for-exchange"></a>Sicherung und Wiederherstellung für Exchange
  
Exchange Server 2013 bietet Datenbankverfügbarkeitsgruppen (Database Availability Groups, DAGs), die dazu beitragen, gespeicherte Daten sicher und verfügbar zu halten und die Notwendigkeit benutzerdefinierter Sicherungs- und Wiederherstellungsanwendungen zu reduzieren. DAGs ermöglichen redundanz von Off-Site-Daten, um sicherzustellen, dass Keine Daten verloren gehen. Viele Notfallwiederherstellungspläne umfassen jedoch weiterhin herkömmlichere Sicherungs- und Wiederherstellungsmethoden und -systeme, einschließlich benutzerdefinierter Anwendungen, für Redundanz mit der DAG. Um die Datenverfügbarkeit und Redundanz in Ihrer Organisation sicherzustellen, können Sie benutzerdefinierte Anwendungen erstellen, die Exchange Server- und Windows Server-Betriebssystemtechnologien verwenden, um Ihre Exchange Daten zu sichern und wiederherzustellen.

<a name="bk_plugin"> </a>

## <a name="backup-technologies-in-exchange-2013"></a>Sicherungstechnologien in Exchange 2013

Exchange 2013 enthält ein Plug-In für Windows Serversicherung, mit dem Administratoren VSS-basierte Sicherungen von Exchange Daten erstellen können. Administratoren können auch Windows Serversicherung verwenden, um Exchange Datenbanken zu sichern und wiederherzustellen. Wenn Sie eine Sicherungs- und Wiederherstellungsanwendung für Exchange 2013 erstellen, müssen Sie eine Exchange-fähige Anwendung erstellen, die den VSS Writer für Exchange 2013 unterstützt, und die CHKSGFILES-API verwenden, um die Konsistenz dieser Sicherung zu überprüfen. Weitere Informationen finden Sie unter [Überprüfen der Sicherungsintegrität mithilfe der CHKSGFILES-API in Exchange 2013.](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)

<a name="bk_vsswriter"> </a>

## <a name="vss-writer-in-exchange-2013"></a>VSS Writer in Exchange 2013

Exchange 2013 wurde die VSS Writer-Architektur in Exchange Server 2010 und Exchange Server 2007 erheblich geändert. Exchange 2010 und Exchange 2007 umfassen zwei VSS-Autoren: einen innerhalb des Exchange Information Store-Diensts (store.exe) und einen innerhalb des Exchange Replikationsdiensts (msexchangerepl.exe). In Exchange 2013 befindet sich die VSS Writer-Funktion im Exchange Replikationsdienst. Ihre Sicherungs- und Wiederherstellungsanwendung verwendet den neuen VSS Writer, der als Microsoft Exchange Writer bezeichnet wird, zum Sichern aktiver und passiver Datenbankkopien und zum Wiederherstellen gesicherter Datenbankkopien. Obwohl der neue VSS Writer im Exchange Replikationsdienst ausgeführt wird, muss der dienst Exchange Information Store ausgeführt werden, damit der Writer verfügbar ist. Es sind also beide Dienste erforderlich, um Exchange-Datenbanken zu sichern oder wiederherzustellen.
  
Obwohl die VSS Writer-Architektur in Exchange 2013 aktualisiert wurde, hat sich die zugrunde liegende Funktionalität nicht geändert. Wenn Sie eine Sicherungs- und Wiederherstellungsanwendung für Exchange 2010 erstellt haben, müssen Sie für Exchange 2013 keine Änderungen an ihrer Anwendung vornehmen. Stellen Sie sicher, dass Sie Ihre Anwendung mit den neuesten Dateien neu kompilieren, um die Kompatibilität sicherzustellen. Für Sicherungs- und Wiederherstellungsanwendungen, die für Exchange 2007 oder frühere Versionen erstellt wurden, müssen Sie Ihren Code neu schreiben, um die neueste CHKSGFILES-API zu verwenden.
  
## <a name="what-you-need-to-know-about-vss-backup-and-restore"></a>Wissenswertes zur VSS-Sicherung und -Wiederherstellung

|Wenn Sie sich fragen...|Lesen Sie diesen Artikel|
|:-----|:-----|
|Anwendungsarchitekturen  <br/> |Sicherungs- und Wiederherstellungsanwendungen, die VSS zum Sichern Exchange Datenbanken verwenden, bestehen in der Regel aus einem Hintergrunddienst, der die Sicherung durchführt, einem Planungsdienst und einer Windows GUI-Anwendungskonsole, die das Sicherungs- und Wiederherstellungssystem steuert und konfiguriert.  <br/> |
|Remoteverwendung  <br/> |Anwendungen, die VSS zum Sichern von Exchange Servern verwenden, müssen auf dem computer Windows Server 2008 ausgeführt werden, auf dem der Exchange Speicherprozess ausgeführt wird. Aufgrund der Flexibilität bei großen Speichersystemen ist die Hardware, die die Speichervolumes hostet, möglicherweise nicht Teil des Computers, auf dem Windows Server 2008 ausgeführt wird.  <br/> |
|Sprachen und Tools  <br/> |Sie können eine beliebige COM-kompatible Sprache verwenden, um VSS zu verwenden. Es wird am häufigsten in Anwendungen verwendet, die in C++ geschrieben wurden. Da Sie den Exchange Speicher offline schalten müssen, um Schattenkopien zu erstellen, sind Sicherungsanwendungen in der Regel zeitaufwendig, was in den meisten Fällen die Verwendung von Sprachen wie Visual Basic oder VBScript unpraktisch macht.  <br/> |
|Verwaltete Implementierung  <br/> |Sie können die VSS-APIs in einer Umgebung mit verwaltetem Code über eine COM-Interopassembly verwenden.  <br/> |
|Skriptfähigkeit  <br/> |Ja, wird jedoch nicht empfohlen.  <br/> |
|Verfügbare Test- und Debuggingtools  <br/> |Zum Debuggen von Anwendungen, die den Windows VSS verwenden, sind keine speziellen Tools erforderlich.  <br/> |
   
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Erstellen von Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [CChkSGFiles-Klassenreferenz](cchksgfiles-class-reference.md)
    
## <a name="see-also"></a>Siehe auch

- [Volumeschattenkopie-Dienst (Windows)](https://msdn.microsoft.com/library/windows/desktop/bb968832%28v=vs.85%29.aspx)   
- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Exchange-Verwaltungsshell](../management/exchange-management-shell.md)   
- [Transport-Agents in Exchange](../transport-agents/transport-agents-in-exchange-2013.md) 
    

