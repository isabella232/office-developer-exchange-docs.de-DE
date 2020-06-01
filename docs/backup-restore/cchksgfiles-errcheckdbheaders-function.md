---
title: CChkSGFiles. ErrCheckDbHeaders-Funktion
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
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: a62c5940322d3d7a71f2db93214f1e970fc6859b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455247"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a>CChkSGFiles. ErrCheckDbHeaders-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013 
  
Überprüft die Header der Datenbankdateien, die von der **ErrInit** -Funktion angegeben wurden. Diese Funktion gibt auch die Seitengröße und die Anzahl der Seiten in jeder der angegebenen Datenbanken zurück. 
  
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
  
Output-Parameter. Die Seitengröße jeder der angegebenen Datenbanken in Bytes.
    
### <a name="pcheaderpagesperdb"></a>pcHeaderPagesPerDb 
  
Output-Parameter. Die Anzahl der Seiten am Anfang jeder angegebenen Datenbank, die vom Datenbankmodul für die interne Verwendung reserviert werden. Beachten Sie, dass Sie *keine* Kopfzeilenseiten zur Validierung an die **ErrCheckDbPages** -Funktion übergeben sollten. 
    
### <a name="pidberrorencountered"></a>piDbErrorEncountered
  
Output-Parameter. Wenn der Rückgabewert der Funktion einen Fehler angibt, ist dieser Parameter ein Index in das **rgwszDb []** -Array, das an die **ErrInit** -Funktion übergeben wird. Das indizierte Array-Element stellt die Datenbank dar, in der der Fehler aufgetreten ist. Wenn die Funktion keinen Fehlerwert zurückgibt, ist dieser Parameterwert ungültig. 
    
### <a name="ulflags"></a>ulFlags 
  
Optionaler Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der übergebene Wert sollte 0 (null) sein.
    
## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen Fehlercode aus der [CChkSGFiles. err-Aufzählung](cchksgfiles-err-enumeration.md)zurück.
  
## <a name="remarks"></a>Bemerkungen

**ErrCheckDbHeaders** überprüft, ob alle mit **ErrInit** registrierten Datenbanken dieselbe Protokollsignatur und Datenbankseitengröße aufweisen. Sie können auch den niedrigsten **genMin** -Parameterwert und den höchsten Wert für den **genMax** -Parameter verwenden, um den Protokoll Dateiensatz zu ermitteln, die erforderlich sind, um alle registrierten Datenbanken in den Zustand "Clean Shutdown" zu versetzen. 
  
Der **piDbErrorEncountered** -Parameter wird nur festgelegt, wenn ein Fehler erkannt wird, wie durch einen **ErrCheckDbHeaders** -Rückgabewert ungleich NULL angegeben. 
  
Wenn in dieser Funktion ein Fehler auftritt, wird dem Windows-Fehlerereignisprotokoll ein Error-Ereignis hinzugefügt.
  
Sie können **ErrCheckDbHeaders** nur aufrufen, nachdem Sie **ErrInit**aufgerufen haben, und Sie müssen ihn aufrufen, bevor Sie **ErrCheckDbPages** und **ErrCheckLogs**aufrufen.
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **ErrCheckDbHeaders** -Funktion im Einzelthread-Teil aufrufen, und Sie können Sie für jedes **CCheckSGFiles** -Objekt nur einmal aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.
  

