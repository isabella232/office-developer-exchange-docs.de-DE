---
title: Eintrag (physikalische Adresse)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: 9e5b6515-453e-4f4c-b55e-6ffefe23c31b
description: Entry-Element wird eine einzelne physische Adresse für ein Kontaktelement beschrieben.
ms.openlocfilehash: 4551e6117e5f91d901fe160f37e8f67cb1bc5ac7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758253"
---
# <a name="entry-physicaladdress"></a><span data-ttu-id="27f89-103">Eintrag (physikalische Adresse)</span><span class="sxs-lookup"><span data-stu-id="27f89-103">Entry (PhysicalAddress)</span></span>

<span data-ttu-id="27f89-104">**Entry** -Element wird eine einzelne physische Adresse für ein Kontaktelement beschrieben.</span><span class="sxs-lookup"><span data-stu-id="27f89-104">The **Entry** element describes a single physical address for a contact item.</span></span> 
  
```xml
<Entry Key="">
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
</Entry>
```

 <span data-ttu-id="27f89-105">**PhysicalAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="27f89-105">**PhysicalAddressDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27f89-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="27f89-106">Attributes and elements</span></span>

<span data-ttu-id="27f89-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="27f89-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27f89-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="27f89-108">Attributes</span></span>

|<span data-ttu-id="27f89-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="27f89-109">**Attribute**</span></span>|<span data-ttu-id="27f89-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27f89-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27f89-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="27f89-111">**Key**</span></span> <br/> | <span data-ttu-id="27f89-112">Eine physische Adresse identifiziert.</span><span class="sxs-lookup"><span data-stu-id="27f89-112">Identifies a physical address.</span></span><br/><br/> <span data-ttu-id="27f89-113">Es folgen die möglichen Werte für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="27f89-113">The following are the possible values for this attribute:</span></span><br/>  <br/><span data-ttu-id="27f89-114">-Business</span><span class="sxs-lookup"><span data-stu-id="27f89-114">-  Business</span></span>  <br/><span data-ttu-id="27f89-115">-Startseite</span><span class="sxs-lookup"><span data-stu-id="27f89-115">-  Home</span></span>  <br/><span data-ttu-id="27f89-116">-Andere</span><span class="sxs-lookup"><span data-stu-id="27f89-116">-  Other</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="27f89-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27f89-117">Child elements</span></span>

|<span data-ttu-id="27f89-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="27f89-118">**Element**</span></span>|<span data-ttu-id="27f89-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27f89-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27f89-120">Straße</span><span class="sxs-lookup"><span data-stu-id="27f89-120">Street</span></span>](street.md) <br/> |<span data-ttu-id="27f89-121">Stellt eine Adresse für ein Kontaktelement.</span><span class="sxs-lookup"><span data-stu-id="27f89-121">Represents a street address for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="27f89-122">City</span><span class="sxs-lookup"><span data-stu-id="27f89-122">City</span></span>](city.md) <br/> |<span data-ttu-id="27f89-123">Stellt den Namen der Stadt, der einem Kontakt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="27f89-123">Represents the city name that is associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="27f89-124">State</span><span class="sxs-lookup"><span data-stu-id="27f89-124">State</span></span>](state-ex15websvcsotherref.md) <br/> |<span data-ttu-id="27f89-125">Stellt den Zustand des US-Bundesstaates, ein Kontaktelement.</span><span class="sxs-lookup"><span data-stu-id="27f89-125">Represents the state of residence for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="27f89-126">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="27f89-126">CountryOrRegion</span></span>](countryorregion.md) <br/> |<span data-ttu-id="27f89-127">Stellt das Land oder die Region für eine bestimmte physische Adresse.</span><span class="sxs-lookup"><span data-stu-id="27f89-127">Represents the country or region for a given physical address.</span></span>  <br/> |
|[<span data-ttu-id="27f89-128">PostalCode</span><span class="sxs-lookup"><span data-stu-id="27f89-128">PostalCode</span></span>](postalcode.md) <br/> |<span data-ttu-id="27f89-129">Stellt die Postleitzahl für ein Kontaktelement.</span><span class="sxs-lookup"><span data-stu-id="27f89-129">Represents the postal code for a contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="27f89-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27f89-130">Parent elements</span></span>

|<span data-ttu-id="27f89-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="27f89-131">**Element**</span></span>|<span data-ttu-id="27f89-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27f89-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27f89-133">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="27f89-133">PhysicalAddresses</span></span>](physicaladdresses.md) <br/> |<span data-ttu-id="27f89-134">Enthält eine Auflistung von physischen Adressen, die mit einem Kontakt verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="27f89-134">Contains a collection of physical addresses that are associated with a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27f89-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="27f89-135">Remarks</span></span>

<span data-ttu-id="27f89-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="27f89-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27f89-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="27f89-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27f89-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="27f89-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27f89-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="27f89-139">Schema Name</span></span>  <br/> |<span data-ttu-id="27f89-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="27f89-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="27f89-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="27f89-141">Validation File</span></span>  <br/> |<span data-ttu-id="27f89-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="27f89-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="27f89-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="27f89-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="27f89-144">False</span><span class="sxs-lookup"><span data-stu-id="27f89-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27f89-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27f89-145">See also</span></span>

- [<span data-ttu-id="27f89-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="27f89-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="27f89-147">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="27f89-147">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="27f89-148">Aktualisierung von Kontakten</span><span class="sxs-lookup"><span data-stu-id="27f89-148">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="27f89-149">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="27f89-149">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

