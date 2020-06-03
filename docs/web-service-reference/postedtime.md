---
title: Gebucht
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostedTime
api_type:
- schema
ms.assetid: e8b3813c-fc7e-4674-a4c6-6818c13d2bcf
description: Das gebuchte Time-Element stellt die Uhrzeit dar, zu der ein PostItem-Element bereitgestellt wurde. Dieses Element ist schreibgeschützt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 5fc670bfee97a46700bc4442d489696a4489f88a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459195"
---
# <a name="postedtime"></a><span data-ttu-id="1674d-105">Gebucht</span><span class="sxs-lookup"><span data-stu-id="1674d-105">PostedTime</span></span>

<span data-ttu-id="1674d-106">Das **gebuchte** Time-Element stellt die Uhrzeit dar, zu der ein [PostItem](postitem.md) -Element bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1674d-106">The **PostedTime** element represents the time at which a [PostItem](postitem.md) was posted.</span></span> <span data-ttu-id="1674d-107">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1674d-107">This element is read-only.</span></span> <span data-ttu-id="1674d-108">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1674d-108">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<PostedTime/>
```

 <span data-ttu-id="1674d-109">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="1674d-109">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1674d-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1674d-110">Attributes and elements</span></span>

<span data-ttu-id="1674d-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1674d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1674d-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="1674d-112">Attributes</span></span>

<span data-ttu-id="1674d-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1674d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1674d-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1674d-114">Child elements</span></span>

<span data-ttu-id="1674d-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="1674d-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1674d-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1674d-116">Parent elements</span></span>

|<span data-ttu-id="1674d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1674d-117">**Element**</span></span>|<span data-ttu-id="1674d-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1674d-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1674d-119">PostItem</span><span class="sxs-lookup"><span data-stu-id="1674d-119">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="1674d-120">Stellt ein PostItem im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="1674d-120">Represents a PostItem in the Exchange store.</span></span> <span data-ttu-id="1674d-121">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1674d-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1674d-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="1674d-122">Text value</span></span>

<span data-ttu-id="1674d-123">Der Textwert ist ein DateTime-Wert, der darstellt, wann ein **PostItem** gepostet wurde.</span><span class="sxs-lookup"><span data-stu-id="1674d-123">The text value is a dateTime that represents when a **PostItem** was posted.</span></span> <span data-ttu-id="1674d-124">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1674d-124">This property is read-only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1674d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1674d-125">Remarks</span></span>

<span data-ttu-id="1674d-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1674d-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1674d-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1674d-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1674d-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="1674d-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1674d-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1674d-129">Schema Name</span></span>  <br/> |<span data-ttu-id="1674d-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1674d-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="1674d-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1674d-131">Validation File</span></span>  <br/> |<span data-ttu-id="1674d-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1674d-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1674d-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1674d-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="1674d-134">False</span><span class="sxs-lookup"><span data-stu-id="1674d-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1674d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1674d-135">See also</span></span>



- [<span data-ttu-id="1674d-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1674d-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

