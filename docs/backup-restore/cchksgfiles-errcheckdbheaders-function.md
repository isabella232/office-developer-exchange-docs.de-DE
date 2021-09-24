---
title: CChkSGFiles.ErrCheckDbHeaders-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrCheckDbHeaders
api_type:
- dllExport
ms.assetid: 75289cd2-35b1-4f75-a651-dce01f1ddda1
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: 215a0d1126fce48b7e3800016619b0c52915312b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510470"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a>CChkSGFiles.ErrCheckDbHeaders-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013 
  
Überprüft die Kopfzeilen der Datenbankdateien, die von der **ErrInit-Funktion** angegeben wurden. Diese Funktion gibt auch die Seitengröße und die Seitenanzahl in jeder der angegebenen Datenbanken zurück. 
  
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

### <a name="pcbdbpagesize"></a>"pwDbPageSize" 
  
Output-Parameter. Die Seitengröße jeder der angegebenen Datenbanken in Byte.
    
### <a name="pcheaderpagesperdb"></a>pcHeaderPagesPerDb 
  
Output-Parameter. Die Anzahl der Seiten am Anfang jeder angegebenen Datenbank, die vom Datenbankmodul für die interne Verwendung reserviert sind. Beachten Sie, dass Sie *keine* Kopfzeilenseiten zur Überprüfung an die **ErrCheckDbPages-Funktion** übergeben sollten. 
    
### <a name="pidberrorencountered"></a>piDbErrorEncountered
  
Output-Parameter. Wenn der Rückgabewert der Funktion einen Fehler angibt, ist dieser Parameter ein Index in das **rgwszDb[]-Array,** das an die **ErrInit-Funktion** übergeben wird. Das indizierte Arrayelement stellt die Datenbank dar, in der der Fehler aufgetreten ist. Wenn die Funktion keinen Fehlerwert zurückgibt, ist dieser Parameterwert ungültig. 
    
### <a name="ulflags"></a>ulFlags 
  
Optionaler Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der übergebene Wert sollte 0 (Null) sein.
    
## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen Fehlercode aus der [CChkSGFiles.ERR -Enumeration](cchksgfiles-err-enumeration.md)zurück.
  
## <a name="remarks"></a>HinwBemerkungeneise

**ErrCheckDbHeaders** überprüft, ob alle bei **ErrInit** registrierten Datenbanken über die gleiche Protokollsignatur und datenbankseitige Größe verfügen. Sie können auch den niedrigsten **GenMin-Parameterwert** und den höchsten **GenMax-Parameterwert** verwenden, um den Satz von Protokolldateien zu bestimmen, die erforderlich sind, um alle registrierten Datenbanken in einen Zustand des sauberen Herunterfahrens zu versetzen. 
  
Der **PiDbErrorEncountered-Parameter** wird nur festgelegt, wenn ein Fehler erkannt wird, wie durch einen Rückgabewert ungleich Null **ErrCheckDbHeaders** angegeben. 
  
Wenn in dieser Funktion ein Fehler auftritt, wird dem Windows Fehlerereignisprotokoll ein Fehlerereignis hinzugefügt.
  
Sie können **ErrCheckDbHeaders** nur nach dem Aufrufen **von ErrInit** aufrufen, und Sie müssen es vor dem Aufrufen **von ErrCheckDbPages** und **ErrCheckLogs** aufrufen.
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **ErrCheckDbHeaders-Funktion** im Singlethread-Teil aufrufen, und Sie können sie nur einmal für jedes **CCheckSGFiles-Objekt** aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung ausgeführt wird, muss über Lesezugriffsberechtigungen für die Datenbank und die Protokolldateien verfügen, die überprüft werden sollen.
  

