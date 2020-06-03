---
title: SearchExpression
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchExpression
api_type:
- schema
ms.assetid: daa179b6-8c7f-4268-a312-c2acc67fa7c3
description: Das Search-Element ist ein abstraktes Element, das das ersetzte Element innerhalb einer Einschränkung darstellt. Alle Suchausdrücke werden von diesem Basistyp abgeleitet. Dieses Element wird in einem XML-Instanzendokument nicht verwendet.
ms.openlocfilehash: db06ce8e2faa0f2589963d58aab55073c618c171
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530352"
---
# <a name="searchexpression"></a><span data-ttu-id="2c9c2-105">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="2c9c2-105">SearchExpression</span></span>

<span data-ttu-id="2c9c2-106">Das **Search** -Element ist ein abstraktes Element, das das ersetzte Element innerhalb einer Einschränkung darstellt.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-106">The **SearchExpression** element is an abstract element that represents the substituted element within a restriction.</span></span> <span data-ttu-id="2c9c2-107">Alle Suchausdrücke werden von diesem Basistyp abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-107">All search expressions derive from this base type.</span></span> <span data-ttu-id="2c9c2-108">Dieses Element wird in einem XML-Instanzendokument nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-108">This element is not used in an XML instance document.</span></span> 
  
```xml
<SearchExpression/>
```

 <span data-ttu-id="2c9c2-109">**SearchExpressionType**</span><span class="sxs-lookup"><span data-stu-id="2c9c2-109">**SearchExpressionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c9c2-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2c9c2-110">Attributes and elements</span></span>

<span data-ttu-id="2c9c2-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c9c2-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c9c2-112">Attributes</span></span>

<span data-ttu-id="2c9c2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c9c2-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c9c2-114">Child elements</span></span>

<span data-ttu-id="2c9c2-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2c9c2-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c9c2-116">Parent elements</span></span>

|<span data-ttu-id="2c9c2-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c9c2-117">**Element**</span></span>|<span data-ttu-id="2c9c2-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c9c2-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c9c2-119">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="2c9c2-119">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="2c9c2-120">Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-120">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="2c9c2-121">not</span><span class="sxs-lookup"><span data-stu-id="2c9c2-121">Not</span></span>](not.md) <br/> |<span data-ttu-id="2c9c2-122">Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-122">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="2c9c2-123">Und</span><span class="sxs-lookup"><span data-stu-id="2c9c2-123">And</span></span>](and.md) <br/> |<span data-ttu-id="2c9c2-124">Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert **und** eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-124">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="2c9c2-125">Das Ergebnis der **and-** Operation ist **true** , wenn alle im **and-** Element enthaltenen Suchausdrücke **true**sind.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-125">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="2c9c2-126">- oder -</span><span class="sxs-lookup"><span data-stu-id="2c9c2-126">Or</span></span>](or.md) <br/> |<span data-ttu-id="2c9c2-127">Stellt einen Suchausdruck dar, der eine logische **or** -Operation für den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-127">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="2c9c2-128">**Oder** gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-128">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="2c9c2-129">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-129">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c9c2-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c9c2-130">Remarks</span></span>

<span data-ttu-id="2c9c2-131">Jedes Filter-Element, das Teil der Such Satz Ersetzungsgruppe ist, kann anstelle des Search-Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-131">Any filter element that is part of the SearchExpression substitution group can appear in place of the SearchExpression element.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2c9c2-132">Dieses Element wird nie direkt in einem Instanzdokument auftreten.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-132">This element will never occur directly within an instance document.</span></span> 
  
<span data-ttu-id="2c9c2-133">Die folgenden Elemente sind Mitglieder der Substitutions Gruppe "Search":</span><span class="sxs-lookup"><span data-stu-id="2c9c2-133">The following elements are members of the SearchExpression substitution group:</span></span>
  
- [<span data-ttu-id="2c9c2-134">Exists</span><span class="sxs-lookup"><span data-stu-id="2c9c2-134">Exists</span></span>](exists.md)
    
- [<span data-ttu-id="2c9c2-135">Schließt</span><span class="sxs-lookup"><span data-stu-id="2c9c2-135">Excludes</span></span>](excludes.md)
    
- [<span data-ttu-id="2c9c2-136">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="2c9c2-136">IsEqualTo</span></span>](isequalto.md)
    
- [<span data-ttu-id="2c9c2-137">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="2c9c2-137">IsNotEqualTo</span></span>](isnotequalto.md)
    
- [<span data-ttu-id="2c9c2-138">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="2c9c2-138">IsGreaterThan</span></span>](isgreaterthan.md)
    
- [<span data-ttu-id="2c9c2-139">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="2c9c2-139">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md)
    
- [<span data-ttu-id="2c9c2-140">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="2c9c2-140">IsLessThan</span></span>](islessthan.md)
    
- [<span data-ttu-id="2c9c2-141">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="2c9c2-141">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md)
    
- [<span data-ttu-id="2c9c2-142">Contains</span><span class="sxs-lookup"><span data-stu-id="2c9c2-142">Contains</span></span>](contains.md)
    
- [<span data-ttu-id="2c9c2-143">not</span><span class="sxs-lookup"><span data-stu-id="2c9c2-143">Not</span></span>](not.md)
    
- [<span data-ttu-id="2c9c2-144">Und</span><span class="sxs-lookup"><span data-stu-id="2c9c2-144">And</span></span>](and.md)
    
- [<span data-ttu-id="2c9c2-145">- oder -</span><span class="sxs-lookup"><span data-stu-id="2c9c2-145">Or</span></span>](or.md)
    
<span data-ttu-id="2c9c2-146">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2c9c2-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c9c2-147">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2c9c2-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c9c2-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c9c2-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c9c2-149">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2c9c2-149">Schema Name</span></span>  <br/> |<span data-ttu-id="2c9c2-150">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2c9c2-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="2c9c2-151">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2c9c2-151">Validation File</span></span>  <br/> |<span data-ttu-id="2c9c2-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2c9c2-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c9c2-153">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2c9c2-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="2c9c2-154">False</span><span class="sxs-lookup"><span data-stu-id="2c9c2-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c9c2-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c9c2-155">See also</span></span>



- [<span data-ttu-id="2c9c2-156">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2c9c2-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

