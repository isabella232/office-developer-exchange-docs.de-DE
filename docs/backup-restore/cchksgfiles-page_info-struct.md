---
title: CChkSGFiles. PAGE_INFO-Struktur
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
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: 5ec9f4303b26ea95b125adac6943945ae1276439
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456339"
---
# <a name="cchksgfilespage_info-struct"></a><span data-ttu-id="60ab7-103">CChkSGFiles. PAGE_INFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="60ab7-103">CChkSGFiles.PAGE_INFO struct</span></span>

<span data-ttu-id="60ab7-104">**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="60ab7-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="60ab7-105">Speichert Informationen für eine Exchange-Datenbankseite.</span><span class="sxs-lookup"><span data-stu-id="60ab7-105">Holds information for an Exchange database page.</span></span> <span data-ttu-id="60ab7-106">Diese Struktur wird mit der **ErrCheckDbPages** -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="60ab7-106">This structure is used with the **ErrCheckDbPages** function.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="60ab7-107">Members</span><span class="sxs-lookup"><span data-stu-id="60ab7-107">Members</span></span>

### <a name="ulpgno"></a><span data-ttu-id="60ab7-108">ulPgNo</span><span class="sxs-lookup"><span data-stu-id="60ab7-108">ulPgNo</span></span>
  
<span data-ttu-id="60ab7-109">Lange ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="60ab7-109">Unsigned Long.</span></span> <span data-ttu-id="60ab7-110">Logische Seitenzahl der zu überprüfenden Datenbankseite.</span><span class="sxs-lookup"><span data-stu-id="60ab7-110">Logical page number of the database page to be checked.</span></span> <span data-ttu-id="60ab7-111">Dieser Wert muss festgelegt werden, bevor **ErrCheckDbPages**aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="60ab7-111">This value must be set before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="60ab7-112">Wenn die Anwendung die Datei auf der Grundlage von Datei Offsets liest und diese Datei Offsets daher logischen Seitenzahlen zuordnen muss, finden Sie die **PgnoFromFileOffset** -Methode hilfreich, um den Wert für dieses Feld zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="60ab7-112">If the application is reading the file based on file offsets, and must therefore map those file offsets to logical page numbers, you will find the **PgnoFromFileOffset** method useful to determine the value for this field.</span></span> <span data-ttu-id="60ab7-113">Dieser Wert wird von **ErrCheckDbPages** nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="60ab7-113">**ErrCheckDbPages** does not modify this value.</span></span> 
    
### <a name="fpageisinitialized"></a><span data-ttu-id="60ab7-114">fPageIsInitialized</span><span class="sxs-lookup"><span data-stu-id="60ab7-114">fPageIsInitialized</span></span> 
  
<span data-ttu-id="60ab7-115">Boolean.</span><span class="sxs-lookup"><span data-stu-id="60ab7-115">Boolean.</span></span> <span data-ttu-id="60ab7-116">Der Wert true gibt an, dass die Datenbankseite Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="60ab7-116">A value of TRUE indicates that the database page contains data.</span></span> <span data-ttu-id="60ab7-117">Der Wert false gibt an, dass die Seite nur Nullen enthält.</span><span class="sxs-lookup"><span data-stu-id="60ab7-117">A value of FALSE indicates that the page contains only zeros.</span></span> <span data-ttu-id="60ab7-118">**ErrCheckDbPages** legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="60ab7-118">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="fcorrectableerror"></a><span data-ttu-id="60ab7-119">fCorrectableError</span><span class="sxs-lookup"><span data-stu-id="60ab7-119">fCorrectableError</span></span>
  
<span data-ttu-id="60ab7-120">Boolean.</span><span class="sxs-lookup"><span data-stu-id="60ab7-120">Boolean.</span></span> <span data-ttu-id="60ab7-121">Der Wert true gibt an, dass auf der Datenbankseite ein Prüfsummen Konflikt festgestellt wurde, dass es sich jedoch um einen korrigierbaren Fehler handelt.</span><span class="sxs-lookup"><span data-stu-id="60ab7-121">A value of TRUE indicates that there was a checksum mismatch detected in the database page, but that it is a correctable error.</span></span> <span data-ttu-id="60ab7-122">**ErrCheckDbPages** legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="60ab7-122">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumactual"></a><span data-ttu-id="60ab7-123">checksumActual</span><span class="sxs-lookup"><span data-stu-id="60ab7-123">checksumActual</span></span>
  
<span data-ttu-id="60ab7-124">Vorzeichenlose 64-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="60ab7-124">Unsigned 64-bit integer.</span></span> <span data-ttu-id="60ab7-125">Gibt den in der Datenbank für diese logische Seite gespeicherten Prüfsummenwert an.</span><span class="sxs-lookup"><span data-stu-id="60ab7-125">Indicates the checksum value stored in the database for this logical page.</span></span> <span data-ttu-id="60ab7-126">**ErrCheckDbPages** legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="60ab7-126">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumexpected"></a><span data-ttu-id="60ab7-127">checksumExpected</span><span class="sxs-lookup"><span data-stu-id="60ab7-127">checksumExpected</span></span>
  
<span data-ttu-id="60ab7-128">Vorzeichenlose 64-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="60ab7-128">Unsigned 64-bit integer.</span></span> <span data-ttu-id="60ab7-129">Dies ist der erwartete Prüfsummenwert, der für die Datenbankseite berechnet wird; Sie wird von **ErrCheckDbPages**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60ab7-129">This is the expected checksum value that is calculated for the database page; it is set by **ErrCheckDbPages**.</span></span> <span data-ttu-id="60ab7-130">Wenn sich dieser Wert von dem auf der Datenbankseite (also dem in **checksumActual**zurückgegebenen Wert) unterscheidet, gibt **ErrCheckDbPages** an, dass auf dieser Datenbankseite ein Fehler gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="60ab7-130">If this value is different from that stored on the database page (that is, the value returned in **checksumActual**), **ErrCheckDbPages** will indicate that an error was found on this database page.</span></span> 
    
### <a name="dbtime"></a><span data-ttu-id="60ab7-131">dbTime</span><span class="sxs-lookup"><span data-stu-id="60ab7-131">dbTime</span></span>
  
<span data-ttu-id="60ab7-132">Vorzeichenlose 64-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="60ab7-132">Unsigned 64-bit integer.</span></span> <span data-ttu-id="60ab7-133">**ErrCheckDbPages** legt dieses Element auf den Zeitstempel auf der Datenbankseite fest.</span><span class="sxs-lookup"><span data-stu-id="60ab7-133">**ErrCheckDbPages** sets this member to the timestamp on the database page.</span></span> 
    
### <a name="checksumpagestructure"></a><span data-ttu-id="60ab7-134">checksumPageStructure</span><span class="sxs-lookup"><span data-stu-id="60ab7-134">checksumPageStructure</span></span> 
  
<span data-ttu-id="60ab7-135">Unsigned 64-BT Integer.</span><span class="sxs-lookup"><span data-stu-id="60ab7-135">Unsigned 64-bt integer.</span></span> <span data-ttu-id="60ab7-136">**ErrCheckDbPages** legt dieses Element auf den berechneten Prüfsummenwert des Inhalts der Seite mit Ausnahme von Daten fest, die bei der Bestimmung der Äquivalenz der logischen Seite nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="60ab7-136">**ErrCheckDbPages** sets this member to the calculated checksum value of the contents of the page excluding data which is unnecessary when determining the logical page equivalence.</span></span> <span data-ttu-id="60ab7-137">Beispielsweise ist es nicht erforderlich, die Datenwerte in nicht verwendeten Datenbankseiten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="60ab7-137">For example, it is unnecessary to consider the data values in unused database page space.</span></span> <span data-ttu-id="60ab7-138">Dieser Member ist nur gültig, wenn die **checksumActual** -und **checksumExpected** -Werte einander gleich sind.</span><span class="sxs-lookup"><span data-stu-id="60ab7-138">This member is only valid if the **checksumActual**  and  **checksumExpected**  values are equal to each other.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="60ab7-139">ulFlags</span><span class="sxs-lookup"><span data-stu-id="60ab7-139">ulFlags</span></span>
  
<span data-ttu-id="60ab7-140">Vorzeichenlose 64-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="60ab7-140">Unsigned 64-bit integer.</span></span> <span data-ttu-id="60ab7-141">Reserviert für zukünftige Verwendung.</span><span class="sxs-lookup"><span data-stu-id="60ab7-141">Reserved for future use.</span></span> <span data-ttu-id="60ab7-142">Der Wert dieses Felds muss auf 0 (null) festgelegt werden, bevor **ErrCheckDbPages**aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="60ab7-142">The value of this field must be set to 0 (zero) before calling **ErrCheckDbPages**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60ab7-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60ab7-143">Remarks</span></span>

<span data-ttu-id="60ab7-144">Beim Aufrufen der **ErrCheckDbPages** -Funktion ist der **rgPageInfo** -Parameter ein Array von **Seiten \_ Info** Strukturen.</span><span class="sxs-lookup"><span data-stu-id="60ab7-144">When calling the **ErrCheckDbPages** function, the **rgPageInfo**  parameter is an array of **PAGE\_INFO** structures.</span></span> <span data-ttu-id="60ab7-145">Es muss eine **Seiten \_ Info** Struktur für jede zu überprüfende Datenbankseite geben.</span><span class="sxs-lookup"><span data-stu-id="60ab7-145">There must be one **PAGE\_INFO** structure for each database page to be checked.</span></span> 
  
<span data-ttu-id="60ab7-146">Die Anwendung muss das **ulPgno** -Element auf den richtigen Wert festlegen und das **ulFlags** -Element auch auf 0 (null) festlegen, bevor **ErrCheckDbPages**aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="60ab7-146">The application must set the **ulPgno**  member to the proper value, and must also set the  **ulFlags**  member to 0 (zero) before calling **ErrCheckDbPages**.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="60ab7-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60ab7-147">Requirements</span></span>

<span data-ttu-id="60ab7-148">Exchange Server 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="60ab7-148">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="60ab7-149">Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="60ab7-149">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

