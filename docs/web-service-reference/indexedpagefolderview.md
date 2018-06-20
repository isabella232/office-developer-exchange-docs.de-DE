---
title: IndexedPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageFolderView
api_type:
- schema
ms.assetid: c6dac232-244b-4db0-9a15-5e01b8aa7a7d
description: Das IndexedPageFolderView-Element beschreibt, wie ausgelagerten Elementinformationen in einer FindFolder Antwort zurückgegeben wird.
ms.openlocfilehash: f32f778daa6fa3fea93ab2bc1951f2407dcf7f80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829910"
---
# <a name="indexedpagefolderview"></a><span data-ttu-id="549c0-103">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="549c0-103">IndexedPageFolderView</span></span>

<span data-ttu-id="549c0-104">Das **IndexedPageFolderView** -Element beschreibt, wie ausgelagerten Elementinformationen in einer [FindFolder](findfolder.md) Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="549c0-104">The **IndexedPageFolderView** element describes how paged item information is returned in a [FindFolder](findfolder.md) response.</span></span> 
  
[<span data-ttu-id="549c0-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="549c0-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="549c0-106">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="549c0-106">IndexedPageFolderView</span></span>](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 <span data-ttu-id="549c0-107">**IndexedPageViewType**</span><span class="sxs-lookup"><span data-stu-id="549c0-107">**IndexedPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="549c0-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="549c0-108">Attributes and elements</span></span>

<span data-ttu-id="549c0-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="549c0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="549c0-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="549c0-110">Attributes</span></span>

|<span data-ttu-id="549c0-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="549c0-111">**Attribute**</span></span>|<span data-ttu-id="549c0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="549c0-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="549c0-113">**"MaxEntriesReturned"**</span><span class="sxs-lookup"><span data-stu-id="549c0-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="549c0-114">Beschreibt die maximale Anzahl von Ordnern in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="549c0-114">Describes the maximum number of folders to return in the response.</span></span> <span data-ttu-id="549c0-115">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="549c0-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="549c0-116">**Offset**</span><span class="sxs-lookup"><span data-stu-id="549c0-116">**Offset**</span></span> <br/> |<span data-ttu-id="549c0-117">Beschreibt die **Basispunkt**-Offset.</span><span class="sxs-lookup"><span data-stu-id="549c0-117">Describes the offset from the **BasePoint**.</span></span> <span data-ttu-id="549c0-118">Offset muss größer als oder gleich 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="549c0-118">Offset must be greater than or equal to zero.</span></span> <span data-ttu-id="549c0-119">Wenn **Basispunkt** Anfang gleich ist, ist der Offset positiv.</span><span class="sxs-lookup"><span data-stu-id="549c0-119">If **BasePoint** is equal to Beginning, the offset is positive.</span></span> <span data-ttu-id="549c0-120">Wenn **Basispunkt** End entspricht, wird der Offset behandelt, als wäre es negative.</span><span class="sxs-lookup"><span data-stu-id="549c0-120">If **BasePoint** is equal to End, the offset is handled as if it were negative.</span></span>  <br/> <span data-ttu-id="549c0-121">Mit diesen wird identifiziert, welcher Ordner der erste Ordner in der Antwort übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="549c0-121">This identifies which folder will be the first folder delivered in the response.</span></span> <span data-ttu-id="549c0-122">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="549c0-122">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="549c0-123">**Basispunkt**</span><span class="sxs-lookup"><span data-stu-id="549c0-123">**BasePoint**</span></span> <br/> |<span data-ttu-id="549c0-124">Beschreibt, ob die Seite Ordner gestartet wird, aus der Anfang oder das Ende des Satzes von Ordnern, die mit den Suchkriterien gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="549c0-124">Describes whether the page of folders will start from the start or the end of the set of folders that are found with the search criteria.</span></span> <span data-ttu-id="549c0-125">Vom Ende immer bemüht sucht rückwärts.</span><span class="sxs-lookup"><span data-stu-id="549c0-125">Seeking from the end always searches backward.</span></span> <span data-ttu-id="549c0-126">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="549c0-126">This attribute is required.</span></span>  <br/> |
   
#### <a name="basepoint-attribute"></a><span data-ttu-id="549c0-127">Basispunkt-Attribut</span><span class="sxs-lookup"><span data-stu-id="549c0-127">BasePoint Attribute</span></span>

|<span data-ttu-id="549c0-128">**Wert**</span><span class="sxs-lookup"><span data-stu-id="549c0-128">**Value**</span></span>|<span data-ttu-id="549c0-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="549c0-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="549c0-130">Anfang</span><span class="sxs-lookup"><span data-stu-id="549c0-130">Beginning</span></span>  <br/> |<span data-ttu-id="549c0-131">Die Seitenansicht beginnt am Anfang des Satzes gefundenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="549c0-131">The paged view starts at the beginning of the found folder set.</span></span>  <br/> |
|<span data-ttu-id="549c0-132">Ende</span><span class="sxs-lookup"><span data-stu-id="549c0-132">End</span></span>  <br/> |<span data-ttu-id="549c0-133">Die Seitenansicht beginnt am Ende des Satzes gefundenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="549c0-133">The paged view starts at the end of the found folder set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="549c0-134">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="549c0-134">Child elements</span></span>

<span data-ttu-id="549c0-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="549c0-135">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="549c0-136">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="549c0-136">Parent elements</span></span>

|<span data-ttu-id="549c0-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="549c0-137">**Element**</span></span>|<span data-ttu-id="549c0-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="549c0-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="549c0-139">FindFolder</span><span class="sxs-lookup"><span data-stu-id="549c0-139">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="549c0-140">Definiert eine Anforderung zum Suchen von Ordnern in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="549c0-140">Defines a request to find folders in a mailbox.</span></span>  <br/> <span data-ttu-id="549c0-141">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="549c0-141">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="549c0-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="549c0-142">Remarks</span></span>

<span data-ttu-id="549c0-143">End gesucht umfasst das Verschieben in den Offset identifizierten Ursprung.</span><span class="sxs-lookup"><span data-stu-id="549c0-143">Seeking from end involves moving to the origin identified by the offset.</span></span> <span data-ttu-id="549c0-144">Darüber hinaus wird der Mauszeiger durch die Anzahl der angeforderten Datensätze zurück verschoben.</span><span class="sxs-lookup"><span data-stu-id="549c0-144">Additionally, the pointer is moved back by the number of requested records.</span></span> <span data-ttu-id="549c0-145">Beispielsweise wenn 100 Datensätze vorhanden sind und der Offset 25 vom Ende ist, beginnt für die Suche von 75.</span><span class="sxs-lookup"><span data-stu-id="549c0-145">For example, if there are 100 records and the offset is 25 from the end, the search starts from 75.</span></span> <span data-ttu-id="549c0-146">Wenn 10 Datensätze zurückgegeben werden, wird der Mauszeiger rückwärts verschoben, zusätzlich 10 65 Datensätze und Datensätze 65 bis 75 zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="549c0-146">If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75.</span></span> <span data-ttu-id="549c0-147">Der nächste Index ist 64.</span><span class="sxs-lookup"><span data-stu-id="549c0-147">The next index is 64.</span></span> <span data-ttu-id="549c0-148">Der nächste Offset vom Ende einer Seite wird 100 minus 64 was 36 entspricht.</span><span class="sxs-lookup"><span data-stu-id="549c0-148">The next offset from the end for a page is 100 minus 64 which equals 36.</span></span> <span data-ttu-id="549c0-149">Der Wert für den nächsten Offset vom Ende zum Abrufen der nächsten Seite indizierten ist 36.</span><span class="sxs-lookup"><span data-stu-id="549c0-149">The value for the next offset from the end to get the next indexed page is 36.</span></span>
  
<span data-ttu-id="549c0-150">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="549c0-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="549c0-151">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="549c0-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="549c0-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="549c0-152">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="549c0-153">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="549c0-153">Schema Name</span></span>  <br/> |<span data-ttu-id="549c0-154">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="549c0-154">Messages schema</span></span>  <br/> |
|<span data-ttu-id="549c0-155">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="549c0-155">Validation File</span></span>  <br/> |<span data-ttu-id="549c0-156">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="549c0-156">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="549c0-157">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="549c0-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="549c0-158">False</span><span class="sxs-lookup"><span data-stu-id="549c0-158">False</span></span>  <br/> |
   

