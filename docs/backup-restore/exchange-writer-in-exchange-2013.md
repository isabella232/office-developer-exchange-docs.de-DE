---
title: Exchange-Writer in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ec126433-9f0a-46ec-a685-ff4af2f97bc1
description: Hier finden Sie Informationen zu den Exchange Writer in Exchange 2013 für die Sicherung und Wiederherstellung.
ms.openlocfilehash: a4dc5963ab24a83969efc6e425b38a35276f3aa3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756800"
---
# <a name="exchange-writer-in-exchange-2013"></a>Exchange-Writer in Exchange 2013

Hier finden Sie Informationen zu den Exchange Writer in Exchange 2013 für die Sicherung und Wiederherstellung. 
  
**Gilt für:** Exchange Server 2013 
  
Der Exchange-Writer ist verantwortlich für die Sicherung und Wiederherstellung von aktiven Datenbanken von Exchange Server 2013. Der Exchange-Writer unterstützt auch backup-Funktionen für eine ausgewählte Datenbank, in dem die Schattenkopie gegen die replizierten Instanz von Datenbank- und Transaktionsprotokolldateien Protokolldateien erstellt wird. 
  
## <a name="overview-of-the-exchange-writer"></a>Übersicht über die Exchange-writer
<a name="bk_Overview"> </a>

Exchange 2013 enthält Datenbank-Mobilitätsfunktionen, die Datenbanken zwischen verschiedenen Exchange-Servern zur Verbesserung der datenbankverfügbarkeit und ausfallsicherheit von Standorten repliziert werden können. Andere Datenbankkopien in einer Database Availability Groups (DAG) bieten eine Möglichkeit für Exchange-Sicherungen, die zusätzlichen Ressourcen verwenden, die an der Position kopieren verfügbar sind. Darüber hinaus, da die Kopie anstelle des Master-aktive Datenbank gesichert haben, kann die Kopie während der Sicherung für einen längeren Zeitraum nicht verfügbar. 
  
Der Exchange-Writer in Koordination mit der Exchange-Webdienste (in Betrieb im Namen der anfordernden Person) die Datenbankdateien für die Sicherung vorbereiten, Fixieren der e/a-Aktivitätsfeeds entsteht Exchange Transaktionen vor dem Sichern der Datenbank, und klicken Sie dann aufzuheben und Abschneiden nach Abschluss die Sicherung die Protokolldateien.
  
Während einer Wiederherstellung weist die Anwendung sichern und Wiederherstellen den Exchange-Writer, überprüfen Sie die Wiederherstellungsziele, benennen Sie die Datenbankdatei bei Bedarf, und klicken Sie dann die Transaktion wiedergeben, um mit dem Exchange-Speicher (in Betrieb im Namen der anfordernden Person) zu koordinieren Protokolle nach Bedarf. Der Exchange-Writer unterstützt Sicherungen und Wiederherstellungen.
  
Der Exchange-Writer ist verfügbar auf allen Exchange-Servern, die die Postfach-Serverrolle installiert ist. 
  
## <a name="exchange-writer-configuration-settings"></a>Exchange-Writer-Konfigurationseinstellungen
<a name="bk_ExchangeWriterConfig"> </a>

Der Exchange-Writer für VSS verwendet eine Vielzahl von Einstellungen und Werte, die richtig eingestellt und während der Sicherung und Wiederherstellung beibehalten werden müssen. Diese Konfigurationseinstellungen werden in Exchange Writer-Metadatendokument gespeichert. Wenn Ihre backup-Anwendung diese Einstellungen nicht beibehalten wird, können unerwartete Fehler auftreten, wenn Sie versuchen, um Ihre Exchange-Datenbanken zu sichern. 
  
Die folgende Tabelle enthält die VSS-Schnittstellen, die Metadaten für die Komponenten Ihrer Datenbank Sicherung verfügbar machen. Diese Schnittstellen werden benötigt, um die Exchange-Writer-Metadatendokument abrufen, die zum Ausführen einer Exchange-Speicher verwendet wird.
  
**In Tabelle 1. VSS-Schnittstellen**

|**VSS-Schnittstelle**|**Beschreibung**|
|:-----|:-----|
|IVssWMComponent  <br/> |Ermöglicht den Zugriff auf die in der Exchange-Writer gespeicherten Komponenteninformationen.  <br/> |
|IVssExamineWriterMetadata  <br/> |Ermöglicht die anfordernde sichern und Wiederherstellen der Anwendung zur Untersuchung der Metadaten von der Exchange-Writer. Exchange Writer-Metadatendokument enthält Exchange 2013-spezifischen Werte und Parameter, die die anfordernde sichern und Wiederherstellen der Anwendung benötigt, damit es ordnungsgemäß die geeigneten Komponenten für die Sicherung angeben kann.  <br/> |
|IVssComponent  <br/> |Enthält Methoden für das Überprüfen und Ändern von Informationen zu in einer Requester Sicherung Komponenten Dokument enthaltenen Komponenten. Objekte können nur für diese Komponenten abgerufen werden, die explizit zu diesem Dokument von der [IVssBackupComponents::AddComponent](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382646%28v=vs.85%29.aspx) -Methode hinzugefügt wurden.  <br/> |
|IVssBackupComponents  <br/> |Wird von der anfordernden Anwendung sichern und Wiederherstellen den Exchange-Writer über Dateistatus Abfragen und zum Ausführen von sicherungs- und Wiederherstellungsvorgängen verwendet. Die [IVssBackupComponents::SetBackupState](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382833%28v=vs.85%29.aspx) -Methode definiert, ob der Sicherungsvorgang eine vollständige, Kopie, inkrementell oder differenzielle Sicherung. Die [IVssBackupComponents::AddRestoreSubcomponent](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382649%28v=vs.85%29.aspx) -Methode definiert die Unterkomponenten einer Exchange 2013-Datenbank, die für den Wiederherstellungsvorgang ausgewählt werden können.  <br/> |
   
Windows Server-Dateisystem eine Exchange 2013-Datenbank gespeichert ist, als eine einzelne Datenbank-Datei mit der Erweiterung *Edb. Der Exchange-Writer macht die *EDB als Datenbankkomponente, während der Transaktionsprotokolle (*.log) und Prüfpunktdateien (* chk) in einer einzelnen Komponente als die Log-Komponente bezeichnet kombiniert werden. Weitere Informationen zu Exchange-Datenbankdateien finden Sie unter [Sichern und Wiederherstellen Konzepte für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md).
  
## <a name="interactions-between-the-exchange-writer-vss-and-vss-requesters"></a>Interaktionen zwischen den Exchange-Writer, VSS und VSS anfordernden Personen
<a name="bk_interactions"> </a>

Die allgemeinen Interaktion zwischen den VSS, der Exchange-Verfasser und Exchange 2013 während Sicherungsvorgängen lautet wie folgt:
  
1. Vom Sicherungsprogramm (oder Agent) wird ein geplanter Auftrag ausgeführt. 
    
2. Der VSS-anforderer in der Anwendung sichern und Wiederherstellen sendet einen Befehl an VSS zu einer Schattenkopie der ausgewählten Exchange 2013-Datenbanken. 
    
3. VSS kommuniziert mit den Exchange-Writer für eine Snapshot-Sicherung vorbereiten. Exchange 2013 verbietet administrative Aktionen für die Datenbanken, Volumeabhängigkeiten überprüft und hält alle Schreibvorgänge auf ausgewählte Instanz der Protokolldateien Datenbank- und Transaktionsprotokolldateien wobei schreibgeschützten Zugriff. 
    
4. VSS kommuniziert mit dem entsprechenden Speicheranbieter eine Schattenkopie des Speichervolumes zu erstellen, die Exchange 2013-Datenbanken enthält. 
    
5. VSS gibt Exchange 2013, um die normalen Vorgänge fortzusetzen. 
    
6. Der VSS-Requester überprüft, ob die physische Konsistenz von den Sicherungssatz vor dem signalisieren, dass die Sicherung erfolgreich war. Exchange 2013 kürzt die Transaktionsprotokolle (wenn die Datenbank Teil einer DAG ist, Abschneiden des Protokolls wird repliziert zwischen alle Kopien) und die Uhrzeit der letzten Sicherung für die Datenbank aufgezeichnet.
    
VSS serialisiert anfordernden Personen Interaktion mit dem Exchange-Writer beginnt mit der [OnPrepareBackup](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381571%28v=vs.85%29.aspx) -Methode und endet mit der [OnPostSnapshot](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381568%28v=vs.85%29.aspx) -Methode. In der Regel erfolgt der größten Teil der Exchange-Writer arbeiten mit der Schattenkopie verbringt Zeit nach der Methode **OnPostSnapshot** , wenn die Konsistenz der Schattenkopie vor dem Abschluss von Sicherungen überprüft wird. Der Exchange-Writer unterstützt parallele Sicherungen zwischen **OnPostSnapshot** und [OnBackupComplete](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381557%28v=vs.85%29.aspx).
  
Exchange 2013 zulässig gleichzeitige Sicherungen von derselben Datenbank nicht. Nur einen Sicherungsauftrag kann für eine bestimmte Datenbank auf einmal ausgeführt. Wenn die Sicherung ausgeführt wird, versetzt Exchange-Speicher die Datenbank im Zustand Sicherung in Bearbeitung. Dieser Status im Arbeitsspeicher deaktiviert ist, entweder nach Abschluss des Sicherungsvorgangs oder der Dienst neu gestartet wird. Den Status der in-Memory-Sicherung in Bearbeitung und die zugehörigen Daten gehen verloren, wenn der Dienst, der den Exchange-Writer hostet, neu gestartet wird, wenn das Betriebssystem neu gestartet wird oder wenn ein Clusterfailover auftritt. Eines dieser Ereignisse wird den Sicherungsauftrag Fehler verursacht.
  
Sicherung initiiert Transaktion abgeschnittene Datei wird ausgelöst, basierend auf die Art der Sicherung ausgeführt werden. In nicht-DAG-Konfigurationen werden der Exchange-Writer die Transaktionsprotokolldateien nach Abschluss der erfolgreichen vollständigen oder inkrementellen Sicherung abgeschnitten. In DAG repliziert Konfigurationen, Abschneiden des Protokolls wird vom Replikationsdienst verzögert, bis alle erforderlichen Protokolldateien in alle anderen Kopien wiedergegeben werden. Der Replikationsdienst werden die gesicherten Protokolldateien gelöscht, die aus der aktiv sind und die Kopie Dateipfade melden, nachdem sie überprüft, ob die Protokolldateien erfolgreich auf der Kopie und sowohl aktive Datenbank angewendet wurden und die Kopien Prüfpunkts verstrichen ist die Protokolldateien gelöscht werden soll.
  
## <a name="see-also"></a>Siehe auch

- [Transaktionsprotokolle und Prüfpunktdateien für Sicherung und Wiederherstellung in Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Sicherung und Wiederherstellung Konzepte für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

