---
title: IsGreaterThan
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsGreaterThan
api_type:
- schema
ms.assetid: a6e9d462-cfa7-40ec-903e-128c95050352
description: Das isgreaterthan-Element stellt einen Suchausdruck dar, der eine Eigenschaft entweder mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und true zurückgibt, wenn die erste Eigenschaft größer ist.
ms.openlocfilehash: 52f2c1b84e4072649092637de091c0dbd8187032
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530043"
---
# <a name="isgreaterthan"></a><span data-ttu-id="96d0d-103">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="96d0d-103">IsGreaterThan</span></span>

<span data-ttu-id="96d0d-104">Das **isgreaterthan** -Element stellt einen Suchausdruck dar, der eine Eigenschaft entweder mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft größer ist.</span><span class="sxs-lookup"><span data-stu-id="96d0d-104">The **IsGreaterThan** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater.</span></span> 
  
```xml
<IsGreaterThan>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThan>
```

```xml
<IsGreaterThan>
   <IndexedFieldURI/> 
   <FieldURIOrConstant/>
</IsGreaterThan>
```

```xml
<IsGreaterThan>
   <ExtendedFieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThan>
```

<span data-ttu-id="96d0d-105">**Isgreaterthantype**</span><span class="sxs-lookup"><span data-stu-id="96d0d-105">**IsGreaterThanType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="96d0d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="96d0d-106">Attributes and elements</span></span>

<span data-ttu-id="96d0d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="96d0d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="96d0d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="96d0d-108">Attributes</span></span>

<span data-ttu-id="96d0d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="96d0d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="96d0d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="96d0d-110">Child elements</span></span>

|<span data-ttu-id="96d0d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="96d0d-111">**Element**</span></span>|<span data-ttu-id="96d0d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96d0d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96d0d-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="96d0d-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="96d0d-114">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="96d0d-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="96d0d-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="96d0d-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="96d0d-116">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="96d0d-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="96d0d-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="96d0d-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="96d0d-118">Identifiziert MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="96d0d-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="96d0d-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="96d0d-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="96d0d-120">Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96d0d-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="96d0d-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="96d0d-121">Parent elements</span></span>

|<span data-ttu-id="96d0d-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="96d0d-122">**Element**</span></span>|<span data-ttu-id="96d0d-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96d0d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96d0d-124">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="96d0d-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="96d0d-125">Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96d0d-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="96d0d-126">not</span><span class="sxs-lookup"><span data-stu-id="96d0d-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="96d0d-127">Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="96d0d-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="96d0d-128">Und</span><span class="sxs-lookup"><span data-stu-id="96d0d-128">And</span></span>](and.md) <br/> |<span data-ttu-id="96d0d-129">Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert und eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="96d0d-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="96d0d-130">Das Ergebnis der and-Operation ist **true** , wenn alle in der enthaltenen Suchausdrücke auf **true**festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="96d0d-130">The result of the And operation is **true** if all the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="96d0d-131">- oder -</span><span class="sxs-lookup"><span data-stu-id="96d0d-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="96d0d-132">Stellt einen Suchausdruck dar, der eine logische OR-Anweisung für den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="96d0d-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="96d0d-133">[Oder](or.md) gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="96d0d-133">[Or](or.md) will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96d0d-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96d0d-134">Remarks</span></span>

<span data-ttu-id="96d0d-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="96d0d-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="96d0d-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="96d0d-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96d0d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="96d0d-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="96d0d-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="96d0d-138">Schema Name</span></span>  <br/> |<span data-ttu-id="96d0d-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="96d0d-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="96d0d-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="96d0d-140">Validation File</span></span>  <br/> |<span data-ttu-id="96d0d-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="96d0d-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="96d0d-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="96d0d-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="96d0d-143">False</span><span class="sxs-lookup"><span data-stu-id="96d0d-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96d0d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96d0d-144">See also</span></span>

- [<span data-ttu-id="96d0d-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="96d0d-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

