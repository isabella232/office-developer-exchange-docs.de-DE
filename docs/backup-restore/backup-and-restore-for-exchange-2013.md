---
title: Sicherung und Wiederherstellung für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 329902d9-0ecb-4cfb-86dd-5ce863deff3f
description: Hier finden Sie Informationen zum Erstellen von Sicherungs-und Wiederherstellungsanwendungen für Exchange 2013.
ms.openlocfilehash: 1c5d99be60501fd1c4414ea22294bd05645bb0a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455240"
---
# <a name="backup-and-restore-for-exchange"></a>Sicherung und Wiederherstellung für Exchange
  
Exchange Server 2013 bietet Database Availability Groups (DAGs), mit denen die Sicherheit und Verfügbarkeit gespeicherter Daten gewährleistet wird und die Notwendigkeit benutzerdefinierter Sicherungs-und Wiederherstellungsanwendungen reduziert wird. DAGs ermöglichen die Datenredundanz außerhalb des Standorts, um sicherzustellen, dass keine Daten verloren gehen. Viele Notfallwiederherstellungspläne enthalten jedoch weiterhin herkömmliche Sicherungs-und Wiederherstellungsmethoden und-Systeme, einschließlich benutzerdefinierter Anwendungen, für Redundanz mit der DAG. Um die Verfügbarkeit und Redundanz von Daten in Ihrer Organisation sicherzustellen, können Sie benutzerdefinierte Anwendungen erstellen, die Exchange Server-und Windows Server-Betriebssystemtechnologien verwenden, um Ihre Exchange-Daten zu sichern und wiederherzustellen.

<a name="bk_plugin"> </a>

## <a name="backup-technologies-in-exchange-2013"></a>Sicherungstechnologien in Exchange 2013

Exchange 2013 enthält ein Plug-in für die Windows Server-Sicherung, mit dem Administratoren VSS-basierte Sicherungen von Exchange-Daten erstellen können. Administratoren können auch die Windows Server-Sicherung zum Sichern und Wiederherstellen von Exchange-Datenbanken verwenden. Wenn Sie eine Sicherungs-und Wiederherstellungsanwendung für Exchange 2013 erstellen, müssen Sie eine Exchange-fähige Anwendung erstellen, die den VSS-Writer für Exchange 2013 unterstützt, und die Konsistenz dieser Sicherung mithilfe der CHKSGFILES-API überprüfen. Weitere Informationen finden Sie unter [Überprüfen der Integrität von Sicherungen mithilfe der CHKSGFILES-API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).

<a name="bk_vsswriter"> </a>

## <a name="vss-writer-in-exchange-2013"></a>VSS-Writer in Exchange 2013

Exchange 2013 stellt eine bedeutende Änderung an der VSS Writer-Architektur in Exchange Server 2010 und Exchange Server 2007. Exchange 2010 und Exchange 2007 enthalten zwei VSS-Writer: eine innerhalb des Exchange-Informationsspeicherdiensts (Store. exe) und eine innerhalb des Exchange-Replikationsdiensts (MSExchangeRepl. exe). In Exchange 2013 befindet sich die VSS Writer-Funktion im Exchange-Replikationsdienst. Die Sicherungs-und Wiederherstellungsanwendung verwendet den neuen VSS-Writer, der als Microsoft Exchange Writer bezeichnet wird, um aktive und passive Datenbankkopien zu sichern und gesicherte Datenbankkopien wiederherzustellen. Obwohl der neue VSS-Writer im Exchange-Replikationsdienst ausgeführt wird, muss der Exchange-Informationsspeicherdienst ausgeführt werden, damit der Writer zur Verfügung steht. Es sind also beide Dienste erforderlich, um Exchange-Datenbanken zu sichern oder wiederherzustellen.
  
Die VSS Writer-Architektur wurde zwar in Exchange 2013 aktualisiert, die zugrunde liegende Funktionalität wurde jedoch nicht geändert. Wenn Sie eine Sicherungs-und Wiederherstellungsanwendung für Exchange 2010 erstellt haben, müssen Sie keine Änderungen an Ihrer Anwendung für Exchange 2013 vornehmen. Stellen Sie sicher, dass Sie Ihre Anwendung mit den neuesten Dateien neu kompilieren, um die Kompatibilität sicherzustellen. Für Sicherungs-und Wiederherstellungsanwendungen, die für Exchange 2007 oder früheren Versionen erstellt wurden, müssen Sie den Code neu schreiben, um die neueste CHKSGFILES-API zu verwenden.
  
## <a name="what-you-need-to-know-about-vss-backup-and-restore"></a>Was Sie über VSS-Sicherung und-Wiederherstellung wissen müssen

|Wenn Sie sich Fragen, über...|Lesen Sie diesen Artikel|
|:-----|:-----|
|Anwendungsarchitekturen  <br/> |Sicherungs-und Wiederherstellungsanwendungen, die VSS zum Sichern von Exchange-Datenbanken verwenden, bestehen in der Regel aus einem Hintergrunddienst, der die Sicherung ausführt, einem Planungsdienst und einer Windows GUI-Anwendungs Konsole, die das Sicherungs-und Wiederherstellungssystem steuert und konfiguriert.  <br/> |
|Remoteverwendung  <br/> |Anwendungen, die VSS zum Sichern von Exchange-Servern verwenden, müssen auf dem Windows Server 2008 Computer ausgeführt werden, auf dem der Exchange-Informationsspeicher Prozess ausgeführt wird. Aufgrund der Flexibilität in großen Speichersystemen ist die Hardware, die die Speicher Datenträger hostet, möglicherweise nicht physisch Bestandteil des Computers, auf dem Windows Server 2008 läuft.  <br/> |
|Sprachen und Tools  <br/> |Sie können eine beliebige com-kompatible Sprache verwenden, um VSS zu verwenden. Sie wird am häufigsten in in C++ geschriebenen Anwendungen verwendet. Da Sie die Exchange-Informationsspeicher zum Erstellen von Schattenkopien offline schalten müssen, sind Sicherungsanwendungen in der Regel zeitkritisch, was in den meisten Fällen die Verwendung von Sprachen wie Visual Basic oder VBScript unpraktisch gestaltet.  <br/> |
|Verwaltete Implementierung  <br/> |Sie können die VSS-APIs in einer Umgebung mit verwaltetem Code über eine COM-Interop-Assembly verwenden.  <br/> |
|Skriptfähigkeit  <br/> |Ja, wird jedoch nicht empfohlen.  <br/> |
|Verfügbare Test- und Debuggingtools  <br/> |Zum Debuggen von Anwendungen, die den Windows VSS verwenden, sind keine speziellen Tools erforderlich.  <br/> |
   
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Erstellen von Sicherungs-und Wiederherstellungsanwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [CChkSGFiles-Klassenreferenz](cchksgfiles-class-reference.md)
    
## <a name="see-also"></a>Siehe auch

- [Volumenschattenkopie-Dienst (Windows)](https://msdn.microsoft.com/library/windows/desktop/bb968832%28v=vs.85%29.aspx)   
- [Erkunden von EWS Managed API, EWS und Webdiensten in Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Exchange-Verwaltungsshell](../management/exchange-management-shell.md)   
- [Transport-Agents in Exchange](../transport-agents/transport-agents-in-exchange-2013.md) 
    

