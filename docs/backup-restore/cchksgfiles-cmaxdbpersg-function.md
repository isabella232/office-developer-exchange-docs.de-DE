---
title: CChkSGFiles. CMaxDbPerSG-Funktion
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
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: b7c3517779eb07ef053c1dd4fa25544310fb3343
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455261"
---
# <a name="cchksgfilescmaxdbpersg-function"></a><span data-ttu-id="3f2fb-103">CChkSGFiles. CMaxDbPerSG-Funktion</span><span class="sxs-lookup"><span data-stu-id="3f2fb-103">CChkSGFiles.CMaxDbPerSG function</span></span>

<span data-ttu-id="3f2fb-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f2fb-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="3f2fb-105">Gibt die maximale Anzahl von Datenbanken zurück, die in einer einzelnen Exchange Server-Speichergruppe zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="3f2fb-105">Returns the maximum number of databases allowed in a single Exchange server storage group.</span></span>
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a><span data-ttu-id="3f2fb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f2fb-106">Parameters</span></span>

<span data-ttu-id="3f2fb-107">Keine.</span><span class="sxs-lookup"><span data-stu-id="3f2fb-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3f2fb-108">Return value</span><span class="sxs-lookup"><span data-stu-id="3f2fb-108">Return value</span></span>

<span data-ttu-id="3f2fb-109">Die maximale Anzahl von Datenbanken, die der angegebene Exchange-Server pro Speichergruppe zulässt.</span><span class="sxs-lookup"><span data-stu-id="3f2fb-109">The maximum number of databases that the specified Exchange server allows per storage group.</span></span> <span data-ttu-id="3f2fb-110">Da Speichergruppen nicht Teil Exchange 2013 sind, gibt diese Funktion den Wert 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="3f2fb-110">Because storage groups are not part of Exchange 2013, this function returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f2fb-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f2fb-111">Remarks</span></span>

<span data-ttu-id="3f2fb-112">Mit dem **CCheckSGFiles** -Objekt können Sie Datenbanken (und Transaktionsprotokolldateien) nur in einer Speichergruppe validieren, sodass der von der **CMaxDbPerSG** -Funktion zurückgegebene Wert auch die maximale Anzahl von Datenbanken darstellt, die Sie überprüfen können, indem Sie eine Instanz der **CCheckSGFiles** -Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="3f2fb-112">You can use the **CCheckSGFiles** object to validate databases (and transaction log files) in only one storage group, so the value returned by the **CMaxDbPerSG** function also represents the maximum number of databases that you can check by using an instance of the **CCheckSGFiles** class.</span></span> 
  
<span data-ttu-id="3f2fb-113">Beachten Sie, dass Exchange Server 2003 und Exchange Server 2007 standardmäßig maximal fünf Datenbanken pro Speichergruppe zulassen.</span><span class="sxs-lookup"><span data-stu-id="3f2fb-113">Note that by default, Exchange Server 2003 and Exchange Server 2007 allow a maximum of five databases per storage group.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="3f2fb-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f2fb-114">Requirements</span></span>

<span data-ttu-id="3f2fb-115">Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="3f2fb-115">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="3f2fb-116">Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="3f2fb-116">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

