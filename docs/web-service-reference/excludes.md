---
title: Schließt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Excludes
api_type:
- schema
ms.assetid: bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1
description: Das excludes-Element führt eine bitweise Maske der angegebenen Eigenschaft und eines angegebenen Werts aus.
ms.openlocfilehash: d5fcd8b86b454aa731bd43974b5b7d674fe76ed6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530614"
---
# <a name="excludes"></a><span data-ttu-id="e8a73-103">Schließt</span><span class="sxs-lookup"><span data-stu-id="e8a73-103">Excludes</span></span>

<span data-ttu-id="e8a73-104">Das **excludes** -Element führt eine bitweise Maske der angegebenen Eigenschaft und eines angegebenen Werts aus.</span><span class="sxs-lookup"><span data-stu-id="e8a73-104">The **Excludes** element performs a bitwise mask of the specified property and a supplied value.</span></span> 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <ExtendedFieldURI/> 
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <IndexedFieldURI/> 
   <Bitmask/>
</Excludes>
```

<span data-ttu-id="e8a73-105">**ExcludesType**</span><span class="sxs-lookup"><span data-stu-id="e8a73-105">**ExcludesType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e8a73-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e8a73-106">Attributes and elements</span></span>

<span data-ttu-id="e8a73-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e8a73-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8a73-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e8a73-108">Attributes</span></span>

<span data-ttu-id="e8a73-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e8a73-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8a73-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8a73-110">Child elements</span></span>

|<span data-ttu-id="e8a73-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8a73-111">**Element**</span></span>|<span data-ttu-id="e8a73-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8a73-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8a73-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="e8a73-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="e8a73-114">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="e8a73-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="e8a73-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e8a73-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="e8a73-116">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="e8a73-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="e8a73-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e8a73-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="e8a73-118">Identifiziert MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e8a73-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="e8a73-119">Bitmaske</span><span class="sxs-lookup"><span data-stu-id="e8a73-119">Bitmask</span></span>](bitmask.md) <br/> |<span data-ttu-id="e8a73-120">Stellt eine Hexadezimal-oder Dezimal Maske dar, die während eines [Exclude](excludes.md) -Einschränkungs Vorgangs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8a73-120">Represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> <span data-ttu-id="e8a73-121">Wenn die Bitmaske eine Hexadezimalzahl darstellt, muss Ihr das Präfix 0x oder 0x vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e8a73-121">If the bitmask represents a hexadecimal number, it must be prefixed by 0x or 0X.</span></span> <span data-ttu-id="e8a73-122">Andernfalls wird Sie als Dezimalzahl betrachtet.</span><span class="sxs-lookup"><span data-stu-id="e8a73-122">Otherwise, it will be considered a decimal number.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e8a73-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8a73-123">Parent elements</span></span>

|<span data-ttu-id="e8a73-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8a73-124">**Element**</span></span>|<span data-ttu-id="e8a73-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8a73-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8a73-126">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="e8a73-126">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="e8a73-127">Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8a73-127">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="e8a73-128">not</span><span class="sxs-lookup"><span data-stu-id="e8a73-128">Not</span></span>](not.md) <br/> |<span data-ttu-id="e8a73-129">Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="e8a73-129">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="e8a73-130">Und</span><span class="sxs-lookup"><span data-stu-id="e8a73-130">And</span></span>](and.md) <br/> |<span data-ttu-id="e8a73-131">Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert und eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="e8a73-131">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="e8a73-132">Das Ergebnis der and-Operation ist **true** , wenn alle in der enthaltenen Suchausdrücke auf **true**festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e8a73-132">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="e8a73-133">- oder -</span><span class="sxs-lookup"><span data-stu-id="e8a73-133">Or</span></span>](or.md) <br/> |<span data-ttu-id="e8a73-134">Stellt einen Suchausdruck dar, der eine logische OR-Anweisung für den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="e8a73-134">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="e8a73-135">Das [or](or.md) -Element gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e8a73-135">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8a73-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8a73-136">Remarks</span></span>

<span data-ttu-id="e8a73-137">" **Excludes** " wird in " **true** " aufgelöst, wenn ein-und-Vorgang, der für Folgendes ausgeführt wird, in 0 aufgelöst wird:</span><span class="sxs-lookup"><span data-stu-id="e8a73-137">**Excludes** will resolve to **true** if an AND operation performed on the following resolves to 0:</span></span> 
  
1. <span data-ttu-id="e8a73-138">Der bitweise Wert für die Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e8a73-138">The bitwise value for the property</span></span>
    
2. <span data-ttu-id="e8a73-139">Der Wert der Bitmaske für die Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e8a73-139">The bitmask value for the property</span></span>
    
<span data-ttu-id="e8a73-140">**Excludes** können nur auf eine Eigenschaft angewendet werden, die einen ganzzahligen Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="e8a73-140">**Excludes** can only be applied to a property that has an integer value.</span></span> <span data-ttu-id="e8a73-141">Wenn der Eigenschaftentyp etwas anderes als eine ganze Zahl ist, wird ein Fehlercode von **ErrorUnsupportedPathForQuery** in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e8a73-141">If the property type is anything other than an integer, an error code of **ErrorUnsupportedPathForQuery** is returned in the response.</span></span> 
  
<span data-ttu-id="e8a73-142">Sie können den Reverse-Vorgang durchführen, indem Sie Not (excludes) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e8a73-142">You can perform the reverse operation by calling Not(Excludes).</span></span>
  
<span data-ttu-id="e8a73-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e8a73-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8a73-144">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e8a73-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8a73-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8a73-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e8a73-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e8a73-146">Schema Name</span></span>  <br/> |<span data-ttu-id="e8a73-147">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e8a73-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="e8a73-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e8a73-148">Validation File</span></span>  <br/> |<span data-ttu-id="e8a73-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e8a73-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e8a73-150">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e8a73-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="e8a73-151">False</span><span class="sxs-lookup"><span data-stu-id="e8a73-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8a73-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8a73-152">See also</span></span>

- [<span data-ttu-id="e8a73-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e8a73-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

