---
title: CChkSGFiles. ErrCheckDbHeaders-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbHeaders
api_type:
- dllExport
ms.assetid: 75289cd2-35b1-4f75-a651-dce01f1ddda1
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: a62c5940322d3d7a71f2db93214f1e970fc6859b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455247"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a><span data-ttu-id="fc7eb-103">CChkSGFiles. ErrCheckDbHeaders-Funktion</span><span class="sxs-lookup"><span data-stu-id="fc7eb-103">CChkSGFiles.ErrCheckDbHeaders function</span></span>

<span data-ttu-id="fc7eb-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc7eb-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span> 
  
<span data-ttu-id="fc7eb-105">Überprüft die Header der Datenbankdateien, die von der **ErrInit** -Funktion angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-105">Validates the headers of the database files that were specified by the **ErrInit** function.</span></span> <span data-ttu-id="fc7eb-106">Diese Funktion gibt auch die Seitengröße und die Anzahl der Seiten in jeder der angegebenen Datenbanken zurück.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-106">This function also returns the page size and number of pages in each of the specified databases.</span></span> 
  
```cs
Vitual ERRErrCheckDbHeaders  
(
        ULONG  * const pcbDbPageSize,
        ULONG  * const pcHeaderPagesPerDb,
        ULONG   const piDbErrorEncountered,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="fc7eb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc7eb-107">Parameters</span></span>

### <a name="pcbdbpagesize"></a><span data-ttu-id="fc7eb-108">pcbDbPageSize</span><span class="sxs-lookup"><span data-stu-id="fc7eb-108">pcbDbPageSize</span></span> 
  
<span data-ttu-id="fc7eb-109">Output-Parameter.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-109">Output parameter.</span></span> <span data-ttu-id="fc7eb-110">Die Seitengröße jeder der angegebenen Datenbanken in Bytes.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-110">The page size of each of the specified databases, in bytes.</span></span>
    
### <a name="pcheaderpagesperdb"></a><span data-ttu-id="fc7eb-111">pcHeaderPagesPerDb</span><span class="sxs-lookup"><span data-stu-id="fc7eb-111">pcHeaderPagesPerDb</span></span> 
  
<span data-ttu-id="fc7eb-112">Output-Parameter.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-112">Output parameter.</span></span> <span data-ttu-id="fc7eb-113">Die Anzahl der Seiten am Anfang jeder angegebenen Datenbank, die vom Datenbankmodul für die interne Verwendung reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-113">The number of pages at the beginning of each specified database that are reserved by the database engine for internal use.</span></span> <span data-ttu-id="fc7eb-114">Beachten Sie, dass Sie *keine* Kopfzeilenseiten zur Validierung an die **ErrCheckDbPages** -Funktion übergeben sollten.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-114">Note that you should *not* pass header pages to the **ErrCheckDbPages** function for validation.</span></span> 
    
### <a name="pidberrorencountered"></a><span data-ttu-id="fc7eb-115">piDbErrorEncountered</span><span class="sxs-lookup"><span data-stu-id="fc7eb-115">piDbErrorEncountered</span></span>
  
<span data-ttu-id="fc7eb-116">Output-Parameter.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-116">Output parameter.</span></span> <span data-ttu-id="fc7eb-117">Wenn der Rückgabewert der Funktion einen Fehler angibt, ist dieser Parameter ein Index in das **rgwszDb []** -Array, das an die **ErrInit** -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-117">If the return value of the function indicates an error, this parameter will be an index into the **rgwszDb[]** array passed to the **ErrInit** function.</span></span> <span data-ttu-id="fc7eb-118">Das indizierte Array-Element stellt die Datenbank dar, in der der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-118">The indexed array element represents the database in which the error was encountered.</span></span> <span data-ttu-id="fc7eb-119">Wenn die Funktion keinen Fehlerwert zurückgibt, ist dieser Parameterwert ungültig.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-119">If the function does not return an error value, this parameter value is invalid.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="fc7eb-120">ulFlags</span><span class="sxs-lookup"><span data-stu-id="fc7eb-120">ulFlags</span></span> 
  
<span data-ttu-id="fc7eb-121">Optionaler Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-121">Optional input parameter.</span></span> <span data-ttu-id="fc7eb-122">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-122">This value is reserved for future use.</span></span> <span data-ttu-id="fc7eb-123">Der übergebene Wert sollte 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-123">The value passed should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc7eb-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc7eb-124">Return value</span></span>

<span data-ttu-id="fc7eb-125">Diese Funktion gibt einen Fehlercode aus der [CChkSGFiles. err-Aufzählung](cchksgfiles-err-enumeration.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-125">This function returns an error code from the [CChkSGFiles.ERR enumeration](cchksgfiles-err-enumeration.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fc7eb-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc7eb-126">Remarks</span></span>

<span data-ttu-id="fc7eb-127">**ErrCheckDbHeaders** überprüft, ob alle mit **ErrInit** registrierten Datenbanken dieselbe Protokollsignatur und Datenbankseitengröße aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-127">**ErrCheckDbHeaders** verifies that all databases registered with **ErrInit** have the same log signature and database page size.</span></span> <span data-ttu-id="fc7eb-128">Sie können auch den niedrigsten **genMin** -Parameterwert und den höchsten Wert für den **genMax** -Parameter verwenden, um den Protokoll Dateiensatz zu ermitteln, die erforderlich sind, um alle registrierten Datenbanken in den Zustand "Clean Shutdown" zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-128">You can also use the lowest **genMin** parameter value and the highest **genMax** parameter value to determine the set of log files that are necessary to bring all of the registered databases to a clean-shutdown state.</span></span> 
  
<span data-ttu-id="fc7eb-129">Der **piDbErrorEncountered** -Parameter wird nur festgelegt, wenn ein Fehler erkannt wird, wie durch einen **ErrCheckDbHeaders** -Rückgabewert ungleich NULL angegeben.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-129">The **piDbErrorEncountered** parameter is set only when an error is detected, as indicated by a non-zero **ErrCheckDbHeaders** return value.</span></span> 
  
<span data-ttu-id="fc7eb-130">Wenn in dieser Funktion ein Fehler auftritt, wird dem Windows-Fehlerereignisprotokoll ein Error-Ereignis hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-130">When an error occurs in this function, an error event will be added to the Windows Error event log.</span></span>
  
<span data-ttu-id="fc7eb-131">Sie können **ErrCheckDbHeaders** nur aufrufen, nachdem Sie **ErrInit**aufgerufen haben, und Sie müssen ihn aufrufen, bevor Sie **ErrCheckDbPages** und **ErrCheckLogs**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-131">You can call **ErrCheckDbHeaders** only after calling **ErrInit**, and you must call it before calling **ErrCheckDbPages** and **ErrCheckLogs**.</span></span>
  
<span data-ttu-id="fc7eb-132">Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **ErrCheckDbHeaders** -Funktion im Einzelthread-Teil aufrufen, und Sie können Sie für jedes **CCheckSGFiles** -Objekt nur einmal aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-132">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrCheckDbHeaders** function in the single-threaded portion, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="fc7eb-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc7eb-133">Requirements</span></span>

<span data-ttu-id="fc7eb-134">Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-134">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="fc7eb-135">Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="fc7eb-135">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

