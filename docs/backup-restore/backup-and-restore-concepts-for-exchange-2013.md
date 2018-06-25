---
title: Sichern und Wiederherstellen von Konzepten für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a1c4709-9313-4ccf-9f8a-673a51d51f23
description: Hier finden Sie Informationen zu den Exchange-Datenbanken, die Sie erstellen sichern und Wiederherstellen von Anwendungen für Exchange 2013 unterstützen.
ms.openlocfilehash: 5fa62c3d34ffbe8f0bab852c6d41c49220e2883a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756809"
---
# <a name="backup-and-restore-concepts-for-exchange-2013"></a>Sichern und Wiederherstellen von Konzepten für Exchange 2013

Hier finden Sie Informationen zu den Exchange-Datenbanken, die Sie erstellen sichern und Wiederherstellen von Anwendungen für Exchange 2013 unterstützen.
  
Bevor Sie Sicherungsdatei erstellen und Anwendungen für Exchange Server 2013 wiederherstellen, sollten Sie mit der Exchange-Datenbank-Dateistruktur vertraut sein. Mithilfe der Exchange-Informationsspeicher-Datenbankdateien können Sie sichern Sie die Daten in Ihrem Shop und stellen Sie es zu einem späteren Zeitpunkt bei Bedarf wieder her. Wenn Sie den Speicherplatz auf dem Datenträger beschränkt werden, kann der Administrator umlaufprotokollierung implementieren, und dies wirkt sich auf die Möglichkeit zum Sichern der Datenbank. Sie können auch nutzen des Datenbank-Mobilitätsfeatures in Exchange 2013 zum Sichern und Wiederherstellen von Exchange-Daten. Datenbankmobilität in Kombination mit der Anwendung sichern und Wiederherstellen ist eine gute Maß Redundanz für Disaster Recovery.

<a name="bk_exchangedatabases"> </a>

## <a name="exchange-store-database-files"></a>Exchange-Speicherdatenbankdateien

Exchange 2013 bietet Unterstützung für bis zu 100 Datenbanken. Jede Exchange 2013-Datenbank enthält die Dateien in der folgenden Tabelle aufgeführt. 
  
**In Tabelle 1. Exchange 2013-Datenbankdateien**

|Dateityp|Erweiterung|Beschreibung|
|:-----|:-----|:-----|
|Datenbankdatei  <br/> |\*EDB  <br/> |Zeichnet alle Änderungen auf, die in der im Arbeitsspeicher abgelegten Datenbank übernommen wurden.  <br/> |
|Transaktionsprotokoll-Datenstrom  <br/> |\*.log  <br/> |Datensatzvorgänge, z. B. Erstellung oder Änderung von einer Nachricht, die in der Datenbank übernommen werden sollen. Jeweils auf 1 MB beschränkt.  <br/> |
|Prüfpunktdatei  <br/> |\*CHK  <br/> |Datensätze, die in Datenbankdateien auf dem Datenträger geschriebene Transaktionen protokolliert haben.  <br/> |
   
Exchange 2013 verwaltet einen einzelnen Satz von Transaktionsprotokolldateien für jede Datenbank. Die Transaktionsprotokolle sind für sicherungs-und Wiederherstellungsvorgänge wichtig. Wenn Sie erstellen Sie eine Sicherung und Wiederherstellung der Anwendung, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwendet, müssen Sie sicherstellen, dass Sie diese Protokolle ordnungsgemäß behandeln. Weitere Informationen finden Sie unter [Transaktionsprotokolle und Prüfpunktdateien für Sicherung und Wiederherstellung in Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md). Zum Sichern einer Datenbank und dessen Protokollstream müssen Sie das gesamte Volume sichern, die die Datenbank und die Protokolle enthält. Abschneiden des Protokolls tritt erst nach einer erfolgreichen Abschluss einer vollständigen Sicherung von einem Datenträger oder Ordner, die eine Exchange-Datenbank enthalten.
  
Auf jedem Exchange-Server können Sie jeweils nur eine Wiederherstellungsdatenbank bereitstellen. Sie können die Wiederherstellungsdatenbank mithilfe der Exchange-Verwaltungsshell-Cmdlets wie **New-MailboxRestoreRequest**zugreifen. Weitere Informationen zu Exchange Wiederherstellungsdatenbank finden Sie unter [Recovery Databases](http://technet.microsoft.com/en-us/library/dd876954%28v=exchg.150%29.aspx) auf TechNet. Weitere Informationen zu Exchange-Verwaltungsshell-Cmdlets finden Sie unter [Exchange 2013-Cmdlets](http://technet.microsoft.com/en-us/library/bb124413.aspx) auf TechNet. 
  
## <a name="circular-logging"></a>Umlaufprotokollierung
<a name="bk_circularlogging"> </a>

Ist die Speicherkapazität auf ein Problem, kann der Administrator umlaufprotokollierung aktivieren. Wenn die zirkuläre Protokollierung aktiviert ist, schreibt Exchange Transaktionsprotokolle wie gewohnt, aber bei eine Prüfpunktdatei auf Erweitert festgelegt ist, wird der inaktive Teil des Transaktionsprotokolls abgeschnitten. Der Administrator sollte nicht konfigurieren Exchange 2013-Datenbanken Verwendung zirkuläre Protokollierung, wenn Sie auch VSS zum Aktivieren der benutzerdefinierten Sicherung und Wiederherstellung verwenden möchten. Umlaufprotokollierung erstellt die folgenden Einschränkungen: 
  
- Wenn sie während des Sicherungs- oder Wiederherstellungsvorgangs aktiviert ist, können Sie die einzelne Datenbanken nicht wiederherstellen.
    
- Nur Recovery Point-in-Time-Vorgänge sind möglich. Wenn zirkuläre Protokollierung aktiviert ist, können Sie löschen Transaktionsprotokolle im gleichen Verzeichnis befindet, wenn eine Datenbank wiederhergestellt wird, obwohl diese Protokolle Bestandteil einer anderen Exchange 2013-Datenbank möglicherweise. 
    
- Sie können keine inkrementellen oder differenziellen Sicherung auszuführen. Weitere Informationen über diese Art von Sicherungen finden Sie unter [Typen von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md).
    
Wenn zirkuläre Protokollierung aktiviert ist, sollte der Administrator deaktivieren Sie ihn so bald wie möglich, um sicherzustellen, dass Ihre VSS-Sicherung nicht ausgeführt werden. Weitere Informationen checken Sie den Blogbeitrag [Exchange zirkuläre Protokollierung und VSS-Sicherung](http://blogs.technet.com/b/exchange/archive/2010/08/18/3410672.aspx)aus. 
  
## <a name="exchange-database-mobility"></a>Exchange-Datenbankmobilität
<a name="bk_exchangedatabasemobility"> </a>

Exchange 2013 ermöglicht datenbankmobilität um Postfach Zuverlässigkeit und Verfügbarkeit zu verbessern. Datenbankmobilität können Sie Kopien der Exchange Store-Datenbank, trennen Sie die Datenbank vom Server und auf einem anderen Server zu speichern. In einer Exchange 2013 Database Availability Group (DAG), werden mehrere Kopien der Datenbank auf unterschiedlichen Computern gespeichert. Wenn eine oder mehrere Kopien der Datenbank von Hardware- oder andere Systemfehler verloren gegangen sind, kann Informationen von den anderen Kopien auf die Datenbank über normale Replikationsvorgänge Ausführen eines erneuten Seedings verwendet werden.
  
Für backup-Vorgänge Wenn die Konfiguration der zu sichernden Exchange 2013-Datenbanken in einer DAG kann die backup-Anwendung besser Interferenzen zwischen der Momentaufnahme und der aktiven Server Performance verhindern, indem Sie den Snapshot auf einem der inaktiv Datenbank kopiert. Da in den meisten Fällen Datenbankkopien synchronisiert werden, kann die backup-Anwendung Momentaufnahmen aus verschiedenen Kopien der Datenbank, und es später von der Pfadkomponenten wiederherzustellen.
  
Die einzige unterstützte Methode zum Wiederherstellen von DAG-Datenbanken aus Sicherungsdaten besteht darin, alle Kopien der Datenbank unter Verwendung derselben Sicherungsdaten wiederherzustellen. Da die Datenbankprotokolldateien der Kopien geringfügig voneinander abweichen können, kann das Wiederherstellen einzelner Datenbankkopien unter Verwendung unterschiedlicher Daten dazu führen, dass die Datenbank nicht mehr bereitgestellt werden kann.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Transaktionsprotokolle und Prüfpunktdateien für Sicherung und Wiederherstellung in Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Exchange-Writer in Exchange 2013](exchange-writer-in-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch

- [Exchange Online und Exchange-Entwicklung](../exchange-server-development.md) 
- [Arten von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Wiederherstellen von Exchange 2013-Datenbanken](restoring-exchange-2013-databases.md)
    

