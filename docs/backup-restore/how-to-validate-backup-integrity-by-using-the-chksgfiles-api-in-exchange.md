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
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a><span data-ttu-id="a6d43-103">Überprüfen der Integrität mithilfe der API für CHKSGFILES in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a6d43-103">Validate backup integrity by using the CHKSGFILES API in Exchange 2013</span></span>

<span data-ttu-id="a6d43-104">Erfahren Sie, wie die CHKSGFILES-API verwenden, um eine Sicherung der Exchange-Speicher in Exchange 2013 zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a6d43-104">Find out how to use the CHKSGFILES API to validate a backup of the Exchange store in Exchange 2013.</span></span>
  
<span data-ttu-id="a6d43-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6d43-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="a6d43-106">Während der Sicherungsvorgänge Volume Shadow Copy Service (VSS) verwaltet kann nicht Exchange Server 2013 lesen Sie jede Datenbankdatei in seiner Gesamtheit und überprüfen Sie die Prüfsummenintegrität.</span><span class="sxs-lookup"><span data-stu-id="a6d43-106">During backup operations managed by the Volume Shadow Copy Service (VSS), Exchange Server 2013 cannot read each database file in its entirety and verify its checksum integrity.</span></span> <span data-ttu-id="a6d43-107">Aus diesem Grund sollten Sie Ihre backup-Anwendung die Datenbank- und Transaktionsprotokolldateien Log File Integrität zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a6d43-107">Therefore, you might want your backup application to verify database and transaction log file integrity.</span></span> <span data-ttu-id="a6d43-108">Es wird empfohlen, dass Ihre backup-Anwendung überprüfen, ob die physische Konsistenz von der Shadow Copy-Satz vor dem Exchange-Writer informiert werden, dass die Sicherung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a6d43-108">We recommend that your backup application verify the physical consistency of the shadow copy set prior to informing the Exchange writer that the backup is complete.</span></span> <span data-ttu-id="a6d43-109">Nach einer erfolgreichen Sicherung aktualisiert Exchange-Speicher die Kopfzeilen der gesicherten Datenbanken, um die letzte erfolgreiche Sicherung Zeiten und Transaktionsprotokolle vom Server entfernt wiederzugeben, die nicht mehr benötigt werden, aus der letzten erfolgreichen Sicherung vorwärts bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a6d43-109">After a successful backup, the Exchange store updates the headers of the backed-up databases to reflect the last successful backup times and removes transaction logs from the server that are no longer required to roll forward from the last successful backup.</span></span>
  
## <a name="prerequisites-for-validating-backup-integrity"></a><span data-ttu-id="a6d43-110">Erforderliche Komponenten zum Überprüfen der Integrität</span><span class="sxs-lookup"><span data-stu-id="a6d43-110">Prerequisites for validating backup integrity</span></span>

<span data-ttu-id="a6d43-111">Bevor die Anwendung die Integrität Ihrer Sicherung überprüfen kann, benötigen Sie Zugriff auf die folgenden:</span><span class="sxs-lookup"><span data-stu-id="a6d43-111">Before your application can validate the integrity of your backup, you must have access to the following:</span></span>
  
- <span data-ttu-id="a6d43-112">Speichern von Dateien aus Ihrer Exchange-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="a6d43-112">Files from your Exchange store backup.</span></span>
- <span data-ttu-id="a6d43-113">Eine Version von Visual Studio beginnend mit Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="a6d43-113">A version of Visual Studio starting with Visual Studio 2010.</span></span>
- <span data-ttu-id="a6d43-114">Die CHKSGFILES Bibliothek und Header-Dateien.</span><span class="sxs-lookup"><span data-stu-id="a6d43-114">The CHKSGFILES library and header files.</span></span> <span data-ttu-id="a6d43-115">Sie können die Bibliothek und Header-Dateien aus dem [Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=36802)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="a6d43-115">You can download the library and header files from the [Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=36802).</span></span>
    
## <a name="validate-backup-integrity"></a><span data-ttu-id="a6d43-116">Überprüfen der Integrität</span><span class="sxs-lookup"><span data-stu-id="a6d43-116">Validate backup integrity</span></span>

<span data-ttu-id="a6d43-117">Das folgende Verfahren beschreibt, wie Überprüfen der Integrität der Daten in die Sicherung und Wiederherstellung von Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a6d43-117">The following procedure describes how to validate data integrity in your backup and restore application.</span></span>
  
### <a name="to-validate-backup-integrity"></a><span data-ttu-id="a6d43-118">Überprüfen der Integrität</span><span class="sxs-lookup"><span data-stu-id="a6d43-118">To validate backup integrity</span></span>

1. <span data-ttu-id="a6d43-119">Erstellen Sie eine neue Instanz der **CChkSGFiles** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="a6d43-119">Create a new instance of the **CChkSGFiles** class.</span></span> 
   
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

   <span data-ttu-id="a6d43-120">Die ersten Codezeilen ein Error-Objekt erstellen und Anfangswert auf Erfolg festlegen und erstellen ein Objekt, das die Gültigkeit der Datenbank überprüft.</span><span class="sxs-lookup"><span data-stu-id="a6d43-120">The first lines of code create an error object and set its initial value to success, and create an object that checks the validity of the database.</span></span> <span data-ttu-id="a6d43-121">Die [CChkSGFiles.New-Funktion](cchksgfiles-new-function.md) erstellt dann eine neue Instanz der **CChkSGFiles** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="a6d43-121">Then, the [CChkSGFiles.New function](cchksgfiles-new-function.md) creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="a6d43-122">Eine schnelle Überprüfung des neuen Objekts angibt, ob beim Erstellen die neue Instanz Probleme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a6d43-122">A quick check of the new object indicates whether any issues occurred when the new instance was created.</span></span> 
    
2. <span data-ttu-id="a6d43-123">Initialisieren Sie das **CChkSGFiles** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a6d43-123">Initialize the **CChkSGFiles** object.</span></span> 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   <span data-ttu-id="a6d43-124">Weitere Informationen zu den Parametern finden Sie unter [CChkSGFiles.ErrInit-Funktion](cchksgfiles-errinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="a6d43-124">For more information about the parameters, see [CChkSGFiles.ErrInit function](cchksgfiles-errinit-function.md).</span></span>
   
3. <span data-ttu-id="a6d43-125">Verwenden Sie die [CChkSGFiles.ErrCheckDbHeaders-Funktion](cchksgfiles-errcheckdbheaders-function.md) , um die Datenbankintegrität überprüfen, indem Sie die Datenbank-Kopfzeilen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a6d43-125">Use the [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md) to validate database integrity by checking the database headers.</span></span>
   
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
   
   <span data-ttu-id="a6d43-126">Weitere Informationen zu den Parametern finden Sie unter [CChkSGFiles.ErrCheckDbHeaders-Funktion](cchksgfiles-errcheckdbheaders-function.md).</span><span class="sxs-lookup"><span data-stu-id="a6d43-126">For more information about the parameters, see [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md).</span></span>
   
4. <span data-ttu-id="a6d43-127">Behandeln von Fehlern und mit der [CChkSGFiles.Delete-Funktion](cchksgfiles-delete-function.md) können Sie die **CChkSGFiles** -Klasse aus dem Speicher zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a6d43-127">Handle errors, and use the [CChkSGFiles.Delete function](cchksgfiles-delete-function.md) to remove the **CChkSGFiles** class from memory.</span></span> 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a><span data-ttu-id="a6d43-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6d43-128">See also</span></span>

- [<span data-ttu-id="a6d43-129">Referenz für die CChkSGFiles</span><span class="sxs-lookup"><span data-stu-id="a6d43-129">CChkSGFiles class reference</span></span>](cchksgfiles-class-reference.md)
- [<span data-ttu-id="a6d43-130">Erstellen von Sicherung und Wiederherstellen von Anwendungen für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a6d43-130">Build backup and restore applications for Exchange 2013</span></span>](build-backup-and-restore-applications-for-exchange-2013.md)
- [<span data-ttu-id="a6d43-131">Sicherung und Wiederherstellung Konzepte für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a6d43-131">Backup and restore concepts for Exchange 2013</span></span>](backup-and-restore-concepts-for-exchange-2013.md)
    

