---
title: CChkSGFiles.ERR-Aufzählung
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ERR
api_type:
- dllExport
ms.assetid: f0efe195-91c3-4f3a-8c7d-e5dba336465a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 20f10c43e3b92604bb51e1aa5f896a8bd7c4b335
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757749"
---
# <a name="cchksgfileserr-enumeration"></a>CChkSGFiles.ERR-Aufzählung 
  
**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Gibt die Ergebnisse der aufgerufenen Funktion an. Diese Aufzählung wird von viele Funktionen der **CCheckSGFiles** -Klasse zurückgegeben. 
  
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
|errSuccess  <br/> |0  <br/> |Die Funktion ohne Fehler abgeschlossen.  <br/> |
|errTaskDropped  <br/> |-106  <br/> |Wird von der Funktion **ErrTerm** , um anzugeben, dass nicht alle Datenbankseiten und Transaktionsprotokolldateien nicht überprüft wurden oder bei der Überprüfung Fehler aufgetreten sind.  <br/> |
|errRequiredLogFilesMissing  <br/> |-543  <br/> |Eine oder mehrere Protokolldateien, die erforderlich sind, um die Datenbank auf einen clean Shutdown-Status in der Pfad der Protokolldatei nicht gefunden oder verfügte nicht über den angegebenen drei Buchstaben Basisnamen.  <br/> |
|errInvalidParameter  <br/> |-1003  <br/> |Mindestens einen Parameter, die an die Funktion übergeben wurden war ungültig.  <br/> |
|errOutOfMemory  <br/> |-1011  <br/> |Es wurde nicht genügend Arbeitsspeicher verfügbar, um den angeforderten Vorgang abzuschließen.  <br/> |
|errReadVerifyFailure  <br/> |-1018  <br/> |Die Prüfsumme, die auf einer Datenbankseite gespeichert ist stimmt nicht mit der erwarteten Prüfsumme überein.  <br/> |
|errTooManyActiveUsers  <br/> |-1059  <br/> |Die Funktion **ErrTerm** wurde aufgerufen, während das Objekt wurde noch verwendet wird. Dies kann vorkommen, wenn **ErrTerm** , bevor **ErrCheckDbPages aufgerufen wird** oder **ErrCheckLogFiles** zurückgegeben hat.  <br/> |
   
## <a name="requirements"></a>Anforderungen

Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.
  

