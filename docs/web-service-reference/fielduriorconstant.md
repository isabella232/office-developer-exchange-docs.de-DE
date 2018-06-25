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
description: Das Element FieldURIOrConstant stellt eine Eigenschaft oder einen konstanten Wert beim Vergleich mit einer anderen Eigenschaft verwendet werden.
ms.openlocfilehash: 5195feec2a314d9ec15dc4a25a7a014aded1696a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758419"
---
# <a name="fielduriorconstant"></a><span data-ttu-id="672c1-103">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="672c1-103">FieldURIOrConstant</span></span>

<span data-ttu-id="672c1-104">Das Element **FieldURIOrConstant** stellt eine Eigenschaft oder einen konstanten Wert beim Vergleich mit einer anderen Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="672c1-104">The **FieldURIOrConstant** element represents either a property or a constant value to be used when comparing with another property.</span></span> 
  
```xml
<FieldURIOrConstant>
   <Constant/>
</FieldURIOrConstant>
```

 <span data-ttu-id="672c1-105">**FieldURIOrConstantType**</span><span class="sxs-lookup"><span data-stu-id="672c1-105">**FieldURIOrConstantType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="672c1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="672c1-106">Attributes and elements</span></span>

<span data-ttu-id="672c1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="672c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="672c1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="672c1-108">Attributes</span></span>

<span data-ttu-id="672c1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="672c1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="672c1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="672c1-110">Child elements</span></span>

|<span data-ttu-id="672c1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="672c1-111">**Element**</span></span>|<span data-ttu-id="672c1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="672c1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="672c1-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="672c1-113">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="672c1-114">Gibt einen konstanten Wert in einer Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="672c1-114">Identifies a constant value in a restriction.</span></span>  <br/> |
|[<span data-ttu-id="672c1-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="672c1-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="672c1-116">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="672c1-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="672c1-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="672c1-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="672c1-118">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="672c1-118">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="672c1-119">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="672c1-119">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="672c1-120">MAPI-Eigenschaften identifiziert.</span><span class="sxs-lookup"><span data-stu-id="672c1-120">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="672c1-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="672c1-121">Parent elements</span></span>

|<span data-ttu-id="672c1-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="672c1-122">**Element**</span></span>|<span data-ttu-id="672c1-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="672c1-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="672c1-124">"IsEqualTo"</span><span class="sxs-lookup"><span data-stu-id="672c1-124">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="672c1-125">Stellt einen Search-Ausdruck, der mit entweder einen konstanten Wert einer Eigenschaft oder eine andere Eigenschaft vergleicht und wird zu True ausgewertet, falls diese gleich sind.</span><span class="sxs-lookup"><span data-stu-id="672c1-125">Represents a search expression that compares a property with either a constant value or another property and evaluates to true if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="672c1-126">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="672c1-126">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="672c1-127">Stellt einen Search-Ausdruck, der mit entweder einen konstanten Wert einer Eigenschaft oder eine andere Eigenschaft vergleicht und gibt true, wenn die erste Eigenschaft größer ist.</span><span class="sxs-lookup"><span data-stu-id="672c1-127">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater.</span></span>  <br/> |
|[<span data-ttu-id="672c1-128">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="672c1-128">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="672c1-129">Stellt einen Search-Ausdruck, der mit entweder einen konstanten Wert einer Eigenschaft oder eine andere Eigenschaft vergleicht und gibt true, wenn die erste Eigenschaft größer als oder gleich dem zweiten Wert oder-Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="672c1-129">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="672c1-130">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="672c1-130">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="672c1-131">Stellt einen Search-Ausdruck, der vergleicht eine Eigenschaft mit entweder einen konstanten Wert oder eine andere Eigenschaft und gibt true, wenn die erste Eigenschaft kleiner als der zweite Wert oder -Eigenschaft ist zurück.</span><span class="sxs-lookup"><span data-stu-id="672c1-131">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="672c1-132">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="672c1-132">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="672c1-133">Stellt einen Search-Ausdruck, der vergleicht eine Eigenschaft mit entweder einen konstanten Wert oder eine andere Eigenschaft und gibt true, wenn die erste Eigenschaft kleiner oder gleich dem zweiten Wert oder-Eigenschaft ist zurück.</span><span class="sxs-lookup"><span data-stu-id="672c1-133">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="672c1-134">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="672c1-134">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="672c1-135">Stellt einen Search-Ausdruck, der vergleicht eine Eigenschaft mit entweder einen konstanten Wert oder eine andere Eigenschaft und gibt true, wenn die Werte nicht identisch sind.</span><span class="sxs-lookup"><span data-stu-id="672c1-135">Represents a search expression that compares a property with either a constant value or another property and returns true if the values are not the same.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="672c1-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="672c1-136">Remarks</span></span>

<span data-ttu-id="672c1-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="672c1-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="672c1-138">Beispiel</span><span class="sxs-lookup"><span data-stu-id="672c1-138">Example</span></span>

<span data-ttu-id="672c1-139">Das folgende XML-Beispiel zeigt das FieldURIOrConstant-Element mit einer Konstante und die URI-Feld verwendet.</span><span class="sxs-lookup"><span data-stu-id="672c1-139">The following XML example shows the FieldURIOrConstant element used with both a constant and field URI.</span></span>
  
```
[xml]
<Restriction>
  <Or xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="672c1-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="672c1-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="672c1-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="672c1-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="672c1-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="672c1-142">Schema Name</span></span>  <br/> |<span data-ttu-id="672c1-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="672c1-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="672c1-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="672c1-144">Validation File</span></span>  <br/> |<span data-ttu-id="672c1-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="672c1-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="672c1-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="672c1-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="672c1-147">False</span><span class="sxs-lookup"><span data-stu-id="672c1-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="672c1-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="672c1-148">See also</span></span>



- [<span data-ttu-id="672c1-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="672c1-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

