---
title: Überprüfen der Integrität der Sicherung mithilfe der CHKSGFILES-API in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 607cbeb9-0a02-4079-8a4d-34bdeb560224
description: Erfahren Sie, wie Sie mithilfe der CHKSGFILES-API eine Sicherung der Exchange-Informationsspeicher in Exchange 2013 überprüfen.
ms.openlocfilehash: c101413793cf3b952d3db3e0f792c8bcf2dd9fc9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452860"
---
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a>Überprüfen der Integrität der Sicherung mithilfe der CHKSGFILES-API in Exchange 2013

Erfahren Sie, wie Sie mithilfe der CHKSGFILES-API eine Sicherung der Exchange-Informationsspeicher in Exchange 2013 überprüfen.
  
**Gilt für:** Exchange Server 2013 
  
Während von dem Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwaltete Sicherungsvorgänge können Exchange Server 2013 nicht jede Datenbankdatei vollständig lesen und die Prüfsummenintegrität überprüfen. Daher empfiehlt es sich, dass Ihre Sicherungsanwendung die Integrität der Datenbank-und Transaktionsprotokolldatei überprüft. Es wird empfohlen, dass Ihre Sicherungsanwendung die physische Konsistenz des Shadow Copy-Satzes überprüft, bevor der Exchange-Writer informiert wird, dass die Sicherung abgeschlossen ist. Nach einer erfolgreichen Sicherung aktualisiert der Exchange-Informationsspeicher die Kopfzeilen der gesicherten Datenbanken so, dass die letzten erfolgreichen Sicherungszeiten wiedergegeben werden, und entfernt Transaktionsprotokolle von dem Server, die für das Rollforward von der letzten erfolgreichen Sicherung nicht mehr benötigt werden.
  
## <a name="prerequisites-for-validating-backup-integrity"></a>Voraussetzungen für die Überprüfung der Integrität der Sicherung

Bevor Ihre Anwendung die Integrität ihrer Sicherung validieren kann, benötigen Sie Zugriff auf Folgendes:
  
- Dateien aus Ihrer Exchange-Informationsspeicher Sicherung.
- Eine Version von Visual Studio, die mit Visual Studio 2010 beginnt.
- Die CHKSGFILES-Bibliothek und die Headerdateien. Sie können die Bibliotheks-und Headerdateien aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802)herunterladen.
    
## <a name="validate-backup-integrity"></a>Überprüfen der Integrität der Sicherung

Im folgenden Verfahren wird beschrieben, wie die Datenintegrität in der Sicherungs-und Wiederherstellungsanwendung überprüft wird.
  
### <a name="to-validate-backup-integrity"></a>So überprüfen Sie die Integrität der Sicherung

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

   In den ersten Codezeilen wird ein Error-Objekt erstellt und sein anfänglicher Wert auf Success festgelegt, und es wird ein Objekt erstellt, das die Gültigkeit der Datenbank überprüft. Anschließend erstellt die [CChkSGFiles. New-Funktion](cchksgfiles-new-function.md) eine neue Instanz der **CChkSGFiles** -Klasse. Eine Schnellüberprüfung des neuen Objekts gibt an, ob beim Erstellen der neuen Instanz Probleme aufgetreten sind. 
    
2. Initialisieren Sie das **CChkSGFiles** -Objekt. 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   Weitere Informationen zu den Parametern finden Sie unter [CChkSGFiles. ErrInit-Funktion](cchksgfiles-errinit-function.md).
   
3. Verwenden Sie die [CChkSGFiles. ErrCheckDbHeaders-Funktion](cchksgfiles-errcheckdbheaders-function.md) , um die Integrität der Datenbank zu überprüfen, indem Sie die Datenbankheader überprüfen.
   
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
   
   Weitere Informationen zu den Parametern finden Sie unter [CChkSGFiles. ErrCheckDbHeaders-Funktion](cchksgfiles-errcheckdbheaders-function.md).
   
4. Behandeln Sie Fehler, und verwenden Sie die [CChkSGFiles. Delete-Funktion](cchksgfiles-delete-function.md) , um die **CChkSGFiles** -Klasse aus dem Arbeitsspeicher zu entfernen. 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a>Siehe auch

- [CChkSGFiles-Klassenreferenz](cchksgfiles-class-reference.md)
- [Erstellen von Sicherungs-und Wiederherstellungsanwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

