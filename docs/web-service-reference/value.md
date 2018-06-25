---
title: Wert
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Value
api_type:
- schema
ms.assetid: 9a30cadd-909e-41b1-b4e9-291643dd89c6
description: Das Value-Element enthält den Wert einer erweiterten Eigenschaft.
ms.openlocfilehash: 4b8674d267b78f0384f9457e794e88ace8234826
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839496"
---
# <a name="value"></a><span data-ttu-id="ea96d-103">Wert</span><span class="sxs-lookup"><span data-stu-id="ea96d-103">Value</span></span>

<span data-ttu-id="ea96d-104">Das **Value** -Element enthält den Wert einer erweiterten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ea96d-104">The **Value** element contains the value of an extended property.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="ea96d-105">**String**</span><span class="sxs-lookup"><span data-stu-id="ea96d-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ea96d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ea96d-106">Attributes and elements</span></span>

<span data-ttu-id="ea96d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ea96d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ea96d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ea96d-108">Attributes</span></span>

<span data-ttu-id="ea96d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ea96d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ea96d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea96d-110">Child elements</span></span>

<span data-ttu-id="ea96d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ea96d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ea96d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea96d-112">Parent elements</span></span>

|<span data-ttu-id="ea96d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ea96d-113">**Element**</span></span>|<span data-ttu-id="ea96d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ea96d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea96d-115">Values</span><span class="sxs-lookup"><span data-stu-id="ea96d-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="ea96d-116">Enthält eine Auflistung von Werten für eine erweiterte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ea96d-116">Contains a collection of values for an extended property.</span></span>  <br/> |
|[<span data-ttu-id="ea96d-117">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="ea96d-117">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="ea96d-118">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ea96d-118">Identifies extended properties on folders and items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ea96d-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="ea96d-119">Text value</span></span>

<span data-ttu-id="ea96d-120">Der Textwert muss mit dem Typ kompatibel sein, die vom PropertyType-Attribut des der ExtendedFieldURI angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ea96d-120">The text value must be compatible with the type that is indicated by the PropertyType attribute of the ExtendedFieldURI.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ea96d-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ea96d-121">Remarks</span></span>

<span data-ttu-id="ea96d-122">**Value** -Element kann in beiden Fällen ein- und mehrwertige erweiterte Eigenschaft auftreten.</span><span class="sxs-lookup"><span data-stu-id="ea96d-122">A **Value** element can occur in both single and multivalued extended property instances.</span></span> <span data-ttu-id="ea96d-123">Für ein einwertiges Instanzen vorhanden ist es als direktes untergeordnetes Element des [ExtendedProperty](extendedproperty.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="ea96d-123">For single-valued instances, it exists as a direct child of the [ExtendedProperty](extendedproperty.md) element.</span></span> <span data-ttu-id="ea96d-124">Für mehrwertige Instanz ist es als ein direktes untergeordnetes Element der Auflistung **Werte** vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ea96d-124">For multivalued instance, it exists as a direct child of the **Values** collection.</span></span> 
  
<span data-ttu-id="ea96d-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ea96d-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ea96d-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ea96d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea96d-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea96d-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ea96d-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ea96d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="ea96d-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ea96d-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="ea96d-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ea96d-130">Validation File</span></span>  <br/> |<span data-ttu-id="ea96d-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ea96d-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ea96d-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ea96d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="ea96d-133">False</span><span class="sxs-lookup"><span data-stu-id="ea96d-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea96d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea96d-134">See also</span></span>

- [<span data-ttu-id="ea96d-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ea96d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

