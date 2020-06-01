---
title: CChkSGFiles. PAGE_INFO-Struktur
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
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: 5ec9f4303b26ea95b125adac6943945ae1276439
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456339"
---
# <a name="cchksgfilespage_info-struct"></a>CChkSGFiles. PAGE_INFO-Struktur

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Speichert Informationen für eine Exchange-Datenbankseite. Diese Struktur wird mit der **ErrCheckDbPages** -Funktion verwendet. 
  
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
  
Lange ohne Vorzeichen. Logische Seitenzahl der zu überprüfenden Datenbankseite. Dieser Wert muss festgelegt werden, bevor **ErrCheckDbPages**aufgerufen wird. Wenn die Anwendung die Datei auf der Grundlage von Datei Offsets liest und diese Datei Offsets daher logischen Seitenzahlen zuordnen muss, finden Sie die **PgnoFromFileOffset** -Methode hilfreich, um den Wert für dieses Feld zu ermitteln. Dieser Wert wird von **ErrCheckDbPages** nicht geändert. 
    
### <a name="fpageisinitialized"></a>fPageIsInitialized 
  
Boolean. Der Wert true gibt an, dass die Datenbankseite Daten enthält. Der Wert false gibt an, dass die Seite nur Nullen enthält. **ErrCheckDbPages** legt diesen Wert fest. 
    
### <a name="fcorrectableerror"></a>fCorrectableError
  
Boolean. Der Wert true gibt an, dass auf der Datenbankseite ein Prüfsummen Konflikt festgestellt wurde, dass es sich jedoch um einen korrigierbaren Fehler handelt. **ErrCheckDbPages** legt diesen Wert fest. 
    
### <a name="checksumactual"></a>checksumActual
  
Vorzeichenlose 64-Bit-Ganzzahl. Gibt den in der Datenbank für diese logische Seite gespeicherten Prüfsummenwert an. **ErrCheckDbPages** legt diesen Wert fest. 
    
### <a name="checksumexpected"></a>checksumExpected
  
Vorzeichenlose 64-Bit-Ganzzahl. Dies ist der erwartete Prüfsummenwert, der für die Datenbankseite berechnet wird; Sie wird von **ErrCheckDbPages**festgelegt. Wenn sich dieser Wert von dem auf der Datenbankseite (also dem in **checksumActual**zurückgegebenen Wert) unterscheidet, gibt **ErrCheckDbPages** an, dass auf dieser Datenbankseite ein Fehler gefunden wurde. 
    
### <a name="dbtime"></a>dbTime
  
Vorzeichenlose 64-Bit-Ganzzahl. **ErrCheckDbPages** legt dieses Element auf den Zeitstempel auf der Datenbankseite fest. 
    
### <a name="checksumpagestructure"></a>checksumPageStructure 
  
Unsigned 64-BT Integer. **ErrCheckDbPages** legt dieses Element auf den berechneten Prüfsummenwert des Inhalts der Seite mit Ausnahme von Daten fest, die bei der Bestimmung der Äquivalenz der logischen Seite nicht erforderlich sind. Beispielsweise ist es nicht erforderlich, die Datenwerte in nicht verwendeten Datenbankseiten zu überprüfen. Dieser Member ist nur gültig, wenn die **checksumActual** -und **checksumExpected** -Werte einander gleich sind. 
    
### <a name="ulflags"></a>ulFlags
  
Vorzeichenlose 64-Bit-Ganzzahl. Reserviert für zukünftige Verwendung. Der Wert dieses Felds muss auf 0 (null) festgelegt werden, bevor **ErrCheckDbPages**aufgerufen wird.
    
## <a name="remarks"></a>Bemerkungen

Beim Aufrufen der **ErrCheckDbPages** -Funktion ist der **rgPageInfo** -Parameter ein Array von **Seiten \_ Info** Strukturen. Es muss eine **Seiten \_ Info** Struktur für jede zu überprüfende Datenbankseite geben. 
  
Die Anwendung muss das **ulPgno** -Element auf den richtigen Wert festlegen und das **ulFlags** -Element auch auf 0 (null) festlegen, bevor **ErrCheckDbPages**aufgerufen wird. 
  
## <a name="requirements"></a>Anforderungen

Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.
  

