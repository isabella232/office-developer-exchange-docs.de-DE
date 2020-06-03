---
title: CChkSGFiles. PgnoFromFileOffset-Funktion
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
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: 3c8f749a03b4aa251bf9312eba5d7e2d46c91fae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452895"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a>CChkSGFiles. PgnoFromFileOffset-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Gibt die Seitenzahl der logischen Datenbank zurück, die dem angegebenen Byte Index in der physischen Datenbankdatei entspricht. Wenn der Dateioffset ungültig ist oder die **ErrCheckDbHeaders** -Funktion nicht für die Datenbanken aufgerufen wurde, gibt diese Funktion 0 (null) zurück. 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a>Parameter

### <a name="ibfileoffset"></a>ibFileOffset
  
Eingabeparameter. Der Offset in einer Datenbankdatei in Bytes.
    
## <a name="return-value"></a>Rückgabewert

Die logische Seitenzahl der Datenbankdatei, die den angegebenen Offset enthält.
  
## <a name="remarks"></a>Bemerkungen

Wenn der **ibFileOffset** -Parameter ungültig ist, gibt die **PgnoFromFileOffset** -Funktion 0 (null) zurück. 
  
**PgnoFromFileOffset** gibt auch 0 (null) zurück, wenn Sie die **ErrCheckDbHeaders** -Funktion nicht für die **CCheckSGFiles** -Instanz aufgerufen haben. Sie müssen **ErrCheckDbHeaders** aufrufen, um die Datenbankseitengröße und die Anzahl der Seiten zu initialisieren, die den Daten Bank Headern zugeordnet sind. 
  
Sie sollten **PgnoFromFileOffset** verwenden, um die **Seiten \_ Info** Strukturelemente in Vorbereitung auf das Aufrufen von **ErrCheckDbPages**auszufüllen. Der **rgPageInfo** -Parameter für **ErrCheckDbPages** erfordert, dass jedes Element im Array eine **PAGE_INFO** Struktur ist, wobei die **ulPgno** -Elementwerte ordnungsgemäß initialisiert werden. 
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, können Sie die **PgnoFromFileOffset** -Funktion im Multithread-Teil der Anwendung aufrufen. Beachten Sie, dass Sie diese Funktion in der Regel für jede geprüfte Datenbank mehrmals aufrufen würden. 
  
## <a name="requirements"></a>Anforderungen

Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung läuft, muss über Leseberechtigung für die zu überprüfende Datenbank-und Protokolldateien verfügen.
  

