---
title: CChkSGFiles.ErrCheckDbHeaders-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbHeaders
api_type:
- dllExport
ms.assetid: 75289cd2-35b1-4f75-a651-dce01f1ddda1
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: a407019063b34970e883a00ca4f4d730935d7cba
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756810"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a>CChkSGFiles.ErrCheckDbHeaders-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013 
  
Überprüft die Kopfzeilen der Datenbankdateien, die von der Funktion **ErrInit** angegeben wurden. Diese Funktion gibt auch die Seitengröße und die Anzahl der Seiten in den einzelnen der angegebenen Datenbanken. 
  
```cs
Vitual ERRErrCheckDbHeaders  
(
        ULONG  * const pcbDbPageSize,
        ULONG  * const pcHeaderPagesPerDb,
        ULONG   const piDbErrorEncountered,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parameter

### <a name="pcbdbpagesize"></a>pcbDbPageSize 
  
Output-Parameter. Das Seitenformat der einzelnen angegebenen Datenbanken, in Byte.
    
### <a name="pcheaderpagesperdb"></a>pcHeaderPagesPerDb 
  
Output-Parameter. Die Anzahl der Seiten am Anfang jeder angegebene Datenbank, die von der Datenbank-Engine für die interne Verwendung reserviert sind. Beachten Sie, dass *nicht* Durchlauf Kopfzeilenseiten an die Funktion **ErrCheckDbPages** für die Validierung sollten. 
    
### <a name="pidberrorencountered"></a>piDbErrorEncountered
  
Output-Parameter. Wenn der Rückgabewert der Funktion einen Fehler weist darauf hin, wird dieser Parameter als Farbindex in der **ErrInit** -Funktion übergebenen Arrays **RgwszDb []** . Das indizierte Arrayelement steht für die Datenbank, in der der Fehler aufgetreten ist. Wenn die Funktion keinen Fehlerwert zurückgibt, ist dieser Parameterwert ungültig. 
    
### <a name="ulflags"></a>ulFlags 
  
Optionale Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der übergebene Wert muss 0 (null) sein.
    
## <a name="return-value"></a>R�ckgabewert

Diese Funktion gibt einen Fehlercode aus der [CChkSGFiles.ERR-Enumeration](cchksgfiles-err-enumeration.md).
  
## <a name="remarks"></a>Hinweise

**ErrCheckDbHeaders** überprüft, ob alle Datenbanken, die mit **ErrInit** registriert die gleiche Signatur und Datenbank Seite Protokollgröße verfügen. Sie können auch der niedrigste Wert des Parameters **GenMin** und der höchste Wert des Parameters **GenMax** verwenden, um die Protokolldateien zu bestimmen, die erforderlich sind, um alle registrierten Datenbanken auf einen clean Shutdown-Status zu bringen. 
  
Der Parameter **PiDbErrorEncountered** festgelegt ist, nur, wenn ein Fehler erkannt wird, wie eine ungleich NULL angegeben **ErrCheckDbHeaders** -Wert zurück. 
  
Tritt ein Fehler in dieser Funktion wird ein Error-Ereignis in das Ereignisprotokoll Windows Fehler hinzugefügt werden.
  
Sie können nur nach der **ErrInit** **ErrCheckDbHeaders** anrufen, und Sie müssen vor dem Aufruf von **ErrCheckDbPages** und **ErrCheckLogs**aufrufen.
  
Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, müssen Sie die **ErrCheckDbHeaders** -Funktion in den einzelnen Thread Teil aufrufen und können Sie nur einmal für jede **CCheckSGFiles** -Objekt aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.
  

