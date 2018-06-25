---
title: CChkSGFiles.PgnoFromFileOffset-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PgnoFromFileOffset
api_type:
- dllExport
ms.assetid: 3d69ca6d-5ed1-4038-859e-106e776eeec1
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: d42ba7c8178c6fccdddec0b5da88a972f51184c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756811"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a><span data-ttu-id="c833b-103">CChkSGFiles.PgnoFromFileOffset-Funktion</span><span class="sxs-lookup"><span data-stu-id="c833b-103">CChkSGFiles.PgnoFromFileOffset function</span></span>

<span data-ttu-id="c833b-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="c833b-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="c833b-105">Gibt die Anzahl der logischen Datenbank-Seite, die entspricht dem Index angegebene Bytearray in der physischen Datenbankdatei zurück.</span><span class="sxs-lookup"><span data-stu-id="c833b-105">Returns the logical database page number that corresponds to the specified byte index in the physical database file.</span></span> <span data-ttu-id="c833b-106">Wenn der Dateioffset ungültig ist oder für die Datenbanken nicht die **ErrCheckDbHeaders** -Funktion aufgerufen wurde, gibt diese Funktion 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c833b-106">If the file offset is invalid, or if the **ErrCheckDbHeaders** function has not been called for the databases, this function returns 0 (zero).</span></span> 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a><span data-ttu-id="c833b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c833b-107">Parameters</span></span>

### <a name="ibfileoffset"></a><span data-ttu-id="c833b-108">ibFileOffset</span><span class="sxs-lookup"><span data-stu-id="c833b-108">ibFileOffset</span></span>
  
<span data-ttu-id="c833b-109">Input-Parameter.</span><span class="sxs-lookup"><span data-stu-id="c833b-109">Input parameter.</span></span> <span data-ttu-id="c833b-110">Der Abstand in eine Datenbankdatei in Byte.</span><span class="sxs-lookup"><span data-stu-id="c833b-110">The offset into a database file, in bytes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c833b-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c833b-111">Return value</span></span>

<span data-ttu-id="c833b-112">Die Datenbankdatei logische Seitenzahl, die den angegebenen Offset enthält.</span><span class="sxs-lookup"><span data-stu-id="c833b-112">The database file's logical page number that includes the specified offset.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c833b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c833b-113">Remarks</span></span>

<span data-ttu-id="c833b-114">Wenn der Parameter **IbFileOffset** ungültig ist, gibt die Funktion **PgnoFromFileOffset** 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c833b-114">If the **ibFileOffset** parameter is invalid, the **PgnoFromFileOffset** function returns 0 (zero).</span></span> 
  
<span data-ttu-id="c833b-115">**PgnoFromFileOffset** gibt auch 0 (null) zurück, wenn Sie nicht die **ErrCheckDbHeaders** -Funktion in der **CCheckSGFiles** -Instanz aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c833b-115">**PgnoFromFileOffset** also returns 0 (zero) if you haven't called the **ErrCheckDbHeaders** function on the **CCheckSGFiles** instance.</span></span> <span data-ttu-id="c833b-116">Sie müssen **ErrCheckDbHeaders** , um die Seitengröße der Datenbank und die Anzahl der reservierten Seiten für Datenbank-Kopfzeilen initialisieren aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c833b-116">You must call **ErrCheckDbHeaders** to initialize the database page size and number of pages allocated to database headers.</span></span> 
  
<span data-ttu-id="c833b-117">Verwenden Sie **PgnoFromFileOffset** zum Füllen der **Seite\_INFO** Elemente im Rahmen der Vorbereitung für den Aufruf von **ErrCheckDbPages**-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c833b-117">You should use **PgnoFromFileOffset** to fill in the **PAGE\_INFO** structure elements in preparation for calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="c833b-118">Der Parameter **RgPageInfo** **ErrCheckDbPages** erfordert, dass jedes Element im Array eine **PAGE_INFO** -Struktur mit den **UlPgno** Memberwerte korrekt initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c833b-118">The **rgPageInfo** parameter to **ErrCheckDbPages** requires that each element in the array be a **PAGE_INFO** structure, with the **ulPgno** member values correctly initialized.</span></span> 
  
<span data-ttu-id="c833b-119">Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, können Sie die **PgnoFromFileOffset** -Funktion im Multithread-Teil der Anwendung anrufen.</span><span class="sxs-lookup"><span data-stu-id="c833b-119">If you're using CHKSGFILES in a multithreaded application, you can call the **PgnoFromFileOffset** function in the multithreaded portion of the application.</span></span> <span data-ttu-id="c833b-120">Beachten Sie, dass Sie in der Regel diese Funktion mehrere Male für jede Datenbank, die zu überprüfenden aufgerufen würde.</span><span class="sxs-lookup"><span data-stu-id="c833b-120">Note that you would typically call this function multiple times for each database being checked.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="c833b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c833b-121">Requirements</span></span>

<span data-ttu-id="c833b-122">Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="c833b-122">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="c833b-123">Das Konto, unter die Anwendung ausgeführt wird, muss auf die Datenbank- und Protokolldateien Dateien gelesen haben, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c833b-123">The account that the application is running under must have read permission to the database and log files that are to be checked.</span></span>
  

