---
title: CChkSGFiles. ErrCheckLogs-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckLogs
api_type:
- dllExport
ms.assetid: cec0df4b-4679-4682-bacf-69b4f4aef343
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: 71e21bb3a748a532f9e3167e0b36898acde71b02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526718"
---
# <a name="cchksgfileserrchecklogs-function"></a>CChkSGFiles. ErrCheckLogs-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Überprüft die Protokolldateien aller Datenbankdateien, die in der **ErrInit** -Funktion angegeben wurden. Die überprüften Protokolle sind diejenigen, die im Pfad vorhanden sind und die den Namen der Basisprotokoll Datei mit drei Buchstaben an **ErrInit**übergeben haben.
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parameter

### <a name="pfonlyunnecessarylogscorrupt"></a>pfOnlyUnnecessaryLogsCorrupt 
  
Output-Parameter. Bei **true**gibt dieser Parameter an, dass Fehler in den Transaktionsprotokolldateien gefunden wurden, aber diese Fehler wurden alle in Protokolldateien gefunden, die nicht erforderlich sind, um die Datenbank ohne Datenverlust in den Zustand "Clean Shutdown" zu versetzen. Ein **true** -Wert, der in diesem Parameter zurückgegeben wird, ist nur gültig, wenn **ErrCheckLogs** **errSuccess**zurückgibt. 
    
### <a name="ulflags"></a>ulFlags
  
Optionaler Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der von diesem Parameter übergebene Wert sollte 0 (null) sein.
    
## <a name="return-value"></a>Rückgabewert

Ein Fehlercode aus der [Err](cchksgfiles-err-enumeration.md) -Aufzählung. 
  
Beachten Sie, dass diese Funktion **errSuccess** auch dann zurückgeben kann, wenn Fehler in den Protokolldateien gefunden werden. Wenn **ErrCheckLogs** also **errSuccess**zurückgibt, sollte die Anwendung auch den **pfOnlyUnnecessaryLogsCorrupt** -Rückgabeparameter überprüfen. Wenn **pfOnlyUnnecessaryLogsCorrupts** auf **true** festgelegt ist, wenn **ErrCheckLogs** **errSuccess**zurückgibt, deutet dies darauf hin, dass ein oder mehrere Fehler gefunden wurden, jedoch nur in Protokolldateien, die nicht benötigt wurden, um die Datenbank auf den neuesten Stand zu bringen.
  
## <a name="remarks"></a>Bemerkungen

Die **ErrCheckDbHeaders** -Funktion muss aufgerufen werden, bevor die **ErrCheckLogs** -Funktion aufgerufen werden kann. 
  
Wenn die Transaktionsprotokolldateien von Exchange-Datenbank überprüft werden, sind einige Protokolldateienerforderlich, um die Datenbanken in der Speichergruppe ohne Datenverlust in den Zustand "Clean Shutdown" zu versetzen, während andere Protokolldateien möglicherweise nicht benötigt werden. Die **ErrCheckLogs** -Funktion bestimmt sowohl die älteste als auch die neueste Protokolldatei, die zum Aktualisieren der Datenbanken benötigt werden. 
  
Die **ErrCheckLogs** -Funktion überprüft alle Protokolldateien in den angegebenen Pfaden, die auch den angegebenen Namen der Basisdatei mit drei Buchstaben aufweisen und an die **ErrInit** -Funktion übergeben werden. 
  
Wenn in den Protokolldateien keine Fehler gefunden werden, **ErrCheckLogs** gibt ErrCheckLogs **errSuccess**zurück. 
  
Wenn eine der erforderlichen Protokolldateien als beschädigt festgestellt wird, gibt **ErrCheckLogs** einen Fehler zurück. 
  
Wenn Fehler nur in Protokolldateien gefunden werden, die älter als die frühesten sind, die benötigt werden, gibt die Funktion **errSuccess** zurück und legt den Rückgabeparameter **pfOnlyUnnecessaryLogCorrupt** auf **true**fest. Die Anwendung sollte erkennen, dass in einigen dieser alten Protokolldateien Fehler vorliegen, und wenn dies der Fall ist, wird der Benutzer möglicherweise gewarnt. In jedem Fall sollten diese Fehler keine Auswirkungen auf die Gesamtintegrität der Datenbank haben oder sich darauf auswirken, ob die Wiedergabe der Protokolle erfolgreich ausgeführt wird.
  
Wenn Fehler in einer Protokolldatei gefunden werden, die nach dem frühesten Protokoll erstellt wurde, das von **ErrCheckLogs** bestimmt wird, gibt die Funktion einen Fehler zurück. Der Fehler wird auch dann zurückgegeben, wenn der Protokolldatei Fehler in einer Protokolldatei gefunden wurde, die später als erforderlich generiert wurde, um die Datenbank auf den neuesten Stand zu bringen. Obwohl es möglich wäre, die Datenbanken mithilfe der identifizierten Protokolldateien in den Zustand "Clean Shutdown" zu versetzen, wurden in den später beschädigten Protokolldateien angegebene Transaktionen nicht angewendet, was zu einem Datenverlust bei der Wiederherstellung der Datenbank führte. 
  
Das **CChkSGFiles** -Objekt bestimmt, ob alle mit der **ErrInit** -Funktion registrierten Protokolldateien tatsächlich überprüft wurden. Wenn nicht alle Protokolle erfolgreich überprüft wurden, gibt die **ErrTerm** -Funktion einen Fehler zurück. 
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, können Sie die **ErrCheckLogs** -Funktion im Multithread-Teil der Anwendung aufrufen, Sie können Sie jedoch nur einmal für jedes **CCheckSGFiles** -Objekt aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.
  

