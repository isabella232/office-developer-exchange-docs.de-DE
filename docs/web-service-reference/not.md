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
description: Das not-Element stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.
ms.openlocfilehash: 84c64a6d9d39f260d416fc32e4e5f5fcdef027e5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466717"
---
# <a name="not"></a><span data-ttu-id="b22e5-103">Nicht</span><span class="sxs-lookup"><span data-stu-id="b22e5-103">Not</span></span>

<span data-ttu-id="b22e5-104">Das **Not** -Element stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="b22e5-104">The **Not** element represents a search expression that negates the Boolean value of the search expression that it contains.</span></span> 
  
```xml
<Not>
   <SearchExpression/>
</Not>
```

 <span data-ttu-id="b22e5-105">**NotType**</span><span class="sxs-lookup"><span data-stu-id="b22e5-105">**NotType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b22e5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b22e5-106">Attributes and elements</span></span>

<span data-ttu-id="b22e5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b22e5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b22e5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b22e5-108">Attributes</span></span>

<span data-ttu-id="b22e5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b22e5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b22e5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b22e5-110">Child elements</span></span>

|<span data-ttu-id="b22e5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b22e5-111">**Element**</span></span>|<span data-ttu-id="b22e5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b22e5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b22e5-113">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="b22e5-113">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="b22e5-114">Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar.</span><span class="sxs-lookup"><span data-stu-id="b22e5-114">Represents the base class for expressions within a restriction.</span></span> <br/><br/><span data-ttu-id="b22e5-115">Eines der folgenden Elemente muss **durch das Search** -Element ersetzt werden:</span><span class="sxs-lookup"><span data-stu-id="b22e5-115">One of the following elements must be substituted for the **SearchExpression** element:</span></span> <br/> <br/><span data-ttu-id="b22e5-116">- [Existiert](exists.md)</span><span class="sxs-lookup"><span data-stu-id="b22e5-116">- [Exists](exists.md)</span></span> <br/><span data-ttu-id="b22e5-117">- [Schließt](excludes.md)</span><span class="sxs-lookup"><span data-stu-id="b22e5-117">- [Excludes](excludes.md)</span></span> <br/><span data-ttu-id="b22e5-118">- [IsEqualTo](isequalto.md)</span><span class="sxs-lookup"><span data-stu-id="b22e5-118">- [IsEqualTo](isequalto.md)</span></span> <br/><span data-ttu-id="b22e5-119">- [IsNotEqualTo](isnotequalto.md)</span><span class="sxs-lookup"><span data-stu-id="b22e5-119">- [IsNotEqualTo](isnotequalto.md)</span></span> <br/><span data-ttu-id="b22e5-120">- [Isgreaterthan](isgreaterthan.md)</span><span class="sxs-lookup"><span data-stu-id="b22e5-120">- [IsGreaterThan](isgreaterthan.md)</span></span> <br/><span data-ttu-id="b22e5-121">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="b22e5-121">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span></span> <br/><span data-ttu-id="b22e5-122">- [IsLessThan](islessthan.md)</span><span class="sxs-lookup"><span data-stu-id="b22e5-122">- [IsLessThan](islessthan.md)</span></span> <br/><span data-ttu-id="b22e5-123">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="b22e5-123">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span></span> <br/><span data-ttu-id="b22e5-124">- [Enthält](contains.md)</span><span class="sxs-lookup"><span data-stu-id="b22e5-124">- [Contains](contains.md)</span></span> <br/><span data-ttu-id="b22e5-125">- **Nicht**</span><span class="sxs-lookup"><span data-stu-id="b22e5-125">- **Not**</span></span> <br/><span data-ttu-id="b22e5-126">- [Und](and.md)</span><span class="sxs-lookup"><span data-stu-id="b22e5-126">- [And](and.md)</span></span> <br/><span data-ttu-id="b22e5-127">- [Oder](or.md)</span><span class="sxs-lookup"><span data-stu-id="b22e5-127">- [Or](or.md)</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b22e5-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b22e5-128">Parent elements</span></span>

|<span data-ttu-id="b22e5-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="b22e5-129">**Element**</span></span>|<span data-ttu-id="b22e5-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b22e5-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b22e5-131">Restriction</span><span class="sxs-lookup"><span data-stu-id="b22e5-131">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="b22e5-132">Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b22e5-132">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|<span data-ttu-id="b22e5-133">**Not**</span><span class="sxs-lookup"><span data-stu-id="b22e5-133">**Not**</span></span> <br/> |<span data-ttu-id="b22e5-134">Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="b22e5-134">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="b22e5-135">Und</span><span class="sxs-lookup"><span data-stu-id="b22e5-135">And</span></span>](and.md) <br/> |<span data-ttu-id="b22e5-136">Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert **und** eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="b22e5-136">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="b22e5-137">Das Ergebnis der **and-** Operation ist **true** , wenn alle im **and-** Element enthaltenen Suchausdrücke **true**sind.</span><span class="sxs-lookup"><span data-stu-id="b22e5-137">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="b22e5-138">- oder -</span><span class="sxs-lookup"><span data-stu-id="b22e5-138">Or</span></span>](or.md) <br/> |<span data-ttu-id="b22e5-139">Stellt einen Suchausdruck dar, der eine logische **or** -Operation für den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="b22e5-139">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="b22e5-140">**Oder** gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b22e5-140">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="b22e5-141">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b22e5-141">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b22e5-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b22e5-142">Remarks</span></span>

<span data-ttu-id="b22e5-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b22e5-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b22e5-144">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b22e5-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b22e5-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="b22e5-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b22e5-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b22e5-146">Schema Name</span></span>  <br/> |<span data-ttu-id="b22e5-147">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b22e5-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="b22e5-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b22e5-148">Validation File</span></span>  <br/> |<span data-ttu-id="b22e5-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b22e5-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b22e5-150">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b22e5-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="b22e5-151">False</span><span class="sxs-lookup"><span data-stu-id="b22e5-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b22e5-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b22e5-152">See also</span></span>

- [<span data-ttu-id="b22e5-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b22e5-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

