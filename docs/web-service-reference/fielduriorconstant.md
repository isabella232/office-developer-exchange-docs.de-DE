---
title: FieldURIOrConstant
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FieldURIOrConstant
api_type:
- schema
ms.assetid: 89d7a87e-7c93-49b8-83ec-8798e08c1052
description: Das FieldURIOrConstant-Element stellt entweder eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.
ms.openlocfilehash: 8b5cb888a3bd2026b15e38fc8c005ab5ef5a2b11
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461226"
---
# <a name="fielduriorconstant"></a><span data-ttu-id="53df7-103">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="53df7-103">FieldURIOrConstant</span></span>

<span data-ttu-id="53df7-104">Das **FieldURIOrConstant** -Element stellt entweder eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="53df7-104">The **FieldURIOrConstant** element represents either a property or a constant value to be used when comparing with another property.</span></span> 
  
```xml
<FieldURIOrConstant>
   <Constant/>
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
    <IndexedFieldURI/> 
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
   <FieldURI/>
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
   <ExtendedFieldURI/> 
</FieldURIOrConstant>
```

<span data-ttu-id="53df7-105">**FieldURIOrConstantType**</span><span class="sxs-lookup"><span data-stu-id="53df7-105">**FieldURIOrConstantType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="53df7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="53df7-106">Attributes and elements</span></span>

<span data-ttu-id="53df7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="53df7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53df7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="53df7-108">Attributes</span></span>

<span data-ttu-id="53df7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="53df7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53df7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53df7-110">Child elements</span></span>

|<span data-ttu-id="53df7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="53df7-111">**Element**</span></span>|<span data-ttu-id="53df7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53df7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53df7-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="53df7-113">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="53df7-114">Gibt einen konstanten Wert in einer Einschränkung an.</span><span class="sxs-lookup"><span data-stu-id="53df7-114">Identifies a constant value in a restriction.</span></span>  <br/> |
|[<span data-ttu-id="53df7-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="53df7-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="53df7-116">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="53df7-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="53df7-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="53df7-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="53df7-118">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="53df7-118">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="53df7-119">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="53df7-119">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="53df7-120">Identifiziert MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="53df7-120">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="53df7-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53df7-121">Parent elements</span></span>

|<span data-ttu-id="53df7-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="53df7-122">**Element**</span></span>|<span data-ttu-id="53df7-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53df7-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53df7-124">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="53df7-124">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="53df7-125">Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und true ausgibt, wenn sie gleich sind.</span><span class="sxs-lookup"><span data-stu-id="53df7-125">Represents a search expression that compares a property with either a constant value or another property and evaluates to true if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="53df7-126">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="53df7-126">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="53df7-127">Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und true zurückgibt, wenn die erste Eigenschaft größer ist.</span><span class="sxs-lookup"><span data-stu-id="53df7-127">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater.</span></span>  <br/> |
|[<span data-ttu-id="53df7-128">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="53df7-128">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="53df7-129">Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und true zurückgibt, wenn die erste Eigenschaft größer oder gleich dem zweiten Wert oder der Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="53df7-129">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="53df7-130">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="53df7-130">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="53df7-131">Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und true zurückgibt, wenn die erste Eigenschaft kleiner als der zweite Wert oder die Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="53df7-131">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="53df7-132">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="53df7-132">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="53df7-133">Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und true zurückgibt, wenn die erste Eigenschaft kleiner oder gleich dem zweiten Wert oder der Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="53df7-133">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="53df7-134">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="53df7-134">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="53df7-135">Stellt einen Suchausdruck dar, der einer Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und true zurückgibt, wenn die Wert nicht identisch sind.</span><span class="sxs-lookup"><span data-stu-id="53df7-135">Represents a search expression that compares a property with either a constant value or another property and returns true if the values are not the same.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53df7-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53df7-136">Remarks</span></span>

<span data-ttu-id="53df7-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="53df7-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="53df7-138">Beispiel</span><span class="sxs-lookup"><span data-stu-id="53df7-138">Example</span></span>

<span data-ttu-id="53df7-139">Das folgende XML-Beispiel zeigt das FieldURIOrConstant-Element, das sowohl mit einer Konstanten als auch mit einem Feld-URI verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53df7-139">The following XML example shows the FieldURIOrConstant element used with both a constant and field URI.</span></span>
  
```xml
<Restriction>
  <Or xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
    <IsEqualTo>
      <FieldURI FieldURI="item:DateTimeCreated"/>
      <FieldURIOrConstant>
        <FieldURI FieldURI="item:DateTimeReceived"/>
      </FieldURIOrConstant>
    </IsEqualTo>
    <IsEqualTo>
      <FieldURI FieldURI="item:Subject"/>
      <FieldURIOrConstant>
        <Constant Value="Here is a test message"/>
      </FieldURIOrConstant>
    </IsEqualTo>
  </Or>
</Restriction>
```

## <a name="element-information"></a><span data-ttu-id="53df7-140">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="53df7-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53df7-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="53df7-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="53df7-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="53df7-142">Schema Name</span></span>  <br/> |<span data-ttu-id="53df7-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="53df7-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="53df7-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="53df7-144">Validation File</span></span>  <br/> |<span data-ttu-id="53df7-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="53df7-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="53df7-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="53df7-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="53df7-147">False</span><span class="sxs-lookup"><span data-stu-id="53df7-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53df7-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53df7-148">See also</span></span>

- [<span data-ttu-id="53df7-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="53df7-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

