---
title: CChkSGFiles.ErrTerm-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrTerm
api_type:
- dllExport
ms.assetid: eea20a55-4a2a-4209-ae79-dc1ee1cd631b
description: 'Zuletzt geändert: 25 Februar 2013'
ms.openlocfilehash: 099ec33663baa2414a0c28b90364523b6191c697
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756808"
---
# <a name="cchksgfileserrterm-function"></a>CChkSGFiles.ErrTerm-Funktion
  
**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Bietet einen allgemeinen Status der Überprüfung Datenbank- und Protokolldateien, die angibt, ob die Datenbankseiten und Protokolle erfolgreich überprüft wurden.
  
> [!IMPORTANT]
> Speichergruppen sind nicht verfügbar in Exchange 2013. Für die Abwärtskompatibilität mit Datenbanken und Speichergruppen in Exchange-Versionen vor Exchange Server 2010 können mit der API für CHKSGFILES Speichergruppen angeben. Wenn Sie für CHKSGFILES in Exchange 2013-Datenbanken ausführen, sollten Sie Parameter festlegen, die einen Gruppenbezeichner Speicher auf eine leere Zeichenfolge angeben. 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parameter

### <a name="ulflags"></a>ulFlags
  
Optionale Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der durch diesen Parameter übergebene Wert muss 0 (null) sein.
    
## <a name="return-value"></a>R�ckgabewert

Ein Fehlercode aus der [ERR](cchksgfiles-err-enumeration.md) -Aufzählung. 
  
## <a name="remarks"></a>Hinweise

Das Objekt **CChkSGFiles** bestimmt, ob alle Datenbanken, die mit der Funktion **ErrInit** registriert tatsächlich aktiviert wurden. Dieses Objekt verwendet der **ErrCheckDbPages** -Funktion zu überprüfen, ob die gleiche Anzahl von Datenbank, die Seiten von der Funktion **ErrCheckDbHeaders** identifizierten tatsächlich überprüft wurden. Wenn die richtige Anzahl von Seiten in jeder Datenbank nicht erfolgreich aktiviert sind, gibt die **ErrTerm** -Funktion einen Fehler zurück. 
  
Wenn die Anzahl von Datenbankseiten mit **ErrCheckDbPages** überprüft kleiner als der mit **ErrCheckDbHeaders**angegeben ist, diese Funktion erstellt einen Fehler im Windows-Ereignisprotokoll und **ErrTerm** gibt einen Fehler zurück. 
  
Wenn die Anzahl von Datenbankseiten überprüft mit **ErrCheckDbPages** größer als der mit **ErrCheckDbHeaders**angegeben ist, erstellt diese Funktion eine Warnung in der Windows-Ereignisprotokoll, um anzugeben, dass die Anwendung unnötig einige überprüft werden mehr als einmal Datenbankseiten. In diesem Fall ist erfolgreich, jedoch die **ErrTerm** -Funktion. 
  
Das Objekt **CChkSGFiles** bestimmt auch, ob die Protokolldateien mit **ErrInit** registriert tatsächlich aktiviert wurden. Wenn nicht alle Protokolle wurden erfolgreich überprüft, die **ErrTerm** -Funktion gibt einen Fehler zurück. 
  
Wenn **ErrTerm** einen Fehler zurückgibt, werden der erste Fehler, die, den es findet, den Obwohl den Status der Überprüfung für alle Datenbanken, die mit **ErrInit**registriert überprüft.
  
Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, müssen Sie die **ErrTerm** -Funktion in den einzelnen Thread Teil der Anwendung aufrufen, und Sie erreichen sie mehr als einmal für jedes Objekt **CCheckSGFiles** . 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 umfasst nur eine 64-Bit-Version von CHKSGFILES.
  
Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.
  

