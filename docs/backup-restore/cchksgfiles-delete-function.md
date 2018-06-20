---
title: CChkSGFiles.Delete-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- dllExport
ms.assetid: 869e927f-7df2-4247-88ef-b8b05b29a700
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: 5c41007a797e5a256692b2c4bdcb3cfae82c12ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756804"
---
# <a name="cchksgfilesdelete-function"></a><span data-ttu-id="3b9af-103">CChkSGFiles.Delete-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b9af-103">CChkSGFiles.Delete function</span></span>

<span data-ttu-id="3b9af-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b9af-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="3b9af-105">Löscht eine vorhandene Instanz der **CChkSGFiles** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="3b9af-105">Destroys an existing instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="3b9af-106">Sie müssen diese Funktion aufrufen, nachdem die Anwendung arbeiten mit dem angegebenen Objekt beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3b9af-106">You must call this function after the application has finished working with the specified object.</span></span> 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a><span data-ttu-id="3b9af-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b9af-107">Parameters</span></span>

### <a name="pcchecksgfiles"></a><span data-ttu-id="3b9af-108">pcchecksgfiles</span><span class="sxs-lookup"><span data-stu-id="3b9af-108">pcchecksgfiles</span></span> 
  
<span data-ttu-id="3b9af-109">Input-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3b9af-109">Input parameter.</span></span> <span data-ttu-id="3b9af-110">Ein Zeiger auf ein vorhandenes **CCheckSGFiles** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3b9af-110">A pointer to an existing **CCheckSGFiles** object.</span></span> <span data-ttu-id="3b9af-111">Klicken Sie dann das Objekt zugeordnete Arbeitsspeicher bleiben.</span><span class="sxs-lookup"><span data-stu-id="3b9af-111">The memory associated with the object will then be freed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3b9af-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b9af-112">Return value</span></span>

<span data-ttu-id="3b9af-113">None.</span><span class="sxs-lookup"><span data-stu-id="3b9af-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b9af-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3b9af-114">Remarks</span></span>

<span data-ttu-id="3b9af-115">Die **Löschen** -Funktion gibt den Speicherplatz frei **CCheckSGFiles** -Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3b9af-115">The **Delete** function frees the memory associated with the **CCheckSGFiles** object.</span></span> <span data-ttu-id="3b9af-116">Nach dem Aufruf von **Löschen**der *Pcchecksgfiles* -Parameter übergebene Zeiger ist ungültig und keine anderen Operationen für dieses Objekt ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="3b9af-116">After you call **Delete**, the pointer passed in the  *pcchecksgfiles*  parameter will be invalid and no other operations can be performed on that object.</span></span> 
  
<span data-ttu-id="3b9af-117">Wenn die Anwendung die **ErrCheckDbPages** -Funktion verwendet wird, muss die Anwendung Pufferüberläufe manuell frei; die **Löschen** -Funktion gibt es nicht frei.</span><span class="sxs-lookup"><span data-stu-id="3b9af-117">If the application uses the **ErrCheckDbPages** function, the application must free the memory buffer manually; the **Delete** function will not free it.</span></span> 
  
<span data-ttu-id="3b9af-118">Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, müssen Sie die **Löschen** -Funktion in den einzelnen Thread Teil der Anwendung aufrufen und können Sie nur einmal für jede **CCheckSGFiles** -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3b9af-118">If you're using CHKSGFILES in a multithreaded application, you must call the **Delete** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="3b9af-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b9af-119">Requirements</span></span>

<span data-ttu-id="3b9af-120">Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="3b9af-120">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="3b9af-121">Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3b9af-121">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

