---
title: CChkSGFiles.ERR-Aufzählung
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ERR
api_type:
- dllExport
ms.assetid: f0efe195-91c3-4f3a-8c7d-e5dba336465a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 12cfff44a6dacbb07ee5518d0008092fbfb644d1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510463"
---
# <a name="cchksgfileserr-enumeration"></a>CChkSGFiles.ERR-Aufzählung 
  
**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Gibt die Ergebnisse der aufgerufenen Funktion an. Diese Enumeration wird von vielen Funktionen der **CCheckSGFiles-Klasse** zurückgegeben. 
  
```cs
Enum ERR  
{
        errSuccess = 0,
        errTaskDropped = -106,
        errRequiredLogFilesMissing = -543,
        errInvalidParameter = -1003,
        errOutOfMemory = -1011,
        errReadVerifyFailure = -1018,
        errTooManyActiveUsers = -1059,
        errDatabaseCorrupted = -1206
}

```

## <a name="values"></a>Werte

|**Elementname**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|errSuccess  <br/> |0  <br/> |Die Funktion wurde ohne Fehler abgeschlossen.  <br/> |
|errTaskDropped  <br/> |-106  <br/> |Wird von der **ErrTerm-Funktion** zurückgegeben, um anzugeben, dass nicht alle Datenbankseiten und Transaktionsprotokolldateien überprüft wurden oder dass während der Überprüfung Fehler aufgetreten sind.  <br/> |
|errRequiredLogFilesMissing  <br/> |-543  <br/> |Eine oder mehrere Protokolldateien, die erforderlich sind, um die Datenbank in einen Zustand des sauberen Herunterfahrens zu versetzen, wurden im Protokolldateipfad nicht gefunden oder hatten nicht den angegebenen Drei-Buchstaben-Basisnamen.  <br/> |
|errInvalidParameter  <br/> |-1003  <br/> |Ein oder mehrere Parameter, die an die Funktion übergeben wurden, waren ungültig.  <br/> |
|errOutOfMemory  <br/> |-1011  <br/> |Zum Abschließen des angeforderten Vorgangs war nicht genügend Arbeitsspeicher verfügbar.  <br/> |
|errReadVerifyFailure  <br/> |-1018  <br/> |Die auf einer Datenbankseite gespeicherte Prüfsumme stimmt nicht mit der erwarteten Prüfsumme überein.  <br/> |
|errTooManyActiveUsers  <br/> |-1059  <br/> |Die **ErrTerm-Funktion** wurde aufgerufen, während das Objekt noch verwendet wurde. Dies kann vorkommen, wenn **ErrTerm** aufgerufen wird, bevor **ErrCheckDbPages** oder **ErrCheckLogFiles** zurückgegeben wurde.  <br/> |
   
## <a name="requirements"></a>Anforderungen

Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung ausgeführt wird, muss über Lesezugriffsberechtigungen für die Datenbank und die Protokolldateien verfügen, die überprüft werden sollen.
  

