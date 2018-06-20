---
title: Nicht
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Not
api_type:
- schema
ms.assetid: 1aa16318-7e90-4b19-bce8-dd1a20a66223
description: Das Element nicht stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.
ms.openlocfilehash: f5bc709d8b1e77a13b3598905651ac1750436f03
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830553"
---
# <a name="not"></a><span data-ttu-id="ff18b-103">Nicht</span><span class="sxs-lookup"><span data-stu-id="ff18b-103">Not</span></span>

<span data-ttu-id="ff18b-104">Das Element **nicht** stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="ff18b-104">The **Not** element represents a search expression that negates the Boolean value of the search expression that it contains.</span></span> 
  
```xml
<Not>
   <SearchExpression/>
</Not>
```

 <span data-ttu-id="ff18b-105">**NotType**</span><span class="sxs-lookup"><span data-stu-id="ff18b-105">**NotType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff18b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ff18b-106">Attributes and elements</span></span>

<span data-ttu-id="ff18b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ff18b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff18b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ff18b-108">Attributes</span></span>

<span data-ttu-id="ff18b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ff18b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff18b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff18b-110">Child elements</span></span>

|<span data-ttu-id="ff18b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff18b-111">**Element**</span></span>|<span data-ttu-id="ff18b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff18b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff18b-113">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="ff18b-113">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="ff18b-114">Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar.</span><span class="sxs-lookup"><span data-stu-id="ff18b-114">Represents the base class for expressions within a restriction.</span></span> <br/><br/><span data-ttu-id="ff18b-115">Eines der folgenden Elemente muss für das Element **SearchExpression** ersetzt werden:</span><span class="sxs-lookup"><span data-stu-id="ff18b-115">One of the following elements must be substituted for the **SearchExpression** element:</span></span> <br/> <br/><span data-ttu-id="ff18b-116">- [Vorhanden ist](exists.md)</span><span class="sxs-lookup"><span data-stu-id="ff18b-116">- [Exists](exists.md)</span></span> <br/><span data-ttu-id="ff18b-117">- [Schließt](excludes.md)</span><span class="sxs-lookup"><span data-stu-id="ff18b-117">- [Excludes](excludes.md)</span></span> <br/><span data-ttu-id="ff18b-118">- ["IsEqualTo"](isequalto.md)</span><span class="sxs-lookup"><span data-stu-id="ff18b-118">- [IsEqualTo](isequalto.md)</span></span> <br/><span data-ttu-id="ff18b-119">- [IsNotEqualTo](isnotequalto.md)</span><span class="sxs-lookup"><span data-stu-id="ff18b-119">- [IsNotEqualTo](isnotequalto.md)</span></span> <br/><span data-ttu-id="ff18b-120">- [IsGreaterThan](isgreaterthan.md)</span><span class="sxs-lookup"><span data-stu-id="ff18b-120">- [IsGreaterThan](isgreaterthan.md)</span></span> <br/><span data-ttu-id="ff18b-121">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="ff18b-121">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span></span> <br/><span data-ttu-id="ff18b-122">- [IsLessThan](islessthan.md)</span><span class="sxs-lookup"><span data-stu-id="ff18b-122">- [IsLessThan](islessthan.md)</span></span> <br/><span data-ttu-id="ff18b-123">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="ff18b-123">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span></span> <br/><span data-ttu-id="ff18b-124">- [Enthält](contains.md)</span><span class="sxs-lookup"><span data-stu-id="ff18b-124">- [Contains](contains.md)</span></span> <br/><span data-ttu-id="ff18b-125">- **Nicht**</span><span class="sxs-lookup"><span data-stu-id="ff18b-125">- **Not**</span></span> <br/><span data-ttu-id="ff18b-126">- [Und](and.md)</span><span class="sxs-lookup"><span data-stu-id="ff18b-126">- [And](and.md)</span></span> <br/><span data-ttu-id="ff18b-127">- [Oder](or.md)</span><span class="sxs-lookup"><span data-stu-id="ff18b-127">- [Or](or.md)</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ff18b-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff18b-128">Parent elements</span></span>

|<span data-ttu-id="ff18b-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff18b-129">**Element**</span></span>|<span data-ttu-id="ff18b-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff18b-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff18b-131">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="ff18b-131">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="ff18b-132">Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff18b-132">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|<span data-ttu-id="ff18b-133">**not**</span><span class="sxs-lookup"><span data-stu-id="ff18b-133">**Not**</span></span> <br/> |<span data-ttu-id="ff18b-134">Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="ff18b-134">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="ff18b-135">Und</span><span class="sxs-lookup"><span data-stu-id="ff18b-135">And</span></span>](and.md) <br/> |<span data-ttu-id="ff18b-136">Stellt einen Search-Ausdruck, der eine Boolean **und** -Operation zwischen zwei oder mehr Suchausdrücke ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="ff18b-136">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="ff18b-137">Das Ergebnis der **AND** -Operation ist **true** , wenn **alle enthaltenen das Element **und** Suchausdrücke zutreffen**.</span><span class="sxs-lookup"><span data-stu-id="ff18b-137">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="ff18b-138">- oder -</span><span class="sxs-lookup"><span data-stu-id="ff18b-138">Or</span></span>](or.md) <br/> |<span data-ttu-id="ff18b-139">Stellt einen Search-Ausdruck, der eine logische **OR** -Operation für den Suchbegriff durchführt, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="ff18b-139">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="ff18b-140">**Oder** gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff18b-140">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="ff18b-141">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ff18b-141">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff18b-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ff18b-142">Remarks</span></span>

<span data-ttu-id="ff18b-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ff18b-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff18b-144">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ff18b-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff18b-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff18b-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ff18b-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ff18b-146">Schema Name</span></span>  <br/> |<span data-ttu-id="ff18b-147">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ff18b-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="ff18b-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ff18b-148">Validation File</span></span>  <br/> |<span data-ttu-id="ff18b-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ff18b-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ff18b-150">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ff18b-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff18b-151">False</span><span class="sxs-lookup"><span data-stu-id="ff18b-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff18b-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff18b-152">See also</span></span>

- [<span data-ttu-id="ff18b-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ff18b-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

