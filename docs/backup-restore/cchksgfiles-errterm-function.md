---
title: CChkSGFiles. ErrTerm-Funktion
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
description: 'Letzte Änderung: 25. Februar 2013'
ms.openlocfilehash: 12b07fba69054d327c7250bbf83e4c77016e8b3f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466199"
---
# <a name="cchksgfileserrterm-function"></a>CChkSGFiles. ErrTerm-Funktion
  
**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Stellt einen allgemeinen Status der Datenbank-und Protokoll Überprüfung bereit, der angibt, ob alle Datenbankseiten und Protokolle erfolgreich überprüft wurden.
  
> [!IMPORTANT]
> Speichergruppen stehen in Exchange 2013 nicht zur Verfügung. Aus Gründen der Abwärtskompatibilität mit Datenbanken und Speichergruppen in Exchange-Versionen, die älter als Exchange Server 2010 sind, können Sie mit der CHKSGFILES-API Speichergruppen angeben. Wenn Sie CHKSGFILES für Exchange 2013 Datenbanken ausführen, sollten Sie Parameter festlegen, die einen Speichergruppen Bezeichner in eine leere Zeichenfolge angeben. 
  
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

Ein Fehlercode aus der [Err](cchksgfiles-err-enumeration.md) -Aufzählung. 
  
## <a name="remarks"></a>Bemerkungen

Das **CChkSGFiles** -Objekt bestimmt, ob alle Datenbanken, die mit der **ErrInit** -Funktion registriert wurden, tatsächlich überprüft wurden. Dieses Objekt verwendet die **ErrCheckDbPages** -Funktion, um zu überprüfen, ob die gleiche Anzahl von Datenbankseiten, die von der **ErrCheckDbHeaders** -Funktion identifiziert wurden, tatsächlich überprüft wurde. Wenn die richtige Anzahl von Seiten in jeder Datenbank nicht erfolgreich überprüft wird, gibt die **ErrTerm** -Funktion einen Fehler zurück. 
  
Wenn die Anzahl der mit **ErrCheckDbPages** geprüften Datenbankseiten kleiner als die von **ErrCheckDbHeaders**ist, erstellt diese Funktion einen Fehler im Windows-Ereignisprotokoll, und **ErrTerm** gibt einen Fehler zurück. 
  
Wenn die Anzahl der mit **ErrCheckDbPages** überprüften Datenbankseiten größer als der von **ErrCheckDbHeaders**ist, wird mit dieser Funktion eine Warnung im Windows-Ereignisprotokoll erstellt, um anzugeben, dass die Anwendung möglicherweise unnötig viele Datenbankseiten mehr als einmal überprüft. In diesem Fall ist die **ErrTerm** -Funktion jedoch erfolgreich. 
  
Das **CChkSGFiles** -Objekt bestimmt auch, ob die bei **ErrInit** registrierten Protokolldateien tatsächlich überprüft wurden. Wenn nicht alle Protokolle erfolgreich überprüft wurden, gibt die **ErrTerm** -Funktion einen Fehler zurück. 
  
Wenn **ErrTerm** einen Fehler zurückgibt, ist dies der erste gefundene Fehler, auch wenn der Überprüfungsstatus für alle mit **ErrInit**registrierten Datenbanken überprüft wird.
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **ErrTerm** -Funktion im Single-Thread-Teil der Anwendung aufrufen, und Sie können Sie für jedes **CCheckSGFiles** -Objekt nicht mehr als einmal aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version von CHKSGFILES.
  
Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.
  

