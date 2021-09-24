---
title: CChkSGFiles.PgnoFromFileOffset-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PgnoFromFileOffset
api_type:
- dllExport
ms.assetid: 3d69ca6d-5ed1-4038-859e-106e776eeec1
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: 3e2845cc326520ad875dc8bda52bac3d7c2e2cfa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516244"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a>CChkSGFiles.PgnoFromFileOffset-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Gibt die seitenzahl der logischen Datenbank zurück, die dem angegebenen Byteindex in der physischen Datenbankdatei entspricht. Wenn der Dateiversatz ungültig ist oder die **ErrCheckDbHeaders-Funktion** für die Datenbanken nicht aufgerufen wurde, gibt diese Funktion 0 (null) zurück. 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a>Parameter

### <a name="ibfileoffset"></a>ibFileOffset
  
Eingabeparameter. Der Offset in eine Datenbankdatei in Bytes.
    
## <a name="return-value"></a>Rückgabewert

Die logische Seitenzahl der Datenbankdatei, die den angegebenen Offset enthält.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der **ibFileOffset-Parameter** ungültig ist, gibt die **PgnoFromFileOffset-Funktion** 0 (null) zurück. 
  
**PgnoFromFileOffset** gibt auch 0 (null) zurück, wenn Sie die **ErrCheckDbHeaders-Funktion** in der **CCheckSGFiles-Instanz** nicht aufgerufen haben. Sie müssen **ErrCheckDbHeaders** aufrufen, um die Größe der Datenbankseite und die Anzahl der Seiten zu initialisieren, die Datenbankheadern zugeordnet sind. 
  
Sie sollten **PgnoFromFileOffset** verwenden, um die **\_ SEITENINFO-Strukturelemente** in Vorbereitung auf den Aufruf **von ErrCheckDbPages** auszufüllen. Der **rgPageInfo-Parameter** für **ErrCheckDbPages** erfordert, dass jedes Element im Array eine **PAGE_INFO** Struktur ist, wobei die **ulPgno-Memberwerte** korrekt initialisiert werden. 
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, können Sie die **PgnoFromFileOffset-Funktion** im Multithreadteil der Anwendung aufrufen. Beachten Sie, dass Sie diese Funktion in der Regel mehrmals für jede überprüfte Datenbank aufrufen würden. 
  
## <a name="requirements"></a>Anforderungen

Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung ausgeführt wird, muss über Leseberechtigungen für die Datenbank und die Protokolldateien verfügen, die überprüft werden sollen.
  

