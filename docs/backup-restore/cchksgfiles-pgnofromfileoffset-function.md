---
title: CChkSGFiles.PgnoFromFileOffset-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PgnoFromFileOffset
api_type:
- dllExport
ms.assetid: 3d69ca6d-5ed1-4038-859e-106e776eeec1
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: d42ba7c8178c6fccdddec0b5da88a972f51184c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756811"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a>CChkSGFiles.PgnoFromFileOffset-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Gibt die Anzahl der logischen Datenbank-Seite, die entspricht dem Index angegebene Bytearray in der physischen Datenbankdatei zurück. Wenn der Dateioffset ungültig ist oder für die Datenbanken nicht die **ErrCheckDbHeaders** -Funktion aufgerufen wurde, gibt diese Funktion 0 (null) zurück. 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a>Parameter

### <a name="ibfileoffset"></a>ibFileOffset
  
Input-Parameter. Der Abstand in eine Datenbankdatei in Byte.
    
## <a name="return-value"></a>R�ckgabewert

Die Datenbankdatei logische Seitenzahl, die den angegebenen Offset enthält.
  
## <a name="remarks"></a>Hinweise

Wenn der Parameter **IbFileOffset** ungültig ist, gibt die Funktion **PgnoFromFileOffset** 0 (null) zurück. 
  
**PgnoFromFileOffset** gibt auch 0 (null) zurück, wenn Sie nicht die **ErrCheckDbHeaders** -Funktion in der **CCheckSGFiles** -Instanz aufgerufen wurde. Sie müssen **ErrCheckDbHeaders** , um die Seitengröße der Datenbank und die Anzahl der reservierten Seiten für Datenbank-Kopfzeilen initialisieren aufrufen. 
  
Verwenden Sie **PgnoFromFileOffset** zum Füllen der **Seite\_INFO** Elemente im Rahmen der Vorbereitung für den Aufruf von **ErrCheckDbPages**-Struktur. Der Parameter **RgPageInfo** **ErrCheckDbPages** erfordert, dass jedes Element im Array eine **PAGE_INFO** -Struktur mit den **UlPgno** Memberwerte korrekt initialisiert werden. 
  
Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, können Sie die **PgnoFromFileOffset** -Funktion im Multithread-Teil der Anwendung anrufen. Beachten Sie, dass Sie in der Regel diese Funktion mehrere Male für jede Datenbank, die zu überprüfenden aufgerufen würde. 
  
## <a name="requirements"></a>Anforderungen

Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter die Anwendung ausgeführt wird, muss auf die Datenbank- und Protokolldateien Dateien gelesen haben, die überprüft werden sollen.
  

