---
title: CChkSGFiles.ErrCheckLogs-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrCheckLogs
api_type:
- dllExport
ms.assetid: cec0df4b-4679-4682-bacf-69b4f4aef343
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: 64484b32fdc566d6fee8631f80d078aca82b11d1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516384"
---
# <a name="cchksgfileserrchecklogs-function"></a>CChkSGFiles.ErrCheckLogs-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Überprüft die Protokolldateien aller Datenbankdateien, die in der **ErrInit-Funktion** angegeben wurden. Bei den überprüften Protokollen handelt es sich um die Protokolle, die im Pfad vorhanden sind und deren Drei-Buchstaben-Basisprotokolldateiname an **ErrInit** übergeben wird.
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parameter

### <a name="pfonlyunnecessarylogscorrupt"></a>pfOnlyUnnecessaryLogsCorrupt 
  
Output-Parameter. Wenn **true**, gibt dieser Parameter an, dass Fehler in den Transaktionsprotokolldateien gefunden wurden, aber alle diese Fehler wurden in Protokolldateien gefunden, die nicht benötigt werden, um die Datenbank ohne Datenverlust in einen Zustand des sauberen Herunterfahrens zu versetzen. Ein in diesem Parameter zurückgegebener **true-Wert** ist nur gültig, wenn **ErrCheckLogs** **ErrSuccess** zurückgibt. 
    
### <a name="ulflags"></a>ulFlags
  
Optionaler Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der von diesem Parameter übergebene Wert sollte 0 (null) sein.
    
## <a name="return-value"></a>Rückgabewert

Ein Fehlercode aus der [ERR-Enumeration.](cchksgfiles-err-enumeration.md) 
  
Es ist wichtig zu beachten, dass diese Funktion **errSuccess** auch dann zurückgeben kann, wenn Fehler in den Protokolldateien gefunden werden. Wenn **ErrCheckLogs** **errSuccess** zurückgibt, sollte die Anwendung daher auch den  **Rückgabeparameter "pfOnlyUnnecessaryLogsCorrupt"** überprüfen. Wenn **pfOnlyUnnecessaryLogsCorrupts** **"true"** ist, wenn **ErrCheckLogs** **errSuccess** zurückgibt, bedeutet dies, dass ein oder mehrere Fehler gefunden wurden, jedoch nur in Protokolldateien, die nicht benötigt werden, um die Datenbank auf dem neuesten Stand zu halten.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **ErrCheckDbHeaders-Funktion** muss aufgerufen werden, bevor die **ErrCheckLogs-Funktion** aufgerufen werden kann. 
  
Wenn Exchange Protokolldateien für Datenbanktransaktionen überprüft werden, sind einige der Protokolldateien erforderlich, um die Datenbanken in der Speichergruppe ohne Datenverlust in den Zustand "Clean Shutdown" zu versetzen, während andere Protokolldateien möglicherweise nicht benötigt werden. Die **ErrCheckLogs-Funktion** bestimmt sowohl die ältesten als auch die neuesten Protokolldateien, die erforderlich sind, um die Datenbanken auf dem neuesten Stand zu halten. 
  
Die **ErrCheckLogs-Funktion** überprüft alle Protokolldateien in den angegebenen Pfaden, die auch den angegebenen Drei-Buchstaben-Basisdateinamen aufweisen, wie an die **ErrInit-Funktion** übergeben. 
  
Wenn in den Protokolldateien keine Fehler gefunden werden, gibt **ErrCheckLogs** **errSuccess** zurück. 
  
Wenn eine der erforderlichen Protokolldateien beschädigt ist, gibt **ErrCheckLogs** einen Fehler zurück. 
  
Wenn Fehler nur in Protokolldateien gefunden werden, die älter als die frühesten benötigten sind, gibt die Funktion **errSuccess** zurück und legt den Rückgabeparameter **pfOnlyUnnecessaryLogCorrupt** auf **"true"** fest. Die Anwendung sollte erkennen, dass fehler in einigen dieser alten Protokolldateien vorhanden sind, und wenn ja, wird der Benutzer möglicherweise benachrichtigt. In jedem Fall sollten sich diese Fehler nicht auf die allgemeine Integrität der Datenbank auswirken oder darauf auswirken, ob die Wiedergabe der Protokolle erfolgreich ist.
  
Wenn Fehler in einer Protokolldatei gefunden werden, die nach dem frühesten Protokoll erstellt wurde, das **ErrCheckLogs** ermittelt, ist erforderlich, gibt die Funktion einen Fehler zurück. Der Fehler wird auch zurückgegeben, wenn der Protokolldateifehler in einer Protokolldatei gefunden wurde, die später als erforderlich generiert wurde, um die Datenbank auf den neuesten Stand zu bringen. Obwohl es möglich wäre, die Datenbanken mithilfe der identifizierten Protokolldateien in einen Zustand des sauberen Herunterfahrens zu versetzen, würden die in den späteren beschädigten Protokolldateien angegebenen Transaktionen nicht angewendet, was zu Einem Datenverlust führen würde, wenn die Datenbank wiederhergestellt wird. 
  
Das **CChkSGFiles-Objekt** bestimmt, ob alle protokolldateien, die mit der **ErrInit-Funktion** registriert wurden, tatsächlich überprüft wurden. Wenn nicht alle Protokolle erfolgreich überprüft wurden, gibt die **ErrTerm-Funktion** einen Fehler zurück. 
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, können Sie die **ErrCheckLogs-Funktion** im Multithreadbereich der Anwendung aufrufen, aber Sie können sie nur einmal für jedes **CCheckSGFiles-Objekt** aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung ausgeführt wird, muss über Lesezugriffsberechtigungen für die Datenbank und die Protokolldateien verfügen, die überprüft werden sollen.
  

