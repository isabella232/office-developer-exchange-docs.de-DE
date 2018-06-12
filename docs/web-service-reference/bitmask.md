---
title: Bitmaske
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Bitmask
api_type:
- schema
ms.assetid: fc7eeac2-555f-4cbc-8b48-26d9ed67748a
description: Das Bitmask-Element steht eine Hexadezimal- oder Dezimalmaske dar, die während eines Schließt-Einschränkungsvorgangs verwendet wird.
ms.openlocfilehash: 86c8c61f22d8d620a9139280b2a43ed7fec4727d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757459"
---
# <a name="bitmask"></a><span data-ttu-id="bd3b9-103">Bitmaske</span><span class="sxs-lookup"><span data-stu-id="bd3b9-103">Bitmask</span></span>

<span data-ttu-id="bd3b9-104">Das **Bitmask**-Element steht eine Hexadezimal- oder Dezimalmaske dar, die während eines [Schließt](excludes.md)-Einschränkungsvorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-104">The **Bitmask** element represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> 
  
```xml
<Bitmask Value="" />
```

<span data-ttu-id="bd3b9-105">**ExcludesValueType**</span><span class="sxs-lookup"><span data-stu-id="bd3b9-105">**ExcludesValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bd3b9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bd3b9-106">Attributes and elements</span></span>

<span data-ttu-id="bd3b9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd3b9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bd3b9-108">Attributes</span></span>

|<span data-ttu-id="bd3b9-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bd3b9-109">**Attribute**</span></span>|<span data-ttu-id="bd3b9-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bd3b9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bd3b9-111">**Value**</span><span class="sxs-lookup"><span data-stu-id="bd3b9-111">**Value**</span></span> | <span data-ttu-id="bd3b9-112">Stellt eine Bitmaske dezimale oder hexadezimale.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-112">Represents a decimal or hexadecimal bitmask.</span></span> <span data-ttu-id="bd3b9-113">Der Wert wird durch den folgenden regulären Ausdruck dargestellt:</span><span class="sxs-lookup"><span data-stu-id="bd3b9-113">The value is represented by the following regular expression:</span></span><br/><span data-ttu-id="bd3b9-114">' ((0 X</span><span class="sxs-lookup"><span data-stu-id="bd3b9-114">\`((0x</span></span>|<span data-ttu-id="bd3b9-115">0x)[0-9a-FA-f]\*)</span><span class="sxs-lookup"><span data-stu-id="bd3b9-115">0X)[0-9A-Fa-f]\*)</span></span>|<span data-ttu-id="bd3b9-116">([0-9] \*) ".</span><span class="sxs-lookup"><span data-stu-id="bd3b9-116">([0-9]\*)\`.</span></span><br/><br/><span data-ttu-id="bd3b9-117">Nachfolgend sehen Sie Beispiele für Hexadezimalwerte für dieses Attribut:</span><span class="sxs-lookup"><span data-stu-id="bd3b9-117">The following are examples of hexadecimal values for this attribute:</span></span><br/><span data-ttu-id="bd3b9-118">-0x12AF</span><span class="sxs-lookup"><span data-stu-id="bd3b9-118">- 0x12AF</span></span><br/><span data-ttu-id="bd3b9-119">-0X334AE</span><span class="sxs-lookup"><span data-stu-id="bd3b9-119">- 0X334AE</span></span><br/><br/><span data-ttu-id="bd3b9-120">Nachfolgend sehen Sie Beispiele für Dezimalwerte für dieses Attribut:</span><span class="sxs-lookup"><span data-stu-id="bd3b9-120">The following are examples of decimal values for this attribute:</span></span><br/><span data-ttu-id="bd3b9-121">-10</span><span class="sxs-lookup"><span data-stu-id="bd3b9-121">- 10</span></span><br/><span data-ttu-id="bd3b9-122">-255</span><span class="sxs-lookup"><span data-stu-id="bd3b9-122">- 255</span></span><br/><span data-ttu-id="bd3b9-123">-4562</span><span class="sxs-lookup"><span data-stu-id="bd3b9-123">- 4562</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="bd3b9-124">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd3b9-124">Child elements</span></span>

<span data-ttu-id="bd3b9-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-125">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bd3b9-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd3b9-126">Parent elements</span></span>

|<span data-ttu-id="bd3b9-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd3b9-127">**Element**</span></span>|<span data-ttu-id="bd3b9-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bd3b9-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd3b9-129">Schließt</span><span class="sxs-lookup"><span data-stu-id="bd3b9-129">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="bd3b9-130">Führt eine bitweise Maske der Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-130">Performs a bitwise mask of the properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd3b9-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bd3b9-131">Remarks</span></span>

<span data-ttu-id="bd3b9-p102">Hexadezimale Werte müssen die Präfix 0x oder 0X aufweisen. Wenn diese Präfix nicht vorhanden ist, wird davon ausgegangen, dass der Wert eine Dezimalzahl sein.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-p102">Hexadecimal values must have a prefix of either 0x or 0X. If this prefix does not exist, the value is assumed to be a decimal number.</span></span>
  
<span data-ttu-id="bd3b9-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd3b9-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bd3b9-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd3b9-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd3b9-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bd3b9-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bd3b9-137">Schema name</span></span>  <br/> |<span data-ttu-id="bd3b9-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bd3b9-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="bd3b9-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bd3b9-139">Validation file</span></span>  <br/> |<span data-ttu-id="bd3b9-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bd3b9-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bd3b9-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="bd3b9-141">Can be empty</span></span>  <br/> |<span data-ttu-id="bd3b9-142">False</span><span class="sxs-lookup"><span data-stu-id="bd3b9-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd3b9-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd3b9-143">See also</span></span>

- [<span data-ttu-id="bd3b9-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bd3b9-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

