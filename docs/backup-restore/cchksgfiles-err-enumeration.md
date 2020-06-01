---
title: CChkSGFiles. err-Aufzählung
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dbc76601a808f79ce3ed5b5dc9fbe4cf92efb015
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455254"
---
# <a name="cchksgfileserr-enumeration"></a><span data-ttu-id="1968c-103">CChkSGFiles. err-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="1968c-103">CChkSGFiles.ERR enumeration</span></span> 
  
<span data-ttu-id="1968c-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="1968c-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="1968c-105">Gibt die Ergebnisse der aufgerufenen Funktion an.</span><span class="sxs-lookup"><span data-stu-id="1968c-105">Indicates the results of the called function.</span></span> <span data-ttu-id="1968c-106">Diese Aufzählung wird von vielen Funktionen der **CCheckSGFiles** -Klasse zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1968c-106">This enumeration is returned by many functions of the **CCheckSGFiles** class.</span></span> 
  
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

## <a name="values"></a><span data-ttu-id="1968c-107">Werte</span><span class="sxs-lookup"><span data-stu-id="1968c-107">Values</span></span>

|<span data-ttu-id="1968c-108">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="1968c-108">**Member name**</span></span>|<span data-ttu-id="1968c-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1968c-109">**Value**</span></span>|<span data-ttu-id="1968c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1968c-110">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1968c-111">errSuccess</span><span class="sxs-lookup"><span data-stu-id="1968c-111">errSuccess</span></span>  <br/> |<span data-ttu-id="1968c-112">0</span><span class="sxs-lookup"><span data-stu-id="1968c-112">0</span></span>  <br/> |<span data-ttu-id="1968c-113">Die Funktion wurde ohne Fehler abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1968c-113">The function completed without any errors.</span></span>  <br/> |
|<span data-ttu-id="1968c-114">errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="1968c-114">errTaskDropped</span></span>  <br/> |<span data-ttu-id="1968c-115">-106</span><span class="sxs-lookup"><span data-stu-id="1968c-115">-106</span></span>  <br/> |<span data-ttu-id="1968c-116">Wird von der **ErrTerm** -Funktion zurückgegeben, um anzugeben, dass nicht alle Datenbankseiten und Transaktionsprotokolldateien überprüft wurden oder dass während der Überprüfung Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="1968c-116">Returned by the **ErrTerm** function to indicate that not all database pages and transaction log files were checked, or that errors were encountered during the verification.</span></span>  <br/> |
|<span data-ttu-id="1968c-117">errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="1968c-117">errRequiredLogFilesMissing</span></span>  <br/> |<span data-ttu-id="1968c-118">-543</span><span class="sxs-lookup"><span data-stu-id="1968c-118">-543</span></span>  <br/> |<span data-ttu-id="1968c-119">Mindestens eine Protokolldatei, die erforderlich ist, um die Datenbank in den Zustand "Clean Shutdown" zu versetzen, wurde im Protokoll Dateipfad nicht gefunden oder hat nicht den angegebenen drei Buchstaben-Basisnamen.</span><span class="sxs-lookup"><span data-stu-id="1968c-119">One or more log files that are required to bring the database to a clean-shutdown state was not found in the log file path, or did not have the specified three-letter base name.</span></span>  <br/> |
|<span data-ttu-id="1968c-120">errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1968c-120">errInvalidParameter</span></span>  <br/> |<span data-ttu-id="1968c-121">-1003</span><span class="sxs-lookup"><span data-stu-id="1968c-121">-1003</span></span>  <br/> |<span data-ttu-id="1968c-122">Mindestens ein Parameter, der an die Funktion übergeben wurde, war ungültig.</span><span class="sxs-lookup"><span data-stu-id="1968c-122">One or more parameters that were passed to the function were invalid.</span></span>  <br/> |
|<span data-ttu-id="1968c-123">errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="1968c-123">errOutOfMemory</span></span>  <br/> |<span data-ttu-id="1968c-124">-1011</span><span class="sxs-lookup"><span data-stu-id="1968c-124">-1011</span></span>  <br/> |<span data-ttu-id="1968c-125">Zum Abschließen des angeforderten Vorgangs war nicht genügend Arbeitsspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1968c-125">Insufficient memory was available to complete the requested operation.</span></span>  <br/> |
|<span data-ttu-id="1968c-126">errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="1968c-126">errReadVerifyFailure</span></span>  <br/> |<span data-ttu-id="1968c-127">-1018</span><span class="sxs-lookup"><span data-stu-id="1968c-127">-1018</span></span>  <br/> |<span data-ttu-id="1968c-128">Die auf einer Datenbankseite gespeicherte Prüfsumme stimmt nicht mit der erwarteten Prüfsumme überein.</span><span class="sxs-lookup"><span data-stu-id="1968c-128">The checksum that is stored on a database page does not match its expected checksum.</span></span>  <br/> |
|<span data-ttu-id="1968c-129">errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="1968c-129">errTooManyActiveUsers</span></span>  <br/> |<span data-ttu-id="1968c-130">-1059</span><span class="sxs-lookup"><span data-stu-id="1968c-130">-1059</span></span>  <br/> |<span data-ttu-id="1968c-131">Die **ErrTerm** -Funktion wurde aufgerufen, während das Objekt noch verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1968c-131">The **ErrTerm** function was called while the object was still being used.</span></span> <span data-ttu-id="1968c-132">Dies kann auftreten, wenn **ErrTerm** aufgerufen wird, bevor **ErrCheckDbPages** oder **ErrCheckLogFiles** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1968c-132">This can occur if **ErrTerm** is called before **ErrCheckDbPages** or **ErrCheckLogFiles** has returned.</span></span>  <br/> |
   
## <a name="requirements"></a><span data-ttu-id="1968c-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1968c-133">Requirements</span></span>

<span data-ttu-id="1968c-134">Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="1968c-134">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="1968c-135">Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="1968c-135">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

