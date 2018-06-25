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
description: Die Einschränkungselement stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.
ms.openlocfilehash: 6b5702696db29910ae476a370bf362fe6a036ae7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831213"
---
# <a name="restriction"></a><span data-ttu-id="562d9-103">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="562d9-103">Restriction</span></span>

<span data-ttu-id="562d9-104">**Die Einschränkungselement** stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="562d9-104">The **Restriction** element represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span> 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 <span data-ttu-id="562d9-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="562d9-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="562d9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="562d9-106">Attributes and elements</span></span>

<span data-ttu-id="562d9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="562d9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="562d9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="562d9-108">Attributes</span></span>

<span data-ttu-id="562d9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="562d9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="562d9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="562d9-110">Child elements</span></span>

|<span data-ttu-id="562d9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="562d9-111">**Element**</span></span>|<span data-ttu-id="562d9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="562d9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="562d9-113">Und</span><span class="sxs-lookup"><span data-stu-id="562d9-113">And</span></span>](and.md) <br/> |<span data-ttu-id="562d9-114">Stellt einen Search-Ausdruck, der Sie einen booleschen **AND** -Vorgang zwischen zwei oder mehr Suchausdrücke ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="562d9-114">Represents a search expression that enables you to perform a Boolean **AND** operation between two or more search expressions.</span></span>  <br/> |
|[<span data-ttu-id="562d9-115">Enthält</span><span class="sxs-lookup"><span data-stu-id="562d9-115">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="562d9-116">Stellt einen Suchausdruck dar, der bestimmt, ob eine angegebene Eigenschaft den angegebenen konstanten Zeichenfolgewert enthält.</span><span class="sxs-lookup"><span data-stu-id="562d9-116">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="562d9-117">Schließt</span><span class="sxs-lookup"><span data-stu-id="562d9-117">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="562d9-118">Führt eine bitweise Maske der Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="562d9-118">Performs a bitwise mask of the properties.</span></span>  <br/> |
|[<span data-ttu-id="562d9-119">Exists</span><span class="sxs-lookup"><span data-stu-id="562d9-119">Exists</span></span>](exists.md) <br/> |<span data-ttu-id="562d9-120">Stellt einen Suchausdruck dar, der **true** zurückgibt, wenn die angegebene Eigenschaft zu einem Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="562d9-120">Represents a search expression that returns **true** if the supplied property exists on an item.</span></span>  <br/> |
|[<span data-ttu-id="562d9-121">"IsEqualTo"</span><span class="sxs-lookup"><span data-stu-id="562d9-121">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="562d9-122">Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** ausgibt, wenn sie gleich sind.</span><span class="sxs-lookup"><span data-stu-id="562d9-122">Represents a search expression that compares a property with either a constant value or another property and evaluates to **true** if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="562d9-123">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="562d9-123">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="562d9-124">Stellt einen Search-Ausdruck, der eine Eigenschaft mit einem konstanten Wert oder einen anderen-Eigenschaft und gibt **true** verglichen, wenn die erste Eigenschaft größer ist als der Wert oder -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="562d9-124">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="562d9-125">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="562d9-125">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="562d9-126">Stellt einen Search-Ausdruck, der vergleicht eine Eigenschaft mit einen konstanten Wert oder einen anderen-Eigenschaft und gibt **true,** Wenn die erste Eigenschaft größer als oder gleich dem Wert oder-Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="562d9-126">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="562d9-127">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="562d9-127">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="562d9-128">Stellt einen Search-Ausdruck, der eine Eigenschaft mit einem konstanten Wert oder einen anderen-Eigenschaft und gibt **true** vergleicht, ob die erste Eigenschaft kleiner als der Wert oder -Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="562d9-128">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="562d9-129">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="562d9-129">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="562d9-130">Stellt einen Search-Ausdruck, der eine Eigenschaft mit einem konstanten Wert oder einen anderen-Eigenschaft und gibt **true** vergleicht, ob die erste Eigenschaft kleiner oder gleich dem Wert oder-Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="562d9-130">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="562d9-131">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="562d9-131">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="562d9-132">Stellt einen Suchausdruck dar, der einer Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die Wert nicht identisch sind.</span><span class="sxs-lookup"><span data-stu-id="562d9-132">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.</span></span>  <br/> |
|[<span data-ttu-id="562d9-133">not</span><span class="sxs-lookup"><span data-stu-id="562d9-133">Not</span></span>](not.md) <br/> |<span data-ttu-id="562d9-134">Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert darin enthaltenen dar.</span><span class="sxs-lookup"><span data-stu-id="562d9-134">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="562d9-135">- oder -</span><span class="sxs-lookup"><span data-stu-id="562d9-135">Or</span></span>](or.md) <br/> |<span data-ttu-id="562d9-136">Stellt einen Search-Ausdruck, der eine logische **OR** -Operation für den Suchbegriff durchführt darin enthaltenen dar.</span><span class="sxs-lookup"><span data-stu-id="562d9-136">Represents a search expression that performs a logical **OR** operation on the search expression it contains.</span></span> <span data-ttu-id="562d9-137">Das Element **oder** gibt **true** zurück, wenn ein untergeordnetes Element **true**zurück.</span><span class="sxs-lookup"><span data-stu-id="562d9-137">The **Or** element will return **true** if any of its children return **true**.</span></span>  <br/> |
|[<span data-ttu-id="562d9-138">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="562d9-138">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="562d9-139">Stellt das ersetzte Element innerhalb einer Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="562d9-139">Represents the substituted element within a restriction.</span></span> <span data-ttu-id="562d9-140">Dieses Element wird in einem XML-Instanzendokument nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="562d9-140">This element is not used in an XML instance document.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="562d9-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="562d9-141">Parent elements</span></span>

|<span data-ttu-id="562d9-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="562d9-142">**Element**</span></span>|<span data-ttu-id="562d9-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="562d9-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="562d9-144">FindFolder</span><span class="sxs-lookup"><span data-stu-id="562d9-144">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="562d9-145">Definiert eine Anforderung zum Ordner in einem Postfach zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="562d9-145">Defines a request to identify folders in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="562d9-146">FindItem</span><span class="sxs-lookup"><span data-stu-id="562d9-146">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="562d9-147">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="562d9-147">Defines a request to find items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="562d9-148">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="562d9-148">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="562d9-149">Stellt die Parameter, die einen Suchordner definieren.</span><span class="sxs-lookup"><span data-stu-id="562d9-149">Represents the parameters that define a search folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="562d9-150">Hinweise</span><span class="sxs-lookup"><span data-stu-id="562d9-150">Remarks</span></span>

<span data-ttu-id="562d9-151">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="562d9-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="562d9-152">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="562d9-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="562d9-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="562d9-153">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="562d9-154">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="562d9-154">Schema Name</span></span>  <br/> |<span data-ttu-id="562d9-155">Schematypen</span><span class="sxs-lookup"><span data-stu-id="562d9-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="562d9-156">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="562d9-156">Validation File</span></span>  <br/> |<span data-ttu-id="562d9-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="562d9-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="562d9-158">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="562d9-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="562d9-159">False</span><span class="sxs-lookup"><span data-stu-id="562d9-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="562d9-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="562d9-160">See also</span></span>



- [<span data-ttu-id="562d9-161">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="562d9-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

