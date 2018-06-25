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
description: Das Element ausgeschlossen führt eine bitweise Maske der angegebenen Eigenschaft und einen angegebenen Wert.
ms.openlocfilehash: 73e4eb782a4f54c113ea9a9b67fcf185a9028153
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758307"
---
# <a name="excludes"></a><span data-ttu-id="37f84-103">Schließt</span><span class="sxs-lookup"><span data-stu-id="37f84-103">Excludes</span></span>

<span data-ttu-id="37f84-104">Das Element **ausgeschlossen** führt eine bitweise Maske der angegebenen Eigenschaft und einen angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="37f84-104">The **Excludes** element performs a bitwise mask of the specified property and a supplied value.</span></span> 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

 <span data-ttu-id="37f84-105">**ExcludesType**</span><span class="sxs-lookup"><span data-stu-id="37f84-105">**ExcludesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37f84-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="37f84-106">Attributes and elements</span></span>

<span data-ttu-id="37f84-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="37f84-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37f84-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="37f84-108">Attributes</span></span>

<span data-ttu-id="37f84-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="37f84-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37f84-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37f84-110">Child elements</span></span>

|<span data-ttu-id="37f84-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="37f84-111">**Element**</span></span>|<span data-ttu-id="37f84-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37f84-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37f84-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="37f84-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="37f84-114">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="37f84-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="37f84-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="37f84-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="37f84-116">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="37f84-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="37f84-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="37f84-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="37f84-118">MAPI-Eigenschaften identifiziert.</span><span class="sxs-lookup"><span data-stu-id="37f84-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="37f84-119">Bitmaske</span><span class="sxs-lookup"><span data-stu-id="37f84-119">Bitmask</span></span>](bitmask.md) <br/> |<span data-ttu-id="37f84-120">Stellt eine hexadezimale oder decimal Maske, die während einer Einschränkung [ausgeschlossen](excludes.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37f84-120">Represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> <span data-ttu-id="37f84-121">Wenn die Bitmaske eine hexadezimale Zahl darstellt, muss es 0 X oder 0 X vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="37f84-121">If the bitmask represents a hexadecimal number, it must be prefixed by 0x or 0X.</span></span> <span data-ttu-id="37f84-122">Andernfalls wird er eine Dezimalzahl betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="37f84-122">Otherwise, it will be considered a decimal number.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="37f84-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37f84-123">Parent elements</span></span>

|<span data-ttu-id="37f84-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="37f84-124">**Element**</span></span>|<span data-ttu-id="37f84-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37f84-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37f84-126">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="37f84-126">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="37f84-127">Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37f84-127">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="37f84-128">not</span><span class="sxs-lookup"><span data-stu-id="37f84-128">Not</span></span>](not.md) <br/> |<span data-ttu-id="37f84-129">Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="37f84-129">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="37f84-130">Und</span><span class="sxs-lookup"><span data-stu-id="37f84-130">And</span></span>](and.md) <br/> |<span data-ttu-id="37f84-131">Stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="37f84-131">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="37f84-132">Das Ergebnis der And-Operation ist **true** , wenn **alle enthaltenen das And Search Ausdrücke zutreffen**.</span><span class="sxs-lookup"><span data-stu-id="37f84-132">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="37f84-133">- oder -</span><span class="sxs-lookup"><span data-stu-id="37f84-133">Or</span></span>](or.md) <br/> |<span data-ttu-id="37f84-134">Stellt einen Suche Ausdruck, der ein logisches OR Suchbegriffs durchführt darin enthaltenen dar.</span><span class="sxs-lookup"><span data-stu-id="37f84-134">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="37f84-135">Das Element [oder](or.md) gibt **true** zurück, wenn ein untergeordnetes Element **true**zurück.</span><span class="sxs-lookup"><span data-stu-id="37f84-135">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37f84-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="37f84-136">Remarks</span></span>

 <span data-ttu-id="37f84-137">**Ausgeschlossen** lösen auf **true fest,** Wenn eine AND-Operation für die folgenden auf 0 aufgelöst wird:</span><span class="sxs-lookup"><span data-stu-id="37f84-137">**Excludes** will resolve to **true** if an AND operation performed on the following resolves to 0:</span></span> 
  
1. <span data-ttu-id="37f84-138">Die bitweise Wert für die Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="37f84-138">The bitwise value for the property</span></span>
    
2. <span data-ttu-id="37f84-139">Der Bitmaskenwert für die-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="37f84-139">The bitmask value for the property</span></span>
    
 <span data-ttu-id="37f84-140">**Ausgeschlossen** kann nur auf eine Eigenschaft angewendet werden, die einen ganzzahligen Wert hat.</span><span class="sxs-lookup"><span data-stu-id="37f84-140">**Excludes** can only be applied to a property that has an integer value.</span></span> <span data-ttu-id="37f84-141">Wenn der Eigenschaftentyp etwas anderes als eine ganze Zahl ist, wird ein Fehlercode des **ErrorUnsupportedPathForQuery** in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37f84-141">If the property type is anything other than an integer, an error code of **ErrorUnsupportedPathForQuery** is returned in the response.</span></span> 
  
<span data-ttu-id="37f84-142">Sie können den umgekehrten Vorgang durch Aufrufen von Not(Excludes) ausführen.</span><span class="sxs-lookup"><span data-stu-id="37f84-142">You can perform the reverse operation by calling Not(Excludes).</span></span>
  
<span data-ttu-id="37f84-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="37f84-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37f84-144">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="37f84-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37f84-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="37f84-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="37f84-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="37f84-146">Schema Name</span></span>  <br/> |<span data-ttu-id="37f84-147">Schematypen</span><span class="sxs-lookup"><span data-stu-id="37f84-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="37f84-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="37f84-148">Validation File</span></span>  <br/> |<span data-ttu-id="37f84-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="37f84-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="37f84-150">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="37f84-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="37f84-151">False</span><span class="sxs-lookup"><span data-stu-id="37f84-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37f84-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37f84-152">See also</span></span>



- [<span data-ttu-id="37f84-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="37f84-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

