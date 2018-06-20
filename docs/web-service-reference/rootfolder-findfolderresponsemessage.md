---
title: RootFolder (FindFolderResponseMessage)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 5089c815-663f-46be-bc59-aed9ee20f94a
description: Das RootFolder-Element enthält die Ergebnisse der Suche in der ein einzelner Stammordner während eines Vorgangs FindFolder.
ms.openlocfilehash: 1cd79d5fa34318e7fe29606df84cbf0ef0520b93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831253"
---
# <a name="rootfolder-findfolderresponsemessage"></a><span data-ttu-id="52e23-103">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="52e23-103">RootFolder (FindFolderResponseMessage)</span></span>

<span data-ttu-id="52e23-104">Das **RootFolder** -Element enthält die Ergebnisse der Suche in der ein einzelner Stammordner während einer [FindFolder Vorgang](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="52e23-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Folders/>
</RootFolder>
```

 <span data-ttu-id="52e23-105">**FindFolderParentType**</span><span class="sxs-lookup"><span data-stu-id="52e23-105">**FindFolderParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52e23-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="52e23-106">Attributes and elements</span></span>

<span data-ttu-id="52e23-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="52e23-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52e23-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="52e23-108">Attributes</span></span>

|<span data-ttu-id="52e23-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="52e23-109">**Attribute**</span></span>|<span data-ttu-id="52e23-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52e23-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52e23-111">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="52e23-111">IndexedPagingOffset</span></span>  <br/> |<span data-ttu-id="52e23-112">Stellt den Index, der bei Verwendung eine indizierten Paging-Ansicht für die nächste Anforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52e23-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="52e23-113">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="52e23-113">NumeratorOffset</span></span>  <br/> |<span data-ttu-id="52e23-114">Steht für den neuen Wert Zähler verwenden Sie für die nächste Anforderung bei Bruchzahlen Seitenansichten Verwendung.</span><span class="sxs-lookup"><span data-stu-id="52e23-114">Represents the new numerator value to use for the next request when using fractional page views.</span></span>  <br/> |
|<span data-ttu-id="52e23-115">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="52e23-115">AbsoluteDenominator</span></span>  <br/> |<span data-ttu-id="52e23-116">Verwenden Sie für die nächste Anforderung bei Bruchzahlen Paging die nächste Nenner darstellt.</span><span class="sxs-lookup"><span data-stu-id="52e23-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="52e23-117">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="52e23-117">IncludesLastItemInRange</span></span>  <br/> |<span data-ttu-id="52e23-118">Gibt an, ob die aktuellen Ergebnisse der letzten Ordner in der Abfrage enthalten, so dass weitere paging nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="52e23-118">Indicates whether the current results contain the last folder in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="52e23-119">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="52e23-119">TotalItemsInView</span></span>  <br/> |<span data-ttu-id="52e23-120">Stellt die Gesamtzahl der Ordner, in denen die Einschränkung übergeben.</span><span class="sxs-lookup"><span data-stu-id="52e23-120">Represents the total number of folders that pass the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="52e23-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52e23-121">Child elements</span></span>

|<span data-ttu-id="52e23-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="52e23-122">**Element**</span></span>|<span data-ttu-id="52e23-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52e23-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52e23-124">Ordner</span><span class="sxs-lookup"><span data-stu-id="52e23-124">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="52e23-125">Enthält ein Array von Ordnern mithilfe der [FindFolder Vorgang](findfolder-operation.md)gefunden.</span><span class="sxs-lookup"><span data-stu-id="52e23-125">Contains an array of folders found by using the [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52e23-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52e23-126">Parent elements</span></span>

|<span data-ttu-id="52e23-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="52e23-127">**Element**</span></span>|<span data-ttu-id="52e23-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52e23-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52e23-129">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="52e23-129">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md) <br/> |<span data-ttu-id="52e23-130">Enthält den Status und das Ergebnis einer Anforderung [FindFolder Vorgang](findfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="52e23-130">Contains the status and result of a [FindFolder operation](findfolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52e23-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="52e23-131">Remarks</span></span>

<span data-ttu-id="52e23-132">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="52e23-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52e23-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="52e23-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52e23-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="52e23-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="52e23-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="52e23-135">Schema name</span></span>  <br/> |<span data-ttu-id="52e23-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="52e23-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="52e23-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="52e23-137">Validation file</span></span>  <br/> |<span data-ttu-id="52e23-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="52e23-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52e23-139">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="52e23-139">Can be empty</span></span>  <br/> |<span data-ttu-id="52e23-140">False</span><span class="sxs-lookup"><span data-stu-id="52e23-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52e23-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52e23-141">See also</span></span>



[<span data-ttu-id="52e23-142">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="52e23-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="52e23-143">Suchen nach Ordnern</span><span class="sxs-lookup"><span data-stu-id="52e23-143">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

