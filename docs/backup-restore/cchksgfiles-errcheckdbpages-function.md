---
title: CChkSGFiles. ErrCheckDbPages-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbPages
api_type:
- dllExport
ms.assetid: 5e981a7c-28cd-470c-b7eb-606463e9dd05
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: 78d2dbee6253096d597b4ec2de3878f40ee1b6d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526725"
---
# <a name="cchksgfileserrcheckdbpages-function"></a><span data-ttu-id="5746b-103">CChkSGFiles. ErrCheckDbPages-Funktion</span><span class="sxs-lookup"><span data-stu-id="5746b-103">CChkSGFiles.ErrCheckDbPages function</span></span>

<span data-ttu-id="5746b-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="5746b-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="5746b-105">Überprüft einen Bereich von Seiten in einer angegebenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5746b-105">Validates a range of pages in a specified database.</span></span> 
  
```cs
Vitual ERRErrCheckDbPages  
(
    Const ULONGiDb,
    Const VOID  * const pvPageBuffer,
    Const ULONGcbPageBuffer,
    PAGE_INFOrgPageInfo[],
    Const ULONGcPageInfo,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="5746b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5746b-106">Parameters</span></span>

### <a name="idb"></a><span data-ttu-id="5746b-107">iDb</span><span class="sxs-lookup"><span data-stu-id="5746b-107">iDb</span></span>
  
<span data-ttu-id="5746b-108">Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="5746b-108">Input parameter.</span></span> <span data-ttu-id="5746b-109">Ein Index in das im **rgwszDb []** -Parameter angegebene Array von Datenbanken für die **ErrInit** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5746b-109">An index into the array of databases specified in the **rgwszDb[]** parameter to the **ErrInit** function.</span></span> <span data-ttu-id="5746b-110">Die von diesem Parameter indizierte Datenbank wird überprüft.</span><span class="sxs-lookup"><span data-stu-id="5746b-110">The database indexed by this parameter will be checked.</span></span> 
    
### <a name="pvpagebuffer"></a><span data-ttu-id="5746b-111">pvPageBuffer</span><span class="sxs-lookup"><span data-stu-id="5746b-111">pvPageBuffer</span></span> 
  
<span data-ttu-id="5746b-112">Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="5746b-112">Input parameter.</span></span> <span data-ttu-id="5746b-113">Ein Zeiger auf einen Puffer, der eine oder mehrere zu überprüfende Datenbankseiten enthält.</span><span class="sxs-lookup"><span data-stu-id="5746b-113">A pointer to a buffer containing one or more database pages to be checked.</span></span> <span data-ttu-id="5746b-114">Die Größe des Puffers muss ein Vielfaches der Datenbankseitengröße sein, wie er im **pcbDbPageSize** -Parameter von der **ErrCheckDbHeaders** -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5746b-114">The size of the buffer must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> <span data-ttu-id="5746b-115">Die aufrufende Anwendung muss den Puffer mit dem Inhalt der Datenbankseite füllen, bevor **ErrCheckDbPages**aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5746b-115">The calling application must fill the buffer with the database page contents before calling **ErrCheckDbPages**.</span></span>
    
### <a name="cbpagebuffer"></a><span data-ttu-id="5746b-116">cbPageBuffer</span><span class="sxs-lookup"><span data-stu-id="5746b-116">cbPageBuffer</span></span>
  
<span data-ttu-id="5746b-117">Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="5746b-117">Input parameter.</span></span> <span data-ttu-id="5746b-118">Die Größe des **pvPageBuffer** -Parameters in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5746b-118">The size of the **pvPageBuffer** parameter, in bytes.</span></span> <span data-ttu-id="5746b-119">Dieser Wert muss ein Vielfaches der Datenbankseitengröße sein, wie er im **pcbDbPageSize** -Parameter von der **ErrCheckDbHeaders** -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5746b-119">This value must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> 
    
### <a name="rgpageinfo"></a><span data-ttu-id="5746b-120">rgPageInfo[]</span><span class="sxs-lookup"><span data-stu-id="5746b-120">rgPageInfo[]</span></span> 
  
<span data-ttu-id="5746b-121">Input/Output-Parameter.</span><span class="sxs-lookup"><span data-stu-id="5746b-121">Input/output parameter.</span></span> <span data-ttu-id="5746b-122">Ein Array von **Seiten \_ Info** Strukturen, das von **ErrCheckDbPages** mit detaillierten Ergebnissen jeder geprüften Datenbankseite gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="5746b-122">An array of **PAGE\_INFO** structures that **ErrCheckDbPages** fills with detailed results of each database page that is checked.</span></span> <span data-ttu-id="5746b-123">Das Array muss ein Element für jede Datenbankseite haben, die im **pvPageBuffer** -Parameter übergeben wird, und das **ulPgno** -Feld in jeder **Seiten \_ Info** Struktur muss auf die logische Seitenzahl festgelegt werden, die der Datenbankseite entspricht.</span><span class="sxs-lookup"><span data-stu-id="5746b-123">The array must have one element for each database page passed in the **pvPageBuffer** parameter, and the **ulPgno** field in each **PAGE\_INFO** structure must be set to the logical page number that corresponds to the database page.</span></span> <span data-ttu-id="5746b-124">Weitere Informationen finden Sie weiter unten in diesem Thema unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="5746b-124">For more information, see "Remarks" later in this topic.</span></span> 
    
### <a name="cpageinfo"></a><span data-ttu-id="5746b-125">cPageInfo</span><span class="sxs-lookup"><span data-stu-id="5746b-125">cPageInfo</span></span>
  
<span data-ttu-id="5746b-126">Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="5746b-126">Input parameter.</span></span> <span data-ttu-id="5746b-127">Die Anzahl der Einträge im **rgPageInfo []** -Array.</span><span class="sxs-lookup"><span data-stu-id="5746b-127">The number of entries in the **rgPageInfo[]** array.</span></span> <span data-ttu-id="5746b-128">Dieser Wert muss der Anzahl der Datenbankseiten entsprechen, die im Parameter **pvPageBuffer** übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="5746b-128">This value must be equal to the number of database pages passed in the **pvPageBuffer** parameter.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="5746b-129">ulFlags</span><span class="sxs-lookup"><span data-stu-id="5746b-129">ulFlags</span></span> 
  
<span data-ttu-id="5746b-130">Optionaler Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="5746b-130">Optional input parameter.</span></span> <span data-ttu-id="5746b-131">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5746b-131">This value is reserved for future use.</span></span> <span data-ttu-id="5746b-132">Der in diesem Parameter übergebene Wert sollte 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="5746b-132">The value passed in this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5746b-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5746b-133">Return value</span></span>

<span data-ttu-id="5746b-134">Ein Fehlercode aus der [Err](cchksgfiles-err-enumeration.md) -Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="5746b-134">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5746b-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5746b-135">Remarks</span></span>

<span data-ttu-id="5746b-136">Beachten Sie, dass Sie die Datenbank im Array von Datenbanken angegeben haben müssen, die an die **ErrInit** -Funktion übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="5746b-136">Note that you need to have specified the database in the array of databases passed to the **ErrInit** function.</span></span> <span data-ttu-id="5746b-137">Außerdem muss **ErrCheckDbHeaders** vor **ErrCheckDbPages**aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5746b-137">Also, **ErrCheckDbHeaders** must be called before **ErrCheckDbPages**.</span></span>
  
<span data-ttu-id="5746b-138">Die aufrufende Anwendung muss einen Arbeitsspeicherpuffer zuweisen, der groß genug ist, um die zu prüfenden Datenbankseiten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5746b-138">The calling application must allocate a memory buffer that is large enough to hold the database pages to be checked.</span></span> <span data-ttu-id="5746b-139">Die Anwendung ist für das Ausfüllen des Puffers mit dem Inhalt einer oder mehrerer solcher Datenbankseiten verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="5746b-139">The application is responsible for filling the buffer with the contents of one or more such database pages.</span></span> 
  
<span data-ttu-id="5746b-140">Die aufrufende Anwendung muss **ErrCheckDbHeaders** vor dem Aufruf von **ErrCheckDbPages**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5746b-140">The calling application must call **ErrCheckDbHeaders** before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="5746b-141">Diese Funktion kann so oft wie erforderlich aufgerufen werden, um alle Seiten in allen Datenbankdateien abzudecken, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5746b-141">This function can be called as many times as necessary to cover all the pages in all database files that are to be checked.</span></span>
  
<span data-ttu-id="5746b-142">Im **rgPageInfo []** -Parameter enthält jedes zurückgegebene Elementinformationen zur Datenbankseite in einer **Seiten \_ Info** Struktur.</span><span class="sxs-lookup"><span data-stu-id="5746b-142">In the **rgPageInfo[]** parameter, each element returned contains information about the database page in a **PAGE\_INFO** structure.</span></span> <span data-ttu-id="5746b-143">Wenn die **ErrCheckDbPages** -Funktion einen Fehler zurückgibt, sollte die Anwendung jede **Seiten \_ Info** Struktur überprüfen, um zu bestimmen, auf welcher Seite der Fehler gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="5746b-143">If the **ErrCheckDbPages** function returns an error, the application should check each **PAGE\_INFO** structure to determine on which page the error was found.</span></span> <span data-ttu-id="5746b-144">Wenn Sie beispielsweise den **checksumActual** -und den **checksumExpected** -Wert vergleichen, wird angegeben, ob auf dieser Datenbankseite ein Prüfsummenfehler erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="5746b-144">For example, comparing the **checksumActual** and **checksumExpected** values will indicate whether a checksum error was detected on that database page.</span></span> 
  
<span data-ttu-id="5746b-145">Wenn **ErrCheckDbPages** Fehler im Datenbankinhalt erkennt, wird ein Windows-Fehlerereignisprotokoll Eintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="5746b-145">If **ErrCheckDbPages** detects any errors in the database content, it will create a Windows Error event log entry.</span></span> 
  
<span data-ttu-id="5746b-146">Das **CChkSGFiles** -Objekt bestimmt, ob alle Datenbanken, die mit der **ErrInit** -Funktion registriert wurden, tatsächlich überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="5746b-146">The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="5746b-147">Insbesondere verwendet **CChkSGFiles** die **ErrCheckDbPages** -Funktion, um zu bestimmen, ob die gleiche Anzahl von Datenbankseiten, die von **ErrCheckDbHeaders** angezeigt wurden, tatsächlich überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="5746b-147">Specifically, **CChkSGFiles** uses the **ErrCheckDbPages** function to determine whether the same number of database pages indicated by **ErrCheckDbHeaders** were actually verified.</span></span> <span data-ttu-id="5746b-148">Wenn die richtige Anzahl von Seiten in jeder Datenbank nicht erfolgreich überprüft wurde, gibt die **ErrTerm** -Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5746b-148">If the correct number of pages in each database were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="5746b-149">Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, können Sie die **ErrCheckDbPages** -Funktion im Multithread-Teil der Anwendung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5746b-149">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckDbPages** function in the multithreaded portion of the application.</span></span> <span data-ttu-id="5746b-150">Beachten Sie, dass **ErrCheckDbPages** in der Regel für jede geprüfte Datenbank mehrmals aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5746b-150">Note that **ErrCheckDbPages** is typically called multiple times for each database that is checked.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="5746b-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5746b-151">Requirements</span></span>

<span data-ttu-id="5746b-152">Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="5746b-152">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="5746b-153">Das Konto, unter dem die Anwendung betrieben wird, muss über Leseberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="5746b-153">The account that the application is running under must have read permissions to the database and log files that are to be checked.</span></span>
  

