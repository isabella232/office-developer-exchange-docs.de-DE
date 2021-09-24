---
title: Sichern und Wiederherstellen von Konzepten für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9a1c4709-9313-4ccf-9f8a-673a51d51f23
description: Hier finden Sie Informationen zu Exchange Datenbanken, mit denen Sie Ihre Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013 erstellen können.
ms.openlocfilehash: c0b2e0269c3668779f980bf6984d84aff76573f1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510519"
---
# <a name="backup-and-restore-concepts-for-exchange-2013"></a>Sichern und Wiederherstellen von Konzepten für Exchange 2013

Hier finden Sie Informationen zu Exchange Datenbanken, mit denen Sie Ihre Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013 erstellen können.
  
Bevor Sie Sicherungs- und Wiederherstellungsanwendungen für Exchange Server 2013 erstellen, sollten Sie mit der Exchange Datenbankdateistruktur vertraut sein. Mit den Exchange-Speicherdatenbankdateien können Sie die Daten im Speicher sichern und sie bei Bedarf zu einem späteren Zeitpunkt wiederherstellen. Wenn der Speicherplatz auf dem Datenträger begrenzt ist, implementiert Ihr Administrator möglicherweise die Umlaufprotokollierung, was sich auf die Sicherung der Datenbank auswirkt. Sie können auch das Datenbank-Mobilitätsfeature in Exchange 2013 nutzen, um Exchange Daten zu sichern und wiederherzustellen. Datenbankmobilität dient in Verbindung mit Ihrer Sicherungs- und Wiederherstellungsanwendung als Maßstab für die Redundanz für die Notfallwiederherstellung.

<a name="bk_exchangedatabases"> </a>

## <a name="exchange-store-database-files"></a>Exchange-Speicherdatenbankdateien

Exchange 2013 umfasst Unterstützung für bis zu 100 Datenbanken. Jede Exchange 2013-Datenbank enthält die in der folgenden Tabelle aufgeführten Dateien. 
  
**Tabelle 1. Exchange 2013-Datenbankdateien**

|Dateityp|Erweiterung|Beschreibung|
|:-----|:-----|:-----|
|Datenbankdatei  <br/> |\*.edb  <br/> |Zeichnet alle Änderungen auf, die in der im Arbeitsspeicher abgelegten Datenbank übernommen wurden.  <br/> |
|Transaktionsprotokoll-Datenstrom  <br/> |\*LOG  <br/> |Datensatzvorgänge, z. B. Erstellung oder Änderung von einer Nachricht, die in der Datenbank übernommen werden sollen. Jeweils auf 1 MB beschränkt.  <br/> |
|Prüfpunktdatei  <br/> |\*CHK  <br/> |Datensätze, die in Datenbankdateien auf dem Datenträger geschriebene Transaktionen protokolliert haben.  <br/> |
   
Exchange 2013 verwaltet eine einzelne Gruppe von Transaktionsprotokolldateien für jede Datenbank. Die Transaktionsprotokolle sind wichtig für Sicherungs- und Wiederherstellungsvorgänge. Beim Erstellen einer Sicherung oder Wiederherstellen einer Anwendung, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwendet, müssen Sie sicherstellen, dass diese Protokolle ordnungsgemäß verarbeitet werden. Weitere Informationen finden Sie unter [Transaktionsprotokolle und Prüfpunktdateien für die Sicherung und Wiederherstellung in Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md). Zum Sichern einer Datenbank und deren Protokolldatenstrom müssen Sie das komplette Volume mit der Datenbank und den Protokollen sichern. Nach erfolgreichem Abschluss einer vollständigen Sicherung von Volumes oder Ordnern mit einer Exchange-Datenbank wird das Protokoll abgeschnitten.
  
Auf jedem Exchange-Server können Sie jeweils nur eine Wiederherstellungsdatenbank bereitstellen. Sie können mithilfe von Exchange-Verwaltungsshell-Cmdlets wie z. B. **New-MailboxRestoreRequest** auf die Wiederherstellungsdatenbank zugreifen. Weitere Informationen zu Exchange Wiederherstellungsdatenbanken finden Sie unter ["Wiederherstellungsdatenbanken"](https://technet.microsoft.com/library/dd876954%28v=exchg.150%29.aspx) auf TechNet. Weitere Informationen zu Exchange Verwaltungsshell-Cmdlets finden Sie unter [Exchange 2013 Cmdlets](https://technet.microsoft.com/library/bb124413.aspx) on TechNet. 
  
## <a name="circular-logging"></a>Umlaufprotokollierung
<a name="bk_circularlogging"> </a>

Wenn die Speicherkapazität ein Problem darstellt, kann Ihr Administrator die Zirkelprotokollierung aktivieren. Wenn die Zirkelprotokollierung aktiviert ist, schreibt Exchange Transaktionsprotokolle wie gewohnt, aber wenn eine Prüfpunktdatei erweitert ist, wird der inaktive Teil des Transaktionsprotokolls abgeschnitten. Ihr Administrator sollte Exchange 2013-Datenbanken nicht für die Verwendung der Zirkelprotokollierung konfigurieren, wenn Sie auch vss verwenden möchten, um ihre benutzerdefinierten Sicherungs- und Wiederherstellungsvorgänge zu aktivieren. Die Zirkelprotokollierung erstellt die folgenden Einschränkungen: 
  
- Wenn sie während des Sicherungs- oder Wiederherstellungsvorgangs aktiviert ist, können Sie die einzelne Datenbanken nicht wiederherstellen.
    
- Es sind nur Zeitpunkwiederherstellungsvorgänge möglich. Wenn die Zirkelprotokollierung aktiviert ist, können Sie Transaktionsprotokolle im selben Verzeichnis löschen, wenn eine Datenbank wiederhergestellt wird, obwohl diese Protokolle möglicherweise Teil einer anderen Exchange 2013-Datenbank sind. 
    
- Sie können keine inkrementellen und differenziellen Sicherungsvorgänge ausführen. Weitere Informationen zu diesen Sicherungstypen finden Sie unter [Arten von Sicherungsvorgängen für Exchange 2013.](types-of-backup-operations-for-exchange-2013.md)
    
Wenn die Zirkelprotokollierung aktiviert ist, sollte der Administrator sie so schnell wie möglich deaktivieren, um sicherzustellen, dass ihre VSS-Sicherungen nicht fehlschlagen. Weitere Informationen finden Sie im Blogbeitrag [Exchange Circular Logging und VSS Backups.](https://blogs.technet.com/b/exchange/archive/2010/08/18/3410672.aspx) 
  
## <a name="exchange-database-mobility"></a>Exchange-Datenbankmobilität
<a name="bk_exchangedatabasemobility"> </a>

Exchange 2013 ermöglicht die Datenbank-Mobilität, um die Zuverlässigkeit und Verfügbarkeit von Postfächern zu verbessern. Mithilfe der Datenbankmobilität können Sie Kopien Ihrer Exchange-Speicherdatenbank erstellen, die Verbindung zwischen der Datenbank und dem Server trennen und sie auf einem anderen Server speichern. In einer Exchange 2013 Database Availability Group (DAG) werden mehrere Kopien der Datenbank auf verschiedenen Computern gespeichert. Wenn Kopien der Datenbank aufgrund von Hardware- oder anderen Systemausfällen verloren gehen, können die Informationen aus anderen Kopien der Datenbank über gewöhnliche Replikationsvorgänge Seeding für das erneute Seeding verwendet werden.
  
Wenn die zu sichernden Exchange 2013-Datenbanken für Sicherungsvorgänge in einer DAG konfiguriert sind, kann die Sicherungsanwendung Interferenzen zwischen der Momentaufnahme und der Leistung des aktiven Servers besser verhindern, indem sie die Momentaufnahme auf einer der inaktiven Datenbankkopien erstellt. Da die Datenbankkopien in den meisten Fällen synchronisiert werden, kann die Sicherungsanwendung Momentaufnahmen der verschiedenen Datenbankkopien erstellen und die Datenbank später aus den Datenelementen wiederherstellen.
  
Die einzige unterstützte Methode zum Wiederherstellen von DAG-Datenbanken aus Sicherungsdaten besteht darin, alle Kopien der Datenbank unter Verwendung derselben Sicherungsdaten wiederherzustellen. Da die Datenbankprotokolldateien der Kopien geringfügig voneinander abweichen können, kann das Wiederherstellen einzelner Datenbankkopien unter Verwendung unterschiedlicher Daten dazu führen, dass die Datenbank nicht mehr bereitgestellt werden kann.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Transaktionsprotokolle und Prüfpunktdateien für Sicherung und Wiederherstellung in Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Exchange Writer in Exchange 2013](exchange-writer-in-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch

- [Exchange Online- und Exchange-Entwicklung](../exchange-server-development.md) 
- [Arten von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Wiederherstellen Exchange 2013-Datenbanken](restoring-exchange-2013-databases.md)
    

