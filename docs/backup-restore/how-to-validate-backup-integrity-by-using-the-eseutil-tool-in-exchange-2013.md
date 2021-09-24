---
title: Überprüfen der Sicherungsintegrität mithilfe des Eseutil-Tools in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: Erfahren Sie, wie Sie das Eseutil-Befehlszeilentool verwenden, um eine Sicherung des Exchange Speichers zu überprüfen.
ms.openlocfilehash: 0ac994201d1f6c711e5d4d0a3d5835f9bac6e041
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516223"
---
#  <a name="validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013"></a>Überprüfen der Sicherungsintegrität mithilfe des Eseutil-Tools in Exchange 2013

Erfahren Sie, wie Sie das Eseutil-Befehlszeilentool verwenden, um eine Sicherung des Exchange Speichers zu überprüfen. 
  
**Gilt für:** Exchange Server 2013 
  
Da der Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) Sicherungen erstellen kann, während Exchange weiterhin in die Datenbank schreibt, berührt der Server nicht alle Seiten und führt die erforderlichen Konsistenzprüfungen aus. Aus diesem Grund muss jede Sicherungs- und Wiederherstellungsanwendung, die VSS verwendet, die Konsistenz der Momentaufnahmen überprüfen. Exchange Server 2013 unterstützt die folgenden beiden Methoden zur Überprüfung der Konsistenz von Momentaufnahmen: 
  
- Die CHKSGFILES-API
    
- Das Eseutil-Befehlszeilentool
    
Es wird empfohlen, die CHKSGFILES-API zu verwenden, da es für die Sicherungsanwendung einfacher ist, Fehler zu erkennen, zu diagnostizieren und zu melden, die während der CHKSGFILES-Konsistenzprüfung gefunden wurden. Informationen zur Verwendung der CHKSGFILES-API finden Sie unter [Überprüfen der Sicherungsintegrität mithilfe der CHKSGFILES-API in Exchange 2013.](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
  
## <a name="running-the-eseutil-tool"></a>Ausführen des Eseutil-Tools

Um die Konsistenz der Momentaufnahme zu überprüfen, führen Sie den Befehl "eseutil" für die Datenbank und die Protokolldateien aus, die in der folgenden Tabelle angegeben sind. 
  
**Tabelle 1. Eseutil.exe Befehle für jeden Sicherungstyp**

|**Dateityp/Sicherungstyp**|**Vollständige Sicherung**|**Kopiersicherung**|**Inkrementelle Sicherung**|**Differenzielle Sicherung**|
|:-----|:-----|:-----|:-----|:-----|
|.edb  <br/> |"eseutil /k /i"  <br/> |"eseutil /k /i"  <br/> |Nicht zutreffend  <br/> |Nicht zutreffend  <br/> |
|LOG  <br/> |"eseutil /k" (1)  <br/> |"eseutil /k" (1)  <br/> |"eseutil /k" (2)  <br/> |"eseutil /k" (2)  <br/> |
   
> [!NOTE]
> Sie müssen den eseutil-Befehl nicht für STM- und CHK-Dateien ausführen. 
  
Alle Protokolldateien mit einer Generierungsnummer der Protokolldatei, die der Generierungsnummer der Prüfpunktprotokolldatei entspricht oder größer ist, sind erforderlich, um eine Momentaufnahmedatenbank wiederherzustellen. Falls vorhanden, ist die aktuelle Protokolldatei (Enn.log) auch für die Datenbankwiederherstellung erforderlich. Wenn eine der erforderlichen Protokolldateien die Konsistenzprüfung nicht besteht, muss der Antragsteller sicherstellen, dass der Status der Sicherungskomponente auf FALSE festgelegt ist, bevor die [BackupComplete-Methode](https://msdn.microsoft.com/library/windows/desktop/aa382651%28v=vs.85%29.aspx) aufgerufen wird. Um die Prüfpunktprotokolldatei zu identifizieren, führen Sie Eseutil.exe für die Snapshot-Prüfpunktdatei aus, und analysieren Sie die Ausgabe für "Prüfpunkt:". Das folgende Beispiel zeigt, wie sie Eseutil.exe für eine Prüfpunktdatei ausführen. 
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

Die zweite Zeile im Beispiel ist der Rückgabewert, wobei 0x20 die hexadezimale Protokollgenerierungsnummer der Prüfpunktprotokolldatei ist. In diesem Beispiel dürfen alle Protokolldateien, einschließlich E01000020.log und höher, nicht beschädigt sein, um die Momentaufnahmedatenbank wiederherzustellen, auch wenn die Datenbank selbst die physische Konsistenzprüfung bereits bestanden hat.
  
Alle Protokolldateien in einem inkrementellen oder differenziellen Sicherungssatz sind für die Datenbankwiederherstellung erforderlich. Sie können die Konsistenz einer Protokollsequenz überprüfen, indem Sie Eseutil.exe anhand des Protokolldateipräfixes ausführen. Das folgende Beispiel zeigt, wie Konsistenzüberprüfungen für alle Dateien des Formulars "E01xxxxx.log" unter einem bestimmten Pfad ausgeführt werden.
  
```cpp
c:\eseutil /k E01
```

## <a name="checking-the-eseutilexe-output"></a>Überprüfen der ausgabe Eseutil.exe

Der Anforderer muss überprüfen, ob alle zurückgegebenen ErrorLEVEL-Fehlerwerte beim Beenden nichtegativ sind. Informationen zu ERRORLEVEL-Werten finden Sie unter [Reference for Common Eseutil Errors](https://technet.microsoft.com/library/aa996759%28v=exchg.80%29.aspx). Um errorlevel an der Befehlszeile anzuzeigen, geben Sie "echo %errorlevel%" ein, nachdem Eseutil.exe die Ausführung abgeschlossen hat. Ein negativer ERRORLEVEL gibt an, dass eine oder mehrere Dateien beschädigt sind.
  
Bevor der Antragsteller die **BackupComplete-Methode aufruft,** muss er sicherstellen, dass der Status der Sicherungskomponente das Ergebnis der Konsistenzprüfung widerspiegelt. Wenn eine Beschädigung gefunden wurde, lautet der Status FALSE. Wenn keine Beschädigung gefunden wurde, ist der Status TRUE. 
  
## <a name="see-also"></a>Siehe auch

- [Überprüfen der Sicherungsintegrität mithilfe der CHKSGFILES-API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [Erstellen von Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [CChkSGFiles-Klassenreferenz](cchksgfiles-class-reference.md)
- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

