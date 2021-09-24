---
title: Exchange Writer in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ec126433-9f0a-46ec-a685-ff4af2f97bc1
description: Hier finden Sie Informationen zum Exchange Writer in Exchange 2013 für Sicherungs- und Wiederherstellungsvorgänge.
ms.openlocfilehash: 7c50c2aa014308b05bdbc1acf0f2a91e33717ed6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516237"
---
# <a name="exchange-writer-in-exchange-2013"></a>Exchange Writer in Exchange 2013

Hier finden Sie Informationen zum Exchange Writer in Exchange 2013 für Sicherungs- und Wiederherstellungsvorgänge. 
  
**Gilt für:** Exchange Server 2013 
  
Der Exchange Writer ist für die Sicherung und Wiederherstellung aktiver Exchange Server 2013-Datenbanken verantwortlich. Der Exchange Writer unterstützt auch Sicherungsfunktionen für eine ausgewählte Datenbank, in der die Schattenkopie für die replizierte Instanz der Datenbank- und Transaktionsprotokolldateien erstellt wird. 
  
## <a name="overview-of-the-exchange-writer"></a>Übersicht über den Exchange Writer
<a name="bk_Overview"> </a>

Exchange 2013 umfasst Datenbank-Mobilitätsfunktionen, die es ermöglichen, Datenbanken auf verschiedenen Exchange Servern zu replizieren, um die Datenbankverfügbarkeit und Standortresilienz zu verbessern. Die anderen Datenbankkopien in einer Datenbankverfügbarkeitsgruppe (Database Availability Group, DAG) bieten eine wertvolle Gelegenheit für Exchange Sicherungen, die zusätzlichen Ressourcen zu verwenden, die am Kopierspeicherort verfügbar sind. Da die Kopie anstelle des aktiven Datenbankmasters gesichert wird, kann die Kopie während der Sicherung für einen längeren Zeitraum nicht mehr verfügbar sein. 
  
Der Exchange Writer koordiniert sich mit den Exchange Diensten (die im Auftrag des Antragstellers ausgeführt werden), um die Datenbankdateien für Sicherungen vorzubereiten, die E/A-Aktivität aus Exchange Transaktionen zu fixieren, bevor die Datenbank gesichert wird, und die Protokolldateien nach Abschluss der Sicherung aufzuheben und zu kürzen.
  
Während einer Wiederherstellung weist die Sicherungs- und Wiederherstellungsanwendung den Exchange Writer an, sich mit dem Exchange Speicher (der im Auftrag des Antragstellers ausgeführt wird) zu koordinieren, um die Wiederherstellungsziele zu überprüfen, die Datenbankdatei bei Bedarf umzubenennen und dann die Transaktionsprotokolle nach Bedarf wiederzugeben. Der Exchange Writer unterstützt Sicherungen und Wiederherstellungen.
  
Der Exchange Writer ist auf jedem Exchange Server verfügbar, auf dem die Postfachserverrolle installiert ist. 
  
## <a name="exchange-writer-configuration-settings"></a>Exchange Writer-Konfigurationseinstellungen
<a name="bk_ExchangeWriterConfig"> </a>

Der Exchange Writer für VSS verwendet eine Vielzahl von Einstellungen und Werten, die korrekt festgelegt und während Sicherungs- und Wiederherstellungsvorgängen beibehalten werden müssen. Diese Konfigurationseinstellungen werden im Exchange Writer-Metadatendokument gespeichert. Wenn ihre Sicherungsanwendung diese Einstellungen nicht beibehalten, treten möglicherweise unerwartete Fehler auf, wenn Sie versuchen, Ihre Exchange Datenbanken zu sichern. 
  
In der folgenden Tabelle sind die VSS-Schnittstellen aufgeführt, die Metadaten zu den Komponenten ihrer Datenbanksicherung verfügbar machen. Diese Schnittstellen sind erforderlich, um das Exchange Writer-Metadatendokument abzurufen, das zum Ausführen einer Sicherung des Exchange Speichers verwendet wird.
  
**Tabelle 1. VSS-Schnittstellen**

|**VSS-Schnittstelle**|**Beschreibung**|
|:-----|:-----|
|IVssWMComponent  <br/> |Ermöglicht den Zugriff auf Komponenteninformationen, die im Exchange Writer gespeichert sind.  <br/> |
|IVssExaminWriterMetadata  <br/> |Ermöglicht der anfordernden Sicherungs- und Wiederherstellungsanwendung, die Metadaten des Exchange Writers zu überprüfen. Das Exchange Writer-Metadatendokument enthält Exchange 2013-spezifische Werte und Parameter, die die anfordernde Sicherungs- und Wiederherstellungsanwendung benötigt, damit sie die entsprechenden Komponenten für die Sicherung korrekt angeben kann.  <br/> |
|IVssComponent  <br/> |Enthält Methoden zum Untersuchen und Ändern von Informationen zu Komponenten, die im Sicherungskomponentendokument eines Anfordernden enthalten sind. Objekte können nur für die Komponenten abgerufen werden, die diesem Dokument durch die [IVssBackupComponents::AddComponent-Methode](https://msdn.microsoft.com/library/windows/desktop/aa382646%28v=vs.85%29.aspx) explizit hinzugefügt wurden.  <br/> |
|IVssBackupComponents  <br/> |Wird von der anfordernden Sicherungs- und Wiederherstellungsanwendung verwendet, um den Exchange Writer über den Dateistatus abfragt und Sicherungs- und Wiederherstellungsvorgänge auszuführen. Die [IVssBackupComponents::SetBackupState-Methode ](https://msdn.microsoft.com/library/windows/desktop/aa382833%28v=vs.85%29.aspx) definiert, ob es sich bei dem Sicherungsvorgang um eine vollständige, kopier-, inkrementelle oder differenzielle Sicherung handelt. Die [IVssBackupComponents::AddRestoreSubcomponent-Methode](https://msdn.microsoft.com/library/windows/desktop/aa382649%28v=vs.85%29.aspx) definiert die Unterkomponenten einer Exchange 2013-Datenbank, die für einen Wiederherstellungsvorgang ausgewählt werden kann.  <br/> |
   
Innerhalb des dateisystems Windows Servers wird eine Exchange 2013-Datenbank als einzelne Datenbankdatei mit der Erweiterung *EDB gespeichert. Der Exchange Writer macht die *EDB-Datei als Datenbankkomponente verfügbar, während Transaktionsprotokolle (* LOG) und Prüfpunktdateien (CHK)* in einer einzigen Komponente zusammengefasst werden, die als Protokollkomponente bezeichnet wird. Weitere Informationen zu Exchange Datenbankdateien finden Sie unter [Sicherungs- und Wiederherstellungskonzepte für Exchange 2013.](backup-and-restore-concepts-for-exchange-2013.md)
  
## <a name="interactions-between-the-exchange-writer-vss-and-vss-requesters"></a>Interaktionen zwischen dem Exchange Writer, VSS und VSS-Anforderern
<a name="bk_interactions"> </a>

Die allgemeine Interaktion zwischen dem VSS, dem Exchange Writer und Exchange 2013 bei Sicherungsvorgängen lautet wie folgt:
  
1. Vom Sicherungsprogramm (oder Agent) wird ein geplanter Auftrag ausgeführt. 
    
2. Der VSS-Anforderer in der Sicherungs- und Wiederherstellungsanwendung sendet einen Befehl an VSS, um eine Schattenkopie der ausgewählten Exchange 2013-Datenbanken zu erstellen. 
    
3. VSS kommuniziert mit dem Exchange Writer, um eine Momentaufnahmesicherung vorzubereiten. Exchange 2013 verbietet administrative Aktionen für die Datenbanken, überprüft Volumenabhängigkeiten und hält alle Schreibvorgänge in ausgewählte Instanzen der Datenbank- und Transaktionsprotokolldateien an, während schreibgeschützter Zugriff gewährt wird. 
    
4. VSS kommuniziert mit dem entsprechenden Speicheranbieter, um eine Schattenkopie des Speichervolumes zu erstellen, das die Exchange 2013-Datenbanken enthält. 
    
5. VSS veröffentlicht Exchange 2013, um normale Vorgänge fortzusetzen. 
    
6. Der VSS-Anforderer überprüft die physische Konsistenz des Sicherungssatzes, bevor er signalisiert, dass die Sicherung erfolgreich war. Exchange 2013 werden die Transaktionsprotokolle abgeschnitten (wenn die Datenbank Teil einer DAG ist, wird die Protokollkürzung zwischen allen Kopien repliziert) und zeichnet den Zeitpunkt der letzten Sicherung für die Datenbank auf.
    
VSS serialisiert die Interaktion von Anforderern mit dem Exchange Writer beginnend mit der [OnPrepareBackup-Methode](https://msdn.microsoft.com/library/windows/desktop/aa381571%28v=vs.85%29.aspx) und endet mit der [OnPostSnapshot-Methode.](https://msdn.microsoft.com/library/windows/desktop/aa381568%28v=vs.85%29.aspx) In der Regel erfolgt der Großteil der Zeit, die der Exchange Writer mit der Schattenkopie verbringt, nach der **OnPostSnapshot-Methode,** wenn die Konsistenz der Schattenkopie vor Abschluss der Sicherungen überprüft wird. Der Exchange Writer unterstützt parallele Sicherungen zwischen **OnPostSnapshot** und [OnBackupComplete.](https://msdn.microsoft.com/library/windows/desktop/aa381557%28v=vs.85%29.aspx)
  
Exchange 2013 lässt keine gleichzeitigen Sicherungen derselben Datenbank zu. Es kann jeweils nur ein Sicherungsauftrag für eine bestimmte Datenbank ausgeführt werden. Wenn die Sicherung ausgeführt wird, versetzt der Exchange Speicher die Datenbank in den Status "In Bearbeitung der Sicherung". Dieser Zustand im Arbeitsspeicher wird entweder nach Abschluss des Sicherungsvorgangs oder beim Neustart des Diensts gelöscht. Der zustand der laufenden Speichersicherung und die zugehörigen Daten gehen verloren, wenn der Dienst, der den Exchange Writer hostet, neu gestartet wird, wenn das Betriebssystem neu gestartet wird oder wenn ein Clusterfailover auftritt. Jedes dieser Ereignisse führt dazu, dass der Sicherungsauftrag fehlschlägt.
  
Die durch die Sicherung initiierte Transaktionsprotokoll-Abkürzung wird basierend auf dem Typ der durchzuführenden Sicherung ausgelöst. In Nicht-DAG-Konfigurationen werden die Transaktionsprotokolldateien vom Exchange Writer nach Abschluss erfolgreicher vollständiger oder inkrementeller Sicherungen abgeschnitten. In replizierten DAG-Konfigurationen wird die Protokollkürzung vom Replikationsdienst verzögert, bis alle erforderlichen Protokolldateien in allen anderen Kopien wiedergegeben werden. Der Replikationsdienst löscht die gesicherten Protokolldateien sowohl aus dem aktiven als auch aus dem Kopierprotokolldateipfad, nachdem überprüft wurde, ob die Protokolldateien erfolgreich auf die Kopierdatenbank angewendet wurden und sowohl die aktive Datenbank als auch der Datenbankkopieprüfpunkt die zu löschenden Protokolldateien übergeben hat.
  
## <a name="see-also"></a>Siehe auch

- [Transaktionsprotokolle und Prüfpunktdateien für Sicherung und Wiederherstellung in Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

