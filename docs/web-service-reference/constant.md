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
description: Das constant-Element identifiziert einen konstanten Wert in einer Einschränkung.
ms.openlocfilehash: 6cb2eaa4227a8fd0985e8ff5a15d647c3bb1cd6a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461555"
---
# <a name="constant"></a><span data-ttu-id="466a7-103">Konstante</span><span class="sxs-lookup"><span data-stu-id="466a7-103">Constant</span></span>

<span data-ttu-id="466a7-104">Das **Constant** -Element identifiziert einen konstanten Wert in einer Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="466a7-104">The **Constant** element identifies a constant value in a restriction.</span></span> 
  
```xml
<Constant Value="" />
```

 <span data-ttu-id="466a7-105">**ConstantValueType**</span><span class="sxs-lookup"><span data-stu-id="466a7-105">**ConstantValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="466a7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="466a7-106">Attributes and elements</span></span>

<span data-ttu-id="466a7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="466a7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="466a7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="466a7-108">Attributes</span></span>

|<span data-ttu-id="466a7-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="466a7-109">**Attribute**</span></span>|<span data-ttu-id="466a7-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="466a7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="466a7-111">**Wert**</span><span class="sxs-lookup"><span data-stu-id="466a7-111">**Value**</span></span> <br/> |<span data-ttu-id="466a7-112">Gibt den Wert an, der in der Einschränkung verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="466a7-112">Specifies the value to compare in the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="466a7-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="466a7-113">Child elements</span></span>

<span data-ttu-id="466a7-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="466a7-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="466a7-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="466a7-115">Parent elements</span></span>

|<span data-ttu-id="466a7-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="466a7-116">**Element**</span></span>|<span data-ttu-id="466a7-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="466a7-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="466a7-118">Enthält</span><span class="sxs-lookup"><span data-stu-id="466a7-118">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="466a7-119">Stellt einen Suchausdruck dar, der bestimmt, ob eine angegebene Eigenschaft den angegebenen konstanten Zeichenfolgewert enthält.</span><span class="sxs-lookup"><span data-stu-id="466a7-119">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="466a7-120">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="466a7-120">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="466a7-121">Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="466a7-121">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="466a7-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="466a7-122">Remarks</span></span>

<span data-ttu-id="466a7-123">Der Zeichenfolgenwert im **value** -Attribut muss in den Typ Coercible werden, den Sie vergleichen möchten.</span><span class="sxs-lookup"><span data-stu-id="466a7-123">The string value in the **Value** attribute must be coercible into the type you are trying to compare against.</span></span> <span data-ttu-id="466a7-124">Wenn Sie beispielsweise eine Date/Time-Eigenschaft mit einem konstanten Wert vergleichen, muss der Zeichenfolgenwert ein Datum/eine Uhrzeit darstellen.</span><span class="sxs-lookup"><span data-stu-id="466a7-124">For example, if you are comparing a date/time property against a constant value, the string value must represent a date/time.</span></span> 
  
<span data-ttu-id="466a7-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="466a7-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="466a7-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="466a7-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="466a7-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="466a7-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="466a7-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="466a7-128">Schema Name</span></span>  <br/> |<span data-ttu-id="466a7-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="466a7-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="466a7-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="466a7-130">Validation File</span></span>  <br/> |<span data-ttu-id="466a7-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="466a7-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="466a7-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="466a7-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="466a7-133">False</span><span class="sxs-lookup"><span data-stu-id="466a7-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="466a7-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="466a7-134">See also</span></span>



- [<span data-ttu-id="466a7-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="466a7-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

