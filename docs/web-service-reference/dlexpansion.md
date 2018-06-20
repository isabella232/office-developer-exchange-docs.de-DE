---
title: DLExpansion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DLExpansion
api_type:
- schema
ms.assetid: 9e50278d-fe6a-45e2-a72b-0fb06809e128
description: Das DLExpansion-Element enthält ein Array von Postfächern, die in einer Verteilerliste enthalten sind.
ms.openlocfilehash: 06081b4aba761a7137f921b3bc1c8d6b2afab88c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758083"
---
# <a name="dlexpansion"></a><span data-ttu-id="14797-103">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="14797-103">DLExpansion</span></span>

<span data-ttu-id="14797-104">Das **DLExpansion** -Element enthält ein Array von Postfächern, die in einer Verteilerliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="14797-104">The **DLExpansion** element contains an array of mailboxes that are contained in a distribution list.</span></span> 
  
- [<span data-ttu-id="14797-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="14797-105">ExpandDLResponse</span></span>](expanddlresponse.md) 
- [<span data-ttu-id="14797-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="14797-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="14797-107">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="14797-107">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
- [<span data-ttu-id="14797-108">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="14797-108">DLExpansion</span></span>](dlexpansion.md)
  
```xml
<DLExpansion AbsoluteDenominator"" IncludesLastItemInRange="" IndexedPagingOffset="" NumeratorOffset="" TotalItemsInView="">
   <Mailbox/>
</DLExpansion>
```

 <span data-ttu-id="14797-109">**ArrayOfDLExpansionType**</span><span class="sxs-lookup"><span data-stu-id="14797-109">**ArrayOfDLExpansionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="14797-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="14797-110">Attributes and elements</span></span>

<span data-ttu-id="14797-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="14797-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14797-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="14797-112">Attributes</span></span>

|<span data-ttu-id="14797-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="14797-113">**Attribute**</span></span>|<span data-ttu-id="14797-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="14797-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="14797-115">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="14797-115">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="14797-116">Stellt den Index, der bei Verwendung einer indizierten Seitenansicht für die nächste Anforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14797-116">Represents the next index that should be used for the next request when you are using an indexed page view.</span></span>  <br/> |
|<span data-ttu-id="14797-117">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="14797-117">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="14797-118">Den neue Zähler-Wert, für die nächste Anforderung verwendet wird, bei Verwendung der Seitenansichten Bruch darstellt.</span><span class="sxs-lookup"><span data-stu-id="14797-118">Represents the new numerator value to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="14797-119">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="14797-119">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="14797-120">Die nächste Nenner für die nächste Anforderung verwendet wird, bei Verwendung der Seitenansichten Bruch darstellt.</span><span class="sxs-lookup"><span data-stu-id="14797-120">Represents the next denominator to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="14797-121">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="14797-121">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="14797-122">Gibt an, ob die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten, sodass zusätzliche Paging nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="14797-122">Indicates whether the current results contain the last item in the query so that additional paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="14797-123">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="14797-123">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="14797-124">Die Gesamtanzahl der Elemente in der Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="14797-124">Represents the total number of items in the view.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="14797-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="14797-125">Child elements</span></span>

|<span data-ttu-id="14797-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="14797-126">**Element**</span></span>|<span data-ttu-id="14797-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="14797-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14797-128">Postfach</span><span class="sxs-lookup"><span data-stu-id="14797-128">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="14797-129">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="14797-129">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="14797-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="14797-130">Parent elements</span></span>

|<span data-ttu-id="14797-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="14797-131">**Element**</span></span>|<span data-ttu-id="14797-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="14797-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14797-133">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="14797-133">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md) <br/> |<span data-ttu-id="14797-134">Enthält den Status und das Ergebnis einer Anforderung der ExpandDL.</span><span class="sxs-lookup"><span data-stu-id="14797-134">Contains the status and result of a single ExpandDL request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14797-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="14797-135">Remarks</span></span>

<span data-ttu-id="14797-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="14797-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14797-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="14797-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14797-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="14797-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="14797-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="14797-139">Schema Name</span></span>  <br/> |<span data-ttu-id="14797-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="14797-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="14797-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="14797-141">Validation File</span></span>  <br/> |<span data-ttu-id="14797-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="14797-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="14797-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="14797-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="14797-144">False</span><span class="sxs-lookup"><span data-stu-id="14797-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14797-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14797-145">See also</span></span>

- [<span data-ttu-id="14797-146">Der ExpandDL-Vorgang</span><span class="sxs-lookup"><span data-stu-id="14797-146">ExpandDL operation</span></span>](expanddl-operation.md)
- [<span data-ttu-id="14797-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="14797-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md) 
- [<span data-ttu-id="14797-148">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="14797-148">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

