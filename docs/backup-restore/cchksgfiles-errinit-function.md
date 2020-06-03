---
title: CChkSGFiles. ErrInit-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrInit
api_type:
- dllExport
ms.assetid: 61bb3af1-8b51-4bae-8e25-90a4dc1226c5
description: 'Letzte Änderung: März 03, 2013'
ms.openlocfilehash: c881691e7c1ba83a396e659f6aac0328625e49a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457011"
---
# <a name="cchksgfileserrinit-function"></a><span data-ttu-id="7308f-103">CChkSGFiles. ErrInit-Funktion</span><span class="sxs-lookup"><span data-stu-id="7308f-103">CChkSGFiles.ErrInit function</span></span>
  
<span data-ttu-id="7308f-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="7308f-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="7308f-105">Initialisiert das **CChkSGFiles** -Objekt, indem die zu überprüfenden Datenbanken und der Pfad und der Basis Name der zu überprüfenden Transaktionsprotokolldateien angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7308f-105">Initializes the **CChkSGFiles** object by specifying the databases to be checked and the path and base name of the transaction log files to be checked.</span></span> <span data-ttu-id="7308f-106">Anwendungen sollten diese Funktion sofort aufrufen, nachdem die **neue** Funktion erfolgreich aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7308f-106">Applications should call this function immediately after successfully calling the **New** function.</span></span> 
  
```cs
Vitual ERRErrInit  
(
    Const WCHAR  * const rgwszDb[],
    Const ULONGcDB,
    __in_z const WCHAR  * const wszLogPath,
    __in_z const WCHAR  * const wszBaseName,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="7308f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7308f-107">Parameters</span></span>

### <a name="rgwszdb"></a><span data-ttu-id="7308f-108">rgwszDb[]</span><span class="sxs-lookup"><span data-stu-id="7308f-108">rgwszDb[]</span></span>
  
<span data-ttu-id="7308f-109">Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="7308f-109">Input parameter.</span></span> <span data-ttu-id="7308f-110">Ein Array, das angibt, welche Datenbanken überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7308f-110">An array that specifies the databases to be checked.</span></span> <span data-ttu-id="7308f-111">Jedes Array-Element ist eine mit NULL endende Unicode-Zeichenfolge, die den Pfad und den Dateinamen einer Datenbank enthält, die überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="7308f-111">Each array element is a null-terminated Unicode string that contains the path and file name of a database to be checked.</span></span>
    
### <a name="cdb"></a><span data-ttu-id="7308f-112">cDB</span><span class="sxs-lookup"><span data-stu-id="7308f-112">cDB</span></span>
  
<span data-ttu-id="7308f-113">Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="7308f-113">Input parameter.</span></span> <span data-ttu-id="7308f-114">Die Anzahl gültiger Datenbankpfad Elemente im **rgwszDb** -Array.</span><span class="sxs-lookup"><span data-stu-id="7308f-114">The number of valid database path elements in the **rgwszDb** array.</span></span> 
    
#### <a name="wszlogpath"></a><span data-ttu-id="7308f-115">wszLogPath</span><span class="sxs-lookup"><span data-stu-id="7308f-115">wszLogPath</span></span>
  
<span data-ttu-id="7308f-116">Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="7308f-116">Input parameter.</span></span> <span data-ttu-id="7308f-117">Der vollständige Pfad der zu überprüfenden Transaktionsprotokolldateien in Form einer null-terminierten Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7308f-117">The full path of the transaction log files to be checked, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="wszbasename"></a><span data-ttu-id="7308f-118">wszBaseName</span><span class="sxs-lookup"><span data-stu-id="7308f-118">wszBaseName</span></span>
  
<span data-ttu-id="7308f-119">Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="7308f-119">Input parameter.</span></span> <span data-ttu-id="7308f-120">Der dreistellige Basis Name der Exchange-Transaktionsprotokolldateien in Form einer null-terminierten Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7308f-120">The three-letter base name of the Exchange transaction log files, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="ulflags"></a><span data-ttu-id="7308f-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="7308f-121">ulFlags</span></span>
  
<span data-ttu-id="7308f-122">Optionaler Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="7308f-122">Optional input parameter.</span></span> <span data-ttu-id="7308f-123">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="7308f-123">This value is reserved for future use.</span></span> <span data-ttu-id="7308f-124">Der von diesem Parameter übergebene Wert sollte 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="7308f-124">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7308f-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7308f-125">Return value</span></span>

<span data-ttu-id="7308f-126">Ein Fehlercode aus der [Err](cchksgfiles-err-enumeration.md) -Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="7308f-126">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7308f-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7308f-127">Remarks</span></span>

<span data-ttu-id="7308f-128">Die **ErrInit** -Funktion registriert die Datenbanken und Protokolldateien, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7308f-128">The **ErrInit** function registers the databases and log files that are to be checked.</span></span> <span data-ttu-id="7308f-129">Diese Funktion muss aufgerufen werden, nachdem die **neue** Funktion aufgerufen wurde, aber bevor eine andere **ChkSGFiles** -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7308f-129">This function must be called after the **New** function is called but before any other **ChkSGFiles** function is called.</span></span> 
  
<span data-ttu-id="7308f-130">Sie müssen alle Datenbanknamen, den Protokolldateipfad und den Basisnamen als NULL-terminierte Unicode-Zeichenfolgen angeben.</span><span class="sxs-lookup"><span data-stu-id="7308f-130">You must provide all the database names, the log file path, and the base name as null-terminated Unicode strings.</span></span>
  
<span data-ttu-id="7308f-131">Sie können nur die Datenbankdateien, nur die Protokolldateien oder sowohl die Datenbank-als auch die Protokolldateien überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7308f-131">You can check only the database files, only the log files, or both the database and log files.</span></span> <span data-ttu-id="7308f-132">Wenn diese Funktion aufgerufen wird, muss die Anwendung jedoch mindestens eine Entität angeben, die überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="7308f-132">However, when calling this function, the application must specify at least one entity to be checked.</span></span> <span data-ttu-id="7308f-133">Durch die Übergabe von 0 (null) für **cDB** und NULL für **wszLogPath** wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7308f-133">Passing 0 (zero) for  **cDB**  and NULL for  **wszLogPath**  will return an error.</span></span> 
  
<span data-ttu-id="7308f-134">Wenn der Wert von **cDB** nicht 0 (null) ist, führt die Übergabe von NULL für **rgwszDb** zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="7308f-134">If the value of  **cDB**  is other than 0 (zero), passing NULL for  **rgwszDb**  will result in an error.</span></span> <span data-ttu-id="7308f-135">Um die Datenbankdateien zu überprüfen, muss die Anwendung die Datenbanknamen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7308f-135">To check the database files, the application must provide the database names.</span></span> 
  
<span data-ttu-id="7308f-136">Wenn NULL für **wszBaseName** übergeben wird, **wszLogPath** jedoch nicht NULL ist, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7308f-136">If NULL is passed for  **wszBaseName**  but  **wszLogPath**  is not NULL, an error will be returned.</span></span> <span data-ttu-id="7308f-137">Bei der Überprüfung von Protokolldateien ist immer ein Protokolldatei-Basis Name erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7308f-137">A log file base name is always required when checking log files.</span></span> 
  
<span data-ttu-id="7308f-138">Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **ErrInit** -Funktion im Single-Thread-Teil der Anwendung aufrufen, und Sie können Sie nur einmal für jedes **CCheckSGFiles** -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7308f-138">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrInit** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="7308f-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7308f-139">Requirements</span></span>

<span data-ttu-id="7308f-140">Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="7308f-140">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="7308f-141">Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="7308f-141">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

