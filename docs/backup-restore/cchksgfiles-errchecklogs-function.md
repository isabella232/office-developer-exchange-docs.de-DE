---
title: CChkSGFiles. ErrCheckLogs-Funktion
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
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: 71e21bb3a748a532f9e3167e0b36898acde71b02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526718"
---
# <a name="cchksgfileserrchecklogs-function"></a><span data-ttu-id="77b00-103">CChkSGFiles. ErrCheckLogs-Funktion</span><span class="sxs-lookup"><span data-stu-id="77b00-103">CChkSGFiles.ErrCheckLogs function</span></span>

<span data-ttu-id="77b00-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="77b00-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="77b00-105">Überprüft die Protokolldateien aller Datenbankdateien, die in der **ErrInit** -Funktion angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="77b00-105">Validates the log files of all the database files that were specified in the **ErrInit** function.</span></span> <span data-ttu-id="77b00-106">Die überprüften Protokolle sind diejenigen, die im Pfad vorhanden sind und die den Namen der Basisprotokoll Datei mit drei Buchstaben an **ErrInit**übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="77b00-106">The validated logs are those that exist in the path, and that have the three-letter base log file name passed to **ErrInit**.</span></span>
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="77b00-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="77b00-107">Parameters</span></span>

### <a name="pfonlyunnecessarylogscorrupt"></a><span data-ttu-id="77b00-108">pfOnlyUnnecessaryLogsCorrupt</span><span class="sxs-lookup"><span data-stu-id="77b00-108">pfOnlyUnnecessaryLogsCorrupt</span></span> 
  
<span data-ttu-id="77b00-109">Output-Parameter.</span><span class="sxs-lookup"><span data-stu-id="77b00-109">Output parameter.</span></span> <span data-ttu-id="77b00-110">Bei **true**gibt dieser Parameter an, dass Fehler in den Transaktionsprotokolldateien gefunden wurden, aber diese Fehler wurden alle in Protokolldateien gefunden, die nicht erforderlich sind, um die Datenbank ohne Datenverlust in den Zustand "Clean Shutdown" zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="77b00-110">When **true**, this parameter indicates that errors were found in the transaction log files, but those errors were all found in log files that are not needed to bring the database to a clean-shutdown state without data loss.</span></span> <span data-ttu-id="77b00-111">Ein **true** -Wert, der in diesem Parameter zurückgegeben wird, ist nur gültig, wenn **ErrCheckLogs** **errSuccess**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="77b00-111">A **true** value returned in this parameter is valid only when **ErrCheckLogs** returns **errSuccess**.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="77b00-112">ulFlags</span><span class="sxs-lookup"><span data-stu-id="77b00-112">ulFlags</span></span>
  
<span data-ttu-id="77b00-113">Optionaler Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="77b00-113">Optional input parameter.</span></span> <span data-ttu-id="77b00-114">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="77b00-114">This value is reserved for future use.</span></span> <span data-ttu-id="77b00-115">Der von diesem Parameter übergebene Wert sollte 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="77b00-115">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="77b00-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77b00-116">Return value</span></span>

<span data-ttu-id="77b00-117">Ein Fehlercode aus der [Err](cchksgfiles-err-enumeration.md) -Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="77b00-117">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
<span data-ttu-id="77b00-118">Beachten Sie, dass diese Funktion **errSuccess** auch dann zurückgeben kann, wenn Fehler in den Protokolldateien gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="77b00-118">It's important to remember that this function can return **errSuccess** even when errors are found in the log files.</span></span> <span data-ttu-id="77b00-119">Wenn **ErrCheckLogs** also **errSuccess**zurückgibt, sollte die Anwendung auch den **pfOnlyUnnecessaryLogsCorrupt** -Rückgabeparameter überprüfen.</span><span class="sxs-lookup"><span data-stu-id="77b00-119">Therefore, when **ErrCheckLogs** returns **errSuccess**, the application should also check the  **pfOnlyUnnecessaryLogsCorrupt** return parameter.</span></span> <span data-ttu-id="77b00-120">Wenn **pfOnlyUnnecessaryLogsCorrupts** auf **true** festgelegt ist, wenn **ErrCheckLogs** **errSuccess**zurückgibt, deutet dies darauf hin, dass ein oder mehrere Fehler gefunden wurden, jedoch nur in Protokolldateien, die nicht benötigt wurden, um die Datenbank auf den neuesten Stand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="77b00-120">If **pfOnlyUnnecessaryLogsCorrupts** is **true** when **ErrCheckLogs** returns **errSuccess**, this indicates that one or more errors were found, but only in log files not needed to bring the database up-to-date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="77b00-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77b00-121">Remarks</span></span>

<span data-ttu-id="77b00-122">Die **ErrCheckDbHeaders** -Funktion muss aufgerufen werden, bevor die **ErrCheckLogs** -Funktion aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="77b00-122">The **ErrCheckDbHeaders** function must be called before the **ErrCheckLogs** function can be called.</span></span> 
  
<span data-ttu-id="77b00-123">Wenn die Transaktionsprotokolldateien von Exchange-Datenbank überprüft werden, sind einige Protokolldateienerforderlich, um die Datenbanken in der Speichergruppe ohne Datenverlust in den Zustand "Clean Shutdown" zu versetzen, während andere Protokolldateien möglicherweise nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="77b00-123">When Exchange database transaction log files are being checked, some of the log files will be necessary to bring the databases in the storage group to a clean-shutdown state without data loss, whereas other log files might not be needed.</span></span> <span data-ttu-id="77b00-124">Die **ErrCheckLogs** -Funktion bestimmt sowohl die älteste als auch die neueste Protokolldatei, die zum Aktualisieren der Datenbanken benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="77b00-124">The **ErrCheckLogs** function determines both the oldest and the newest log files that are needed to bring the databases up to date.</span></span> 
  
<span data-ttu-id="77b00-125">Die **ErrCheckLogs** -Funktion überprüft alle Protokolldateien in den angegebenen Pfaden, die auch den angegebenen Namen der Basisdatei mit drei Buchstaben aufweisen und an die **ErrInit** -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="77b00-125">The **ErrCheckLogs** function verifies all the log files in the specified paths that also have the specified three-letter base file name, as passed to the **ErrInit** function.</span></span> 
  
<span data-ttu-id="77b00-126">Wenn in den Protokolldateien keine Fehler gefunden werden, **ErrCheckLogs** gibt ErrCheckLogs **errSuccess**zurück.</span><span class="sxs-lookup"><span data-stu-id="77b00-126">If no errors are found in the log files, **ErrCheckLogs** returns **errSuccess**.</span></span> 
  
<span data-ttu-id="77b00-127">Wenn eine der erforderlichen Protokolldateien als beschädigt festgestellt wird, gibt **ErrCheckLogs** einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="77b00-127">If any of the required log files are found to be corrupted, **ErrCheckLogs** returns an error.</span></span> 
  
<span data-ttu-id="77b00-128">Wenn Fehler nur in Protokolldateien gefunden werden, die älter als die frühesten sind, die benötigt werden, gibt die Funktion **errSuccess** zurück und legt den Rückgabeparameter **pfOnlyUnnecessaryLogCorrupt** auf **true**fest.</span><span class="sxs-lookup"><span data-stu-id="77b00-128">If errors are found only in log files that are older than the earliest ones needed, the function returns **errSuccess** and sets the return parameter **pfOnlyUnnecessaryLogCorrupt** to **true**.</span></span> <span data-ttu-id="77b00-129">Die Anwendung sollte erkennen, dass in einigen dieser alten Protokolldateien Fehler vorliegen, und wenn dies der Fall ist, wird der Benutzer möglicherweise gewarnt.</span><span class="sxs-lookup"><span data-stu-id="77b00-129">The application should recognize that there are errors in some of those old log files, and if so, it will possibly alert the user.</span></span> <span data-ttu-id="77b00-130">In jedem Fall sollten diese Fehler keine Auswirkungen auf die Gesamtintegrität der Datenbank haben oder sich darauf auswirken, ob die Wiedergabe der Protokolle erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77b00-130">In any case, those errors should not affect the overall integrity of the database or affect whether playing the logs forward will succeed.</span></span>
  
<span data-ttu-id="77b00-131">Wenn Fehler in einer Protokolldatei gefunden werden, die nach dem frühesten Protokoll erstellt wurde, das von **ErrCheckLogs** bestimmt wird, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="77b00-131">If errors are found in any log file created after the earliest log that **ErrCheckLogs** determines is needed, the function returns an error.</span></span> <span data-ttu-id="77b00-132">Der Fehler wird auch dann zurückgegeben, wenn der Protokolldatei Fehler in einer Protokolldatei gefunden wurde, die später als erforderlich generiert wurde, um die Datenbank auf den neuesten Stand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="77b00-132">The error will be returned even if the log file error was found in a log file that was generated later than what is needed to bring the database up to date.</span></span> <span data-ttu-id="77b00-133">Obwohl es möglich wäre, die Datenbanken mithilfe der identifizierten Protokolldateien in den Zustand "Clean Shutdown" zu versetzen, wurden in den später beschädigten Protokolldateien angegebene Transaktionen nicht angewendet, was zu einem Datenverlust bei der Wiederherstellung der Datenbank führte.</span><span class="sxs-lookup"><span data-stu-id="77b00-133">Although it would be possible to bring the databases to a clean-shutdown state by using the identified log files, transactions specified in the later corrupted log files would not be applied, resulting in data loss when the database is restored.</span></span> 
  
<span data-ttu-id="77b00-134">Das **CChkSGFiles** -Objekt bestimmt, ob alle mit der **ErrInit** -Funktion registrierten Protokolldateien tatsächlich überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="77b00-134">The **CChkSGFiles** object determines whether all of the log files registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="77b00-135">Wenn nicht alle Protokolle erfolgreich überprüft wurden, gibt die **ErrTerm** -Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="77b00-135">If not all of the logs were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="77b00-136">Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, können Sie die **ErrCheckLogs** -Funktion im Multithread-Teil der Anwendung aufrufen, Sie können Sie jedoch nur einmal für jedes **CCheckSGFiles** -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="77b00-136">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckLogs** function in the multithreaded portion of the application, but you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="77b00-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77b00-137">Requirements</span></span>

<span data-ttu-id="77b00-138">Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="77b00-138">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="77b00-139">Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="77b00-139">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

