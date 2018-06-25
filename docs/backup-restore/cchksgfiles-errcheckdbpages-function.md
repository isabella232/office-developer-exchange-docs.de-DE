---
title: CChkSGFiles.ErrCheckDbPages-Funktion
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
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: f1588b1dbc4bd7e83683fa4432a175405ad17903
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756803"
---
# <a name="cchksgfileserrcheckdbpages-function"></a><span data-ttu-id="29e1e-103">CChkSGFiles.ErrCheckDbPages-Funktion</span><span class="sxs-lookup"><span data-stu-id="29e1e-103">CChkSGFiles.ErrCheckDbPages function</span></span>

<span data-ttu-id="29e1e-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="29e1e-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="29e1e-105">Überprüft einen Bereich von Seiten in einer angegebenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="29e1e-105">Validates a range of pages in a specified database.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="29e1e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="29e1e-106">Parameters</span></span>

### <a name="idb"></a><span data-ttu-id="29e1e-107">iDb</span><span class="sxs-lookup"><span data-stu-id="29e1e-107">iDb</span></span>
  
<span data-ttu-id="29e1e-108">Input-Parameter.</span><span class="sxs-lookup"><span data-stu-id="29e1e-108">Input parameter.</span></span> <span data-ttu-id="29e1e-109">Ein Index in das Array von Datenbanken, die im Parameter an die Funktion **ErrInit** **RgwszDb []** angegeben.</span><span class="sxs-lookup"><span data-stu-id="29e1e-109">An index into the array of databases specified in the **rgwszDb[]** parameter to the **ErrInit** function.</span></span> <span data-ttu-id="29e1e-110">Die Datenbank, die von diesem Parameter indiziert werden überprüft.</span><span class="sxs-lookup"><span data-stu-id="29e1e-110">The database indexed by this parameter will be checked.</span></span> 
    
### <a name="pvpagebuffer"></a><span data-ttu-id="29e1e-111">pvPageBuffer</span><span class="sxs-lookup"><span data-stu-id="29e1e-111">pvPageBuffer</span></span> 
  
<span data-ttu-id="29e1e-112">Input-Parameter.</span><span class="sxs-lookup"><span data-stu-id="29e1e-112">Input parameter.</span></span> <span data-ttu-id="29e1e-113">Ein Zeiger auf einen Puffer mit mindestens Datenbankseiten überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="29e1e-113">A pointer to a buffer containing one or more database pages to be checked.</span></span> <span data-ttu-id="29e1e-114">Die Größe des Puffers muss ein Vielfaches von Seitengröße der Datenbank, wie in der **PcbDbPageSize** -Parameter von der Funktion **ErrCheckDbHeaders** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="29e1e-114">The size of the buffer must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> <span data-ttu-id="29e1e-115">Die aufrufende Anwendung muss den Puffer mit dem Inhalt der Datenbank vor dem Aufruf von **ErrCheckDbPages**ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="29e1e-115">The calling application must fill the buffer with the database page contents before calling **ErrCheckDbPages**.</span></span>
    
### <a name="cbpagebuffer"></a><span data-ttu-id="29e1e-116">cbPageBuffer</span><span class="sxs-lookup"><span data-stu-id="29e1e-116">cbPageBuffer</span></span>
  
<span data-ttu-id="29e1e-117">Input-Parameter.</span><span class="sxs-lookup"><span data-stu-id="29e1e-117">Input parameter.</span></span> <span data-ttu-id="29e1e-118">Die Größe des Parameters **PvPageBuffer** in Byte.</span><span class="sxs-lookup"><span data-stu-id="29e1e-118">The size of the **pvPageBuffer** parameter, in bytes.</span></span> <span data-ttu-id="29e1e-119">Dieser Wert muss ein Vielfaches von Seitengröße der Datenbank sein, wie im Parameter **PcbDbPageSize** durch die **ErrCheckDbHeaders** -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="29e1e-119">This value must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> 
    
### <a name="rgpageinfo"></a><span data-ttu-id="29e1e-120">RgPageInfo]</span><span class="sxs-lookup"><span data-stu-id="29e1e-120">rgPageInfo[]</span></span> 
  
<span data-ttu-id="29e1e-121">Input/Output-Parameter.</span><span class="sxs-lookup"><span data-stu-id="29e1e-121">Input/output parameter.</span></span> <span data-ttu-id="29e1e-122">Ein Array von **Seite\_INFO** Strukturen, die mit **ErrCheckDbPages** füllt ausführliche Ergebnisse jeder Datenbank-Seite, die eingecheckt wird.</span><span class="sxs-lookup"><span data-stu-id="29e1e-122">An array of **PAGE\_INFO** structures that **ErrCheckDbPages** fills with detailed results of each database page that is checked.</span></span> <span data-ttu-id="29e1e-123">Das Array muss ein Element für jede Datenbankseite in der **PvPageBuffer** -Parameter und das Feld **UlPgno** in den einzelnen übergeben haben **Seite\_INFO** Struktur muss festgelegt werden, um die logische Seitenzahl, die der Datenbankseite entspricht.</span><span class="sxs-lookup"><span data-stu-id="29e1e-123">The array must have one element for each database page passed in the **pvPageBuffer** parameter, and the **ulPgno** field in each **PAGE\_INFO** structure must be set to the logical page number that corresponds to the database page.</span></span> <span data-ttu-id="29e1e-124">Weitere Informationen finden Sie unter "Hinweise" weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="29e1e-124">For more information, see "Remarks" later in this topic.</span></span> 
    
### <a name="cpageinfo"></a><span data-ttu-id="29e1e-125">cPageInfo</span><span class="sxs-lookup"><span data-stu-id="29e1e-125">cPageInfo</span></span>
  
<span data-ttu-id="29e1e-126">Input-Parameter.</span><span class="sxs-lookup"><span data-stu-id="29e1e-126">Input parameter.</span></span> <span data-ttu-id="29e1e-127">Die Anzahl der Einträge im Array **RgPageInfo []** .</span><span class="sxs-lookup"><span data-stu-id="29e1e-127">The number of entries in the **rgPageInfo[]** array.</span></span> <span data-ttu-id="29e1e-128">Dieser Wert muss gleich der Anzahl von Datenbankseiten im **PvPageBuffer** -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="29e1e-128">This value must be equal to the number of database pages passed in the **pvPageBuffer** parameter.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="29e1e-129">ulFlags</span><span class="sxs-lookup"><span data-stu-id="29e1e-129">ulFlags</span></span> 
  
<span data-ttu-id="29e1e-130">Optionale Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="29e1e-130">Optional input parameter.</span></span> <span data-ttu-id="29e1e-131">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="29e1e-131">This value is reserved for future use.</span></span> <span data-ttu-id="29e1e-132">Der in diesem Parameter übergebene Wert muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="29e1e-132">The value passed in this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="29e1e-133">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="29e1e-133">Return value</span></span>

<span data-ttu-id="29e1e-134">Ein Fehlercode aus der [ERR](cchksgfiles-err-enumeration.md) -Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="29e1e-134">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="29e1e-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="29e1e-135">Remarks</span></span>

<span data-ttu-id="29e1e-136">Beachten Sie, dass müssen Sie die Datenbank in das Array von Datenbanken, die an die Funktion **ErrInit** übergeben angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="29e1e-136">Note that you need to have specified the database in the array of databases passed to the **ErrInit** function.</span></span> <span data-ttu-id="29e1e-137">Darüber hinaus muss **ErrCheckDbHeaders** vor **ErrCheckDbPages**aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="29e1e-137">Also, **ErrCheckDbHeaders** must be called before **ErrCheckDbPages**.</span></span>
  
<span data-ttu-id="29e1e-138">Die aufrufende Anwendung muss Speicherpuffers zuweisen, die groß genug für die Datenbankseiten überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="29e1e-138">The calling application must allocate a memory buffer that is large enough to hold the database pages to be checked.</span></span> <span data-ttu-id="29e1e-139">Die Anwendung ist verantwortlich für die Puffer mit dem Inhalt von mindestens einen solchen Datenbankseiten ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="29e1e-139">The application is responsible for filling the buffer with the contents of one or more such database pages.</span></span> 
  
<span data-ttu-id="29e1e-140">Die aufrufende Anwendung muss vor dem Aufruf von **ErrCheckDbPages** **ErrCheckDbHeaders** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="29e1e-140">The calling application must call **ErrCheckDbHeaders** before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="29e1e-141">So oft wie erforderlich sind, um alle Seiten in allen Datenbankdateien behandelt, die überprüft werden sollen, kann diese Funktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="29e1e-141">This function can be called as many times as necessary to cover all the pages in all database files that are to be checked.</span></span>
  
<span data-ttu-id="29e1e-142">In der Parameter **RgPageInfo []** jedes zurückgegebene Element enthält Informationen zu der Datenbankseite in einer **Seite\_INFO** Struktur.</span><span class="sxs-lookup"><span data-stu-id="29e1e-142">In the **rgPageInfo[]** parameter, each element returned contains information about the database page in a **PAGE\_INFO** structure.</span></span> <span data-ttu-id="29e1e-143">Wenn die **ErrCheckDbPages** -Funktion einen Fehler zurückgibt, sollte die Anwendung überprüfen jeweils **Seite\_INFO** Struktur, um festzulegen, auf welcher Seite der Fehler gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="29e1e-143">If the **ErrCheckDbPages** function returns an error, the application should check each **PAGE\_INFO** structure to determine on which page the error was found.</span></span> <span data-ttu-id="29e1e-144">Vergleichen die Werte **ChecksumActual** und **ChecksumExpected** wird beispielsweise angeben, ob ein Prüfsummenfehler auf der Datenbankseite erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="29e1e-144">For example, comparing the **checksumActual** and **checksumExpected** values will indicate whether a checksum error was detected on that database page.</span></span> 
  
<span data-ttu-id="29e1e-145">Wenn **ErrCheckDbPages** Fehler in der Datenbank erkennt, erstellt er einen Ereignisprotokolleintrag Windows-Fehler.</span><span class="sxs-lookup"><span data-stu-id="29e1e-145">If **ErrCheckDbPages** detects any errors in the database content, it will create a Windows Error event log entry.</span></span> 
  
<span data-ttu-id="29e1e-146">Das Objekt **CChkSGFiles** bestimmt, ob alle Datenbanken, die mit der Funktion **ErrInit** registriert tatsächlich aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="29e1e-146">The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="29e1e-147">Insbesondere wird **CChkSGFiles** die **ErrCheckDbPages** -Funktion verwendet, um zu bestimmen, ob die gleiche Anzahl von Datenbankseiten angegeben durch **ErrCheckDbHeaders** tatsächlich überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="29e1e-147">Specifically, **CChkSGFiles** uses the **ErrCheckDbPages** function to determine whether the same number of database pages indicated by **ErrCheckDbHeaders** were actually verified.</span></span> <span data-ttu-id="29e1e-148">Wenn die richtige Anzahl von Seiten in jeder Datenbank nicht erfolgreich überprüft wurden, gibt die **ErrTerm** -Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="29e1e-148">If the correct number of pages in each database were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="29e1e-149">Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, können Sie die **ErrCheckDbPages** -Funktion im Multithread-Teil der Anwendung anrufen.</span><span class="sxs-lookup"><span data-stu-id="29e1e-149">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckDbPages** function in the multithreaded portion of the application.</span></span> <span data-ttu-id="29e1e-150">Beachten Sie, dass **ErrCheckDbPages** in der Regel mehrere Male für jede Datenbank aufgerufen wird, der überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="29e1e-150">Note that **ErrCheckDbPages** is typically called multiple times for each database that is checked.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="29e1e-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29e1e-151">Requirements</span></span>

<span data-ttu-id="29e1e-152">Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="29e1e-152">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="29e1e-153">Das Konto, unter die Anwendung ausgeführt wird, muss Berechtigungen für die Datenbank- und Protokolldateien Dateien gelesen haben, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="29e1e-153">The account that the application is running under must have read permissions to the database and log files that are to be checked.</span></span>
  

