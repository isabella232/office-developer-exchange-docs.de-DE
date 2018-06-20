---
title: CChkSGFiles.ErrInit-Funktion
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
description: 'Zuletzt geändert: 03 März 2013'
ms.openlocfilehash: d4b76933a747fe4bf084061cf080bc68264132ed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756802"
---
# <a name="cchksgfileserrinit-function"></a><span data-ttu-id="30f36-103">CChkSGFiles.ErrInit-Funktion</span><span class="sxs-lookup"><span data-stu-id="30f36-103">CChkSGFiles.ErrInit function</span></span>
  
<span data-ttu-id="30f36-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="30f36-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="30f36-105">Initialisiert das **CChkSGFiles** -Objekt durch Angeben der Datenbanken überprüft werden soll und den Pfad und den Basisnamen des die Transaktionsprotokolldateien überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="30f36-105">Initializes the **CChkSGFiles** object by specifying the databases to be checked and the path and base name of the transaction log files to be checked.</span></span> <span data-ttu-id="30f36-106">Anwendungen sollte diese Funktion aufrufen, unmittelbar nach der erfolgreichen Aufruf der Funktion **neu** .</span><span class="sxs-lookup"><span data-stu-id="30f36-106">Applications should call this function immediately after successfully calling the **New** function.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="30f36-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="30f36-107">Parameters</span></span>

### <a name="rgwszdb"></a><span data-ttu-id="30f36-108">RgwszDb]</span><span class="sxs-lookup"><span data-stu-id="30f36-108">rgwszDb[]</span></span>
  
<span data-ttu-id="30f36-109">Input-Parameter.</span><span class="sxs-lookup"><span data-stu-id="30f36-109">Input parameter.</span></span> <span data-ttu-id="30f36-110">Ein Array, der angibt, die Datenbanken überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="30f36-110">An array that specifies the databases to be checked.</span></span> <span data-ttu-id="30f36-111">Jedes Arrayelement ist eine Null terminierte Unicode-Zeichenfolge, die den Pfad und den Namen einer Datenbank überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="30f36-111">Each array element is a null-terminated Unicode string that contains the path and file name of a database to be checked.</span></span>
    
### <a name="cdb"></a><span data-ttu-id="30f36-112">cDB</span><span class="sxs-lookup"><span data-stu-id="30f36-112">cDB</span></span>
  
<span data-ttu-id="30f36-113">Input-Parameter.</span><span class="sxs-lookup"><span data-stu-id="30f36-113">Input parameter.</span></span> <span data-ttu-id="30f36-114">Die Anzahl der gültige Datenbank Pfad Elementen im Array **RgwszDb** .</span><span class="sxs-lookup"><span data-stu-id="30f36-114">The number of valid database path elements in the **rgwszDb** array.</span></span> 
    
#### <a name="wszlogpath"></a><span data-ttu-id="30f36-115">wszLogPath</span><span class="sxs-lookup"><span data-stu-id="30f36-115">wszLogPath</span></span>
  
<span data-ttu-id="30f36-116">Input-Parameter.</span><span class="sxs-lookup"><span data-stu-id="30f36-116">Input parameter.</span></span> <span data-ttu-id="30f36-117">Der vollständige Pfad der die Transaktionsprotokolldateien in Form einer Null terminierte Unicode-Zeichenfolge überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="30f36-117">The full path of the transaction log files to be checked, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="wszbasename"></a><span data-ttu-id="30f36-118">wszBaseName</span><span class="sxs-lookup"><span data-stu-id="30f36-118">wszBaseName</span></span>
  
<span data-ttu-id="30f36-119">Input-Parameter.</span><span class="sxs-lookup"><span data-stu-id="30f36-119">Input parameter.</span></span> <span data-ttu-id="30f36-120">Die drei Buchstaben Basisnamen der Transaktionsprotokolldateien in Form einer Null terminierte Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="30f36-120">The three-letter base name of the Exchange transaction log files, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="ulflags"></a><span data-ttu-id="30f36-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="30f36-121">ulFlags</span></span>
  
<span data-ttu-id="30f36-122">Optionale Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="30f36-122">Optional input parameter.</span></span> <span data-ttu-id="30f36-123">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="30f36-123">This value is reserved for future use.</span></span> <span data-ttu-id="30f36-124">Der durch diesen Parameter übergebene Wert muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="30f36-124">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="30f36-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="30f36-125">Return value</span></span>

<span data-ttu-id="30f36-126">Ein Fehlercode aus der [ERR](cchksgfiles-err-enumeration.md) -Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="30f36-126">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="30f36-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="30f36-127">Remarks</span></span>

<span data-ttu-id="30f36-128">Die Funktion **ErrInit** registriert die Datenbanken und Protokolldateien, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30f36-128">The **ErrInit** function registers the databases and log files that are to be checked.</span></span> <span data-ttu-id="30f36-129">Diese Funktion muss aufgerufen werden, nachdem die **New** -Funktion wird aufgerufen, jedoch bevor andere **ChkSGFiles** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="30f36-129">This function must be called after the **New** function is called but before any other **ChkSGFiles** function is called.</span></span> 
  
<span data-ttu-id="30f36-130">Sie müssen den Datenbanknamen und Pfad der Protokolldatei den Basisnamen als Null endende Unicode-Zeichenfolgen angeben.</span><span class="sxs-lookup"><span data-stu-id="30f36-130">You must provide all the database names, the log file path, and the base name as null-terminated Unicode strings.</span></span>
  
<span data-ttu-id="30f36-131">Sie können nur die Datenbankdateien überprüfen nur die Protokolldateien oder die Datenbank- und Protokolldateien Dateien.</span><span class="sxs-lookup"><span data-stu-id="30f36-131">You can check only the database files, only the log files, or both the database and log files.</span></span> <span data-ttu-id="30f36-132">Jedoch muss beim Aufruf von dieser Funktion die Anwendung mindestens eine Entität zu überprüfenden angeben.</span><span class="sxs-lookup"><span data-stu-id="30f36-132">However, when calling this function, the application must specify at least one entity to be checked.</span></span> <span data-ttu-id="30f36-133">Übergeben von 0 (null) für **cDB** und NULL für **WszLogPath** gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="30f36-133">Passing 0 (zero) for  **cDB**  and NULL for  **wszLogPath**  will return an error.</span></span> 
  
<span data-ttu-id="30f36-134">Wenn der Wert der **cDB** als 0 (null) ist, führt zu einem Fehler NULL für **RgwszDb** übergeben.</span><span class="sxs-lookup"><span data-stu-id="30f36-134">If the value of  **cDB**  is other than 0 (zero), passing NULL for  **rgwszDb**  will result in an error.</span></span> <span data-ttu-id="30f36-135">Um die Datenbankdateien zu überprüfen, muss die Anwendung die Datenbanknamen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="30f36-135">To check the database files, the application must provide the database names.</span></span> 
  
<span data-ttu-id="30f36-136">Wenn Sie NULL für **WszBaseName** übergeben wird, aber **WszLogPath** ist nicht NULL, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30f36-136">If NULL is passed for  **wszBaseName**  but  **wszLogPath**  is not NULL, an error will be returned.</span></span> <span data-ttu-id="30f36-137">Eine Protokolldatei-Basisname ist immer erforderlich, beim Überprüfen der Protokolldateien.</span><span class="sxs-lookup"><span data-stu-id="30f36-137">A log file base name is always required when checking log files.</span></span> 
  
<span data-ttu-id="30f36-138">Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, müssen Sie die **ErrInit** -Funktion in den einzelnen Thread Teil der Anwendung aufrufen und können Sie nur einmal für jede **CCheckSGFiles** -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="30f36-138">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrInit** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="30f36-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30f36-139">Requirements</span></span>

<span data-ttu-id="30f36-140">Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="30f36-140">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="30f36-141">Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30f36-141">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

