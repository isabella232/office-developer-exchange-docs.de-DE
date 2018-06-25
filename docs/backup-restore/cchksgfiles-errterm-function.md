---
title: CChkSGFiles.ErrTerm-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrTerm
api_type:
- dllExport
ms.assetid: eea20a55-4a2a-4209-ae79-dc1ee1cd631b
description: 'Zuletzt geändert: 25 Februar 2013'
ms.openlocfilehash: 099ec33663baa2414a0c28b90364523b6191c697
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756808"
---
# <a name="cchksgfileserrterm-function"></a><span data-ttu-id="a853e-103">CChkSGFiles.ErrTerm-Funktion</span><span class="sxs-lookup"><span data-stu-id="a853e-103">CChkSGFiles.ErrTerm function</span></span>
  
<span data-ttu-id="a853e-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="a853e-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="a853e-105">Bietet einen allgemeinen Status der Überprüfung Datenbank- und Protokolldateien, die angibt, ob die Datenbankseiten und Protokolle erfolgreich überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="a853e-105">Provides an overall status of the database and log verification, which indicates whether all the database pages and logs were successfully verified.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a853e-106">Speichergruppen sind nicht verfügbar in Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="a853e-106">Storage groups are not available in Exchange 2013.</span></span> <span data-ttu-id="a853e-107">Für die Abwärtskompatibilität mit Datenbanken und Speichergruppen in Exchange-Versionen vor Exchange Server 2010 können mit der API für CHKSGFILES Speichergruppen angeben.</span><span class="sxs-lookup"><span data-stu-id="a853e-107">For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange Server 2010, the CHKSGFILES API enables you to specify storage groups.</span></span> <span data-ttu-id="a853e-108">Wenn Sie für CHKSGFILES in Exchange 2013-Datenbanken ausführen, sollten Sie Parameter festlegen, die einen Gruppenbezeichner Speicher auf eine leere Zeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="a853e-108">When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string.</span></span> 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="a853e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a853e-109">Parameters</span></span>

### <a name="ulflags"></a><span data-ttu-id="a853e-110">ulFlags</span><span class="sxs-lookup"><span data-stu-id="a853e-110">ulFlags</span></span>
  
<span data-ttu-id="a853e-111">Optionale Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="a853e-111">Optional input parameter.</span></span> <span data-ttu-id="a853e-112">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="a853e-112">This value is reserved for future use.</span></span> <span data-ttu-id="a853e-113">Der durch diesen Parameter übergebene Wert muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="a853e-113">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a853e-114">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a853e-114">Return value</span></span>

<span data-ttu-id="a853e-115">Ein Fehlercode aus der [ERR](cchksgfiles-err-enumeration.md) -Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="a853e-115">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a853e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a853e-116">Remarks</span></span>

<span data-ttu-id="a853e-117">Das Objekt **CChkSGFiles** bestimmt, ob alle Datenbanken, die mit der Funktion **ErrInit** registriert tatsächlich aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="a853e-117">The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="a853e-118">Dieses Objekt verwendet der **ErrCheckDbPages** -Funktion zu überprüfen, ob die gleiche Anzahl von Datenbank, die Seiten von der Funktion **ErrCheckDbHeaders** identifizierten tatsächlich überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="a853e-118">This object uses the **ErrCheckDbPages** function to verify that the same number of database pages identified by the **ErrCheckDbHeaders** function were actually verified.</span></span> <span data-ttu-id="a853e-119">Wenn die richtige Anzahl von Seiten in jeder Datenbank nicht erfolgreich aktiviert sind, gibt die **ErrTerm** -Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a853e-119">If the correct number of pages in each database are not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="a853e-120">Wenn die Anzahl von Datenbankseiten mit **ErrCheckDbPages** überprüft kleiner als der mit **ErrCheckDbHeaders**angegeben ist, diese Funktion erstellt einen Fehler im Windows-Ereignisprotokoll und **ErrTerm** gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a853e-120">If the number of database pages checked with **ErrCheckDbPages** is less than that indicated by **ErrCheckDbHeaders**, this function creates an error in the Windows Event log, and **ErrTerm** returns an error.</span></span> 
  
<span data-ttu-id="a853e-121">Wenn die Anzahl von Datenbankseiten überprüft mit **ErrCheckDbPages** größer als der mit **ErrCheckDbHeaders**angegeben ist, erstellt diese Funktion eine Warnung in der Windows-Ereignisprotokoll, um anzugeben, dass die Anwendung unnötig einige überprüft werden mehr als einmal Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="a853e-121">If the number of database pages checked with **ErrCheckDbPages** is greater than that indicated by **ErrCheckDbHeaders**, this function creates a warning in the Windows Event log to indicate that the application might be unnecessarily checking some database pages more than once.</span></span> <span data-ttu-id="a853e-122">In diesem Fall ist erfolgreich, jedoch die **ErrTerm** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a853e-122">In this case, however, the **ErrTerm** function succeeds.</span></span> 
  
<span data-ttu-id="a853e-123">Das Objekt **CChkSGFiles** bestimmt auch, ob die Protokolldateien mit **ErrInit** registriert tatsächlich aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="a853e-123">The **CChkSGFiles** object also determines whether the log files registered with **ErrInit** were actually checked.</span></span> <span data-ttu-id="a853e-124">Wenn nicht alle Protokolle wurden erfolgreich überprüft, die **ErrTerm** -Funktion gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a853e-124">If not all the logs were successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="a853e-125">Wenn **ErrTerm** einen Fehler zurückgibt, werden der erste Fehler, die, den es findet, den Obwohl den Status der Überprüfung für alle Datenbanken, die mit **ErrInit**registriert überprüft.</span><span class="sxs-lookup"><span data-stu-id="a853e-125">When **ErrTerm** returns an error, it will be the first error it finds, even though it checks the verification status for all databases registered with **ErrInit**.</span></span>
  
<span data-ttu-id="a853e-126">Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, müssen Sie die **ErrTerm** -Funktion in den einzelnen Thread Teil der Anwendung aufrufen, und Sie erreichen sie mehr als einmal für jedes Objekt **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="a853e-126">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrTerm** function in the single-threaded portion of the application, and you can call it no more than once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="a853e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a853e-127">Requirements</span></span>

<span data-ttu-id="a853e-128">Exchange 2013 umfasst nur eine 64-Bit-Version von CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="a853e-128">Exchange 2013 only includes a 64-bit version of CHKSGFILES.</span></span>
  
<span data-ttu-id="a853e-129">Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a853e-129">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

