---
title: 'Oder:'
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
description: Das or-Element stellt einen Suchausdruck dar, der eine logische oder den darin enthaltenen Suchausdruck ausführt. Oder gibt true zurück, wenn eines der untergeordneten Elemente true zurückgibt. Oder muss mindestens zwei untergeordnete Elemente aufweisen.
ms.openlocfilehash: 9bc676da5bbaad64f11f6717fb487c2e9bcf2d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462479"
---
# <a name="or"></a><span data-ttu-id="f7fb1-105">Oder:</span><span class="sxs-lookup"><span data-stu-id="f7fb1-105">Or</span></span>

<span data-ttu-id="f7fb1-106">Das **or** -Element stellt einen Suchausdruck dar, der eine logische **oder** den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-106">The **Or** element represents a search expression that performs a logical **OR** on the search expression that it contains.</span></span> <span data-ttu-id="f7fb1-107">**Oder** gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-107">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="f7fb1-108">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-108">**Or** must have two or more children.</span></span> 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 <span data-ttu-id="f7fb1-109">**Odertyp**</span><span class="sxs-lookup"><span data-stu-id="f7fb1-109">**OrType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7fb1-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f7fb1-110">Attributes and elements</span></span>

<span data-ttu-id="f7fb1-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7fb1-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="f7fb1-112">Attributes</span></span>

<span data-ttu-id="f7fb1-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7fb1-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7fb1-114">Child elements</span></span>

|<span data-ttu-id="f7fb1-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="f7fb1-115">**Element**</span></span>|<span data-ttu-id="f7fb1-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7fb1-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7fb1-117">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="f7fb1-117">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="f7fb1-118">Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-118">Represents the base class for expressions within a restriction.</span></span> <br/><br/><span data-ttu-id="f7fb1-119">Eines der folgenden Elemente muss **durch das Search** -Element ersetzt werden:</span><span class="sxs-lookup"><span data-stu-id="f7fb1-119">One of the following elements must be substituted for the **SearchExpression** element:</span></span> <br/> <br/><span data-ttu-id="f7fb1-120">- [Existiert](exists.md)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-120">- [Exists](exists.md)</span></span> <br/><span data-ttu-id="f7fb1-121">- [Schließt](excludes.md)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-121">- [Excludes](excludes.md)</span></span> <br/><span data-ttu-id="f7fb1-122">- [IsEqualTo](isequalto.md)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-122">- [IsEqualTo](isequalto.md)</span></span> <br/><span data-ttu-id="f7fb1-123">- [IsNotEqualTo](isnotequalto.md)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-123">- [IsNotEqualTo](isnotequalto.md)</span></span> <br/><span data-ttu-id="f7fb1-124">- [Isgreaterthan](isgreaterthan.md)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-124">- [IsGreaterThan](isgreaterthan.md)</span></span> <br/><span data-ttu-id="f7fb1-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span></span> <br/><span data-ttu-id="f7fb1-126">- [IsLessThan](islessthan.md)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-126">- [IsLessThan](islessthan.md)</span></span> <br/><span data-ttu-id="f7fb1-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span></span> <br/><span data-ttu-id="f7fb1-128">- [Enthält](contains.md)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-128">- [Contains](contains.md)</span></span> <br/><span data-ttu-id="f7fb1-129">- [Nicht](not.md)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-129">- [Not](not.md)</span></span> <br/><span data-ttu-id="f7fb1-130">- [Und](and.md)</span><span class="sxs-lookup"><span data-stu-id="f7fb1-130">- [And](and.md)</span></span> <br/><span data-ttu-id="f7fb1-131">- **Oder**</span><span class="sxs-lookup"><span data-stu-id="f7fb1-131">- **Or**</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f7fb1-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7fb1-132">Parent elements</span></span>

|<span data-ttu-id="f7fb1-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="f7fb1-133">**Element**</span></span>|<span data-ttu-id="f7fb1-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7fb1-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7fb1-135">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="f7fb1-135">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="f7fb1-136">Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-136">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="f7fb1-137">not</span><span class="sxs-lookup"><span data-stu-id="f7fb1-137">Not</span></span>](not.md) <br/> |<span data-ttu-id="f7fb1-138">Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-138">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="f7fb1-139">Und</span><span class="sxs-lookup"><span data-stu-id="f7fb1-139">And</span></span>](and.md) <br/> |<span data-ttu-id="f7fb1-140">Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert **und** eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-140">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="f7fb1-141">Das Ergebnis der **and-** Operation ist **true** , wenn alle im **and-** Element enthaltenen Suchausdrücke **true**sind.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-141">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|<span data-ttu-id="f7fb1-142">**- oder -**</span><span class="sxs-lookup"><span data-stu-id="f7fb1-142">**Or**</span></span> <br/> |<span data-ttu-id="f7fb1-143">Stellt einen Suchausdruck dar, der eine logische **or** -Operation für den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-143">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="f7fb1-144">**Oder** gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-144">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="f7fb1-145">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-145">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7fb1-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7fb1-146">Remarks</span></span>

<span data-ttu-id="f7fb1-147">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7fb1-148">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f7fb1-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7fb1-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7fb1-149">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f7fb1-150">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f7fb1-150">Schema Name</span></span>  <br/> |<span data-ttu-id="f7fb1-151">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f7fb1-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="f7fb1-152">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f7fb1-152">Validation File</span></span>  <br/> |<span data-ttu-id="f7fb1-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f7fb1-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f7fb1-154">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f7fb1-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7fb1-155">False</span><span class="sxs-lookup"><span data-stu-id="f7fb1-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7fb1-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7fb1-156">See also</span></span>

- [<span data-ttu-id="f7fb1-157">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f7fb1-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

