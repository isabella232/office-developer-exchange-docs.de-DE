---
title: Überprüfen der Integrität mithilfe des Dienstprogramms Eseutil in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: Erfahren Sie, wie Sie das Befehlszeilentool "Eseutil" verwenden, um eine Sicherung der Exchange-Speicher zu überprüfen.
ms.openlocfilehash: 03c4c23d433418911240bbe7c337308a989f3739
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756799"
---
#  <a name="validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013"></a>Überprüfen der Integrität mithilfe des Dienstprogramms Eseutil in Exchange 2013

Erfahren Sie, wie Sie das Befehlszeilentool "Eseutil" verwenden, um eine Sicherung der Exchange-Speicher zu überprüfen. 
  
**Gilt für:** Exchange Server 2013 
  
Da der Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) zwar Exchange zum Schreiben in die Datenbank ist Sicherungen erstellen können, wird der Server nicht tippen Sie auf allen Seiten und führen Sie die erforderlichen Konsistenz überprüft. Aus diesem Grund muss jede Sicherung und Wiederherstellung Anwendung, die VSS verwendet, Snapshot-Konsistenz überprüfen. Exchange Server 2013 unterstützt die folgenden zwei Methoden für die Überprüfung auf Snapshot-Konsistenz: 
  
- Die CHKSGFILES-API
    
- Das Befehlszeilentool "Eseutil"
    
Es wird empfohlen, dass Sie die CHKSGFILES-API verwenden, da für die backup-Anwendung zu erkennen, diagnostizieren ist es einfacher, und überprüfen Melden von Fehlern, die während der Konsistenz CHKSGFILES gefunden werden. Informationen dazu, wie die CHKSGFILES-API verwenden finden Sie unter [backup Validate-Integrität mithilfe der API für CHKSGFILES in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).
  
## <a name="running-the-eseutil-tool"></a>Ausführen des Tools "Eseutil"

Um die Konsistenz Snapshot zu überprüfen, führen Sie den Befehl "Eseutil" für die Datenbank- und Protokolldateien Dateien, die in der folgenden Tabelle angegeben sind. 
  
**In Tabelle 1. Eseutil.exe Befehle für jede Sicherungsart**

|**Dateityp Typ-Sicherung**|**Vollständige Sicherung**|**Kopie-Sicherung**|**Inkrementelle Sicherung**|**Differenzielle Sicherung**|
|:-----|:-----|:-----|:-----|:-----|
|EDB  <br/> |"Eseutil/k/i"  <br/> |"Eseutil/k/i"  <br/> |–  <br/> |–  <br/> |
|.log  <br/> |"Eseutil/k" (1)  <br/> |"Eseutil/k" (1)  <br/> |"Eseutil/k" (2)  <br/> |"Eseutil/k" (2)  <br/> |
   
> [!NOTE]
> Sie müssen nicht für STM und chk-Dateien den Befehl "Eseutil" ausgeführt. 
  
Alle Protokolldateien, die eine Zahl, die Generierung einer Protokolldatei ist gleich oder größer als die Anzahl der Protokolldatei Prüfpunkt sind erforderlich, um das Wiederherstellen einer Snapshotdatenbank Generation. Wenn es vorhanden ist, wird die aktuelle Protokolldatei (Enn.log) auch für die Wiederherstellung der Datenbank erforderlich. Wenn einer der erforderlichen Protokolldateien konsistenzprüfung fehlschlägt, muss die anfordernde Person sicherstellen, dass der Status der backup-Komponente auf FALSE festgelegt ist, bevor sie die [BackupComplete](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382651%28v=vs.85%29.aspx) -Methode aufruft. Zum Identifizieren der Prüfpunkt-Protokolldatei die Prüfpunktdatei Snapshot Eseutil.exe ausführen, und analysieren Sie die Ausgabe für "Checkpoint:." Im folgenden Beispiel wird veranschaulicht, wie für eine Prüfpunktdatei Eseutil.exe ausführen. 
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

Die zweite Zeile im Beispiel ist der Rückgabewert, wobei 0 x 20 hexadezimale Protokollgenerierungsnummer der Protokolldatei Prüfpunkt. In diesem Beispiel wird eine Protokolldateien, einschließlich E01000020.log und höher, muss nicht beschädigt, um die Snapshotdatenbank wiederhergestellt werden, selbst wenn die Überprüfung der physischen Konsistenz bereits in die Datenbank selbst vergangen ist.
  
Alle Protokolldateien in eine inkrementelle oder differenzielle Sicherungssatz sind für die Wiederherstellung der Datenbank erforderlich. Sie können die Konsistenz der einer Sequenz Protokoll durch Ausführen von Eseutil.exe für das Protokolldateipräfix überprüfen. Im folgenden Beispiel wird gezeigt, wie zum Ausführen von konsistenzprüfungen in alle Dateien des Formulars E01xxxxx.log auf einem angegebenen Pfad.
  
```cpp
c:\eseutil /k E01
```

## <a name="checking-the-eseutilexe-output"></a>Überprüfen die Ausgabe Eseutil.exe

Die anfordernde Person muss sicherstellen, dass alle Exit ERRORLEVEL Fehler, die zurückgegeben werden nicht negative Werte. Informationen zu ERRORLEVEL Werten finden Sie unter [Referenz für häufige Fehler von "Eseutil"](http://technet.microsoft.com/en-us/library/aa996759%28v=exchg.80%29.aspx). Klicken Sie nach Eseutil.exe ERRORLEVEL an der Befehlszeile finden Geben Sie "echo %ERRORLEVEL%". Ein negativer ERRORLEVEL gibt an, dass eine oder mehrere Dateien ist beschädigt.
  
Bevor die anfordernde Person die **BackupComplete** -Methode aufruft, müssen sie sicherstellen, dass der Status der Komponente backup das Ergebnis der konsistenzprüfung widerspiegelt. Wenn eine Beschädigung gefunden wurde, wird der Status FALSE; Wenn keine Beschädigung gefunden wurde, wird der Status "true" sein. 
  
## <a name="see-also"></a>Siehe auch

- [Überprüfen der Integrität mithilfe der API für CHKSGFILES in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [Erstellen von Sicherung und Wiederherstellen von Anwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [Referenz für die CChkSGFiles](cchksgfiles-class-reference.md)
- [Sicherung und Wiederherstellung Konzepte für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

