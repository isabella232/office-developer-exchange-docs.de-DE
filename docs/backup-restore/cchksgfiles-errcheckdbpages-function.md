---
title: CChkSGFiles.ErrCheckDbPages-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrCheckDbPages
api_type:
- dllExport
ms.assetid: 5e981a7c-28cd-470c-b7eb-606463e9dd05
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: e458e4ad552abfebb7611822a6e756bdd2ac6350
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510407"
---
# <a name="cchksgfileserrcheckdbpages-function"></a>CChkSGFiles.ErrCheckDbPages-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Überprüft einen Seitenbereich in einer angegebenen Datenbank. 
  
```cs
Vitual ERRErrCheckDbPages  
(
    Const ULONGiDb,
    Const VOID  * const pvPageBuffer,
    Const ULONGcbPageBuffer,
    PAGE_INFOrgPageInfo[],
    Const ULONGcPageInfo,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parameter

### <a name="idb"></a>Idb
  
Eingabeparameter. Ein Index in das Array von Datenbanken, die im **Parameter rgwszDb[]** für die **ErrInit-Funktion** angegeben sind. Die durch diesen Parameter indizierte Datenbank wird überprüft. 
    
### <a name="pvpagebuffer"></a>pvPageBuffer 
  
Eingabeparameter. Ein Zeiger auf einen Puffer, der eine oder mehrere zu überprüfende Datenbankseiten enthält. Die Größe des Puffers muss ein Vielfaches der Datenbankseitengröße sein, wie im **parameter "gifDbPageSize"** von der **ErrCheckDbHeaders-Funktion** zurückgegeben. Die aufrufende Anwendung muss den Puffer mit dem Inhalt der Datenbankseite füllen, bevor **ErrCheckDbPages** aufgerufen wird.
    
### <a name="cbpagebuffer"></a>cbPageBuffer
  
Eingabeparameter. Die Größe des **pvPageBuffer-Parameters** in Bytes. Dieser Wert muss ein Vielfaches der Datenbankseitengröße sein, wie im **parameter "gifDbPageSize"** von der **ErrCheckDbHeaders-Funktion** zurückgegeben. 
    
### <a name="rgpageinfo"></a>rgPageInfo[] 
  
Eingabe-/Ausgabeparameter. Ein Array von **PAGE \_ INFO-Strukturen,** die **ErrCheckDbPages** mit detaillierten Ergebnissen jeder überprüften Datenbankseite ausfüllt. Das Array muss ein Element für jede Datenbankseite aufweisen, die im **Parameter "pvPageBuffer"** übergeben wird, und das **UlPgno-Feld** in jeder **PAGE \_ INFO-Struktur** muss auf die logische Seitenzahl festgelegt werden, die der Datenbankseite entspricht. Weitere Informationen finden Sie weiter unten in diesem Thema unter "Hinweise". 
    
### <a name="cpageinfo"></a>cPageInfo
  
Eingabeparameter. Die Anzahl der Einträge im **rgPageInfo[]-Array.** Dieser Wert muss der Anzahl der Datenbankseiten entsprechen, die im **Parameter "pvPageBuffer"** übergeben werden. 
    
### <a name="ulflags"></a>ulFlags 
  
Optionaler Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der in diesem Parameter übergebene Wert sollte 0 (null) sein.
    
## <a name="return-value"></a>Rückgabewert

Ein Fehlercode aus der [ERR-Enumeration.](cchksgfiles-err-enumeration.md) 
  
## <a name="remarks"></a>HinwBemerkungeneise

Beachten Sie, dass Sie die Datenbank im Datenbankarray angegeben haben müssen, das an die **ErrInit-Funktion** übergeben wird. Außerdem muss **ErrCheckDbHeaders** vor **ErrCheckDbPages** aufgerufen werden.
  
Die aufrufende Anwendung muss einen Speicherpuffer zuordnen, der groß genug ist, um die zu überprüfenden Datenbankseiten zu speichern. Die Anwendung ist für das Auffüllen des Puffers mit dem Inhalt einer oder mehrerer solcher Datenbankseiten verantwortlich. 
  
Die aufrufende Anwendung muss **ErrCheckDbHeaders** vor dem Aufrufen **von ErrCheckDbPages** aufrufen. Diese Funktion kann so oft wie nötig aufgerufen werden, um alle Seiten in allen zu überprüfenden Datenbankdateien abzudecken.
  
Im Parameter **rgPageInfo[]** enthält jedes zurückgegebene Element Informationen zur Datenbankseite in einer **PAGE \_ INFO-Struktur.** Wenn die **ErrCheckDbPages-Funktion** einen Fehler zurückgibt, sollte die Anwendung jede **PAGE \_ INFO-Struktur** überprüfen, um zu ermitteln, auf welcher Seite der Fehler gefunden wurde. Wenn Sie beispielsweise die Werte **checksumActual** und **checksumExpected** vergleichen, wird angegeben, ob auf dieser Datenbankseite ein Prüfsummenfehler erkannt wurde. 
  
Wenn **ErrCheckDbPages** Fehler im Datenbankinhalt erkennt, wird ein Windows Fehlerereignisprotokolleintrag erstellt. 
  
Das **CChkSGFiles-Objekt** bestimmt, ob alle mit der **ErrInit-Funktion** registrierten Datenbanken tatsächlich überprüft wurden. Insbesondere verwendet **CChkSGFiles** die **ErrCheckDbPages-Funktion,** um zu bestimmen, ob die gleiche Anzahl von Datenbankseiten, die von **ErrCheckDbHeaders** angegeben wurden, tatsächlich überprüft wurden. Wenn die richtige Anzahl von Seiten in jeder Datenbank nicht erfolgreich überprüft wurde, gibt die **ErrTerm-Funktion** einen Fehler zurück. 
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, können Sie die **ErrCheckDbPages-Funktion** im Multithreadteil der Anwendung aufrufen. Beachten Sie, dass **ErrCheckDbPages** in der Regel mehrmals für jede überprüfte Datenbank aufgerufen wird. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung ausgeführt wird, muss über Leseberechtigungen für die Datenbank und die Protokolldateien verfügen, die überprüft werden sollen.
  

