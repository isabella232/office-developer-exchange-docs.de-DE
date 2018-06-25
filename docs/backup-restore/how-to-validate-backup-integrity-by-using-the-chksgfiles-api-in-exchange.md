---
title: Überprüfen der Integrität mithilfe der API für CHKSGFILES in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 607cbeb9-0a02-4079-8a4d-34bdeb560224
description: Erfahren Sie, wie die CHKSGFILES-API verwenden, um eine Sicherung der Exchange-Speicher in Exchange 2013 zu überprüfen.
ms.openlocfilehash: 968484cd5bb7439730685643683e1d850bec33ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756807"
---
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a>Überprüfen der Integrität mithilfe der API für CHKSGFILES in Exchange 2013

Erfahren Sie, wie die CHKSGFILES-API verwenden, um eine Sicherung der Exchange-Speicher in Exchange 2013 zu überprüfen.
  
**Gilt für:** Exchange Server 2013 
  
Während der Sicherungsvorgänge Volume Shadow Copy Service (VSS) verwaltet kann nicht Exchange Server 2013 lesen Sie jede Datenbankdatei in seiner Gesamtheit und überprüfen Sie die Prüfsummenintegrität. Aus diesem Grund sollten Sie Ihre backup-Anwendung die Datenbank- und Transaktionsprotokolldateien Log File Integrität zu überprüfen. Es wird empfohlen, dass Ihre backup-Anwendung überprüfen, ob die physische Konsistenz von der Shadow Copy-Satz vor dem Exchange-Writer informiert werden, dass die Sicherung abgeschlossen ist. Nach einer erfolgreichen Sicherung aktualisiert Exchange-Speicher die Kopfzeilen der gesicherten Datenbanken, um die letzte erfolgreiche Sicherung Zeiten und Transaktionsprotokolle vom Server entfernt wiederzugeben, die nicht mehr benötigt werden, aus der letzten erfolgreichen Sicherung vorwärts bereitzustellen.
  
## <a name="prerequisites-for-validating-backup-integrity"></a>Erforderliche Komponenten zum Überprüfen der Integrität

Bevor die Anwendung die Integrität Ihrer Sicherung überprüfen kann, benötigen Sie Zugriff auf die folgenden:
  
- Speichern von Dateien aus Ihrer Exchange-Sicherung.
- Eine Version von Visual Studio beginnend mit Visual Studio 2010.
- Die CHKSGFILES Bibliothek und Header-Dateien. Sie können die Bibliothek und Header-Dateien aus dem [Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=36802)herunterladen.
    
## <a name="validate-backup-integrity"></a>Überprüfen der Integrität

Das folgende Verfahren beschreibt, wie Überprüfen der Integrität der Daten in die Sicherung und Wiederherstellung von Anwendung.
  
### <a name="to-validate-backup-integrity"></a>Überprüfen der Integrität

1. Erstellen Sie eine neue Instanz der **CChkSGFiles** -Klasse. 
   
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

   Die ersten Codezeilen ein Error-Objekt erstellen und Anfangswert auf Erfolg festlegen und erstellen ein Objekt, das die Gültigkeit der Datenbank überprüft. Die [CChkSGFiles.New-Funktion](cchksgfiles-new-function.md) erstellt dann eine neue Instanz der **CChkSGFiles** -Klasse. Eine schnelle Überprüfung des neuen Objekts angibt, ob beim Erstellen die neue Instanz Probleme aufgetreten ist. 
    
2. Initialisieren Sie das **CChkSGFiles** -Objekt. 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   Weitere Informationen zu den Parametern finden Sie unter [CChkSGFiles.ErrInit-Funktion](cchksgfiles-errinit-function.md).
   
3. Verwenden Sie die [CChkSGFiles.ErrCheckDbHeaders-Funktion](cchksgfiles-errcheckdbheaders-function.md) , um die Datenbankintegrität überprüfen, indem Sie die Datenbank-Kopfzeilen überprüfen.
   
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
   
   Weitere Informationen zu den Parametern finden Sie unter [CChkSGFiles.ErrCheckDbHeaders-Funktion](cchksgfiles-errcheckdbheaders-function.md).
   
4. Behandeln von Fehlern und mit der [CChkSGFiles.Delete-Funktion](cchksgfiles-delete-function.md) können Sie die **CChkSGFiles** -Klasse aus dem Speicher zu entfernen. 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a>Siehe auch

- [Referenz für die CChkSGFiles](cchksgfiles-class-reference.md)
- [Erstellen von Sicherung und Wiederherstellen von Anwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [Sicherung und Wiederherstellung Konzepte für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

