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
ms.openlocfilehash: 5de1528dda6d58ea772d050e709c0720e389fae6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465212"
---
# <a name="value"></a><span data-ttu-id="d0c71-103">Wert</span><span class="sxs-lookup"><span data-stu-id="d0c71-103">Value</span></span>

<span data-ttu-id="d0c71-104">Das **value** -Element enthält den Wert einer erweiterten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d0c71-104">The **Value** element contains the value of an extended property.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="d0c71-105">**String**</span><span class="sxs-lookup"><span data-stu-id="d0c71-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d0c71-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d0c71-106">Attributes and elements</span></span>

<span data-ttu-id="d0c71-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d0c71-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0c71-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d0c71-108">Attributes</span></span>

<span data-ttu-id="d0c71-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0c71-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0c71-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0c71-110">Child elements</span></span>

<span data-ttu-id="d0c71-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0c71-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d0c71-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0c71-112">Parent elements</span></span>

|<span data-ttu-id="d0c71-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0c71-113">**Element**</span></span>|<span data-ttu-id="d0c71-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0c71-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0c71-115">Werte</span><span class="sxs-lookup"><span data-stu-id="d0c71-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="d0c71-116">Enthält eine Auflistung von Werten für eine erweiterte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d0c71-116">Contains a collection of values for an extended property.</span></span>  <br/> |
|[<span data-ttu-id="d0c71-117">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="d0c71-117">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="d0c71-118">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d0c71-118">Identifies extended properties on folders and items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d0c71-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="d0c71-119">Text value</span></span>

<span data-ttu-id="d0c71-120">Der Textwert muss mit dem Typ kompatibel sein, der durch das PropertyType-Attribut des ExtendedFieldURI-Attributs angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d0c71-120">The text value must be compatible with the type that is indicated by the PropertyType attribute of the ExtendedFieldURI.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0c71-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0c71-121">Remarks</span></span>

<span data-ttu-id="d0c71-122">Ein **value** -Element kann sowohl in einzelnen als auch in mehrwertigen Extended Property-Instanzen vorkommen.</span><span class="sxs-lookup"><span data-stu-id="d0c71-122">A **Value** element can occur in both single and multivalued extended property instances.</span></span> <span data-ttu-id="d0c71-123">Für Instanzen mit einer einwertigen Instanz ist es als direkt untergeordnetes Element des [Extended](extendedproperty.md) -Elements vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d0c71-123">For single-valued instances, it exists as a direct child of the [ExtendedProperty](extendedproperty.md) element.</span></span> <span data-ttu-id="d0c71-124">Für mehrwertige Instanz ist es als direkt untergeordnetes Element der **Values** -Auflistung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d0c71-124">For multivalued instance, it exists as a direct child of the **Values** collection.</span></span> 
  
<span data-ttu-id="d0c71-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d0c71-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0c71-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d0c71-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0c71-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0c71-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0c71-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d0c71-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d0c71-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d0c71-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="d0c71-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d0c71-130">Validation File</span></span>  <br/> |<span data-ttu-id="d0c71-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d0c71-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0c71-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d0c71-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0c71-133">False</span><span class="sxs-lookup"><span data-stu-id="d0c71-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0c71-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0c71-134">See also</span></span>

- [<span data-ttu-id="d0c71-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d0c71-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

