---
title: CChkSGFiles.ERR-Aufzählung
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ERR
api_type:
- dllExport
ms.assetid: f0efe195-91c3-4f3a-8c7d-e5dba336465a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 20f10c43e3b92604bb51e1aa5f896a8bd7c4b335
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757749"
---
# <a name="cchksgfileserr-enumeration"></a><span data-ttu-id="5626e-103">CChkSGFiles.ERR-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="5626e-103">CChkSGFiles.ERR enumeration</span></span> 
  
<span data-ttu-id="5626e-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="5626e-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="5626e-105">Gibt die Ergebnisse der aufgerufenen Funktion an.</span><span class="sxs-lookup"><span data-stu-id="5626e-105">Indicates the results of the called function.</span></span> <span data-ttu-id="5626e-106">Diese Aufzählung wird von viele Funktionen der **CCheckSGFiles** -Klasse zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5626e-106">This enumeration is returned by many functions of the **CCheckSGFiles** class.</span></span> 
  
```cs
Enum ERR  
{
        errSuccess = 0,
        errTaskDropped = -106,
        errRequiredLogFilesMissing = -543,
        errInvalidParameter = -1003,
        errOutOfMemory = -1011,
        errReadVerifyFailure = -1018,
        errTooManyActiveUsers = -1059,
        errDatabaseCorrupted = -1206
}

```

## <a name="values"></a><span data-ttu-id="5626e-107">Werte</span><span class="sxs-lookup"><span data-stu-id="5626e-107">Values</span></span>

|<span data-ttu-id="5626e-108">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="5626e-108">**Member name**</span></span>|<span data-ttu-id="5626e-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5626e-109">**Value**</span></span>|<span data-ttu-id="5626e-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5626e-110">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5626e-111">errSuccess</span><span class="sxs-lookup"><span data-stu-id="5626e-111">errSuccess</span></span>  <br/> |<span data-ttu-id="5626e-112">0</span><span class="sxs-lookup"><span data-stu-id="5626e-112">0</span></span>  <br/> |<span data-ttu-id="5626e-113">Die Funktion ohne Fehler abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5626e-113">The function completed without any errors.</span></span>  <br/> |
|<span data-ttu-id="5626e-114">errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="5626e-114">errTaskDropped</span></span>  <br/> |<span data-ttu-id="5626e-115">-106</span><span class="sxs-lookup"><span data-stu-id="5626e-115">-106</span></span>  <br/> |<span data-ttu-id="5626e-116">Wird von der Funktion **ErrTerm** , um anzugeben, dass nicht alle Datenbankseiten und Transaktionsprotokolldateien nicht überprüft wurden oder bei der Überprüfung Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="5626e-116">Returned by the **ErrTerm** function to indicate that not all database pages and transaction log files were checked, or that errors were encountered during the verification.</span></span>  <br/> |
|<span data-ttu-id="5626e-117">errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="5626e-117">errRequiredLogFilesMissing</span></span>  <br/> |<span data-ttu-id="5626e-118">-543</span><span class="sxs-lookup"><span data-stu-id="5626e-118">-543</span></span>  <br/> |<span data-ttu-id="5626e-119">Eine oder mehrere Protokolldateien, die erforderlich sind, um die Datenbank auf einen clean Shutdown-Status in der Pfad der Protokolldatei nicht gefunden oder verfügte nicht über den angegebenen drei Buchstaben Basisnamen.</span><span class="sxs-lookup"><span data-stu-id="5626e-119">One or more log files that are required to bring the database to a clean-shutdown state was not found in the log file path, or did not have the specified three-letter base name.</span></span>  <br/> |
|<span data-ttu-id="5626e-120">errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5626e-120">errInvalidParameter</span></span>  <br/> |<span data-ttu-id="5626e-121">-1003</span><span class="sxs-lookup"><span data-stu-id="5626e-121">-1003</span></span>  <br/> |<span data-ttu-id="5626e-122">Mindestens einen Parameter, die an die Funktion übergeben wurden war ungültig.</span><span class="sxs-lookup"><span data-stu-id="5626e-122">One or more parameters that were passed to the function were invalid.</span></span>  <br/> |
|<span data-ttu-id="5626e-123">errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="5626e-123">errOutOfMemory</span></span>  <br/> |<span data-ttu-id="5626e-124">-1011</span><span class="sxs-lookup"><span data-stu-id="5626e-124">-1011</span></span>  <br/> |<span data-ttu-id="5626e-125">Es wurde nicht genügend Arbeitsspeicher verfügbar, um den angeforderten Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="5626e-125">Insufficient memory was available to complete the requested operation.</span></span>  <br/> |
|<span data-ttu-id="5626e-126">errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="5626e-126">errReadVerifyFailure</span></span>  <br/> |<span data-ttu-id="5626e-127">-1018</span><span class="sxs-lookup"><span data-stu-id="5626e-127">-1018</span></span>  <br/> |<span data-ttu-id="5626e-128">Die Prüfsumme, die auf einer Datenbankseite gespeichert ist stimmt nicht mit der erwarteten Prüfsumme überein.</span><span class="sxs-lookup"><span data-stu-id="5626e-128">The checksum that is stored on a database page does not match its expected checksum.</span></span>  <br/> |
|<span data-ttu-id="5626e-129">errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="5626e-129">errTooManyActiveUsers</span></span>  <br/> |<span data-ttu-id="5626e-130">-1059</span><span class="sxs-lookup"><span data-stu-id="5626e-130">-1059</span></span>  <br/> |<span data-ttu-id="5626e-131">Die Funktion **ErrTerm** wurde aufgerufen, während das Objekt wurde noch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5626e-131">The **ErrTerm** function was called while the object was still being used.</span></span> <span data-ttu-id="5626e-132">Dies kann vorkommen, wenn **ErrTerm** , bevor **ErrCheckDbPages aufgerufen wird** oder **ErrCheckLogFiles** zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="5626e-132">This can occur if **ErrTerm** is called before **ErrCheckDbPages** or **ErrCheckLogFiles** has returned.</span></span>  <br/> |
   
## <a name="requirements"></a><span data-ttu-id="5626e-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5626e-133">Requirements</span></span>

<span data-ttu-id="5626e-134">Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="5626e-134">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="5626e-135">Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5626e-135">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

