---
title: Einschränkung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Restriction
api_type:
- schema
ms.assetid: 77f19014-d112-4999-8e83-ecc32a117a73
description: Das restriction-Element stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.
ms.openlocfilehash: 6037ba15417d67d393ca70f3edf2248749c396e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465289"
---
# <a name="restriction"></a><span data-ttu-id="4ae1a-103">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="4ae1a-103">Restriction</span></span>

<span data-ttu-id="4ae1a-104">Das **Restriction** -Element stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-104">The **Restriction** element represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span> 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 <span data-ttu-id="4ae1a-105">**Restrictiontype**</span><span class="sxs-lookup"><span data-stu-id="4ae1a-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ae1a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4ae1a-106">Attributes and elements</span></span>

<span data-ttu-id="4ae1a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ae1a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ae1a-108">Attributes</span></span>

<span data-ttu-id="4ae1a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ae1a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ae1a-110">Child elements</span></span>

|<span data-ttu-id="4ae1a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ae1a-111">**Element**</span></span>|<span data-ttu-id="4ae1a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ae1a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ae1a-113">Und</span><span class="sxs-lookup"><span data-stu-id="4ae1a-113">And</span></span>](and.md) <br/> |<span data-ttu-id="4ae1a-114">Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert **und** eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-114">Represents a search expression that enables you to perform a Boolean **AND** operation between two or more search expressions.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-115">Enthält</span><span class="sxs-lookup"><span data-stu-id="4ae1a-115">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="4ae1a-116">Stellt einen Suchausdruck dar, der bestimmt, ob eine angegebene Eigenschaft den angegebenen konstanten Zeichenfolgewert enthält.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-116">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-117">Schließt</span><span class="sxs-lookup"><span data-stu-id="4ae1a-117">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="4ae1a-118">Führt eine bitweise Maske der Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-118">Performs a bitwise mask of the properties.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-119">Exists</span><span class="sxs-lookup"><span data-stu-id="4ae1a-119">Exists</span></span>](exists.md) <br/> |<span data-ttu-id="4ae1a-120">Stellt einen Suchausdruck dar, der **true** zurückgibt, wenn die angegebene Eigenschaft zu einem Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-120">Represents a search expression that returns **true** if the supplied property exists on an item.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-121">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="4ae1a-121">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="4ae1a-122">Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** ausgibt, wenn sie gleich sind.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-122">Represents a search expression that compares a property with either a constant value or another property and evaluates to **true** if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-123">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="4ae1a-123">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="4ae1a-124">Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft größer als der Wert oder die Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-124">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-125">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="4ae1a-125">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="4ae1a-126">Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft größer oder gleich dem Wert oder der Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-126">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-127">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="4ae1a-127">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="4ae1a-128">Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft kleiner als der Wert oder die Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-128">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-129">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="4ae1a-129">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="4ae1a-130">Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft kleiner als oder gleich dem Wert oder der Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-130">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-131">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="4ae1a-131">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="4ae1a-132">Stellt einen Suchausdruck dar, der einer Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die Wert nicht identisch sind.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-132">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-133">not</span><span class="sxs-lookup"><span data-stu-id="4ae1a-133">Not</span></span>](not.md) <br/> |<span data-ttu-id="4ae1a-134">Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-134">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-135">- oder -</span><span class="sxs-lookup"><span data-stu-id="4ae1a-135">Or</span></span>](or.md) <br/> |<span data-ttu-id="4ae1a-136">Stellt einen Suchausdruck dar, der eine logische **or** -Operation für den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-136">Represents a search expression that performs a logical **OR** operation on the search expression it contains.</span></span> <span data-ttu-id="4ae1a-137">Das **or** -Element gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-137">The **Or** element will return **true** if any of its children return **true**.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-138">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="4ae1a-138">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="4ae1a-139">Stellt das ersetzte Element innerhalb einer Einschränkung dar.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-139">Represents the substituted element within a restriction.</span></span> <span data-ttu-id="4ae1a-140">Dieses Element wird in einem XML-Instanzendokument nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-140">This element is not used in an XML instance document.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ae1a-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ae1a-141">Parent elements</span></span>

|<span data-ttu-id="4ae1a-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ae1a-142">**Element**</span></span>|<span data-ttu-id="4ae1a-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ae1a-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ae1a-144">FindFolder</span><span class="sxs-lookup"><span data-stu-id="4ae1a-144">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="4ae1a-145">Definiert eine Anforderung zum Identifizieren von Ordnern in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-145">Defines a request to identify folders in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-146">FindItem</span><span class="sxs-lookup"><span data-stu-id="4ae1a-146">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="4ae1a-147">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-147">Defines a request to find items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4ae1a-148">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="4ae1a-148">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="4ae1a-149">Stellt die Parameter dar, die einen Suchordner definieren.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-149">Represents the parameters that define a search folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ae1a-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ae1a-150">Remarks</span></span>

<span data-ttu-id="4ae1a-151">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4ae1a-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ae1a-152">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4ae1a-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ae1a-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ae1a-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4ae1a-154">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4ae1a-154">Schema Name</span></span>  <br/> |<span data-ttu-id="4ae1a-155">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4ae1a-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="4ae1a-156">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4ae1a-156">Validation File</span></span>  <br/> |<span data-ttu-id="4ae1a-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4ae1a-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4ae1a-158">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4ae1a-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ae1a-159">False</span><span class="sxs-lookup"><span data-stu-id="4ae1a-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ae1a-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ae1a-160">See also</span></span>



- [<span data-ttu-id="4ae1a-161">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4ae1a-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

