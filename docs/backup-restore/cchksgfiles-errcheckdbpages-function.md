---
title: CChkSGFiles. ErrCheckDbPages-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbPages
api_type:
- dllExport
ms.assetid: 5e981a7c-28cd-470c-b7eb-606463e9dd05
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: 78d2dbee6253096d597b4ec2de3878f40ee1b6d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526725"
---
# <a name="cchksgfileserrcheckdbpages-function"></a>CChkSGFiles. ErrCheckDbPages-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Überprüft einen Bereich von Seiten in einer angegebenen Datenbank. 
  
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

### <a name="idb"></a>iDb
  
Eingabeparameter. Ein Index in das im **rgwszDb []** -Parameter angegebene Array von Datenbanken für die **ErrInit** -Funktion. Die von diesem Parameter indizierte Datenbank wird überprüft. 
    
### <a name="pvpagebuffer"></a>pvPageBuffer 
  
Eingabeparameter. Ein Zeiger auf einen Puffer, der eine oder mehrere zu überprüfende Datenbankseiten enthält. Die Größe des Puffers muss ein Vielfaches der Datenbankseitengröße sein, wie er im **pcbDbPageSize** -Parameter von der **ErrCheckDbHeaders** -Funktion zurückgegeben wird. Die aufrufende Anwendung muss den Puffer mit dem Inhalt der Datenbankseite füllen, bevor **ErrCheckDbPages**aufgerufen wird.
    
### <a name="cbpagebuffer"></a>cbPageBuffer
  
Eingabeparameter. Die Größe des **pvPageBuffer** -Parameters in Bytes. Dieser Wert muss ein Vielfaches der Datenbankseitengröße sein, wie er im **pcbDbPageSize** -Parameter von der **ErrCheckDbHeaders** -Funktion zurückgegeben wird. 
    
### <a name="rgpageinfo"></a>rgPageInfo[] 
  
Input/Output-Parameter. Ein Array von **Seiten \_ Info** Strukturen, das von **ErrCheckDbPages** mit detaillierten Ergebnissen jeder geprüften Datenbankseite gefüllt wird. Das Array muss ein Element für jede Datenbankseite haben, die im **pvPageBuffer** -Parameter übergeben wird, und das **ulPgno** -Feld in jeder **Seiten \_ Info** Struktur muss auf die logische Seitenzahl festgelegt werden, die der Datenbankseite entspricht. Weitere Informationen finden Sie weiter unten in diesem Thema unter "Hinweise". 
    
### <a name="cpageinfo"></a>cPageInfo
  
Eingabeparameter. Die Anzahl der Einträge im **rgPageInfo []** -Array. Dieser Wert muss der Anzahl der Datenbankseiten entsprechen, die im Parameter **pvPageBuffer** übergeben wurden. 
    
### <a name="ulflags"></a>ulFlags 
  
Optionaler Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der in diesem Parameter übergebene Wert sollte 0 (null) sein.
    
## <a name="return-value"></a>Rückgabewert

Ein Fehlercode aus der [Err](cchksgfiles-err-enumeration.md) -Aufzählung. 
  
## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass Sie die Datenbank im Array von Datenbanken angegeben haben müssen, die an die **ErrInit** -Funktion übergeben wurden. Außerdem muss **ErrCheckDbHeaders** vor **ErrCheckDbPages**aufgerufen werden.
  
Die aufrufende Anwendung muss einen Arbeitsspeicherpuffer zuweisen, der groß genug ist, um die zu prüfenden Datenbankseiten zu speichern. Die Anwendung ist für das Ausfüllen des Puffers mit dem Inhalt einer oder mehrerer solcher Datenbankseiten verantwortlich. 
  
Die aufrufende Anwendung muss **ErrCheckDbHeaders** vor dem Aufruf von **ErrCheckDbPages**aufrufen. Diese Funktion kann so oft wie erforderlich aufgerufen werden, um alle Seiten in allen Datenbankdateien abzudecken, die überprüft werden sollen.
  
Im **rgPageInfo []** -Parameter enthält jedes zurückgegebene Elementinformationen zur Datenbankseite in einer **Seiten \_ Info** Struktur. Wenn die **ErrCheckDbPages** -Funktion einen Fehler zurückgibt, sollte die Anwendung jede **Seiten \_ Info** Struktur überprüfen, um zu bestimmen, auf welcher Seite der Fehler gefunden wurde. Wenn Sie beispielsweise den **checksumActual** -und den **checksumExpected** -Wert vergleichen, wird angegeben, ob auf dieser Datenbankseite ein Prüfsummenfehler erkannt wurde. 
  
Wenn **ErrCheckDbPages** Fehler im Datenbankinhalt erkennt, wird ein Windows-Fehlerereignisprotokoll Eintrag erstellt. 
  
Das **CChkSGFiles** -Objekt bestimmt, ob alle Datenbanken, die mit der **ErrInit** -Funktion registriert wurden, tatsächlich überprüft wurden. Insbesondere verwendet **CChkSGFiles** die **ErrCheckDbPages** -Funktion, um zu bestimmen, ob die gleiche Anzahl von Datenbankseiten, die von **ErrCheckDbHeaders** angezeigt wurden, tatsächlich überprüft wurde. Wenn die richtige Anzahl von Seiten in jeder Datenbank nicht erfolgreich überprüft wurde, gibt die **ErrTerm** -Funktion einen Fehler zurück. 
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, können Sie die **ErrCheckDbPages** -Funktion im Multithread-Teil der Anwendung aufrufen. Beachten Sie, dass **ErrCheckDbPages** in der Regel für jede geprüfte Datenbank mehrmals aufgerufen wird. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung betrieben wird, muss über Leseberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.
  

