---
title: CChkSGFiles.PAGE_INFO-Struktur
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PAGE_INFO
api_type:
- dllExport
ms.assetid: 408335e1-6977-441f-bfad-ede791d1630c
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: fa66d253b4fc6bd5c29a39c5323f59bf323a906f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757743"
---
# <a name="cchksgfilespageinfo-struct"></a>CChkSGFiles.PAGE_INFO-Struktur

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Enthält Informationen für eine Exchange-Datenbank-Seite. Diese Struktur wird mit der **ErrCheckDbPages** -Funktion verwendet. 
  
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
  
Nicht signierte lange. Logische Seitenzahl der Datenbankseite überprüft werden soll. Dieser Wert muss vor dem Aufruf von **ErrCheckDbPages**festgelegt werden. Wenn die Anwendung die Datei basierend auf Datei Offsets liest und muss daher diese Datei Offsets auf logische Seitenzahlen zuordnen, finden Sie die **PgnoFromFileOffset** -Methode hilfreich sein, die den Wert für dieses Feld zu ermitteln. Dieser Wert **ErrCheckDbPages** nicht geändert. 
    
### <a name="fpageisinitialized"></a>fPageIsInitialized 
  
Boolean-Wert. TRUE gibt an, dass die Datenbankseite Daten enthält. Der Wert FALSE gibt an, dass die Seite nur Nullen enthält. **ErrCheckDbPages** legt diesen Wert fest. 
    
### <a name="fcorrectableerror"></a>fCorrectableError
  
Boolean-Wert. Der Wert TRUE gibt an, dass es einer Nichtübereinstimmung der Prüfsumme der Seite Datenbank erkannt wurde, aber es einen behebbaren Fehler ist. **ErrCheckDbPages** legt diesen Wert fest. 
    
### <a name="checksumactual"></a>checksumActual
  
64-Bit-Ganzzahl ohne Vorzeichen. Gibt den Prüfsummenwert in der Datenbank für diese logische Seite gespeichert. **ErrCheckDbPages** legt diesen Wert fest. 
    
### <a name="checksumexpected"></a>checksumExpected
  
64-Bit-Ganzzahl ohne Vorzeichen. Dies ist der erwartete Prüfsumme-Wert, der für die Datenbankseite berechnet wird. Es wird vom **ErrCheckDbPages**festgelegt. Wenn dieser Wert unterscheiden, die auf der Datenbankseite gespeichert ist (d. h., der Rückgabewert in **ChecksumActual**), **ErrCheckDbPages** werden anzugeben, dass ein Fehler auf dieser Datenbankseite gefunden wurde. 
    
### <a name="dbtime"></a>Zeitpunkt
  
64-Bit-Ganzzahl ohne Vorzeichen. **ErrCheckDbPages** wird dieser Member auf den Zeitstempel auf der Datenbankseite. 
    
### <a name="checksumpagestructure"></a>checksumPageStructure 
  
64-Bt-Ganzzahl ohne Vorzeichen. **ErrCheckDbPages** wird dieser Member auf den Wert berechnete Prüfsumme des Inhalts der Seite Ausschließen von Daten, die nicht erforderlich ist, wenn die logische Seite Gleichwertigkeit bestimmen. Beispielsweise ist es nicht erforderlich, die Datenwerte in nicht verwendeten Seite Datenbankspeicherplatzes berücksichtigt werden sollten. Dieser Member ist nur gültig, wenn die Werte **ChecksumActual** und **ChecksumExpected** entsprechen. 
    
### <a name="ulflags"></a>ulFlags
  
64-Bit-Ganzzahl ohne Vorzeichen. Reserviert für zukünftige Verwendung. Der Wert dieses Felds muss vor dem Aufruf von **ErrCheckDbPages**auf 0 (null) festgelegt werden.
    
## <a name="remarks"></a>Hinweise

Beim Aufruf der Funktion **ErrCheckDbPages** der **RgPageInfo** -Parameter ist ein Array von **Seite\_INFO** Strukturen. Es muss eine **Seite\_INFO** Struktur für jede Datenbankseite überprüft werden soll. 
  
Die Anwendung den **UlPgno** Member muss auf den korrekten Wert festgelegt, und den **UlFlags** Member muss auch auf 0 (null) festgelegt werden, bevor **ErrCheckDbPages**aufgerufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.
  

