---
title: Exists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exists
api_type:
- schema
ms.assetid: 55d568bd-8dbc-4d50-b9d7-54b74a54d4b5
description: Exists-Element stellt einen Search-Ausdruck, der gibt true zurück, wenn die angegebene Eigenschaft vorhanden ist für ein Element.
ms.openlocfilehash: d30f4b505afcac32afbfeaf2289c964ba145668e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758310"
---
# <a name="exists"></a><span data-ttu-id="ed017-103">Exists</span><span class="sxs-lookup"><span data-stu-id="ed017-103">Exists</span></span>

<span data-ttu-id="ed017-104">**Exists** -Element stellt einen Search-Ausdruck, der **true** zurückgibt, wenn die angegebene Eigenschaft vorhanden ist für ein Element.</span><span class="sxs-lookup"><span data-stu-id="ed017-104">The **Exists** element represents a search expression that returns **true** if the supplied property exists on an item.</span></span> 
  
```xml
<Exists>
   <Path/>
</Exists>
```

 <span data-ttu-id="ed017-105">**ExistsType**</span><span class="sxs-lookup"><span data-stu-id="ed017-105">**ExistsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed017-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ed017-106">Attributes and elements</span></span>

<span data-ttu-id="ed017-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ed017-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed017-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ed017-108">Attributes</span></span>

<span data-ttu-id="ed017-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ed017-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed017-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed017-110">Child elements</span></span>

|<span data-ttu-id="ed017-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ed017-111">**Element**</span></span>|<span data-ttu-id="ed017-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ed017-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed017-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="ed017-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="ed017-114">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ed017-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="ed017-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ed017-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="ed017-116">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ed017-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="ed017-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ed017-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="ed017-118">MAPI-Eigenschaften identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ed017-118">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ed017-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed017-119">Parent elements</span></span>

|<span data-ttu-id="ed017-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="ed017-120">**Element**</span></span>|<span data-ttu-id="ed017-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ed017-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed017-122">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="ed017-122">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="ed017-123">Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed017-123">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="ed017-124">not</span><span class="sxs-lookup"><span data-stu-id="ed017-124">Not</span></span>](not.md) <br/> |<span data-ttu-id="ed017-125">Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="ed017-125">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="ed017-126">Und</span><span class="sxs-lookup"><span data-stu-id="ed017-126">And</span></span>](and.md) <br/> |<span data-ttu-id="ed017-127">Stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="ed017-127">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="ed017-128">Das Ergebnis der And-Operation ist **true** , wenn **alle enthaltenen das And Suchausdrücke zutreffen**.</span><span class="sxs-lookup"><span data-stu-id="ed017-128">The result of the And operation is **true** if all the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="ed017-129">- oder -</span><span class="sxs-lookup"><span data-stu-id="ed017-129">Or</span></span>](or.md) <br/> |<span data-ttu-id="ed017-130">Stellt ein Suchbegriff, der ein logisches OR Suchbegriffs durchführt, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="ed017-130">Represents a search expression that performs a logical OR on the search expression that it contains.</span></span> <span data-ttu-id="ed017-131">[Oder](or.md) gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ed017-131">[Or](or.md) will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed017-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed017-132">Remarks</span></span>

<span data-ttu-id="ed017-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ed017-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed017-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ed017-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed017-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed017-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ed017-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ed017-136">Schema Name</span></span>  <br/> |<span data-ttu-id="ed017-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ed017-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="ed017-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ed017-138">Validation File</span></span>  <br/> |<span data-ttu-id="ed017-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ed017-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ed017-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ed017-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed017-141">False</span><span class="sxs-lookup"><span data-stu-id="ed017-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed017-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed017-142">See also</span></span>



- [<span data-ttu-id="ed017-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ed017-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

