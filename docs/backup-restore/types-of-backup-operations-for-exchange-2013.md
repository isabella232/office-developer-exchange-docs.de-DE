---
title: Arten von Sicherungsvorgängen für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 70510902-9583-4177-be3d-afbf757a1ec0
description: Hier finden Sie Informationen zu den verschiedenen Arten von Sicherungen, die Sie für Ihre Exchange 2013 Store-Datenbanken ausführen können, einschließlich vollständiger, Kopie, inkrementeller und differenzieller Sicherungen.
ms.openlocfilehash: dd07226acb3a3bb055e98f861a5c01375ee50dda
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456287"
---
# <a name="types-of-backup-operations-for-exchange-2013"></a>Arten von Sicherungsvorgängen für Exchange 2013

Hier finden Sie Informationen zu den verschiedenen Arten von Sicherungen, die Sie für Ihre Exchange 2013 Store-Datenbanken ausführen können, einschließlich vollständiger, Kopie, inkrementeller und differenzieller Sicherungen.
  
**Gilt für:** Exchange Server 2013 
  
Dieser Artikel enthält Informationen zu den verschiedenen Sicherungstypen, die Sie für Exchange Server 2013 Datenbanken ausführen können, und darüber, wie sich diese Sicherungen auf die Datenbankdateien auswirken. 
  
Sicherungs-und Wiederherstellungsanwendungen, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) und den Exchange-Writer verwenden, können die in der folgenden Tabelle aufgeführten Sicherungstypen ausführen.
  
**Tabelle 1. Arten von Sicherungsvorgängen**

|**Sicherungstyp**|**Beschreibung**|
|:-----|:-----|
|[Vollständige Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_FullBackups) <br/> |Sichert die Datenbanken ( \* EDB), Transaktionsprotokolle ( \* Log), Prüfpunktdateien ( \* chk) und schneidet dann die Transaktionsprotokolle für eine bestimmte Datenbank ab.  <br/> |
|[Kopieren von Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_CopyBackups) <br/> |Sichert die Datenbank, Transaktionsprotokolle und Prüfpunktdateien. Durch Kopieren von Sicherungen werden die Transaktionsprotokolle für die Datenbank nicht abgeschnitten.  <br/> |
|[Inkrementelle Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_IncrementalBackups) <br/> |Sichert die Transaktionsprotokolle, um Änderungen seit der letzten vollständigen oder inkrementellen Sicherung aufzuzeichnen, und schneidet dann die Transaktionsprotokolle ab.  <br/> |
|[Differenzielle Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_DifferentialBackups) <br/> |Sichert die Transaktionsprotokolle, um Änderungen seit der letzten vollständigen oder inkrementellen Sicherung aufzuzeichnen, und schneidet die Transaktionsprotokolle nicht ab.  <br/> |
   
Die vom Exchange-Writer definierten Komponenten oder Datenbankdateien stellen die Datenbankdateien und Transaktionsprotokolle in Exchange 2013 Datenbanken dar. Dadurch können Ihre Sicherungs-und Wiederherstellungsanwendung die Namen der Komponenten in einer Exchange 2013 Datenbank während Sicherungsvorgängen anzeigen. Ihre Sicherungsanwendung kann jedoch nicht einzelne Datenbankkomponenten sichern; Es kann nur ganze Datenbanken sichern. 
  
Der Exchange-Writer standardisiert die logischen Pfade der Datenbankkomponente, die in den Exchange-Writer-Metadaten angegeben sind. Der Exchange-Writer gibt die logischen Pfade zu ihrer Sicherungs-und Wiederherstellungsanwendung nach Bedarf zurück.
  
Der Exchange-Writer stellt logische Pfade im folgenden Format bereit: 
  
 `logicalPath = "Exchange Server\Microsoft Information Store\<Server name>"`
  
Die Server-und Datenbankkomponenten sind Dateigruppen Komponenten, die jedoch keine zugeordneten Dateien aufweisen. Sie verfügen über unter Komponenten, die die einzelnen Dateien angeben. Eine Datenbank enthält nur eine Protokollkomponente namens Logs. Die Komponentennamen der einzelnen Datenbankkomponenten sind die GUIDs der Datenbanken, die als Zeichenfolgen angezeigt werden. 
  
Der Exchange-Writer listet nur Datenbanken auf, die auf der Grundlage von VSS-Framework-Richtlinien gesichert werden können. Datenbanken, die als Exchange 2013 Wiederherstellungsdatenbank bereitgestellt werden, sowie Datenbanken, die nicht bereitgestellt wurden, können nicht gesichert werden und werden daher nicht in den Metadaten des Exchange-Writers aufgeführt.
  
In der folgenden Abbildung ist der Exchange Writer-Sicherungsvorgang dargestellt. 
  
**Abbildung 1. Abfolge der Ereignisse für den Sicherungsvorgang**

![Diagramm der Abfolge von Ereignissen beim Sicherungsprozess. Die Abfolge beginnt mit den Startvorgängen des Exchange-Speichers und setzt sich in zahlreichen Schritten zwischen dem Exchange Writer, VSS und der Clientanwendung fort.](media/VSS_StoreWriterBackup.gif)
  
## <a name="full-backups"></a>Vollständige Sicherungen
<a name="bk_FullBackups"> </a>

Eine vollständige Sicherung einer Exchange-Datenbank umfasst das Erstellen und Speichern einer Kopie der Datenbankdatei, der Transaktionsprotokolle und der Prüfpunktdateien. Eine Exchange 2013 Datenbank verfügt über einen Paket dedizierter Transaktionsprotokolldateien.
  
Nachdem die Datenbank gesichert wurde, werden die Transaktionsprotokolldateien auf dem Datenträger abgeschnitten, sodass nur Datenbankänderungen verbleiben, die nach dem Erstellen der Sicherung stattgefunden haben. Während dieses Vorgangs löscht der Exchange-Writer alle Protokolleinträge bis zum Prüfpunkt, basierend auf der Annahme, dass die Datenbanken nun in einem konsistenten Zustand gesichert wurden, der alle Änderungen bis zum letzten Prüfpunkt enthält. 
  
Wenn die Bereitstellung der zu sichernden Datenbank während des Sicherungsvorgangs aufgehoben wird, schneidet Exchange 2013 die Transaktionsprotokolle nicht ab, und das Ergebnis entspricht einem Sicherungsvorgang kopieren und nicht einem vollständigen Sicherungsvorgang. 
  
Wenn eine vollständige Sicherung abgeschlossen ist, werden die Kopfzeilen der aktiven bereitgestellten Datenbank mit den aktuellen Sicherungsinformationen aktualisiert. In replizierten Bereitstellungen werden diese Informationen in eine Transaktionsprotokolldatei übernommen und auf die anderen DAG-Kopien der Datenbank repliziert. Kopfzeilen der Datenbankkopien werden aktualisiert, wenn diese Transaktionsprotokolldatei in die Datenbankkopie wiedergegeben wird.
  
Eine vollständige Shadow Copy-Sicherung ist erforderlich, um inkrementelle oder differenzielle Shadow Copy-Sicherungen auszuführen. Die vollständigen Sicherungen können aus jeder Kopie entnommen werden, solange es sich um eine Shadow Copy-Sicherung handelt.
  
Vollständige Sicherungen werden in den folgenden Szenarien verwendet:
  
- Eine Datenbank wird beschädigt oder geht verloren, die Transaktionsprotokolldateien auf dem Datenträger sind jedoch intakt. In diesem Szenario können die betroffenen Datenbankdateien aus der vollständigen Sicherung wiederhergestellt und dann durch erneutes Abspielen der Transaktionsprotokolle wiederhergestellt werden, die sich noch auf dem Datenträger befinden. 
    
- Transaktionsprotokolldateien, sowie die Datenbankdatei auf dem Datenträger, gehen verloren. In diesem Szenario werden die Transaktionsprotokolldateien, die zum Zeitpunkt der vollständigen Sicherung gesichert wurden, zusammen mit der Datenbank wiederhergestellt.
    
In Exchange 2013 können Protokolle wiederhergestellt werden, ohne dass die zutreffende Datenbank aus einem vollständigen Sicherungssatzes wiederhergestellt werden muss. Mit dieser Option ist es möglich, eine vorherige vollständige Sicherung wiederherzustellen und mit den Transaktionsprotokolldateien der letzten vollständigen Sicherung zu kombinieren, um einen Rollforward durchführen zu können.
  
Wenn die [VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) -Aufzählung in VSS auf **VSS_BT_FULL** festgelegt ist, wenn der Exchange-Writer eine Sicherung ausführt, sind die folgenden Komponenten in der Sicherung enthalten: 
  
- Eine Datenbank mit dem logischen Pfad Exchange Server\Microsoft-Informationsspeicher \\<Server Name \> \\<Daten Bank GUID\> 
    
- Eine Protokolldatei mit dem logischen Pfad Exchange Server\Microsoft Information Store \\<Server Name \> \\<Database GUID\> 
    
## <a name="copy-backups"></a>Kopieren von Sicherungen
<a name="bk_CopyBackups"> </a>

Bei einer Kopie-Sicherung einer Exchange-Datenbank müssen dieselben Elemente erstellt und gespeichert werden, die in einer vollständigen Sicherung enthalten sind. Im Gegensatz zu einer vollständigen Sicherung werden die Transaktionsprotokolldateien auf dem Datenträger jedoch nicht abgeschnitten, wenn die Sicherung abgeschlossen ist. Sicherungskopien sind nicht für Daten Wiederherstellungszwecke vorgesehen. Stattdessen stellen Sicherungskopien ein Abbild der Daten bereit, die zum Testen, zur Problemdiagnose oder zum Seeding eines Replikats verwendet werden können.
  
Beispielsweise kann ein Exchange 2013 Administrator, bei dem Probleme mit dem Exchange-Informationsspeicher auftreten, eine Kopie-Sicherung für die Verwendung in einer Testumgebung erstellen, ohne dass sich dies auf das Produktionssystem auswirkt. Kopien von Sicherungen wirken sich nicht auf reguläre Sicherungszeitpläne aus; Da eine Kopie-Sicherung auch die Exchange-Informationsspeicher in einen Status der Sicherung in Bearbeitung versetzt, werden andere geplante Sicherungen erst dann blockiert, wenn die Kopie-Sicherung abgeschlossen oder abgebrochen wurde. 
  
Wenn die [VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) -Aufzählung in VSS auf **VSS_BT_COPY**festgelegt ist, sind die folgenden Komponenten in einer Kopie-Sicherung enthalten: 
  
- Eine Datenbank mit dem logischen Pfad Exchange Server\Microsoft-Informationsspeicher \\<Server Name \> \\<Daten Bank GUID\> 
    
- Eine Protokolldatei Komponente mit dem logischen Pfad Exchange Server\Microsoft-Informationsspeicher \\<Server Name \> \\<Daten Bank GUID\>
    
## <a name="incremental-backups"></a>Inkrementelle Sicherungen
<a name="bk_IncrementalBackups"> </a>

Bei einer inkrementellen Sicherung einer Exchange 2013 Datenbank werden Änderungen an der Datenbank gespeichert, die seit der letzten vollständigen oder inkrementellen Sicherung aufgetreten sind. Wenn alle Datenbankdateien und Protokolldateien im System wiederhergestellt werden, können Sie in dem Zustand wiederhergestellt werden, in dem Sie sich zum Zeitpunkt der letzten inkrementellen Sicherung befanden. Die in einer inkrementellen Sicherung gespeicherten Daten umfassen nur die Transaktionsprotokolldateien bis zur aktuellen Uhrzeit. 
  
Nach Abschluss der Sicherung schneidet der Exchange-Server die Protokolldateien ab und markiert die Sicherungszeit in den Datenbankkopfzeilen. Bei Verwendung einer inkrementellen Sicherung zum Wiederherstellen einer Datenbank müssen mindestens zwei Datensätze wiederhergestellt werden: die letzte vollständige Sicherung und dann jede inkrementelle Sicherung, die nach der letzten vollständigen Sicherung ausgeführt wurde. Der Vorteil der Verwendung von inkrementellen Sicherungen liegt darin, dass die einzelnen Sicherungen viel kleiner als eine vollständige Sicherung sind und dass einzelne inkrementelle Sicherungen häufig kleiner als differenzielle Sicherungen sind. 
  
Der Nachteil bei der Verwendung von inkrementellen Sicherungen besteht darin, dass bei der Wiederherstellung von Exchange-Informationsspeicher möglicherweise viele inkrementelle Sicherungen wiederhergestellt werden, wenn zwischen vollständigen Sicherungen viele inkrementelle Sicherungen vorgenommen wurden. Exchange lässt nicht zu, dass eine inkrementelle Sicherung durchgeführt wird, wenn keine vorherige vollständige Sicherung vorhanden ist, um den Ausgangspunkt für die inkrementellen Änderungen festzulegen. 
  
Eine vollständige Sicherung, die von einem Speicherort der DAG-Kopie entnommen wurde, kann durch eine inkrementelle Sicherung vom aktiven Speicherort gefolgt werden und umgekehrt. Eine Einschränkung ist, dass der letzte Sicherungsstatus im Header der aktiven Datenbank beibehalten wird und die Änderungen an der Datenbankkopfzeile in Transaktionsprotokolle geschrieben, repliziert und am Speicherort der Kopie-Datenbank wiedergegeben werden, genauso wie alle anderen Transaktionsprotokolle in DAG-Bereitstellungen. Da Sicherungen und Wiederherstellungen zusammenarbeiten, können Sicherungsanwendungen die Funktionen zum Ausführen von Sicherungen ausschließlich auf einem bestimmten DAG-Knoten bereitstellen, unabhängig davon, ob der Knoten aktiv oder passiv ist, sowie um Sicherungen ausschließlich aus dem passiven Knoten oder ausschließlich aus dem aktiven Knoten auszuführen.
  
Wenn die [VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) -Aufzählung in VSS auf **VSS_BT_INCREMENTAL**festgelegt ist, sind die folgenden Komponenten in einer inkrementellen Sicherung enthalten: 
  
- Eine Datenbank mit dem logischen Pfad Exchange Server\Microsoft-Informationsspeicher \\<Server Name \> \\<Daten Bank GUID\> 
    
- Eine Protokolldatei mit dem logischen Pfad Exchange Server\Microsoft Information Store \\<Server Name \> \\<Database GUID\>
    
## <a name="differential-backups"></a>Differenzielle Sicherungen
<a name="bk_DifferentialBackups"> </a>

Eine differenzielle Sicherung einer Exchange 2013 Datenbank speichert Änderungen an der Datenbank, die seit der letzten vollständigen oder inkrementellen Sicherung aufgetreten sind. Wenn die Datenbankdateien und Protokolldateien vom System wiederhergestellt werden, können Sie in dem Zustand wiederhergestellt werden, in dem Sie sich bei der letzten differenziellen Sicherung befanden. 
  
Die in einer differenziellen Sicherung gespeicherten Daten umfassen nur die Transaktionsprotokolldateien bis zum aktuellen Prüfpunkt. Differenzielle Sicherungen löschen oder ändern nicht die Protokolldateien oder ändern die Datenbankheader. Um eine differenzielle Sicherung zum Wiederherstellen einer Datenbank zu verwenden, müssen Sie nur zwei Datensätze wiederherstellen: die letzte vollständige Sicherung und dann die neueste differenzielle Sicherung. 
  
Der Nachteil bei der Verwendung von differenziellen Sicherungen besteht darin, dass die gesicherten Daten in jeder Sicherung durch die differenziellen Sicherungen dupliziert werden, bis eine vollständige Sicherung ausgeführt wird. Wenn zahlreiche differenzielle Sicherungen zwischen vollständigen Sicherungen vorgenommen werden, kann der erforderliche Speicherplatz die gleiche Anzahl von inkrementellen Sicherungen überschreiten. Exchange lässt keine differenzielle Sicherung zu, wenn keine vollständige oder inkrementelle Sicherung durchgeführt wurde, um den Ausgangspunkt für differenzielle Sicherungen festzulegen.
  
Einer vollständigen Sicherung, die vom Speicherort der Kopie entnommen wurde, kann eine differenzielle Sicherung vom aktiven Speicherort gefolgt werden und umgekehrt. Eine Einschränkung ist, dass der letzte Sicherungsstatus im Header der aktiven Datenbank beibehalten wird und die Änderungen an der Datenbankkopfzeile in Transaktionsprotokolle geschrieben, repliziert und am Speicherort der Kopie-Datenbank wiedergegeben werden, genauso wie alle anderen Transaktionsprotokolle in DAG-Bereitstellungen. Da Sicherungen und Wiederherstellungen zusammenarbeiten, bieten Sicherungsanwendungen die Funktionalität zum Ausführen aller Sicherungen ausschließlich auf einem bestimmten DAG-Knoten an, unabhängig davon, ob der Knoten aktiv oder passiv ist, sowie zum Ausführen von Sicherungen ausschließlich aus dem passiven Knoten oder ausschließlich aus dem aktiven Knoten.
  
Wenn die [VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) -Aufzählung in VSS auf **VSS_BT_DIFFERENTIAL**festgelegt ist, sind die folgenden Komponenten in einer differenziellen Sicherung enthalten: 
  
- Eine Datenbank mit dem logischen Pfad Exchange Server\Microsoft-Informationsspeicher \\<Server Name \> \\<Daten Bank GUID\> 
    
- Eine Protokolldatei mit dem logischen Pfad Exchange Server\Microsoft Information Store \\<Server Name \> \\<Database GUID\>
    
## <a name="see-also"></a>Siehe auch
<a name="bk_AdditionalResources"> </a>

- [Erstellen von Sicherungs-und Wiederherstellungsanwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Wiederherstellen Exchange 2013 Datenbanken](restoring-exchange-2013-databases.md)
    
- [Überprüfen der Integrität der Sicherung mithilfe der CHKSGFILES-API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Überprüfen der Integrität der Sicherung mithilfe des Tools "Eseutil" in Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    

