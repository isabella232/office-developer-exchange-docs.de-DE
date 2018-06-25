---
title: Konstante
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Constant
api_type:
- schema
ms.assetid: 340af0cd-9f12-44ab-b8f1-21d107c8d0c9
description: Das Konstante Element identifiziert einen konstanten Wert in einer Einschränkung.
ms.openlocfilehash: 73912bc1981c5d54040f7c4a563ad805916fe721
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757605"
---
# <a name="constant"></a><span data-ttu-id="6fe47-103">Konstante</span><span class="sxs-lookup"><span data-stu-id="6fe47-103">Constant</span></span>

<span data-ttu-id="6fe47-104">Das **Konstanten** Element identifiziert einen konstanten Wert in einer Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="6fe47-104">The **Constant** element identifies a constant value in a restriction.</span></span> 
  
```xml
<Constant Value="" />
```

 <span data-ttu-id="6fe47-105">**ConstantValueType**</span><span class="sxs-lookup"><span data-stu-id="6fe47-105">**ConstantValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6fe47-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6fe47-106">Attributes and elements</span></span>

<span data-ttu-id="6fe47-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6fe47-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6fe47-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6fe47-108">Attributes</span></span>

|<span data-ttu-id="6fe47-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6fe47-109">**Attribute**</span></span>|<span data-ttu-id="6fe47-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fe47-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6fe47-111">**Value**</span><span class="sxs-lookup"><span data-stu-id="6fe47-111">**Value**</span></span> <br/> |<span data-ttu-id="6fe47-112">Gibt den Wert in die Einschränkung vergleichen.</span><span class="sxs-lookup"><span data-stu-id="6fe47-112">Specifies the value to compare in the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6fe47-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fe47-113">Child elements</span></span>

<span data-ttu-id="6fe47-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="6fe47-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6fe47-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fe47-115">Parent elements</span></span>

|<span data-ttu-id="6fe47-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="6fe47-116">**Element**</span></span>|<span data-ttu-id="6fe47-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fe47-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6fe47-118">Enthält</span><span class="sxs-lookup"><span data-stu-id="6fe47-118">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="6fe47-119">Stellt einen Suchausdruck dar, der bestimmt, ob eine angegebene Eigenschaft den angegebenen konstanten Zeichenfolgewert enthält.</span><span class="sxs-lookup"><span data-stu-id="6fe47-119">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="6fe47-120">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="6fe47-120">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="6fe47-121">Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fe47-121">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fe47-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6fe47-122">Remarks</span></span>

<span data-ttu-id="6fe47-123">Der String-Wert in das **Value** -Attribut muss in den Typ umgewandelt werden können, die mit der verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fe47-123">The string value in the **Value** attribute must be coercible into the type you are trying to compare against.</span></span> <span data-ttu-id="6fe47-124">Wenn Sie eine Datum/Uhrzeit-Eigenschaft mit einem konstanten Wert verglichen werden, muss der Zeichenfolgenwert beispielsweise einen Datum/Uhrzeit darstellen.</span><span class="sxs-lookup"><span data-stu-id="6fe47-124">For example, if you are comparing a date/time property against a constant value, the string value must represent a date/time.</span></span> 
  
<span data-ttu-id="6fe47-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6fe47-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6fe47-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6fe47-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fe47-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="6fe47-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6fe47-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6fe47-128">Schema Name</span></span>  <br/> |<span data-ttu-id="6fe47-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6fe47-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="6fe47-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6fe47-130">Validation File</span></span>  <br/> |<span data-ttu-id="6fe47-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6fe47-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6fe47-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6fe47-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="6fe47-133">False</span><span class="sxs-lookup"><span data-stu-id="6fe47-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6fe47-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fe47-134">See also</span></span>



- [<span data-ttu-id="6fe47-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6fe47-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

