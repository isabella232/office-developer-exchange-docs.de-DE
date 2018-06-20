---
title: RecurringMasterItemId (ItemIdType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: Das RecurringMasterItemId (ItemIdType)-Element identifiziert ein Master-Shape Recurrence-Element durch das Identifizieren von Bezeichner eines seiner Elemente verwandte vorkommen.
ms.openlocfilehash: 89089067963e99ac1a6cae6ea6e1e8350d148e82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831010"
---
# <a name="recurringmasteritemid-itemidtype"></a><span data-ttu-id="9130f-103">RecurringMasterItemId (ItemIdType)</span><span class="sxs-lookup"><span data-stu-id="9130f-103">RecurringMasterItemId (ItemIdType)</span></span>

<span data-ttu-id="9130f-104">Das **RecurringMasterItemId (ItemIdType)** -Element identifiziert ein Master-Shape Recurrence-Element durch das Identifizieren von Bezeichner eines seiner Elemente verwandte vorkommen.</span><span class="sxs-lookup"><span data-stu-id="9130f-104">The **RecurringMasterItemId (ItemIdType)** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items.</span></span> 
  
```XML
<RecurringMasterItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="9130f-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="9130f-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9130f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9130f-106">Attributes and elements</span></span>

<span data-ttu-id="9130f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9130f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9130f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9130f-108">Attributes</span></span>

****

|<span data-ttu-id="9130f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9130f-109">**Attribute**</span></span>|<span data-ttu-id="9130f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9130f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9130f-111">Id</span><span class="sxs-lookup"><span data-stu-id="9130f-111">Id</span></span>  <br/> |<span data-ttu-id="9130f-112">Gibt ein einzelnes Vorkommen des ein wiederkehrendes master-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9130f-112">Identifies a single occurrence of a recurring master item.</span></span> <span data-ttu-id="9130f-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9130f-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="9130f-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="9130f-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="9130f-115">Identifiziert eine bestimmte Version für ein einzelnes Auftreten eines sich wiederholenden master-Elements an.</span><span class="sxs-lookup"><span data-stu-id="9130f-115">Identifies a specific version of a single occurrence of a recurring master item.</span></span> <span data-ttu-id="9130f-116">Darüber hinaus wird wiederkehrenden master-Objekts auch identifiziert, da es und die einzelnen Vorkommen der gleichen Änderungsschlüssel enthalten.</span><span class="sxs-lookup"><span data-stu-id="9130f-116">Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key.</span></span> <span data-ttu-id="9130f-117">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="9130f-117">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9130f-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9130f-118">Child elements</span></span>

<span data-ttu-id="9130f-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="9130f-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9130f-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9130f-120">Parent elements</span></span>

[<span data-ttu-id="9130f-121">Reminder</span><span class="sxs-lookup"><span data-stu-id="9130f-121">Reminder</span></span>](reminder.md)
  
## <a name="remarks"></a><span data-ttu-id="9130f-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9130f-122">Remarks</span></span>

<span data-ttu-id="9130f-123">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9130f-123">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="9130f-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9130f-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9130f-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9130f-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9130f-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="9130f-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9130f-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9130f-127">Schema Name</span></span>  <br/> |<span data-ttu-id="9130f-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9130f-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="9130f-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9130f-129">Validation File</span></span>  <br/> |<span data-ttu-id="9130f-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9130f-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9130f-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9130f-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="9130f-132">True</span><span class="sxs-lookup"><span data-stu-id="9130f-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9130f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9130f-133">See also</span></span>



[<span data-ttu-id="9130f-134">Reminder</span><span class="sxs-lookup"><span data-stu-id="9130f-134">Reminder</span></span>](reminder.md)


- [<span data-ttu-id="9130f-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9130f-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

