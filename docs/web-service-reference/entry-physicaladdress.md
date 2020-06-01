---
title: Eintrag (PhysicalAddress)
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
description: Das Entry-Element beschreibt eine einzelne physikalische Adresse für ein Kontaktelement.
ms.openlocfilehash: 5e8343e9abebeeff8c2b81327b2e0f4ddcf45364
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459630"
---
# <a name="entry-physicaladdress"></a><span data-ttu-id="bfc35-103">Eintrag (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="bfc35-103">Entry (PhysicalAddress)</span></span>

<span data-ttu-id="bfc35-104">Das **Entry** -Element beschreibt eine einzelne physikalische Adresse für ein Kontaktelement.</span><span class="sxs-lookup"><span data-stu-id="bfc35-104">The **Entry** element describes a single physical address for a contact item.</span></span> 
  
```xml
<Entry Key="">
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
</Entry>
```

 <span data-ttu-id="bfc35-105">**PhysicalAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="bfc35-105">**PhysicalAddressDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bfc35-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bfc35-106">Attributes and elements</span></span>

<span data-ttu-id="bfc35-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bfc35-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bfc35-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bfc35-108">Attributes</span></span>

|<span data-ttu-id="bfc35-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bfc35-109">**Attribute**</span></span>|<span data-ttu-id="bfc35-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfc35-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfc35-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="bfc35-111">**Key**</span></span> <br/> | <span data-ttu-id="bfc35-112">Identifiziert eine physikalische Adresse.</span><span class="sxs-lookup"><span data-stu-id="bfc35-112">Identifies a physical address.</span></span><br/><br/> <span data-ttu-id="bfc35-113">Es folgen die möglichen Werte für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="bfc35-113">The following are the possible values for this attribute:</span></span><br/>  <br/><span data-ttu-id="bfc35-114">-Business</span><span class="sxs-lookup"><span data-stu-id="bfc35-114">-  Business</span></span>  <br/><span data-ttu-id="bfc35-115">-Startseite</span><span class="sxs-lookup"><span data-stu-id="bfc35-115">-  Home</span></span>  <br/><span data-ttu-id="bfc35-116">-Sonstiges</span><span class="sxs-lookup"><span data-stu-id="bfc35-116">-  Other</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bfc35-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfc35-117">Child elements</span></span>

|<span data-ttu-id="bfc35-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="bfc35-118">**Element**</span></span>|<span data-ttu-id="bfc35-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfc35-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfc35-120">Straße</span><span class="sxs-lookup"><span data-stu-id="bfc35-120">Street</span></span>](street.md) <br/> |<span data-ttu-id="bfc35-121">Stellt eine Straßenadresse für ein Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="bfc35-121">Represents a street address for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="bfc35-122">City</span><span class="sxs-lookup"><span data-stu-id="bfc35-122">City</span></span>](city.md) <br/> |<span data-ttu-id="bfc35-123">Stellt den Namen der Stadt dar, die einem Kontakt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bfc35-123">Represents the city name that is associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="bfc35-124">State</span><span class="sxs-lookup"><span data-stu-id="bfc35-124">State</span></span>](state-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bfc35-125">Stellt den Wohnsitzstatus für ein Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="bfc35-125">Represents the state of residence for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="bfc35-126">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="bfc35-126">CountryOrRegion</span></span>](countryorregion.md) <br/> |<span data-ttu-id="bfc35-127">Stellt das Land oder die Region für eine bestimmte physikalische Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="bfc35-127">Represents the country or region for a given physical address.</span></span>  <br/> |
|[<span data-ttu-id="bfc35-128">PostalCode</span><span class="sxs-lookup"><span data-stu-id="bfc35-128">PostalCode</span></span>](postalcode.md) <br/> |<span data-ttu-id="bfc35-129">Stellt die Postleitzahl für ein Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="bfc35-129">Represents the postal code for a contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bfc35-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfc35-130">Parent elements</span></span>

|<span data-ttu-id="bfc35-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="bfc35-131">**Element**</span></span>|<span data-ttu-id="bfc35-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfc35-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfc35-133">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="bfc35-133">PhysicalAddresses</span></span>](physicaladdresses.md) <br/> |<span data-ttu-id="bfc35-134">Enthält eine Auflistung von physikalischen Adressen, die einem Kontakt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bfc35-134">Contains a collection of physical addresses that are associated with a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfc35-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfc35-135">Remarks</span></span>

<span data-ttu-id="bfc35-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bfc35-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bfc35-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bfc35-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bfc35-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="bfc35-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bfc35-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bfc35-139">Schema Name</span></span>  <br/> |<span data-ttu-id="bfc35-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bfc35-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="bfc35-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bfc35-141">Validation File</span></span>  <br/> |<span data-ttu-id="bfc35-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bfc35-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bfc35-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bfc35-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="bfc35-144">False</span><span class="sxs-lookup"><span data-stu-id="bfc35-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bfc35-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfc35-145">See also</span></span>

- [<span data-ttu-id="bfc35-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bfc35-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="bfc35-147">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="bfc35-147">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="bfc35-148">Aktualisieren von Kontakten</span><span class="sxs-lookup"><span data-stu-id="bfc35-148">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="bfc35-149">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="bfc35-149">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

