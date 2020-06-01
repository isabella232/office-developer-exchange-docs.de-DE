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
description: Das EXISTS-Element stellt einen Suchausdruck dar, der true zurückgibt, wenn die angegebene Eigenschaft für ein Element vorhanden ist.
ms.openlocfilehash: b5e7a24c5214574ef385cd6ffca87ed5f861c188
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456948"
---
# <a name="exists"></a><span data-ttu-id="2c1ba-103">Exists</span><span class="sxs-lookup"><span data-stu-id="2c1ba-103">Exists</span></span>

<span data-ttu-id="2c1ba-104">Das **EXISTS** -Element stellt einen Suchausdruck dar, der **true** zurückgibt, wenn die angegebene Eigenschaft für ein Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-104">The **Exists** element represents a search expression that returns **true** if the supplied property exists on an item.</span></span> 
  
```xml
<Exists>
   <Path/>
</Exists>
```

 <span data-ttu-id="2c1ba-105">**Existtype**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-105">**ExistsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c1ba-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2c1ba-106">Attributes and elements</span></span>

<span data-ttu-id="2c1ba-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c1ba-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c1ba-108">Attributes</span></span>

<span data-ttu-id="2c1ba-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c1ba-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c1ba-110">Child elements</span></span>

|<span data-ttu-id="2c1ba-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-111">**Element**</span></span>|<span data-ttu-id="2c1ba-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c1ba-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="2c1ba-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="2c1ba-114">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="2c1ba-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="2c1ba-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="2c1ba-116">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="2c1ba-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="2c1ba-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="2c1ba-118">Identifiziert MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-118">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2c1ba-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c1ba-119">Parent elements</span></span>

|<span data-ttu-id="2c1ba-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-120">**Element**</span></span>|<span data-ttu-id="2c1ba-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c1ba-122">Restriction</span><span class="sxs-lookup"><span data-stu-id="2c1ba-122">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="2c1ba-123">Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-123">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="2c1ba-124">Not</span><span class="sxs-lookup"><span data-stu-id="2c1ba-124">Not</span></span>](not.md) <br/> |<span data-ttu-id="2c1ba-125">Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-125">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="2c1ba-126">Und</span><span class="sxs-lookup"><span data-stu-id="2c1ba-126">And</span></span>](and.md) <br/> |<span data-ttu-id="2c1ba-127">Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert und eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-127">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="2c1ba-128">Das Ergebnis der and-Operation ist **true** , wenn alle in der enthaltenen Suchausdrücke auf **true**festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-128">The result of the And operation is **true** if all the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="2c1ba-129">- oder -</span><span class="sxs-lookup"><span data-stu-id="2c1ba-129">Or</span></span>](or.md) <br/> |<span data-ttu-id="2c1ba-130">Stellt einen Suchausdruck dar, der einen logischen oder den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-130">Represents a search expression that performs a logical OR on the search expression that it contains.</span></span> <span data-ttu-id="2c1ba-131">[Oder](or.md) gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-131">[Or](or.md) will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c1ba-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c1ba-132">Remarks</span></span>

<span data-ttu-id="2c1ba-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c1ba-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2c1ba-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c1ba-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c1ba-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c1ba-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2c1ba-136">Schema Name</span></span>  <br/> |<span data-ttu-id="2c1ba-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2c1ba-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="2c1ba-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2c1ba-138">Validation File</span></span>  <br/> |<span data-ttu-id="2c1ba-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2c1ba-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c1ba-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2c1ba-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="2c1ba-141">False</span><span class="sxs-lookup"><span data-stu-id="2c1ba-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c1ba-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c1ba-142">See also</span></span>



- [<span data-ttu-id="2c1ba-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2c1ba-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

