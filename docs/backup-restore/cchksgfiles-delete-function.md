---
title: CChkSGFiles. Delete-Funktion
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
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: 38cb72b42727855f652de607bb2a02ecdeaae16e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44447050"
---
# <a name="cchksgfilesdelete-function"></a><span data-ttu-id="98b9a-103">CChkSGFiles. Delete-Funktion</span><span class="sxs-lookup"><span data-stu-id="98b9a-103">CChkSGFiles.Delete function</span></span>

<span data-ttu-id="98b9a-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="98b9a-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="98b9a-105">Zerstört eine vorhandene Instanz der **CChkSGFiles** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="98b9a-105">Destroys an existing instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="98b9a-106">Sie müssen diese Funktion aufrufen, nachdem die Anwendung die Arbeit mit dem angegebenen Objekt abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="98b9a-106">You must call this function after the application has finished working with the specified object.</span></span> 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a><span data-ttu-id="98b9a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="98b9a-107">Parameters</span></span>

### <a name="pcchecksgfiles"></a><span data-ttu-id="98b9a-108">pcchecksgfiles</span><span class="sxs-lookup"><span data-stu-id="98b9a-108">pcchecksgfiles</span></span> 
  
<span data-ttu-id="98b9a-109">Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="98b9a-109">Input parameter.</span></span> <span data-ttu-id="98b9a-110">Ein Zeiger auf ein vorhandenes **CCheckSGFiles** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="98b9a-110">A pointer to an existing **CCheckSGFiles** object.</span></span> <span data-ttu-id="98b9a-111">Der dem Objekt zugeordnete Arbeitsspeicher wird dann freigegeben.</span><span class="sxs-lookup"><span data-stu-id="98b9a-111">The memory associated with the object will then be freed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98b9a-112">Return value</span><span class="sxs-lookup"><span data-stu-id="98b9a-112">Return value</span></span>

<span data-ttu-id="98b9a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="98b9a-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98b9a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98b9a-114">Remarks</span></span>

<span data-ttu-id="98b9a-115">Die **Delete** -Funktion gibt den Arbeitsspeicher frei, der dem **CCheckSGFiles** -Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="98b9a-115">The **Delete** function frees the memory associated with the **CCheckSGFiles** object.</span></span> <span data-ttu-id="98b9a-116">Nachdem Sie **Delete**aufgerufen haben, ist der im *pcchecksgfiles* -Parameter übergebene Zeiger ungültig, und für dieses Objekt können keine anderen Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="98b9a-116">After you call **Delete**, the pointer passed in the  *pcchecksgfiles*  parameter will be invalid and no other operations can be performed on that object.</span></span> 
  
<span data-ttu-id="98b9a-117">Wenn die Anwendung die **ErrCheckDbPages** -Funktion verwendet, muss die Anwendung den Arbeitsspeicherpuffer manuell freigeben; die **Delete** -Funktion kann Sie nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="98b9a-117">If the application uses the **ErrCheckDbPages** function, the application must free the memory buffer manually; the **Delete** function will not free it.</span></span> 
  
<span data-ttu-id="98b9a-118">Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **Delete** -Funktion im Single-Thread-Teil der Anwendung aufrufen, und Sie können Sie nur einmal für jedes **CCheckSGFiles** -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="98b9a-118">If you're using CHKSGFILES in a multithreaded application, you must call the **Delete** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="98b9a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98b9a-119">Requirements</span></span>

<span data-ttu-id="98b9a-120">Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="98b9a-120">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="98b9a-121">Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="98b9a-121">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

