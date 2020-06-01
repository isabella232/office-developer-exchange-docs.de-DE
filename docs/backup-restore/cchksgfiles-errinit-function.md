---
title: CChkSGFiles. ErrInit-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrInit
api_type:
- dllExport
ms.assetid: 61bb3af1-8b51-4bae-8e25-90a4dc1226c5
description: 'Letzte Änderung: März 03, 2013'
ms.openlocfilehash: c881691e7c1ba83a396e659f6aac0328625e49a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457011"
---
# <a name="cchksgfileserrinit-function"></a>CChkSGFiles. ErrInit-Funktion
  
**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Initialisiert das **CChkSGFiles** -Objekt, indem die zu überprüfenden Datenbanken und der Pfad und der Basis Name der zu überprüfenden Transaktionsprotokolldateien angegeben werden. Anwendungen sollten diese Funktion sofort aufrufen, nachdem die **neue** Funktion erfolgreich aufgerufen wurde. 
  
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
  
Eingabeparameter. Ein Array, das angibt, welche Datenbanken überprüft werden sollen. Jedes Array-Element ist eine mit NULL endende Unicode-Zeichenfolge, die den Pfad und den Dateinamen einer Datenbank enthält, die überprüft werden soll.
    
### <a name="cdb"></a>cDB
  
Eingabeparameter. Die Anzahl gültiger Datenbankpfad Elemente im **rgwszDb** -Array. 
    
#### <a name="wszlogpath"></a>wszLogPath
  
Eingabeparameter. Der vollständige Pfad der zu überprüfenden Transaktionsprotokolldateien in Form einer null-terminierten Unicode-Zeichenfolge.
    
### <a name="wszbasename"></a>wszBaseName
  
Eingabeparameter. Der dreistellige Basis Name der Exchange-Transaktionsprotokolldateien in Form einer null-terminierten Unicode-Zeichenfolge.
    
### <a name="ulflags"></a>ulFlags
  
Optionaler Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der von diesem Parameter übergebene Wert sollte 0 (null) sein.
    
## <a name="return-value"></a>Rückgabewert

Ein Fehlercode aus der [Err](cchksgfiles-err-enumeration.md) -Aufzählung. 
  
## <a name="remarks"></a>Bemerkungen

Die **ErrInit** -Funktion registriert die Datenbanken und Protokolldateien, die überprüft werden sollen. Diese Funktion muss aufgerufen werden, nachdem die **neue** Funktion aufgerufen wurde, aber bevor eine andere **ChkSGFiles** -Funktion aufgerufen wird. 
  
Sie müssen alle Datenbanknamen, den Protokolldateipfad und den Basisnamen als NULL-terminierte Unicode-Zeichenfolgen angeben.
  
Sie können nur die Datenbankdateien, nur die Protokolldateien oder sowohl die Datenbank-als auch die Protokolldateien überprüfen. Wenn diese Funktion aufgerufen wird, muss die Anwendung jedoch mindestens eine Entität angeben, die überprüft werden soll. Durch die Übergabe von 0 (null) für **cDB** und NULL für **wszLogPath** wird ein Fehler zurückgegeben. 
  
Wenn der Wert von **cDB** nicht 0 (null) ist, führt die Übergabe von NULL für **rgwszDb** zu einem Fehler. Um die Datenbankdateien zu überprüfen, muss die Anwendung die Datenbanknamen bereitstellen. 
  
Wenn NULL für **wszBaseName** übergeben wird, **wszLogPath** jedoch nicht NULL ist, wird ein Fehler zurückgegeben. Bei der Überprüfung von Protokolldateien ist immer ein Protokolldatei-Basis Name erforderlich. 
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **ErrInit** -Funktion im Single-Thread-Teil der Anwendung aufrufen, und Sie können Sie nur einmal für jedes **CCheckSGFiles** -Objekt aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.
  

