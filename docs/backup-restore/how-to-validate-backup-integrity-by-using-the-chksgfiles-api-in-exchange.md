---
title: Überprüfen der Sicherungsintegrität mithilfe der CHKSGFILES-API in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 607cbeb9-0a02-4079-8a4d-34bdeb560224
description: Erfahren Sie, wie Sie die CHKSGFILES-API verwenden, um eine Sicherung des Exchange Speichers in Exchange 2013 zu überprüfen.
ms.openlocfilehash: 7a12a0a8f66128970a782da50ba59f41767c60d3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516230"
---
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a>Überprüfen der Sicherungsintegrität mithilfe der CHKSGFILES-API in Exchange 2013

Erfahren Sie, wie Sie die CHKSGFILES-API verwenden, um eine Sicherung des Exchange Speichers in Exchange 2013 zu überprüfen.
  
**Gilt für:** Exchange Server 2013 
  
Während der vom Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwalteten Sicherungsvorgänge kann Exchange Server 2013 nicht jede Datenbankdatei vollständig lesen und ihre Prüfsummenintegrität überprüfen. Daher möchten Sie möglicherweise, dass ihre Sicherungsanwendung die Integrität von Datenbank- und Transaktionsprotokolldateien überprüft. Es wird empfohlen, dass Ihre Sicherungsanwendung die physische Konsistenz des Schattenkopiesatzes überprüft, bevor der Exchange Writer informiert wird, dass die Sicherung abgeschlossen ist. Nach einer erfolgreichen Sicherung aktualisiert der Exchange die Header der gesicherten Datenbanken, um die letzten erfolgreichen Sicherungszeiten widerzuspiegeln, und entfernt Transaktionsprotokollen vom Server, die nicht mehr für die Weiterleitung von der letzten erfolgreichen Sicherung erforderlich sind.
  
## <a name="prerequisites-for-validating-backup-integrity"></a>Voraussetzungen für die Überprüfung der Sicherungsintegrität

Bevor Ihre Anwendung die Integrität der Sicherung überprüfen kann, müssen Sie Zugriff auf Folgendes haben:
  
- Dateien aus Ihrer Exchange Speichernsicherung.
- Eine Version von Visual Studio ab Visual Studio 2010.
- Die CHKSGFILES-Bibliotheks- und Headerdateien. Sie können die Bibliotheks- und Headerdateien aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802)herunterladen.
    
## <a name="validate-backup-integrity"></a>Überprüfen der Sicherungsintegrität

Im folgenden Verfahren wird beschrieben, wie Sie die Datenintegrität in Ihrer Sicherungs- und Wiederherstellungsanwendung überprüfen.
  
### <a name="to-validate-backup-integrity"></a>So überprüfen Sie die Sicherungsintegrität

1. Erstellen Sie eine neue Instanz der **CChkSGFiles-Klasse.** 
   
   ```cpp
   CCheckSGFiles::ERRerr = CCheckSGFiles::errSuccess;
   ULONGiDbError = (ULONG)CCheckSGFiles::iDbInvalid;
   CCheckSGFiles * const pcchecksgfiles = CCheckSGFiles::New();
   if ( NULL == pcchecksgfiles )
   {
     err = CCheckSGFiles::errOutOfMemory;
     printf( "ERROR: Could not allocate CCheckSGFiles object.\n" );
     goto HandleError;
   }
   ```

   Die ersten Codezeilen erstellen ein Fehlerobjekt, legen den Anfangswert auf "erfolgreich" fest, und erstellen ein Objekt, das die Gültigkeit der Datenbank überprüft. Anschließend erstellt die [CChkSGFiles.New-Funktion](cchksgfiles-new-function.md) eine neue Instanz der **CChkSGFiles-Klasse.** Eine schnelle Überprüfung des neuen Objekts gibt an, ob beim Erstellen der neuen Instanz Probleme aufgetreten sind. 
    
2. Initialisieren Sie das **CChkSGFiles-Objekt.** 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   Weitere Informationen zu den Parametern finden Sie unter ["CChkSGFiles.ErrInit"-Funktion.](cchksgfiles-errinit-function.md)
   
3. Verwenden Sie die [CChkSGFiles.ErrCheckDbHeaders-Funktion,](cchksgfiles-errcheckdbheaders-function.md) um die Datenbankintegrität durch Überprüfen der Datenbankheader zu überprüfen.
   
   ```cpp
   err = pcchecksgfiles->ErrCheckDbHeaders(
   &amp;cbDbPageSize,
   &amp;cDbHeaderPages,
   &amp;iDbError );
   if ( CCheckSGFiles::errSuccess != err )
   {
   if ( CCheckSGFiles::iDbInvalid != iDbError )
   {
   printf(
   "ERROR: Database header validation for '%S' failed with error %d (0x%x)\n",
   rgwszDb[ iDbError ],
   err,
   err );
   }
   goto HandleError;
   }
   ```
   
   Weitere Informationen zu den Parametern finden Sie unter ["CChkSGFiles.ErrCheckDbHeaders"-Funktion.](cchksgfiles-errcheckdbheaders-function.md)
   
4. Behandeln Sie Fehler, und verwenden Sie die [CChkSGFiles.Delete-Funktion,](cchksgfiles-delete-function.md) um die **CChkSGFiles-Klasse** aus dem Arbeitsspeicher zu entfernen. 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a>Siehe auch

- [CChkSGFiles-Klassenreferenz](cchksgfiles-class-reference.md)
- [Erstellen von Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

