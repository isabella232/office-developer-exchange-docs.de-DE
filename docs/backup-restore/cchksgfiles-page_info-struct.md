---
title: CChkSGFiles.PAGE_INFO-Struktur
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PAGE_INFO
api_type:
- dllExport
ms.assetid: 408335e1-6977-441f-bfad-ede791d1630c
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: f324ec9aca6f94911041c227ce039139292a10aa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516258"
---
# <a name="cchksgfilespage_info-struct"></a>CChkSGFiles.PAGE_INFO-Struktur

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Enthält Informationen für eine Exchange Datenbankseite. Diese Struktur wird mit der **ErrCheckDbPages-Funktion** verwendet. 
  
```cs
Struct PAGE_INFO  
{
        ULONGulPgno;
        BOOLfPageIsInitialized : 1;
        BOOLfCorrectableError : 1;
        ULONGLONGchecksumActual;
        ULONGLONGchecksumExpected;
        ULONGLONGdbTime;
        ULONGLONGchecksumPageStructure;
        ULONGLONGulFlags;
}

```

## <a name="members"></a>Members

### <a name="ulpgno"></a>ulPgNo
  
Unsigned Long. Logische Seitenzahl der zu überprüfenden Datenbankseite. Dieser Wert muss vor dem Aufrufen **von ErrCheckDbPages** festgelegt werden. Wenn die Anwendung die Datei basierend auf Dateiversatz liest und diese Dateiversätze daher logischen Seitenzahlen zuordnen muss, wird die **PgnoFromFileOffset-Methode** hilfreich sein, um den Wert für dieses Feld zu bestimmen. **ErrCheckDbPages** ändert diesen Wert nicht. 
    
### <a name="fpageisinitialized"></a>fPageIsInitialized 
  
Boolean. Der Wert TRUE gibt an, dass die Datenbankseite Daten enthält. Der Wert FALSE gibt an, dass die Seite nur Nullen enthält. **ErrCheckDbPages** legt diesen Wert fest. 
    
### <a name="fcorrectableerror"></a>fCorrectableError
  
Boolean. Der Wert TRUE gibt an, dass auf der Datenbankseite ein Prüfsummenkonflikt erkannt wurde, es sich jedoch um einen korrektierbaren Fehler handelt. **ErrCheckDbPages** legt diesen Wert fest. 
    
### <a name="checksumactual"></a>checksumActual
  
64-Bit-Ganzzahl ohne Vorzeichen. Gibt den Prüfsummenwert an, der in der Datenbank für diese logische Seite gespeichert ist. **ErrCheckDbPages** legt diesen Wert fest. 
    
### <a name="checksumexpected"></a>checksumExpected
  
64-Bit-Ganzzahl ohne Vorzeichen. Dies ist der erwartete Prüfsummenwert, der für die Datenbankseite berechnet wird. sie wird von **ErrCheckDbPages** festgelegt. Wenn sich dieser Wert von dem auf der Datenbankseite gespeicherten unterscheidet (d. h. der in **checksumActual** zurückgegebene Wert), gibt **ErrCheckDbPages** an, dass auf dieser Datenbankseite ein Fehler gefunden wurde. 
    
### <a name="dbtime"></a>dbTime
  
64-Bit-Ganzzahl ohne Vorzeichen. **ErrCheckDbPages** legt diesen Member auf den Zeitstempel auf der Datenbankseite fest. 
    
### <a name="checksumpagestructure"></a>checksumPageStructure 
  
64-bt-Ganzzahl ohne Vorzeichen. **ErrCheckDbPages** legt diesen Member auf den berechneten Prüfsummenwert des Inhalts der Seite ohne Daten fest, die beim Ermitteln der logischen Seitenäquivalenz nicht erforderlich sind. Es ist beispielsweise nicht erforderlich, die Datenwerte im nicht verwendeten Datenbankseitenbereich zu berücksichtigen. Dieser Member ist nur gültig, wenn die Werte **"checksumActual"**  und  **"checksumExpected"**  gleicheinander sind. 
    
### <a name="ulflags"></a>ulFlags
  
64-Bit-Ganzzahl ohne Vorzeichen. Reserviert für zukünftige Verwendung. Der Wert dieses Felds muss auf 0 (null) festgelegt werden, bevor **ErrCheckDbPages** aufgerufen wird.
    
## <a name="remarks"></a>HinwBemerkungeneise

Beim Aufrufen der **ErrCheckDbPages-Funktion** ist der **rgPageInfo-Parameter** ein Array von **PAGE \_ INFO-Strukturen.** Es muss eine **PAGE \_ INFO-Struktur** vorhanden sein, damit jede Datenbankseite überprüft werden kann. 
  
Die Anwendung muss den **ulPgno-Member**  auf den richtigen Wert festlegen und außerdem den  **ulFlags-Member**  auf 0 (null) festlegen, bevor **ErrCheckDbPages** aufgerufen wird. 
  
## <a name="requirements"></a>Anforderungen

Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung ausgeführt wird, muss über Lesezugriffsberechtigungen für die Datenbank und die Protokolldateien verfügen, die überprüft werden sollen.
  

