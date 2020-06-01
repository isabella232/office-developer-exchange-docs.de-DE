---
title: CChkSGFiles. New-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- New
api_type:
- dllExport
ms.assetid: 588d8c74-c9ce-4d5e-8a79-a2a68676e858
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: d18d3ef20890012a1d8c193ec87bdca10a1ed451
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455233"
---
# <a name="cchksgfilesnew-function"></a><span data-ttu-id="6dfbe-103">CChkSGFiles. New-Funktion</span><span class="sxs-lookup"><span data-stu-id="6dfbe-103">CChkSGFiles.New function</span></span>

<span data-ttu-id="6dfbe-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="6dfbe-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="6dfbe-105">Erstellt eine neue Instanz der **CChkSGFiles** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="6dfbe-105">Creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="6dfbe-106">Sie müssen diese Funktion aufrufen, bevor Sie die zu überprüfende Speichergruppe und Datenbanken angeben können.</span><span class="sxs-lookup"><span data-stu-id="6dfbe-106">You must call this function before you can specify the storage group and databases to be checked.</span></span> 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a><span data-ttu-id="6dfbe-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dfbe-107">Parameters</span></span>

<span data-ttu-id="6dfbe-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="6dfbe-108">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6dfbe-109">Return value</span><span class="sxs-lookup"><span data-stu-id="6dfbe-109">Return value</span></span>

<span data-ttu-id="6dfbe-110">Ein Verweis (Zeiger) auf das neu erstellte Objekt.</span><span class="sxs-lookup"><span data-stu-id="6dfbe-110">A reference (pointer) to the newly created object.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6dfbe-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dfbe-111">Remarks</span></span>

<span data-ttu-id="6dfbe-112">Die **neue** Funktion erstellt ein **CCheckSGFiles** -Objekt und gibt dem Aufrufer einen Verweis (Zeiger) auf dieses Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="6dfbe-112">The **New** function creates a **CCheckSGFiles** object and returns to the caller a reference (pointer) to that object.</span></span> <span data-ttu-id="6dfbe-113">Sie müssen diese Funktion aufrufen, bevor Sie eine der anderen Funktionen in der **CCheckSGFiles** -Klasse aufruft.</span><span class="sxs-lookup"><span data-stu-id="6dfbe-113">You must call this function before it calls any of the other functions in the **CCheckSGFiles** class.</span></span> 
  
<span data-ttu-id="6dfbe-114">Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **neue** Funktion im Single-Thread-Teil der Anwendung aufrufen, und Sie können Sie nur einmal für jedes **CCheckSGFiles** -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6dfbe-114">If you're using CHKSGFILES in a multithreaded application, you must call the **New** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="6dfbe-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dfbe-115">Requirements</span></span>

<span data-ttu-id="6dfbe-116">Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="6dfbe-116">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="6dfbe-117">Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="6dfbe-117">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

