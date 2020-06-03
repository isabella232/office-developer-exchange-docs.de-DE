---
title: RecurringMasterItemId (itemidtype)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: Das RecurringMasterItemId (itemidtype)-Element identifiziert ein Serienmasterelement durch Identifizieren der Bezeichner eines seiner Verwandten vorkommen Elemente.
ms.openlocfilehash: c725998ad3a728ef1f47ff6491592b461753b895
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468439"
---
# <a name="recurringmasteritemid-itemidtype"></a><span data-ttu-id="636e7-103">RecurringMasterItemId (itemidtype)</span><span class="sxs-lookup"><span data-stu-id="636e7-103">RecurringMasterItemId (ItemIdType)</span></span>

<span data-ttu-id="636e7-104">Das **RecurringMasterItemId (itemidtype)-** Element identifiziert ein Serienmasterelement durch Identifizieren der Bezeichner eines seiner Verwandten vorkommen Elemente.</span><span class="sxs-lookup"><span data-stu-id="636e7-104">The **RecurringMasterItemId (ItemIdType)** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items.</span></span> 
  
```XML
<RecurringMasterItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="636e7-105">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="636e7-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="636e7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="636e7-106">Attributes and elements</span></span>

<span data-ttu-id="636e7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="636e7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="636e7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="636e7-108">Attributes</span></span>

****

|<span data-ttu-id="636e7-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="636e7-109">**Attribute**</span></span>|<span data-ttu-id="636e7-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="636e7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="636e7-111">Id</span><span class="sxs-lookup"><span data-stu-id="636e7-111">Id</span></span>  <br/> |<span data-ttu-id="636e7-112">Gibt ein einzelnes Vorkommen eines wiederkehrenden Hauptelements an.</span><span class="sxs-lookup"><span data-stu-id="636e7-112">Identifies a single occurrence of a recurring master item.</span></span> <span data-ttu-id="636e7-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="636e7-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="636e7-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="636e7-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="636e7-115">Gibt eine bestimmte Version eines einzelnen Auftretens eines wiederkehrenden Hauptelements an.</span><span class="sxs-lookup"><span data-stu-id="636e7-115">Identifies a specific version of a single occurrence of a recurring master item.</span></span> <span data-ttu-id="636e7-116">Darüber hinaus wird das wiederkehrende Hauptelement ebenfalls identifiziert, da es und das einzelne Vorkommen denselben Änderungsschlüssel enthalten werden.</span><span class="sxs-lookup"><span data-stu-id="636e7-116">Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key.</span></span> <span data-ttu-id="636e7-117">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="636e7-117">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="636e7-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="636e7-118">Child elements</span></span>

<span data-ttu-id="636e7-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="636e7-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="636e7-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="636e7-120">Parent elements</span></span>

[<span data-ttu-id="636e7-121">Reminder</span><span class="sxs-lookup"><span data-stu-id="636e7-121">Reminder</span></span>](reminder.md)
  
## <a name="remarks"></a><span data-ttu-id="636e7-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="636e7-122">Remarks</span></span>

<span data-ttu-id="636e7-123">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="636e7-123">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="636e7-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="636e7-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="636e7-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="636e7-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="636e7-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="636e7-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="636e7-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="636e7-127">Schema Name</span></span>  <br/> |<span data-ttu-id="636e7-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="636e7-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="636e7-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="636e7-129">Validation File</span></span>  <br/> |<span data-ttu-id="636e7-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="636e7-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="636e7-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="636e7-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="636e7-132">True</span><span class="sxs-lookup"><span data-stu-id="636e7-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="636e7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="636e7-133">See also</span></span>



[<span data-ttu-id="636e7-134">Reminder</span><span class="sxs-lookup"><span data-stu-id="636e7-134">Reminder</span></span>](reminder.md)


- [<span data-ttu-id="636e7-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="636e7-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

