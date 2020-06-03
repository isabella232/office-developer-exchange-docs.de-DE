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
description: Das IndexedPageFolderView-Element beschreibt, wie Informationen zum ausgelagerten Element in einer FindFolder-Antwort zurückgegeben werden.
ms.openlocfilehash: 6e9e2796c0bdcd9a15487f0e1bc7cbdf09d0a492
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457200"
---
# <a name="indexedpagefolderview"></a><span data-ttu-id="d6b84-103">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="d6b84-103">IndexedPageFolderView</span></span>

<span data-ttu-id="d6b84-104">Das **IndexedPageFolderView** -Element beschreibt, wie Informationen zum ausgelagerten Element in einer [FindFolder](findfolder.md) -Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d6b84-104">The **IndexedPageFolderView** element describes how paged item information is returned in a [FindFolder](findfolder.md) response.</span></span> 
  
[<span data-ttu-id="d6b84-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="d6b84-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="d6b84-106">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="d6b84-106">IndexedPageFolderView</span></span>](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 <span data-ttu-id="d6b84-107">**IndexedPageViewType**</span><span class="sxs-lookup"><span data-stu-id="d6b84-107">**IndexedPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d6b84-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d6b84-108">Attributes and elements</span></span>

<span data-ttu-id="d6b84-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d6b84-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6b84-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d6b84-110">Attributes</span></span>

|<span data-ttu-id="d6b84-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d6b84-111">**Attribute**</span></span>|<span data-ttu-id="d6b84-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6b84-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6b84-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="d6b84-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="d6b84-114">Beschreibt die maximale Anzahl von Ordnern, die in der Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6b84-114">Describes the maximum number of folders to return in the response.</span></span> <span data-ttu-id="d6b84-115">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="d6b84-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="d6b84-116">**Offset**</span><span class="sxs-lookup"><span data-stu-id="d6b84-116">**Offset**</span></span> <br/> |<span data-ttu-id="d6b84-117">Beschreibt den Offset aus dem **Basepoint**.</span><span class="sxs-lookup"><span data-stu-id="d6b84-117">Describes the offset from the **BasePoint**.</span></span> <span data-ttu-id="d6b84-118">Offset muss größer als oder gleich NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d6b84-118">Offset must be greater than or equal to zero.</span></span> <span data-ttu-id="d6b84-119">Wenn **Basepoint** gleich dem Anfang ist, ist der Offset positiv.</span><span class="sxs-lookup"><span data-stu-id="d6b84-119">If **BasePoint** is equal to Beginning, the offset is positive.</span></span> <span data-ttu-id="d6b84-120">Wenn **Basepoint** gleich End ist, wird der Offset so behandelt, als wäre er negativ.</span><span class="sxs-lookup"><span data-stu-id="d6b84-120">If **BasePoint** is equal to End, the offset is handled as if it were negative.</span></span>  <br/> <span data-ttu-id="d6b84-121">Dadurch wird angegeben, welcher Ordner der erste in der Antwort zugestellte Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="d6b84-121">This identifies which folder will be the first folder delivered in the response.</span></span> <span data-ttu-id="d6b84-122">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6b84-122">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="d6b84-123">**Basepoint**</span><span class="sxs-lookup"><span data-stu-id="d6b84-123">**BasePoint**</span></span> <br/> |<span data-ttu-id="d6b84-124">Beschreibt, ob die Seite von Ordnern am Anfang oder am Ende der Ordnergruppe beginnt, die mit den Suchkriterien gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d6b84-124">Describes whether the page of folders will start from the start or the end of the set of folders that are found with the search criteria.</span></span> <span data-ttu-id="d6b84-125">Suche von Ende aus sucht immer rückwärts.</span><span class="sxs-lookup"><span data-stu-id="d6b84-125">Seeking from the end always searches backward.</span></span> <span data-ttu-id="d6b84-126">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6b84-126">This attribute is required.</span></span>  <br/> |
   
#### <a name="basepoint-attribute"></a><span data-ttu-id="d6b84-127">Basepoint-Attribut</span><span class="sxs-lookup"><span data-stu-id="d6b84-127">BasePoint Attribute</span></span>

|<span data-ttu-id="d6b84-128">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d6b84-128">**Value**</span></span>|<span data-ttu-id="d6b84-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6b84-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6b84-130">Anfang</span><span class="sxs-lookup"><span data-stu-id="d6b84-130">Beginning</span></span>  <br/> |<span data-ttu-id="d6b84-131">Die ausgelagerte Ansicht beginnt am Anfang der gefundenen Ordnergruppe.</span><span class="sxs-lookup"><span data-stu-id="d6b84-131">The paged view starts at the beginning of the found folder set.</span></span>  <br/> |
|<span data-ttu-id="d6b84-132">Ende</span><span class="sxs-lookup"><span data-stu-id="d6b84-132">End</span></span>  <br/> |<span data-ttu-id="d6b84-133">Die ausgelagerte Ansicht beginnt am Ende der gefundenen Ordnergruppe.</span><span class="sxs-lookup"><span data-stu-id="d6b84-133">The paged view starts at the end of the found folder set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d6b84-134">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6b84-134">Child elements</span></span>

<span data-ttu-id="d6b84-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="d6b84-135">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d6b84-136">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6b84-136">Parent elements</span></span>

|<span data-ttu-id="d6b84-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6b84-137">**Element**</span></span>|<span data-ttu-id="d6b84-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6b84-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6b84-139">FindFolder</span><span class="sxs-lookup"><span data-stu-id="d6b84-139">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="d6b84-140">Definiert eine Anforderung zum Suchen von Ordnern in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="d6b84-140">Defines a request to find folders in a mailbox.</span></span>  <br/> <span data-ttu-id="d6b84-141">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="d6b84-141">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6b84-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6b84-142">Remarks</span></span>

<span data-ttu-id="d6b84-143">Bei der Suche von Ende wird der vom Offset angegebene Ursprung verschoben.</span><span class="sxs-lookup"><span data-stu-id="d6b84-143">Seeking from end involves moving to the origin identified by the offset.</span></span> <span data-ttu-id="d6b84-144">Darüber hinaus wird der Zeiger nach der Anzahl der angeforderten Datensätze zurück verschoben.</span><span class="sxs-lookup"><span data-stu-id="d6b84-144">Additionally, the pointer is moved back by the number of requested records.</span></span> <span data-ttu-id="d6b84-145">Wenn beispielsweise 100 Datensätze vorhanden sind und der Offset 25 vom Ende ist, beginnt die Suche von 75.</span><span class="sxs-lookup"><span data-stu-id="d6b84-145">For example, if there are 100 records and the offset is 25 from the end, the search starts from 75.</span></span> <span data-ttu-id="d6b84-146">Wenn 10 Datensätze zurückgegeben werden, wird der Zeiger rückwärts um weitere 10 Datensätze nach 65 verschoben und gibt Datensätze 65 bis 75 zurück.</span><span class="sxs-lookup"><span data-stu-id="d6b84-146">If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75.</span></span> <span data-ttu-id="d6b84-147">Der nächste Index lautet 64.</span><span class="sxs-lookup"><span data-stu-id="d6b84-147">The next index is 64.</span></span> <span data-ttu-id="d6b84-148">Der nächste Offset vom Ende für eine Seite ist 100 minus 64, was 36 entspricht.</span><span class="sxs-lookup"><span data-stu-id="d6b84-148">The next offset from the end for a page is 100 minus 64 which equals 36.</span></span> <span data-ttu-id="d6b84-149">Der Wert für den nächsten Offset vom Ende zum Abrufen der nächsten indizierten Seite lautet 36.</span><span class="sxs-lookup"><span data-stu-id="d6b84-149">The value for the next offset from the end to get the next indexed page is 36.</span></span>
  
<span data-ttu-id="d6b84-150">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d6b84-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6b84-151">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d6b84-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6b84-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6b84-152">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d6b84-153">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d6b84-153">Schema Name</span></span>  <br/> |<span data-ttu-id="d6b84-154">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d6b84-154">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d6b84-155">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d6b84-155">Validation File</span></span>  <br/> |<span data-ttu-id="d6b84-156">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d6b84-156">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d6b84-157">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d6b84-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="d6b84-158">False</span><span class="sxs-lookup"><span data-stu-id="d6b84-158">False</span></span>  <br/> |
   

