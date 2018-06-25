---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: Das EmailAddressAttributedValue-Element gibt eine Instanz des ein Array von e-Mail-Adressen und deren zugeordneten Hinweise.
ms.openlocfilehash: 3bcbb5c0a2bc9a2dc24516b5fc62e6e3363a360b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758175"
---
# <a name="emailaddressattributedvalue"></a><span data-ttu-id="a13c8-103">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="a13c8-103">EmailAddressAttributedValue</span></span>

<span data-ttu-id="a13c8-104">Das **EmailAddressAttributedValue** -Element gibt eine Instanz des ein Array von e-Mail-Adressen und deren zugeordneten Hinweise.</span><span class="sxs-lookup"><span data-stu-id="a13c8-104">The **EmailAddressAttributedValue** element specifies an instance of an array of email addresses and their associated attributions.</span></span> 
  
```XML
<EmailAddressAttributedValue>
    <Value></Value>
    <Attributions></Attributions>
<EmailAddressAttributedValue>
```

 <span data-ttu-id="a13c8-105">**EmailAddressAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="a13c8-105">**EmailAddressAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a13c8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a13c8-106">Attributes and elements</span></span>

<span data-ttu-id="a13c8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a13c8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a13c8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a13c8-108">Attributes</span></span>

<span data-ttu-id="a13c8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a13c8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a13c8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a13c8-110">Child elements</span></span>

|<span data-ttu-id="a13c8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a13c8-111">**Element**</span></span>|<span data-ttu-id="a13c8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a13c8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a13c8-113">Wert (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="a13c8-113">Value (EmailAddressType)</span></span>](value-emailaddresstype.md) <br/> |<span data-ttu-id="a13c8-114">Gibt an, dass ein Array Marken der Wert der ein **EmailAddress** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a13c8-114">Specifies the value of an **EmailAddress** associated with an attributions array.</span></span>  <br/> |
|[<span data-ttu-id="a13c8-115">Hinweise (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="a13c8-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="a13c8-116">Gibt ein Array von Marken für zugeordneten **Wert** Elements an.</span><span class="sxs-lookup"><span data-stu-id="a13c8-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a13c8-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a13c8-117">Parent elements</span></span>

|<span data-ttu-id="a13c8-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="a13c8-118">**Element**</span></span>|<span data-ttu-id="a13c8-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a13c8-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a13c8-120">Emails1</span><span class="sxs-lookup"><span data-stu-id="a13c8-120">Emails1</span></span>](emails1.md) <br/> |<span data-ttu-id="a13c8-121">Gibt ein Array von Werten für e-Mail und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="a13c8-121">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
|[<span data-ttu-id="a13c8-122">Emails2</span><span class="sxs-lookup"><span data-stu-id="a13c8-122">Emails2</span></span>](emails2.md) <br/> |<span data-ttu-id="a13c8-123">Gibt ein Array von Werten für e-Mail und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="a13c8-123">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
|[<span data-ttu-id="a13c8-124">Emails3</span><span class="sxs-lookup"><span data-stu-id="a13c8-124">Emails3</span></span>](emails3.md) <br/> |<span data-ttu-id="a13c8-125">Gibt ein Array von Werten für e-Mail und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="a13c8-125">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a13c8-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a13c8-126">Remarks</span></span>

<span data-ttu-id="a13c8-127">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a13c8-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a13c8-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a13c8-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a13c8-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a13c8-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a13c8-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a13c8-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a13c8-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a13c8-131">Schema Name</span></span>  <br/> |<span data-ttu-id="a13c8-132">Typschema</span><span class="sxs-lookup"><span data-stu-id="a13c8-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="a13c8-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a13c8-133">Validation File</span></span>  <br/> |<span data-ttu-id="a13c8-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a13c8-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a13c8-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a13c8-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a13c8-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a13c8-136">See also</span></span>



- [<span data-ttu-id="a13c8-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a13c8-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

