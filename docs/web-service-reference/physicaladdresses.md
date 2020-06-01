---
title: PhysicalAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhysicalAddresses
api_type:
- schema
ms.assetid: 5276c5f2-9e08-43af-a0b2-da4ff1dcae2d
description: Das PhysicalAddresses-Element enthält eine Auflistung von physikalischen Adressen, die einem Kontakt zugeordnet sind.
ms.openlocfilehash: b609abed481359fa6562f41a551645eb613ddfa0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468880"
---
# <a name="physicaladdresses"></a><span data-ttu-id="e29ae-103">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="e29ae-103">PhysicalAddresses</span></span>

<span data-ttu-id="e29ae-104">Das **PhysicalAddresses** -Element enthält eine Auflistung von physikalischen Adressen, die einem Kontakt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e29ae-104">The **PhysicalAddresses** element contains a collection of physical addresses that are associated with a contact.</span></span> 
  
```xml
<PhysicalAddresses>
   <Entry/>
</PhysicalAddresses>
```

 <span data-ttu-id="e29ae-105">**PhysicalAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="e29ae-105">**PhysicalAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e29ae-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e29ae-106">Attributes and elements</span></span>

<span data-ttu-id="e29ae-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e29ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e29ae-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e29ae-108">Attributes</span></span>

<span data-ttu-id="e29ae-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e29ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e29ae-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e29ae-110">Child elements</span></span>

|<span data-ttu-id="e29ae-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e29ae-111">**Element**</span></span>|<span data-ttu-id="e29ae-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e29ae-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e29ae-113">Eintrag (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="e29ae-113">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md) <br/> |<span data-ttu-id="e29ae-114">Beschreibt eine einzelne physische Adresse für ein Kontaktelement.</span><span class="sxs-lookup"><span data-stu-id="e29ae-114">Describes a single physical address for a contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e29ae-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e29ae-115">Parent elements</span></span>

|<span data-ttu-id="e29ae-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e29ae-116">**Element**</span></span>|<span data-ttu-id="e29ae-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e29ae-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e29ae-118">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="e29ae-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="e29ae-119">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="e29ae-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e29ae-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e29ae-120">Remarks</span></span>

<span data-ttu-id="e29ae-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e29ae-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e29ae-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e29ae-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e29ae-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e29ae-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e29ae-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e29ae-124">Schema name</span></span>  <br/> |<span data-ttu-id="e29ae-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e29ae-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="e29ae-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e29ae-126">Validation file</span></span>  <br/> |<span data-ttu-id="e29ae-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e29ae-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e29ae-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e29ae-128">Can be empty</span></span>  <br/> |<span data-ttu-id="e29ae-129">False</span><span class="sxs-lookup"><span data-stu-id="e29ae-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e29ae-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e29ae-130">See also</span></span>



- [<span data-ttu-id="e29ae-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e29ae-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="e29ae-132">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="e29ae-132">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="e29ae-133">Aktualisieren von Kontakten</span><span class="sxs-lookup"><span data-stu-id="e29ae-133">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="e29ae-134">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="e29ae-134">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

