---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: Das EmailAddressAttributedValue-Element gibt eine Instanz eines Arrays von e-Mail-Adressen und deren zugeordneten Zuschreibungen an.
ms.openlocfilehash: 09fdd5921cef3d70a6da4b6d4d38f08834c5d482
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530691"
---
# <a name="emailaddressattributedvalue"></a><span data-ttu-id="e204d-103">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="e204d-103">EmailAddressAttributedValue</span></span>

<span data-ttu-id="e204d-104">Das **EmailAddressAttributedValue** -Element gibt eine Instanz eines Arrays von e-Mail-Adressen und deren zugeordneten Zuschreibungen an.</span><span class="sxs-lookup"><span data-stu-id="e204d-104">The **EmailAddressAttributedValue** element specifies an instance of an array of email addresses and their associated attributions.</span></span> 
  
```XML
<EmailAddressAttributedValue>
    <Value></Value>
    <Attributions></Attributions>
<EmailAddressAttributedValue>
```

 <span data-ttu-id="e204d-105">**EmailAddressAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="e204d-105">**EmailAddressAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e204d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e204d-106">Attributes and elements</span></span>

<span data-ttu-id="e204d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e204d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e204d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e204d-108">Attributes</span></span>

<span data-ttu-id="e204d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e204d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e204d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e204d-110">Child elements</span></span>

|<span data-ttu-id="e204d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e204d-111">**Element**</span></span>|<span data-ttu-id="e204d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e204d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e204d-113">Wert (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="e204d-113">Value (EmailAddressType)</span></span>](value-emailaddresstype.md) <br/> |<span data-ttu-id="e204d-114">Gibt den Wert einer e- **mailemail** an, die einem attributes-Array zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e204d-114">Specifies the value of an **EmailAddress** associated with an attributions array.</span></span>  <br/> |
|[<span data-ttu-id="e204d-115">Zuordnungen (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="e204d-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="e204d-116">Gibt ein Array von Attributes für das zugehörige **value** -Element an.</span><span class="sxs-lookup"><span data-stu-id="e204d-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e204d-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e204d-117">Parent elements</span></span>

|<span data-ttu-id="e204d-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="e204d-118">**Element**</span></span>|<span data-ttu-id="e204d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e204d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e204d-120">Emails1</span><span class="sxs-lookup"><span data-stu-id="e204d-120">Emails1</span></span>](emails1.md) <br/> |<span data-ttu-id="e204d-121">Gibt ein Array von e-Mail-Werten und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.</span><span class="sxs-lookup"><span data-stu-id="e204d-121">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
|[<span data-ttu-id="e204d-122">Emails2</span><span class="sxs-lookup"><span data-stu-id="e204d-122">Emails2</span></span>](emails2.md) <br/> |<span data-ttu-id="e204d-123">Gibt ein Array von e-Mail-Werten und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.</span><span class="sxs-lookup"><span data-stu-id="e204d-123">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
|[<span data-ttu-id="e204d-124">Emails3</span><span class="sxs-lookup"><span data-stu-id="e204d-124">Emails3</span></span>](emails3.md) <br/> |<span data-ttu-id="e204d-125">Gibt ein Array von e-Mail-Werten und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.</span><span class="sxs-lookup"><span data-stu-id="e204d-125">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e204d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e204d-126">Remarks</span></span>

<span data-ttu-id="e204d-127">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e204d-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e204d-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e204d-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e204d-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e204d-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e204d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e204d-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e204d-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e204d-131">Schema Name</span></span>  <br/> |<span data-ttu-id="e204d-132">Typschema</span><span class="sxs-lookup"><span data-stu-id="e204d-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="e204d-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e204d-133">Validation File</span></span>  <br/> |<span data-ttu-id="e204d-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e204d-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e204d-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e204d-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e204d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e204d-136">See also</span></span>



- [<span data-ttu-id="e204d-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e204d-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

