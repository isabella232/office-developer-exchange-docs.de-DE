---
title: CChkSGFiles.ErrCheckDbPages-Funktion
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
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: f1588b1dbc4bd7e83683fa4432a175405ad17903
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756803"
---
# <a name="cchksgfileserrcheckdbpages-function"></a>CChkSGFiles.ErrCheckDbPages-Funktion

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
  
Input-Parameter. Ein Index in das Array von Datenbanken, die im Parameter an die Funktion **ErrInit** **RgwszDb []** angegeben. Die Datenbank, die von diesem Parameter indiziert werden überprüft. 
    
### <a name="pvpagebuffer"></a>pvPageBuffer 
  
Input-Parameter. Ein Zeiger auf einen Puffer mit mindestens Datenbankseiten überprüft werden soll. Die Größe des Puffers muss ein Vielfaches von Seitengröße der Datenbank, wie in der **PcbDbPageSize** -Parameter von der Funktion **ErrCheckDbHeaders** zurückgegeben. Die aufrufende Anwendung muss den Puffer mit dem Inhalt der Datenbank vor dem Aufruf von **ErrCheckDbPages**ausfüllen.
    
### <a name="cbpagebuffer"></a>cbPageBuffer
  
Input-Parameter. Die Größe des Parameters **PvPageBuffer** in Byte. Dieser Wert muss ein Vielfaches von Seitengröße der Datenbank sein, wie im Parameter **PcbDbPageSize** durch die **ErrCheckDbHeaders** -Funktion zurückgegeben. 
    
### <a name="rgpageinfo"></a>RgPageInfo] 
  
Input/Output-Parameter. Ein Array von **Seite\_INFO** Strukturen, die mit **ErrCheckDbPages** füllt ausführliche Ergebnisse jeder Datenbank-Seite, die eingecheckt wird. Das Array muss ein Element für jede Datenbankseite in der **PvPageBuffer** -Parameter und das Feld **UlPgno** in den einzelnen übergeben haben **Seite\_INFO** Struktur muss festgelegt werden, um die logische Seitenzahl, die der Datenbankseite entspricht. Weitere Informationen finden Sie unter "Hinweise" weiter unten in diesem Thema. 
    
### <a name="cpageinfo"></a>cPageInfo
  
Input-Parameter. Die Anzahl der Einträge im Array **RgPageInfo []** . Dieser Wert muss gleich der Anzahl von Datenbankseiten im **PvPageBuffer** -Parameter übergeben werden. 
    
### <a name="ulflags"></a>ulFlags 
  
Optionale Eingabeparameter. Dieser Wert ist für die zukünftige Verwendung reserviert. Der in diesem Parameter übergebene Wert muss 0 (null) sein.
    
## <a name="return-value"></a>R�ckgabewert

Ein Fehlercode aus der [ERR](cchksgfiles-err-enumeration.md) -Aufzählung. 
  
## <a name="remarks"></a>Hinweise

Beachten Sie, dass müssen Sie die Datenbank in das Array von Datenbanken, die an die Funktion **ErrInit** übergeben angegeben haben. Darüber hinaus muss **ErrCheckDbHeaders** vor **ErrCheckDbPages**aufgerufen werden.
  
Die aufrufende Anwendung muss Speicherpuffers zuweisen, die groß genug für die Datenbankseiten überprüft werden soll. Die Anwendung ist verantwortlich für die Puffer mit dem Inhalt von mindestens einen solchen Datenbankseiten ausfüllen. 
  
Die aufrufende Anwendung muss vor dem Aufruf von **ErrCheckDbPages** **ErrCheckDbHeaders** aufrufen. So oft wie erforderlich sind, um alle Seiten in allen Datenbankdateien behandelt, die überprüft werden sollen, kann diese Funktion aufgerufen werden.
  
In der Parameter **RgPageInfo []** jedes zurückgegebene Element enthält Informationen zu der Datenbankseite in einer **Seite\_INFO** Struktur. Wenn die **ErrCheckDbPages** -Funktion einen Fehler zurückgibt, sollte die Anwendung überprüfen jeweils **Seite\_INFO** Struktur, um festzulegen, auf welcher Seite der Fehler gefunden wurde. Vergleichen die Werte **ChecksumActual** und **ChecksumExpected** wird beispielsweise angeben, ob ein Prüfsummenfehler auf der Datenbankseite erkannt wurde. 
  
Wenn **ErrCheckDbPages** Fehler in der Datenbank erkennt, erstellt er einen Ereignisprotokolleintrag Windows-Fehler. 
  
Das Objekt **CChkSGFiles** bestimmt, ob alle Datenbanken, die mit der Funktion **ErrInit** registriert tatsächlich aktiviert wurden. Insbesondere wird **CChkSGFiles** die **ErrCheckDbPages** -Funktion verwendet, um zu bestimmen, ob die gleiche Anzahl von Datenbankseiten angegeben durch **ErrCheckDbHeaders** tatsächlich überprüft wurden. Wenn die richtige Anzahl von Seiten in jeder Datenbank nicht erfolgreich überprüft wurden, gibt die **ErrTerm** -Funktion einen Fehler zurück. 
  
Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, können Sie die **ErrCheckDbPages** -Funktion im Multithread-Teil der Anwendung anrufen. Beachten Sie, dass **ErrCheckDbPages** in der Regel mehrere Male für jede Datenbank aufgerufen wird, der überprüft wird. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter die Anwendung ausgeführt wird, muss Berechtigungen für die Datenbank- und Protokolldateien Dateien gelesen haben, die überprüft werden sollen.
  

