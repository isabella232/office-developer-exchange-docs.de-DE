---
title: Arten von Sicherungsvorgängen für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 70510902-9583-4177-be3d-afbf757a1ec0
description: Hier finden Sie Informationen zu den verschiedenen Arten von Sicherungen, die Sie für Ihre Exchange 2013-Speicherdatenbanken ausführen können, einschließlich vollständiger, kopierfähiger, inkrementeller und differenzieller Sicherungen.
ms.openlocfilehash: 79fcdaa40409ee7cac4df44711c1551946b85ca1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520255"
---
# <a name="types-of-backup-operations-for-exchange-2013"></a>Arten von Sicherungsvorgängen für Exchange 2013

Hier finden Sie Informationen zu den verschiedenen Arten von Sicherungen, die Sie für Ihre Exchange 2013-Speicherdatenbanken ausführen können, einschließlich vollständiger, kopierfähiger, inkrementeller und differenzieller Sicherungen.
  
**Gilt für:** Exchange Server 2013 
  
Dieser Artikel enthält Informationen zu den verschiedenen Arten von Sicherungen, die Sie auf Exchange Server 2013-Datenbanken ausführen können, und wie sich diese Sicherungen auf die Datenbankdateien auswirken. 
  
Sicherung und Wiederherstellung von Anwendungen, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) und den Exchange Writer verwenden, können die in der folgenden Tabelle aufgeführten Sicherungstypen ausführen.
  
**Tabelle 1. Arten von Sicherungsvorgängen**

|**Sicherungstyp**|**Beschreibung**|
|:-----|:-----|
|[Vollständige Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_FullBackups) <br/> |Sichert die Datenbanken ( \* .edb), Transaktionsprotokolle ( \* LOG), Prüfpunktdateien ( \* CHK) und abschneidet dann die Transaktionsprotokolle für eine bestimmte Datenbank.  <br/> |
|[Kopieren von Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_CopyBackups) <br/> |Sichert die Datenbank, Transaktionsprotokolle und Prüfpunktdateien. Kopiersicherungen schneiden die Transaktionsprotokolle für die Datenbank nicht ab.  <br/> |
|[Inkrementelle Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_IncrementalBackups) <br/> |Sichert die Transaktionsprotokolle, um Änderungen seit der letzten vollständigen oder inkrementellen Sicherung aufzuzeichnen, und gekürzt dann die Transaktionsprotokolle.  <br/> |
|[Differenzielle Sicherungen](types-of-backup-operations-for-exchange-2013.md#bk_DifferentialBackups) <br/> |Sichert die Transaktionsprotokolle, um Änderungen seit der letzten vollständigen oder inkrementellen Sicherung aufzuzeichnen, und die Transaktionsprotokolle werden nicht abgeschnitten.  <br/> |
   
Die vom Exchange Writer definierten Komponenten oder Datenbankdateien stellen die Datenbankdateien und Transaktionsprotokolle in Exchange 2013-Datenbanken dar. Dadurch kann die Sicherungs- und Wiederherstellungsanwendung die Namen der Komponenten in einer Exchange 2013-Datenbank während sicherungsvorgängen anzeigen. Ihre Sicherungsanwendung kann jedoch einzelne Datenbankkomponenten nicht sichern. Es kann nur ganze Datenbanken sichern. 
  
Der Exchange Writer standardisiert die logischen Pfade der Datenbankkomponente, die in den Exchange Writer-Metadaten angegeben sind. Der Exchange Writer gibt die logischen Pfade zur Sicherungs- und Wiederherstellungsanwendung nach Bedarf zurück.
  
Der Exchange Writer stellt logische Pfade im Formular bereit: 
  
 `logicalPath = "Exchange Server\Microsoft Information Store\<Server name>"`
  
Die Server- und Datenbankkomponenten sind Dateigruppenkomponenten, verfügen jedoch nicht über zugeordnete Dateien. Sie verfügen über Unterkomponenten, die die einzelnen Dateien angeben. Eine Datenbank enthält nur eine Protokollkomponente mit dem Namen "Protokolle". Die Komponentennamen der einzelnen Datenbankkomponenten sind die GUIDs der Datenbanken, die als Zeichenfolgen angezeigt werden. 
  
Der Exchange Writer listet nur Datenbanken auf, die gesichert werden können, basierend auf VSS-Framework-Richtlinien. Datenbanken, die als Exchange 2013-Wiederherstellungsdatenbank bereitgestellt werden, sowie Datenbanken, die nicht bereitgestellt werden, können nicht gesichert werden und sind daher nicht in den Metadaten des Exchange Writers aufgeführt.
  
Die folgende Abbildung zeigt den Exchange Writer-Sicherungsvorgang. 
  
**Abbildung 1. Abfolge von Ereignissen für den Sicherungsvorgang**

![Diagramm der Abfolge von Ereignissen beim Sicherungsprozess. Die Abfolge beginnt mit den Startvorgängen des Exchange-Speichers und setzt sich in zahlreichen Schritten zwischen dem Exchange Writer, VSS und der Clientanwendung fort.](media/VSS_StoreWriterBackup.gif)
  
## <a name="full-backups"></a>Vollständige Sicherungen
<a name="bk_FullBackups"> </a>

Eine vollständige Sicherung einer Exchange Datenbank umfasst das Erstellen und Speichern einer Kopie der Datenbankdatei, transaktionsprotokollen und Prüfpunktdateien. Eine Exchange 2013-Datenbank verfügt über einen Satz dedizierter Transaktionsprotokolldateien.
  
Nachdem die Datenbank gesichert wurde, werden die Transaktionsprotokolldateien auf dem Datenträger abgeschnitten, sodass nur die Datenbankänderungen beibehalten werden, die nach der Sicherung aufgetreten sind. Während dieses Vorgangs löscht der Exchange Writer alle Protokolleinträge bis zum Prüfpunkt, basierend auf der Annahme, dass die Datenbanken jetzt in einem konsistenten Zustand gesichert wurden, der alle Änderungen bis zum letzten Prüfpunkt enthält. 
  
Wenn die Datenbank, die gesichert wird, während des Sicherungsvorgangs nicht bereitgestellt wird, werden die Transaktionsprotokolle Exchange 2013 nicht abgeschnitten, und das Ergebnis entspricht einem Kopiersicherungsvorgang und nicht einem vollständigen Sicherungsvorgang. 
  
Wenn eine vollständige Sicherung abgeschlossen ist, werden die Header der aktiven bereitgestellten Datenbank mit den aktuellen Sicherungsinformationen aktualisiert. In replizierten Bereitstellungen werden diese Informationen in eine Transaktionsprotokolldatei übernommen und in die anderen DAG-Kopien der Datenbank repliziert. Header der Datenbankkopien werden aktualisiert, wenn diese Transaktionsprotokolldatei in der Datenbankkopie wiedergegeben wird.
  
Zum Ausführen inkrementeller oder differenzieller Schattenkopiesicherungen ist eine vollständige Schattenkopiesicherung erforderlich. Die vollständigen Sicherungen können einer beliebigen Kopie entnommen werden, solange es sich um eine Schattenkopie-Sicherung handelt.
  
Vollständige Sicherungen werden in den folgenden Szenarien verwendet:
  
- Eine Datenbank wird beschädigt oder geht verloren, aber die Transaktionsprotokolldateien auf dem Datenträger sind intakt. In diesem Szenario können die betroffenen Datenbankdateien aus der vollständigen Sicherung wiederhergestellt und dann wiederhergestellt werden, indem die Transaktionsprotokolle wiedergegeben werden, die sich noch auf dem Datenträger befinden. 
    
- Transaktionsprotokolldateien sowie die Datenbankdatei auf dem Datenträger gehen verloren. In diesem Szenario werden die Transaktionsprotokolldateien, die zum Zeitpunkt der vollständigen Sicherung gesichert wurden, zusammen mit der Datenbank wiederhergestellt.
    
In Exchange 2013 können Protokolle wiederhergestellt werden, ohne dass die entsprechende Datenbank aus einem vollständigen Sicherungssatz wiederhergestellt werden muss. Mit dieser Option kann eine vorherige vollständige Sicherung wiederhergestellt und mit den Transaktionsprotokolldateien aus der letzten vollständigen Sicherung kombiniert werden, um ein Roll forward durchzuführen.
  
Wenn die [VSS_BACKUP_TYPE-Enumeration](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) in VSS auf **VSS_BT_FULL** festgelegt ist, wenn der Exchange Writer eine Sicherung durchführt, sind die folgenden Komponenten in der Sicherung enthalten: 
  
- Eine Datenbank mit dem logischen Pfad Exchange Server\Microsoft Information Store \\<Servername \> \\<Datenbank-GUID\> 
    
- Eine Protokolldatei mit dem logischen Pfad Exchange Server\Microsoft Information Store \\<Servername \> \\<Datenbank-GUID\> 
    
## <a name="copy-backups"></a>Kopieren von Sicherungen
<a name="bk_CopyBackups"> </a>

Eine Kopiersicherung einer Exchange Datenbank umfasst das Erstellen und Speichern derselben Elemente, die in einer vollständigen Sicherung enthalten sind. Im Gegensatz zu einer vollständigen Sicherung werden die Transaktionsprotokolldateien auf dem Datenträger jedoch nicht abgeschnitten, wenn die Sicherung abgeschlossen ist. Kopiersicherungen sind nicht für Datenwiederherstellungszwecke vorgesehen. Stattdessen stellen Kopiersicherungen ein Bild der Daten für tests, problemdiagnose oder zum Seeding eines Replikats bereit.
  
Beispielsweise kann ein Exchange 2013-Administrator, der Probleme mit dem Exchange Speicher hat, eine Kopiersicherung zur Verwendung in einer Testumgebung erstellen, ohne das Produktionssystem zu beeinträchtigen. Kopiersicherungen wirken sich nicht auf reguläre Sicherungszeitpläne aus. Da eine Kopiersicherung jedoch auch den Exchange Speicher in einen Zustand versetzt, der gerade ausgeführt wird, wird verhindert, dass andere geplante Sicherungen fortgesetzt werden, bis die Kopiersicherung abgeschlossen oder abgebrochen wird. 
  
Wenn die [VSS_BACKUP_TYPE-Enumeration](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) in VSS auf **VSS_BT_COPY** festgelegt ist, sind die folgenden Komponenten in einer Kopiersicherung enthalten: 
  
- Eine Datenbank mit dem logischen Pfad Exchange Server\Microsoft Information Store \\<Servername \> \\<Datenbank-GUID\> 
    
- Eine Protokolldateikomponente mit dem logischen Pfad Exchange Server\Microsoft Information Store \\<Servername \> \\<Datenbank-GUID\>
    
## <a name="incremental-backups"></a>Inkrementelle Sicherungen
<a name="bk_IncrementalBackups"> </a>

Eine inkrementelle Sicherung einer Exchange 2013-Datenbank speichert Änderungen an der Datenbank, die seit der letzten vollständigen oder inkrementellen Sicherung aufgetreten sind. Wenn alle Datenbankdateien und Protokolldateien im System wiederhergestellt werden, können sie in dem Zustand wiederhergestellt werden, in dem sie sich zum Zeitpunkt der letzten inkrementellen Sicherung befanden. Die in einer inkrementellen Sicherung gespeicherten Daten umfassen nur die Transaktionsprotokolldateien bis zum aktuellen Zeitpunkt. 
  
Nach Abschluss der Sicherung werden die Protokolldateien vom Exchange Server abgeschnitten und die Sicherungszeit in den Datenbankheadern markiert. Für die Verwendung einer inkrementellen Sicherung zum Wiederherstellen einer Datenbank müssen mindestens zwei Datensätze wiederhergestellt werden: die letzte vollständige Sicherung und dann jede inkrementelle Sicherung, die nach der letzten vollständigen Sicherung durchgeführt wurde. Der Vorteil der Verwendung inkrementeller Sicherungen besteht darin, dass die einzelnen Sicherungen wesentlich kleiner sind als eine vollständige Sicherung, und einzelne inkrementelle Sicherungen sind häufig kleiner als differenzielle Sicherungen. 
  
Der Nachteil bei der Verwendung inkrementeller Sicherungen besteht darin, dass bei vielen inkrementellen Sicherungen zwischen vollständigen Sicherungen die Wiederherstellung des Exchange Speichers die Wiederherstellung vieler inkrementeller Sicherungen beinhalten kann. Exchange lässt keine inkrementelle Sicherung zu, wenn keine vorherige vollständige Sicherung vorhanden ist, um den Ausgangspunkt für die inkrementellen Änderungen festzulegen. 
  
Auf eine vollständige Sicherung aus einem DAG-Kopierspeicherort kann eine inkrementelle Sicherung vom aktiven Speicherort gefolgt werden und umgekehrt. Eine zu beachtende Einschränkung besteht darin, dass der letzte Sicherungsstatus im Header der aktiven Datenbank beibehalten wird und die Änderungen am Datenbankheader in Transaktionsprotokolle geschrieben, repliziert und am Speicherort der Kopierdatenbank wiedergegeben werden, genau wie alle anderen Transaktionsprotokollen in DAG-Bereitstellungen. Da Sicherungen und Wiederherstellungen interoperiert sind, können Sicherungsanwendungen die Funktionalität bereitstellen, Sicherungen ausschließlich auf einem bestimmten DAG-Knoten auszuführen, unabhängig davon, ob der Knoten aktiv oder passiv ist, sowie Sicherungen ausschließlich vom passiven Knoten oder ausschließlich vom aktiven Knoten aus auszuführen.
  
Wenn die [VSS_BACKUP_TYPE-Enumeration](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) in VSS auf **VSS_BT_INCREMENTAL** festgelegt ist, sind die folgenden Komponenten in einer inkrementellen Sicherung enthalten: 
  
- Eine Datenbank mit dem logischen Pfad Exchange Server\Microsoft Information Store \\<Servername \> \\<Datenbank-GUID\> 
    
- Eine Protokolldatei mit dem logischen Pfad Exchange Server\Microsoft Information Store \\<Servername \> \\<Datenbank-GUID\>
    
## <a name="differential-backups"></a>Differenzielle Sicherungen
<a name="bk_DifferentialBackups"> </a>

Eine differenzielle Sicherung einer Exchange 2013-Datenbank speichert Änderungen an der Datenbank, die seit der letzten vollständigen oder inkrementellen Sicherung aufgetreten sind. Wenn die Datenbankdateien und Protokolldateien vom System wiederhergestellt werden, können sie in dem Zustand wiederhergestellt werden, in dem sie sich bei der letzten differenziellen Sicherung befanden. 
  
Die in einer differenziellen Sicherung gespeicherten Daten umfassen nur die Transaktionsprotokolldateien bis zum aktuellen Prüfpunkt. Differenzielle Sicherungen löschen oder ändern weder die Protokolldateien noch die Datenbankheader. Um eine differenzielle Sicherung zum Wiederherstellen einer Datenbank zu verwenden, müssen Sie nur zwei Datensätze wiederherstellen: die letzte vollständige Sicherung und dann die letzte differenzielle Sicherung. 
  
Der Nachteil bei der Verwendung differenzieller Sicherungen besteht darin, dass die differenziellen Sicherungen die gesicherten Daten in jeder Sicherung duplizieren, bis eine vollständige Sicherung durchgeführt wird. Wenn viele differenzielle Sicherungen zwischen vollständigen Sicherungen durchgeführt werden, kann der erforderliche Speicherplatz den von der gleichen Anzahl inkrementeller Sicherungen benötigten Speicherplatz überschreiten. Exchange lässt keine differenzielle Sicherung zu, wenn keine vollständige oder inkrementelle Sicherung zum Einrichten des Ausgangspunkts für differenzielle Sicherungen vorhanden ist.
  
Auf eine vollständige Sicherung aus dem Kopierspeicherort kann eine differenzielle Sicherung vom aktiven Speicherort gefolgt werden und umgekehrt. Eine zu beachtende Einschränkung besteht darin, dass der letzte Sicherungsstatus im Header der aktiven Datenbank beibehalten wird und die Änderungen am Datenbankheader in Transaktionsprotokolle geschrieben, repliziert und am Speicherort der Kopierdatenbank wiedergegeben werden, genau wie alle anderen Transaktionsprotokollen in DAG-Bereitstellungen. Da Sicherungen und Wiederherstellungen interoperator sind, bieten Sicherungsanwendungen die Funktionalität, alle Sicherungen ausschließlich auf einem bestimmten DAG-Knoten auszuführen, unabhängig davon, ob der Knoten aktiv oder passiv ist, sowie Sicherungen ausschließlich vom passiven Knoten oder ausschließlich vom aktiven Knoten aus auszuführen.
  
Wenn die [VSS_BACKUP_TYPE-Enumeration](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx) in VSS auf **VSS_BT_DIFFERENTIAL** festgelegt ist, sind die folgenden Komponenten in einer differenziellen Sicherung enthalten: 
  
- Eine Datenbank mit dem logischen Pfad Exchange Server\Microsoft Information Store \\<Servername \> \\<Datenbank-GUID\> 
    
- Eine Protokolldatei mit dem logischen Pfad Exchange Server\Microsoft Information Store \\<Servername \> \\<Datenbank-GUID\>
    
## <a name="see-also"></a>Siehe auch
<a name="bk_AdditionalResources"> </a>

- [Erstellen von Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Wiederherstellen Exchange 2013-Datenbanken](restoring-exchange-2013-databases.md)
    
- [Überprüfen der Sicherungsintegrität mithilfe der CHKSGFILES-API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Überprüfen der Sicherungsintegrität mithilfe des Eseutil-Tools in Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    

