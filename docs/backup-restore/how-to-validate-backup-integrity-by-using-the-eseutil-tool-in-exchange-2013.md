---
title: Überprüfen der Integrität der Sicherung mithilfe des Tools "Eseutil" in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: Erfahren Sie, wie Sie mithilfe des Befehlszeilentools Eseutil eine Sicherung der Exchange-Informationsspeicher überprüfen.
ms.openlocfilehash: e8f1a46e2d94729ae5586861317312e277216d63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452797"
---
#  <a name="validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013"></a>Überprüfen der Integrität der Sicherung mithilfe des Tools "Eseutil" in Exchange 2013

Erfahren Sie, wie Sie mithilfe des Befehlszeilentools Eseutil eine Sicherung der Exchange-Informationsspeicher überprüfen. 
  
**Gilt für:** Exchange Server 2013 
  
Da der Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) Sicherungen erstellen kann, während Exchange weiterhin in die Datenbank schreibt, berührt der Server nicht alle Seiten und führt die erforderlichen Konsistenzprüfungen aus. Aus diesem Grund muss jede Sicherungs-und Wiederherstellungsanwendung, die VSS verwendet, die Momentaufnahme Konsistenz überprüfen. Exchange Server 2013 unterstützt die folgenden beiden Methoden zum Überprüfen der Momentaufnahme Konsistenz: 
  
- Die CHKSGFILES-API
    
- Das Befehlszeilentool "Eseutil"
    
Es wird empfohlen, die CHKSGFILES-API zu verwenden, da es für die Sicherungsanwendung einfacher ist, Fehler zu erkennen, zu diagnostizieren und zu melden, die während der CHKSGFILES-Konsistenzprüfung gefunden werden. Informationen zur Verwendung der CHKSGFILES-API finden Sie unter [Überprüfen der Integrität von Sicherungen mithilfe der CHKSGFILES-API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).
  
## <a name="running-the-eseutil-tool"></a>Ausführung des Tools "Eseutil"

Um die Snapshot-Konsistenz zu überprüfen, führen Sie den Befehl Eseutil für die Datenbank-und Protokolldateien aus, die in der folgenden Tabelle angegeben sind. 
  
**Tabelle 1. Befehle des Typs "Eseutil. exe" für jeden Sicherungstyp**

|**Dateityp/Sicherungstyp**|**Vollständige Sicherung**|**Sicherung kopieren**|**Inkrementelle Sicherung**|**Differenzielle Sicherung**|
|:-----|:-----|:-----|:-----|:-----|
|EDB  <br/> |"Eseutil k/i"  <br/> |"Eseutil k/i"  <br/> |Nicht zutreffend  <br/> |Nicht zutreffend  <br/> |
|. log  <br/> |"Eseutil k" (1)  <br/> |"Eseutil k" (1)  <br/> |"Eseutil k" (2)  <br/> |"Eseutil k" (2)  <br/> |
   
> [!NOTE]
> Sie müssen den Befehl Eseutil nicht für STM-und CHK-Dateien ausführen. 
  
Alle Protokolldateien mit einer Generierungsnummer der Protokolldatei, die größer oder gleich der Generierungsnummer der Prüfpunktprotokoll Datei ist, sind erforderlich, um eine Momentaufnahmedatenbank wiederherzustellen. Wenn diese vorhanden ist, ist die aktuelle Protokolldatei (enn. log) auch für die Datenbankwiederherstellung erforderlich. Wenn bei einer der erforderlichen Protokolldateien die Konsistenzprüfung fehlschlägt, muss der Anforderer sicherstellen, dass der Status der Sicherungskomponente auf false festgelegt ist, bevor die [BackupComplete](https://msdn.microsoft.com/library/windows/desktop/aa382651%28v=vs.85%29.aspx) -Methode aufgerufen wird. Führen Sie zum Identifizieren der Prüfpunktprotokoll Datei Eseutil. exe für die Snapshot-Prüfpunktdatei aus, und analysieren Sie die Ausgabe für "Prüfpunkt:". Im folgenden Beispiel wird gezeigt, wie Eseutil. exe für eine Prüfpunktdatei ausgeführt wird. 
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

Die zweite Codezeile im Beispiel ist der Rückgabewert, wobei 0x20 die hexadezimale Protokollgenerierungsnummer der Prüfpunktprotokoll Datei ist. In diesem Beispiel dürfen Protokolldateien, einschließlich E01000020. log und höher, nicht beschädigt werden, um die Snapshotdatenbank wiederherzustellen, selbst wenn die Datenbank selbst die physikalische Konsistenzprüfung bereits bestanden hat.
  
Für die Datenbankwiederherstellung sind alle Protokolldateien in einem inkrementellen oder differenziellen Sicherungssatzes erforderlich. Sie können die Konsistenz einer Protokollsequenz überprüfen, indem Sie "Eseutil. exe" für das Präfix der Protokolldatei verwenden. Im folgenden Beispiel wird gezeigt, wie Konsistenzprüfungen für alle Dateien des Formulars E01xxxxx. log für einen bestimmten Pfad ausgeführt werden.
  
```cpp
c:\eseutil /k E01
```

## <a name="checking-the-eseutilexe-output"></a>Überprüfen der Ausgabe von "Eseutil. exe"

Der Anforderer muss überprüfen, ob alle zurückgegebenen Exit ERRORLEVEL-Fehlerwerte nicht negativ sind. Informationen zu ERRORLEVEL-Werten finden Sie unter [Reference für häufige Eseutil-Fehler](https://technet.microsoft.com/library/aa996759%28v=exchg.80%29.aspx). Um den ERRORLEVEL an der Befehlszeile anzuzeigen, geben Sie "Echo% ERRORLEVEL%" ein, nachdem die Ausführung von "Eseutil. exe" abgeschlossen wurde. Ein negativer ERRORLEVEL gibt an, dass eine oder mehrere Dateien beschädigt sind.
  
Bevor der Anforderer die **BackupComplete** -Methode aufruft, muss er sicherstellen, dass der Status der Sicherungskomponente das Ergebnis der Konsistenzprüfung widerspiegelt. Wenn eine Beschädigung gefunden wurde, ist der Status false; Wenn keine Beschädigung gefunden wurde, wird der Status auf true festgelegt. 
  
## <a name="see-also"></a>Siehe auch

- [Überprüfen der Integrität der Sicherung mithilfe der CHKSGFILES-API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [Erstellen von Sicherungs-und Wiederherstellungsanwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [CChkSGFiles-Klassenreferenz](cchksgfiles-class-reference.md)
- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

