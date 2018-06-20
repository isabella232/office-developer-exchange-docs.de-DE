---
title: Arten von Sicherungsvorgängen für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 70510902-9583-4177-be3d-afbf757a1ec0
description: Datenbanken, einschließlich vollständige, inkrementelle, kopieren und differenzielle Sicherungen finden Sie Informationen zu den verschiedenen Arten von Sicherungen, dass Sie für Ihre Exchange 2013 ausführen können zu speichern.
ms.openlocfilehash: 588bc0ffe896f286258006f7f123cf09d28b218c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756848"
---
# <a name="types-of-backup-operations-for-exchange-2013"></a>Arten von Sicherungsvorgängen für Exchange 2013

Datenbanken, einschließlich vollständige, inkrementelle, kopieren und differenzielle Sicherungen finden Sie Informationen zu den verschiedenen Arten von Sicherungen, dass Sie für Ihre Exchange 2013 ausführen können zu speichern.
  
**Gilt für:** Exchange Server 2013 
  
Dieser Artikel enthält Informationen zu den verschiedenen Arten von Sicherungen können Sie auf Exchange Server 2013-Datenbanken ausführen und wie diese Backups die Datenbankdateien beeinflussen. 
  
Sicherung und Wiederherstellung von Webanwendungen, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) und der Exchange-Writer verwenden, können in der folgenden Tabelle aufgeführten Sicherungstypen ausführen.
  
**In Tabelle 1. Arten von Sicherungsvorgängen**

|**Sicherungsart**|**Beschreibung**|
|:-----|:-----|
|[Vollständige Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_FullBackups) <br/> |Sichert die Datenbanken (\*EDB), Transaktionsprotokolle (\*.log), Prüfpunktdateien (\*chk), und klicken Sie dann die Transaktionsprotokolle für eine bestimmte Datenbank schneidet.  <br/> |
|[Kopieren Sie Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_CopyBackups) <br/> |Sichert die Datenbank sowie die Transaktionsprotokolle und Prüfpunktdateien. Kopie Sicherungen führen Sie die Transaktionsprotokolle für die Datenbank nicht abgeschnitten.  <br/> |
|[Inkrementelle Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_IncrementalBackups) <br/> |Sichert die Transaktionsprotokolle auf Datensatz Änderungen seit der letzten vollständigen oder inkrementellen Sicherung, und klicken Sie dann kürzt die Transaktionsprotokolle.  <br/> |
|[Differenzielle Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_DifferentialBackups) <br/> |Sichert die Transaktionsprotokolle auf Datensatz Änderungen seit der letzten vollständigen oder inkrementellen Sicherung, und die Transaktionsprotokolle werden nicht abgeschnitten.  <br/> |
   
Die Komponenten oder Datenbankdateien, von der Exchange-Writer definierten darstellen der Datenbank-Datendateien und Transaktionsprotokolle in Exchange 2013-Datenbanken. Dadurch wird die Sicherung und Wiederherstellung Anwendung zum Anzeigen der Namen der Komponenten in einer Exchange 2013-Datenbank während der Sicherungsvorgänge. Ihre backup-Anwendung sichern nicht jedoch einzelne Datenbankkomponenten; Es kann nur ganze Datenbanken sichern. 
  
Der Exchange-Writer standardisiert die Komponente logische Datenbankpfaden, die in der Exchange-Writer-Metadaten angegeben werden. Der Exchange-Writer gibt die logische Pfade für die Anwendung sichern und wiederherstellen, je nach Bedarf.
  
Der Exchange-Writer bietet logische Pfade im Format: 
  
 `logicalPath = "Exchange Server\Microsoft Information Store\<Server name>"`
  
Die Server- und Komponenten sind Komponenten der Datei Gruppe, aber sie müssen keine zugehörigen Dateien. Sie verfügen über Unterkomponenten, die die einzelnen Dateien angeben. Eine Datenbank enthält nur eine Log-Komponente, mit dem Namen Protokolle. Die Namen der Komponenten der einzelnen Datenbank-Komponenten sind die GUIDs der Datenbanken, die als Zeichenfolgen dargestellt. 
  
Der Exchange-Writer werden nur die Datenbanken, die gesichert werden können basierend auf VSS-Framework-Richtlinien aufgelistet. Datenbanken, die bereitgestellt werden, wie die Exchange 2013 Wiederherstellungsdatenbank sowie die Datenbanken, die nicht bereitgestellt werden, können nicht gesichert werden und werden daher nicht in der Exchange-Writer-Metadaten aufgeführt.
  
Die folgende Abbildung zeigt den Exchange-Writer backup-Vorgang. 
  
**Abbildung 1. Abfolge der Ereignisse zum des Sicherungsvorgangs**

![Diagramm der Abfolge von Ereignissen beim Sicherungsprozess. Die Abfolge beginnt mit den Startvorgängen des Exchange-Speichers und setzt sich in zahlreichen Schritten zwischen dem Exchange Writer, VSS und der Clientanwendung fort.](media/VSS_StoreWriterBackup.gif)
  
## <a name="full-backups"></a>Vollständige Sicherungen
<a name="bk_FullBackups"> </a>

Eine vollständige Sicherung der Exchange-Datenbank umfasst das Erstellen und speichern eine Kopie der Datenbankdatei, Transaktionsprotokolle und Prüfpunktdateien. Eine Exchange 2013-Datenbank verfügt über eine Gruppe von dedizierten Transaktionsprotokolldateien.
  
Nachdem die Datenbank gesichert wurde, werden die Transaktionsprotokolldateien auf dem Datenträger, damit nur Datenbank Änderungen, die nach der Sicherung ist aufgetreten bleiben gekürzt. Während dieses Vorgangs löscht der Exchange Writer alle Protokolleinträge bis zu dem Prüfpunkt, basierend auf der Annahme, die die Datenbanken jetzt in einen konsistenten Status, der alle Änderungen gesichert wurden von enthält bis zum letzten Checkpoint. 
  
Wenn die Datenbank gesichert wird während des Sicherungsvorgangs Bereitstellung aufgehoben wird, Exchange 2013 kürzt die Transaktionsprotokolle nicht, und das Ergebnis wird das Äquivalent von einer Kopie Sicherungsvorgang nicht vollständige Sicherungsvorgang. 
  
Wenn eine vollständige Sicherung abgeschlossen ist, werden die Kopfzeilen der aktiven eingebundene Datenbank mit den aktuellen Informationen zur Sicherung aktualisiert. Replizierte Bereitstellungen wird diese Informationen für eine Transaktionsprotokolldatei zugesichert und auf andere DAG Kopien der Datenbank repliziert werden. Kopfzeilen der Datenbankkopien werden aktualisiert, wenn diese Transaktionsprotokolldatei in die Datenbankkopie wiedergegeben wird.
  
Eine vollständige Volumeschattenkopie-Sicherung ist erforderlich, um inkrementelle oder differenzielle Shadow Copy Sicherungen ausführen. Die vollständigen Sicherungen können eine beliebige Kopie entnommen werden, solange es eine Schattenkopie ist backup.
  
Vollständige Sicherungen werden in den folgenden Szenarien verwendet:
  
- Eine Datenbank beschädigt oder geht verloren, aber die Transaktionsprotokolldateien auf dem Datenträger intakt sind. In diesem Szenario können die betroffenen Datenbank-Dateien werden von der vollständigen Sicherung wiederhergestellt, und klicken Sie dann wiederhergestellt durch die Wiedergabe der Transaktionsprotokolle, die noch auf dem Datenträger sind. 
    
- Transaktionsprotokolldateien als auch die Datenbankdatei auf dem Datenträger, gehen verloren. In diesem Szenario werden die Transaktionsprotokolldateien, die zum Zeitpunkt der vollständigen Sicherung gesichert wurden, zusammen mit der Datenbank wiederhergestellt.
    
In Exchange 2013 können Protokolle wiederhergestellt werden, ohne dass Sie die entsprechende Datenbank aus einer vollständigen Sicherung wiederherstellen. Diese Option ermöglicht eine vollständige Sicherung wiederhergestellt werden und in Kombination mit der Transaktionsprotokolldateien aus der aktuellsten vollständigen Sicherung vorwärts bereitzustellen.
  
Wenn die [VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx) -Aufzählung in VSS auf **VSS_BT_FULL** festgelegt ist, wenn der Exchange-Writer eine Sicherung ausgeführt wird, werden die folgenden Komponenten in der Sicherung enthalten: 
  
- Eine Datenbank mit den logischen Pfad Exchange Server Microsoft Information Store\\< Servername\>\\< Datenbank-GUID\> 
    
- Eine Protokolldatei mit den logischen Pfad Exchange Server Microsoft Information Store\\< Servername\>\\< Datenbank-GUID\> 
    
## <a name="copy-backups"></a>Kopieren Sie Sicherungen
<a name="bk_CopyBackups"> </a>

Eine Kopie-Sicherung von Exchange-Datenbanken umfasst das Erstellen und speichern die gleichen Elemente, die bei einer vollständigen Sicherung enthalten sind. Allerdings werden im Gegensatz zu mit einer vollständigen Sicherung, die Transaktionsprotokolldateien auf dem Datenträger nicht abgeschnitten, wenn die Sicherung abgeschlossen ist. Kopie Sicherungen sind nicht für die Wiederherstellung von Daten vorgesehen. Stattdessen bieten Kopie Sicherungen ein Bild der Daten für die Verwendung des Tests, Problemdiagnose, oder für das seeding ein Replikat.
  
Beispielsweise kann ein Exchange 2013-Administrator, der Probleme mit dem Exchange-Speicher eine Kopie backup für die Verwendung in einer testumgebung tätigen, ohne Auswirkungen auf das Produktionssystem. Kopie Sicherungen haben keinen Einfluss auf die reguläre Sicherungszeitpläne; Da eine Kopie-Sicherung auch den Exchange-Speicher Sicherung in Bearbeitung verbraucht, blockiert es andere geplanten Sicherungen anzuhalten, bis die Sicherung abgeschlossen oder abgebrochen wird. 
  
Wenn die [VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx) -Aufzählung in VSS auf **VSS_BT_COPY**festgelegt ist, sind die folgenden Komponenten in einer Sicherung enthalten: 
  
- Eine Datenbank mit den logischen Pfad Exchange Server Microsoft Information Store\\< Servername\>\\< Datenbank-GUID\> 
    
- Eine Komponente des Protokoll-Datei mit den logischen Pfad Exchange Server Microsoft Information Store\\< Servername\>\\< Datenbank-GUID\>
    
## <a name="incremental-backups"></a>Inkrementelle Sicherungen
<a name="bk_IncrementalBackups"> </a>

Bei einer inkrementelle Sicherung einer Exchange 2013-Datenbank speichert Änderungen an der Datenbank, die seit der letzten vollständigen oder inkrementellen Sicherung aufgetreten sind. Wenn die Datenbankdateien und-Protokolldateien auf das System wiederhergestellt werden, können sie in den Zustand wiederhergestellt werden, die zum Zeitpunkt der letzten inkrementellen Sicherung waren. Die Daten aus einer inkrementellen Sicherung enthält nur die Transaktionsprotokolldateien bis zu die aktuelle Uhrzeit. 
  
Wenn die Sicherung abgeschlossen ist, der Exchange-Server kürzt die Protokolldateien und die backup-Zeit in der Datenbank-Kopfzeilen markiert. Verwenden bei einer inkrementelle Sicherung zum Wiederherstellen einer Datenbank erfordert mindestens zwei Datasets wiederhergestellt werden: der letzten vollständigen Sicherung, und klicken Sie dann alle inkrementellen Sicherung seit der letzten vollständigen Sicherung durchgeführt. Der Vorteil inkrementelle Sicherungen ist, dass die einzelnen Sicherungen viel kleiner als eine vollständige Sicherung sind und einzelne inkrementelle Sicherungen häufig kleiner als differenzielle Sicherungen werden. 
  
Der Nachteil inkrementelle Sicherungen von ist, wenn viele inkrementelle Sicherungen zwischen vollständige Sicherungen vorgenommen wurden, Wiederherstellen von Exchange-Speicher beinhalten kann viele inkrementelle Sicherungen wiederherstellen. Exchange lässt nicht bei einer inkrementelle Sicherung auftreten, wenn keine vollständige Sicherung vorhanden ist den Ausgangspunkt für die inkrementellen Änderungen herstellen. 
  
Eine vollständige Sicherung aus einer DAG-Kopierspeicherort kann bei einer inkrementellen Sicherung aus dem aktiven Speicherort und umgekehrt folgen. Eine Einschränkung im Hinterkopf behalten besteht darin, dass der letzte Sicherung Status ist in der aktiven Datenbank Kopfzeile beibehalten, und die Änderungen an der Datenbank-Kopfzeile in Transaktionsprotokolle, repliziert und am Speicherort für die Datenbank Kopie genau wie alle anderen Transaktion wiedergegeben geschrieben werden die Protokolle in der DAG-Bereitstellungen. Da Sicherungen und Wiederherstellungen zusammenarbeiten, backup-Anwendungen bieten die Funktionalität zum Ausführen von Sicherungen ausschließlich auf einem bestimmten DAG-Knoten, unabhängig davon, ob der Knoten aktiv oder passiv, ist als auch zur Ausführung von Sicherungen ausschließlich über den passiven Knoten übergeben oder ausschließlich vom aktiven Knoten.
  
Wenn die [VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx) -Aufzählung in VSS auf **VSS_BT_INCREMENTAL**festgelegt ist, sind die folgenden Komponenten in einer inkrementellen Sicherung enthalten: 
  
- Eine Datenbank mit den logischen Pfad Exchange Server Microsoft Information Store\\< Servername\>\\< Datenbank-GUID\> 
    
- Eine Protokolldatei mit den logischen Pfad Exchange Server Microsoft Information Store\\< Servername\>\\< Datenbank-GUID\>
    
## <a name="differential-backups"></a>Differenzielle Sicherungen
<a name="bk_DifferentialBackups"> </a>

Eine differenzielle Sicherung einer Exchange 2013-Datenbank speichert Änderungen an der Datenbank, die seit der letzten vollständigen oder inkrementellen Sicherung aufgetreten sind. Wenn die Datenbankdateien und-Protokolldateien vom System wiederhergestellt werden, können sie in den Zustand wiederhergestellt werden bei der letzten differenziellen Sicherung wiederhergestellt. 
  
Die Daten aus einer differenziellen Sicherung enthält nur die Transaktionsprotokolldateien bis zu dem aktuellen Prüfpunkt. Differenzielle Sicherungen löschen oder ändern die Protokolldateien oder ändern Sie nicht die Datenbank-Header. Um eine differenzielle Sicherung zum Wiederherstellen einer Datenbank zu verwenden, müssen nur zwei Datasets wiederherstellen: der letzten vollständigen Sicherung, und klicken Sie dann die letzte differenzielle Sicherung. 
  
Der Nachteil differenzielle Sicherungen von ist, dass die differenziellen Sicherungen die gesicherte Duplizieren von Daten in jede Sicherung, bis eine vollständige Sicherung ausgeführt wird. Falls viele differenzielle Sicherungen zwischen vollständige Sicherungen erstellt werden, kann der benötigte Speicherplatz, um die gleiche Anzahl inkrementeller Sicherungen erforderlich überschreiten. Exchange lässt nicht zu einer differenziellen Sicherung auftreten, wenn es wurde keine vollständige oder inkrementelle Sicherung den Ausgangspunkt für differenzielle Sicherungen herstellen.
  
Eine vollständige Sicherung der Kopierspeicherort kann eine differenzielle Sicherung aus dem aktiven Speicherort und umgekehrt folgen. Eine Einschränkung im Hinterkopf behalten besteht darin, dass der letzte Sicherung Status ist in der aktiven Datenbank Kopfzeile beibehalten, und die Änderungen an der Datenbank-Kopfzeile in Transaktionsprotokolle, repliziert und am Speicherort für die Datenbank Kopie genau wie alle anderen Transaktion wiedergegeben geschrieben werden die Protokolle in der DAG-Bereitstellungen. Da Sicherungen und Wiederherstellungen zusammenarbeiten, verfügen backup Applikationen über dieselbe Funktionalität zum Ausführen von Sicherungen alle ausschließlich auf einem bestimmten DAG-Knoten, unabhängig davon, ob der Knoten aktiv oder passiv, ist als auch zur Ausführung von Sicherungen ausschließlich über den passiven Knoten übergeben oder ausschließlich vom aktiven Knoten.
  
Wenn die [VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx) -Aufzählung in VSS auf **VSS_BT_DIFFERENTIAL**festgelegt ist, sind die folgenden Komponenten in einer differenziellen Sicherung enthalten: 
  
- Eine Datenbank mit den logischen Pfad Exchange Server Microsoft Information Store\\< Servername\>\\< Datenbank-GUID\> 
    
- Eine Protokolldatei mit den logischen Pfad Exchange Server Microsoft Information Store\\< Servername\>\\< Datenbank-GUID\>
    
## <a name="see-also"></a>Siehe auch
<a name="bk_AdditionalResources"> </a>

- [Erstellen von Sicherung und Wiederherstellen von Anwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Sicherung und Wiederherstellung Konzepte für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Wiederherstellen von Exchange 2013-Datenbanken](restoring-exchange-2013-databases.md)
    
- [Überprüfen der Integrität mithilfe der API für CHKSGFILES in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Überprüfen der Integrität mithilfe des Dienstprogramms Eseutil in Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    

