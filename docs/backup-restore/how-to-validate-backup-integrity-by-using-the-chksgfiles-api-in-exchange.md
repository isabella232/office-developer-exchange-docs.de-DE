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
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a><span data-ttu-id="bd970-103">Überprüfen der Integrität der Sicherung mithilfe der CHKSGFILES-API in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="bd970-103">Validate backup integrity by using the CHKSGFILES API in Exchange 2013</span></span>

<span data-ttu-id="bd970-104">Erfahren Sie, wie Sie mithilfe der CHKSGFILES-API eine Sicherung der Exchange-Informationsspeicher in Exchange 2013 überprüfen.</span><span class="sxs-lookup"><span data-stu-id="bd970-104">Find out how to use the CHKSGFILES API to validate a backup of the Exchange store in Exchange 2013.</span></span>
  
<span data-ttu-id="bd970-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="bd970-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="bd970-106">Während von dem Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwaltete Sicherungsvorgänge können Exchange Server 2013 nicht jede Datenbankdatei vollständig lesen und die Prüfsummenintegrität überprüfen.</span><span class="sxs-lookup"><span data-stu-id="bd970-106">During backup operations managed by the Volume Shadow Copy Service (VSS), Exchange Server 2013 cannot read each database file in its entirety and verify its checksum integrity.</span></span> <span data-ttu-id="bd970-107">Daher empfiehlt es sich, dass Ihre Sicherungsanwendung die Integrität der Datenbank-und Transaktionsprotokolldatei überprüft.</span><span class="sxs-lookup"><span data-stu-id="bd970-107">Therefore, you might want your backup application to verify database and transaction log file integrity.</span></span> <span data-ttu-id="bd970-108">Es wird empfohlen, dass Ihre Sicherungsanwendung die physische Konsistenz des Shadow Copy-Satzes überprüft, bevor der Exchange-Writer informiert wird, dass die Sicherung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bd970-108">We recommend that your backup application verify the physical consistency of the shadow copy set prior to informing the Exchange writer that the backup is complete.</span></span> <span data-ttu-id="bd970-109">Nach einer erfolgreichen Sicherung aktualisiert der Exchange-Informationsspeicher die Kopfzeilen der gesicherten Datenbanken so, dass die letzten erfolgreichen Sicherungszeiten wiedergegeben werden, und entfernt Transaktionsprotokolle von dem Server, die für das Rollforward von der letzten erfolgreichen Sicherung nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="bd970-109">After a successful backup, the Exchange store updates the headers of the backed-up databases to reflect the last successful backup times and removes transaction logs from the server that are no longer required to roll forward from the last successful backup.</span></span>
  
## <a name="prerequisites-for-validating-backup-integrity"></a><span data-ttu-id="bd970-110">Voraussetzungen für die Überprüfung der Integrität der Sicherung</span><span class="sxs-lookup"><span data-stu-id="bd970-110">Prerequisites for validating backup integrity</span></span>

<span data-ttu-id="bd970-111">Bevor Ihre Anwendung die Integrität ihrer Sicherung validieren kann, benötigen Sie Zugriff auf Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bd970-111">Before your application can validate the integrity of your backup, you must have access to the following:</span></span>
  
- <span data-ttu-id="bd970-112">Dateien aus Ihrer Exchange-Informationsspeicher Sicherung.</span><span class="sxs-lookup"><span data-stu-id="bd970-112">Files from your Exchange store backup.</span></span>
- <span data-ttu-id="bd970-113">Eine Version von Visual Studio, die mit Visual Studio 2010 beginnt.</span><span class="sxs-lookup"><span data-stu-id="bd970-113">A version of Visual Studio starting with Visual Studio 2010.</span></span>
- <span data-ttu-id="bd970-114">Die CHKSGFILES-Bibliothek und die Headerdateien.</span><span class="sxs-lookup"><span data-stu-id="bd970-114">The CHKSGFILES library and header files.</span></span> <span data-ttu-id="bd970-115">Sie können die Bibliotheks-und Headerdateien aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="bd970-115">You can download the library and header files from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802).</span></span>
    
## <a name="validate-backup-integrity"></a><span data-ttu-id="bd970-116">Überprüfen der Integrität der Sicherung</span><span class="sxs-lookup"><span data-stu-id="bd970-116">Validate backup integrity</span></span>

<span data-ttu-id="bd970-117">Im folgenden Verfahren wird beschrieben, wie die Datenintegrität in der Sicherungs-und Wiederherstellungsanwendung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="bd970-117">The following procedure describes how to validate data integrity in your backup and restore application.</span></span>
  
### <a name="to-validate-backup-integrity"></a><span data-ttu-id="bd970-118">So überprüfen Sie die Integrität der Sicherung</span><span class="sxs-lookup"><span data-stu-id="bd970-118">To validate backup integrity</span></span>

1. <span data-ttu-id="bd970-119">Erstellen Sie eine neue Instanz der **CChkSGFiles** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="bd970-119">Create a new instance of the **CChkSGFiles** class.</span></span> 
   
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

   <span data-ttu-id="bd970-120">In den ersten Codezeilen wird ein Error-Objekt erstellt und sein anfänglicher Wert auf Success festgelegt, und es wird ein Objekt erstellt, das die Gültigkeit der Datenbank überprüft.</span><span class="sxs-lookup"><span data-stu-id="bd970-120">The first lines of code create an error object and set its initial value to success, and create an object that checks the validity of the database.</span></span> <span data-ttu-id="bd970-121">Anschließend erstellt die [CChkSGFiles. New-Funktion](cchksgfiles-new-function.md) eine neue Instanz der **CChkSGFiles** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="bd970-121">Then, the [CChkSGFiles.New function](cchksgfiles-new-function.md) creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="bd970-122">Eine Schnellüberprüfung des neuen Objekts gibt an, ob beim Erstellen der neuen Instanz Probleme aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="bd970-122">A quick check of the new object indicates whether any issues occurred when the new instance was created.</span></span> 
    
2. <span data-ttu-id="bd970-123">Initialisieren Sie das **CChkSGFiles** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd970-123">Initialize the **CChkSGFiles** object.</span></span> 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   <span data-ttu-id="bd970-124">Weitere Informationen zu den Parametern finden Sie unter [CChkSGFiles. ErrInit-Funktion](cchksgfiles-errinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="bd970-124">For more information about the parameters, see [CChkSGFiles.ErrInit function](cchksgfiles-errinit-function.md).</span></span>
   
3. <span data-ttu-id="bd970-125">Verwenden Sie die [CChkSGFiles. ErrCheckDbHeaders-Funktion](cchksgfiles-errcheckdbheaders-function.md) , um die Integrität der Datenbank zu überprüfen, indem Sie die Datenbankheader überprüfen.</span><span class="sxs-lookup"><span data-stu-id="bd970-125">Use the [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md) to validate database integrity by checking the database headers.</span></span>
   
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
   
   <span data-ttu-id="bd970-126">Weitere Informationen zu den Parametern finden Sie unter [CChkSGFiles. ErrCheckDbHeaders-Funktion](cchksgfiles-errcheckdbheaders-function.md).</span><span class="sxs-lookup"><span data-stu-id="bd970-126">For more information about the parameters, see [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md).</span></span>
   
4. <span data-ttu-id="bd970-127">Behandeln Sie Fehler, und verwenden Sie die [CChkSGFiles. Delete-Funktion](cchksgfiles-delete-function.md) , um die **CChkSGFiles** -Klasse aus dem Arbeitsspeicher zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="bd970-127">Handle errors, and use the [CChkSGFiles.Delete function](cchksgfiles-delete-function.md) to remove the **CChkSGFiles** class from memory.</span></span> 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a><span data-ttu-id="bd970-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd970-128">See also</span></span>

- [<span data-ttu-id="bd970-129">CChkSGFiles-Klassenreferenz</span><span class="sxs-lookup"><span data-stu-id="bd970-129">CChkSGFiles class reference</span></span>](cchksgfiles-class-reference.md)
- [<span data-ttu-id="bd970-130">Erstellen von Sicherungs-und Wiederherstellungsanwendungen für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="bd970-130">Build backup and restore applications for Exchange 2013</span></span>](build-backup-and-restore-applications-for-exchange-2013.md)
- [<span data-ttu-id="bd970-131">Sichern und Wiederherstellen von Konzepten für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="bd970-131">Backup and restore concepts for Exchange 2013</span></span>](backup-and-restore-concepts-for-exchange-2013.md)
    

