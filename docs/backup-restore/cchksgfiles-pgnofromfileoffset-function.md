---
title: CChkSGFiles. PgnoFromFileOffset-Funktion
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
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: 3c8f749a03b4aa251bf9312eba5d7e2d46c91fae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452895"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a><span data-ttu-id="c0737-103">CChkSGFiles. PgnoFromFileOffset-Funktion</span><span class="sxs-lookup"><span data-stu-id="c0737-103">CChkSGFiles.PgnoFromFileOffset function</span></span>

<span data-ttu-id="c0737-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0737-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="c0737-105">Gibt die Seitenzahl der logischen Datenbank zurück, die dem angegebenen Byte Index in der physischen Datenbankdatei entspricht.</span><span class="sxs-lookup"><span data-stu-id="c0737-105">Returns the logical database page number that corresponds to the specified byte index in the physical database file.</span></span> <span data-ttu-id="c0737-106">Wenn der Dateioffset ungültig ist oder die **ErrCheckDbHeaders** -Funktion nicht für die Datenbanken aufgerufen wurde, gibt diese Funktion 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c0737-106">If the file offset is invalid, or if the **ErrCheckDbHeaders** function has not been called for the databases, this function returns 0 (zero).</span></span> 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a><span data-ttu-id="c0737-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0737-107">Parameters</span></span>

### <a name="ibfileoffset"></a><span data-ttu-id="c0737-108">ibFileOffset</span><span class="sxs-lookup"><span data-stu-id="c0737-108">ibFileOffset</span></span>
  
<span data-ttu-id="c0737-109">Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="c0737-109">Input parameter.</span></span> <span data-ttu-id="c0737-110">Der Offset in einer Datenbankdatei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c0737-110">The offset into a database file, in bytes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0737-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0737-111">Return value</span></span>

<span data-ttu-id="c0737-112">Die logische Seitenzahl der Datenbankdatei, die den angegebenen Offset enthält.</span><span class="sxs-lookup"><span data-stu-id="c0737-112">The database file's logical page number that includes the specified offset.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0737-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0737-113">Remarks</span></span>

<span data-ttu-id="c0737-114">Wenn der **ibFileOffset** -Parameter ungültig ist, gibt die **PgnoFromFileOffset** -Funktion 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c0737-114">If the **ibFileOffset** parameter is invalid, the **PgnoFromFileOffset** function returns 0 (zero).</span></span> 
  
<span data-ttu-id="c0737-115">**PgnoFromFileOffset** gibt auch 0 (null) zurück, wenn Sie die **ErrCheckDbHeaders** -Funktion nicht für die **CCheckSGFiles** -Instanz aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="c0737-115">**PgnoFromFileOffset** also returns 0 (zero) if you haven't called the **ErrCheckDbHeaders** function on the **CCheckSGFiles** instance.</span></span> <span data-ttu-id="c0737-116">Sie müssen **ErrCheckDbHeaders** aufrufen, um die Datenbankseitengröße und die Anzahl der Seiten zu initialisieren, die den Daten Bank Headern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c0737-116">You must call **ErrCheckDbHeaders** to initialize the database page size and number of pages allocated to database headers.</span></span> 
  
<span data-ttu-id="c0737-117">Sie sollten **PgnoFromFileOffset** verwenden, um die **Seiten \_ Info** Strukturelemente in Vorbereitung auf das Aufrufen von **ErrCheckDbPages**auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="c0737-117">You should use **PgnoFromFileOffset** to fill in the **PAGE\_INFO** structure elements in preparation for calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="c0737-118">Der **rgPageInfo** -Parameter für **ErrCheckDbPages** erfordert, dass jedes Element im Array eine **PAGE_INFO** Struktur ist, wobei die **ulPgno** -Elementwerte ordnungsgemäß initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c0737-118">The **rgPageInfo** parameter to **ErrCheckDbPages** requires that each element in the array be a **PAGE_INFO** structure, with the **ulPgno** member values correctly initialized.</span></span> 
  
<span data-ttu-id="c0737-119">Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, können Sie die **PgnoFromFileOffset** -Funktion im Multithread-Teil der Anwendung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c0737-119">If you're using CHKSGFILES in a multithreaded application, you can call the **PgnoFromFileOffset** function in the multithreaded portion of the application.</span></span> <span data-ttu-id="c0737-120">Beachten Sie, dass Sie diese Funktion in der Regel für jede geprüfte Datenbank mehrmals aufrufen würden.</span><span class="sxs-lookup"><span data-stu-id="c0737-120">Note that you would typically call this function multiple times for each database being checked.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="c0737-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0737-121">Requirements</span></span>

<span data-ttu-id="c0737-122">Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="c0737-122">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="c0737-123">Das Konto, unter dem die Anwendung läuft, muss über Leseberechtigung für die zu überprüfende Datenbank-und Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="c0737-123">The account that the application is running under must have read permission to the database and log files that are to be checked.</span></span>
  

