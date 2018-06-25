---
title: CChkSGFiles.ErrInit-Funktion
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
description: 'Zuletzt geändert: 03 März 2013'
ms.openlocfilehash: d4b76933a747fe4bf084061cf080bc68264132ed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756802"
---
# <a name="cchksgfileserrinit-function"></a>CChkSGFiles.ErrInit-Funktion
  
**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Initialisiert das **CChkSGFiles** -Objekt durch Angeben der Datenbanken überprüft werden soll und den Pfad und den Basisnamen des die Transaktionsprotokolldateien überprüft werden soll. Anwendungen sollte diese Funktion aufrufen, unmittelbar nach der erfolgreichen Aufruf der Funktion **neu** . 
  
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

### <a name="rgwszdb"></a>RgwszDb]
  
Input-Parameter. Ein Array, der angibt, die Datenbanken überprüft werden soll. Jedes Arrayelement ist eine Null terminierte Unicode-Zeichenfolge, die den Pfad und den Namen einer Datenbank überprüft werden soll.
    
### <a name="cdb"></a>cDB
  
Input-Parameter. Die Anzahl der gültige Datenbank Pfad Elementen im Array **RgwszDb** . 
    
#### <a name="wszlogpath"></a>wszLogPath
  
Input-Parameter. Der vollständige Pfad der die Transaktionsprotokolldateien in Form einer Null terminierte Unicode-Zeichenfolge überprüft werden soll.
    
### <a name="wszbasename"></a>wszBaseName
  
Input-Parameter. Die drei Buchstaben Basisnamen der Transaktionsprotokolldateien in Form einer Null terminierte Unicode-Zeichenfolge.
    
### <a name="ulflags"></a>ulFlags
  
Optionale Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der durch diesen Parameter übergebene Wert muss 0 (null) sein.
    
## <a name="return-value"></a>R�ckgabewert

Ein Fehlercode aus der [ERR](cchksgfiles-err-enumeration.md) -Aufzählung. 
  
## <a name="remarks"></a>Hinweise

Die Funktion **ErrInit** registriert die Datenbanken und Protokolldateien, die überprüft werden sollen. Diese Funktion muss aufgerufen werden, nachdem die **New** -Funktion wird aufgerufen, jedoch bevor andere **ChkSGFiles** aufgerufen. 
  
Sie müssen den Datenbanknamen und Pfad der Protokolldatei den Basisnamen als Null endende Unicode-Zeichenfolgen angeben.
  
Sie können nur die Datenbankdateien überprüfen nur die Protokolldateien oder die Datenbank- und Protokolldateien Dateien. Jedoch muss beim Aufruf von dieser Funktion die Anwendung mindestens eine Entität zu überprüfenden angeben. Übergeben von 0 (null) für **cDB** und NULL für **WszLogPath** gibt einen Fehler zurück. 
  
Wenn der Wert der **cDB** als 0 (null) ist, führt zu einem Fehler NULL für **RgwszDb** übergeben. Um die Datenbankdateien zu überprüfen, muss die Anwendung die Datenbanknamen bereitstellen. 
  
Wenn Sie NULL für **WszBaseName** übergeben wird, aber **WszLogPath** ist nicht NULL, wird ein Fehler zurückgegeben. Eine Protokolldatei-Basisname ist immer erforderlich, beim Überprüfen der Protokolldateien. 
  
Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, müssen Sie die **ErrInit** -Funktion in den einzelnen Thread Teil der Anwendung aufrufen und können Sie nur einmal für jede **CCheckSGFiles** -Objekt aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.
  

