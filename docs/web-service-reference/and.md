---
title: Und
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- And
api_type:
- schema
ms.assetid: 790246c2-37ad-49a8-91b9-6186d743b011
description: Das and-Element stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert und eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können. Das Ergebnis der and-Operation ist true, wenn alle im and-Element enthaltenen Suchausdrücke true sind.
ms.openlocfilehash: f5239f19c2b5a931eefa9ff4a9dd8ed9d775bae2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464721"
---
# <a name="and"></a><span data-ttu-id="5f3de-104">Und</span><span class="sxs-lookup"><span data-stu-id="5f3de-104">And</span></span>

<span data-ttu-id="5f3de-105">Das **and-** Element stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert **und** eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="5f3de-105">The **And** element represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="5f3de-106">Das Ergebnis der **and-** Operation ist **true** , wenn alle im **and-** Element enthaltenen Suchausdrücke **true**sind.</span><span class="sxs-lookup"><span data-stu-id="5f3de-106">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>
  
```xml
<And>
   <SearchExpression/>
   <SearchExpression/>
</And>
```

 <span data-ttu-id="5f3de-107">**AndType**</span><span class="sxs-lookup"><span data-stu-id="5f3de-107">**AndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f3de-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5f3de-108">Attributes and elements</span></span>

<span data-ttu-id="5f3de-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5f3de-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f3de-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="5f3de-110">Attributes</span></span>

<span data-ttu-id="5f3de-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f3de-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f3de-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f3de-112">Child elements</span></span>

|<span data-ttu-id="5f3de-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f3de-113">**Element**</span></span>|<span data-ttu-id="5f3de-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f3de-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f3de-115">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="5f3de-115">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="5f3de-116">Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar.</span><span class="sxs-lookup"><span data-stu-id="5f3de-116">Represents the base class for expressions within a restriction.</span></span> <span data-ttu-id="5f3de-117">In einem und-Vorgang müssen mindestens zwei Suchausdrücke vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="5f3de-117">There must be two or more search expressions in an And operation.</span></span><br/><br/>  <span data-ttu-id="5f3de-118">Eines der folgenden Elemente muss **durch das Search** -Element ersetzt werden:</span><span class="sxs-lookup"><span data-stu-id="5f3de-118">One of the following elements must be substituted for the **SearchExpression** element:</span></span><ul><li> [<span data-ttu-id="5f3de-119">Exists</span><span class="sxs-lookup"><span data-stu-id="5f3de-119">Exists</span></span>](exists.md)</li><li>[<span data-ttu-id="5f3de-120">Schließt</span><span class="sxs-lookup"><span data-stu-id="5f3de-120">Excludes</span></span>](excludes.md)</li><li>[<span data-ttu-id="5f3de-121">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="5f3de-121">IsEqualTo</span></span>](isequalto.md)</li><li>[<span data-ttu-id="5f3de-122">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="5f3de-122">IsNotEqualTo</span></span>](isnotequalto.md)</li><li>[<span data-ttu-id="5f3de-123">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="5f3de-123">IsGreaterThan</span></span>](isgreaterthan.md)</li><li>[<span data-ttu-id="5f3de-124">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="5f3de-124">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md)</li><li>[<span data-ttu-id="5f3de-125">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="5f3de-125">IsLessThan</span></span>](islessthan.md)</li><li>[<span data-ttu-id="5f3de-126">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="5f3de-126">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md)</li><li>[<span data-ttu-id="5f3de-127">Contains</span><span class="sxs-lookup"><span data-stu-id="5f3de-127">Contains</span></span>](contains.md)</li><li>[<span data-ttu-id="5f3de-128">not</span><span class="sxs-lookup"><span data-stu-id="5f3de-128">Not</span></span>](not.md)</li><li><span data-ttu-id="5f3de-129">**Und**</span><span class="sxs-lookup"><span data-stu-id="5f3de-129">**And**</span></span></li><li>[<span data-ttu-id="5f3de-130">- oder -</span><span class="sxs-lookup"><span data-stu-id="5f3de-130">Or</span></span>](or.md) </li></ul> |
   
### <a name="parent-elements"></a><span data-ttu-id="5f3de-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f3de-131">Parent elements</span></span>

|<span data-ttu-id="5f3de-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f3de-132">**Element**</span></span>|<span data-ttu-id="5f3de-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f3de-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f3de-134">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="5f3de-134">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="5f3de-135">Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f3de-135">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="5f3de-136">not</span><span class="sxs-lookup"><span data-stu-id="5f3de-136">Not</span></span>](not.md) <br/> |<span data-ttu-id="5f3de-137">Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="5f3de-137">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|<span data-ttu-id="5f3de-138">**Und**</span><span class="sxs-lookup"><span data-stu-id="5f3de-138">**And**</span></span> <br/> |<span data-ttu-id="5f3de-139">Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert **und** eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="5f3de-139">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="5f3de-140">Das Ergebnis der **and-** Operation ist **true** , wenn alle im **and-** Element enthaltenen Suchausdrücke **true**sind.</span><span class="sxs-lookup"><span data-stu-id="5f3de-140">The result of the **AND** operation is **true** if all of the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="5f3de-141">- oder -</span><span class="sxs-lookup"><span data-stu-id="5f3de-141">Or</span></span>](or.md) <br/> |<span data-ttu-id="5f3de-142">Stellt einen Suchausdruck dar, der eine logische **or** -Operation für den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="5f3de-142">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="5f3de-143">**Oder** gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5f3de-143">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="5f3de-144">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5f3de-144">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f3de-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f3de-145">Remarks</span></span>

<span data-ttu-id="5f3de-146">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5f3de-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f3de-147">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5f3de-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f3de-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f3de-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f3de-149">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5f3de-149">Schema Name</span></span>  <br/> |<span data-ttu-id="5f3de-150">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5f3de-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f3de-151">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5f3de-151">Validation File</span></span>  <br/> |<span data-ttu-id="5f3de-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f3de-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f3de-153">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5f3de-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="5f3de-154">False</span><span class="sxs-lookup"><span data-stu-id="5f3de-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f3de-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f3de-155">See also</span></span>

- [<span data-ttu-id="5f3de-156">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5f3de-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

