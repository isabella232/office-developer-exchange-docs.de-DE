---
title: CChkSGFiles.PAGE_INFO-Struktur
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PAGE_INFO
api_type:
- dllExport
ms.assetid: 408335e1-6977-441f-bfad-ede791d1630c
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: fa66d253b4fc6bd5c29a39c5323f59bf323a906f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757743"
---
# <a name="cchksgfilespageinfo-struct"></a><span data-ttu-id="87ad0-103">CChkSGFiles.PAGE_INFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="87ad0-103">CChkSGFiles.PAGE_INFO struct</span></span>

<span data-ttu-id="87ad0-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="87ad0-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="87ad0-105">Enthält Informationen für eine Exchange-Datenbank-Seite.</span><span class="sxs-lookup"><span data-stu-id="87ad0-105">Holds information for an Exchange database page.</span></span> <span data-ttu-id="87ad0-106">Diese Struktur wird mit der **ErrCheckDbPages** -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="87ad0-106">This structure is used with the **ErrCheckDbPages** function.</span></span> 
  
```cs
Struct PAGE_INFO  
{
        ULONGulPgno;
        BOOLfPageIsInitialized : 1;
        BOOLfCorrectableError : 1;
        ULONGLONGchecksumActual;
        ULONGLONGchecksumExpected;
        ULONGLONGdbTime;
        ULONGLONGchecksumPageStructure;
        ULONGLONGulFlags;
}

```

## <a name="members"></a><span data-ttu-id="87ad0-107">Members</span><span class="sxs-lookup"><span data-stu-id="87ad0-107">Members</span></span>

### <a name="ulpgno"></a><span data-ttu-id="87ad0-108">ulPgNo</span><span class="sxs-lookup"><span data-stu-id="87ad0-108">ulPgNo</span></span>
  
<span data-ttu-id="87ad0-109">Nicht signierte lange.</span><span class="sxs-lookup"><span data-stu-id="87ad0-109">Unsigned Long.</span></span> <span data-ttu-id="87ad0-110">Logische Seitenzahl der Datenbankseite überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="87ad0-110">Logical page number of the database page to be checked.</span></span> <span data-ttu-id="87ad0-111">Dieser Wert muss vor dem Aufruf von **ErrCheckDbPages**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="87ad0-111">This value must be set before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="87ad0-112">Wenn die Anwendung die Datei basierend auf Datei Offsets liest und muss daher diese Datei Offsets auf logische Seitenzahlen zuordnen, finden Sie die **PgnoFromFileOffset** -Methode hilfreich sein, die den Wert für dieses Feld zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="87ad0-112">If the application is reading the file based on file offsets, and must therefore map those file offsets to logical page numbers, you will find the **PgnoFromFileOffset** method useful to determine the value for this field.</span></span> <span data-ttu-id="87ad0-113">Dieser Wert **ErrCheckDbPages** nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="87ad0-113">**ErrCheckDbPages** does not modify this value.</span></span> 
    
### <a name="fpageisinitialized"></a><span data-ttu-id="87ad0-114">fPageIsInitialized</span><span class="sxs-lookup"><span data-stu-id="87ad0-114">fPageIsInitialized</span></span> 
  
<span data-ttu-id="87ad0-115">Boolean-Wert.</span><span class="sxs-lookup"><span data-stu-id="87ad0-115">Boolean.</span></span> <span data-ttu-id="87ad0-116">TRUE gibt an, dass die Datenbankseite Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="87ad0-116">A value of TRUE indicates that the database page contains data.</span></span> <span data-ttu-id="87ad0-117">Der Wert FALSE gibt an, dass die Seite nur Nullen enthält.</span><span class="sxs-lookup"><span data-stu-id="87ad0-117">A value of FALSE indicates that the page contains only zeros.</span></span> <span data-ttu-id="87ad0-118">**ErrCheckDbPages** legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="87ad0-118">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="fcorrectableerror"></a><span data-ttu-id="87ad0-119">fCorrectableError</span><span class="sxs-lookup"><span data-stu-id="87ad0-119">fCorrectableError</span></span>
  
<span data-ttu-id="87ad0-120">Boolean-Wert.</span><span class="sxs-lookup"><span data-stu-id="87ad0-120">Boolean.</span></span> <span data-ttu-id="87ad0-121">Der Wert TRUE gibt an, dass es einer Nichtübereinstimmung der Prüfsumme der Seite Datenbank erkannt wurde, aber es einen behebbaren Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="87ad0-121">A value of TRUE indicates that there was a checksum mismatch detected in the database page, but that it is a correctable error.</span></span> <span data-ttu-id="87ad0-122">**ErrCheckDbPages** legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="87ad0-122">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumactual"></a><span data-ttu-id="87ad0-123">checksumActual</span><span class="sxs-lookup"><span data-stu-id="87ad0-123">checksumActual</span></span>
  
<span data-ttu-id="87ad0-124">64-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-124">Unsigned 64-bit integer.</span></span> <span data-ttu-id="87ad0-125">Gibt den Prüfsummenwert in der Datenbank für diese logische Seite gespeichert.</span><span class="sxs-lookup"><span data-stu-id="87ad0-125">Indicates the checksum value stored in the database for this logical page.</span></span> <span data-ttu-id="87ad0-126">**ErrCheckDbPages** legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="87ad0-126">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumexpected"></a><span data-ttu-id="87ad0-127">checksumExpected</span><span class="sxs-lookup"><span data-stu-id="87ad0-127">checksumExpected</span></span>
  
<span data-ttu-id="87ad0-128">64-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-128">Unsigned 64-bit integer.</span></span> <span data-ttu-id="87ad0-129">Dies ist der erwartete Prüfsumme-Wert, der für die Datenbankseite berechnet wird. Es wird vom **ErrCheckDbPages**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="87ad0-129">This is the expected checksum value that is calculated for the database page; it is set by **ErrCheckDbPages**.</span></span> <span data-ttu-id="87ad0-130">Wenn dieser Wert unterscheiden, die auf der Datenbankseite gespeichert ist (d. h., der Rückgabewert in **ChecksumActual**), **ErrCheckDbPages** werden anzugeben, dass ein Fehler auf dieser Datenbankseite gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="87ad0-130">If this value is different from that stored on the database page (that is, the value returned in **checksumActual**), **ErrCheckDbPages** will indicate that an error was found on this database page.</span></span> 
    
### <a name="dbtime"></a><span data-ttu-id="87ad0-131">Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="87ad0-131">dbTime</span></span>
  
<span data-ttu-id="87ad0-132">64-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-132">Unsigned 64-bit integer.</span></span> <span data-ttu-id="87ad0-133">**ErrCheckDbPages** wird dieser Member auf den Zeitstempel auf der Datenbankseite.</span><span class="sxs-lookup"><span data-stu-id="87ad0-133">**ErrCheckDbPages** sets this member to the timestamp on the database page.</span></span> 
    
### <a name="checksumpagestructure"></a><span data-ttu-id="87ad0-134">checksumPageStructure</span><span class="sxs-lookup"><span data-stu-id="87ad0-134">checksumPageStructure</span></span> 
  
<span data-ttu-id="87ad0-135">64-Bt-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-135">Unsigned 64-bt integer.</span></span> <span data-ttu-id="87ad0-136">**ErrCheckDbPages** wird dieser Member auf den Wert berechnete Prüfsumme des Inhalts der Seite Ausschließen von Daten, die nicht erforderlich ist, wenn die logische Seite Gleichwertigkeit bestimmen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-136">**ErrCheckDbPages** sets this member to the calculated checksum value of the contents of the page excluding data which is unnecessary when determining the logical page equivalence.</span></span> <span data-ttu-id="87ad0-137">Beispielsweise ist es nicht erforderlich, die Datenwerte in nicht verwendeten Seite Datenbankspeicherplatzes berücksichtigt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="87ad0-137">For example, it is unnecessary to consider the data values in unused database page space.</span></span> <span data-ttu-id="87ad0-138">Dieser Member ist nur gültig, wenn die Werte **ChecksumActual** und **ChecksumExpected** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-138">This member is only valid if the **checksumActual**  and  **checksumExpected**  values are equal to each other.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="87ad0-139">ulFlags</span><span class="sxs-lookup"><span data-stu-id="87ad0-139">ulFlags</span></span>
  
<span data-ttu-id="87ad0-140">64-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-140">Unsigned 64-bit integer.</span></span> <span data-ttu-id="87ad0-141">Reserviert für zukünftige Verwendung.</span><span class="sxs-lookup"><span data-stu-id="87ad0-141">Reserved for future use.</span></span> <span data-ttu-id="87ad0-142">Der Wert dieses Felds muss vor dem Aufruf von **ErrCheckDbPages**auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="87ad0-142">The value of this field must be set to 0 (zero) before calling **ErrCheckDbPages**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87ad0-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="87ad0-143">Remarks</span></span>

<span data-ttu-id="87ad0-144">Beim Aufruf der Funktion **ErrCheckDbPages** der **RgPageInfo** -Parameter ist ein Array von **Seite\_INFO** Strukturen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-144">When calling the **ErrCheckDbPages** function, the **rgPageInfo**  parameter is an array of **PAGE\_INFO** structures.</span></span> <span data-ttu-id="87ad0-145">Es muss eine **Seite\_INFO** Struktur für jede Datenbankseite überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="87ad0-145">There must be one **PAGE\_INFO** structure for each database page to be checked.</span></span> 
  
<span data-ttu-id="87ad0-146">Die Anwendung den **UlPgno** Member muss auf den korrekten Wert festgelegt, und den **UlFlags** Member muss auch auf 0 (null) festgelegt werden, bevor **ErrCheckDbPages**aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-146">The application must set the **ulPgno**  member to the proper value, and must also set the  **ulFlags**  member to 0 (zero) before calling **ErrCheckDbPages**.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="87ad0-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87ad0-147">Requirements</span></span>

<span data-ttu-id="87ad0-148">Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="87ad0-148">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="87ad0-149">Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-149">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

