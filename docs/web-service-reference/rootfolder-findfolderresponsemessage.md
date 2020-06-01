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
description: Das RootFolder-Element enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines FindFolder-Vorgangs.
ms.openlocfilehash: b5601d6abec67196c9991908e272a2122a201d69
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457137"
---
# <a name="rootfolder-findfolderresponsemessage"></a><span data-ttu-id="b7402-103">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="b7402-103">RootFolder (FindFolderResponseMessage)</span></span>

<span data-ttu-id="b7402-104">Das **RootFolder** -Element enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines [FindFolder-Vorgangs](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="b7402-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Folders/>
</RootFolder>
```

 <span data-ttu-id="b7402-105">**FindFolderParentType**</span><span class="sxs-lookup"><span data-stu-id="b7402-105">**FindFolderParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7402-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b7402-106">Attributes and elements</span></span>

<span data-ttu-id="b7402-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b7402-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7402-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b7402-108">Attributes</span></span>

|<span data-ttu-id="b7402-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b7402-109">**Attribute**</span></span>|<span data-ttu-id="b7402-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7402-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7402-111">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="b7402-111">IndexedPagingOffset</span></span>  <br/> |<span data-ttu-id="b7402-112">Stellt den nächsten Index dar, der bei der Verwendung einer indizierten Auslagerungs Ansicht für die nächste Anforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7402-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="b7402-113">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="b7402-113">NumeratorOffset</span></span>  <br/> |<span data-ttu-id="b7402-114">Stellt den neuen Zählerwert dar, der für die nächste Anforderung bei der Verwendung von Bruch Seitenansichten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7402-114">Represents the new numerator value to use for the next request when using fractional page views.</span></span>  <br/> |
|<span data-ttu-id="b7402-115">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="b7402-115">AbsoluteDenominator</span></span>  <br/> |<span data-ttu-id="b7402-116">Stellt den nächsten Nenner dar, der für die nächste Anforderung bei Bruchzahlen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7402-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="b7402-117">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="b7402-117">IncludesLastItemInRange</span></span>  <br/> |<span data-ttu-id="b7402-118">Gibt an, ob die aktuellen Ergebnisse den letzten Ordner in der Abfrage enthalten, sodass kein weiteres Paging erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b7402-118">Indicates whether the current results contain the last folder in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="b7402-119">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="b7402-119">TotalItemsInView</span></span>  <br/> |<span data-ttu-id="b7402-120">Stellt die Gesamtzahl der Ordner dar, die die Einschränkung übergeben.</span><span class="sxs-lookup"><span data-stu-id="b7402-120">Represents the total number of folders that pass the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b7402-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7402-121">Child elements</span></span>

|<span data-ttu-id="b7402-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="b7402-122">**Element**</span></span>|<span data-ttu-id="b7402-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7402-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7402-124">Ordner</span><span class="sxs-lookup"><span data-stu-id="b7402-124">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b7402-125">Enthält ein Array von Ordnern, die mit dem [FindFolder-Vorgang](findfolder-operation.md)gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="b7402-125">Contains an array of folders found by using the [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b7402-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7402-126">Parent elements</span></span>

|<span data-ttu-id="b7402-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="b7402-127">**Element**</span></span>|<span data-ttu-id="b7402-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7402-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7402-129">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b7402-129">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md) <br/> |<span data-ttu-id="b7402-130">Enthält den Status und das Ergebnis einer [FindFolder-Vorgangs](findfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b7402-130">Contains the status and result of a [FindFolder operation](findfolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7402-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7402-131">Remarks</span></span>

<span data-ttu-id="b7402-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b7402-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7402-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b7402-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7402-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7402-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b7402-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b7402-135">Schema name</span></span>  <br/> |<span data-ttu-id="b7402-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b7402-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b7402-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b7402-137">Validation file</span></span>  <br/> |<span data-ttu-id="b7402-138">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b7402-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7402-139">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b7402-139">Can be empty</span></span>  <br/> |<span data-ttu-id="b7402-140">False</span><span class="sxs-lookup"><span data-stu-id="b7402-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7402-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7402-141">See also</span></span>



[<span data-ttu-id="b7402-142">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b7402-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="b7402-143">Suchen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="b7402-143">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

