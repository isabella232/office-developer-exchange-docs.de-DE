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
ms.openlocfilehash: f05be466d05b13f8f362afb5fc0552653a532475
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458810"
---
# <a name="bitmask"></a><span data-ttu-id="a314c-103">Bitmaske</span><span class="sxs-lookup"><span data-stu-id="a314c-103">Bitmask</span></span>

<span data-ttu-id="a314c-104">Das **Bitmask**-Element steht eine Hexadezimal- oder Dezimalmaske dar, die während eines [Schließt](excludes.md)-Einschränkungsvorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a314c-104">The **Bitmask** element represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> 
  
```xml
<Bitmask Value="" />
```

<span data-ttu-id="a314c-105">**ExcludesValueType**</span><span class="sxs-lookup"><span data-stu-id="a314c-105">**ExcludesValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a314c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a314c-106">Attributes and elements</span></span>

<span data-ttu-id="a314c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a314c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a314c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a314c-108">Attributes</span></span>

|<span data-ttu-id="a314c-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a314c-109">**Attribute**</span></span>|<span data-ttu-id="a314c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a314c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a314c-111">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a314c-111">**Value**</span></span> | <span data-ttu-id="a314c-112">Stellt eine Dezimal- bzw. Hexadezimal-Bitmaske dar.</span><span class="sxs-lookup"><span data-stu-id="a314c-112">Represents a decimal or hexadecimal bitmask.</span></span> <span data-ttu-id="a314c-113">Der Wert wird durch den folgenden regulären Ausdruck dargestellt:</span><span class="sxs-lookup"><span data-stu-id="a314c-113">The value is represented by the following regular expression:</span></span><br/><span data-ttu-id="a314c-114">`((0x|0X)[0-9A-Fa-f]*)|([0-9]*)`.</span><span class="sxs-lookup"><span data-stu-id="a314c-114">`((0x|0X)[0-9A-Fa-f]*)|([0-9]*)`.</span></span><br/><br/><span data-ttu-id="a314c-115">Nachfolgend sehen Sie Beispiele für Hexadezimalwerte für dieses Attribut:</span><span class="sxs-lookup"><span data-stu-id="a314c-115">The following are examples of hexadecimal values for this attribute:</span></span><br/><span data-ttu-id="a314c-116">- 0x12AF</span><span class="sxs-lookup"><span data-stu-id="a314c-116">- 0x12AF</span></span><br/><span data-ttu-id="a314c-117">- 0X334AE</span><span class="sxs-lookup"><span data-stu-id="a314c-117">- 0X334AE</span></span><br/><br/><span data-ttu-id="a314c-118">Nachfolgend sehen Sie Beispiele für Dezimalwerte für dieses Attribut:</span><span class="sxs-lookup"><span data-stu-id="a314c-118">The following are examples of decimal values for this attribute:</span></span><br/><span data-ttu-id="a314c-119">- 10</span><span class="sxs-lookup"><span data-stu-id="a314c-119">- 10</span></span><br/><span data-ttu-id="a314c-120">- 255</span><span class="sxs-lookup"><span data-stu-id="a314c-120">- 255</span></span><br/><span data-ttu-id="a314c-121">- 4562</span><span class="sxs-lookup"><span data-stu-id="a314c-121">- 4562</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="a314c-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a314c-122">Child elements</span></span>

<span data-ttu-id="a314c-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="a314c-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a314c-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a314c-124">Parent elements</span></span>

|<span data-ttu-id="a314c-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="a314c-125">**Element**</span></span>|<span data-ttu-id="a314c-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a314c-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a314c-127">Schließt</span><span class="sxs-lookup"><span data-stu-id="a314c-127">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="a314c-128">Führt eine bitweise Maske der Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="a314c-128">Performs a bitwise mask of the properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a314c-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a314c-129">Remarks</span></span>

<span data-ttu-id="a314c-p102">Hexadezimale Werte müssen die Präfix 0x oder 0X aufweisen. Wenn diese Präfix nicht vorhanden ist, wird davon ausgegangen, dass der Wert eine Dezimalzahl sein.</span><span class="sxs-lookup"><span data-stu-id="a314c-p102">Hexadecimal values must have a prefix of either 0x or 0X. If this prefix does not exist, the value is assumed to be a decimal number.</span></span>
  
<span data-ttu-id="a314c-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a314c-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a314c-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a314c-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a314c-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="a314c-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a314c-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a314c-135">Schema name</span></span>  <br/> |<span data-ttu-id="a314c-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a314c-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="a314c-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a314c-137">Validation file</span></span>  <br/> |<span data-ttu-id="a314c-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a314c-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a314c-139">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a314c-139">Can be empty</span></span>  <br/> |<span data-ttu-id="a314c-140">False</span><span class="sxs-lookup"><span data-stu-id="a314c-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a314c-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a314c-141">See also</span></span>

- [<span data-ttu-id="a314c-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a314c-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

