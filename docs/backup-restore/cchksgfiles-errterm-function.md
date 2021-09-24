---
title: CChkSGFiles.ErrTerm-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrTerm
api_type:
- dllExport
ms.assetid: eea20a55-4a2a-4209-ae79-dc1ee1cd631b
description: 'Last modified: February 25, 2013'
ms.openlocfilehash: 152fd613ef461d8c1ef69401237cfea09cd32b08
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516286"
---
# <a name="cchksgfileserrterm-function"></a>CChkSGFiles.ErrTerm-Funktion
  
**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Stellt einen Gesamtstatus der Datenbank- und Protokollüberprüfung bereit, der angibt, ob alle Datenbankseiten und Protokolle erfolgreich überprüft wurden.
  
> [!IMPORTANT]
> Storage Gruppen sind in Exchange 2013 nicht verfügbar. Aus Gründen der Abwärtskompatibilität mit Datenbanken und Speichergruppen in Früheren Versionen von Exchange als Exchange Server 2010 können Sie mit der CHKSGFILES-API Speichergruppen angeben. Wenn Sie CHKSGFILES für Exchange 2013-Datenbanken ausführen, sollten Sie Parameter festlegen, die einen Speichergruppenbezeichner auf eine leere Zeichenfolge festlegen. 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parameter

### <a name="ulflags"></a>ulFlags
  
Optionaler Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der von diesem Parameter übergebene Wert sollte 0 (null) sein.
    
## <a name="return-value"></a>Rückgabewert

Ein Fehlercode aus der [ERR-Enumeration.](cchksgfiles-err-enumeration.md) 
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **CChkSGFiles-Objekt** bestimmt, ob alle mit der **ErrInit-Funktion** registrierten Datenbanken tatsächlich überprüft wurden. Dieses Objekt verwendet die **ErrCheckDbPages-Funktion,** um zu überprüfen, ob die gleiche Anzahl von Datenbankseiten, die von der **ErrCheckDbHeaders-Funktion** identifiziert wurden, tatsächlich überprüft wurde. Wenn die richtige Anzahl von Seiten in jeder Datenbank nicht erfolgreich überprüft wird, gibt die **ErrTerm-Funktion** einen Fehler zurück. 
  
Wenn die Anzahl der mit **ErrCheckDbPages** überprüften Datenbankseiten kleiner ist als die von **ErrCheckDbHeaders** angegebene, erstellt diese Funktion einen Fehler im Windows Ereignisprotokoll, und **ErrTerm** gibt einen Fehler zurück. 
  
Wenn die Anzahl der mit **ErrCheckDbPages** überprüften Datenbankseiten größer ist als die von **ErrCheckDbHeaders** angegebene, erstellt diese Funktion eine Warnung im Windows Ereignisprotokoll, um anzugeben, dass die Anwendung einige Datenbankseiten möglicherweise unnötig mehrmals überprüft. In diesem Fall ist die **ErrTerm-Funktion** jedoch erfolgreich. 
  
Das **CChkSGFiles-Objekt** bestimmt auch, ob die bei **ErrInit** registrierten Protokolldateien tatsächlich überprüft wurden. Wenn nicht alle Protokolle erfolgreich überprüft wurden, gibt die **ErrTerm-Funktion** einen Fehler zurück. 
  
Wenn **ErrTerm** einen Fehler zurückgibt, ist dies der erste gefundene Fehler, obwohl der Überprüfungsstatus für alle Datenbanken überprüft wird, die bei **ErrInit** registriert sind.
  
Wenn Sie CHKSGFILES in einer Multithreadanwendung verwenden, müssen Sie die **ErrTerm-Funktion** im Singlethreadteil der Anwendung aufrufen, und Sie können sie nicht mehr als einmal für jedes **CCheckSGFiles-Objekt** aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version von CHKSGFILES.
  
Das Konto, unter dem die Anwendung ausgeführt wird, muss über Lesezugriffsberechtigungen für die Datenbank und die Protokolldateien verfügen, die überprüft werden sollen.
  

