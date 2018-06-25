---
title: Oder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Or
api_type:
- schema
ms.assetid: 4876d83a-73a3-4953-9d95-3048e6b76ccb
description: Or-Element stellt ein Suchbegriff, der ein logisches OR Suchbegriffs durchführt, die er enthält. Oder zurückgegebenen True, wenn ein untergeordnetes Element true zurückgegeben. Oder benötigen Sie mindestens zwei untergeordnete Elemente.
ms.openlocfilehash: 46cf031047aeb09e05a385150ab7587968aef345
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830661"
---
# <a name="or"></a><span data-ttu-id="9f529-105">Oder</span><span class="sxs-lookup"><span data-stu-id="9f529-105">Or</span></span>

<span data-ttu-id="9f529-106">Das Element **oder** stellt einen Suchbegriff, der ein logisches **oder** den Ausdruck für die Suche durchführt, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="9f529-106">The **Or** element represents a search expression that performs a logical **OR** on the search expression that it contains.</span></span> <span data-ttu-id="9f529-107">**Oder** gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9f529-107">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="9f529-108">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9f529-108">**Or** must have two or more children.</span></span> 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 <span data-ttu-id="9f529-109">**OrType**</span><span class="sxs-lookup"><span data-stu-id="9f529-109">**OrType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9f529-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9f529-110">Attributes and elements</span></span>

<span data-ttu-id="9f529-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9f529-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9f529-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="9f529-112">Attributes</span></span>

<span data-ttu-id="9f529-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="9f529-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9f529-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9f529-114">Child elements</span></span>

|<span data-ttu-id="9f529-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="9f529-115">**Element**</span></span>|<span data-ttu-id="9f529-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f529-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9f529-117">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="9f529-117">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="9f529-118">Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar.</span><span class="sxs-lookup"><span data-stu-id="9f529-118">Represents the base class for expressions within a restriction.</span></span> <br/><br/><span data-ttu-id="9f529-119">Eines der folgenden Elemente muss für das Element **SearchExpression** ersetzt werden:</span><span class="sxs-lookup"><span data-stu-id="9f529-119">One of the following elements must be substituted for the **SearchExpression** element:</span></span> <br/> <br/><span data-ttu-id="9f529-120">- [Vorhanden ist](exists.md)</span><span class="sxs-lookup"><span data-stu-id="9f529-120">- [Exists](exists.md)</span></span> <br/><span data-ttu-id="9f529-121">- [Schließt](excludes.md)</span><span class="sxs-lookup"><span data-stu-id="9f529-121">- [Excludes](excludes.md)</span></span> <br/><span data-ttu-id="9f529-122">- ["IsEqualTo"](isequalto.md)</span><span class="sxs-lookup"><span data-stu-id="9f529-122">- [IsEqualTo](isequalto.md)</span></span> <br/><span data-ttu-id="9f529-123">- [IsNotEqualTo](isnotequalto.md)</span><span class="sxs-lookup"><span data-stu-id="9f529-123">- [IsNotEqualTo](isnotequalto.md)</span></span> <br/><span data-ttu-id="9f529-124">- [IsGreaterThan](isgreaterthan.md)</span><span class="sxs-lookup"><span data-stu-id="9f529-124">- [IsGreaterThan](isgreaterthan.md)</span></span> <br/><span data-ttu-id="9f529-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="9f529-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span></span> <br/><span data-ttu-id="9f529-126">- [IsLessThan](islessthan.md)</span><span class="sxs-lookup"><span data-stu-id="9f529-126">- [IsLessThan](islessthan.md)</span></span> <br/><span data-ttu-id="9f529-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="9f529-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span></span> <br/><span data-ttu-id="9f529-128">- [Enthält](contains.md)</span><span class="sxs-lookup"><span data-stu-id="9f529-128">- [Contains](contains.md)</span></span> <br/><span data-ttu-id="9f529-129">- [Nicht](not.md)</span><span class="sxs-lookup"><span data-stu-id="9f529-129">- [Not](not.md)</span></span> <br/><span data-ttu-id="9f529-130">- [Und](and.md)</span><span class="sxs-lookup"><span data-stu-id="9f529-130">- [And](and.md)</span></span> <br/><span data-ttu-id="9f529-131">- **Oder**</span><span class="sxs-lookup"><span data-stu-id="9f529-131">- **Or**</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9f529-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9f529-132">Parent elements</span></span>

|<span data-ttu-id="9f529-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="9f529-133">**Element**</span></span>|<span data-ttu-id="9f529-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f529-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9f529-135">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="9f529-135">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="9f529-136">Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f529-136">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="9f529-137">not</span><span class="sxs-lookup"><span data-stu-id="9f529-137">Not</span></span>](not.md) <br/> |<span data-ttu-id="9f529-138">Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="9f529-138">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="9f529-139">Und</span><span class="sxs-lookup"><span data-stu-id="9f529-139">And</span></span>](and.md) <br/> |<span data-ttu-id="9f529-140">Stellt einen Search-Ausdruck, der eine Boolean **und** -Operation zwischen zwei oder mehr Suchausdrücke ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="9f529-140">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="9f529-141">Das Ergebnis der **AND** -Operation ist **true** , wenn **alle enthaltenen das Element **und** Suchausdrücke zutreffen**.</span><span class="sxs-lookup"><span data-stu-id="9f529-141">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|<span data-ttu-id="9f529-142">**- oder -**</span><span class="sxs-lookup"><span data-stu-id="9f529-142">**Or**</span></span> <br/> |<span data-ttu-id="9f529-143">Stellt einen Search-Ausdruck, der eine logische **OR** -Operation für den Suchbegriff durchführt, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="9f529-143">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="9f529-144">**Oder** gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9f529-144">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="9f529-145">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9f529-145">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f529-146">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f529-146">Remarks</span></span>

<span data-ttu-id="9f529-147">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9f529-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9f529-148">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9f529-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f529-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f529-149">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9f529-150">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9f529-150">Schema Name</span></span>  <br/> |<span data-ttu-id="9f529-151">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9f529-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="9f529-152">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9f529-152">Validation File</span></span>  <br/> |<span data-ttu-id="9f529-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9f529-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9f529-154">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9f529-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="9f529-155">False</span><span class="sxs-lookup"><span data-stu-id="9f529-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9f529-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f529-156">See also</span></span>

- [<span data-ttu-id="9f529-157">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9f529-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

