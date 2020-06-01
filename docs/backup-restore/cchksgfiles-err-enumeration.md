---
title: CChkSGFiles. err-Aufzählung
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dbc76601a808f79ce3ed5b5dc9fbe4cf92efb015
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455254"
---
# <a name="cchksgfileserr-enumeration"></a>CChkSGFiles. err-Aufzählung 
  
**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Gibt die Ergebnisse der aufgerufenen Funktion an. Diese Aufzählung wird von vielen Funktionen der **CCheckSGFiles** -Klasse zurückgegeben. 
  
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
|errTaskDropped  <br/> |-106  <br/> |Wird von der **ErrTerm** -Funktion zurückgegeben, um anzugeben, dass nicht alle Datenbankseiten und Transaktionsprotokolldateien überprüft wurden oder dass während der Überprüfung Fehler aufgetreten sind.  <br/> |
|errRequiredLogFilesMissing  <br/> |-543  <br/> |Mindestens eine Protokolldatei, die erforderlich ist, um die Datenbank in den Zustand "Clean Shutdown" zu versetzen, wurde im Protokoll Dateipfad nicht gefunden oder hat nicht den angegebenen drei Buchstaben-Basisnamen.  <br/> |
|errInvalidParameter  <br/> |-1003  <br/> |Mindestens ein Parameter, der an die Funktion übergeben wurde, war ungültig.  <br/> |
|errOutOfMemory  <br/> |-1011  <br/> |Zum Abschließen des angeforderten Vorgangs war nicht genügend Arbeitsspeicher verfügbar.  <br/> |
|errReadVerifyFailure  <br/> |-1018  <br/> |Die auf einer Datenbankseite gespeicherte Prüfsumme stimmt nicht mit der erwarteten Prüfsumme überein.  <br/> |
|errTooManyActiveUsers  <br/> |-1059  <br/> |Die **ErrTerm** -Funktion wurde aufgerufen, während das Objekt noch verwendet wurde. Dies kann auftreten, wenn **ErrTerm** aufgerufen wird, bevor **ErrCheckDbPages** oder **ErrCheckLogFiles** zurückgegeben wurde.  <br/> |
   
## <a name="requirements"></a>Anforderungen

Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.
  

