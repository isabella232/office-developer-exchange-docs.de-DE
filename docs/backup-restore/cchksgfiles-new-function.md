---
title: CChkSGFiles.New-Funktion
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
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: b40f8b1a95477715b29defb4addabfb333e92d04
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756798"
---
# <a name="cchksgfilesnew-function"></a><span data-ttu-id="eba41-103">CChkSGFiles.New-Funktion</span><span class="sxs-lookup"><span data-stu-id="eba41-103">CChkSGFiles.New function</span></span>

<span data-ttu-id="eba41-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="eba41-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="eba41-105">Erstellt eine neue Instanz der **CChkSGFiles** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="eba41-105">Creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="eba41-106">Sie müssen diese Funktion aufrufen, bevor Sie angeben können, die Speichergruppe und Datenbanken überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="eba41-106">You must call this function before you can specify the storage group and databases to be checked.</span></span> 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a><span data-ttu-id="eba41-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="eba41-107">Parameters</span></span>

<span data-ttu-id="eba41-108">None.</span><span class="sxs-lookup"><span data-stu-id="eba41-108">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="eba41-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eba41-109">Return value</span></span>

<span data-ttu-id="eba41-110">Ein Verweis (Zeiger) auf das neu erstellte Objekt.</span><span class="sxs-lookup"><span data-stu-id="eba41-110">A reference (pointer) to the newly created object.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eba41-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eba41-111">Remarks</span></span>

<span data-ttu-id="eba41-112">Die **New** -Funktion erstellt ein **CCheckSGFiles** -Objekt und gibt einen Verweis (Zeiger) auf dieses Objekt an den Anrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="eba41-112">The **New** function creates a **CCheckSGFiles** object and returns to the caller a reference (pointer) to that object.</span></span> <span data-ttu-id="eba41-113">Sie müssen diese Funktion aufrufen, bevor sie eine der anderen Funktionen in der **CCheckSGFiles** -Klasse aufruft.</span><span class="sxs-lookup"><span data-stu-id="eba41-113">You must call this function before it calls any of the other functions in the **CCheckSGFiles** class.</span></span> 
  
<span data-ttu-id="eba41-114">Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, müssen Sie die **New** -Funktion in den einzelnen Thread Teil der Anwendung aufrufen und können Sie nur einmal für jede **CCheckSGFiles** -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eba41-114">If you're using CHKSGFILES in a multithreaded application, you must call the **New** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="eba41-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eba41-115">Requirements</span></span>

<span data-ttu-id="eba41-116">Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="eba41-116">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="eba41-117">Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eba41-117">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

