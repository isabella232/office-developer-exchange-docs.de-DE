---
title: CChkSGFiles.ErrCheckLogs-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckLogs
api_type:
- dllExport
ms.assetid: cec0df4b-4679-4682-bacf-69b4f4aef343
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: 5b1070de73bc23ae09ddb7835bd72c8e8a71a95f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756806"
---
# <a name="cchksgfileserrchecklogs-function"></a><span data-ttu-id="fe0c2-103">CChkSGFiles.ErrCheckLogs-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe0c2-103">CChkSGFiles.ErrCheckLogs function</span></span>

<span data-ttu-id="fe0c2-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="fe0c2-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="fe0c2-105">Überprüft die Protokolldateien aller Datenbankdateien, die in der Funktion **ErrInit** angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-105">Validates the log files of all the database files that were specified in the **ErrInit** function.</span></span> <span data-ttu-id="fe0c2-106">Die validierten Protokolle sind nur die, die im Pfad vorhanden sind, und drei Buchstaben Logarithmus zur Basis Dateinamen **ErrInit**übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-106">The validated logs are those that exist in the path, and that have the three-letter base log file name passed to **ErrInit**.</span></span>
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="fe0c2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe0c2-107">Parameters</span></span>

### <a name="pfonlyunnecessarylogscorrupt"></a><span data-ttu-id="fe0c2-108">pfOnlyUnnecessaryLogsCorrupt</span><span class="sxs-lookup"><span data-stu-id="fe0c2-108">pfOnlyUnnecessaryLogsCorrupt</span></span> 
  
<span data-ttu-id="fe0c2-109">Output-Parameter.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-109">Output parameter.</span></span> <span data-ttu-id="fe0c2-110">Wenn **true**, dieser Parameter gibt an, dass Fehler in die Transaktionsprotokolldateien, aber diese Fehler gefunden wurden wurden alle gefunden in Protokolldateien, die nicht benötigt werden versetzen die Datenbank in einen Zustand "clean Shutdown" ohne Datenverlust.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-110">When **true**, this parameter indicates that errors were found in the transaction log files, but those errors were all found in log files that are not needed to bring the database to a clean-shutdown state without data loss.</span></span> <span data-ttu-id="fe0c2-111">Der Wert **true** zurückgegeben, die in diesem Parameter gilt nur, wenn **ErrCheckLogs** **ErrSuccess**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-111">A **true** value returned in this parameter is valid only when **ErrCheckLogs** returns **errSuccess**.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="fe0c2-112">ulFlags</span><span class="sxs-lookup"><span data-stu-id="fe0c2-112">ulFlags</span></span>
  
<span data-ttu-id="fe0c2-113">Optionale Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-113">Optional input parameter.</span></span> <span data-ttu-id="fe0c2-114">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-114">This value is reserved for future use.</span></span> <span data-ttu-id="fe0c2-115">Der durch diesen Parameter übergebene Wert muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-115">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fe0c2-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="fe0c2-116">Return value</span></span>

<span data-ttu-id="fe0c2-117">Ein Fehlercode aus der [ERR](cchksgfiles-err-enumeration.md) -Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-117">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
<span data-ttu-id="fe0c2-118">Es ist wichtig, denken Sie daran, dass diese Funktion **ErrSuccess** zurückgeben kann, selbst wenn Fehler in den Protokolldateien gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-118">It's important to remember that this function can return **errSuccess** even when errors are found in the log files.</span></span> <span data-ttu-id="fe0c2-119">Aus diesem Grund beim **ErrCheckLogs** **ErrSuccess**zurückgegeben wird, sollte die Anwendung auch **PfOnlyUnnecessaryLogsCorrupt** Rückgabeparameter überprüfen.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-119">Therefore, when **ErrCheckLogs** returns **errSuccess**, the application should also check the  **pfOnlyUnnecessaryLogsCorrupt** return parameter.</span></span> <span data-ttu-id="fe0c2-120">Wenn **PfOnlyUnnecessaryLogsCorrupts** **ErrCheckLogs** **ErrSuccess**gibt **true** ist, bedeutet dies, dass eine oder mehrere Fehler gefunden wurden, jedoch nur in den Protokolldateien nicht erforderlich, um die Datenbank auf dem neuesten Stand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-120">If **pfOnlyUnnecessaryLogsCorrupts** is **true** when **ErrCheckLogs** returns **errSuccess**, this indicates that one or more errors were found, but only in log files not needed to bring the database up-to-date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe0c2-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe0c2-121">Remarks</span></span>

<span data-ttu-id="fe0c2-122">Bevor die **ErrCheckLogs** -Funktion aufgerufen werden kann, muss die **ErrCheckDbHeaders** -Funktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-122">The **ErrCheckDbHeaders** function must be called before the **ErrCheckLogs** function can be called.</span></span> 
  
<span data-ttu-id="fe0c2-123">Wenn Exchange-Datenbank-Transaktionsprotokolldateien überprüft werden, werden einige der Protokolldateien erforderlich sind, um die Datenbanken in der Speichergruppe in einen Zustand "clean Shutdown" ohne Datenverlust, schalten sein, während andere Protokolldateien möglicherweise nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-123">When Exchange database transaction log files are being checked, some of the log files will be necessary to bring the databases in the storage group to a clean-shutdown state without data loss, whereas other log files might not be needed.</span></span> <span data-ttu-id="fe0c2-124">Die Funktion **ErrCheckLogs** bestimmt die ältesten und neuesten Protokolldateien, die erforderlich sind, um die Datenbanken auf dem aktuellen Stand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-124">The **ErrCheckLogs** function determines both the oldest and the newest log files that are needed to bring the databases up to date.</span></span> 
  
<span data-ttu-id="fe0c2-125">Die Funktion **ErrCheckLogs** überprüft die Protokolldateien in der angegebenen Pfade, die auch den Namen angegebenen drei Buchstaben Basisdatei haben, an die Funktion **ErrInit** übergeben.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-125">The **ErrCheckLogs** function verifies all the log files in the specified paths that also have the specified three-letter base file name, as passed to the **ErrInit** function.</span></span> 
  
<span data-ttu-id="fe0c2-126">Wenn keine Fehler in den Protokolldateien gefunden werden, gibt **ErrCheckLogs** **ErrSuccess**zurück.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-126">If no errors are found in the log files, **ErrCheckLogs** returns **errSuccess**.</span></span> 
  
<span data-ttu-id="fe0c2-127">Wenn eines der erforderlichen Protokolldateien beschädigt gefunden wird, gibt **ErrCheckLogs** einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-127">If any of the required log files are found to be corrupted, **ErrCheckLogs** returns an error.</span></span> 
  
<span data-ttu-id="fe0c2-128">Wenn Fehler nur in den Protokolldateien, die älter als die früheste erforderlich sind gefunden werden, wird die Funktion gibt **ErrSuccess** und wird die Rückgabeparameter **PfOnlyUnnecessaryLogCorrupt** auf **true**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-128">If errors are found only in log files that are older than the earliest ones needed, the function returns **errSuccess** and sets the return parameter **pfOnlyUnnecessaryLogCorrupt** to **true**.</span></span> <span data-ttu-id="fe0c2-129">Die Anwendung sollte erkennen, dass Fehler in einige der die alte Protokolldateien sind, und wenn dies der Fall ist, wird möglicherweise der Benutzer gewarnt werden.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-129">The application should recognize that there are errors in some of those old log files, and if so, it will possibly alert the user.</span></span> <span data-ttu-id="fe0c2-130">Dieser Fehler sollten auf jeden Fall nicht Einfluss auf die allgemeine Integrität der Datenbank oder Einfluss darauf, ob die Protokolle vorwärts Wiedergabe erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-130">In any case, those errors should not affect the overall integrity of the database or affect whether playing the logs forward will succeed.</span></span>
  
<span data-ttu-id="fe0c2-131">In einer Protokolldatei nach den frühesten erstellt wurden, der bestimmt, **ErrCheckLogs** Protokoll ist erforderlich, die Funktion gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-131">If errors are found in any log file created after the earliest log that **ErrCheckLogs** determines is needed, the function returns an error.</span></span> <span data-ttu-id="fe0c2-132">Der Fehler wird zurückgegeben, selbst wenn in der Datei Fehlern gefunden wurde eine Protokolldatei, die später als generiert wurde ist erforderlich, um die Datenbank auf dem aktuellen Stand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-132">The error will be returned even if the log file error was found in a log file that was generated later than what is needed to bring the database up to date.</span></span> <span data-ttu-id="fe0c2-133">Obwohl es möglich, einen clean Shutdown-Status die Datenbanken mithilfe der identifizierten Protokolldateien Unterlagen werden würde, würde Transaktionen, die in den später beschädigten Protokolldateien angegeben nicht angewendet werden Datenverlust entstehen kann, wenn die Datenbank wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-133">Although it would be possible to bring the databases to a clean-shutdown state by using the identified log files, transactions specified in the later corrupted log files would not be applied, resulting in data loss when the database is restored.</span></span> 
  
<span data-ttu-id="fe0c2-134">Das Objekt **CChkSGFiles** bestimmt, ob alle Protokolldateien, die mit der Funktion **ErrInit** registriert tatsächlich aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-134">The **CChkSGFiles** object determines whether all of the log files registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="fe0c2-135">Wenn nicht alle Protokolle nicht erfolgreich überprüft wurden, die **ErrTerm** -Funktion gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-135">If not all of the logs were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="fe0c2-136">Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, können Sie die **ErrCheckLogs** -Funktion im Multithread-Teil der Anwendung aufrufen, jedoch können Sie nur einmal für jede **CCheckSGFiles** -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-136">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckLogs** function in the multithreaded portion of the application, but you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="fe0c2-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe0c2-137">Requirements</span></span>

<span data-ttu-id="fe0c2-138">Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-138">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="fe0c2-139">Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fe0c2-139">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

