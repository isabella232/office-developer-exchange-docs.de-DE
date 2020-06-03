---
title: CChkSGFiles. ErrTerm-Funktion
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
description: 'Letzte Änderung: 25. Februar 2013'
ms.openlocfilehash: 12b07fba69054d327c7250bbf83e4c77016e8b3f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466199"
---
# <a name="cchksgfileserrterm-function"></a><span data-ttu-id="05fba-103">CChkSGFiles. ErrTerm-Funktion</span><span class="sxs-lookup"><span data-stu-id="05fba-103">CChkSGFiles.ErrTerm function</span></span>
  
<span data-ttu-id="05fba-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="05fba-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="05fba-105">Stellt einen allgemeinen Status der Datenbank-und Protokoll Überprüfung bereit, der angibt, ob alle Datenbankseiten und Protokolle erfolgreich überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="05fba-105">Provides an overall status of the database and log verification, which indicates whether all the database pages and logs were successfully verified.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="05fba-106">Speichergruppen stehen in Exchange 2013 nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="05fba-106">Storage groups are not available in Exchange 2013.</span></span> <span data-ttu-id="05fba-107">Aus Gründen der Abwärtskompatibilität mit Datenbanken und Speichergruppen in Exchange-Versionen, die älter als Exchange Server 2010 sind, können Sie mit der CHKSGFILES-API Speichergruppen angeben.</span><span class="sxs-lookup"><span data-stu-id="05fba-107">For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange Server 2010, the CHKSGFILES API enables you to specify storage groups.</span></span> <span data-ttu-id="05fba-108">Wenn Sie CHKSGFILES für Exchange 2013 Datenbanken ausführen, sollten Sie Parameter festlegen, die einen Speichergruppen Bezeichner in eine leere Zeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="05fba-108">When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string.</span></span> 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="05fba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="05fba-109">Parameters</span></span>

### <a name="ulflags"></a><span data-ttu-id="05fba-110">ulFlags</span><span class="sxs-lookup"><span data-stu-id="05fba-110">ulFlags</span></span>
  
<span data-ttu-id="05fba-111">Optionaler Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="05fba-111">Optional input parameter.</span></span> <span data-ttu-id="05fba-112">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="05fba-112">This value is reserved for future use.</span></span> <span data-ttu-id="05fba-113">Der von diesem Parameter übergebene Wert sollte 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="05fba-113">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="05fba-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05fba-114">Return value</span></span>

<span data-ttu-id="05fba-115">Ein Fehlercode aus der [Err](cchksgfiles-err-enumeration.md) -Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="05fba-115">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="05fba-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05fba-116">Remarks</span></span>

<span data-ttu-id="05fba-117">Das **CChkSGFiles** -Objekt bestimmt, ob alle Datenbanken, die mit der **ErrInit** -Funktion registriert wurden, tatsächlich überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="05fba-117">The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="05fba-118">Dieses Objekt verwendet die **ErrCheckDbPages** -Funktion, um zu überprüfen, ob die gleiche Anzahl von Datenbankseiten, die von der **ErrCheckDbHeaders** -Funktion identifiziert wurden, tatsächlich überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="05fba-118">This object uses the **ErrCheckDbPages** function to verify that the same number of database pages identified by the **ErrCheckDbHeaders** function were actually verified.</span></span> <span data-ttu-id="05fba-119">Wenn die richtige Anzahl von Seiten in jeder Datenbank nicht erfolgreich überprüft wird, gibt die **ErrTerm** -Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="05fba-119">If the correct number of pages in each database are not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="05fba-120">Wenn die Anzahl der mit **ErrCheckDbPages** geprüften Datenbankseiten kleiner als die von **ErrCheckDbHeaders**ist, erstellt diese Funktion einen Fehler im Windows-Ereignisprotokoll, und **ErrTerm** gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="05fba-120">If the number of database pages checked with **ErrCheckDbPages** is less than that indicated by **ErrCheckDbHeaders**, this function creates an error in the Windows Event log, and **ErrTerm** returns an error.</span></span> 
  
<span data-ttu-id="05fba-121">Wenn die Anzahl der mit **ErrCheckDbPages** überprüften Datenbankseiten größer als der von **ErrCheckDbHeaders**ist, wird mit dieser Funktion eine Warnung im Windows-Ereignisprotokoll erstellt, um anzugeben, dass die Anwendung möglicherweise unnötig viele Datenbankseiten mehr als einmal überprüft.</span><span class="sxs-lookup"><span data-stu-id="05fba-121">If the number of database pages checked with **ErrCheckDbPages** is greater than that indicated by **ErrCheckDbHeaders**, this function creates a warning in the Windows Event log to indicate that the application might be unnecessarily checking some database pages more than once.</span></span> <span data-ttu-id="05fba-122">In diesem Fall ist die **ErrTerm** -Funktion jedoch erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="05fba-122">In this case, however, the **ErrTerm** function succeeds.</span></span> 
  
<span data-ttu-id="05fba-123">Das **CChkSGFiles** -Objekt bestimmt auch, ob die bei **ErrInit** registrierten Protokolldateien tatsächlich überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="05fba-123">The **CChkSGFiles** object also determines whether the log files registered with **ErrInit** were actually checked.</span></span> <span data-ttu-id="05fba-124">Wenn nicht alle Protokolle erfolgreich überprüft wurden, gibt die **ErrTerm** -Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="05fba-124">If not all the logs were successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="05fba-125">Wenn **ErrTerm** einen Fehler zurückgibt, ist dies der erste gefundene Fehler, auch wenn der Überprüfungsstatus für alle mit **ErrInit**registrierten Datenbanken überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="05fba-125">When **ErrTerm** returns an error, it will be the first error it finds, even though it checks the verification status for all databases registered with **ErrInit**.</span></span>
  
<span data-ttu-id="05fba-126">Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **ErrTerm** -Funktion im Single-Thread-Teil der Anwendung aufrufen, und Sie können Sie für jedes **CCheckSGFiles** -Objekt nicht mehr als einmal aufrufen.</span><span class="sxs-lookup"><span data-stu-id="05fba-126">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrTerm** function in the single-threaded portion of the application, and you can call it no more than once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="05fba-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05fba-127">Requirements</span></span>

<span data-ttu-id="05fba-128">Exchange 2013 enthält nur eine 64-Bit-Version von CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="05fba-128">Exchange 2013 only includes a 64-bit version of CHKSGFILES.</span></span>
  
<span data-ttu-id="05fba-129">Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="05fba-129">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

