---
title: Exchange Writer in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ec126433-9f0a-46ec-a685-ff4af2f97bc1
description: Hier finden Sie Informationen zum Exchange-Writer in Exchange 2013 für Sicherungs-und Wiederherstellungsvorgänge.
ms.openlocfilehash: 44270a87c38b08d274d389fa6e46f3864da13ed2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452888"
---
# <a name="exchange-writer-in-exchange-2013"></a>Exchange Writer in Exchange 2013

Hier finden Sie Informationen zum Exchange-Writer in Exchange 2013 für Sicherungs-und Wiederherstellungsvorgänge. 
  
**Gilt für:** Exchange Server 2013 
  
Der Exchange-Writer ist für die Sicherung und Wiederherstellung aktiver Exchange Server 2013 Datenbanken verantwortlich. Der Exchange-Writer unterstützt auch Sicherungsfunktionen für eine ausgewählte Datenbank, in der die Schattenkopie der replizierten Instanz der Datenbank-und Transaktionsprotokolldateien entnommen wird. 
  
## <a name="overview-of-the-exchange-writer"></a>Übersicht über den Exchange-Writer
<a name="bk_Overview"> </a>

Exchange 2013 umfasst Daten Bank Mobilitätsfeatures, mit denen Datenbanken zwischen verschiedenen Exchange-Servern repliziert werden können, um die Datenbankverfügbarkeit und Ausfallsicherheit von Standorten zu verbessern. Die anderen Datenbankkopien in einer Database Availability Group (DAG) bieten eine wertvolle Gelegenheit für Exchange-Sicherungen, die zusätzlichen Ressourcen zu verwenden, die am Speicherort der Kopie zur Verfügung stehen. Darüber hinaus kann die Kopie während der Sicherung für einen längeren Zeitraum nicht verfügbar sein, da die Kopie statt des aktiven Daten Bank Masters gesichert wird. 
  
Der Exchange-Writer koordiniert die Exchange-Dienste (im Auftrag des anfordernden Betriebs), um die Datenbankdateien auf Sicherungen vorzubereiten, die e/a-Aktivität, die sich aus Exchange-Transaktionen ergibt, vor dem Sichern der Datenbank zu fixieren und anschließend die Fixierung und das Abschneiden von Protokolldateien nach Abschluss der Sicherung aufzuheben.
  
Während einer Wiederherstellung weist die Sicherungs-und Wiederherstellungsanwendung den Exchange-Writer an, sich mit dem Exchange-Informationsspeicher zu koordinieren (im Auftrag des anfordernden Benutzers), die Wiederherstellungsziele zu überprüfen, die Datenbankdatei gegebenenfalls umzubenennen und die Transaktionsprotokolle nach Bedarf wiederzugeben. Der Exchange-Writer unterstützt sowohl Sicherungen als auch Wiederherstellungen.
  
Der Exchange-Writer ist auf jedem Exchange-Server verfügbar, auf dem die Postfachserverrolle installiert ist. 
  
## <a name="exchange-writer-configuration-settings"></a>Exchange Writer-Konfigurationseinstellungen
<a name="bk_ExchangeWriterConfig"> </a>

Der Exchange-Writer für VSS verwendet eine Vielzahl von Einstellungen und Werten, die ordnungsgemäß festgelegt und während Sicherungs-und Wiederherstellungsvorgängen beibehalten werden müssen. Diese Konfigurationseinstellungen werden im Dokument Exchange Writer Metadata gespeichert. Wenn die Sicherungsanwendung diese Einstellungen nicht aufrecht erhält, können unerwartete Fehler auftreten, wenn Sie versuchen, Ihre Exchange-Datenbanken zu sichern. 
  
In der folgenden Tabelle sind die VSS-Schnittstellen aufgeführt, die Metadaten zu den Komponenten der Datenbanksicherung verfügbar machen. Diese Schnittstellen sind erforderlich, um das Exchange Writer-Metadaten Dokument abzurufen, das zum Ausführen einer Sicherung des Exchange-Informationsspeicher verwendet wird.
  
**Tabelle 1. VSS-Schnittstellen**

|**VSS-Schnittstelle**|**Beschreibung**|
|:-----|:-----|
|IVssWMComponent  <br/> |Ermöglicht den Zugriff auf Komponenteninformationen, die im Exchange-Writer gespeichert sind.  <br/> |
|IVssExamineWriterMetadata  <br/> |Ermöglicht der anfordernden Sicherungs-und Wiederherstellungsanwendung, die Metadaten des Exchange-Writers zu untersuchen. Das Dokument "Exchange Writer Metadata" enthält Exchange 2013 spezifische Werte und Parameter, die die anfordernde Sicherungs-und Wiederherstellungsanwendung benötigt, damit die entsprechenden Komponenten für die Sicherung ordnungsgemäß angegeben werden können.  <br/> |
|IVssComponent  <br/> |Enthält Methoden zum Überprüfen und Ändern von Informationen zu Komponenten, die in einem Dokument mit den Sicherungskomponenten eines Anforderers enthalten sind. Objekte können nur für die Komponenten abgerufen werden, die diesem Dokument explizit durch die [IVssBackupComponents:: addComponent](https://msdn.microsoft.com/library/windows/desktop/aa382646%28v=vs.85%29.aspx) -Methode hinzugefügt wurden.  <br/> |
|IVssBackupComponents  <br/> |Wird von der anfordernden Sicherungs-und Wiederherstellungsanwendung verwendet, um den Exchange-Writer über den Dateistatus abzurufen und um Sicherungs-und Wiederherstellungsvorgänge auszuführen. Die [IVssBackupComponents:: SetBackupState](https://msdn.microsoft.com/library/windows/desktop/aa382833%28v=vs.85%29.aspx) -Methode definiert, ob es sich bei dem Sicherungsvorgang um eine vollständige, Kopie-, inkrementelle oder differenzielle Sicherung handelt. Die [IVssBackupComponents:: AddRestoreSubcomponent](https://msdn.microsoft.com/library/windows/desktop/aa382649%28v=vs.85%29.aspx) -Methode definiert die unter Komponenten einer Exchange 2013 Datenbank, die für einen Wiederherstellungsvorgang ausgewählt werden kann.  <br/> |
   
Im Windows Server-Dateisystem wird eine Exchange 2013 Datenbank als einzelne Datenbankdatei mit einer Erweiterung *. edb gespeichert. Der Exchange-Writer macht die *EDB als Datenbankkomponente verfügbar, während Transaktionsprotokolle (* Log) und Prüfpunktdateien (* chk) zu einer einzigen Komponente zusammengefasst werden, die als Protokollkomponente bezeichnet wird. Weitere Informationen zu Exchange-Datenbankdateien finden Sie unter [Backup and Restore Concepts for Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md).
  
## <a name="interactions-between-the-exchange-writer-vss-and-vss-requesters"></a>Interaktionen zwischen den Exchange Writer-, VSS-und VSS-anfordernden
<a name="bk_interactions"> </a>

Die allgemeine Interaktion zwischen VSS, Exchange Writer und Exchange 2013 während Sicherungsvorgängen lautet wie folgt:
  
1. Vom Sicherungsprogramm (oder Agent) wird ein geplanter Auftrag ausgeführt. 
    
2. Der VSS-Anforderer in der Sicherungs-und Wiederherstellungsanwendung sendet einen Befehl an VSS, um eine Shadow-Kopie der ausgewählten Exchange 2013 Datenbanken zu erstellen. 
    
3. VSS kommuniziert mit dem Exchange-Writer, um eine Momentaufnahme Sicherung vorzubereiten. Exchange 2013 verhindert administrative Aktionen für die Datenbanken, überprüft die Volume-Abhängigkeiten und unterbricht alle Schreibvorgänge für die ausgewählte Instanz der Datenbank-und Transaktionsprotokolldateien, während der schreibgeschützte Zugriff zulässig ist. 
    
4. VSS kommuniziert mit dem entsprechenden Speicheranbieter, um eine Schattenkopie des Speichervolumens zu erstellen, das die Exchange 2013 Datenbanken enthält. 
    
5. VSS gibt Exchange 2013 aus, um den normalen Betrieb fortzusetzen. 
    
6. Der VSS-Anforderer überprüft die physische Konsistenz des Sicherungssatzes, bevor er signalisiert, dass die Sicherung erfolgreich war. Exchange 2013 schneidet die Transaktionsprotokolle ab (wenn die Datenbank Teil einer DAG ist, wird das Abschneiden von Protokollen unter allen Kopien repliziert) und die Uhrzeit der letzten Sicherung für die Datenbank aufgezeichnet.
    
VSS serialisiert die Interaktion von Anforderern mit dem Exchange-Writer, beginnend mit der [OnPrepareBackup](https://msdn.microsoft.com/library/windows/desktop/aa381571%28v=vs.85%29.aspx) -Methode und endend mit der [OnPostSnapshot](https://msdn.microsoft.com/library/windows/desktop/aa381568%28v=vs.85%29.aspx) -Methode. Normalerweise tritt der Großteil der Zeit, die der Exchange-Writer für die Arbeit mit der Shadow Copy aufwendet, nach der **OnPostSnapshot** -Methode auf, wenn die Konsistenz der Shadow Copy vor Abschluss der Sicherungen überprüft wird. Der Exchange-Writer unterstützt parallele Sicherungen zwischen **OnPostSnapshot** und [OnBackupComplete](https://msdn.microsoft.com/library/windows/desktop/aa381557%28v=vs.85%29.aspx).
  
In Exchange 2013 werden gleichzeitige Sicherungen derselben Datenbank nicht zugelassen. Für eine bestimmte Datenbank kann gleichzeitig nur ein Sicherungsauftrag ausgeführt werden. Wenn die Sicherung ausgeführt wird, stellt der Exchange-Informationsspeicher die Datenbank in einen Status "Sicherung in Bearbeitung" ein. Dieser Status im Arbeitsspeicher wird entweder bei Abschluss des Sicherungsvorgangs oder beim Neustart des Diensts gelöscht. Die im Arbeitsspeicher befindliche Sicherung im Status und die zugehörigen Daten gehen verloren, wenn der Dienst, der den Exchange-Writer hostet, neu gestartet wird, wenn das Betriebssystem neu gestartet wird oder wenn ein Cluster Failover erfolgt. Jedes dieser Ereignisse führt dazu, dass der Sicherungsauftrag fehlschlägt.
  
Das Abschneiden von Sicherungs initiierten Transaktionsprotokolldateien wird basierend auf dem Typ der durchzuführenden Sicherung ausgelöst. In Konfigurationen ohne DAG schneidet der Exchange-Writer die Transaktionsprotokolldateien nach Abschluss einer erfolgreichen vollständigen oder inkrementellen Sicherung ab. In DAG-replizierten Konfigurationen wird das Abschneiden von Protokollen vom Replikationsdienst verzögert, bis alle erforderlichen Protokolldateien in allen anderen Kopien wiedergegeben werden. Der Replikationsdienst löscht die gesicherten Protokolldateien sowohl aus den aktiven als auch aus den Protokolldatei Pfaden, nachdem er überprüft hat, ob die Protokolldateien erfolgreich auf die kopiedatenbank angewendet wurden und sowohl die aktiven als auch die Datenbankkopien-Prüf Punkt die zu löschenden Protokolldateien bestanden hat.
  
## <a name="see-also"></a>Siehe auch

- [Transaktionsprotokolle und Prüfpunktdateien für Sicherung und Wiederherstellung in Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

