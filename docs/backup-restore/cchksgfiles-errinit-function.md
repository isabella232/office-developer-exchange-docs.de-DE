---
title: CChkSGFiles.ErrInit-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrInit
api_type:
- dllExport
ms.assetid: 61bb3af1-8b51-4bae-8e25-90a4dc1226c5
description: 'Last modified: March 03, 2013'
ms.openlocfilehash: ccb5293e35f20328181c4cf1cb5f0eddbb42e03f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516293"
---
# <a name="cchksgfileserrinit-function"></a>CChkSGFiles.ErrInit-Funktion
  
**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Initialisiert das **CChkSGFiles-Objekt,** indem die zu überprüfenden Datenbanken sowie der Pfad und der Basisname der zu überprüfenden Transaktionsprotokolldateien angegeben werden. Anwendungen sollten diese Funktion unmittelbar nach dem erfolgreichen Aufrufen der **New-Funktion** aufrufen. 
  
```cs
Vitual ERRErrInit  
(
    Const WCHAR  * const rgwszDb[],
    Const ULONGcDB,
    __in_z const WCHAR  * const wszLogPath,
    __in_z const WCHAR  * const wszBaseName,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parameter

### <a name="rgwszdb"></a>rgwszDb[]
  
Eingabeparameter. Ein Array, das die zu überprüfenden Datenbanken angibt. Jedes Arrayelement ist eine Unicode-Zeichenfolge mit NULL-Termin, die den Pfad und den Dateinamen einer zu überprüfenden Datenbank enthält.
    
### <a name="cdb"></a>Cdb
  
Eingabeparameter. Die Anzahl der gültigen Datenbankpfadelemente im **rgwszDb-Array.** 
    
#### <a name="wszlogpath"></a>wszLogPath
  
Eingabeparameter. Der vollständige Pfad der zu überprüfenden Transaktionsprotokolldateien in Form einer Unicode-Zeichenfolge mit NULL-Terminierung.
    
### <a name="wszbasename"></a>wszBaseName
  
Eingabeparameter. Der aus drei Buchstaben bestehende Basisname der Exchange Transaktionsprotokolldateien in Form einer Unicode-Zeichenfolge mit NULL-Terminierung.
    
### <a name="ulflags"></a>ulFlags
  
Optionaler Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der von diesem Parameter übergebene Wert sollte 0 (null) sein.
    
## <a name="return-value"></a>Rückgabewert

Ein Fehlercode aus der [ERR-Enumeration.](cchksgfiles-err-enumeration.md) 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **ErrInit-Funktion** registriert die Datenbanken und Protokolldateien, die überprüft werden sollen. Diese Funktion muss aufgerufen werden, nachdem die **New-Funktion** aufgerufen wurde, aber bevor eine andere **ChkSGFiles-Funktion** aufgerufen wird. 
  
Sie müssen alle Datenbanknamen, den Protokolldateipfad und den Basisnamen als Unicode-Zeichenfolgen mit NULL-Terminierung angeben.
  
Sie können nur die Datenbankdateien, nur die Protokolldateien oder sowohl die Datenbank als auch die Protokolldateien überprüfen. Beim Aufrufen dieser Funktion muss die Anwendung jedoch mindestens eine zu überprüfende Entität angeben. Wenn Sie 0 (null) für  **cDB**  und NULL für  **wszLogPath**  übergeben, wird ein Fehler zurückgegeben. 
  
Wenn der Wert von  **cDB**  nicht 0 (null) ist, führt das Übergeben von NULL für  **rgwszDb**  zu einem Fehler. Um die Datenbankdateien zu überprüfen, muss die Anwendung die Datenbanknamen angeben. 
  
Wenn NULL für  **wszBaseName**  übergeben wird,  **wszLogPath**  jedoch nicht NULL ist, wird ein Fehler zurückgegeben. Bei der Überprüfung von Protokolldateien ist immer ein Protokolldateibasisname erforderlich. 
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **ErrInit-Funktion** im Singlethreadteil der Anwendung aufrufen, und Sie können sie nur einmal für jedes **CCheckSGFiles-Objekt** aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung ausgeführt wird, muss über Lesezugriffsberechtigungen für die Datenbank und die Protokolldateien verfügen, die überprüft werden sollen.
  

