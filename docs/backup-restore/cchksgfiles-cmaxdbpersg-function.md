---
title: CChkSGFiles.CMaxDbPerSG-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CMaxDbPerSG
api_type:
- dllExport
ms.assetid: 5871988b-a5d7-42cc-9b83-8fededb5072f
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: bf09074bab6dee13e97e8a59a22ae1b19522a5e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757766"
---
# <a name="cchksgfilescmaxdbpersg-function"></a><span data-ttu-id="1fdad-103">CChkSGFiles.CMaxDbPerSG-Funktion</span><span class="sxs-lookup"><span data-stu-id="1fdad-103">CChkSGFiles.CMaxDbPerSG function</span></span>

<span data-ttu-id="1fdad-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fdad-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="1fdad-105">Gibt die maximale Anzahl von Datenbanken in einer einzelnen Exchange Server-Speichergruppe zulässig.</span><span class="sxs-lookup"><span data-stu-id="1fdad-105">Returns the maximum number of databases allowed in a single Exchange server storage group.</span></span>
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a><span data-ttu-id="1fdad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fdad-106">Parameters</span></span>

<span data-ttu-id="1fdad-107">None.</span><span class="sxs-lookup"><span data-stu-id="1fdad-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="1fdad-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fdad-108">Return value</span></span>

<span data-ttu-id="1fdad-109">Die maximale Anzahl von Datenbanken, die der angegebene Exchange-Server pro Speichergruppe zulässt.</span><span class="sxs-lookup"><span data-stu-id="1fdad-109">The maximum number of databases that the specified Exchange server allows per storage group.</span></span> <span data-ttu-id="1fdad-110">Diese Funktion gibt 1 zurück, da Speichergruppen nicht Teil der Exchange 2013 sind.</span><span class="sxs-lookup"><span data-stu-id="1fdad-110">Because storage groups are not part of Exchange 2013, this function returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1fdad-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1fdad-111">Remarks</span></span>

<span data-ttu-id="1fdad-112">Sie können das **CCheckSGFiles** -Objekt verwenden, um Datenbanken (und Transaktionsprotokolldateien) in nur einer Speichergruppe, überprüfen, damit der von der Funktion **CMaxDbPerSG** zurückgegebene Wert auch die maximale Anzahl von Datenbanken darstellt, die Sie mithilfe von überprüfen kann ein die Instanz der **CCheckSGFiles** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="1fdad-112">You can use the **CCheckSGFiles** object to validate databases (and transaction log files) in only one storage group, so the value returned by the **CMaxDbPerSG** function also represents the maximum number of databases that you can check by using an instance of the **CCheckSGFiles** class.</span></span> 
  
<span data-ttu-id="1fdad-113">Beachten Sie, dass standardmäßig bis zu fünf Datenbanken pro Speichergruppe Exchange Server 2003 und Exchange Server 2007 ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1fdad-113">Note that by default, Exchange Server 2003 and Exchange Server 2007 allow a maximum of five databases per storage group.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="1fdad-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fdad-114">Requirements</span></span>

<span data-ttu-id="1fdad-115">Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="1fdad-115">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="1fdad-116">Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1fdad-116">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

