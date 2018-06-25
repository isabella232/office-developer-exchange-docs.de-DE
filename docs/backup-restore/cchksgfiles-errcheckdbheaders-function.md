---
title: CChkSGFiles.ErrCheckDbHeaders-Funktion
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
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: a407019063b34970e883a00ca4f4d730935d7cba
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756810"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a><span data-ttu-id="ae976-103">CChkSGFiles.ErrCheckDbHeaders-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae976-103">CChkSGFiles.ErrCheckDbHeaders function</span></span>

<span data-ttu-id="ae976-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae976-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span> 
  
<span data-ttu-id="ae976-105">Überprüft die Kopfzeilen der Datenbankdateien, die von der Funktion **ErrInit** angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="ae976-105">Validates the headers of the database files that were specified by the **ErrInit** function.</span></span> <span data-ttu-id="ae976-106">Diese Funktion gibt auch die Seitengröße und die Anzahl der Seiten in den einzelnen der angegebenen Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="ae976-106">This function also returns the page size and number of pages in each of the specified databases.</span></span> 
  
```cs
Vitual ERRErrCheckDbHeaders  
(
        ULONG  * const pcbDbPageSize,
        ULONG  * const pcHeaderPagesPerDb,
        ULONG   const piDbErrorEncountered,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="ae976-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae976-107">Parameters</span></span>

### <a name="pcbdbpagesize"></a><span data-ttu-id="ae976-108">pcbDbPageSize</span><span class="sxs-lookup"><span data-stu-id="ae976-108">pcbDbPageSize</span></span> 
  
<span data-ttu-id="ae976-109">Output-Parameter.</span><span class="sxs-lookup"><span data-stu-id="ae976-109">Output parameter.</span></span> <span data-ttu-id="ae976-110">Das Seitenformat der einzelnen angegebenen Datenbanken, in Byte.</span><span class="sxs-lookup"><span data-stu-id="ae976-110">The page size of each of the specified databases, in bytes.</span></span>
    
### <a name="pcheaderpagesperdb"></a><span data-ttu-id="ae976-111">pcHeaderPagesPerDb</span><span class="sxs-lookup"><span data-stu-id="ae976-111">pcHeaderPagesPerDb</span></span> 
  
<span data-ttu-id="ae976-112">Output-Parameter.</span><span class="sxs-lookup"><span data-stu-id="ae976-112">Output parameter.</span></span> <span data-ttu-id="ae976-113">Die Anzahl der Seiten am Anfang jeder angegebene Datenbank, die von der Datenbank-Engine für die interne Verwendung reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="ae976-113">The number of pages at the beginning of each specified database that are reserved by the database engine for internal use.</span></span> <span data-ttu-id="ae976-114">Beachten Sie, dass *nicht* Durchlauf Kopfzeilenseiten an die Funktion **ErrCheckDbPages** für die Validierung sollten.</span><span class="sxs-lookup"><span data-stu-id="ae976-114">Note that you should *not* pass header pages to the **ErrCheckDbPages** function for validation.</span></span> 
    
### <a name="pidberrorencountered"></a><span data-ttu-id="ae976-115">piDbErrorEncountered</span><span class="sxs-lookup"><span data-stu-id="ae976-115">piDbErrorEncountered</span></span>
  
<span data-ttu-id="ae976-116">Output-Parameter.</span><span class="sxs-lookup"><span data-stu-id="ae976-116">Output parameter.</span></span> <span data-ttu-id="ae976-117">Wenn der Rückgabewert der Funktion einen Fehler weist darauf hin, wird dieser Parameter als Farbindex in der **ErrInit** -Funktion übergebenen Arrays **RgwszDb []** .</span><span class="sxs-lookup"><span data-stu-id="ae976-117">If the return value of the function indicates an error, this parameter will be an index into the **rgwszDb[]** array passed to the **ErrInit** function.</span></span> <span data-ttu-id="ae976-118">Das indizierte Arrayelement steht für die Datenbank, in der der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ae976-118">The indexed array element represents the database in which the error was encountered.</span></span> <span data-ttu-id="ae976-119">Wenn die Funktion keinen Fehlerwert zurückgibt, ist dieser Parameterwert ungültig.</span><span class="sxs-lookup"><span data-stu-id="ae976-119">If the function does not return an error value, this parameter value is invalid.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="ae976-120">ulFlags</span><span class="sxs-lookup"><span data-stu-id="ae976-120">ulFlags</span></span> 
  
<span data-ttu-id="ae976-121">Optionale Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="ae976-121">Optional input parameter.</span></span> <span data-ttu-id="ae976-122">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ae976-122">This value is reserved for future use.</span></span> <span data-ttu-id="ae976-123">Der übergebene Wert muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="ae976-123">The value passed should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ae976-124">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ae976-124">Return value</span></span>

<span data-ttu-id="ae976-125">Diese Funktion gibt einen Fehlercode aus der [CChkSGFiles.ERR-Enumeration](cchksgfiles-err-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="ae976-125">This function returns an error code from the [CChkSGFiles.ERR enumeration](cchksgfiles-err-enumeration.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae976-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ae976-126">Remarks</span></span>

<span data-ttu-id="ae976-127">**ErrCheckDbHeaders** überprüft, ob alle Datenbanken, die mit **ErrInit** registriert die gleiche Signatur und Datenbank Seite Protokollgröße verfügen.</span><span class="sxs-lookup"><span data-stu-id="ae976-127">**ErrCheckDbHeaders** verifies that all databases registered with **ErrInit** have the same log signature and database page size.</span></span> <span data-ttu-id="ae976-128">Sie können auch der niedrigste Wert des Parameters **GenMin** und der höchste Wert des Parameters **GenMax** verwenden, um die Protokolldateien zu bestimmen, die erforderlich sind, um alle registrierten Datenbanken auf einen clean Shutdown-Status zu bringen.</span><span class="sxs-lookup"><span data-stu-id="ae976-128">You can also use the lowest **genMin** parameter value and the highest **genMax** parameter value to determine the set of log files that are necessary to bring all of the registered databases to a clean-shutdown state.</span></span> 
  
<span data-ttu-id="ae976-129">Der Parameter **PiDbErrorEncountered** festgelegt ist, nur, wenn ein Fehler erkannt wird, wie eine ungleich NULL angegeben **ErrCheckDbHeaders** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ae976-129">The **piDbErrorEncountered** parameter is set only when an error is detected, as indicated by a non-zero **ErrCheckDbHeaders** return value.</span></span> 
  
<span data-ttu-id="ae976-130">Tritt ein Fehler in dieser Funktion wird ein Error-Ereignis in das Ereignisprotokoll Windows Fehler hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ae976-130">When an error occurs in this function, an error event will be added to the Windows Error event log.</span></span>
  
<span data-ttu-id="ae976-131">Sie können nur nach der **ErrInit** **ErrCheckDbHeaders** anrufen, und Sie müssen vor dem Aufruf von **ErrCheckDbPages** und **ErrCheckLogs**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ae976-131">You can call **ErrCheckDbHeaders** only after calling **ErrInit**, and you must call it before calling **ErrCheckDbPages** and **ErrCheckLogs**.</span></span>
  
<span data-ttu-id="ae976-132">Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, müssen Sie die **ErrCheckDbHeaders** -Funktion in den einzelnen Thread Teil aufrufen und können Sie nur einmal für jede **CCheckSGFiles** -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ae976-132">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrCheckDbHeaders** function in the single-threaded portion, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="ae976-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae976-133">Requirements</span></span>

<span data-ttu-id="ae976-134">Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="ae976-134">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="ae976-135">Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ae976-135">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

