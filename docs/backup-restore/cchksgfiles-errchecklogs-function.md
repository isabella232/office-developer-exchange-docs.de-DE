---
title: CChkSGFiles.ErrCheckLogs-Funktion
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
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: 5b1070de73bc23ae09ddb7835bd72c8e8a71a95f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756806"
---
# <a name="cchksgfileserrchecklogs-function"></a>CChkSGFiles.ErrCheckLogs-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Überprüft die Protokolldateien aller Datenbankdateien, die in der Funktion **ErrInit** angegeben wurden. Die validierten Protokolle sind nur die, die im Pfad vorhanden sind, und drei Buchstaben Logarithmus zur Basis Dateinamen **ErrInit**übergeben haben.
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parameter

### <a name="pfonlyunnecessarylogscorrupt"></a>pfOnlyUnnecessaryLogsCorrupt 
  
Output-Parameter. Wenn **true**, dieser Parameter gibt an, dass Fehler in die Transaktionsprotokolldateien, aber diese Fehler gefunden wurden wurden alle gefunden in Protokolldateien, die nicht benötigt werden versetzen die Datenbank in einen Zustand "clean Shutdown" ohne Datenverlust. Der Wert **true** zurückgegeben, die in diesem Parameter gilt nur, wenn **ErrCheckLogs** **ErrSuccess**zurückgegeben. 
    
### <a name="ulflags"></a>ulFlags
  
Optionale Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der durch diesen Parameter übergebene Wert muss 0 (null) sein.
    
## <a name="return-value"></a>R�ckgabewert

Ein Fehlercode aus der [ERR](cchksgfiles-err-enumeration.md) -Aufzählung. 
  
Es ist wichtig, denken Sie daran, dass diese Funktion **ErrSuccess** zurückgeben kann, selbst wenn Fehler in den Protokolldateien gefunden werden. Aus diesem Grund beim **ErrCheckLogs** **ErrSuccess**zurückgegeben wird, sollte die Anwendung auch **PfOnlyUnnecessaryLogsCorrupt** Rückgabeparameter überprüfen. Wenn **PfOnlyUnnecessaryLogsCorrupts** **ErrCheckLogs** **ErrSuccess**gibt **true** ist, bedeutet dies, dass eine oder mehrere Fehler gefunden wurden, jedoch nur in den Protokolldateien nicht erforderlich, um die Datenbank auf dem neuesten Stand zu bringen.
  
## <a name="remarks"></a>Hinweise

Bevor die **ErrCheckLogs** -Funktion aufgerufen werden kann, muss die **ErrCheckDbHeaders** -Funktion aufgerufen werden. 
  
Wenn Exchange-Datenbank-Transaktionsprotokolldateien überprüft werden, werden einige der Protokolldateien erforderlich sind, um die Datenbanken in der Speichergruppe in einen Zustand "clean Shutdown" ohne Datenverlust, schalten sein, während andere Protokolldateien möglicherweise nicht benötigt werden. Die Funktion **ErrCheckLogs** bestimmt die ältesten und neuesten Protokolldateien, die erforderlich sind, um die Datenbanken auf dem aktuellen Stand zu bringen. 
  
Die Funktion **ErrCheckLogs** überprüft die Protokolldateien in der angegebenen Pfade, die auch den Namen angegebenen drei Buchstaben Basisdatei haben, an die Funktion **ErrInit** übergeben. 
  
Wenn keine Fehler in den Protokolldateien gefunden werden, gibt **ErrCheckLogs** **ErrSuccess**zurück. 
  
Wenn eines der erforderlichen Protokolldateien beschädigt gefunden wird, gibt **ErrCheckLogs** einen Fehler zurück. 
  
Wenn Fehler nur in den Protokolldateien, die älter als die früheste erforderlich sind gefunden werden, wird die Funktion gibt **ErrSuccess** und wird die Rückgabeparameter **PfOnlyUnnecessaryLogCorrupt** auf **true**festgelegt. Die Anwendung sollte erkennen, dass Fehler in einige der die alte Protokolldateien sind, und wenn dies der Fall ist, wird möglicherweise der Benutzer gewarnt werden. Dieser Fehler sollten auf jeden Fall nicht Einfluss auf die allgemeine Integrität der Datenbank oder Einfluss darauf, ob die Protokolle vorwärts Wiedergabe erfolgreich ausgeführt werden kann.
  
In einer Protokolldatei nach den frühesten erstellt wurden, der bestimmt, **ErrCheckLogs** Protokoll ist erforderlich, die Funktion gibt einen Fehler zurück. Der Fehler wird zurückgegeben, selbst wenn in der Datei Fehlern gefunden wurde eine Protokolldatei, die später als generiert wurde ist erforderlich, um die Datenbank auf dem aktuellen Stand zu bringen. Obwohl es möglich, einen clean Shutdown-Status die Datenbanken mithilfe der identifizierten Protokolldateien Unterlagen werden würde, würde Transaktionen, die in den später beschädigten Protokolldateien angegeben nicht angewendet werden Datenverlust entstehen kann, wenn die Datenbank wiederhergestellt wird. 
  
Das Objekt **CChkSGFiles** bestimmt, ob alle Protokolldateien, die mit der Funktion **ErrInit** registriert tatsächlich aktiviert wurden. Wenn nicht alle Protokolle nicht erfolgreich überprüft wurden, die **ErrTerm** -Funktion gibt einen Fehler zurück. 
  
Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, können Sie die **ErrCheckLogs** -Funktion im Multithread-Teil der Anwendung aufrufen, jedoch können Sie nur einmal für jede **CCheckSGFiles** -Objekt aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.
  

